---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (28 mei 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 28 mei 2020.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 00a5881ea88749c8553e4c810fb57070f217b01c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712007"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (28 mei 2020)

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources. Wijzigingen die van toepassing zijn op buildnummer 8.1.3287. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>LeaveRequest-entiteit werkt niet wanneer u meerdere typen per verlofplan inschakelt (447498)

Met deze wijziging is **LeaveEnrollmentV2Entity** nu beschikbaar om de fout te corrigeren die optreedt wanneer u meerdere verloftypen inschakelt.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Functie voor beperking van batchconflicten (preview) (446619)

Wanneer u deze functie inschakelt, kan het aantal blokkeringen in batchframeworktabellen tijdens het selecteren van taken en het voltooien van taken worden beperkt.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict tijdens het opslaan van de werknemer voorkomt dat een record in Personen wordt bewerkt (427915)

Deze wijziging corrigeert een fout bij het toevoegen van een nieuwe werknemer, het bijwerken van adresgegevens en het wijzigen van de taalvoorkeur. In dit unieke scenario wordt een fout weergegeven die aangeeft dat de record niet kan worden bijgewerkt. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Kan geen bijlage toevoegen aan een goedgekeurde verlofaanvraag die opnieuw wordt aangeboden (425407)

Door deze wijziging kunnen bijlagen worden goedgekeurd voor goedgekeurde verlofaanvragen.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Gebruiker kan compensatie voor een werknemer in een ander rechtspersoonformulier invoeren (409529)

Door deze wijziging worden compensatieopties uitgeschakeld om te voorkomen dat er per ongeluk compensatierecords worden ingevoerd voor de verkeerde rechtspersoon.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Fout bij het overbrengen van een werknemer en de datum voor Positietoewijzingen werknemer ligt vóór de positieduur (429402)

Foutberichten wanneer u een werknemer in dit scenario overdraagt, zijn bijgewerkt om beter te kunnen beschrijven welke wijzigingen nodig zijn om het probleem op te lossen.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Bijlagemogelijkheden bij inschrijving voor vergoedingen in Selfservice werknemer
 
U kunt nu bijlagen toevoegen tijdens het inschrijvingsproces voor vergoedingen voor elk plan waarvoor de werknemer is ingeschreven. U kunt vervolgens de bijlagen weergeven in het formulier **Vergoeding waarvoor medewerker zich heeft ingeschreven**.

## <a name="in-preview"></a>Preview

## <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Zie [Human resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) voor meer informatie. 

## <a name="leave-suspension"></a>Verlof opschorten

U kunt verlof en verzuim in Human Resources opschorten voor een werknemer. Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen. Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt. Zie [Verlof opschorten](hr-leave-and-absence-suspend-leave.md) voor meer informatie.

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Update voor gebruikerservaring om aan te geven dat toerekening wordt opgeschort (429550)

De gebruikerservaring geeft nu aan dat de toerekening voor een plan is opgeschort.

## <a name="coming-soon"></a>Binnenkort beschikbaar

## <a name="database-logging-in-preview-in-june"></a>Databaselogboeken (in preview in juni)

Met de functie voor databaselogboeken kunt u bepalen welke tabel en velden moeten worden gecontroleerd. U kunt hiermee ook bepalen welke gebeurtenissen het bijhouden van wijzigingen moeten activeren. Mogelijkheden voor query's zijn beschikbaar om deze wijzigingen in de loop van de tijd te bekijken.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Verlof kopen en verkopen (in preview vanaf 1 juni)

Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen. Dit proces wordt vaak handmatig beheerd. Deze functie biedt een meer geautomatiseerde manier om beleid en aanvragen voor de HR-afdeling te beheren en helpt fouten te elimineren tijdens het stroomlijnen van het proces voor verlofbeheer. Ga voor meer informatie naar:

- [Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer
 
Entiteiten voor vergoedingenbeheer worden vrijgegeven. DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen. Er is ook een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens. De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Redencode toevoegen voor opschorten van toerekeningen (1 juni)

Er zijn redencodes toegevoegd voor het opschorten van de toerekening.

## <a name="carry-forward-rules-june-1"></a>Regels voor transporteren (1 juni)

U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt. Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen. Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Toerekening voor verlof voor opgegeven verloftypen opschorten (1 juni)

In deze versie kan in HR een regel worden gemaakt voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof. Onbetaald verlof kan een type zijn, maar dat hoeft niet. U kunt elk verlof uitstellen op basis van een ander verloftype.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF-entiteit beschikbaar voor opschorten van toerekeningen (1 juni)

Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)