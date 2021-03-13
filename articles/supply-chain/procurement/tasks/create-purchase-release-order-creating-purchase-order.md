---
title: Een vrijgaveorder voor inkoop maken wanneer de inkooporder wordt gemaakt
description: Deze procedure laat zien hoe u een inkoopovereenkomst gebruikt wanneer u een inkooporder maakt.
author: RichardLuan
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f82cabebea5c9e86e898c064c70a0e7a48b49d3
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016598"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>Een vrijgaveorder voor inkoop maken wanneer de inkooporder wordt gemaakt

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een inkoopovereenkomst gebruikt wanneer u een inkooporder maakt. De inkoopovereenkomst moet worden toegepast wanneer u de inkooporder maakt omdat er algemene voorwaarden zijn die naar de koptekst van de inkooporder moeten worden gekopieerd. Deze taak worden meestal uitgevoerd door een inkoopagent. Als vereiste voor deze taakbegeleiding moet u een effectieve inkoopovereenkomst met een toezegging van een producthoeveelheid hebben voor een leverancier en voor artikelen. Dezelfde procedure kan worden gebruikt als u een inkoopovereenkomst met andere typen toezeggingen hebt. U kunt deze handleiding uitvoeren in het demobedrijf USMF. Als u USMF gebruikt, kunt u eerst de begeleiding "Een inkoopovereenkomst maken" uitvoeren om de benodigde condities voor deze begeleiding in te stellen.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Open het werkgebied voor het voorbereiden van inkooporders.
2. Klik op Nieuwe inkooporder.
3. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Schakel de uitbreiding van de sectie Algemeen om.
7. Klik in het veld Inkoopovereenkomst op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Alle beschikbare overeenkomsten voor de leverancier worden hier weergegeven. Zoek de effectieve overeenkomst die u wilt gebruiken.  
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik op Ja.
10. Klik op OK.

## <a name="add-a-line"></a>Een regel toevoegen
1. Typ een waarde in het veld Artikelnummer.
    * Als er specifieke voorraad- of locatiedimensies in de toezegging zijn, moet u dezelfde waarden invoeren op de inkooporderregel om de overeenkomst te gebruiken.  
2. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De locatie kan al gevuld zijn met de standaardwaarde van de order, of van de leverancier. Als dit het geval is, slaat u deze stap over.  
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Voer in het veld Hoeveelheid een getal in.
    * Controleer of de prijs uit de toezegging is gekopieerd.  

## <a name="look-up-the-commitment"></a>De toezegging opzoeken
1. Klik op Regel bijwerken.
2. Klik op Gekoppeld.
    * Hier kunt u gegevens voor de inkoopovereenkomst opvragen. U kunt bijvoorbeeld de prijs zien en of de prijs en korting vast zijn, wat betekent dat als u de prijs of korting op de inkooporder wijzigt in een andere waarde dan in de toezegging, het systeem de koppeling verwijdert zodat de inkooporderregel niet aan de toezegging voldoet. U kunt ook zien of de optie Max is afgedwongen is geselecteerd, wat aangeeft dat de hoeveelheid in de toezegging niet kan worden overschreden door alle inkopen op te tellen die aan de toezegging voldoen.  
3. Sluit de pagina.

## <a name="look-up-the-purchase-agreement"></a>De inkoopovereenkomst opzoeken
1. Klik in het actievenster op Algemeen.
2. Klik op Inkoopovereenkomst.
3. Sluit de pagina.
4. Sluit de pagina.

