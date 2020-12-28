---
title: Een uitbestede werkcel voor lean manufacturing maken
description: Als u uitbesteed werk wilt modelleren voor lean manufacturing, moet u een werkcel maken die is gekoppeld aan de leverancier die het werk levert.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bc1e8551bbebd11cad18d47f9e74a2dedcb908d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425155"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Een uitbestede werkcel voor lean manufacturing maken

[!include [banner](../../includes/banner.md)]

Als u uitbesteed werk wilt modelleren voor lean manufacturing, moet u een werkcel maken die is gekoppeld aan de leverancier die het werk levert. Een uitbestede werkcel is gekoppeld aan de leverancier via de koppeling van een resource van het type Leverancier. Als u deze opname afspeelt in het voorbeeldbedrijf USMF, kunt u de leveranciersrekening ID 1002 en site 1 selecteren.


## <a name="create-a-vendor-resource"></a>Een leveranciersresource maken
1. Ga naar Resources.
2. Klik op Nieuw.
3. Typ een waarde in het veld Bron.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer 'Leverancier' in het veld Type.
6. Klik in het veld Leverancier op de vervolgkeuzeknop om de zoekopdracht te openen.

## <a name="create-the-resource-group"></a>De resourcegroep maken
1. Ga naar Resourcegroepen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Resourcegroep.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer de locatie waaraan de werkcel moet worden toegewezen. In theorie kan een site één site vertegenwoordigen die door een leverancier wordt gebruikt. Echter in de meeste gevallen worden uitbestede resources alleen toegewezen aan de site die het uitbesteed werk bestelt. Zorg ervoor dat de invoer- en uitvoermagazijnen van uitbestede werkcellen zich op dezelfde locatie bevinden.  
6. Typ een waarde in het veld Locatie.
7. @SysTaskRecorder:_RequestClose
8. Schakel het selectievakje Werkcel in of uit.
9. Klik in het veld Invoermagazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer het magazijn en de locatie die worden gebruikt voor het klaarzetten van het materiaal voor de door de leverancier beheerde werkcel. In veel gevallen worden het magazijn en locatie gemodelleerd met behulp van een afzonderlijk magazijn per leverancier en één locatie per werkcel.  
10. Klik in het veld Invoerlocatie op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Klik in het veld Uitvoermagazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Definieer het magazijn en de locatie waar het materiaal wordt geboekt wanneer de uitbestede activiteiten van de werkcel worden geboekt. Het magazijn en de locatie kunnen zich op de leverancierslocatie bevinden als de leverancier de kanbantaken rapporteert. Het magazijn en de locatie kunnen ook de ontvangstlocatie zijn die aan de volgende stap van de productiestroom is gekoppeld.  
12. Klik in het veld Uitvoerlocatie op de vervolgkeuzeknop om de zoekopdracht te openen.
13. Vouw de sectie Kalenders uit of samen.
14. Klik op Toevoegen.
15. Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Koppel de werktijdkalender van de werkcel aan de resourcegroep. Voor kritieke resources wordt u aangeraden dat u specifieke kalenders definieert die staan voor de exacte werktijden en de verwante capaciteit van de werkcel of leverancierslocatie.  
16. Vouw de sectie Resources uit of samen.
17. Klik op Toevoegen.
    * Een uitbestede resourcegroep moet een gekoppelde resource van het type leverancier hebben die de resourcegroep koppelt aan de leveranciersrekening.  
18. Klik in het veld Resource op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer of typ de leveranciersresource die u hebt gemaakt in de vorige subtaak.  
19. Vouw de sectie Werkcelcapaciteit uit of samen.
20. Klik op Toevoegen.
    * Een werkcel moet een gedefinieerde capaciteit hebben. In dit voorbeeld maken we een doorvoercapaciteit van 100 stuks per standaardwerkdag.  
21. Klik in het veld Model voor productiestroom op de vervolgkeuzeknop om de zoekopdracht te openen.
22. Selecteer een optie in het veld Capaciteitsperiode.
23. Typ een getal in het veld Gemiddelde doorvoerhoeveelheid.
24. Klik in het veld Eenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
25. ResolveChanges de Eenheid.

