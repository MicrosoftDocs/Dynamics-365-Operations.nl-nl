---
title: Startpagina van Organisatiebeheer
description: Dit onderwerp verwijst naar resources die u helpen in uw organisatie.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36784311294f80f56f680cd6d14cc989b629ba12
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177251"
---
# <a name="organization-administration-home-page"></a>Startpagina van Organisatiebeheer

[!include [banner](../includes/banner.md)]

Dit onderwerp verwijst naar inhoud die hoofdgebruikers en beheerders zal helpen het systeem te configureren zodat dit vloeiend en effectief werkt voor uw organisatie en zakelijke activiteiten.

Veel van de hier vermelde informatie is van toepassing op functies in de module **Organisatiebeheer**. Er zijn echter enkele taken, zoals het maken en gebruiken van een recordsjabloon, die in elke module kunnen worden uitgevoerd om uw organisatie efficiënter te laten werken.

## <a name="number-sequences"></a>Nummerreeksen

Nummerreeksen worden gebruikt om leesbare, unieke id´s te maken voor hoofdgegevensregistraties en transactieregistraties die deze nodig hebben. Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een *verwijzing* genoemd. Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen.

- [Overzicht van nummerreeksen](number-sequence-overview.md)
- [Nummerreeksen instellen met een wizard](tasks/set-up-number-sequences-wizard.md) (taakbegeleiding)
- [Nummerreeksen op een individuele basis instellen](tasks/set-up-number-sequences-individual-basis.md) (taakbegeleiding)

## <a name="organizations"></a>Organisaties

Een organisatie is een groep mensen die samenwerkt om een bedrijfsproces uit te voeren of een doel te bereiken. Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat.

Voordat u de installatieorganisaties en organisatiehiërarchieën instelt, moet u plannen hoe uw bedrijf wordt gemodelleerd. Het organisatiemodel heeft een aanzienlijk effect op implementatie- en op bedrijfsprocessen.

- [Organisaties en organisatiehiërarchieën](organizations-organizational-hierarchies.md)
- [Uw organisatiehiërarchie plannen](plan-organizational-hierarchy.md)
- [Een organisatiehiërarchie maken](tasks/create-organization-hierarchy.md) (taakbegeleiding)
- [Een rechtspersoon selecteren](tasks/create-legal-entity.md) (taakbegeleiding)
- [Een operationele eenheid maken](tasks/create-operating-unit.md) (taakbegeleiding)

## <a name="address-books"></a>Adresboeken

Het algemene adresboek is een centrale opslagplaats voor hoofdgegevens die moet worden opgeslagen voor alle interne en externe personen en organisaties waarmee het bedrijf werkt. De gegevens die zijn gekoppeld aan records van partijen bevatten de naam, het adres en de contactgegevens van partijen.

Nadat u het algemene adresboek hebt gemaakt, kunt u desgewenst extra adresboeken maken, zoals een apart adresboek voor elk bedrijf in uw organisatie of voor elke bedrijfstak.

- [Globaal adresboek](overview-global-address-book.md)
- [Plannen hoe u het algemene adresboek en extra adresboeken configureert](plan-configuration-global-address-book-additional-address-books.md)
- [Het globale adresboek configureren](tasks/configure-global-address-book.md)
- [Veelgestelde vragen over adresboeken](qa-address-books.md)

## <a name="workflow"></a>Werkstroom

Workflow is een systeem waarmee u afzonderlijke workflows of bedrijfsprocessen kunt maken. Wanneer u een workflow maakt, geeft u op hoe een document zich door het systeem begeeft of stroomt door aan te geven wie een taak moet voltooien, een beslissing moet nemen of een document moet goedkeuren.

- [Workflowoverzicht](overview-workflow-system.md)
- [Workflowelementen](workflow-elements.md)
- [Workflowacties](workflow-actions.md)
- [Een workflow maken](create-workflow.md)

## <a name="electronic-signatures"></a>Elektronische handtekeningen

Met een elektronische handtekening wordt de identiteit bevestigd van een persoon die een computerproces wil starten of goedkeuren. In bepaalde bedrijfstakken is een elektronische handtekening in dezelfde mate juridisch bindend als een handtekening die met de hand is geschreven. Elektronische handtekeningen zijn volgens de wetgeving vereist voor verschillende gereguleerde bedrijfstakken, zoals farmaceutische bedrijven, voedsel en drank, de ruimtevaartindustrie en defensie.

U kunt elektronische handtekeningen gebruiken voor belangrijke bedrijfsprocessen. Een aantal processen bevat ingebouwde functies voor elektronische handtekeningen. Daarnaast kunt u aangepaste vereisten voor handtekeningen maken voor databasetabellen en -velden.

- [Overzicht van elektronische handtekeningen](electronic-signature-overview.md)
- [Elektronische handtekeningen instellen](tasks/set-up-electronic-signatures.md) (taakbegeleiding)

## <a name="case-management"></a>Casebeheer

Door aanvragen te plannen, te traceren en te analyseren kunt u efficiënte oplossingen ontwikkelen die voor vergelijkbare problemen kunnen worden gebruikt. Zo kunnen medewerkers van de klantenservice of HRM-medewerkers bij het maken van een aanvraag kennisartikelen raadplegen waarin ze kunnen nalezen hoe ze aanvragen kunnen behandelen of efficiënter kunnen oplossen.

- [Overzicht van casebeheer](cases.md)
- [Casebeveiliging, -processen en -categorieën configureren](plan-case-management.md)

## <a name="record-templates"></a>Recordsjablonen

Met recordsjablonen kunt u sneller records maken. U kunt een recordsjabloon maken, zodat vaak gebruikte veldwaarden niet expliciet hoeven te worden ingevoerd voor elke nieuwe record.

- [Recordsjablonen](record-templates.md)
- [Een recordsjabloon maken om de invoer van gegevens te vergemakkelijken](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (taakbegeleiding)
- [Een nieuwe record maken met behulp van een recordsjabloon](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (taakbegeleiding)

## <a name="general-organization-administration"></a>Algemeen organisatiebeheer

- [Banner of logo wijzigen](../get-started/tasks/change-banner-or-logo.md) (taakbegeleiding)
- [Documentbeheer configureren](configure-document-management.md)
- [E-mail configureren en verzenden](configure-email.md)
- [Datum-/tijdgegevens en tijdzones](date-time-zones.md)
