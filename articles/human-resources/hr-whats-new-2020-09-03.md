---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (03 september 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 3 september 2020.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d1cc3a64e6c345df7727f5ca7336821388c9dbcf
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063538"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (3 september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources. Wijzigingen die van toepassing zijn op buildnummer 8.1.3504. De getallen tussen haakjes in sommige koppen verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).

Zie [overzicht van Dynamics 365 Human Resources 2019 releasewave 2 voor meer informatie over geplande functies in HRM](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Zie [Het updateproces](hr-admin-setup-update-process.md) voor meer informatie over het updateproces voor Human Resources.

## <a name="in-this-release"></a>In deze versie

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Nieuw standaardpatroon voor raster en dialoogvenster voor financiële dimensies in Human Resources (469495)

Het nieuwe patroon voor financiële dimensies is nu beschikbaar op de volgende gebieden:

- Positieacties (formulier: **HcmPositionActionDetail**)
- Inkomstencodes voor salarissen (formulier: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Vermeldingen worden niet weergegeven in de verlofkalender van het bedrijf als kalenderverbeteringen voor verlof en verzuim niet zijn ingeschakeld (484406)

Met deze versie wordt een probleem opgelost waarbij verlofitems niet worden weergegeven in de verlofkalender van het bedrijf. Dit probleem treedt alleen op als de optie **Kalenderverbeteringen voor verlof en verzuim** in Functiebeheer niet is ingeschakeld.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity-probleem (467597)

Deze release corrigeert een probleem met de entiteit **BenefitsPlanEmployee**. Bij het importeren van medewerkersinschrijvingen worden **Dekkingscode** en **Plantypecode** nu juist ingesteld. Door dit probleem werden vergoedingsplannen van werknemers onjuist weergegeven in het formulier **Medewerkersvergoedingenplan** en in het formulier **Open inschrijving** in Selfservice voor werknemers.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>In uitvoer van elektronisch bestand 1094-C ontbreekt een letter in XML (435190)

Deze wijziging corrigeert een probleem met het 1094-C-uitvoerbestand waarin een teken ontbreekt dat nodig is bij het indienen bij de belastingdienst (IRS).

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Tabel met variabele compensatie voor werknemers die is toegewezen aan het formulier voor vaste compensatie (476117)

Met deze wijziging worden de velden voor vaste compensatie uitgelijnd met het formulier voor vaste compensatie. Velden voor variabele compensatie zijn nu alleen beschikbaar met het formulier voor variabele compensatie.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Verlofaanvragen toegestaan vóór inschrijving als dat verloftype een negatief minimumsaldo heeft (469917)

Deze wijziging verhindert het invoeren van verlofaanvragen voordat deze in het plan worden ingeschreven, zelfs als de inschrijving een negatief minimumsaldo heeft. U kunt alleen aanvragen invoeren of indienen wanneer het plan actief is.

### <a name="document-templates-dont-download-457279"></a>Documentsjablonen worden niet gedownload (457279)

Door deze wijziging kunt u nu alle documentsjablonen downloaden. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Gegevens worden als kolomkoppen weergegeven in plaats van als rijen voor het veld Loontarief in het compensatieplanrapport (476077)

In het analyserapport wordt nu de juiste informatie voor **Loontarief** weergegeven.

## <a name="in-preview"></a>Preview

### <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Ga voor meer informatie naar:

- [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 1-plan
- [Human Resources-app in Teams](./hr-admin-teams-leave-app.md) in Human Resources-documentatie

### <a name="human-resources-app-in-teams-preview-features"></a>Preview-functies op Human Resources-app in Teams
 
-  **Meldingen**: inzenders en goedkeurders van verlofaanvragen worden in de Human Resources-app in Teams geïnformeerd. Fiatteurs kunnen verlofaanvragen goedkeuren of weigeren. Voor indieners wordt een melding weergegeven als de aanvraag is goedgekeurd of geweigerd. Ga voor meer informatie naar:
   - [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 2-plan
   - [Meldingen inschakelen voor de Human Resources-app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources-documentatie
   - [Teams-meldingen in- of uitschakelen voor individuele gebruikers](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources-documentatie
   - [Teams-meldingen](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources-documentatie
   - [De verlofkalender van uw team weergeven](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources-documentatie
 
- **Verlofagenda van manager**: managers kunnen goedgekeurde en in behandeling zijnde verlofaanvragen van hun ondergeschikten in een kalenderweergave bekijken. Deze weergave geeft duidelijk weer wanneer teamleden afwezig zijn. Ga voor meer informatie naar:
   - [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 2-plan
   - [De verlofkalender van uw team weergeven](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources-documentatie

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Configuratieoptie om de lijst Aan mij toegewezen werkitems te positioneren (477004)

Er is nu een nieuwe optie beschikbaar om de lijst **Aan mij toegewezen werkitems** in de rechterkolom van het dashboard te positioneren. Met deze wijziging worden alle werkitems en takenlijsten in hetzelfde gebied weergegeven. Schakel deze functionaliteit in door **Preview - Verbeteringen in werkstroomervaring** in Functiebeheer in te schakelen. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van preview-functies.

Deze functie bevordert ook de werkstroomopties die worden weergegeven in de formulieren voor personeelsacties. Werkstroomopties worden ook boven het sneltabblad Actie weergegeven voor snelle toegang. Ga voor meer informatie naar: 

- [Verbeteringen in de werkstroom voor organisatie- en personeelsbeheer](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in het Dynamics 365 2020 releasewave 2-abonnement

![Aan mij toegewezen werkitems.](./media/hr-workflow-work-items-assigned-to-me.png)

![Snelle toegang tot werkstroomitems.](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="checklist-entities-included-in-dataverse"></a>Check List-entiteiten opgenomen in Dataverse

Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.

### <a name="benefits-management-reason-codes"></a>Redencodes voor vergoedingenbeheer

Redencodes voor vergoedingenbeheer worden binnenkort gecombineerd met bestaande redencodes in Human Resources. Als u redencodes van meer dan 15 tekens hebt gemaakt in Vergoedingenbeheer, moet u de naam van de redencodes in het formulier **Redencodes** wijzigen in een code van maximaal 15 tekens. Nadat u de naam hebt bijgewerkt, wordt de redencode weergegeven onder het bestaande redencodeformulier in Personeelsbeheer. Deze wijziging wordt in de toekomst beschikbaar en heeft geen invloed op bestaande functionaliteit.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
