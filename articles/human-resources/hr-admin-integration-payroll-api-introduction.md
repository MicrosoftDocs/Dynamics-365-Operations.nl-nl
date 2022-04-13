---
title: Inleiding bij API voor integratie van salarisadministratie
description: In dit onderwerp wordt de Salarisintegratie-API van Dynamics 365 Human Resources beschreven.
author: twheeloc
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3743561e3ea3c798c37d71d851eb6b197c8d1c41
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533821"
---
# <a name="payroll-integration-api-introduction"></a>Inleiding bij API voor integratie van salarisadministratie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit document wordt de Salarisintegratie-API van Dynamics 365 Human Resources beschreven. De API maakt complete en gestroomlijnde integraties tussen Human Resources en de partneradministratie mogelijk. De geïntegreerde ervaring begint in Human Resources met werknemersprofiel, salaris, inhoudingen en bijdragegegevens. Wanneer u een werknemer in dienst neemt en het vereiste profiel en salarisgegevens in Human Resources invoert, haalt de salarisadministratie de informatie op die wordt gebruikt bij de verwerking van salarissen. Updates van de werknemer- of salarisgegevens worden ook uitgevoerd voor latere salarisruns.

[![Integratiestroom van salarisadministratie.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Human Resources bevat de volgende onderdelen om de integratie in te schakelen:

- [Functionaliteit om een werknemer te markeren als gereed voor betaling.](hr-compensation-payroll.md)
- Een integratie-API die de nieuwe functionaliteit opent voor de integratie van toepassingen.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Deze API is gebouwd op Microsoft Dataverse (voorheen Common Data Service). Alle RESTful-interactie met deze API gaat via de Microsoft Dataverse web-API, die OData gebruikt. Deze API is een subset van de Dataverse web-API. De Dataverse web-API definieert kenmerken als verificatie, SLA's, batch, gelijktijdigheidscontrole en foutverwerking.

Voor meer algemene informatie over de Microsoft Dataverse web-API, zie:

- [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [De Microsoft Dataverse web-API gebruiken](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse ontwikkelaarshandleiding](/powerapps/developer/data-platform)

Deze documentatie bevat details en richtlijnen voor ontwikkelaars van de Dataverse-web-API, waaronder de volgende onderwerpen:

- [Verifiëren bij Microsoft Dataverse met de web-API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Bewerkingen uitvoeren met de web-API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Postman gebruiken met de web-API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Wijzigingen bijhouden voor het synchroniseren van gegevens met externe systemen](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuele tabellen in Dataverse voor Human Resources

De eindpunten voor de API voor Salarisintegratie maken gebruik van de mogelijkheden van het virtuele tabelplatform van Microsoft Dataverse. Standaard worden de virtuele tabellen en de bijbehorende API-eindpunten niet geïmplementeerd voor Human Resources-omgevingen, waardoor organisaties kunnen bepalen welke OData-eindpunten beschikbaar worden voor de omgeving. Als u de API wilt gebruiken, moeten de virtuele tabellen voor de Human Resources-entiteiten worden gegenereerd voor de omgeving.

Zie [Dataverse virtuele tabellen configureren](./hr-admin-integration-common-data-service-virtual-entities.md) voor informatie over het genereren van de virtuele tabellen voor de API.

## <a name="data-model"></a>Gegevensmodel

In het volgende diagram worden de relaties binnen de API weergegeven. Verschillende typen hebben refererende sleutels voor andere, bestaande entiteiten in HumanResources die hier niet worden geïllustreerd. Dit document bevat informatie over entiteiten die specifiek zijn voor salarisintegratiescenario's. De Dataverse web-API voor Human Resources bevat echter een groot aantal andere entiteiten die ook relevant kunnen zijn voor uw integratie. Naar sommige van deze entiteiten worden verwezen in refererende sleutelrelaties of navigatie-eigenschappen.

[![Salarisintegratie API-gegevensmodel.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Salariswerker en gerelateerde entiteiten

Entiteiten:

- [Werknemer in salarisadministratie](hr-admin-integration-payroll-api-payroll-employee.md)
- [Adres medewerker salarisadministratie](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Vast compensatieplan in salarisadministratie](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Variabel compensatieplan in salarisadministratie](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Salarispositiefunctie](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Salarispositie](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Zie ook

[Entiteiten voor salarisadministratie genereren en beoordelen](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Human Resources-parameters configureren](hr-setup-parameters.md)<br>
[Gedeelde Human Resources-parameters onderhouden](hr-setup-shared-parameters.md)<br>
[Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[De Microsoft Dataverse web-API gebruiken](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
