---
title: Een besturingselement aanbevelingen toevoegen aan de transactie-pagina op een POS-apparaat
description: In dit onderwerp wordt beschreven hoe een besturingselement aanbevelingen toevoegen aan het scherm van de transactie op een punt van verkooppunten (POS)-apparaat met behulp van de ontwerper van schermindeling in Microsoft Dynamics 365 voor bewerkingen.
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

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Een besturingselement aanbevelingen toevoegen aan de transactie-pagina op een POS-apparaat

In dit onderwerp wordt beschreven hoe een besturingselement aanbevelingen toevoegen aan het scherm van de transactie op een punt van verkooppunten (POS)-apparaat met behulp van de ontwerper van schermindeling in Microsoft Dynamics 365 voor bewerkingen.

Wanneer u Microsoft Dynamics 365 voor bewerkingen, kunt u de aanbevelingen weergeven op het POS-apparaat. *Aanbevelingen* zijn artikelen die uw klant geïnteresseerd kan zijn op basis van hun inkoophistorie, artikelen in de onderwerpen en artikelen die andere klanten online gekocht en in de markering en fysieke winkels. Als u wilt weergeven van aanbevelingen, moet u een besturingselement toevoegen aan het scherm van de transactie met de ontwerper van schermindeling.

## <a name="open-layout-designer"></a>Open de ontwerper van formulierindeling
1.  Ga naar **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS**&gt;**schermindelingen**.
2.  Met het snelfilter zoeken naar het scherm dat u wilt toevoegen van het besturingselement. Bijvoorbeeld filteren op de **scherm indelings-ID** veld met de waarde 'F2CP16:9M'.
3.  Zoek en selecteer de gewenste record in de lijst. Selecteer bijvoorbeeld ' naam: F2CP16:9M scherm indelings-ID: F2CP16:9M'.
4.  Klik op **ontwerper van formulierindeling**.
5.  Volg de aanwijzingen voor het starten van de ontwerper van formulierindeling. Wanneer naar referenties gevraagd, voert u dezelfde referenties die zijn gebruikt toen de ontwerper van formulierindeling is gestart **schermindelingen** pagina.
6.  Wanneer u zich aanmeldt, wordt er een vergelijkbaar zijn met de instellingen onder pagina weergegeven. De lay-out zullen afwijken, afhankelijk van de aanpassingen die zijn gemaakt voor uw winkel.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Kies een weergaveoptie
-----------------------

Er zijn twee configuraties opties beschikbaar. Kies de optie die het meest geschikt voor uw winkel en volg de instructies voor het instellen van het besturingselement te voltooien. De twee opties zijn:
-   Aanbevelingen zijn altijd zichtbaar.
-   A **aanbevelingen** tabblad wordt weergegeven in het raster aan de rechterkant van het scherm.

#### <a name="to-make-recommendations-always-visible"></a>Om aanbevelingen te doen altijd zichtbaar

1.  Verklein de hoogte van het detailgebied van de transactie-regels zodat deze even hoog als het deelvenster klant aan de linkerkant. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Klik in het menu aan de linkerkant slepen en neerzetten van het besturingselement aanbevelingen tussen het detailgebied van de transactie-regel en het knoppenraster onderaan in het midden van het scherm van de transactie. Het formaat van het besturingselement zodat deze in die ruimte past. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klik op de **X** op te slaan en sluit de ontwerper van formulierindeling.
4.  In Dynamics 365 voor bewerkingen, gaat u naar **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributie-schema's**.
5.  Selecteer in de lijst **1090 registreert**.
6.  Klik op **nu uitvoeren**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Een tabblad aanbevelingen op de knoppenraster aan de rechterkant van het scherm toevoegen

1.  Met de rechtermuisknop op de lege ruimte onder het laatste tabblad van het knoppenraster dat aan de rechterkant van de pagina bevindt.
2.  Klik op **aanpassen**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klik op **nieuw tabblad**.
4.  Zoeken naar het nieuwe tabblad dat u zojuist hebt toegevoegd. Wellicht moet u omlaag bladeren.
5.  In de **inhoud** vervolgkeuzelijst, selecteer **aanbevolen producten**. [![PIC-6](./media/pic-6.png)](./media/pic-6.png)
6.  In de **Label** veld, typ een naam voor het tabblad aanbevelingen. Typ bijvoorbeeld "Aanbevolen producten".
7.  In de **afbeelding** veld, selecteert u de afbeelding wilt weergeven op het tabblad.
8.  Click **OK**. Het nieuwe tabblad wordt weergegeven in het knoppenraster.
9.  Klik op de **X** op te slaan en sluit de ontwerper van formulierindeling.
10. In Dynamics 365 voor bewerkingen, gaat u naar **detailhandel en commerce**&gt;**detailhandel IT**&gt;**distributie-schema's**.
11. Selecteer in de lijst **1090 registreert**.
12. Klik op **nu uitvoeren**.


<a name="see-also"></a>Zie ook
--------

[Persoonlijke aanbevelingen-productoverzicht](personalized-product-recommendations.md)


