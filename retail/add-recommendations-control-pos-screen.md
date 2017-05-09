---
title: Een besturingselement voor aanbevelingen toevoegen aan de transactiepagina op een POS-apparaat
description: In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Operations.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Een besturingselement voor aanbevelingen toevoegen aan de transactiepagina op een POS-apparaat

[!include[banner](includes/banner.md)]


In dit onderwerp wordt beschreven hoe u een besturingselement voor aanbevelingen kunt toevoegen aan het transactiescherm op een POS-apparaat (Point of Sale) met behulp van de schermindelingsontwerper in Microsoft Dynamics 365 for Operations.

Wanneer u Microsoft Dynamics 365 for Operations gebruikt, kunt u productaanbevelingen weergeven op uw POS-apparaat. *Aanbevelingen* zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht. Als u productaanbevelingen wilt weergeven, moet u een besturingselement toevoegen aan het transactiescherm met de schermindelingsontwerper.

## <a name="open-layout-designer"></a>Indelingsontwerper openen
1.  Ga naar **Detailhandel en commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Schermindelingen**.
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
4.  Ga in Dynamics 365 for Operations naar **Detailhandel en commerce** &gt; **IT detailhandel** &gt; **Distributieplanningen**.
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
10. Ga in Dynamics 365 for Operations naar **Detailhandel en commerce** &gt; **IT detailhandel** &gt; **Distributieplanningen**.
11. Selecteer **1090, kassa´s** in de lijst.
12. Klik op **Nu uitvoeren**.


<a name="see-also"></a>Zie ook
--------

[Overzicht persoonlijke productaanbevelingen](personalized-product-recommendations.md)




