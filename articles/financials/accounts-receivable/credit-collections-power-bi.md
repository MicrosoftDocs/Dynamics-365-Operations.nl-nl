---
title: Power BI-inhoud Crediterings- en aanmaningsbeheer
description: In dit onderwerp wordt beschreven wat er is opgenomen in de Power BI-inhoud Crediterings- en aanmaningsbeheer. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5f08df6cb8549e87e123b10c5a771ae1c60ff39c
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Power BI-inhoud Crediterings- en aanmaningsbeheer

In dit onderwerp wordt beschreven wat er is opgenomen in de Microsoft Power BI-inhoud **Crediterings- en aanmaningsbeheer**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Crediterings- en aanmaningsbeheer** is gemaakt voor crediterings- en incassomanagers en incassomedewerkers. Deze Power BI-inhoud bevat belangrijke metrische gegevens over crediteringen en aanmaningen, zoals aantal dagen voor uitstaande verkopen, achterstallig saldo, kredietrisico en klanten die hun kredietlimiet hebben overschreden. Deze Power BI-inhoud gebruikt transactiegegevens en biedt samengevoegde weergaven van creditering en aanmaningen voor alle bedrijven. Ook wordt een onderverdeling per bedrijf, klantengroep en klant verschaft.

Deze Power BI-inhoud bestaat uit 10 rapportpagina's:

- Twee overzichtspagina's (één pagina voor een overzicht van crediteringen en één pagina voor een overzicht van aanmaningen)
- Acht detailpagina's die metrische gegevens bevatten over crediteringen en aanmaningen die zijn gesegmenteerd en verdeeld in verschillende dimensies

Alle bedragen worden weergegeven in de systeemvaluta. U kunt de systeemvaluta instellen op de pagina **Systeemparameters**.

Standaard worden de gegevens over crediteringen en aanmaningen voor het huidige bedrijf weergegeven. Als u de gegevens voor alle bedrijven wilt bekijken, wijst u de taak **CustCollectionsBICrossCompany** aan de rol toe.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), vindt u de Power BI-inhoud **Crediterings- en aanmaningsbeheer** in het werkgebied **Klantcrediteringen- en aanmaningsbeheer**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud

De Power BI-inhoud **CustCollectionsBICrossCompany** bevat een rapport dat uit een verzameling van metrische gegevens bestaat. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de Power BI-inhoud **CustCollectionsBICrossCompany**.

