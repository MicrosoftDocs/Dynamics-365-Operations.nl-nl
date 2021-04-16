---
title: Van toepassing zijnde prijzen en kortingen opzoeken
description: Deze procedure laat zien hoe u de prijs en/of de korting vindt voor een product dat momenteel geldig is voor een specifieke klant, zonder een verkooporder te maken.
author: omulvad
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50d7cf7b765c27db5aa9ea50c8593132c68c850a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824841"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Van toepassing zijnde prijzen en kortingen opzoeken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u de prijs en/of de korting vindt voor een product dat momenteel geldig is voor een specifieke klant, zonder een verkooporder te maken. De procedure doorloopt een specifiek voorbeeld en u moet het voorbeeld met het demobedrijf USMF volgen om de benodigde waarden te selecteren.


## <a name="find-the-applicable-price"></a>De toepasselijke prijs zoeken
1. Ga naar Verkoop en marketing > Prijzen en kortingen > Prijzen zoeken.
2. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer in de lijst klant US-001.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ in het veld Artikelnummer de waarde 'T0004'.
    * Standaard is het veld Hoeveelheid ingesteld op 1. Echter, als u de grootte van de order weet die de klant van plan is voor het product te plaatsen, gebruikt u in plaats daarvan deze waarde. Deze informatie is alleen relevant als de handelsovereenkomsten met de klant hoeveelheidscategorieën bevatten, dat wil zeggen dat de prijs van het product afhankelijk is van de aangeschafte minimumhoeveelheid.  
6. Voer in het datumveld een datum in voor wanneer de klant verwacht een order te plaatsen. 
    * De datum kan de datum van vandaag of een datum in de toekomst zijn.  
    * Het systeem retourneert nu de prijs die geldig is voor het geselecteerde product als het wordt gekocht door de geselecteerde klant op de geselecteerde datum met een opgegeven hoeveelheid. Als klant US-001 in dit voorbeeld vandaag 1 eenheid van product T0004 koopt, wordt CAD 350 per eenheid in rekening gebracht. Deze prijs komt uit een bestaande en actieve handelsovereenkomst met de klant.      Andere velden op de pagina bevatten meer details over de productprijs en de productkosten (indien ingesteld in het productmodel), en berekende rentabiliteit.  
    * Als de optie Verwante productvarianten weergeven is ingeschakeld, betekent dit dat er extra handelsovereenkomsten voor varianten van het product zijn.  
7. Klik op het selectievakje Verwante productvarianten weergeven.
    * Een lijst van de productvarianten wordt weergegeven, met informatie over de dimensies ervan.  
8. Markeer in de lijst de regel die de kleur wit voorstelt.
    * De productprijs verschilt nu van de prijs die eerder werd weergegeven, toen deze niet per dimensie was opgegeven.  
9. Klik op Verkoopprijzen weergeven.
    * De pagina Prijs (verkoop) bevat alle handelsovereenkomsten die van toepassing zijn op het product, inclusief de varianten ervan.  
10. Sluit de pagina.

## <a name="find-the-applicable-discount"></a>De toepasselijke korting zoeken
Zorg ervoor dat het veld Klantrekening klantnummer US-001 bevat.    
1. Typ in het veld Artikelnummer de waarde 'T0012'.
    * Zorg dat het veld Hoeveelheid is ingesteld op 1.  
    * De volgende prijsgegevens die worden weergegeven voor product T0012, komen uit een of meerdere handelsovereenkomsten: de eenheidsprijs is CAD 1,000 en het kortingspercentage is 5.  
2. Stel Hoeveelheid in op '20'.
    * De verhoogde orderhoeveelheid leidt ertoe dat de regelkorting die aan de klant wordt aangeboden, verandert van 5 in 7 procent.  
    * Het nettobedrag wordt berekend op basis van de eenheidsprijs, de korting en de totale hoeveelheid.  
3. Klik op Regelkorting weergeven.
    * Er zijn twee regelkortingovereenkomsten voor product T0012, die een korting van 5% opgeven voor een orderregelhoeveelheid van 1 tot 10, en een korting van 7% voor orderhoeveelheden boven 10. Merk op dat de kortingen worden toegepast op een groep producten, in dit voorbeeld groepscode 01, waarvan product T0012 lid is.  
4. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]