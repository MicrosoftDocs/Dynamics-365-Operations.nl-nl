---
title: Periodieke journalen boeken
description: De periodieke journalen worden soms terugkerende journalen genoemd, omdat het bedrag, de tekst en andere informatie telkens worden herhaald als het periodieke journaal wordt opgehaald.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 214a7618bbec1d30212f7c53b7086ee0d5da4e6b5de40d11d3bf16399b812597
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763113"
---
# <a name="post-periodic-journals"></a>Periodieke journalen boeken

[!include [banner](../../includes/banner.md)]

De periodieke journalen worden soms terugkerende journalen genoemd, omdat het bedrag, de tekst en andere informatie telkens worden herhaald als het periodieke journaal wordt opgehaald. Wanneer u een periodiek journaal maakt, geeft u het periode-interval op voor het terugkeerpatroon, zoals dagen of maanden. Deze taakbegeleiding maakt een periodiek journaal met een maandelijkse herhaling.

1. Ga naar **Navigatievenster > Modules > Grootboek > Periodieke taken > Periodieke journalen**.
2. Klik op **Nieuw**.
3. Typ of selecteer een waarde in het veld **Naam**.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ een waarde in het veld **Beschrijving**. De omschrijving wordt de naam van het periodieke journaal wanneer deze later wordt opgehaald, dus zorg ervoor dat u een relevante naam opgeeft.
6. Klik in het **actievenster** op **Regels**. Een periodiek journaal bevat doorgaans meerdere journaalregels. Deze taakbegeleiding voegt echter slechts één regel toe.
7. Voer een datum in het veld **Datum** in. Het veld **Datum** bevat de boekingsdatum voor de volgende overboeking naar het dagelijks journaal. Voor journalen die elke maand worden opgehaald is het raadzaam om de datum in de maand te gebruiken wanneer het wordt geboekt, meestal de eerste of de laatste datum in de periode. Het is mogelijk om het datumveld leeg te laten en een datum te geven wanneer het journaal wordt opgehaald door het lege datumveld te gebruiken. Het veld wordt automatisch bijgewerkt naar de volgende terugkerende datum waarop transacties worden opgehaald. 
8. Geef in het veld **Rekening** de gewenste waarden op.
9. Selecteer een waarde in het veld **Beschrijving**.
10. Sluit de pagina.
11. Voer een nummer in het veld **Debet** in.
12. Geef in het veld **Tegenrekening** de gewenste waarden op.
13. Selecteer 'Maanden' in het veld **Eenheid**.
14. Voer '1' in het veld **Aantal eenheden** in.
15. Voer een datum in het veld **Laatste datum** in. Het invoeren van de laatste datum in de eerdere periode voorkomt dat het terugkerende journaal per ongeluk in de verkeerde beginperiode wordt gemaakt. De laatste datum wordt later bijgewerkt telkens als het periodieke journaal wordt opgehaald. 
16. Klik op **Opslaan**.
17. Ga naar **Navigatievenster > Modules > Grootboek > Journaalboekingen > Algemene journalen**.
18. Klik op **Nieuw**.
19. Typ of selecteer een waarde in het veld **Naam**.
20. Zoek en selecteer de gewenste record in de lijst.
21. Klik in de lijst op de koppeling in de geselecteerde rij.
22. Typ een waarde in het veld **Beschrijving**.
23. Klik in het **actievenster** op **Regels**.
24. Klik in het **actievenster** op **Periodejournaal**.
25. Klik op **Journaal ophalen**.
26. Voer een datum in het veld **Einddatum** in. De **einddatum** dient als de afsluitdatum voor de periodieke boekstukregels. Gebaseerd op de herhalingsinstelling kunnen de laatste datum en de einddatum van dezelfde regel meer dan één keer in het resulterende journaal worden opgenomen. De einddatum wordt automatisch bijgewerkt op basis van de sessiedatum van de laatste keer dat de periodieke regel is overgeboekt naar een journaal. 
27. Typ of selecteer een waarde in het veld **Periodiek-journaalnummer**.
28. Klik in de lijst op de koppeling in de geselecteerde rij.
29. Klik op **OK**. Het periodejournaal kan nu worden gecontroleerd, goedgekeurd of geboekt, afhankelijk van vereisten en instellingen.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]