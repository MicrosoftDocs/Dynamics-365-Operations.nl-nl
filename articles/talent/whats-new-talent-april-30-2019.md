---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (30 april 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 112146ac46193e37b33bf429dc5a359f8cfaca94
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505364"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-30-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (30 april 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

De wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2270. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Feedback geven

De optie om feedback te geven bevindt zich in het menu **Help** (**?**) in Talent. Dit menu biedt toegang tot de volgende bronnen:

- Feedback
- Help
- Aan de slag
- Ondersteuning
- Ideeën
- Informatie

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Verbeteringen in de gebruikersinterface voor detectie van dubbele werknemers

Door deze wijziging worden dubbele records nu gedetecteerd tijdens het instellen van naamvelden en geeft een statusindicator het aantal gedetecteerde duplicaten aan. Via een koppeling wordt een pagina geopend waarop u kunt beoordelen of u een van de dubbele exemplaren moet gebruiken. Om te voorkomen dat de gegevensinvoer wordt onderbroken, wordt de pagina met dubbele records niet automatisch geopend. U moet de koppeling selecteren om de pagina te openen.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Ondersteuning van Common Data Service-entiteiten voor aangepaste velden

In de release van deze week ondersteunen de volgende entiteiten nu aangepaste velden: Aanstelling, Vergoedingstype en Betalingscyclus.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Er treedt een fout op wanneer een controlelijst voor offboarding wordt toegewezen (299877)

Deze wijziging corrigeert een foutbericht dat wordt weergegeven wanneer u een controlelijst voor offboarding toewijst aan een werknemer buiten het ontslagproces.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Met de afgesloten koppeling voor werknemers wordt de verkeerde werknemer geopend (309939)

Via deze wijziging wordt een probleem gecorrigeerd dat optreedt wanneer u een werknemer opnieuw aanstelt vanuit een andere rechtspersoon en probeert naar de werknemer te gaan vanuit de lijst met afgesloten werknemers.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>In de self-service compensatiekaart voor werknemers worden geen samenvattingswaarden weergegeven wanneer geavanceerde beveiliging is ingeschakeld (315231)

Via deze wijziging wordt een probleem gecorrigeerd dat optreedt wanneer u geavanceerde compensatiebeveiliging gebruikt. Wanneer geavanceerde beveiliging is ingeschakeld, wordt in de self-service voor werknemers nu een overzicht van de compensatiebedragen weergegeven voor zowel werknemers als managers. Vóór deze wijziging werden overzichtswaarden weergegeven als 0 (nul).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Als een positie zonder titel wordt gemaakt in Common Data Service, wordt geen positie gemaakt in Talent (314562)

Met de wijzigingen van deze week wordt een probleem gecorrigeerd dat optreedt wanneer u posities maakt in Common Data Service maar geen titel opgeeft.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Foutbericht in journaalposten voor prestaties in self-service voor werknemers (314134)

Met deze wijziging wordt een probleem gecorrigeerd dat optreedt wanneer u prestatiedoelstellingen koppelt aan journaalposten voor prestaties in self-service voor werknemers.

## <a name="in-preview"></a>Preview

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Toestaan dat redencodes voor verloftypen worden opgegeven

Organisaties hebben mogelijk extra informatie over verlofaanvragen nodig. U kunt nu redencodes voor verloftypen opgeven en toestaan dat werknemers een redencode in hun verlofaanvragen selecteren.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Redencodes voor specifieke verloftypen vereisen voor verlofaanvragen

Organisaties vereisen wellicht redencodes voor specifieke verloftypen wanneer werknemers verlofaanvragen indienen. Deze vereiste kan bestaan vanwege bedrijfsbeleid of wettelijke vereisten. U kunt nu opgeven welke verloftypen een redencode vereisen en u kunt vereisen dat werknemers een redencode opgeven voor het verloftype in hun verlofaanvragen.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Een lijst met verlof- en afwezigheidstransacties verschaffen voor HR

De mogelijkheid om verlof van werknemers bij te houden en inzicht te krijgen in de berekening van verlof helpt HR niet alleen bij het beantwoorden van werknemersvragen, maar helpt tevens nauwkeurige verloftoekenningen voor werknemers te waarborgen. HR heeft nu een nieuwe weergave om de transacties te bekijken (toekenningen, toerekeningen, correcties en aanvragen) zodat HR-medewerkers de redenen achter saldi kunnen bekijken.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="email-support-for-alerts"></a>E-ondersteuning voor waarschuwingen

In platformupdate 26 kunnen gebruikers waarschuwingsregels maken waarmee automatisch e-mailmeldingen worden verzonden naar contactpersonen wanneer meldingen door een gebeurtenis worden geactiveerd.
