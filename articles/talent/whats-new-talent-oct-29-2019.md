---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (29 oktober 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529679"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (29 oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2586. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Partijen zonder rollen verwijderen moet standaard zijn ingeschakeld (371233)

Wanneer u een nieuwe omgeving inricht in Talent, is **Partijen zonder rollen verwijderen** standaard ingeschakeld. Wanneer u een werknemer verwijdert, wordt de partij die aan de werknemer is gekoppeld alleen verwijderd als deze instelling is ingeschakeld. Door deze wijziging worden dubbele records in het algemene adresboek beperkt wanneer u werknemers importeert, wijzigt of opnieuw importeert.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Concept- en geannuleerde verlofaanvragen moeten kunnen worden verwijderd in Common Data Service (376999)

Met deze wijziging kunt u nu verlofaanvragen met de status **Concept** of **Geannuleerd** in Common Data Service verwijderen.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Aanvullende lijstwaarden in aangepaste velden worden niet weergegeven in Common Data Service nadat u op Toepassen hebt geklikt in het formulier Aangepaste velden (379599)

Wanneer u nieuwe lijstwaarden toevoegt aan een bestaand aangepast veld dat al is gesynchroniseerd met Common Data Service, zijn deze nu beschikbaar in Common Data Service nadat u de wijzigingen hebt toegepast in het formulier **Aangepaste velden**.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Controlelijsten voor onboarden toepassen op rechtspersonen wanneer meer dan één dienstverband bestaat (371270)

In de release van deze week kunt u controlelijsten toepassen op werknemers met meer dan één werknemer in **Formulier Medewerker > Controlelijsten**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>De preview-functie Open inschrijving voor voordelen is verwijderd

In combinatie met onze mededeling in het blogbericht [Strategische investeringen Core HR dragen bij tot uitmuntendheid](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) heeft Microsoft de functie Open inschrijving voor voordelen uit de openbare preview-versie verwijderd. In de toekomst wordt nieuwe functionaliteit uitgebracht. Het productiegebruik van de functie voor open inschrijving voor voordelen wordt niet ondersteund.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="print-performance-reviews"></a>Prestatiebeoordelingen afdrukken

Zie [Beoordelingen van afdrukprestaties](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in het Dynamics 365: releasewave 2-plan van 2019.

### <a name="feature-management-workspace"></a>Werkgebied Functiebeheer

Functies worden toegevoegd en bijgewerkt in elke release. De Functiebeheerervaring biedt een werkgebied waarin u een lijst met functies kunt weergeven die in elke release zijn geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven.

Voor meer informatie over de wijzigingen in functiebeheer raadpleegt u [Overzicht van Functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]