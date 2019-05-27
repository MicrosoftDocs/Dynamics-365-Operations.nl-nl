---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (5 maart 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e4ad32ef71c87f52e59959d80c21ae7fcd6d6524
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517747"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (5 maart 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="extending-option-sets-in-attract"></a>Optiesets uitbreiden in Attract

Attract bevat meerdere velden die optiesets zijn in Common Data Service. Er zijn nieuwe mogelijkheden geïntroduceerd om de optiesets uit te breiden, te beginnen met het veld **Reden voor afwijzing**, het veld **Type dienstverband** en het veld **Type anciënniteit**.

> [!IMPORTANT]
> De functionaliteit voor publicatie van vacatures naar LinkedIn vereist het gebruik van het veld **Type dienstverband** en het veld **Type anciënniteit** op de pagina **Functiedetails**. De standaardwaarden in deze velden worden ondersteund door LinkedIn en worden weergegeven wanneer de vacature wordt gepubliceerd. Als u vacatures naar LinkedIn publiceert en de bestaande optiesetwaarden voor deze velden wijzigt, wordt de vacature wel gepubliceerd, maar worden op LinkedIn de aangepaste waarden voor **Type dienstverband** en **Type anciënniteit** niet weergegeven.

## <a name="changes-in-onboarding"></a>Wijzigingen in Onboarding

### <a name="private-preview-for-onboard-teams"></a>Beperkte preview voor onboardteams
U kunt nu sjablonen gemakkelijk delen en gemakkelijk samenwerken aan sjablonen in uw gehele organisatie. Zie voor meer informatie [Best practices delen in uw organisatie met behulp van onboardteams](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Beperkte preview voor tijdelijke aanduidingen van toegewezene
U kunt uw sjablonen verrijken door activiteiten toe te wijzen aan rollen in plaats van aan individuen. Rollen worden vervolgens toegewezen aan individuen tijdens het maken van begeleiding. Zie voor meer informatie [Beheer van begeleiding stroomlijnen door activiteiten aan rollen toe te wijzen](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR
**Build 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Workflow configureren om workflow automatisch goed te keuren of workflow te volgen wanneer een HR- of lijnmanager verlofaanvragen indient of bijwerkt
Nieuwe workflowvoorwaarden zijn toegevoegd om toe te staan dat verlofaanvragen automatisch worden goedgekeurd als ze worden ingediend door de manager van een werknemer of door HR. Eén manier om deze automatische goedkeuring voor een workflow te bereiken, is een automatische actie voor de workflowgoedkeuring te activeren.

De voorwaarden die zijn toegevoegd, zijn:

- Ingediend door - gebruikt voor het evalueren van de systeemgebruikers-ID van de gebruiker die de aanvraag bij de workflow heeft ingediend.
- Ingediend uit naam van - gebruikt om te evalueren of de verlofaanvraag namens de werknemer is ingediend die is gekoppeld aan de aanvraag.
- Ingediend door HR - gebruikt om te evalueren of de systeemgebruiker die de aanvraag bij de workflow heeft ingediend, een HR-rol heeft.
- Ingediend door manager - gebruikt om te evalueren of de gebruiker die de verlofaanvraag bij de workflow heeft ingediend, een lijnhiërarchiemanager is van de werknemer die is gekoppeld aan de aanvraag.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Vaste compensatie voor werknemers activeren voor toekomstige positietoewijzingen
Vaak worden werknemers aan een organisatie toegevoegd met een toekomstige begindatum. Dankzij deze wijziging kan een vaste compensatie worden gedefinieerd voor werknemers met toekomstige positietoewijzingen.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Velden voor salaris positie zijn leeg bij het bewerken van de positie
Met deze wijziging worden de salarisvelden voortaan standaard ingesteld op de huidige waarden wanneer wijzigingen in bestaande posities worden aangevraagd.

### <a name="other-miscellaneous-bug-fixes"></a>Andere diverse correcties
Andere kleine correcties zijn opgenomen in deze release.

### <a name="upgrade-to-common-data-service"></a>Upgrade naar Common Data Service
Uiterste datums voor een upgrade naar Common Data Service naderen snel. Meld u aan bij het PowerApps-beheercentrum om te bepalen of een upgrade op uw database moet worden uitgevoerd. Zie voor meer informatie over uiterste datums en de nodige stappen om te upgraden [Upgraden naar Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Binnenkort beschikbaar

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Geavanceerde compensatiebeveiliging (vast en variabel)
In veel organisaties kunnen managers voor compensaties en vergoedingen alleen toegang verkrijgen tot bepaalde compensatierecords, zoals records voor leidinggevenden of werknemers op basis van regio. Met deze wijziging kunt u de compensatieplannen beheren en onderhouden voor verschillende werknemersgroepen in de organisatie. Aan vaste en variabele plannen kunnen beveiligingsrollen worden toegewezen, waarmee de toegang wordt bepaald tot de plannen en de werknemersgegevens met betrekking tot de plannen, zoals salaris- of bonusrecords. Alleen de rollen met de opgegeven toegang kunnen compensatie voor deze werknemers verwerken.

###  <a name="platform-update-24"></a>Platformupdate 24
Zie voor aanvullende informatie over Platform update 24 [Wat is nieuw of gewijzigd in Finance and Operations Platform update 24 (maart 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
