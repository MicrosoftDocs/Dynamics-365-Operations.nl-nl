---
title: Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten
description: In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 26b03b6712c97b12e1221598de308813c7986179
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten

[!include [banner](includes/banner.md)]

> [!NOTE]
> We verwijderen de huidige versie van de productaanbevelingsservice aangezien we deze opnieuw willen ontwerpen met een beter algoritme en nieuwe mogelijkheden voor detailhandelaren. Zie voor meer informatie [Verwijderde of verouderde functies](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features). 

In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Retail.

Wanneer u Microsoft Dynamics 365 for Retail gebruikt, kunt u productaanbevelingen weergeven op uw POS-apparaat. *Aanbevelingen* zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht. Als u productaanbevelingen wilt weergeven, moet u een besturingselement toevoegen aan het transactiescherm met de schermindelingsontwerper.

## <a name="open-layout-designer"></a>Indelingsontwerper openen
1.  Ga naar **Detailhandel** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Schermindelingen**.
2.  Met het snelfilter kunt u zoeken naar het scherm waaraan u het besturingselement wilt toevoegen. Filter bijvoorbeeld op het veld **Schermindelings-ID** met de waarde 'F2CP16:9M'.
3.  Zoek en selecteer de gewenste record in de lijst. Selecteer bijvoorbeeld 'Naam: F2CP16:9M Schermindelings-ID: F2CP16:9M'.
4.  Klik op **Ontwerper van indeling**.
5.  Volg de aanwijzingen voor het starten van de indelingsontwerper. Wanneer naar referenties wordt gevraagd, voert u de referenties in die zijn gebruikt bij het starten van de indelingsontwerper op de pagina **Schermindelingen**.
6.  Wanneer u zich aanmeldt, wordt er een pagina weergegeven die vergelijkbaar is met de onderstaande pagina. De indeling zal afwijken, afhankelijk van de aanpassingen die voor uw winkel zijn gemaakt.

[![schermindelingsafbeelding-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Een weergaveoptie kiezen
-----------------------

Er zijn twee configuratieopties beschikbaar. Kies de optie die het meest geschikt is voor uw winkel en volg de rest van de instructies om de instelling van het besturingselement te voltooien. De twee opties zijn:
-   Aanbevelingen zijn altijd zichtbaar.
-   Het tabblad **Aanbevelingen** wordt weergegeven in het raster aan de rechterkant van het scherm.

#### <a name="to-make-recommendations-always-visible"></a>Aanbevelingen altijd zichtbaar maken

1.  Verklein de hoogte van het detailgebied van de transactieregels zodat het even hoog is als het deelvenster van de klant aan de linkerkant.[](./media/pic-2.png)[![schermindelingsafbeelding-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Sleep in het menu aan de linkerkant het besturingselement voor aanbevelingen en zet het neer tussen het detailgebied van de transactieregels en het knoppenraster onderaan in het midden van het transactiescherm. Pas de grootte van het besturingselement aan zodat het in die ruimte past.[](./media/pic-3.png)[![schermindelingsafbeelding-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.
4.  Ga in Dynamics 365 for Retail naar **Detailhandel** &gt; **IT detailhandel** &gt; **Distributieplanningen**.
5.  Selecteer **1090, kassa´s** in de lijst.
6.  Klik op **Nu uitvoeren**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Het tabblad Aanbevelingen toevoegen aan het knoppenraster aan de rechterkant van het scherm

1.  Klik met de rechtermuisknop op de lege ruimte onder het laatste tabblad van het knoppenraster dat zich aan de rechterkant van de pagina bevindt.
2.  Klik op **Aanpassen**.[![afbeelding-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klik op **Nieuw tabblad**.
4.  Zoek naar het nieuwe tabblad dat u zojuist hebt toegevoegd. Wellicht moet u omlaag bladeren.
5.  Selecteer in de vervolgkeuzelijst **Inhoud** **Aanbevolen producten**. [![afbeelding-6](./media/pic-6.png)](./media/pic-6.png)
6.  Typ in het veld **Label** een naam voor het tabblad Aanbevelingen. Typ bijvoorbeeld ´Aanbevolen producten´.
7.  Selecteer in het veld **Afbeelding** de afbeelding die op het tabblad moet worden weergegeven.
8.  Klik op **OK**. Het nieuwe tabblad wordt weergegeven in het knoppenraster.
9.  Klik op **OK** om de indelingsontwerper op te slaan en af te sluiten.
10. Ga in Dynamics 365 for Retail naar **Detailhandel** &gt; **IT detailhandel** &gt; **Distributieplanningen**.
11. Selecteer **1090, kassa´s** in de lijst.
12. Klik op **Nu uitvoeren**.


<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht van gepersonaliseerde productaanbevelingen](personalized-product-recommendations.md)




