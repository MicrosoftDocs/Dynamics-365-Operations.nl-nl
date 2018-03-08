---
title: Personeelsacties [FAQ]
description: Dit onderwerp bevat antwoorden op vragen die u mogelijk hebt als uw organisatie personeelsacties gebruikt. Personeelsacties zijn aanvullende stappen die u moet voltooien wanneer u bepaalde personeelsgerelateerde taken uitvoert.
author: ShielaSogge
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 93004f45189d16e991a3962ef16b4a102caf07bd
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="personnel-actions-faq"></a>Personeelsacties [FAQ]

[!include[banner](includes/banner.md)]

Dit onderwerp bevat antwoorden op vragen die u mogelijk hebt als uw organisatie personeelsacties gebruikt. Personeelsacties zijn aanvullende stappen die u moet voltooien wanneer u bepaalde personeelsgerelateerde taken uitvoert. Voorbeelden van taken die mogelijk personeelsacties vereisten, zijn wanneer u nieuwe posities maakt, bestaande positiewaarden aanpast, nieuwe werknemers aanneemt, werknemers overdraagt, compensaties van werknemers wijzigt, positietoewijzingen wijzigt of werknemers beëindigt.

**Opmerking:** personeelsacties zijn alleen beschikbaar als de velden **Medewerkersacties inschakelen** en **Positieacties inschakelen** zijn ingesteld op **Ja** op het tabblad **Personeelsacties** op de pagina **Gedeelde Human resources-parameters**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Hoe weet ik of mijn organisatie personeelsacties vereist?
Uw organisatie vereist personeelsacties als u wordt gevraagd een personeelsactie te selecteren wanneer u nieuwe posities maakt, bestaande posities wijzigt, nieuwe werknemers aanwerft, werknemers overdraagt, werknemerscompensaties wijzigt, positietoewijzingen wijzigt, werknemers beëindigt of verlof invoert voor werknemers. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Wat is het verschil tussen een positie-actie en een werknemersactie?
Er zijn twee typen personeelsacties:

- Positieactie: Een positieactie wordt uitgevoerd voor bestaande posities of nieuwe posities. Een positieactie kan bijvoorbeeld zijn vereist als u een waarde op een bestaande positie wijzigt of als u een nieuwe seizoengebonden positie maakt. Zie voor meer informatie over het gebruik van de positieacties de onderwerpen Belangrijke taken: Bestaande werknemerposities en Belangrijke taken: Nieuwe werknemerposities.

- Medewerkersactie: Een werknemersactie wordt uitgevoerd op bestaande werknemers of nieuwe werknemers. Een werknemersactie kan bijvoorbeeld worden vereist wanneer een nieuwe werknemer in dienst wordt genomen of een bestaande werknemer promotie krijgt. Zie voor gedetailleerde informatie over het gebruik van werknemeracties het onderwerp Personeelsacties toewijzen aan werknemers.

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Wat betekent de status van de personeelsacties?
Personeelacties kunnen een van de volgende statussen hebben:

- **Concept**: Als de werkstroom wordt gebruikt, is de actie niet verzonden. Als werkstroom niet wordt gebruikt, is de actie niet voltooid.
- **Wordt gecontroleerd**: De personeelsactie is ingediend bij de werkstroom, maar de werkstroom is niet voltooid.
- **Goedgekeurd in afwachting**: De werkstroom is voltooid, maar de wijzigingen zijn nog in uitvoering. Geannuleerd: De werkstroom is geannuleerd of de personeelsactie is ingetrokken. Afgewezen: De actieaanvraag is afgewezen door de fiatteur.
- **Verwerking van actie**: De actieaanvraag is goedgekeurd en de wijzigingen worden verwerkt.
- **Workflow voltooid**: De werkstroom is voltooid en de wijzigingen zijn verwerkt. Mislukt: De werkstroom is mislukt omdat de gegevens verouderd zijn. Klik op Opnieuw activeren om de meest recente informatie weer te geven en verder te gaan.
- **Voltooid**: De positie is gemaakt of gewijzigd, of de werknemer was succesvol in dienst genomen, overgeplaatst of ontslagen, of diens compensatie werd gewijzigd. Fout: Er deed zich een ander probleem voor dan verouderde informatie. Open het Berichtenlogboek personeelsacties om de oorzaak van de fout te bepalen.
- **Geweigerd**: De actieaanvraag is afgewezen door de fiatteur.

