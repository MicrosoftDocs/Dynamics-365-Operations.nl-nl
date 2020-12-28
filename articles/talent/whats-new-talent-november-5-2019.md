---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (5 november 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4068cf81782d2f9559179b91da31e049c006059
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527115"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (5 november 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2598. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Een Core HR-exemplaar kopiëren

In de release van deze week kunt u Microsoft Dynamics Lifecycle Services (LCS) gebruiken om een Microsoft Dynamics 365 Talent: Core HR-database naar een sandbox-omgeving te kopiëren. Als u nog een sandbox-omgeving hebt, kunt u de database ook vanuit die omgeving kopiëren naar een specifieke sandbox-omgeving. Ga voor meer informatie naar:

- [Uitgebreider omgevingsbeheer](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in het Dynamics 365: releasewave 2-plan van 2019

- [Een Core HR-exemplaar kopiëren](hr-copy-instance.md) in Talent-documentatie

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service-integratiebatchtaken worden niet gemaakt wanneer Common Data Service-integratie is ingeschakeld (388030)

Door deze wijziging worden er batchtaken gemaakt voor Common Data Service-integratie wanneer deze is ingeschakeld.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity past het formaat van de persoonsafbeelding niet aan bij het uploaden (369469)

De release van deze week verandert hoe de grootte van afbeeldingen wordt gewijzigd voor betere prestaties wanneer deze worden geïmporteerd via gegevensbeheer.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>De datum Beschikbaar voor toewijzing van een positie kan voor de activeringsdatum vallen (340103)

Bij deze wijziging wordt er een waarschuwing weergegeven als u een datum bij **Beschikbaar voor toewijzing** selecteert die eerder is dan de **activeringsdatum** van de positie.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Kan geen aanvraag voor compensatiewijziging in de selfservice voor werknemers maken voor op stappen gebaseerde plannen (376872)

Deze release corrigeert een probleem bij het aanvragen van compensatiewijzigingen via de selfservice voor werknemers voor op stappen gebaseerde plannen. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Redencode wordt niet gesynchroniseerd met Common Data Service als de beschrijving langer is dan 30 tekens. Core HR staat er 60 toe (352682)

Met deze wijziging worden redencodes met meer dan 30 tekens bijgewerkt in Common Data Service. Wijzigingen die in Common Data Service worden aangebracht, worden ook weer doorgevoerd in Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Adresintegratie van Talent naar Finance and Operations (351961)

Met deze release wordt een probleem gecorrigeerd waarbij adressen die in Talent worden bijgewerkt, niet worden bijgewerkt in Finance and Operations. Wijzigingen in adresblokken worden nu bijgewerkt.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="print-performance-reviews"></a>Prestatiebeoordelingen afdrukken

Zie [Beoordelingen van afdrukprestaties](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in het Dynamics 365: releasewave 2-plan van 2019.

### <a name="feature-management-workspace"></a>Werkgebied Functiebeheer

Functies worden toegevoegd en bijgewerkt in elke release. De Functiebeheerervaring biedt een werkgebied waarin u een lijst met functies kunt weergeven die in elke release zijn geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven.

Voor meer informatie over de wijzigingen in functiebeheer raadpleegt u [Overzicht van Functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
