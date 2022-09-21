---
title: Productaanbevelingen toevoegen op POS
description: Dit artikel beschrijft het gebruik van productaanbevelingen op een POS-apparaat (Point of Sale).
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460051"
---
# <a name="add-product-recommendations-on-pos"></a>Productaanbevelingen toevoegen op POS

[!include [banner](includes/banner.md)]

In feite zijn productaanbevelingen een transformatieve zakelijke toepassing voor alle gebieden van commerce, voor het creëren van uitgebreide, prettige en op maat gemaakte productkennismakingservaringen. Als u deze functie op POS wilt implementeren, volgt u de stappen voor het [toevoegen van aanbevelingen aan uw POS-apparaten.](add-recommendations-control-pos-screen.md) 

Meer informatie over de functies voor productaanbevelingen vindt u in het [overzicht van productaanbevelingen.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenario's

Productaanbevelingen zijn ingeschakeld voor de volgende POS-scenario's. Ze zijn beschikbaar in de cloud-POS of Modern POS (MPOS).

1. Op de pagina **Productdetails**:

    - Als een winkelmedewerker een pagina met **productdetails** bezoekt wanneer hij eerdere transacties via verschillende kanalen bekijkt, worden door de aanbevelingsservice extra artikelen voorgesteld die veelal samen worden gekocht. Afhankelijk van de invoegtoepassingen voor de service kunnen detailhandelaren aanbevelingen voor **Winkelen voor vergelijkbare producten** en **Winkelen voor vergelijkbare omschrijving** tonen voor producten, naast persoonlijke aanbevelingen voor gebruikers die een historie van aankopen hebben.

    [![Aanbevelingen op de pagina Productgegevens.](./media/proddetails.png)](./media/proddetails.png)

2. Op de pagina **Transactie**:

    - De aanbevelingsengine stelt artikelen voor op basis van de volledige lijst met artikelen in de mand die vaak samen worden gekocht.

    > [!NOTE]
    > Om aanbevelingen weer te geven op de pagina **Transactie**, moet de detailhandelaar de schermindeling in Dynamics 365 Commerce bijwerken. Het besturingselement **Aanbevelingen** moet aan de pagina **Transactie** worden toegevoegd.

    [![Aanbevelingen op de pagina Transactie.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commerce configureren om aanbevelingen voor POS in te schakelen 

Om productaanbevelingen in te stellen, bevestigt u dat u het inrichtingsproces voor productaanbevelingen in Commerce hebt voltooid door de stappen in [Productaanbevelingen inschakelen](../commerce/enable-product-recommendations.md) te volgen. Standaard worden aanbevelingen getoond op zowel de pagina **Productdetails** als de pagina **Klantgegevens** nadat u de inrichtingsstappen hebt voltooid en de gegevens met succes zijn verzameld. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Aanbevelingen toevoegen aan het transactiescherm

1. Als u aanbevelingen wilt toevoegen aan het transactiescherm, volgt u de stappen in [Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md).
1. Om wijzigingen weer te geven die zijn aangebracht in de ontwerper van de POS-schermindeling, moet u kanaalconfiguratietaak **1070** in Commerce Headquarters uitvoeren.

> [!NOTE] 
> Als u POS-aanbevelingen wilt inschakelen via het RecoMock csv-bestand (Comma Separated Values), moet u het csv-bestand uitrollen in de Microsoft Dynamics Lifecycle Services (LCS)-activabibliotheek voordat u de indelingsbeheerder configureert. Als u het RecoMock csv-bestand gebruikt, hoeft u aanbevelingen niet in te schakelen. Het csv-bestand is alleen beschikbaar voor demonstratiedoeleinden. Het wordt aangeraden aan klanten of oplossingsarchitecten die het uiterlijk van aanbevelingslijsten willen nadoen ten behoeve van demonstratie, zonder dat een add-on voorraadeenheid (SKU) te moeten kopen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
