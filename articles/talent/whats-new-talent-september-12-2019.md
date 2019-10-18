---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (10 september 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
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
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48f41b53060c7f2bfc407b22295aa40d85ce1c9d
ms.sourcegitcommit: 7a93ea2dc90d31175b708566a00cd707cb47ab7c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2019
ms.locfileid: "1996183"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (10 september 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="candidate-e-mail-login"></a>E-mail-aanmelding kandidaat

Kandidaten kunnen nu elk willekeurig e-mailadres gebruiken om een account te maken en zich aan te melden bij een carrièrewebsite van Talent om taken uit te voeren en hun toepassingsstatus te controleren. Dit komt nog bij de bestaande mogelijkheid om u aan te melden bij de Talent carrièresite met hun sociale accounts of hun organisatiereferenties.

### <a name="job-activation-and-posting"></a>Activering en boeking van taak

Er zijn enkele wijzigingen aangebracht in het activeren en boeken van een taak. U moet taken activeren voordat u ze boekt naar de carrièrewebsite van Talent of externe jobboards, waaronder LinkedIn of Broadbean.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2482. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>U kunt voorbeeld functies inschakelen in de Sandbox- en Testomgevingen

Wanneer u een nieuw exemplaar van Talent inricht, kunt u opgeven of het exemplaartype Productie of Sandbox is. In exemplaren van het type Sandbox kunnen nieuwe functies vroegtijdig worden getest. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype Sandbox, neemt u contact op met de ondersteuning om de wijzigingsaanvraag te initiëren.

Zie [Talent inrichten](./provisioning-talent.md) voor meer informatie over hoe wijzigingen worden gepubliceerd.

### <a name="platform-update-29"></a>Platformupdate 29

Zie voor meer details over platformupdate 29 [Voorbeeldfuncties in Dynamics 365 for Finance and Operations platformupdate 29 (oktober 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Nieuwe taak-basisentiteit beschikbaar voor de functie in Data Management Framework (347202)

Met deze versie is een nieuwe Taak-basisentiteit beschikbaar voor het importeren/exporteren van gegevens. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>In het geavanceerde beveiligingsbeleid voor werk nemers worden posities in de Positiehiërarchie onjuist weergegeven (354868)

In deze versie worden posities niet meer open weergegeven met een "lege" werknemer als gebruikers beperkte toegang hebben.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Taakformulier sluiten-vak sluit in bepaalde situaties het formulier niet (342467)

Deze versie bevat een wijziging waarmee het Taakformulier in alle scenario's kan worden gesloten.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Nieuwe case op werknemersrecord is vergrendeld voor de rol Human Resources Manager (337111)

Met deze wijziging wordt het formulier aanvraagbeheer niet meer vergrendeld wanneer u het opent vanuit het formulier werknemer.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>De einddatum van de dienst wordt altijd standaard ingesteld op 23:59:59 (351492)

Met deze wijziging kunt u de aanstellingsdatum wijzigen in een andere tijd dan 23:59:59 wanneer u een dienstverband handmatig beëindigt.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Kan geen vervaldatum voor een inkomstencode instellen via Gegevensbeheer (336604)

In deze versie kunt u verdiencodes instellen die via de entiteit **PayrollWorkerPositionEarningCodeEntity** verlopen.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Analytisch rapport werknemersontwikkeling toont geen gegevens (348737)

In de release van deze week is de analyse voor werknemersvaardigheden bijgewerkt om nauwkeurige rapportage te leveren.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Datum/tijd van de arbeidsvoorwaarden vallen niet standaard op het begin van de dag (349101)

Met deze wijziging worden de begindatum/-tijd nu standaard ingesteld op begin van de dag en de einddatum/-tijd standaard ingesteld op einde van dag.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Het wijzigen van de einddatum van het dienstverband op het Werknemersactieformulier geeft een fout weer (354092) 

Deze wijziging corrigeert het probleem bij het wijzigen van de einddatum van het dienstverband als onderdeel van de werknemersactie.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Controlelijsten voor onboarden toepassen op bedrijven (338433)

Met deze versie kunnen nu controlelijsten worden toegepast op werknemers die worden gebruikt in andere rechtspersonen dan de aangemelde rechtspersoon.

## <a name="in-preview"></a>Preview

### <a name="streamlined-employee-entry-and-navigation"></a>Gestroomlijnde invoer en navigatie voor werknemers

Deze functionaliteit is nu beschikbaar in sandbox-omgevingen. Als u deze functie wilt inschakelen, navigeert u naar **Systeembeheer > Koppelingen > Instellingen > Systeemparameters > Voorbeeldfuncties**. Selecteer **Verbeterd medewerkersformulier en navigatie**. Hierdoor worden deze wijzigingen voor alle gebruikers ingeschakeld. U kunt deze optie op elk gewenst moment uitschakelen.

Zie [Gestroomlijnde invoer en navigatie voor werknemers](./streamlined-employee-entry.md) voor meer informatie.
