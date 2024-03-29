---
title: Prestatiebeoordelingen maken
description: In dit artikel leest u hoe u een prestatiebeoordeling maakt, met een beschrijving van het doel van elke sectie van de beoordeling.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2de087f4e345ba826ddbe8a65f917476bd6894
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872176"
---
# <a name="create-performance-reviews"></a>Prestatiebeoordelingen maken


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


In dit artikel leest u hoe u een prestatiebeoordeling maakt, met een beschrijving van het doel van elke sectie van de beoordeling. Deze procedure is gemaakt met het demogegevensbedrijf USMF.

1. Selecteer op de startpagina het werkgebied **Selfservice werknemer**.
2. Selecteer **Nieuwe beoordeling** om een nieuwe beoordeling aan te maken.
3. Typ of selecteer een waarde in het veld **Beoordelingstype**.
4. Typ of selecteer een waarde in het veld **Prestatieperiode**.
5. Voer een datum in het veld **Einddatum** in.
6. Selecteer **OK**. U kunt ook een beoordeling maken op basis van een sjabloon. Dit is de beste manier om een beoordeling te maken, omdat elke sectie de informatie bevat die nodig is om een beoordeling te starten.  
7. U kunt tabbladen weergeven of verbergen, zoals het tabblad Bijlagen:

    1. Selecteer in het actievenster **Secties weergeven** om het dialoogvenster te openen.
    1. Selecteer **Ja** of **Nee** in het veld **Bijlagen weergeven** om het tabblad met bijlagen weer te geven of te verbergen.
    1. Selecteer **Opslaan**.

8. Selecteer **Doelstelling toevoegen aan controle** om een doel toe te voegen. Wanneer u klaar bent, selecteert u **OK**.
9. Klik op **Competentie toevoegen** om het dialoogvenster te openen.
10. Typ een waarde in het veld **Titel**.
11. Voer in het veld **Beschrijving** `Increase customer skills by working with the support team` in.
12. Selecteer **OK**.
13. Selecteer **Alles samenvouwen**.
14. Selecteer **Alles uitvouwen**.
15. Selecteer **Opmerking toevoegen**.
16. Selecteer **Boeken**.
17. Selecteer het tabblad **Metingen**.
18. Selecteer **Meting toevoegen** om het menu te openen.
19. Typ of selecteer een waarde in het veld **Meting**.
26. Typ een getal in het veld **Doelbedrag**.
20. Selecteer **OK**.
21. Selecteer het tabblad **Activiteiten**.
22. Selecteer **Toevoegen**.
23. Typ een waarde in het veld **Titel**.
24. Typ een waarde in het veld **Beschrijving**.
25. Voer een datum in het veld **Startdatum** in.
26. Typ een datum in het veld **Datum voltooid**.
27. Selecteer **Ja** in het veld **Ontwikkelingsplan**.
28. Typ een waarde in het veld **Trefwoorden**.
29. Selecteer **Opslaan**.
30. Selecteer het tabblad **Beoordelingen**.  

    - Met het sneltabblad **Classificeringsdetails** kunnen werknemers zichzelf een waardering geven, en kan de manager de werknemer beoordelen. Als wegingen worden gebruikt, wordt automatisch de gewogen waarde van de scores berekend.  
    - Als u dit gedeelte wilt bekijken, moet u de parameterinstellingen voor het tonen van werknemersbeoordelingen op de pagina **Gedeelde Human Resources-parameters** inschakelen.  

31. Selecteer het tabblad **Afmeldingen**. Als de beoordeling een workflow gebruikt, worden alleen afmeldingen weergegeven nadat de workflow is doorlopen. Als geen workflow wordt gebruikt, dan worden hier zowel de werknemer als de manager vermeld. Het selectievakje **Vereist** voor **Afmeldingen** is geselecteerd op basis van de instellingen van het type beoordeling.  
32. Selecteer het tabblad **Algemeen**.

    - De prestatieperiode maakt de standaarddatums voor begin en einde aan. Deze datums kunnen worden bewerkt.  
    - De status bepalen de toegang tot de beoordeling. Bij de status **Niet gestart** kan iedereen de beoordeling bewerken. Bij de status **In uitvoering** kan alleen de werknemer de beoordeling weergeven en bewerken. Bij de status **Gereed voor beoordeling** kan alleen de manager de beoordeling weergeven en bewerken. Met de status **Definitieve beoordeling** kan zowel de werknemer als de manager de beoordeling bekijken en bewerken als de optie **Bewerken in definitieve beoordeling toestaan** is geselecteerd in het type beoordeling. Bij de statussen **Voltooid** en **Geannuleerd** is de beoordeling alleen-lezen. Als een controle wordt **Afgewezen** en teruggestuurd naar de werknemer, kunnen de werknemer en de manager de nodige wijzigingen aanbrengen die de werknemer opnieuw kan indienen.

33. Typ een waarde in het veld **Overzicht**.
34. Selecteer het tabblad **Beoordeling**. Bij elke status waarin de beoordeling zich bevindt, kunnen de werknemer en de manager opmerkingen toevoegen voor iedere doelstelling of competentie.  
35. Selecteer het tabblad **Afmeldingen**. De werknemer en manager kunnen de beoordeling afmelden. Wanneer alle vereiste afmeldingen zijn uitgevoerd, wordt de status gewijzigd naar **Voltooid** en kan er niets meer worden gewijzigd.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
