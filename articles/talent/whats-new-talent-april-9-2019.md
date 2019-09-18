---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (9 april 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4959f28e0768d43f90a664022c714a126c88e38d
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856419"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-9-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (9 april 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>LCS-integratie (Lifecycle Services) met 'Een probleem melden'
In Attract en Onboard worden met problemen die zijn geregistreerd door eindgebruikers met de functie Een probleem melden, nu automatisch ondersteuningsproblemen gemaakt in het LCS-project van de klant. Beheerders kunnen vervolgens de problemen beoordelen en zo nodig indienen bij Microsoft. Dit komt overeen met hoe Core HR ondersteuningsproblemen van eindgebruikers afhandelt.

### <a name="relevance-search"></a>Relevante zoekopdracht
In talentenpools kunt u nu in uw gehele database met kandidaten zoeken naar bepaalde vaardigheden, namen of opleidingsachtergrond. U hoeft niet meer op te geven in welke sectie van een kandidaatprofiel u wilt zoeken. Attract zoekt in het gehele profiel en markeert alle gevonden overeenkomsten. Attract zoekt ook in alle documenten die beschikbaar zijn voor een kandidaat en rangschikt de zoekresultaten op intelligente wijze. Bovendien kunt u de resultaten per bron of op de status van tweede plaats filteren. Zie voor meer informatie [Kandidaatprofielen doorzoeken en weergeven](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Prospectaanbevelingen
Attract kan helpen bij het zoeken naar resources voor een functie zodra u deze activeert door intelligente kandidaataanbevelingen te doen op basis van de database met kandidaten. De aanbevelingen omvatten de vaardigheden en opleidingsinformatie die zijn geïdentificeerd tijdens het zoeken naar relevante prospects. Deze aanbevelingen worden weergegeven op het tabblad **Prospects** onder een functie, als u het inschakelt tijdens het aanstellingsproces van de functie. Zie [Prospectaanbevelingen](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations) voor meer informatie.

### <a name="interviewer-availability-statuses"></a>Beschikbaarheidsstatussen van interviewer
Planners van sollicitatiegesprekken kunnen binnenkort de statussen **Niet op kantoor, is elders aan het werk** zien voor interviewers zodat ze gemakkelijker tijden kunnen inplannen die beter werken voor interviewers.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Sollicitatiegesprekervaring van kandidaten: kalenderuitnodigingen opslaan
Kandidaten kunnen nu hun sollicitatiegesprekgebeurtenissen downloaden en opslaan in hun persoonlijke agenda's met behulp van een ICS-bestand dat is bijgevoegd bij de aan de kandidaat verzonden e-mail met het sollicitatiegespreksoverzicht.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>LCS-integratie (Lifecycle Services) met Een probleem melden
In Attract en Onboard worden met problemen die zijn geregistreerd door eindgebruikers met de functie Een probleem melden, nu automatisch ondersteuningsproblemen gemaakt in het LCS-project van de klant. Beheerders kunnen vervolgens de problemen beoordelen en zo nodig indienen bij Microsoft. Dit komt overeen met hoe Core HR ondersteuningsproblemen van eindgebruikers afhandelt.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR
Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Voor percentage van variabele basisregelingen wordt een onjuiste bedrag geladen
Met de release van deze week wordt een probleem opgelost bij het laden van variabele compensatietoekenningen met een percentage van basisregelingen.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Datumkiezer op laatste werkdag werkt niet goed
Met deze wijziging wordt het probleem opgelost waarbij een dag wordt toegevoegd aan de selectie wanneer gebruikers de **Einddatum dienstverband** bewerken en de datum selecteren met het kalenderbesturingselement.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Personeelsactietypen beperken tot de ondernomen actie
Met deze wijziging worden de actietypen beperkt die worden weergegeven wanneer specifieke acties worden ondernomen. Wanneer bijvoorbeeld een nieuwe positie wordt aangevraagd, worden alleen de nieuwe positieacties weergegeven in de lijst met te selecteren acties. Eerder werden zowel nieuwe als bewerkte acties weergegeven. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Een werknemer met compensatie in een tweede rechtspersoon overplaatsen
In deze release kan compensatie worden beëindigd in een tweede rechtspersoon als de overplaatsing tussen bedrijven plaatsvindt.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Er kan geen compensatie worden geselecteerd voor een toekomstig dienstverband tijdens een overplaatsing
Wanneer een werknemer wordt overgeplaatst naar een nieuwe rechtspersoon, kunt u nu compensatie instellen voor de nieuwe rechtspersoon tijdens de overplaatsing.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Gebruiker kan geen compensatie toewijzen tijdens positietoewijzing
Als een nieuwe positietoewijzing wordt toegevoegd, kunnen voortaan records voor vaste compensatie worden ingesteld. 

## <a name="in-preview"></a>Preview

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Toestaan dat redencodes voor verloftypen worden opgegeven
Organisaties hebben mogelijk extra informatie over verlofaanvragen nodig. U kunt nu redencodes voor verloftypen opgeven en mogelijk maken dat werknemers een redencode in hun verlofaanvragen selecteren.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Redencodes voor bepaalde verloftypen vereisen voor verlofaanvragen
Organisaties kunnen redencodes vereisen voor specifieke verloftypen wanneer werknemers verlofaanvragen indienen. Dit kan te maken hebben met bedrijfsbeleid of wettelijke vereisten. U kunt nu opgeven welke verloftypen een redencode vereisen en u kunt vereisen dat werknemers een redencode opgeven voor het verloftype in hun verlofaanvragen.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Lijst met verlof- en afwezigheidstransacties verschaffen voor HRM
Door verlof van werknemers bij te houden en inzicht te krijgen in de berekening van verlof helpt HR niet alleen bij het beantwoorden van werknemersvragen, maar zorgt tevens voor nauwkeurige verloftoekenningen voor werknemers. HR heeft nu een nieuwe weergave om de transacties te bekijken (toekenningen, toerekeningen, correcties en aanvragen) om de redenen te zien achter saldi. 

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Verbeteringen in de gebruikersinterface voor controle op dubbele werknemers
Met deze wijziging worden dubbele records gedetecteerd wanneer u naamvelden invoert en met een status wordt het aantal dubbelen weergegeven. U kunt de opgegeven koppeling selecteren om een nieuwe pagina te openen om te beoordelen of de gedetecteerde overeenkomst moet worden gebruikt. Om te voorkomen dat gegevensinvoer wordt onderbroken, wordt het formulier met dubbele records niet automatisch geopend.

###  <a name="email-support-for-alerts"></a>E-ondersteuning voor waarschuwingen
Met platformupdate 25 kunnen gebruikers waarschuwingsregels maken waarmee automatisch e-mailmeldingen worden verzonden naar contactpersonen wanneer deze door een gebeurtenis worden geactiveerd. 
