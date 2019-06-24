---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (13 mei 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591497"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (13 mei 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="coming-soon-in-attract"></a>Binnenkort in Attract

### <a name="job-approvals-on-home-page"></a>Taakgoedkeuringen op startpagina

Goedkeuringen worden weergegeven in de sectie **Goedkeuringen** op het dashboard. Fiatteurs kunnen hun goedkeuringen controleren onder **Aan u toegewezen**, waarin de taak-ID, titel, andere fiatteurs en toewijzingsdatum worden weergegeven. Gebruikers die een taak ter goedkeuring indienen, kunnen hun taken controleren onder **Aangevraagd door u**, waar de fiatteurs worden weergegeven die de ingediende taak nog moeten goedkeuren.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2297. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Exemplaartype aangeven bij het inrichten van Talent

Bij het inrichten van een nieuw exemplaar van Talent kunt u aangeven of het exemplaartype **Productie** of **Sandbox** is, waardoor nieuwe functies vroegtijdig kunnen worden getest. Alle bestaande exemplaren van Talent worden bijgewerkt naar het exemplaartype **Productie**. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype **Sandbox**, neemt u contact op met de [ondersteuning](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) om de wijzigingsaanvraag te initiëren.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Ondersteuning van Common Data Service-entiteiten voor aangepaste velden

In de release van deze week ondersteunen de volgende Common Data Service-entiteiten nu aangepaste velden: Aanstelling, Berekeningsfrequentie vergoeding, Berekeningstarief vergoeding, Werkkalender feestdag en Identificatietype.

### <a name="common-data-service-integration-page"></a>De pagina Common Data Service-integratie

Deze release bevat een nieuwe optie in **Systeembeheer > Koppelingen > Integraties > Common Data Service-configuratie**. De optie **Common Data Service-configuratie** biedt een beheerder of beheerder van gegevensbeheer enige flexibiliteit en inzichten met de Common Data Service. Met deze optie kunt u de integratie van Common Data Service met een exemplaar van Talent in- of uitschakelen en de synchronisatiegegevens tussen het exemplaar van Talent en Common Data Service weergeven.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Prestatiegegevens met definitieve werknemersbeoordeling importeren (316710)

In deze versie kunt u historische werknemersbeoordelingsgegevens importeren. Voor het veld **FinalEmployeeRatingId** gelden nu schrijfmachtigingen.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Kan geen werknemersadres maken in Common Data Service en synchroniseren met Talent (317555)

Dankzij deze wijziging kunnen adresgegevens gemaakt in Common Data Service worden gesynchroniseerd met Talent.

## <a name="in-preview"></a>Preview

### <a name="new-page-to-validate-position-hierarchy-data"></a>Nieuwe pagina voor validatie van positiehiërarchiegegevens

Human Resources (HR) en beheerders kunnen de managementhiërarchie valideren voor kringverwijzingen die onbedoeld zijn geïmporteerd. U kunt deze nieuwe pagina openen vanuit **Organisatiebeheer > Koppelingen > Posities > Validatie van positiehiërarchie**.

### <a name="specify-reason-codes-on-leave-types"></a>Redencodes opgeven voor verloftypen

Organisaties hebben mogelijk extra informatie over verlofaanvragen nodig. U kunt nu redencodes voor verloftypen opgeven en toestaan dat werknemers een redencode in hun verlofaanvragen selecteren.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Redencodes voor specifieke verloftypen vereisen voor verlofaanvragen

Organisaties vereisen wellicht redencodes voor specifieke verloftypen wanneer werknemers verlofaanvragen indienen. Deze vereiste kan bestaan vanwege bedrijfsbeleid of wettelijke vereisten. U kunt opgeven welke verloftypen een redencode vereisen en u kunt vereisen dat werknemers een redencode opgeven voor het verloftype in hun verlofaanvragen.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Een lijst met verlof- en afwezigheidstransacties verschaffen voor HR

De mogelijkheid om verlof van werknemers bij te houden en inzicht te krijgen in de berekening van verlof helpt HR niet alleen bij het beantwoorden van werknemersvragen, maar helpt tevens nauwkeurige verloftoekenningen voor werknemers te waarborgen. HR heeft nu een nieuwe weergave om de transacties te bekijken (toekenningen, toerekeningen, correcties en aanvragen) zodat HR-medewerkers de redenen achter verlofsaldi kunnen bekijken.
