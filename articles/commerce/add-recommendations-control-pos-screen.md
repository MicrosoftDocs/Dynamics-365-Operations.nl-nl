---
title: Aanbevelingen toevoegen aan het transactiescherm
description: In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af2450b27106325a86f6db68f9791637694cda63
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411261"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Aanbevelingen toevoegen aan het transactiescherm

[!include [banner](includes/banner.md)]


In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 Commerce. Meer informatie over productaanbevelingen vindt u in de [documenten met productaanbevelingen voor POS](product.md).


U kunt productaanbevelingen op uw POS-apparaat weergeven wanneer u Commerce gebruikt. Als u productaanbevelingen wilt weergeven, moet u een besturingselement toevoegen aan het transactiescherm met de schermindelingsontwerper. 

## <a name="open-layout-designer"></a>Indelingsontwerper openen

1. Ga naar **Retail en Commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Schermindelingen**.
2. Met het snelfilter kunt u zoeken naar het scherm waaraan u het besturingselement wilt toevoegen. Filter bijvoorbeeld op het veld **Schermindelings-id** met de waarde **F2CP16:9M**.
3. Zoek en selecteer de gewenste record in de lijst. Selecteer bijvoorbeeld **Naam: F2CP16:9M Schermindelings-ID: F2CP16:9M**.
4. Klik op **Ontwerper van indeling**.
5. Volg de aanwijzingen voor het starten van de indelingsontwerper. Wanneer naar referenties wordt gevraagd, voert u de referenties in die zijn gebruikt bij het starten van de indelingsontwerper op de pagina **Schermindelingen**.
6. Wanneer u zich aanmeldt, wordt er een pagina weergegeven die vergelijkbaar is met de onderstaande pagina. De indeling zal afwijken, afhankelijk van de aanpassingen die voor uw winkel zijn gemaakt.


    [![Ontwerper van indeling](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Een weergaveoptie kiezen

Er zijn twee configuratieopties beschikbaar. Kies de optie die het meest geschikt is voor uw winkel en volg de rest van de instructies om de instelling van het besturingselement te voltooien. De twee opties zijn:

- Aanbevelingen zijn altijd zichtbaar.
- Het tabblad **Aanbevelingen** wordt weergegeven in het raster aan de rechterkant van het scherm.

### <a name="make-recommendations-always-visible"></a>Aanbevelingen altijd zichtbaar maken


1. Verklein de hoogte van het detailgebied van de transactieregels zodat het even hoog is als het deelvenster van de klant aan de linkerkant.


    [![Hoogte van het detailgebied van de transactieregels verlaagd](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Sleep in het menu aan de linkerkant het besturingselement voor aanbevelingen en zet het neer tussen het detailgebied van de transactieregels en het knoppenraster onderaan in het midden van het transactiescherm. Pas de grootte van het besturingselement aan zodat het in die ruimte past.

    [![Het besturings Aanbevelingen is toegevoegd aan de indeling](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.
4. Ga in Commerce naar **Retail en Commerce** &gt; **Retail en Commerce IT** &gt; **Distributieplanningen**.
5. Selecteer **1090, kassa´s** in de lijst.
6. Klik op **Nu uitvoeren**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Het tabblad Aanbevelingen toevoegen aan het knoppenraster aan de rechterkant van het scherm

1. Klik met de rechtermuisknop op de lege ruimte onder het laatste tabblad van het knoppenraster dat zich aan de rechterkant van de pagina bevindt.

2. Klik op **Aanpassen**.

    [![Het dialoogvenster Aanpassing - Tabblad](./media/pic-5.png)](./media/pic-5.png)

3. Klik op **Nieuw tabblad**.
4. Zoek naar het nieuwe tabblad dat u zojuist hebt toegevoegd. Wellicht moet u omlaag bladeren.
5. Selecteer in de vervolgkeuzelijst **Inhoud** **Aanbevolen producten**.

    [![Aanbevolen producten in het veld Inhoud](./media/pic-6.png)](./media/pic-6.png)

6. Typ in het veld **Label** een naam voor het tabblad Aanbevelingen. Typ bijvoorbeeld Aanbevolen producten.
7. Selecteer in het veld **Afbeelding** de afbeelding die op het tabblad moet worden weergegeven.
8. Klik op **OK**. Het nieuwe tabblad wordt weergegeven in het knoppenraster.
9. Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.
10. Ga in Commerce naar **Retail en Commerce** &gt; **Retail en Commerce IT** &gt; **Distributieplanningen**.
11. Selecteer **1090, kassa´s** in de lijst.
12. Klik op **Nu uitvoeren**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Productaanbevelingen op POS toevoegen](product.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]