## <a name="can-i-delete-a-personnel-action"></a>Kan ik een personeelsactie verwijderen?
Ja, u kunt personeelsacties verwijderen die een status **Concept**, **Fout**, **Mislukt** of **Geannuleerd** hebben.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Wat is de snelste manier om de status van een personeelsactieaanvraag te bekijken?
Open een van de lijstpagina's van de personeelsacties en selecteer een personeelsactie.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Wat kan ik doen als een personeelsactieaanvraag mislukt?
Als een personeelsactieaanvraag mislukt, moet u deze stappen volgen om de fout op te lossen en de aanvraag opnieuw in te dienen:

> 1. Klik in het **Actievenster** op de knop **Fouttekst** om de berichttekst weer te geven die het probleem beschrijft.

> 2. Klik in het **Actievenster** op **Opnieuw activeren** om de meest recente informatie te laden en de status van de personeelsactie terug te zetten op **Concept**.

> 3. Los de fout op en klik vervolgens op **Voltooien** of **Verzenden**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Wat gebeuren er met een personeelsactie die werkstroom gebruikt wanneer de definitieve goedkeuring is voltooid?
Als er geen fouten zijn, wordt de personeelsactie alleen-lezen. (U kunt de historie bekijken op de lijstpagina **Alle medewerkersacties**, maar u kunt de personeelsactie niet wijzigen.) Wanneer de status van een personeelsactie **Voltooid** is, is de positie- of werknemerrecord al bijgewerkt. Om de wijzigingen weer te geven die zijn uitgevoerd, opent u de lijstpagina **Posities** of **Medewerkers**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Waarom ontvang ik de volgende fout wanneer ik een niet-nulwaarde in het veld Salaristarief invoer? “De waarde valt buiten het geldige bereik. De waarde moet liggen tussen 0.00 en 0.00“
U ziet dit bericht omdat het veld Niveau in het formulier Functie leeg is voor de functie die aan de geselecteerde positie is gekoppeld.

Om deze fout op te lossen, volgt u deze stappen:

> 1. Klik in het formulier Positietoewijzingen medewerker op het veld Positie.  
> 2. Klik op de waarde van het veld Functie om het formulier Functie te openen.
> 3. Klik in het actievenster op Bewerken.
> 4. Klik op het tabblad Compensatie.
> 5. Selecteer een niveau in het veld Niveau.
> 6. Sluit de pagina Functie.
> 7. Sluit de pagina Positie.
> 8. Ga terug naar het tabblad Compensatie op de pagina Medewerker en selecteer Vaste compensatie.  Selecteer Nieuw en voer de positie van de werknemer in het veld Positie in.  Voer een waarde in het veld Plan in en voer vervolgens de compensatie van de werknemer in het veld Loontarief in.

## <a name="why-cant-i-change-the-effective-date-in-the-header-of-the-worker-action-form"></a>Waarom kan ik de ingangsdatum niet wijzigen in de koptekst van het formulier van de Werknemersactie?
U kunt de ingangsdatum niet wijzigen omdat het veld is ingevuld met de meest logische datum voor het actietype.

Bijvoorbeeld:

- De ingangsdatum in de koptekst van een actie **Een medewerker ontslaan** is de datum die u in het veld **Ontslagdatum** voor de werknemer hebt ingevoerd.
- De ingangsdatum van een actie **Een medewerker aannemen** is de datum die u in het veld **Begindatum dienstverband** hebt ingevoerd.
- De ingangsdatum van een actie **Een medewerker overplaatsen** is de datum die u in het veld **Begindatum van toewijzing** voor de medewerker hebt ingevoerd.


