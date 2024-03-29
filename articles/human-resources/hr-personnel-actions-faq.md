---
title: Veelgestelde vragen over personeelsacties
description: Dit artikel bevat antwoorden op vragen die u mogelijk hebt als uw organisatie personeelsacties gebruikt.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8882fd00c68dc3cafcb4ecf1b2fe351a9e7f5741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874302"
---
# <a name="personnel-actions-faq"></a>Veelgestelde vragen over personeelsacties


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dit artikel bevat antwoorden op vragen die u mogelijk hebt als uw organisatie personeelsacties gebruikt. Personeelsacties zijn aanvullende stappen die u moet voltooien wanneer u bepaalde personeelsgerelateerde taken uitvoert. 

Voorbeelden van taken waarvoor personeelsacties zijn vereist:
 - Wanneer u nieuwe posities maakt. 
 - Bestaande positiewaarden bewerken. 
 - Nieuwe medewerkers aannemen. 
 - Medewerkers overdragen. 
 - Medewerkerscompensatie wijzigen. 
 - Positietoewijzingen wijzigen. 
 - Medewerkers ontslaan.

> [!NOTE]
> Personeelsacties zijn alleen beschikbaar als de velden **Medewerkersacties inschakelen** en **Positieacties inschakelen** zijn ingesteld op **Ja** op het tabblad **Personeelsacties** op de pagina **Gedeelde Human resources-parameters**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Hoe weet ik of mijn organisatie personeelsacties vereist?
Uw organisatie vereist personeelsacties als u wordt gevraagd een personeelsactie te selecteren wanneer u nieuwe posities maakt, bestaande posities wijzigt, nieuwe werknemers aanwerft, werknemers overdraagt, werknemerscompensaties wijzigt, positietoewijzingen wijzigt, werknemers beëindigt of verlof invoert voor werknemers. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Wat is het verschil tussen een positie-actie en een werknemersactie?
Er zijn twee typen personeelsacties:

- **Positieactie**: een positieactie wordt uitgevoerd voor bestaande posities of nieuwe posities. Een positieactie kan bijvoorbeeld zijn vereist als u een waarde op een bestaande positie wijzigt of als u een nieuwe seizoengebonden positie maakt. 

- **Medewerkersactie**: een medewerkersactie wordt uitgevoerd op bestaande medewerkers of nieuwe medewerkers. Een werknemersactie kan bijvoorbeeld worden vereist wanneer een nieuwe werknemer in dienst wordt genomen of een bestaande werknemer promotie krijgt. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Wat betekent de status van de personeelsacties?
Personeelacties kunnen een van de volgende statussen hebben:

- **Concept**: Als de werkstroom wordt gebruikt, is de actie niet verzonden. Als werkstroom niet wordt gebruikt, is de actie niet voltooid.
- **Wordt gecontroleerd**: De personeelsactie is ingediend bij de werkstroom, maar de werkstroom is niet voltooid.
- **Goedgekeurd in afwachting**: De werkstroom is voltooid, maar de wijzigingen zijn nog in uitvoering. **Geannuleerd**: de werkstroom is geannuleerd of de personeelsactie is ingetrokken. **Afgewezen**: de actieaanvraag is afgewezen door de fiatteur.
- **Verwerking van actie**: De actieaanvraag is goedgekeurd en de wijzigingen worden verwerkt.
- **Workflow voltooid**: De werkstroom is voltooid en de wijzigingen zijn verwerkt. **Mislukt**: de werkstroom is mislukt omdat de gegevens verouderd zijn. Klik op **Opnieuw activeren** om de meest recente informatie weer te geven en verder te gaan.
- **Voltooid**: De positie is gemaakt of gewijzigd, of de werknemer was succesvol in dienst genomen, overgeplaatst of ontslagen, of diens compensatie werd gewijzigd. **Fout**: er deed zich een ander probleem voor dan verouderde informatie. Open het **Berichtenlogboek personeelsacties** om de oorzaak van de fout te bepalen.
- **Geweigerd**: De actieaanvraag is afgewezen door de fiatteur.

