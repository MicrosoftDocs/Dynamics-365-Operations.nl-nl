---
title: Een inkoopovereenkomst toepassen bij het maken van een inkooporder
description: Deze procedure laat zien hoe u een inkoopovereenkomst gebruikt wanneer u een inkooporder maakt.
author: Henrikan
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130524dc8e0c8724e35bf13c6b250ab721383711
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570364"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Een inkoopovereenkomst toepassen bij het maken van een inkooporder

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een inkoopovereenkomst gebruikt wanneer u een inkooporder maakt. De inkoopovereenkomst moet worden toegepast wanneer u de inkooporder maakt omdat er algemene voorwaarden zijn die naar de koptekst van de inkooporder moeten worden gekopieerd. Deze taak worden meestal uitgevoerd door een inkoopagent. Als vereiste voor deze taakbegeleiding moet u een effectieve inkoopovereenkomst met een toezegging van een producthoeveelheid hebben voor een leverancier en voor artikelen. Dezelfde procedure kan worden gebruikt als u een inkoopovereenkomst met andere typen toezeggingen hebt.

## <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Productie en sourcing \> Werkruimten \> Voorbereiding van inkooporder**.
1. Selecteer in het actievenster de optie **Nieuwe nkooporder**.
1. Het dialoogvenster **Inkooporder maken** wordt geopend. Selecteer een **leveranciersrekening**. Inspecteer en pas de andere adresvelden zo nodig aan.
1. Vouw de het sneltabblad **Algemeen**.
1. Zoek in het veld **Inkoopovereenkomst** naar de effectieve overeenkomst die u wilt gebruiken en selecteer deze. Alle beschikbare overeenkomsten voor de leverancier worden hier weergegeven.  
1. Selecteer **Ja**.
1. Selecteer **OK**.

## <a name="add-a-line"></a>Een regel toevoegen

1. Typ een waarde in het veld **Artikelnummer**. Als er specifieke voorraad- of locatiedimensies in de toezegging zijn, moet u dezelfde waarden invoeren op de inkooporderregel om de overeenkomst te gebruiken.
1. Selecteer in het veld **Locatie** de vervolgkeuzeknop om de zoekopdracht te openen. De locatie kan al gevuld zijn met de standaardwaarde van de order, of van de leverancier. Als dit het geval is, slaat u deze stap over.  
1. Zoek en selecteer de gewenste record in de lijst.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Voer een getal in het veld **Hoeveelheid** in. Controleer of de prijs uit de toezegging is gekopieerd.  

## <a name="look-up-the-commitment"></a>De toezegging opzoeken

1. Selecteer **Regel bijwerken**.
1. Selecteer **Gekoppeld**. Hier kunt u gegevens voor de inkoopovereenkomst opvragen. U kunt bijvoorbeeld de prijs zien en of de prijs en korting vast zijn, wat betekent dat als u de prijs of korting op de inkooporder wijzigt in een andere waarde dan in de toezegging, het systeem de koppeling verwijdert zodat de inkooporderregel niet aan de toezegging voldoet. U kunt ook zien of de optie Max is afgedwongen is geselecteerd, wat aangeeft dat de hoeveelheid in de toezegging niet kan worden overschreden door alle inkopen op te tellen die aan de toezegging voldoen.  
1. Sluit de pagina.

## <a name="look-up-the-purchase-agreement"></a>De inkoopovereenkomst opzoeken

1. Selecteer **Algemeen** in het **Actievenster**.
1. Selecteer **Inkoopovereenkomst**.
1. Sluit de pagina.
1. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]