---
title: Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (25 juni 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 23 juni 2020.
author: andreabichsel
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7fe8b685a2b492fe5ad23b410f6a99d81991e98a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904096"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Nieuwe of gewijzigde functies in Dynamics 365 Human Resources (23 juni 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3347. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Wanneer een inschrijving voor een vertrokken werk nemer is verlopen, worden het verloftype, saldo en bedrag allemaal gewist in het formulier Verlofinschrijving (444867)

De waarden in de velden **Verloftype**, **Saldo** en **Bedrag** worden nu vastgehouden in plaats van gewist wanneer u deze optie selecteert.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Onjuist voorspeld saldo wanneer een een nieuwe functie (verloftoerekening voor een enkel bedrijf of een enkel plan) wordt ingeschakeld (456553)

Het juiste voorspelde saldo wordt nu weergegeven wanneer de verloftoerekening voor een enkel bedrijf of een enkel plan is ingeschakeld.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Entiteiten met relaties die leiden tot dubbele navigatie-eigenschappen (456486)

Deze versie corrigeert een probleem met de navigatie-eigenschappen (relatie) van meerdere entiteiten. Dubbele relaties worden gedetecteerd. Deze scenario's zijn allemaal gecorrigeerd.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Opmerkingen van meerdere bedrijven voor de prestatiebeoordeling (455536)

Met deze oplossingen zijn nu opmerkingen van meerdere bedrijven zichtbaar bij prestatiebeoordelingen. Deze wijziging corrigeert de weergave van opmerkingen van de beoordelaars die in verschillende bedrijven zijn ingevoerd voor dezelfde prestatiebeoordeling.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Inconsistentie in weergave van gegevens uit compensatiebeheer (432562)

Nu wordt een consistente weergave van compensatiegegevens bijgehouden in de selfservice voor managers. Afhankelijk van hoe u navigeert naar de **compensatiedetails** van een werknemer, worden de compensatiegegevens nu consistent weergegeven voor managers.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>De ingangsdatum van de vaste compensatieregeling is standaard ingesteld op de datum van vandaag (411994)

De begindatum voor compensatie wordt nu gebaseerd op de begindatum van de positie die aan de werk nemer wordt toegewezen.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Definitie halve dag inschakelen op het formulier Verlof en verzuim is uitgeschakeld wanneer het formulier wordt geopend (452607)

Met deze wijziging wordt de **Definitie halve dag inschakelen** ingeschakeld totdat nieuwe verloftransacties bestaan. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Het is niet mogelijk te publiceren naar HcmDiscussionEntity via Excel; Fout in veld TotalRatingScore (453899)

U kunt het veld **TotalRatingScore** nu bijwerken met behulp van **HCMDiscussionEntity** in de Excel-werkmapontwerper.

## <a name="in-preview"></a>Preview

## <a name="database-logging"></a>Databaseaanmelding

Met databaselogboeken kunt u bepalen welke tabellen en velden moeten worden bewaakt. U kunt hiermee ook bepalen welke gebeurtenissen het bijhouden van wijzigingen moeten activeren. U gebruikt de functies van databaselogboeken om deze wijzigingen in de loop van de tijd weer te geven. Zie [Databaselogboeken configureren en beheren](hr-admin-database-logging.md) voor meer informatie.

## <a name="mandatory-fields"></a>Verplichte velden 

U kunt nu velden verplicht maken met behulp van de aanpassingsmogelijkheden van Human Resources. Voor deze functie zijn **Opgeslagen weergaven** vereist.

## <a name="human-resources-application-in-teams"></a>Human Resources-toepassing in Teams

Werknemers kunnen vrije tijd bekijken en aanvragen in Microsoft Teams. Ze kunnen met een bot werken om verlofaanvragen te maken. Zie [Human resources-app in Teams](./hr-admin-teams-leave-app.md) voor meer informatie. 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-entiteiten (Data Management Framework) voor vergoedingenbeheer
 
Entiteiten voor vergoedingenbeheer worden vrijgegeven. DMF-entiteiten staan het importeren en exporteren van gegevens toe om het configureren van vergoedingenbeheer te vereenvoudigen. Er is een sjabloon voor vergoedingenbeheer beschikbaar voor het verplaatsen van gegevens. De sjabloon exporteert en importeert de gegevens op volgorde om gegevensafhankelijkheden te behouden.

## <a name="buy-and-sell-leave"></a>Verlof inkopen en verkopen 

Sommige organisaties bieden een werknemers de mogelijkheid om hun verlof te kopen of verkopen. Dit proces wordt vaak handmatig beheerd. Deze functie automatiseert het beheer van beleidsregels en aanvragen voor de HR-afdeling. Het beheerproces voor verlof wordt gestroomlijnd en fouten worden geëlimineerd. Ga voor meer informatie naar:

- [Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Toerekening van verlof voor één bedrijf of één plan

Klanten kunnen toerekeningen verwerken voor één bedrijf of voor één verlof- en verzuimplan. Dit schept duidelijkheid in het toerekenproces voor klanten met verschillende regels voor verlof- of verzuimtoerekening. Zie [Verlof per bedrijf of per verlofplan toerekenen](hr-leave-and-absence-accrue.md) voor meer informatie.

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

## <a name="configure-the-name-of-employee-self-service"></a>De naam van de werknemerselfservice configureren

Een nieuwe optie is beschikbaar in **Parameters personeel** om de naam van de werkruimte voor werknemerselfservice te wijzigen in Selfservice.

## <a name="checklist-entities-included-in-dataverse"></a>Check List-entiteiten opgenomen in Dataverse

Controlelijstentiteiten voor de processen Onboarding, Offboarding, Overdracht en Bedrijfs zijn binnenkort beschikbaar in Dataverse.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]