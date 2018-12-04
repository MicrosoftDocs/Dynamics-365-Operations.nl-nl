---
title: Projectprognoses en -budgetten
description: Microsoft Dynamics 365 for Finance and Operations biedt projectprognoses en -budgetten om uw projecten te beheren en te regelen.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e31a013d6bf33b92b02bd9645a19380ba07f4a05
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="project-forecasts-and-budgets"></a>Projectprognoses en -budgetten

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations biedt twee om uw projecten te beheren en te regelen: projectprognoses en projectbudgetten. 

U kunt projectprognoses gebruiken als uw organisatie een operationeel perspectief heeft en zich richt op opbrengsten en kosten die van specifieke transacties zijn afgeleid. U kunt projectbudgettering gebruiken als uw organisatie zich meer richt op de financiële bedragen. 

Zowel projectprognoses als projectbudgetten gebruiken prognosemodellen om de geprojecteerde transactiebedragen te bewaren. 

Elke methode heeft zijn voordelen. Neem de volgende punten in overweging voordat u een methode selecteert voor uw organisatie.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Projectprognose**                  | **Projectbudgettering**                              |
| **Periodetoewijzing**     | U kunt niet expliciet transacties voor een boekperiode toewijzen. In plaats daarvan is de prognose, en het beheer van de prognose, gebaseerd op de duur van het project. Omdat prognoses op een bepaalde datum zijn gebaseerd, moet u de periode van de datum afleiden. | U kunt transacties toewijzen voor het volledige project of een boekperiode. Als u over een periode toewijst, kunt u ongebruikte bedragen naar de volgende boekperiode transporteren. |
| **Transacties weergeven**  | Transacties kunnen worden weergegeven in de prognoseformulieren, waar de prognoses voor het hele bedrijf en voor alle projecten worden weergegeven, ongeacht de hiërarchie. Om u op een bepaald project te richten, moet u de gegevens filteren.                                       | U kunt gebudgetteerde transacties voor één projecthiërarchie weergeven. Dit betekent dat u transactiegegevens voor een bovenliggend project of subprojecten kunt weergeven.                 |
| **Transactievariabelen** | Wanneer u prognosetransacties invoert, kunt u elk bestaand kenmerk voor een werkelijke transactie gebruiken. Hierdoor is er ruimte voor meer gegevens in de prognose. U kunt bijvoorbeeld gegevens invoeren voor hoeveelheden, werknemers, artikelen, of regeleigenschappen.         | Wanneer u budgetdetails invoert, kunt u alleen bedragen, categorieën en activiteiten gebruiken.                    |
| **Beveiliging**              | Prognoses worden gebaseerd op transacties die u invoert in de prognoseformulieren en hiervoor zijn geen mechanismen voor procesbeheer nodig. Elke werknemer met machtigingen voor een prognoseformulier kan gegevens zonder toestemming wijzigen.                                        | Bij budgettering wordt gebruikgemaakt van het werkstroomsysteem, wat wijzigingsbeheer en het bijhouden van de geschiedenis van revisies mogelijk maakt.         |
| **Invoertypen**           | Prognosetransactieboekingen zijn gebaseerd op het aantal eenheden en op kosten en verkoopeenheidsprijzen.  | Budgetdetails zijn gebaseerd op bedragen en worden opgesplitst in kosten en opbrengsten.                                          |
| **Prognosemodellen**       | Aangezien iedere prognose aan een model moet worden gekoppeld, kunt u meerdere prognosemodellen maken en submodellen instellen.           | Projectbudgettering beperkt de prognosemodellen die voor budgettering worden gebruikt. Minder prognosemodellen kan de consistentie in projecten vergroten.                           |
| **Kostenoverschrijdingen**         | U kunt alleen de invoer van transacties die een overschrijding veroorzaken, toestaan of niet toestaan.   | Met projectbudgettering hebben gebruikers meer controlemogelijkheden. U kunt waarschuwingen en overschrijdingen toestaan.                    |
| **Controle**               | Prognosecontrole wordt uitgevoerd met behulp van prognosereductie. Werkelijke bedragen worden afgetrokken van prognosetransactiesaldi zonder audittrail. Dit kan het lastiger maken om te traceren waar de werkelijke transacties zijn uitgevoerd.                   | In projectbudgetcontrole worden werkelijke bedragen afgetrokken van bedragen in het resterende budget. Dit zorgt voor een duidelijkere audittrail.                                   |

## <a name="project-forecasts"></a>Projectprognoses
Wanneer u projectprognoe gebruikt, kunt u voor elk transactietype prognosetransacties in prognoseformulieren invoeren. Elk beschikbaar attribuut voor een effectieve transactie kan voor een prognosetransactie worden gebruikt, bijvoorbeeld regelrentabiliteit, regelattributen, werknemers of omschrijvingen. U kunt ook voorspellen hoe lang het duurt voordat u een factuur naar een klant stuurt nadat u kosten hebt gemaakt. 

