---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (11 juni 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 6/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39f18dc92fb01f9a0437f4166c0f08f8d6b1b81b
ms.sourcegitcommit: 218e22014a964b8b52fc0152e355b07b0b84ae2c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456615"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (11 juni 2020)

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3316. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Gestroomlijnd werknemerformulier zorgt er soms voor dat de sluitknoppen (X) van het onderliggende formulier niet meer werken (442369)

Wanneer het nieuwe formulier **Medewerker** is ingeschakeld, werkt de knop Sluiten (**X**) soms niet op onderliggende formulieren. Dit probleem trad af en toe op. U kon het formulier sluiten na verlaten en weer terugkomen. U kon bijvoorbeeld een menuoptie aan de linkerkant selecteren en teruggaan naar het formulier **Medewerker** en het formulier sluiten. De release van deze week corrigeert dit probleem. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>De entiteit voor de persoonlijke contactpersoon van de medewerker exporteert geen persoonlijke contactpersonen met een bovenliggend relatietype

Met deze versie exporteert de **Entiteit persoonlijke contactpersoon medewerker** alle relatietypen.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>De HcmPositionWorkerAssignmentV2Entity moet standaard deel uitmaken van het salarisintegratiepakket van Ceridian (448506)

Met deze wijziging wordt **HcmPositionWorkerAssignmentV2Entity** opgenomen in het Ceridian-salarisintegratiepakket.

## <a name="in-preview"></a>Preview

## <a name="database-logging"></a>Databaseaanmelding

Met de functie voor databaselogboeken kunt u bepalen welke tabellen en velden moeten worden gecontroleerd. U kunt hiermee ook bepalen welke gebeurtenissen het bijhouden van wijzigingen moeten activeren. U gebruikt de functies van databaselogboeken om deze wijzigingen in de loop van de tijd weer te geven. Zie [Databaselogboeken configureren en beheren](hr-admin-database-logging.md) voor meer informatie.

## <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Zie [Human resources-app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) voor meer informatie. 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer
 
Entiteiten voor vergoedingenbeheer worden vrijgegeven. DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen. Er is een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens. De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.

## <a name="buy-and-sell-leave"></a>Verlof inkopen en verkopen 

Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen. Dit proces wordt vaak handmatig beheerd. Deze functie automatiseert het beheer van beleidsregels en aanvragen voor de HR-afdeling. Het beheerproces voor verlof wordt gestroomlijnd en fouten worden geëlimineerd. Ga voor meer informatie naar:

- [Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Toerekening van verlof voor één bedrijf of één plan

Klanten kunnen toerekeningen verwerken voor één bedrijf of voor één verlof- en verzuimplan. Dit schept duidelijkheid in het toerekenproces voor klanten met verschillende regels voor verlof- of verzuimtoerekening. Zie [Verlof per bedrijf of per verlofplan toerekenen](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan) voor meer informatie.

## <a name="add-attachments-to-time-off-requests"></a>Bijlagen toevoegen aan timeoutaanvraagen

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

## <a name="new-platform-capabilities"></a>Nieuwe platformfuncties 

U kunt velden verplicht maken door persoonlijke instellingen te gebruiken. Voor deze functie moeten **Opgeslagen weergaven** worden ingeschakeld.

## <a name="configure-the-name-of-employee-self-service"></a>De naam van de werknemerselfservice configureren

Een nieuwe optie is beschikbaar in HR-parameters om de naam van de werkruimte voor werknemerselfservice te wijzigen in selfservice. 
