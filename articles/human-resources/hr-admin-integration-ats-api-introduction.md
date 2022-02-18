---
title: Integratie-API voor sollicitantenvolgsysteem - Inleiding
description: In dit onderwerp wordt de Dynamics 365 Human Resources integratie-API voor sollicitantenvolgsysteem (ATS) beschreven.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e16c781a6e51c57db8ae76dcfe0d28ec709428eb
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069927"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Integratie-API voor sollicitantenvolgsysteem - Inleiding


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de Dynamics 365 Human Resources integratie-API voor sollicitantenvolgsysteem (ATS) beschreven. De API is bedoeld om gestroomlijnde integraties tussen Dynamics 365 Human Resources en ATS-partners mogelijk te maken.

![ATS-integratiestroom.](media/hr-admin-integration-ats-api-introduction-flow.png)

De geïntegreerde ervaring begint in Human Resources wanneer een aanstellende manager een wervingsaanvraag maakt. Wanneer de aanvraag is geactiveerd, haalt de ATS de details op voor de aanvraag om een wervingsproject te maken. Daarna volgt het de wervingspijplijn om een kandidaat voor de functie(s) te selecteren en aan te stellen. Ten slotte rondt het ATS de integratie af door de record van de geselecteerde kandidaat naar Human Resources te sturen. De record van de kandidaat kan dan door meer onboarding validaties en werkstromen gaan om de werknemerrecord te maken.

Human Resources heeft de volgende onderdelen toegevoegd om de integratie in te schakelen:

1.  Functionaliteit om een wervingsaanvraag te maken.
2.  Een uitgebreid kandidaatprofiel en gerelateerde werkstromen.
3.  Een integratie-API die de nieuwe functionaliteit opent voor de integratie van toepassingen.

Zie [Kandidaten werven](hr-personnel-recruit.md) voor meer informatie over het instellen en gebruiken van de functionaliteit voor wervingsaanvragen en kandidaten.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Deze API is gebouwd op Microsoft Dataverse (voorheen Common Data Service). Alle RESTful-interactie met deze API gaat via de Microsoft Dataverse web-API, die OData gebruikt. Deze API is een subset van de Dataverse web-API. De Dataverse web-API definieert kenmerken als verificatie, SLA's, batch, gelijktijdigheidscontrole en foutverwerking.

Voor meer algemene informatie over de Microsoft Dataverse web-API, zie:

- [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [De Microsoft Dataverse web-API gebruiken](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse ontwikkelaarshandleiding](/powerapps/developer/data-platform)

De bovenstaande documentatie bevat gedetailleerde informatie en richtlijnen voor ontwikkelaars voor het gebruik van de Dataverse web-API, zoals [verificatie beheren](/powerapps/developer/data-platform/webapi/authenticate-web-api), [bewerkingen uitvoeren](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postman gebruiken met de API](/powerapps/developer/data-platform/webapi/use-postman-web-api) en [wijzigingen bijhouden of deltatokens gebruiken](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) met de API.

### <a name="option-sets"></a>Optiesets

Het gegevensmodel voor de API voor ATS-integratie die in dit document wordt beschreven, bevat optiesets die opgesomde waarden bevatten die aan entiteitseigenschappen zijn gekoppeld. Zie [Optiesets maken en bijwerken met de web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets) voor gedetailleerde informatie over het werken met optiesets in de Dataverse web-API. Voor elke Dataverse-omgeving worden optiesets gedefinieerd.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuele tabellen in Dataverse voor Human Resources

De eindpunten voor de API voor ATS-integratie maken gebruik van de mogelijkheden van het virtuele tabelplatform van Microsoft Dataverse. Standaard worden de virtuele tabellen en de bijbehorende API-eindpunten niet geïmplementeerd voor Human Resources-omgevingen, waardoor organisaties kunnen bepalen welke OData-eindpunten beschikbaar worden voor de omgeving. Als u de API wilt gebruiken, moeten de virtuele tabellen voor de Human Resources-entiteiten worden gegenereerd voor de omgeving. 

Zie [Dataverse virtuele tabellen configureren](./hr-admin-integration-common-data-service-virtual-entities.md) voor informatie over het genereren van de virtuele tabellen voor de API.

## <a name="data-model"></a>Gegevensmodel

Het gegevensmodel is gericht op twee hoofdentiteiten:

- **Wervingsaanvraag** geeft een aanvraag aan een ATS weer om te werven voor een of meer vacatures. Zie [Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md) voor een voorbeeldquery.
- **Kandidaten voor aanstelling** geeft details weer van een kandidaat die een aanbod voor een functie heeft geaccepteerd. **Persoon** geeft de persoon weer die de kandidaat is. Een persoon kan meerdere rollen in het bedrijf hebben, zoals kandidaat, werknemer, medewerker of contractant. Zie [Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md) voor een voorbeeldquery.

In het volgende diagram worden de relaties binnen de API weergegeven. Verschillende typen hebben refererende sleutels voor andere, bestaande entiteiten in HumanResources die hier niet worden geïllustreerd. Dit document bevat informatie over entiteiten die specifiek zijn voor wervingsintegratiescenario's. De Dataverse web-API voor Dynamics 365 Human Resources bevat echter een groot aantal andere entiteiten die ook relevant kunnen zijn voor uw integratie. U hebt bijvoorbeeld ook details nodig voor werknemers, functies, posities of andere entiteiten die hier niet zijn gedefinieerd. Naar veel van deze entiteiten worden verwezen in refererende sleutelrelaties of navigatie-eigenschappen.

![ATS-integratie API-gegevensmodel.](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Wervingsaanvragen en gerelateerde entiteiten en optiesets

Voorbeeldquery: 

- [Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Entiteiten:

- [Wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request.md)
- [Positie van wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Vaardigheid wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Opleiding wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Locatie van wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-location.md)

Optiesets:

- [Vrijstellingsstatus taak](hr-admin-integration-ats-api-job-exempt-status.md)
- [Positiestatus voor wervingsaanvragen](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Status wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Wettelijke taakcategorie](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Aan te stelledn kandidaat en gerelateerde entiteiten en optiesets

Voorbeeldquery:

- [Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Entiteiten:

- [Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Persoon](hr-admin-integration-ats-api-person.md)
- [Opleiding van persoon](hr-admin-integration-ats-api-person-education.md)
- [Werkervaring van persoon](hr-admin-integration-ats-api-person-professional-experience.md)
- [Adres van persoon](hr-admin-integration-ats-api-person-address.md)
- [Contactpersoon partij](hr-admin-integration-ats-api-party-contact.md)
- [Vaardigheid van persoon](hr-admin-integration-ats-api-person-skill.md)
- [Beoordelingsniveau](hr-admin-integration-ats-api-rating-level.md)
- [Certificaat van persoon](hr-admin-integration-ats-api-person-certificate.md)
- [Type certificaat](hr-admin-integration-ats-api-certificate-type.md)
- [Persoonscreening](hr-admin-integration-ats-api-person-screening.md)
- [Screeningtypen](hr-admin-integration-ats-api-screening-types.md)
- [Persoonlijk identificatienummer](hr-admin-integration-ats-api-person-identification-number.md)

Optiesets:

- [Integratieresultaat van sollicitant](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Leeg Ja Nee](hr-admin-integration-ats-api-blank-yes-no.md)
- [Status van voltooiing](hr-admin-integration-ats-api-completion-status.md)
- [Type contact](hr-admin-integration-ats-api-contact-type.md)
- [Creditbasis van opleiding](hr-admin-integration-ats-api-education-credit-basis.md)
- [Geslacht](hr-admin-integration-ats-api-gender.md)
- [Burgerlijke staat](hr-admin-integration-ats-api-marital-status.md)
- [Maanden van het jaar](hr-admin-integration-ats-api-months-of-year.md)
- [Nee Ja](hr-admin-integration-ats-api-no-yes.md)
- [Periode-eenheid](hr-admin-integration-ats-api-period-unit.md)
- [Screeningfrequentie](hr-admin-integration-ats-api-screening-frequency.md)
- [Screeningfrequentie genereren op basis van](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Type vaardigheidsniveau](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Zie ook

[Kandidaten werven](hr-personnel-recruit.md)<br>
[Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[De Microsoft Dataverse web-API gebruiken](/powerapps/developer/data-platform/webapi/overview)<br>
[Optiesets maken en bijwerken met de web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