| Rapportpagina                 | Visualisatie |
|-----------------------------|---------------|
| Overzicht van aanmaningen        | <ul><li>Klanten over tijd</li><li>Klanten boven kredietlimiet</li><li>30 dagen DSO (dagen uitstaande verkoop)</li><li>Openstaande cases</li><li>Gemiddeld aantal dagen tot sluiten van aanvraag</li><li>Openstaande activiteiten</li><li>Gemiddeld aantal dagen tot sluiten van activiteiten</li><li>Openstaande rentenota´s</li><li>Openstaande aanmaningen</li><li>Klantwachtstand</li><li>Verkoopwachtstand</li><li>Vervallen saldi</li><li>Bedragen aanmaningsstatus</li><li>Bedragen aanmaningscode</li><li>Afschrijving op basis van reden</li><li>Te betalen saldo per regio</li><li>Verwachte betalingen</li></ul> |
| Overzicht van crediteringen             | <ul><li>Klanten over tijd</li><li>Kredietlimiet versus achterstallig saldo</li><li>Raster Klanten boven kredietlimiet</li><li>Klanten boven kredietlimiet per bedrijf</li><li>Krediet versus totale kredietlimiet</li><li>Kredietlimiet versus gebruikt krediet per regio</li><li>Klanten per kredietbeoordeling</li></ul> |
| Kredietlimiet                | <ul><li>Kredietlimiet</li><li>Details kredietlimiet</li><li>Kredietlimiet per klant</li><li>Kredietlimiet per klantengroep</li><li>Kredietlimiet per kredietbeoordeling per bedrijf</li><li>Kredietlimiet vs gebruikt krediet per regio</li></ul> |
| Klanten boven kredietlimiet | <ul><li>Klanten boven kredietlimiet</li><li>Details klanten boven kredietlimiet</li><li>Klanten boven kredietlimiet per bedrijf</li><li>Klant boven kredietlimiet per klantengroep</li><li>Klanten boven kredietlimiet per regio</li></ul> |
| Klanten over tijd          | <ul><li>Klanten over tijd</li><li>Details klanten over tijd</li><li>Klanten over tijd per bedrijf</li><li>Klanten over tijd per klantengroep</li><li>Klanten over tijd per regio</li></ul> |
| Vervallen saldi               | <ul><li>Vervallen saldi</li><li>Details vervallen saldi</li><li>Vervallen saldi per bedrijf</li><li>Vervallen saldi per klantengroep</li></ul> |
| Verwachte betalingen           | <ul><li>Verwachte betalingen</li><li>Details verwachte betalingen</li><li>Verwachte betalingen per bedrijf</li><li>Verwachte betalingen per klantengroep</li><li>Verwachte betalingen per regio</li></ul> |
| Afschrijvingen                  | <ul><li>Afschrijvingen per regio</li><li>Details afschrijvingen</li><li>Afschrijvingen per hoofdrekening</li><li>Afschrijvingen per bedrijf</li><li>Afschrijvingen per klantengroep</li><li>Afschrijvingen per regio</li></ul> |
| Aanmaningsstatus          | <ul><li>Betwist</li><li>Belofte om te betalen geschonden</li><li>Beloofd te betalen</li><li>Details aanmaningsstatus</li><li>Bedragen aanmaningsstatus</li><li>Openstaande cases</li><li>Openstaande activiteiten</li></ul> |
| Aanmaningen         | <ul><li>Verzamelingscodebedragen</li><li>Details bedragen aanmaningscode</li><li>Bedrag aanmaningen per bedrijf</li><li>Bedrag aanmaningen per klantengroep</li><li>Bedrag aanmaningen per regio</li></ul> |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over het filteren en vastmaken in Power BI het onderwerp [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). U kunt ook de functionaliteit voor het exporteren van onderliggende gegevens gebruiken om de onderliggende gegevens te exporteren die worden samengevat in een visualisatie.

## <a name="extending-the-power-bi-content"></a>De Power BI-inhoud uitbreiden
Met behulp van de inhoudpakketten die beschikbaar zijn in Microsoft Dynamics Lifecycle Services (LCS) kunt u grondige analyses verschaffen aan personen die zich niet bij Finance and Operations aanmelden. U kunt deze inhoudpakketten wijzigen zodat ze andere rapporten of visuele elementen bevatten, en de inhoudpakketten vervolgens publiceren naar uw Power BI.com-tenant voor analyse.

U vindt de Power BI-inhoud **Crediterings- en aanmaningsbeheer** in de bibliotheek voor gedeelde activa in LCS. Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Let erop dat u de Power BI-inhoud **Crediterings- en aanmaningsbeheer** downloadt die geldt voor de versie van Finance and Operations die u gebruikt.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

De volgende gegevens worden gebruikt om het rapport in de Power BI-inhoud **Finance and Operations** in te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](../../dev-itpro/analytics/power-bi-integration-entity-store.md).

| Entiteit                                      | Belangrijke samengevoegde metingen           | Gegevensbron                                 | Veld                                                      | Omschrijving |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Het aantal afgesloten activiteiten en de gemiddelde tijd tot het sluiten van deze activiteiten. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Het aantal open activiteiten. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | De som van vervallen saldi. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | De bedragen die achterstallig zijn. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Het aantal afgesloten aanvragen en de gemiddelde tijd tot het sluiten van deze aanvragen. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Het aantal openstaande aanvragen. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Het aantal openstaande aanmaningen. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Het saldo van geboekte aanmaningen. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Het saldo van transacties met aanmaningsstatus. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | De som van kredietrisico´s en bedragen waarmee klanten hun kredietlimiet hebben overschreden. |
| CustCollectionsBICustOnHold                 | Geblokkeerd                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Het aantal klanten dat geblokkeerd is. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Dagen uitstaande verkoop voor 30 dagen. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | De som van verwachte betalingen in het volgende jaar. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Het aantal rentenota´s dat is gemaakt. |
| CustCollectionsBISalesOnHold                | SalesId                              | VerkoopTabel                                  | Count(SalesId)                                             | Het aantal totale verkooporders dat geblokkeerd is. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | De som van transacties die zijn afgeschreven. |