Projectprognosetransacties zijn gebaseerd op eenheden en bedragen. 

U moet elke projectprognose koppelen aan een prognosemodel. Wanneer u een prognosetransactie opgeeft, wordt automatisch een prognosemodel voorgesteld. Het prognosemodel fungeert als container voor de prognosetransacties. 

U kunt prognosemodellen als submodellen voor een model aanwijzen. Hiermee kunt u prognoses op regio, periode of afdeling maken. U kunt de prognosetransacties in een model kopiëren om een nieuw model te maken en u kunt ook de transacties naar het grootboek overbrengen. Aangezien er een één-op-één relatie bestaat tussen een prognose en een model, vormt elk prognosemodel een afzonderlijk budget voor een project. 

Prognosemodellen kunnen gebruikmaken van prognosereductie als controlemechanisme voor projecten. Bij prognosereductie reduceren effectieve transacties de prognosetransactiesaldi. Aangezien prognosereductie echter op het hoogste project in de hiërarchie wordt toegepast, biedt het een beperkt zicht op wijzigingen in de prognose. Als een werknemer bijvoorbeeld aan een subproject is gekoppeld, dan worden de effectieve transacties voor de werknemer in het bovenliggende project geboekt. Daarom kan het moeilijk zijn om wijzigingen bij te houden omdat u niet eenvoudig kunt bepalen welke transactie in welk subproject een reductie van het prognosebedrag veroorzaakt. Daarom is het een goed idee om een kopie van een prognosemodel voor prognosereductie te gebruiken. U kunt rapporten vervolgens gebruiken om te bekijken wat oorspronkelijk was geraamd. 

U kunt projectprognoses herzien, kopiëren, verwijderen of overdragen naar een grootboekbudget. Er is echter geen procescontrole. Elke werknemer met een machtiging voor een prognoseformulier kan zonder controle wijzigingen aanbrengen.

-   **Herzien**: u kunt een prognosetransactie aanpassen in hetzelfde formulier waarin de oorspronkelijke boekingen werden ingevoerd.
-   **Kopiëren of verwijderen**: wanneer u prognosetransacties kopieert, kopieert u de transactieregels van het ene prognosemodel naar een ander prognosemodel. Wanneer u een prognose verwijdert, verwijdert u de prognosetransacties uit een prognosemodel. Als u wilt beperken hoeveel prognosetransacties worden gekopieerd of verwijderd, selecteert u de specifieke transactietypes en -datums. Zo kunt u alleen bepaalde delen van een prognose kopiëren of verwijderen.
-   **Overboeken**: wanneer u een projectprognose overboekt naar een grootboekbudget, boekt u de prognosetransacties over van een prognosemodel naar een grootboekbudget. U kunt eventuele eerder overgeboekte transacties overschrijven in het grootboekbudget waarnaar u de projectprognose overboekt.

## <a name="project-budgets"></a>Projectbudgetten
Projectbudgettering is een eenvoudigere methode dan prognoses maken, hoewel het met prognosemodellen wordt geïntegreerd. Het gebruikt één invoerformulier voor oorspronkelijke budgetdetails en voor revisies en maakt prognoses op basis van alleen het bedrag, de categorie of activiteit mogelijk. 

Bij projectbudgettering moeten alle oorspronkelijke budgetten en revisies ter goedkeuring naar een projectworkflow worden verzonden. Werkstromen geven u meer controle over het proces en maken een record van de wijzigingshistorie. 

Projectbudgettering lijkt op algemene grootboekbudgettering, maar kan sneller en eenvoudiger worden ingesteld. Veel van de opties in de algemene grootboekbudgettering, zoals numerreeksen of valuta, moeten niet afzonderlijk voor projecten worden ingesteld.

Projectbudgetten worden automatisch geassocieerd met twee prognosemodellen, één voor het oorspronkelijke budget en één voor het resterende budget. Daarom kunnen rapporten die op prognosemodellen zijn gebaseerd budgetgegevens gebruiken. Wanneer een projectbudget wordt toegezegd, maakt het systeem prognosetransactie op basis van de gekoppelde modellen, die worden gebruikt voor rapportage- en controledoeleinden.

## <a name="forecast-models"></a>Prognosemodellen
Prognosemodellen hebben een hiërarchie van één laag. Dit betekent dat één projectprognose aan één prognosemodel moet worden gekoppeld.

Als u projectprognose gebruikt, kunt u modellen als submodellen aanwijzen. Zo kunt u prognoses per afdeling, tijd of regio maken. Een prognosemodel kan bijvoorbeeld voor een jaar worden gemaakt, en vervolgens kunnen er submodellen worden gemaakt voor de noordoostelijke, zuidoostelijke, noordwestelijke en zuidwestelijke regioprognoses die door regiohoofden worden ingediend. Door verschillende opties te selecteren in de beschikbare rapporten, kunt u informatie bekijken per totale prognose of per submodel.




