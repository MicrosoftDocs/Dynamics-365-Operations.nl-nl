---
title: Werkcellen voor lean manufacturing definiëren
description: Een werkcel is een specifiek formulier van resourcegroepen die kan worden gebruikt in de activiteiten van het lean manufacturingproces.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 068f87d4fcbee95227bb51ea6b7fdcbef8547d06
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257262"
---
# <a name="define-lean-manufacturing-work-cells"></a>Werkcellen voor lean manufacturing definiëren

[!include [banner](../../includes/banner.md)]

Een werkcel is een specifiek formulier van resourcegroepen die kan worden gebruikt in de activiteiten van het lean manufacturingproces. Werkcellen hebben invoer- en uitvoerlocaties en een capaciteitsdefinitie op basis van een model voor productiestroom. Voor meer informatie over de basisconcepten van werkcellen voor lean manufacturing en capaciteitsberekeningen raadpleegt u de whitepapers over lean manufacturing. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-work-cell"></a>Maak een werkcel. 
1. Ga naar Organisatiebeheer > Resources > Resourcegroepen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Resourcegroep.
    * De werkcel-id is meestal een systematische code en moet uniek zijn voor de rechtspersoon.  
4. Typ een waarde in het veld Omschrijving.
    * De beschrijving bevat de naam of titel van de werkcel.  
5. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Een werkcel bevindt zich op één specifieke locatie. De invoer- en uitvoermagazijnen en -locaties moeten zich op deze site bevinden.  
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik in het veld Productie-eenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer een productie-eenheid waartoe deze werkcel behoort.  
9. Schakel het selectievakje Werkcel in.
    * Om een resourcegroep als lean werkcel te gebruiken, moet het selectievakje Werkcel zijn ingeschakeld.  Deze eigenschap kan niet worden gewijzigd nadat de resourcegroep is gemaakt.  
10. Klik in het veld Invoermagazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Voor controle van boekhouding en materiaal is het materiaal dat wordt gefaseerd op de werkvloer meestal toegewezen aan een specifiek virtueel magazijn. Als u de locaties echter wilt aanvullen met magazijnwerk, moeten deze deel uitmaken van het ontvangende grondstoffenmagazijn.  
12. Klik in het veld Invoerlocatie op de vervolgkeuzeknop om de zoekopdracht te openen.
13. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Voor een procesactiviteit kan de invoerlocatie in het algemeen of voor een bepaald product of een bepaalde productvariant worden overschreven door orderverzamelactiviteiten te definiëren die de procesactiviteit aanvoeren. De invoerlocaties van een werkcel kunnen geen locaties zijn waar nummerplaten worden gecontroleerd.  
14. Klik in het veld Uitvoermagazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
15. Zoek en selecteer de gewenste record in de lijst.
    * In meerdere activiteitproductiestromen of productieregels is dit vaak het invoermagazijn van de volgende werkcel of het verkoop- of transitmagazijn waarin een product na het productieproces meestal naar wordt overgeboekt. Bij het modelleren van lean manufacturingprocessen is transport meestal afval, net zoals rapportage van transport.  
16. Klik in de lijst op de koppeling in de geselecteerde rij.
17. Klik in het veld Uitvoerlocatie op de vervolgkeuzeknop om de zoekopdracht te openen.
    * In een productiestroom met meerdere procesactiviteiten is dit vaak de invoerlocatie van de volgende werkcel.  
18. Zoek en selecteer de gewenste record in de lijst.
19. Klik in de lijst op de koppeling in de geselecteerde rij.
20. Vouw de sectie Bewerking uit of samen.
    * Een uitvoeringstijdcategorie moet worden opgegeven om kostenberekening en verwerking van de kanbantaken mogelijk te maken.  
21. Klik in het veld Uitvoeringstijdcategorie op de vervolgkeuzeknop om de zoekopdracht te openen.
22. Zoek en selecteer de gewenste record in de lijst.
    * De kostencategorie voor uitvoeringstijd wordt gebruikt in de standaardkostenberekening en kostprijsberekening via terugwaarts afboeken.  
23. Klik in de lijst op de koppeling in de geselecteerde rij.
24. Vouw de sectie Kalenders uit of samen.
25. Klik op Toevoegen.
26. Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.
27. Zoek en selecteer de gewenste record in de lijst.
    * Meestal gebruiken werkcellen van een bepaalde site dezelfde werktijdkalender. Als werkcellen afzonderlijke werktijden kunnen hebben, moet u voor de werkcel mogelijk een specifieke werktijdkalender maken. De kalender moet een standaardwerktijd hebben wanneer u deze gebruikt voor een lean werkcel, omdat de capaciteitsdefinitie meestal gekoppeld is aan de standaardwerktijd van een werkdag.  
28. Klik in de lijst op de koppeling in de geselecteerde rij.
29. Vouw de sectie Werkcelcapaciteit uit of samen.
30. Klik op Toevoegen.
31. Klik in het veld Model voor productiestroom op de vervolgkeuzeknop om de zoekopdracht te openen.
32. Zoek en selecteer de gewenste record in de lijst.
    * Deze procedures vereisen een model voor productiestroom van het type Doorvoer om de definitie van doorvoercapaciteit weer te geven.  
33. Klik in de lijst op de koppeling in de geselecteerde rij.
34. Selecteer een optie in het veld Capaciteitsperiode.
    * De opties zijn: Standaardwerkdag - De capaciteit wordt uitgedrukt door de lengte van de standaardwerkdag van de werktijdkalender voor de werkcel. Voor elke dag wordt de werkelijke werktijd bepaald door de kalender en de effectieve beschikbare capaciteit die op basis daarvan wordt berekend.   Week - Hiermee is een wekelijkse capaciteit mogelijk. Er is geen correctie uitgevoerd door de werkelijke werktijd.   Maand - Hiermee is een maandelijkse capaciteit mogelijk. Er is geen correctie uitgevoerd door de werkelijke capaciteit.   Doorgaans wordt de standaardwerkdag gebruikt voor dagelijkse perioden en wordt de wekelijkse capaciteit gebruikt voor wekelijkse capaciteitsperioden.  
35. Typ een getal in het veld Gemiddelde doorvoerhoeveelheid.
    * Een lean bewerking wordt nooit ingesteld voor de maximaal mogelijke capaciteit in een ideale omgeving. In plaats daarvan moet de capaciteit altijd worden gedefinieerd voor bewerkingen die in normale omstandigheden worden uitgevoerd.  
36. Klik in het veld Eenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
37. Klik in de lijst op de koppeling in de geselecteerde rij.
38. ResolveChanges de Eenheid.

## <a name="add-a-financial-dimension"></a>Een financiële dimensie toevoegen
1. Vouw de sectie Financiële dimensies uit of samen.
    * De financiële dimensies die op de productiestroom zijn gedefinieerd negeren de financiële dimensie van een bepaalde werkcel.    De financiële dimensies die kunnen worden geselecteerd hangen af van de configuratie van de financiële dimensies van uw systeem. De volgende stappen komen overeen met de demogegevens die in het bedrijf USMF zijn ingesteld. Bij gebruik van andere gegevens zijn de stappen mogelijk niet van toepassing.  
2. Klik in het veld Kostenplaats op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer de gewenste record in de lijst.
    * De dimensies die op lean werkcellen moeten worden geselecteerd hangen af van de implementatie van financiële dimensies in het boekhoudingsmodel voor een bepaalde rechtspersoon.  
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="save"></a>Opslaan
1. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]