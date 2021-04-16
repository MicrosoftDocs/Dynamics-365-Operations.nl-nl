---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (23 juli 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 23 juli 2020.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10369bd5aa67641fe840312bc3d8ebc0e91865e0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791288"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (23 juli 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources. Wijzigingen die van toepassing zijn op buildnummer 8.1.3416. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Financiële dimensies verwijderen op een positie werkt niet zoals verwacht (445476)

Als u dimensies van een positie verwijdert, worden die posities nu verwijderd uit Dataverse.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Posities die niet in de hiërarchie staan, geven inactieve posities weer (397257)

Niet-actieve posities (met een verstreken duur), worden niet langer in de positiehiërarchie weergegeven als **Posities die niet in de hiërarchie staan**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Validatie die plaatsvindt tussen LeaveEnrollmentEntity en HcmWorkerEntity in DMF-import (Data Management Framework) veroorzaakt langzaam laden van gegevens (442324)

Wijzigingen in deze release verbeteren de prestaties van **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Kan niet personaliseren in organisatiebeheer (447490)

Met deze wijziging kunt u de koppelingen in **organisatiebeheer** nu aanpassen.

## <a name="in-preview"></a>Preview

## <a name="mandatory-fields"></a>Verplichte velden 

U kunt nu velden verplicht maken met behulp van de aanpassingsmogelijkheden van Human Resources. Voor deze functie zijn **Opgeslagen weergaven** vereist.

## <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Zie [Human resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) voor meer informatie. 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer
 
Entiteiten voor vergoedingenbeheer worden vrijgegeven. DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen. Er is een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens. De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.

## <a name="buy-and-sell-leave"></a>Verlof inkopen en verkopen 

Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen. Dit proces wordt vaak handmatig beheerd. Deze functie automatiseert het beheer van beleidsregels en aanvragen voor de HR-afdeling. Het beheerproces voor verlof wordt gestroomlijnd en fouten worden geëlimineerd. Ga voor meer informatie naar:

- [Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Toerekening van verlof voor één bedrijf of één plan

Klanten kunnen toerekeningen verwerken voor één bedrijf of voor één verlof- en verzuimplan. Dit schept duidelijkheid voor het toerekenproces voor klanten met verschillende regels voor verlof- of verzuimtoerekening. Zie [Verlof per bedrijf of per verlofplan toerekenen](hr-leave-and-absence-accrue.md) voor meer informatie.

## <a name="add-attachments-to-time-off-requests"></a>Bijlagen toevoegen aan verlofaanvraagen

De mogelijkheid om bijlagen toe te voegen aan goedgekeurde verlofaanvragen is van cruciaal belang in de huidige COVID-19-omgeving. Werknemers kunnen deze bijlagen nu toevoegen. Ze hebben ook meer inzicht in de manier waarop updates worden uitgevoerd in verlofaanvragen. Zie [Een bijlage toevoegen aan een bestaande aanvraag](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) voor meer informatie.

## <a name="add-reason-code-to-accrual-suspensions"></a>Redencode toevoegen voor opschorten van toerekeningen 

Er zijn redencodes toegevoegd voor het opschorten van de toerekening.

## <a name="carry-forward-rules"></a>Regels voor transporteren 

U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt. Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen. Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Toerekening voor verlof voor opgegeven verloftypen opschorten

In deze versie kunt u een regel maken voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof. Onbetaald verlof kan een type zijn, maar dat hoeft niet. U kunt elk verlof uitstellen op basis van een ander verloftype.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-entiteit beschikbaar voor opschorten van toerekeningen 

Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.

## <a name="coming-soon"></a>Binnenkort beschikbaar

## <a name="checklist-entities-included-in-dataverse"></a>Check List-entiteiten opgenomen in Dataverse

Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.

## <a name="platform-changes"></a>Platformwijzigingen

Platformupdate 10.0.12 (36)

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]