---
title: Overzicht persoonlijke productaanbevelingen
description: "In Dynamics 365 for Operations kunnen productaanbevelingen op het POS-apparaat (Point of Sale) worden weergegeven. Aanbevelingen zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht. Voor detailhandelaren met grote catalogi helpen aanbevelingen de klant producten te ontdekken. Door producten te belichten die zijn gericht op de interesses van een klant en diens koopgewoontes, kunnen productaanbevelingen detailhandelaren helpen met bij- en meerverkoop en klantenbinding. Productaanbevelingen worden in Dynamics 365 for Operations aangestuurd door cognitieve services en Microsoft Azure Machine Learning."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Overzicht persoonlijke productaanbevelingen

[!include[banner](includes/banner.md)]


In Dynamics 365 for Operations kunnen productaanbevelingen op het POS-apparaat (Point of Sale) worden weergegeven. Aanbevelingen zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht. Voor detailhandelaren met grote catalogi helpen aanbevelingen de klant producten te ontdekken. Door producten te belichten die zijn gericht op de interesses van een klant en diens koopgewoontes, kunnen productaanbevelingen detailhandelaren helpen met bij- en meerverkoop en klantenbinding. Productaanbevelingen worden in Dynamics 365 for Operations aangestuurd door cognitieve services en Microsoft Azure Machine Learning.

<a name="scenarios"></a>Scenario's
---------

Productaanbevelingen zijn ingeschakeld voor de volgende POS-scenario's. Ze zijn beschikbaar in de cloud-POS of Modern POS (MPOS).

1.  Op de pagina **Productdetails**:

-   Als een winkelmedewerker een **productdetails**-pagina bezoekt wanneer hij eerdere transacties uit verschillende kanalen bekijkt, stelt de aanbevelingsengine extra artikelen voor die waarschijnlijk samen worden gekocht.
-   Als de winkelmedewerker een klant aan de transactie toevoegt en vervolgens een **productdetails**-pagina bezoekt, geeft de aanbevelingsengine persoonlijke aanbevelingen op basis van de transactiehistorie van de klant.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Op de pagina **Transactie**:

-   De aanbevelingsengine stelt artikelen voor op basis van de volledige lijst met artikelen in het winkelmandje.
-   Als de winkelmedewerker een klant aan de transactie toevoegt, geeft de aanbevelingsengine persoonlijke aanbevelingen op basis van de transactiehistorie van de klant en de lijst met artikelen in het winkelmandje.

**Opmerking**: Om aanbevelingen te laten weergeven op de pagina **Transactie**, moet de detailhandelaar de schermindeling in Dynamics 365 for Operations bijwerken. Het besturingselement **Aanbevelingen** moet aan de pagina **Transactie** worden toegevoegd. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Op de pagina **Details klant**:
    -   De aanbevelingsengine stelt artikelen voor op basis van de gebruikers-id en de artikelen op het wensenlijstje van de klant.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Dynamics 365 for Operations configureren voor POS-aanbevelingen
Ga als volgt te werk om productaanbevelingen te configureren:

1.  Controleer of u de juiste **rechtspersoon** hebt geselecteerd.
2.  Ga naar **Entiteitopslag**, selecteer **Detailhandelverkoop** en klik op **Vernieuwen**.** **Hierdoor worden de demonstratiegegevens (of uw gegevens) uit uw operationele database gebruikt en verplaatst naar de entiteitopslag.
3.  Optioneel: Om aanbevelingen op het transactiescherm te laten weergeven, gaat u naar **Schermindeling, **kiest u de schermindeling, start u de **Ontwerper van schermindeling**,** **en zet u het besturingselement Aanbevelingen **daar neer waar u het hebben wilt.
4.  Ga naar **Detailhandelparameters**, selecteer **Machine Learning**, selecteer **Ja **onder **POS-aanbevelingen inschakelen**.
5.  Als u aanbevelingen op POS wilt zien, voert u algemene-configuratietaak **1110** uit. Om wijzigingen in de ontwerper van de POS-schermindeling door te voeren, voert u afzetkanaalconfiguratietaak **1070** uit.

## <a name="how-does-it-work"></a>[]()Hoe functioneert dit?
Wanneer u de **entiteitsopslag** vernieuwt, worden de volgende acties uitgevoerd.

-   Gegevens in de door Cognitieve services vereiste indeling worden opgehaald uit de operationele database Dynamics 365 for Operations en naar de entiteitsopslag gezonden.
-   De gegevens worden gebruikt door Azure Data Factory (ADF) om de gegevens om de gegevens op te schonen, door middel van Hive-scripts in het kader van de ADF-activiteiten. Opgeschoonde gegevens worden opgeslagen in de blob-opslag.
-   Gegevens uit de blob-opslag worden gebruikt door de API voor cognitieve services om een aanbevelingsmodel te trainen.

Wanneer u **Aanbevelingen inschakelen** activeert en de configuratietaken uitvoert, worde de volgende acties uitgevoerd.

-   Modelreferenties en een model-id worden opgehaald in de API en opgeslagen in de operationele database van Dynamics 365 for Operations, in het bestand web.config voor AOS en ook in de detailhandelserver.
-   Modelreferenties en de model-id worden beschikbaar gesteld aan CRT, zodat aanroepen voor productaanbevelingen vanuit de cloud-POS en MPOS in de online modus kunnen worden gehonoreerd.


<a name="see-also"></a>Zie ook
--------

[Een besturingselement voor aanbevelingen toevoegen aan de transactiepagina op een POS-apparaat](add-recommendations-control-pos-screen.md)




