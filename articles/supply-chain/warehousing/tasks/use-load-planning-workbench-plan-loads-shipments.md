---
title: Belastingen en zendingen plannen met behulp van de Workbench ladingplanning
description: In dit onderwerp wordt getoond hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 277b91944d8f7ee79bed9b85ee6ebd275e72c75b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223285"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Belastingen en zendingen plannen met behulp van de Workbench ladingplanning

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt getoond hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder. Als vereiste maken we eerst de verkooporder. Deze procedure maakt deel uit van het dagelijks werk voor de transportcoördinator. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-sales-order"></a>Verkooporder maken
1. Ga naar **navigatiedeelvenster > Modules > Klanten > Orders > Alle verkooporders**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Klantrekening** de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer rekening **US-004**.
5. Selecteer **OK**.
6. Selecteer in het veld **Artikelnummer** de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer artikel **A0001**. **A0001** is ingeschakeld voor transportbeheer.  
8. Selecteer in het veld **Site** de vervolgkeuzeknop om de zoekopdracht te openen en selecteer vervolgens een artikel.
9. Voer een getal in het veld **Hoeveelheid** in.
10. Typ '24' voor dit voorbeeld in het veld **Magazijn**. Dit magazijn is ingeschakeld voor transportbeheer en geavanceerd magazijnbeheer.  
11. Selecteer **Opslaan**.
12. Sluit de pagina.

## <a name="create-a-new-load"></a>Een nieuwe lading maken
1. Ga naar het **navigatiedeelvenster > Modules > Transportbeheer > Planning > Workbench ladingplanning**.
2. Selecteer het tabblad **Verkoopregels**. Nu gaat u de lading samenstellen voor de verkooporder die u zojuist hebt gemaakt. Ladingen kunnen worden samengesteld op basis van de vraag en aanbod van inkooporders, transferorders en verkooporders.  
3. Selecteer in het actievenster de optie **Vraag en aanbod**.
4. Selecteer **Naar nieuwe lading**.
5. Selecteer in het veld **Ladingsjabloon-id** de vervolgkeuzeknop om de zoekopdracht te openen. De sjabloon voor laden definieert maximummetingen voor gewicht en volume van de volledige lading. Zo kan de laadsjabloon bijvoorbeeld de grootte van een container of een vrachtwagen vertegenwoordigen. Een artikel selecteren.
6. Selecteer **OK**.

## <a name="rate-and-route-the-load"></a>Tarief en route voor lading bepalen
1. Selecteer **Beoordeling en routering**.
2. Selecteer **Routetarief-workbench maken**.
3. Selecteer **Tariefwinkel**.
4. Zoek en selecteer de gewenste record in de lijst.
5. Selecteer **Toewijzen**.
6. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]