---
title: Startpagina Budgetteren
description: Dit onderwerp biedt een overzicht van de budgettering onderdelen, budgetteringstools en rapportagemogelijkheden in Microsoft Dynamics 365 voor bewerkingen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: f7b4efc06b8e64c05da026850b41cb5b68c33ec3
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-home-page"></a>Startpagina Budgetteren

Dit onderwerp biedt een overzicht van de budgettering onderdelen, budgetteringstools en rapportagemogelijkheden in Microsoft Dynamics 365 voor bewerkingen.

<a name="components-of-budgeting-functionality"></a>Onderdelen van budgetfunctionaliteit
-------------------------------------

De resourceplanningscyclus voor een bedrijf bestaat meestal uit plannings-, budgetterings- en prognoseactiviteiten.
[![budgettering onderdelen](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg) de processen voor zowel strategische planning op lange termijn en planning van de jaarlijkse begroting worden ondersteund via een budgetplandocument. De documenten van het budgetplan zijn nauw geïntegreerd met Microsoft Excel. Gebruikers kunnen onbeperkte monetaire en kwantitatieve scenario's configureren en een budgetteringsorganisatiehiërarchie definiëren om top-down en bottom-up budgetteringsmethoden te ondersteunen. Nadat een budget in Microsoft Dynamics 365 for Operations is opgesteld en goedgekeurd, converteert u het budgetplan naar een budgetregisterpost. Budgetregisterposten bieden tools om het budget te onderhouden en om bedragen door middel van budgetcodes te kunnen bijhouden. Met budgetregisterposten kunt u oorspronkelijke budgetten herzien, overboekingen uitvoeren en budgetbedragen van het vorige jaar transporteren. Op basis van het ingestelde budget kan een bedrijf budgetbeheer inschakelen. Het niveau van beheer is afhankelijk van de cultuur van de organisatie en het niveau van vervallen posten van de organisatie. Organisaties die een laag niveau van vervallen posten hebben, laten het budget mogelijk ongewijzigd en zijn mogelijk eerder reactief dan proactief als een budget niet aan de verwachtingen voldoet. Andere organisaties activeren mogelijk budgetbeheerbeleidsregels waarmee wordt voorkomen dat gebruikers iets kunnen aanschaffen als de budgetfondsen niet beschikbaar zijn. Ten slotte kunnen zeer volwassen organisaties vaststellen van een organisatie-cultuur waarin werknemers over de doelpersonen van de organisatie worden opgeleid en volg deze doelen via het beleid zoals ' Overweeg on line vergadering in plaats van een reis.' Dynamics 365 voor bewerkingen bevat een raamwerk voor budgetbeheer waarmee het bedrijf beheer selecteert u beide vaste besturingselementen (waardoor boekingen die het budget heengaat) of zachte (waar gebruikers worden gewaarschuwd dat ze de beschikbare budgetfondsen overschrijdt, maar zelf kunnen beslissen hoe verder te gaan). Ten slotte kunt u Huidig prognoses. Een doorgaande prognose is een normale vergelijking van budget dat u wilt de werkelijke waarden en kunt u definiëren hoe goed het bedrijf actief tegen het budget wordt gebruikt. Een voortschrijdende prognose wordt ook gebruikt om trends te identificeren. In Microsoft Dynamics 365 for Operations worden voortschrijdende prognoses ondersteund via een budgetplandocument als oorspronkelijke planningsactiviteiten. Ze kunnen tegelijk met de planning voor de komende budgetcyclus worden uitgevoerd.

-   [Basisbudgettering: overzicht en configuratie](basic-budgeting-overview-configuration.md)
-   [Budgetbeheer: overzicht en configuratie](budget-control-overview-configuration.md)
-   [Budgetplanning: overzicht en configuratie](budget-planning-overview-configuration.md)
-   [Positie voorspellen](position-forecasting.md)
-   [documenten uitvullen](budget-planning-justification-docs.md)
-   [Microsoft Excel-sjablonen voor budgetplanning](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Budgettering van functies in Dynamics 365 for Operations
[![budgettering hulpmiddelen](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Aanvullende plannings- en budgetteringsmogelijkheden zijn beschikbaar in Dynamics 365 for Operations en geïntegreerd met grootboekbudgetten.

-   **Personeelsbudgetten**: personeelsbudgettering bevat gedetailleerde budgetkostenonderdeelplanning voor posities, compensatiegroepen enzovoort.
-   **Budgetten van vaste activa**: op basis van gegevens over vaste activa kunt u geplande afschrijving berekenen en andere aan vaste activa gerelateerde geplande transacties.
-   **Projectbudgetten**: in de projectenmodule kunt u gedetailleerde projectprognoses maken. De projectprognoses bevatten details over de geplande uren, onkosten, bijzondere kosten en artikelen.
-   ** Vraag prognoses **: gebaseerd op transactiegegevens in historische, kunt u toekomstige voorraad vraag ramen en vraagprognoses maken.

Zie [Budgetplanningsintegratie met andere modules](budget-planning-integration-other-modules.md) voor informatie over het opnemen van planningsgegevens uit andere modules in budgetplannen.

## <a name="user-interface-and-reporting-capabilities"></a>Gebruikersinterface en rapportagemogelijkheden
In Microsoft Dynamics 365 for Operations kunnen gebruikers budgetplannen direct in de Microsoft Dynamics 365 for Operations-client maken (met behulp van een configureerbare pagina voor een budgetplandocument) of met Excel. Excel biedt verschillende aanvullende mogelijkheden. U kunt bijvoorbeeld externe gegevens gebruiken als een bron voor een budgetplan, aangepaste berekeningen uitvoeren en Microsoft-draaitabellen en -grafieken gebruiken. De meeste variabelen in het budgetplanningsproces kunnen worden geconfigureerd. U kunt bijvoorbeeld bepalen wie budgettering doet, wat wordt gebudgetteerd en hoe het proces eruit ziet. Hoewel u Excel kunt gebruiken voor budgetplanning, wordt Dynamics 365 for Operations als één bron van waarheid aangehouden waarmee budgetbeheerproblemen beter worden voorkomen. Periodieke processen kunnen worden gebruikt om oorspronkelijke gegevens voor budgettering in het budgetplan in te voeren. Voor rapportage biedt Dynamics 365 for Operations een set standaardquerypagina's waarmee u budgetteringsgegevens kunt bekijken en analyseren. Budgetplangegevens kunnen via Management Reporter worden geopend, en afzonderlijke budgetplanscenario's kunnen als kolommen in het Management Reporter-rapport worden weergegeven.





