---
title: Productaanbevelingen toevoegen op POS
description: Dit onderwerp beschrijft het gebruik van productaanbevelingen op een POS-apparaat (Point of Sale).
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 437913343d16490fd49a458b5c7a17132be293c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230931"
---
# <a name="add-product-recommendations-on-pos"></a>Productaanbevelingen toevoegen op POS

[!include [banner](includes/banner.md)]

In feite zijn productaanbevelingen een transformatieve zakelijke toepassing voor alle gebieden van commerce, voor het creëren van uitgebreide, prettige en op maat gemaakte productkennismakingservaringen. Als u deze functie op POS wilt implementeren, volgt u de stappen voor het [toevoegen van aanbevelingen aan uw POS-apparaten.](add-recommendations-control-pos-screen.md) 

Meer informatie over de functies voor productaanbevelingen vindt u in het [overzicht van productaanbevelingen.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenario's

Productaanbevelingen zijn ingeschakeld voor de volgende POS-scenario's. Ze zijn beschikbaar in de cloud-POS of Modern POS (MPOS).

1. Op de pagina **Productdetails**:

    - Als een winkelmedewerker een pagina met **productdetails** bezoekt wanneer hij eerdere transacties via verschillende kanalen bekijkt, worden door de aanbevelingsservice extra artikelen voorgesteld die veelal samen worden gekocht.

    [![Aanbevelingen op de pagina Productgegevens](./media/proddetails.png)](./media/proddetails.png)

2. Op de pagina **Transactie**:

    - De aanbevelingsengine stelt artikelen voor op basis van de volledige lijst met artikelen in de mand die vaak samen worden gekocht.

    > [!NOTE]
    > Om aanbevelingen weer te geven op de pagina **Transactie**, moet de detailhandelaar de schermindeling in Dynamics 365 Commerce bijwerken. Het besturingselement **Aanbevelingen** moet aan de pagina **Transactie** worden toegevoegd.

    [![Aanbevelingen op de pagina Transactie](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commerce configureren om aanbevelingen voor POS in te schakelen

Volg deze stappen om productaanbevelingen in te stellen:

1. Controleer of de service is bijgewerkt naar **build 10.0.6**.
2. Volg de instructies voor het [inschakelen van productaanbevelingen](../commerce/enable-product-recommendations.md) voor uw bedrijf.
3. Optioneel: als u aanbevelingen in het transactiescherm wilt weergeven, gaat u naar **Schermindeling**, kiest u de schermindeling, start u **Ontwerper van schermindeling** en plaats u het besturingselement **aanbevelingen** op de gewenste locatie.
4. Ga naar **Commerce-parameters**, selecteer **Machine Learning** en selecteer **Ja** onder **POS-aanbevelingen inschakelen**.
5. Als u aanbevelingen op POS wilt zien, voert u algemene-configuratietaak **1110** uit. Om wijzigingen in de ontwerper van de POS-schermindeling door te voeren, voert u afzetkanaalconfiguratietaak **1070** uit.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Problemen oplossen waar u al ingeschakelde productaanbevelingen hebt

- Ga naar **Commerce-parameters** \> **Lijsten met aanbevelingen** \> **Productaanbevelingen uitschakelen** en start **Algemene configuratietaak \[9999\]**. 
- Als u het besturingselement **Aanbevelingen** hebt toegevoegd aan uw transactiescherm met **Ontwerper van schermindeling**, verwijdert u dat ook.
- Als u nog meer vragen hebt, raadpleegt u [Veelgestelde vragen over aanbevelingen](../commerce/faq-recommendations.md) voor meer informatie.

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