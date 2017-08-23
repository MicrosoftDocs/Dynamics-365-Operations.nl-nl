--- 
title: Een conformiteit maken en verwerken
description: Gebruik deze procedure om beheer van non-conformiteiten uit te voeren, op basis van een bestaande kwaliteitsorder.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4082caf2cc8393345d4f79a991f2cf205b06b142
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-process-a-conformance"></a>Een conformiteit maken en verwerken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Gebruik deze procedure om beheer van non-conformiteiten uit te voeren, op basis van een bestaande kwaliteitsorder. U kunt deze registratie in het demobedrijf USMF uitvoeren en u kunt de voorgestelde waarden gebruiken. Doorgaans wordt deze procedure uitgevoerd door een kwaliteitsbewakingsmedewerker.  Voer als vereiste vooraf de taakregistratie 'De kwaliteit van goederen inspecteren' uit. Om de goedkeuring van een niet-conformering te verwerken moet aan de gebruiker die de taakregistratie uitvoert, een 'Naam'-waarde zijn toegewezen op de pagina Gebruikers. Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties. 


## <a name="select-a-quality-order"></a>Een kwaliteitsorder selecteren
1. Ga naar Kwaliteitsorders.
2. Markeer in de lijst de geselecteerde rij.
    * Selecteer de kwaliteitsorder die is gemaakt van de taakregistratie 'De kwaliteit van goederen inspecteren'.  

## <a name="create-a-nonconformance"></a>Een non-conformiteit maken
1. Klik op Query's.
2. Klik op Non-conformiteiten.
3. Klik op Nieuw.
4. Klik in het veld Probleemtype op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer het probleem dat tijdens het inspectieproces is gevonden.  
5. Klik in het veld Probleemtype op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik op OK.

## <a name="approvereject-a-nonconformance"></a>Een non-conformiteit goedkeuren/afwijzen
1. Klik op Functies.
2. Klik op Non-conformiteit goedkeuren.
    * Keur voor dit voorbeeld de niet-conformering goed. Goedgekeurde non-conformiteiten kunnen aan gerelateerde bewerkingen worden gekoppeld om werk vast te leggen dat is uitgevoerd als onderdeel van de verwerking van de non-conformiteit en, zoals in deze taakregistratie, de verwerking van correctiebehandeling.  
3. Klik op Ja.

## <a name="create-a-correction-action"></a>Een correctieactie maken
1. Klik op Correcties.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Klik in het veld Personeelsnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op Selecteren.
7. Klik op Koppelen.
    * Maak een notitie over de correctie. In dit voorbeeld is de actie contact met de leverancier op te nemen om de non-conformiteit te bespreken.  
8. Klik op Nieuw.
9. Klik op Notitie.
    * Afhankelijk van de rapportinstelling kunnen verschillende documenttypen worden afgedrukt in de rapporten die gerelateerd zijn aan beheer van non-conformiteiten.  
10. Typ een waarde in het veld Omschrijving.
11. Sluit de pagina.

## <a name="maintain-a-correction"></a>Een correctie onderhouden
1. Klik op Als voltooid markeren.
2. Klik op OK.
3. Sluit de pagina.

## <a name="close-a-nonconformance"></a>Een niet-conformering sluiten
1. Klik op Functies.
2. Klik op Non-conformiteit afsluiten.
3. Klik op Ja.
4. Sluit de pagina.
5. Sluit de pagina.


