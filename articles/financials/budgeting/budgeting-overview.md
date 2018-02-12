---
title: Startpagina Budgetteren
description: Dit onderwerp biedt een overzicht van de onderdelen van de budgetteringsfunctionaliteit, budgetteringstools en rapportagemogelijkheden in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
author: twheeloc
manager: AnnBe
ms.date: 08/09/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 953c79b134b82ce2a3e0adc05dc3bdf3ce583482
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="budgeting-home-page"></a>Startpagina Budgetteren

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt een overzicht van de onderdelen van de budgetteringsfunctionaliteit, budgetteringstools en rapportagemogelijkheden in Finance and Operations. 

<a name="components-of-budgeting-functionality"></a>Onderdelen van budgetfunctionaliteit
-------------------------------------

De resourceplanningscyclus voor een bedrijf bestaat meestal uit plannings-, budgetterings- en prognoseactiviteiten.

[![Onderdelen van budgetfunctionaliteit](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

De processen voor zowel strategische planning op de lange termijn als jaarlijkse budgetplanning worden ondersteund door middel van een budgetplandocument. De documenten van het budgetplan zijn nauw geïntegreerd met Microsoft Excel. Gebruikers kunnen onbeperkte monetaire en kwantitatieve scenario's configureren en een budgetteringsorganisatiehiërarchie definiëren om top-down en bottom-up budgetteringsmethoden te ondersteunen. Nadat een budget in Finance and Operations is opgesteld en goedgekeurd, converteert u het budgetplan naar een budgetregisterpost. Budgetregisterposten bieden tools om het budget te onderhouden en om bedragen door middel van budgetcodes te kunnen bijhouden. Met budgetregisterposten kunt u oorspronkelijke budgetten herzien, overboekingen uitvoeren en budgetbedragen van het vorige jaar transporteren. Op basis van het ingestelde budget kan een bedrijf budgetbeheer inschakelen. Het niveau van beheer is afhankelijk van de cultuur van de organisatie en het niveau van vervallen posten van de organisatie. Organisaties die een laag niveau van vervallen posten hebben, laten het budget mogelijk ongewijzigd en zijn mogelijk eerder reactief dan proactief als een budget niet aan de verwachtingen voldoet. Andere organisaties activeren mogelijk budgetbeheerbeleidsregels waarmee wordt voorkomen dat gebruikers iets kunnen aanschaffen als de budgetfondsen niet beschikbaar zijn.

Tot slot kunnen zeer volwassen organisaties een organisatiecultuur creëren waarin werknemers worden onderwezen in organisatorische doelen en deze doelen volgen via beleidsregels, zoals "Onlinevergadering overwegen in plaats van reizen". Finance and Operations bevat een raamwerk voor budgetbeheer waarmee het management van het bedrijf kan kiezen voor de harde lijn (geen boekingen die over het budget heen gaan) of de zachte lijn (gebruikers worden gewaarschuwd als ze de beschikbare budgetfondsen overschrijden en kunnen zelf bepalen hoe ze verdergaan). Tot slot kunt u voortschrijdende prognoses gebruiken. Een voortschrijdende prognose is een normale vergelijking tussen gebudgetteerde en werkelijke bedragen en wordt gebruikt om te bepalen hoe goed het bedrijf werkt met betrekking tot het budget. Een voortschrijdende prognose wordt ook gebruikt om trends te identificeren. In Finance and Operations worden voortschrijdende prognoses ondersteund via een budgetplandocument als oorspronkelijke planningsactiviteiten. Ze kunnen tegelijk met de planning voor de komende budgetcyclus worden uitgevoerd.

-   [Basisbudgettering: overzicht en configuratie](basic-budgeting-overview-configuration.md)
-   [Budgetbeheer: overzicht en configuratie](budget-control-overview-configuration.md)
-   [Budgetplanning: overzicht en configuratie](budget-planning-overview-configuration.md)
-   [Prognosepositie](position-forecasting.md)
-   [Verantwoordingsdocumenten voor budgetplanning](budget-planning-justification-docs.md)
-   [Microsoft Excel-sjablonen voor budgetplanning](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-finance-and-operations"></a>Budgetteringstools in Finance and Operations
[![Budgetteringstools](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Aanvullende plannings- en budgetteringsmogelijkheden zijn beschikbaar in Finance and Operations en geïntegreerd met grootboekbudgetten.

-   **Personeelsbudgetten**: personeelsbudgettering bevat gedetailleerde budgetkostenonderdeelplanning voor posities, compensatiegroepen enzovoort.
-   **Budgetten van vaste activa**: op basis van gegevens over vaste activa kunt u geplande afschrijving berekenen en andere aan vaste activa gerelateerde geplande transacties.
-   **Projectbudgetten**: in de projectenmodule kunt u gedetailleerde projectprognoses maken. De projectprognoses bevatten details over de geplande uren, onkosten, bijzondere kosten en artikelen.
-   **Vraagprognose**: u kunt toekomstige voorraadvraag ramen en vraagprognoses maken op basis van historische transactiegegevens.

Zie [Budgetplanningsintegratie met andere modules](budget-planning-integration-other-modules.md) voor informatie over het opnemen van planningsgegevens uit andere modules in budgetplannen.

## <a name="user-interface-and-reporting-capabilities"></a>Gebruikersinterface en rapportagemogelijkheden
In Finance and Operations kunnen gebruikers budgetplannen direct in de Finance and Operations-client maken (met behulp van een configureerbare pagina voor een budgetplandocument) of met Excel. Excel biedt verschillende aanvullende mogelijkheden. U kunt bijvoorbeeld externe gegevens gebruiken als een bron voor een budgetplan, aangepaste berekeningen uitvoeren en Microsoft-draaitabellen en -grafieken gebruiken. De meeste variabelen in het budgetplanningsproces kunnen worden geconfigureerd. 

U kunt bijvoorbeeld bepalen wie budgettering doet, wat wordt gebudgetteerd en hoe het proces eruit ziet. Hoewel u Excel kunt gebruiken voor budgetplanning, wordt Finance and Operations als één bron van waarheid aangehouden waarmee budgetbeheerproblemen kunnen worden voorkomen. Periodieke processen kunnen worden gebruikt om oorspronkelijke gegevens voor budgettering in het budgetplan in te voeren. Voor rapportage biedt Finance and Operations een set standaardquerypagina's waarmee u budgetteringsgegevens kunt bekijken en analyseren. Budgetplangegevens kunnen via Management Reporter worden geopend, en afzonderlijke budgetplanscenario's kunnen als kolommen in het Management Reporter-rapport worden weergegeven.







