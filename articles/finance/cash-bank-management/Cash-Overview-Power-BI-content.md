---
title: Power BI-inhoud - overzicht van contant geld
description: In dit onderwerp wordt Power BI-inhoud - overzicht van contant geld besproken. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten die zijn opgenomen in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: saraschi2
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0f10022ae4906972d08e08e3e5476630213468d6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985456"
---
# <a name="cash-overview-power-bi-content"></a>Power BI-inhoud - overzicht van contant geld

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt Microsoft Power BI-inhoud - **Overzicht van contant geld** besproken. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten die zijn opgenomen in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

Power BI-inhoud - **Overzicht van contant geld** is gemaakt voor personen die verantwoordelijk zijn voor contante betaling in hun organisatie. De Power BI-inhoud - **Overzicht van contant geld** biedt inzicht in uw cashflow. Het biedt ook prognoses die u kunnen helpen betere beslissingen te nemen en daarmee de status van uw kasstroom te verbeteren. U kunt contanten per rechtspersoon, valuta en bankrekening analyseren voor een beter begrip van overschotten en tekorten.

## <a name="setup-needed-to-view-power-bi-content"></a>Instellingen die nodig zijn om Power BI-inhoud weer te geven

De volgende instellingen moeten worden geconfigureerd om gegevens te kunnen weergeven in de visuele Power BI-elementen van **Overzicht van contant geld** en **Bankbeheer**.

1. Ga naar **Systeembeheer > Instellen > Systeemparameters** om **Systeemvaluta** en **Systeemwisselkoers** in te stellen.
2. Ga naar **Grootboek > Kalenders > Fiscale kalenders** om de boekjaarkalenderdatums te valideren die aan de actieve tijdsperiode zijn toegewezen.
3. Ga naar **Grootboek > Instellen > Grootboek** en stel **Valuta voor boekhouding** en **Wisselkoerstype** in.
4. Definieer wisselkoersen tussen transactievaluta's en valuta voor boekhouding, valuta voor boekhouding en systeemvaluta, en valuta voor boekhouding en bankvaluta's. Ga hiervoor naar **Grootboek > Valuta's > Valutawisselkoersen**.
5. Configureer Cashflowprognose en voer dit uit. Zie [Cashflowprognose](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting) voor meer informatie over het instellen van Cashflowprognose. 
6. Ga naar **Systeembeheer > Instellen > Entiteitopslag** > om de samengevoegde meting **LedgerCovLiquidityMeasurement** te vernieuwen.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud

Rapporten uit de Power BI-inhoud **Overzicht van contant geld** worden weergegeven in de werkgebieden **Overzicht van contant geld** en **Bankbeheer**.

Als u de cashflowprognoserapporten wilt weergeven met gegevens, moet u eerst het prognoseberekeningsproces uitvoeren met de functie **Cashflowprognoses berekenen** in Contanten en bankbeheer. Dit moet worden uitgevoerd voor elk bedrijf dat wordt opgenomen in de prognose.  Vernieuw de samengevoegde meting LedgerCovLiquidityMeasurement op de pagina **Entiteitopslag**.  

Voor demonstratiedoeleinden kunt u demogegevens voor cashflowprognoses toevoegen met de pagina **Gegevens genereren** vanuit de module Demogegevens.  Met dit script worden gegevens ingevoegd in de cashflowprognosetabellen om snel gegevens in te vullen die nodig zijn voor rapporten.  Deze module is alleen beschikbaar als u het model van de Demogegevenssuite hebt geïmplementeerd in de omgeving. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud

De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud - **Overzicht van contant geld**.

| Rapport                                | Inhoud |
|---------------------------------------|----------|
| Overzicht van contant geld - alle bedrijven         | <ul><li>Kasontvangsten en kasuitgaven in systeemvaluta</li><li>Voorspelde valutasaldi</li><li>Totaal banksaldo in systeemvaluta</li><li>Saldo per rechtspersoon</li><li>Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening</li></ul> |
| Overzicht van contant geld - huidig bedrijf       | <ul><li>Kasontvangsten en kasuitgaven in valuta voor boekhouding</li><li>Voorspelde valutasaldi</li><li>Totaal banksaldo in valuta voor boekhouding</li><li>Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening</li></ul> |
| Cashflowprognose – alle bedrijven    | <ul><li>Kasontvangsten en kasuitgaven in systeemvaluta</li><li>Dagelijks prognoseoverzicht</li><li>Prognosedetails</li></ul> |
| Cashflowprognose – bedrijfsvaluta | <ul><li>Kasontvangsten en kasuitgaven in valuta voor boekhouding</li><li>Dagelijks prognoseoverzicht</li><li>Prognosedetails</li></ul> |
| Valutaprognose                     | <ul><li>Voorspelde valutasaldi</li><li>Dagelijks valutaoverzicht</li><li>Prognosedetails</li></ul> |
| Banksaldi                         | <ul><li>Totaal banksaldo in systeemvaluta</li><li>Saldo per rechtspersoon</li><li>Werkelijk versus voorspeld saldo van vandaag in valuta van de bankrekening</li><li>Saldo per bankrekening</li><li>Saldo per valuta</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

In de volgende tabel vindt u de entiteiten waarop de Power BI-inhoud - **Overzicht van contant geld** is gebaseerd.

| Entiteit                                                                          | Inhoud |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Bedrijven waarop rapporten moeten worden gefilterd |
| LedgerCovLiquidityMeasurement\_Date                                             | Datum waarop rapporten moeten worden gefilterd |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Werkelijk banksaldo versus laatst voorspelde banksaldo |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Voorspelde transactiedetails |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Samengevatte kasinkomsten, kasuitgaven en saldo met behulp van de valuta voor boekhouding van elk bedrijf |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Samengevatte kasinkomsten, kasuitgaven en saldo met behulp van de systeemvaluta voor alle bedrijven |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Samengevat nettotransactiebedrag en saldo van valuta´s op basis van de transactievaluta |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]