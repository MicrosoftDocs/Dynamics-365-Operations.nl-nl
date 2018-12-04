--- 
title: Belastingen en zendingen plannen met behulp van de Workbench ladingplanning
description: Deze procedure laat zien hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Belastingen en zendingen plannen met behulp van de Workbench ladingplanning

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder. Als vereiste maken we eerst de verkooporder. Deze procedure maakt deel uit van het dagelijks werk voor de transportcoördinator. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-sales-order"></a>Verkooporder maken
1. Ga naar Klanten > Orders > Alle verkooporders.
2. Klik op Nieuw.
3. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer rekening US-004.
5. Klik op OK.
6. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer artikel A0001.
    * A0001 is ingeschakeld voor transportbeheer.  
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Voer in het veld Hoeveelheid een getal in.
10. Typ "24" in het veld Magazijn.
    * Selecteer in dit voorbeeld magazijn 24. Dit magazijn is ingeschakeld voor transportbeheer en geavanceerd magazijnbeheer.  
11. Klik op Opslaan.
12. Sluit de pagina.

## <a name="create-a-new-load"></a>Een nieuwe lading maken
1. Ga naar Transportbeheer > Planning > Workbench van ladingplanning.
2. Klik op het tabblad Verkoopregels.
    * Nu gaat u de lading samenstellen voor de verkooporder die u zojuist hebt gemaakt. Ladingen kunnen worden samengesteld op basis van de vraag en aanbod van inkooporders, transferorders en verkooporders.  
3. Klik in het actievenster op Vraag en aanbod.
4. Klik op Naar nieuwe lading.
5. Klik in het veld Ladingsjabloon-id op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De sjabloon voor laden definieert maximummetingen voor gewicht en volume van de volledige lading. Zo kan de laadsjabloon bijvoorbeeld de grootte van een container of een vrachtwagen vertegenwoordigen.  
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik op OK.

## <a name="rate-and-route-the-load"></a>Tarief en route voor lading bepalen
1. Klik op Classificatie en routering.
2. Klik op Workbench tariefroute.
3. Klik op Tariefwinkel.
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik op Toewijzen.
6. Sluit de pagina.
7. Sluit de pagina.


