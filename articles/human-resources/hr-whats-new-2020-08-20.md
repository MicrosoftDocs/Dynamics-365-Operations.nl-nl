---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (20 augustus 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 20 augustus 2020.
author: andreabichsel
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a97997212a090f141c7280f7e48fd116a1f31481
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062156"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (20 augustus 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources. Wijzigingen die van toepassing zijn op buildnummer 8.1.3478. De getallen tussen haakjes in sommige koppen verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Gegevens over aanstaand en in behandeling genomen verlof en verzuim weergeven in kaarten in de werkruimte Personen

Opties voor in behandeling zijnde verlofaanvragen zijn nu beschikbaar op de verlof- en afwezigheidskaarten in de werkruimte **Personen**.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Persoonlijk veld is niet standaard Ja voor Werknemersrol in selfservice voor werknemers (477106)

Het veld **Privé** staat nu standaard ingesteld op **Ja** wanneer werknemers nieuwe adresrecords toevoegen via de pagina **Persoonlijke gegevens** in selfservice voor werknemers. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Het sneltabblad Aan te stellen kandidaten in Personeelsbeheer toont een onjuist aantal kandidaten (470110)

De pagina **Personeelsbeheer** toont nu het juiste aantal aan te stellen kandidaten. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Kan geen ziekte voor vertrokken werknemer invoeren als de toename is ingesteld op nul (446195)

Verloftransacties zijn nu toegestaan voor werknemers die in de toekomst zullen vertrekken en voor wie de toename is ingesteld op nul. Verloftransacties kunnen worden ingevoerd tot aan de laatste werkdag van de werknemer. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Als u aangepaste velden toevoegt aan het nieuwe formulier Medewerker, worden de velden in het actievenster voor Verlof beheren uitgeschakeld (473314)

Opties in het actievenster op het nieuwe formulier **Medewerker** in **Verlof beheren** worden niet meer uitgeschakeld als aangepaste velden zijn toegevoegd aan het nieuwe formulier **Medewerker**.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Wanneer het commentaarveld voor Verlof verplicht is gesteld, kan er alsnog een verlofaanvraag worden ingediend wanneer er geen opmerking is ingevoerd (473543)

Commentaarvelden kunnen nu verplicht worden en verlofaanvragen voldoen aan deze instelling. Verplichte velden is een preview-functie.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-entiteit beschikbaar voor opschorten van toerekeningen

Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.

## <a name="in-preview"></a>Preview

### <a name="mandatory-fields"></a>Verplichte velden

U kunt velden verplicht maken met behulp van de aanpassingsmogelijkheden van Human Resources. Voor deze functie zijn **Opgeslagen weergaven** vereist. Voor meer informatie over opgeslagen weergaven zie:

- [Opgeslagen weergaven - algemene beschikbaarheid](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in het Dynamics 365 2020 releasewave 2-plan
- [Formulieren maken waarin opgeslagen weergaven volledig worden gebruikt](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Ga voor meer informatie naar:

- [Voorziening voor verlof en verzuim van werknemers in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in het Dynamics 365 2020 releasewave 1-plan
- [Human Resources-app in Teams](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="human-resources-app-in-teams-preview-features"></a>Preview-functies op Human Resources-app in Teams
 
-  **Meldingen**: inzenders en goedkeurders van verlofaanvragen worden in de Human Resources-app in Teams geïnformeerd. Goedkeurders kunnen verlofaanvragen goedkeuren of weigeren, en inzenders ontvangen een melding als de aanvraag is goedgekeurd of geweigerd.
 
- **Verlofagenda van manager**: managers kunnen goedgekeurde en in behandeling zijnde verlofaanvragen van hun ondergeschikten in een kalenderweergave bekijken. Deze weergave geeft duidelijk weer wanneer teamleden afwezig zijn.

### <a name="checklist-entities-included-in-dataverse"></a>Check List-entiteiten opgenomen in Dataverse

Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.

## <a name="known-issues"></a>Bekende problemen

In het werkgebied voor **Functiebeheer** kunnen functies worden weergegeven die zijn uitgeschakeld als preview-functies wanneer ze algemeen beschikbaar zijn. Hieronder ziet u een lijst met algemeen beschikbare functies waarvoor een onjuiste status wordt weergegeven. 

- Vergoedingenbeheer
- Casebeheer
- Databaselogboeken (controle)
- Verloftoerekening voor één bedrijf of één plan
- Uitstel van toerekening van verlof en verzuim
- Redencode en opmerking voor saldocorrectie
- Verlof inkopen en verkopen
- Verlof- en verzuimkalender
- Transportregels voor verlof
- Controleren van verloftoerekeningen
- Verwijderen van verloftoerekeningen
- Afronding voor verloftoerekening
- Meerdere verloftypen configureren voor één verlofplan
- Verbeteringen voor vrije tijd bijwerken
- De FTE voor toerekeningen van een werknemer gebruiken
- Compensatieweergave voor meerdere bedrijven
- Prestatiebeoordelingen afdrukken
- Feestdagcorrecties voor verloftoerekening

### <a name="benefit-plan-employee-entity"></a>Entiteit Uitkeringsregeling voor werknemers 

We hebben onlangs twee problemen geconstateerd met betrekking tot de entiteit **BenefitsPlanEmployee**. Bij het importeren van medewerkersinschrijvingen worden de **Dekkingscode** en de **Plantypecode** onjuist ingesteld. Door dit probleem worden vergoedingsplannen van werknemers onjuist weergegeven in het formulier **Medewerkersvergoedingenplan** en in het formulier **Open inschrijving** in selfservice voor werknemers. Dit probleem kan ook van invloed zijn op de mogelijkheid van de werknemer om plannen te selecteren in selfservice voor werknemers. Momenteel is er geen oplossing. We behandelen dit als een fix met hoge prioriteit en zullen de fix in de volgende release verspreiden.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]