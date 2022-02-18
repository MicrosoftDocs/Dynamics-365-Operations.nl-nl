---
title: Informatie over verwondingen en ziekte bij werknemers bijhouden
description: Met deze taak wordt beschreven hoe u een letsel- of ziektecase maakt.
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06307331db4d420e99de21c0eb0b3cf1c233f0d5
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066645"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Informatie over verwondingen en ziekte bij werknemers bijhouden


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Het is raadzaam om eerst de taakbegeleiding 'Instelling van letsel en ziekte' te voltooien, want een deel van informatie wordt hier gebruikt. 



Deze taakregistratie beschrijft de basisstappen voor het maken van een letsel- of ziektecase. Naast de details van het letsel of de ziekte, wordt de status van de case gevolgd. Cases hebben standaard de status **Openstaand**. U kunt de status beheren via het menu **Casestatus** boven aan de pagina.

1. Ga naar Human **Resources \> Medewerkers \> Letsel en ziekte \> Incidenten met letsel of ziekte**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Casebeschrijving** een waarde in (bijvoorbeeld **Polsletsel**).
4. In het veld **Medewerker** typt of selecteert u een waarde (bijvoorbeeld **Ana Bowman**).
5. Voer in het veld **Datum en tijd van het incident** een datum en tijd in (bijvoorbeeld 20 januari 2016, om 10:00 uur).
6. Typ of selecteer een waarde in het veld **Type letsel of ziekte** (bijvoorbeeld **Breuk**).
7. In het veld **Lichaamsdeel** typt of selecteert u een waarde (bijvoorbeeld **Pols**).
8. Typ of selecteer een waarde in het veld **Resultaattype** (bijvoorbeeld **Therapie**).
9. Typ een datum en tijd in het veld **Gerapporteerde datum en tijd**.

    De gerapporteerde datum en tijd moeten later zijn dan de datum en tijd van het incident.

10. Typ of selecteer een waarde in het veld **Melder van case** (bijvoorbeeld **Ana Bowman**).

    De opgegeven persoon kan de medewerker of een andere getuige van het incident zijn.

11. Voer in de sectie **Incident**, in het veld **Plaats van incident** een waarde in (bijvoorbeeld **Magazijn**).
12. Selecteer **Ja** in het veld **Op het werk** als het incident op het werk heeft plaatsgevonden.
13. Voer in het veld **Datum en tijd begin werk** de datum en tijd in waarop de betrokken persoon met werken is begonnen voordat het incident heeft plaatsgevonden.
14. Voer in het veld **Functie of taak van werknemer** de taak in die de werknemer heeft verricht op het moment dat het incident heeft plaatsgevonden (bijvoorbeeld **Dozen laden**). 
15. Voer in het veld **Oorzaak van incident** de oorzaak van het incident in (bijvoorbeeld **Uitgegleden op natte vloer**).
16. Typ of selecteer een waarde in het veld **Ernst**.
17. Voer in het veld **Te ondernemen actie** een waarde in (bijvoorbeeld **Gemors onmiddellijk schoonmaken**).
18. Voer in het veld **Verwacht aantal dagen niet op werk** het aantal dagen in dat de persoon naar verwachting niet kan werken.

    Nadat de persoon weer aan het werk is gegaan, werkt u het veld **Dagen niet op werk** bij met het werkelijke aantal dagen dat de persoon afwezig was.

19. In de sectie **Kosten letsel of ziekte** selecteert u **Toevoegen**.
20. Voer een datum in het veld **Datum** in.
21. Typ of selecteer een waarde in het veld **Kostentype** (bijvoorbeeld **Therapie**).

    U kunt ook een bedrag invoeren en alle ondersteunende documenten bij de kosten voegen, (bijvoorbeeld facturen of notities van de arts).

22. Selecteer **Toevoegen**.
23. Voer een datum in het veld **Datum** in.
24. Typ of selecteer een waarde in het veld **Kostentype** (bijvoorbeeld **Arts**).
25. In de sectie **Behandelingen van letsel of ziekte** selecteert u **Toevoegen**.
26. Typ in het veld **Behandelingsdatum** de datum en een tijd.
27. Typ of selecteer een waarde in het veld **Behandelingstype** (bijvoorbeeld **Spalk**).
28. Optioneel: stel de sectie **Bezoek aan spoedeisende hulp in ziekenhuis** desgewenst in op **Ja**.
29. Typ of selecteer een waarde in het veld **Opmerkingen bij behandeling** (bijvoorbeeld **Spalk voor 2 weken**).
30. Voer in het veld **Naam arts** een waarde in (bijvoorbeeld **Dr. Anderson**).
31. Voer in het veld **Instelling en locatie van behandeling** een waarde in (bijvoorbeeld: **SEH Medisch Centrum Oost**).
32. Voer in het veld **Details van de behandeling** een waarde in (bijvoorbeeld **Röntgenfoto's bevestigen breuk, spalk dragen**).
33. Selecteer **Opslaan**.

De casestatus kan op elk moment worden bijgewerkt. Als de verwerking van het letsel of de ziekte in behandeling is, stelt u de status in op **In behandeling**. Nadat u het incident hebt afgesloten, kunt u alleen kosten, behandelingen of registraties toevoegen of verwijderen die met het incident te maken hebben. Als u andere gegevens wilt wijzigen, moet u de case opnieuw openen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
