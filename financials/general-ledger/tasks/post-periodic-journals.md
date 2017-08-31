--- 
title: Periodieke journalen boeken
description: De periodieke journalen worden soms terugkerende journalen genoemd, omdat het bedrag, de tekst en andere informatie telkens worden herhaald als het periodieke journaal wordt opgehaald.
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b1b1b857428ca1ee36496f82c79a17eb157c8dd8
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="post-periodic-journals"></a>Periodieke journalen boeken

[!include[task guide banner](../../includes/task-guide-banner.md)]

De periodieke journalen worden soms terugkerende journalen genoemd, omdat het bedrag, de tekst en andere informatie telkens worden herhaald als het periodieke journaal wordt opgehaald. Wanneer u een periodiek journaal maakt, geeft u het periode-interval op voor het terugkeerpatroon, zoals dagen of maanden. Deze taakbegeleiding maakt een periodiek journaal met een maandelijkse herhaling.



1. Ga naar Grootboek > Periodieke taken > Periodieke journalen.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Naam.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ een waarde in het veld Omschrijving.
    * De omschrijving wordt de naam van het periodieke journaal wanneer deze later wordt opgehaald, dus zorg ervoor dat u een relevante naam opgeeft.  
6. Klik op Regels.
    * Een periodiek journaal bevat doorgaans meerdere journaalregels. Deze taakbegeleiding voegt echter slechts één regel toe.  
7. Voer een datum in het veld Datum in.
    * Het veld Datum bevat de boekingsdatum voor de volgende overboeking naar het dagelijks journaal. Voor journalen die elke maand worden opgehaald is het raadzaam om de datum in de maand te gebruiken wanneer het wordt geboekt, meestal de eerste of de laatste datum in de periode. Het is mogelijk om het datumveld leeg te laten en een datum te geven wanneer het journaal wordt opgehaald door het lege datumveld te gebruiken.    Het veld wordt automatisch bijgewerkt naar de volgende terugkerende datum waarop transacties worden opgehaald.  
8. Geef in het veld Rekening de gewenste waarden op.
9. Typ een waarde in het veld Omschrijving.
10. Sluit de pagina.
11. Voer een nummer in het veld Debet in.
12. Geef in het veld Tegenrekening de gewenste waarden op.
13. Selecteer Maanden in het veld Eenheid.
14. Voer 1 in het veld Aantal eenheden in.
15. Voer een datum in het veld Laatste datum in.
    * Het invoeren van de laatste datum in de eerdere periode voorkomt dat het terugkerende journaal per ongeluk in de verkeerde beginperiode wordt gemaakt. De laatste datum wordt later bijgewerkt telkens als het periodieke journaal wordt opgehaald.  
16. Klik op Opslaan.
17. Ga naar Standaarddashboard.
18. Ga naar Grootboek > Journaalboekingen > Algemene journalen.
19. Klik op Nieuw.
20. Typ of selecteer een waarde in het veld Naam.
21. Zoek en selecteer de gewenste record in de lijst.
22. Klik in de lijst op de koppeling in de geselecteerde rij.
23. Typ een waarde in het veld Omschrijving.
24. Klik op Regels.
25. Klik op Periodejournaal.
26. Klik op Journaal ophalen.
27. Voer een datum in het veld Einddatum in.
    * De einddatum dient als de afsluitdatum voor de periodieke boekstukregels. Gebaseerd op de herhalingsinstelling kunnen de laatste datum en de einddatum van dezelfde regel meer dan één keer in het resulterende journaal worden opgenomen. De einddatum wordt automatisch bijgewerkt op basis van de sessiedatum van de laatste keer dat de periodieke regel is overgeboekt naar een journaal.  
28. Typ of selecteer een waarde in het veld Periodiek-journaalnummer.
29. Klik in de lijst op de koppeling in de geselecteerde rij.
30. Klik op OK.
    * Het periodejournaal kan nu worden gecontroleerd, goedgekeurd of geboekt, afhankelijk van vereisten en instellingen.  


