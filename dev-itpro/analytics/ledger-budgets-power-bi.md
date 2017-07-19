---
title: Power BI-inhoud Werkelijk vs. budget
description: In dit onderwerp wordt de Power BI-inhoud Werkelijk vs. budget besproken. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten die zijn opgenomen in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5d52cce3cccb16f0645d9de1832ebeffbfaf3a09
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Power BI-inhoud Werkelijk vs. budget

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt de Microsoft Power BI-inhoud **Werkelijk vs. budget** besproken. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld. 

# <a name="overview"></a>Overzicht

De Power BI-inhoud **Werkelijk vs. budget** is gemaakt voor personen die verantwoordelijk zijn voor het controleren van werkelijke versus budget-prestaties in hun organisatie. De Power BI-inhoud **Werkelijk vs. budget** biedt inzicht in uw budgetafwijkingen. U kunt het budget voor het huidige jaar analyseren op rekeningcategorie, budgetcode, hoofdrekening, omschrijvingen van hoofdrekeningen of boekperiode, om beter inzicht te verkrijgen in de oorzaken van eventuele afwijkingen. 

# <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
Als u werkt met de update voor juli 2017 van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, vindt u de rapporten uit de Power BI-inhoud **Werkelijk vs. budget** in de werkgebieden **Grootboekbudgetten en prognoses** en **CFO**.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud
De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud **Werkelijk vs. budget**.

| Rapport                      | Metrische gegevens |
|-----------------------------|---------|
| Onkosten - werkelijk versus gebudgetteerd | <ul><li>Totale kosten dit jaar</li><li>Gebudgetteerde totale kosten dit jaar</li></ul> |
| Opbrengst - werkelijk versus gebudgetteerd  | <ul><li>Totale omzet dit jaar</li><li>Gebudgetteerde totale omzet dit jaar</li><ul> |
| Uitgaven                     | <ul><li>Totale kosten dit jaar</li><li>Doel voor onkosten op basis van budget </li><ul> |
| Opbrengst                     | <ul><li>Totale omzet dit jaar</li><li>Doel voor omzet op basis van budget </li><ul> |
| Netto-inkomsten                  | <ul><li>Netto-inkomsten dit jaar</li><li>Doel voor netto-inkomsten op basis van budget </li><ul> |

## <a name="extending-the-power-bi-content"></a>De Power BI-inhoud uitbreiden
Met behulp van de inhoudpakketten die beschikbaar zijn in Microsoft Dynamics Lifecycle Services (LCS) kunt u grondige analyses verschaffen aan personen die zich niet bij Microsoft Dynamics 365 aanmelden. U kunt deze inhoudpakketten wijzigen zodat ze andere rapporten of visuele elementen bevatten, en de inhoudpakketten vervolgens publiceren naar uw Power BI.com-tenant voor analyse. 

U vindt de Power BI-inhoud **Werkelijk vs. budget** in de bibliotheek voor gedeelde materialen in LCS. Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

# <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

| Entiteit                    | Inhoud |
|---------------------------|----------|
| Grootboekactiviteiten | Transactiebedragen voor het grootboek |
| Budgetactiviteiten         | Transactiebedragen voor het budgetregister |
| Hoofdrekeningen             | Hoofdrekeningen om rapporten op te filteren |
| Fiscale kalenders          | Fiscale kalenders om rapporten op te filteren |
| Grootboeken                   | Grootboeken die kunnen worden gebruikt om het rapport te filteren naar het huidige grootboek |
| Budgetcodes              | Budgetcodes om rapporten op te filteren |
| Rechtspersonen            | Rechtspersonen die kunnen worden gebruikt om het rapport te filteren naar de huidige rechtspersoon |

