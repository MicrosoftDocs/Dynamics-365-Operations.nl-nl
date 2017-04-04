---
title: Persoonlijke aanbevelingen-productoverzicht
description: "In Dynamics 365 voor bewerkingen, kunnen de aanbevelingen op het verkooppunt (POS)-apparaat worden weergegeven. De aanbevelingen zijn artikelen die de klant geïnteresseerd kan zijn op basis van hun inkoophistorie, artikelen in de onderwerpen en artikelen die andere klanten online gekocht en in de markering en fysieke winkels. Voor detailhandelaren met grote catalogi helpen aanbevelingen voor de klant met detectie van product. Laat u kennismaken met producten die zijn gericht aan de interesses van een klant en de kopende achterhalen, aanbevelingen detailhandelaren kunnen helpen met verkoop stimuleren en cross-sell en klantinhouding kunnen verbeteren. In Dynamics 365 voor bewerkingen, worden aanbevelingen aangestuurd door cognitieve services en Microsoft Azure machine leren."
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

# <a name="personalized-product-recommendations-overview"></a>Persoonlijke aanbevelingen-productoverzicht

In Dynamics 365 voor bewerkingen, kunnen de aanbevelingen op het verkooppunt (POS)-apparaat worden weergegeven. De aanbevelingen zijn artikelen die de klant geïnteresseerd kan zijn op basis van hun inkoophistorie, artikelen in de onderwerpen en artikelen die andere klanten online gekocht en in de markering en fysieke winkels. Voor detailhandelaren met grote catalogi helpen aanbevelingen voor de klant met detectie van product. Laat u kennismaken met producten die zijn gericht aan de interesses van een klant en de kopende achterhalen, aanbevelingen detailhandelaren kunnen helpen met verkoop stimuleren en cross-sell en klantinhouding kunnen verbeteren. In Dynamics 365 voor bewerkingen, worden aanbevelingen aangestuurd door cognitieve services en Microsoft Azure machine leren.

<a name="scenarios"></a>Scenario's
---------

Aanbevelingen zijn voor de volgende POS-scenario's ingeschakeld. Ze zijn beschikbaar in de Cloud-POS of moderne POS (MPOS).

1.  Op de **productdetails** pagina:

-   Als een winkel bezoeken koppelt een **productdetails** pagina bij het kijken naar de eerdere transacties via verschillende kanalen de aanbeveling engine stelt voor om extra artikelen die zijn waarschijnlijk samen worden gekocht.
-   Als het koppelen van de winkel een klant aan de transactie toegevoegd en vervolgens bezoeken een **productdetails** pagina, de aanbeveling engine bevat persoonlijke aanbevelingen met behulp van de transactiehistorie van de klant.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Op de **transactie** pagina:

-   De engine aanbeveling stelt voor artikelen op basis van de volledige lijst met artikelen in het winkelmandje.
-   Als de winkel is gekoppeld aan de transactie een klant toegevoegd, de aanbeveling-engine biedt persoonlijke aanbevelingen met behulp van de transactiehistorie van de klant en de lijst met artikelen in het winkelmandje.

**opmerking** aanbevelingen weergeven op de **transactie** pagina, de detailhandelaar moet worden bijgewerkt van de schermindeling in Dynamics 365 voor bewerkingen. De **aanbevelingen** -besturingselement moet worden verwijderd bij de **transactie** pagina. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Op de **details klant** pagina:
    -   De engine aanbeveling stelt voor artikelen op basis van de gebruikers-ID en de items in de onderwerpen van de klant.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Dynamics 365 voor bewerkingen als aanbevelingen POS configureren
Als u aanbevelingen instellen, moet u het volgende doen.

1.  Zorg ervoor dat u hebt geselecteerd de juiste **rechtspersoon**.
2.  Ga naar **entiteit winkel**, selecteer **verkoop detailhandel**, en klik vervolgens op **vernieuwen**. ** ** zo de demonstratiegegevens (of uw gegevens) van uw operationele database gebruiken en verplaats deze naar de winkel entiteit.
3.  Optioneel: Om aanbevelingen op het scherm van de transactie weergeven, gaat u naar ** schermindeling, **de schermindeling kiest, start de **ontwerper van schermindeling**,** ** en zet de ** aanbevelingen control ** waar nodig.
4.  Ga naar **parameters detailhandel**, selecteer **Machine-training**, selecteer ** Ja ** onder **schakelen POS aanbevelingen**.
5.  Aanbevelingen voor POS vindt globale configuratie taak uitvoeren **1110**. Om eventuele wijzigingen in de ontwerper van schermindeling POS, kanaal configuratie taak uitvoeren **1070**.

## <a name="how-does-it-work"></a>[]()Hoe werkt het?
Als u vernieuwt de **entiteit winkel** entiteit, de volgende acties uitgevoerd.

-   Gegevens in de indeling van de cognitieve services is afkomstig uit de Dynamics 365 voor operationeel gegevensbestand als bewerkingen en verzonden naar de winkel entiteit.
-   De gegevens worden door Azure gegevens fabriek (ADF) gebruikt om de gegevens met behulp van component scripts als onderdeel van de activiteiten van de ADF opruimen. Gereinigde gegevens zijn opgeslagen in de blob-opslag.
-   Gegevens uit blob-opslag wordt gebruikt door de cognitieve API-services te trainen een aanbeveling-model.

Wanneer u inschakelt **aanbevelingen** en de configuratie-taken, de volgende acties uitgevoerd.

-   Referenties voor model zijn-ID opgehaald van de API en opgeslagen in de Dynamics 365 voor operationeel gegevensbestand als bewerkingen in het bestand web.config voor AOS en ook in de retail-server.
-   Model referenties en -ID zijn beschikbaar gesteld voor CRT zodat gesprekken voor aanbevelingen uit Cloud-POS en MPOS in de online modus kunnen worden gehonoreerd.


<a name="see-also"></a>Zie ook
--------

[Een besturingselement aanbevelingen toevoegen aan de transactie-pagina op een POS-apparaat](add-recommendations-control-pos-screen.md)


