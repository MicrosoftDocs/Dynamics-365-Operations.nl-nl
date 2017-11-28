---
title: Power BI-inhoud Overzicht van contant geld
description: In dit onderwerp wordt de Power BI-inhoud Overzicht van contant geld besproken. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten die zijn opgenomen in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: saraschi2
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fdcd3083f475967ec2e5f94dad850a1bf98c864a
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI-inhoud Overzicht van contant geld

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud **Overzicht van contant geld** besproken. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten die zijn opgenomen in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Overzicht van contant geld** is gemaakt voor personen die verantwoordelijk zijn voor contante betaling in hun organisatie. De Power BI-inhoud **Overzicht van contant geld** biedt inzicht in uw cashflow. Het biedt ook prognoses die u kunnen helpen betere beslissingen te nemen en daarmee de status van uw kasstroom te verbeteren. U kunt contanten per rechtspersoon, valuta en bankrekening analyseren voor een beter begrip van overschotten en tekorten.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen

Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), worden rapporten uit de Power BI-inhoud **Overzicht van contant geld** weergegeven in de werkgebieden **Overzicht van contant geld** en **Bankbeheer**.

Als u de cashflowprognoserapporten wilt weergeven met gegevens, moet u eerst het prognoseberekeningsproces uitvoeren met de functie **Cashflowprognoses berekenen** in Contanten en bankbeheer.  Dit moet worden uitgevoerd voor elk bedrijf dat wordt opgenomen in de prognose.  Vernieuw de samengevoegde meting LedgerCovLiquidityMeasurement op de pagina **Entiteitopslag**.  

Voor demonstratiedoeleinden kunt u demogegevens voor cashflowprognoses toevoegen met de pagina **Gegevens genereren** vanuit de module Demogegevens.  Met dit script worden gegevens ingevoegd in de cashflowprognosetabellen om snel gegevens in te vullen die nodig zijn voor rapporten.  Deze module is alleen beschikbaar als u het model van de Demogegevenssuite hebt geïmplementeerd in de omgeving. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud
De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud **Overzicht van contant geld**.

| Rapport                                | Inhoud |
|---------------------------------------|----------|
| Overzicht van contant geld - alle bedrijven         | <ul><li>Kasontvangsten en kasuitgaven in systeemvaluta</li><li>Voorspelde valutasaldi</li><li>Totaal banksaldo in systeemvaluta</li><li>Saldo per rechtspersoon</li><li>Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening</li></ul> |
| Overzicht van contant geld - huidig bedrijf       | <ul><li>Kasontvangsten en kasuitgaven in valuta voor boekhouding</li><li>Voorspelde valutasaldi</li><li>Totaal banksaldo in valuta voor boekhouding</li><li>Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening</li></ul> |
| Cashflowprognose – alle bedrijven    | <ul><li>Kasontvangsten en kasuitgaven in systeemvaluta</li><li>Dagelijks prognoseoverzicht</li><li>Prognosedetails</li></ul> |
| Cashflowprognose – bedrijfsvaluta | <ul><li>Kasontvangsten en kasuitgaven in valuta voor boekhouding</li><li>Dagelijks prognoseoverzicht</li><li>Prognosedetails</li></ul> |
| Valutaprognose                     | <ul><li>Voorspelde valutasaldi</li><li>Dagelijks valutaoverzicht</li><li>Prognosedetails</li></ul> |
| Banksaldi                         | <ul><li>Totaal banksaldo in systeemvaluta</li><li>Saldo per rechtspersoon</li><li>Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening</li><li>Saldo per bankrekening</li><li>Saldo per valuta</li></ul> |

## <a name="extending-the-power-bi-content"></a>De Power BI-inhoud uitbreiden
U kunt grondige analyses verschaffen aan personen die zich aanmelden bij Dynamics 365. U doet dat met behulp van de inhoudpakketten die beschikbaar zijn in Lifecycle Services (LCS). Deze inhoudpakketten kunnen worden gewijzigd om andere rapporten of visuele elementen op te nemen om vervolgens te worden gepubliceerd naar uw Power BI.com-tenant voor analyse. 

U kunt de Power BI-inhoud **Overzicht van contant geld** vinden in de bibliotheek voor gedeelde activa in LCS. Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

In de volgende tabel vindt u de entiteiten waarop de Power BI-inhoud **Overzicht van contant geld** is gebaseerd.

| Entiteit                                                                          | Inhoud |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Bedrijven waarop rapporten moeten worden gefilterd |
| LedgerCovLiquidityMeasurement\_Date                                             | Datum waarop rapporten moeten worden gefilterd |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Werkelijk banksaldo versus laatst voorspelde banksaldo |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Voorspelde transactiedetails |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Samengevatte kasinkomsten, kasuitgaven en saldo met behulp van de valuta voor boekhouding van elk bedrijf |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Samengevatte kasinkomsten, kasuitgaven en saldo met behulp van de systeemvaluta voor alle bedrijven |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Samengevat nettotransactiebedrag en saldo van valuta´s op basis van de transactievaluta |

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. Deze berekende eenheden worden vervolgens gebruikt om de diagrammen en rapporten te berekenen die in de Power BI-inhoud **Overzicht van contant geld** worden gebruikt. Als u extra berekeningen in uw rapporten en het dashboard wilt opnemen, kunt u het Power BI-bestand downloaden vanuit LCS en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om de inhoud te maken. Wanneer u klaar bent met het aanbrengen van wijzigingen, kunt u organisatorische inhoud en dashboards maken met de informatie die u hebt toegevoegd.