## <a name="can-i-delete-a-personnel-action"></a>Kan ik een personeelsactie verwijderen?
Ja, u kunt personeelsacties verwijderen die een status **Concept**, **Fout**, **Mislukt** of **Geannuleerd** hebben. U kunt personeelsacties met de status **Voltooid** alleen verwijderen als u de optie **Verwijderen van voltooide werknemersacties toestaan** op **Ja** op de pagina **Gedeelde Human Resources-parameter** hebt ingesteld.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Wat is de snelste manier om de status van een personeelsactieaanvraag te bekijken?
Open een van de lijstpagina's van de **personeelsacties** en selecteer een personeelsactie.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Wat kan ik doen als een personeelsactieaanvraag mislukt?
Als een personeelsactieaanvraag mislukt, moet u deze stappen volgen om de fout op te lossen en de aanvraag opnieuw in te dienen:

> 1. Klik in het **Actievenster** op de knop **Fouttekst** om de berichttekst weer te geven die het probleem beschrijft.
> 
> 2. Klik in het **Actievenster** op **Opnieuw activeren** om de meest recente informatie te laden en de status van de personeelsactie terug te zetten op **Concept**.
> 
> 3. Los de fout op en klik vervolgens op **Voltooien** of **Verzenden**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Wat gebeuren er met een personeelsactie die werkstroom gebruikt wanneer de definitieve goedkeuring is voltooid?
Als er geen fouten zijn, wordt de personeelsactie alleen-lezen. (U kunt de historie bekijken op de lijstpagina **Alle medewerkersacties**, maar u kunt de personeelsactie niet wijzigen.) Wanneer de status van een personeelsactie **Voltooid** is, is de positie- of werknemerrecord al bijgewerkt. Om de wijzigingen weer te geven die zijn uitgevoerd, opent u de lijstpagina **Posities** of **Medewerkers**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Waarom ontvang ik de volgende fout wanneer ik een niet-nulwaarde in het veld Salaristarief invoer? "De waarde valt buiten het geldige bereik. De waarde moet liggen tussen 0.00 en 0.00"
U ziet dit bericht omdat het veld **Niveau** op de pagina **Functie** leeg is voor de functie die aan de geselecteerde positie is gekoppeld.

Om deze fout op te lossen, volgt u deze stappen:

> 1. Klik op de pagina **Positietoewijzingen medewerker** op het veld **Positie**.  
> 2. Klik op de waarde van het veld **Functie** om het formulier **Functie** te openen.
> 3. Klik in het actievenster op **Bewerken**.
> 4. Klik op het tabblad **Compensatie**.
> 5. Selecteer een niveau in het veld **Niveau**.
> 6. Sluit de pagina **Functie**.
> 7. Sluit de pagina **Positie**.
> 8. Ga terug naar het tabblad **Compensatie** op de pagina **Medewerker** en selecteer **Vaste compensatie**.  Selecteer **Nieuw** en voer de positie van de medewerker in het veld **Positie** in.  Voer een waarde in het veld **Plan** in en voer vervolgens de compensatie van de medewerker in het veld **Loontarief** in.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Waarom kan ik de ingangsdatum niet wijzigen in de koptekst van de pagina Medewerkersactie?
U kunt de ingangsdatum niet wijzigen omdat het veld is ingevuld met de meest logische datum voor het actietype.

Bijvoorbeeld:

- De ingangsdatum in de koptekst van een actie **Een medewerker ontslaan** is de datum die u in het veld **Ontslagdatum** voor de werknemer hebt ingevoerd.
- De ingangsdatum van een actie **Een medewerker aannemen** is de datum die u in het veld **Begindatum dienstverband** hebt ingevoerd.
- De ingangsdatum van een actie **Een medewerker overplaatsen** is de datum die u in het veld **Begindatum van toewijzing** voor de medewerker hebt ingevoerd.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
