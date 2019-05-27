---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (16 april 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: adf8f470b00a565c62a27f857d490c6c000b21d8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517687"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-16-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (16 april 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="process-auditing"></a>Procescontrole

U kunt nu de wijzigingen bijhouden die zijn aangebracht in kandidaten, vacatures en sollicitaties. Zie [Wijzigingen bijhouden in wervingsgegevens](process-auditing.md) voor meer informatie.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2239. Getallen tussen haakjes verwijzen naar ondersteuningsnummers in Lifecycle Services (LCS).

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Entiteiten Compensatieregio, Compensatieniveau, Vergoedingsoptie en Vaardigheidstype in Common Data Service bijgewerkt met ondersteuning voor klantveld

In deze versie zijn deze Common Data Service-entiteiten bijgewerkt met de mogelijkheid om een aangepast veld op te nemen dat is toegevoegd via Talent (Core HR).

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a>Ondersteuning voor nieuwe Common Data Service-entiteiten voor: Compensatie vestigingsregels, Variabelecompensatieplan, Variabele compensatie

In deze release zijn de entiteiten Compensatie vestigingsregels, Variabelecompensatieplan, Variabele compensatie toegevoegd aan Common Data Service. Deze entiteiten ondersteunen ook aangepaste velden die zijn toegevoegd via Talent (Core HR).

### <a name="powerbi-refresh-issues-314342"></a>Problemen met vernieuwing in PowerBI (314342)

Via deze wijziging wordt een probleem bij het correct vernieuwen van PowerBI-rapporten opgelost.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>Het is niet mogelijk direct door te klikken bij overgangstaken in selfservice voor werknemers (303309)

Door deze wijziging kunnen gebruikers met de rol van werknemer overgangstaken selecteren en bijwerken vanuit de takenlijst van Talent.

### <a name="performance-feedback-email-message-updated-309615"></a>E-mailbericht met feedback over prestaties bijgewerkt (309615)

Met deze wijziging wordt er een bevestigingsbericht weergegeven bij indiening van feedback.

### <a name="missing-tables-in-word-template-308048"></a>Ontbrekende tabellen in Word-sjabloon (308048)

Met deze wijziging worden bij het maken van een Word-sjabloon met werknemer- en vaardigheidsgegevens alleen de vaardigheden voor de geselecteerde werknemer weergegeven in het Word-document.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>Bij het toepassen van een controlelijst voor offboarding wordt een fout weergegeven. (299877)

Met deze wijziging wordt een probleem verholpen bij rechtstreekse toepassing van een controlelijst voor offboarding vanuit het formulier van een werknemer.

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

### <a name="email-support-for-alerts"></a>E-ondersteuning voor waarschuwingen

Met platformupdate 25 kunnen gebruikers waarschuwingsregels maken waarmee automatisch e-mailmeldingen worden verzonden naar contactpersonen wanneer deze door een gebeurtenis worden geactiveerd.


