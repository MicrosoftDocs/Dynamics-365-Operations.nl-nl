---
title: Nieuwe of gewijzigde functies in Dynamics 365 for Talent (25 juni 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
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
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e32768c898e2934b95eb8ab7b212337aff0c1556
ms.sourcegitcommit: fbe6d35ed35aa01f438990e2880c3a3cf223ea8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/27/2019
ms.locfileid: "1704464"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-25-2019"></a>Nieuwe of gewijzigde functies in Dynamics 365 for Talent (25 juni 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Binnenkort in Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Functiegoedkeuringen worden weergegeven op de startpagina

Goedkeuringen worden weergegeven in de sectie **Goedkeuringen** op het dashboard. Fiatteurs kunnen hun goedkeuringen controleren onder **Aan u toegewezen**, waar de taak-ID, functietitel, andere fiatteurs en de toewijzingsdatum worden weergegeven. Gebruikers die een functie ter goedkeuring indienen, kunnen hun functies controleren onder **Aangevraagd door u**, waar de fiatteurs worden weergegeven die de ingediende functie nog moeten goedkeuren.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard
Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Onjuiste waarde weergegeven voor Primaire positie (314266)

Door deze wijzigingen wordt de instelling **Primaire positie** instelling op alle pagina's consistent weergegeven.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Kan niet bewerken na het intrekken van de workflow in beoordeling (318180)

Beoordelingen die zijn ingetrokken via een workflow kunnen nu worden bewerkt.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Het veld Laatste opmerkingen in beoordelingen wordt niet vertaald (325921)

Het label **Laatste opmerkingen** wordt vertaald in Talent.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Preview-functies worden alleen ingeschakeld in sandbox-omgevingen

Wanneer u een nieuw exemplaar van Talent inricht, kunt u aangeven of het exemplaartype **Productie** of **Sandbox** is. In het exemplaartype **Sandbox** kunnen nieuwe functies vroegtijdig worden getest. Alle bestaande exemplaren van Talent worden bijgewerkt naar het exemplaartype **Productie**. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype **Sandbox**, neemt u contact op met de [ondersteuning](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) om de wijzigingsaanvraag te initiëren.

Zie [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) voor meer informatie over hoe wijzigingen worden gepubliceerd.

## <a name="in-preview"></a>Preview

### <a name="restrict-the-leave-types-in-time-off-requests"></a>De verloftypen in verlofaanvragen beperken

Organisaties kunnen veel verloftypen aanbieden aan werknemers. Sommige verloftypen zijn mogelijk niet geschikt voor werknemers . Deze verloftypen kunnen in plaats daarvan door HR worden beheerd. In deze versie kunt u configureren voor welke typen verlof werknemers verlofaanvragen kunnen indienen. 

## <a name="coming-soon-in-core-hr"></a>Binnenkort in Core HR

### <a name="feature-management-area-in-talent"></a>Het gebied Functiebeheer in Talent

**Functiebeheer** wordt verwijderd uit **Systeembeheer** vanwege problemen met de functie. **Functiebeheer** wordt in een toekomstige versie opnieuw geïntroduceerd. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Ondersteuning van Common Data Service-entiteiten voor aangepaste velden

De volgende entiteiten ondersteunen aangepaste velden: **Salarisinkomstencode**, **Vaste compensatiegebeurtenis**, **Compensatieraster**, **Salarisperiode** en **cCompensatiereferentiepunt**. 

### <a name="new-common-data-service-entities"></a>Nieuwe Common Data Service-entiteiten

De entiteit **Redencodes** wordt toegevoegd aan Common Data Service.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Informatie over prestaties voor directe en indirecte ondergeschikten in de selfservice-functionaliteit voor managers weergeven

Met een nieuwe optie kunnen managers de prestaties van hun directe en indirecte ondergeschikten weergeven. Op dit moment kunnen lijnmanagers prestatiedoelstellingen toewijzen en bijwerken, en nieuwe beoordelingen uitgeven. Bovendien kunnen directe leidinggevenden en hun werknemers prestatiejournalen onderhouden en bijwerken om ervoor te zorgen dat het proces voor prestatiebeoordelingen soepel verloopt. Wanneer deze wijziging is geïmplementeerd, kunnen managers prestatiegerelateerde gegevens weergeven en beheren voor indirecte en directe ondergeschikten.

### <a name="print-performance-reviews"></a>Prestatiebeoordelingen afdrukken

Werknemers, managers en HR kunnen de prestatiebeoordeling van een werknemer afdrukken.