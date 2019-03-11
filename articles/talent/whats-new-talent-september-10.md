---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (10 september 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303946"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (10 september 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.138.0**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Specifieke tijd van de dag toestaan in verzoeken om verlof (halve dagen)

Als verlof en verzuim zo zijn ingesteld dat tijd vrijaf in dagen wordt ingediend, kunt u nu ook de definitie van een halve dag inschakelen. Wanneer gebruikers dan vrije tijd aanvragen, kunnen ze opgeven of ze de eerste helft of de tweede helft van de dag vrij willen zijn.

Standaard is deze optie uitgeschakeld. Werknemers kunnen de eerste of tweede helft van de dag alleen vrijaf nemen als u deze optie inschakelt in het gedeelte **Verlof en verzuim** van Parameters personeel.

De beveiligingsbevoegdheid voor deze functie is Parameters personeel onderhouden.

## <a name="validation-of-leave-and-absence-entries"></a>Validatie van verlof- en verzuimvermeldingen

Afhankelijk van hoe verlof is geconfigureerd, wordt voor een werknemer een waarschuwingsbericht weergegeven als deze een aanvraag voor verlof indient die meer tijd omspant dan zijn of haar werkdag. Met andere woorden, ze worden gewaarschuwd als ze meer dan een volledige dag op een bepaalde datum opnemen.

Deze validatie is altijd ingeschakeld. Wanneer werknemers de gedefinieerde drempelwaarde voor een dag overschrijden, ontvangen zij een waarschuwing in hun verlofaanvraag.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Extra velden voor voorwaardelijke instructies in workflows

Voor verschillende workflows in Core HR zijn extra velden toegevoegd aan voorwaardelijke instructies en tijdelijke aanduidingen.

De volgende velden zijn toegevoegd aan workflows voor compensatie, beëindiging en overdracht:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Positie
- Vakbond
- Departement
- PositionType
- CompLocation
- Titel
- Functie
- JobType
- JobFamily
- JobFunction

De volgende velden zijn toegevoegd aan de positieworkflow:

- Positie
- Vakbond
- Departement
- PositionType
- CompLocation
- Titel
- Functie
- JobType
- JobFamily
- JobFunction

Velden in voorwaardelijke instructies en tijdelijke aanduidingen zijn beschikbaar voor alle gebruikers die toegang hebben om de eerder genoemde workflows te configureren.

## <a name="navigation-to-attract-from-personnel-management"></a>Navigatie naar Attract vanuit Personeelsbeheer

Als Attract niet is ingesteld, worden gebruikers in Personeelsbeheer in de sectie **Kandidaten om in dienst te nemen** geïnstrueerd om aan de slag te gaan met Attract in plaats van dat het bericht Er is niets gevonden om hier weer te geven wordt weergegeven.

## <a name="other-changes"></a>Andere wijzigingen

Deze versie bevat verschillende aanvullende correcties:

- Wanneer een contractant wordt aangesteld, moet het tabblad **Compensatie** niet beschikbaar zijn op de aanvraag-/actiepagina.
- Tijdens het proces voor het aanvragen van ontslag kunt u pas doorgaan als alle vereiste velden gegevens bevatten.
- Problemen met de sorteervolgorde en weergave van datums in de analyses in Personeelsbeheer zijn opgelost.
