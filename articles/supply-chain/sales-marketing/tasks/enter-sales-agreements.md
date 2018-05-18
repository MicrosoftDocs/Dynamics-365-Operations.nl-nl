--- 
title: Verkoopovereenkomsten invoeren
description: Deze procedure toont hoe u een verkoopovereenkomst maakt waarmee een van uw klanten toezegt in een bepaalde periode een product voor een bepaald bedrag te kopen in ruil voor speciale kortingen.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a1c4b7623f3409d4474adcd04fb1331b944b9fbb
ms.openlocfilehash: a0d49068d2c6a62bf7912c2fd7cccd53308bd196
ms.contentlocale: nl-nl
ms.lasthandoff: 02/13/2018

---
# <a name="enter-sales-agreements"></a>Verkoopovereenkomsten invoeren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een verkoopovereenkomst maakt waarmee een van uw klanten toezegt in een bepaalde periode een product voor een bepaald bedrag te kopen in ruil voor speciale kortingen. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="set-up-sales-agreement-header"></a>Koptekst van de verkoopovereenkomst instellen
1. Ga naar Verkoop en marketing > Verkoopovereenkomsten > Verkoopovereenkomsten.
2. Klik op Nieuw.
3. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik in het veld Classificatie van verkoopovereenkomst op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Vouw de sectie Algemeen uit.
9. Selecteer 'Toezegging productwaarde' in het veld Standaardtoezegging.
    * Een toezeggingstype is een verplicht criterium dat u aan de overeenkomst moet toewijzen om te bepalen hoe het contact van de overeenkomst wordt afgehandeld. Met de vier vooraf gedefinieerde typen kunt u het toezeggingsdoel van de klant instellen, dat als een hoeveelheid of waarde wordt uitgedrukt. Het toezeggingstype voor hoeveelheid kan alleen voor een bepaald product worden toegepast, maar op de op waarde gebaseerde typen zijn van toepassing op verkoop van zowel specifieke als niet-specifieke producten.  
10. Stel in het veld Vervaldatum de datum in op een toekomstige datum waarop u wilt dat de overeenkomst vervalt.
11. Klik op OK.

## <a name="set-up-product-value-commitment-lines"></a>Toezeggingsregels voor productwaarde instellen
1. Klik op Regel toevoegen.
2. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Het type van toezegging dat u voor de overeenkomst hebt gekozen beïnvloedt het soort informatie dat u voor de overeenkomstregels kunt invoeren. Bij een op waarde gebaseerde overeenkomst moet u bijvoorbeeld het totale nettobedrag (in de goedgekeurde valuta) opgeven waartoe de klant zich verbindt om bij u goederen te kopen. In dit voorbeeld zijn de velden Hoeveelheid en Eenheid op de regel niet beschikbaar omdat u een overeenkomst voor de klant maakt om een specifieke waarde van een product te kopen.   
5. Typ in het veld Nettobedrag het monetaire bedrag waartoe de klant zich verbindt om te kopen.
6. Typ in het veld Kortingspercentage een procentuele waarde die van toepassing zal zijn op de verkooporderregels van de klant die aan deze overeenkomst zijn gekoppeld.
7. Vouw de sectie Regeldetails uit.
8. Selecteer Ja het veld Max is afgedwongen.
    * Als u Max is afgedwongen selecteert, mag het totale bedrag alle verkooporderregels die de speciale prijzen, kortingen en/of betalingsvoorwaarden van de toezegging gebruiken het bedrag niet overschrijden dat op de toezegging wordt opgegeven.  
    * De minimum- en maximumvrijgavebedragen geven een waardebereik op dat moet worden verkocht bij elke verkooporder die de geselecteerde overeenkomst gebruikt.   
9. Vouw de sectie Koptekst verkoopovereenkomst uit.
    * Tenzij de status van de overeenkomst is ingesteld op Van kracht, kunnen verkooporders niet aan de overeenkomst worden gekoppeld en daarom niet bijdragen aan de voltooiing van die overeenkomst. U kunt de status op dit moment handmatig wijzigen. De status wijzigt echter normaal wanneer u de overeenkomst voor de klant bevestigt.  
10. Klik in het actievenster op Verkoopovereenkomst.
11. Klik op Bevestiging.
    * Zorg ervoor dat de optie Overeenkomst als effectief markeren is ingesteld op Ja.  
12. Selecteer Ja in het veld Rapport afdrukken.
13. Klik op OK.
14. Sluit de pagina.
    * De overeenkomst is nu van kracht en u kunt de orders van de klant beginnen te koppelen aan de overeenkomst voor het starten, om het toegezegde doel te verrekenen.  


