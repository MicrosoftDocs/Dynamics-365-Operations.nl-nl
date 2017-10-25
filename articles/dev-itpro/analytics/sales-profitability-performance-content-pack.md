---
title: Power BI-inhoud over prestaties op het gebied van verkoop en winstgevendheid
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Verkoop- en winstgevendheidsprestaties. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97c8f3d57ba1accb8d940c7edd3ddcac2146968b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI-inhoud over prestaties op het gebied van verkoop en winstgevendheid

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Verkoop- en winstgevendheidsprestaties**. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** is opgesteld zodat verkoopmanagers de belangrijkste verkoopmeetwaarden, namelijk opbrengst, brutowinst en winstmarge, kunnen controleren. Op basis van gegevens voor verkooptransacties biedt het zowel een samengevoegde weergave van de verkoopcijfers uit het hele bedrijf als ook een analyse van de verkoopprestaties voor klanten en producten.

Rapporten markeren wijzigingen in opbrengst en winst die in de loop van de tijd optreden. Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends voor afzonderlijke klanten en producten. Bovendien vergelijken diagrammen de inkomsten en winstgevendheid van de verschillende productcategorieën en klantengroepen met elkaar. Zo kunnen categorie- en regiomanagers achterblijvers en leiders identificeren. Tenslotte geeft een uitgebreid rapport de omzet van een individuele klant ten opzichte van de winstmarge weer. Accountmanagers hebben daarmee een fundament op basis van gegevens, waarmee ze hun inspanningen voor verkoop en marketing op het profiel van elke klant kunnen afstemmen. 

Met het inhoudpakket **Verkoop- en winstgevendheidprestaties** kunnen verkoopmanagers verkoopprestaties analyseren op de volgende manieren:

-   Opbrengst, boekjaar tot heden (op klantengroep en individuele klanten, verkoopcategorieën en afzonderlijke producten en regio's)
-   Opbrengstwijziging, jaar op jaar (op klantenregio en verkoopcategorieën)

Winstgevendheid kan worden geanalyseerd op de volgende manieren:

-   Brutowinst en winstmarge (op klantengroepen en categorieën van productverkoop)
-   Wijziging brutowinst wijziging, jaar op jaar
-   Winstgevendheid klant (op opbrengst versus brutomarge)

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), vindt u de Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** op de pagina **Verkoop- en winstgevendheidsprestaties** (**Verkoop en marketing** > **Query's en rapporten** > **Verkoopprestatieanalyse** > **Verkoop- en winstgevendheidsprestaties**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** bevat een rapport dat uit een verzameling van metrische gegevens bestaat. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. In de volgende tabel vindt u een overzicht van de visualisaties die in de inhoud worden gebruikt.

| Rapportpagina            | Diagrammen                                     | Tegels                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Opbrengst op klant    | Top 10-klanten op opbrengst                | Totale opbrengst                                           |
|                        | Totale opbrengst op klantgroep            | Opbrengststijging jaar-op-jaar                                      |
|                        | Gemiddelde omzet van klanten, op klantgroep | Brutomarge                                            |
|                        | Opbrengst & brutowinst op klantengroep   |                                                         |
| Opbrengst op product     | Opbrengst & brutowinst op verkoopcategorie   | Totaal aantal producten                                    |
|                        | Top 10-producten op opbrengst                 | Totaal aantal actieve producten en percentage van totaal |
|                        | Totale opbrengst op verkoopcategorie            | Aantal producten dat 80% van opbrengst oplevert           |
| Opbrengste op periode\*    | Opbrengst per maand                           | Opbrengststijging jaar-op-jaar                                      |
|                        | Achterblijvende opbrengstafwijking, jaar-op-jaar             | % opbrengststijging jaar-op-jaar                                    |
|                        | Totale verkoopafwijking op klantregio    |                                                         |
| Opbrengst op locatie    | Verkoopopbrengst op plaats                      |                                                         |
|                        | % opbrengststijging jaar-op-jaar                       |                                                         |
|                        | Verkoopopbrengst op regio                    |                                                         |
| Winstgevendheid klant | Brutomarge versus opbrengst, op klant   | Brutowinst, brutomarge, opbrengstgroei jaar-op-jaar          |
| Rentabiliteitsanalyse | Opbrengst en brutowinst per maand          |                                                         |
|                        | Top 15-klanten op brutomarge           |                                                         |
|                        | Brutowinst per maand, jaar-op-jaar                 |                                                         |

\* Opbrengst dit jaar en vorig jaar en groei per verkoopcategorie.

## <a name="extending-the-power-bi-content"></a>De Power BI-inhoud uitbreiden
Met behulp van de inhoudpakketten die beschikbaar zijn in Microsoft Dynamics Lifecycle Services (LCS) kunt u grondige analyses verschaffen aan personen die zich niet bij Microsoft Dynamics 365 aanmelden. U kunt deze inhoudpakketten wijzigen zodat ze andere rapporten of visuele elementen bevatten, en de inhoudpakketten vervolgens publiceren naar uw Power BI.com-tenant voor analyse.

U vindt de Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** in de bibliotheek voor gedeelde materialen in LCS. Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Let erop dat u de inhoud **Verkoop- en winstgevendheidsprestaties** downloadt, die van toepassing is voor de versie van Dynamics 365 die u gebruikt.

> [!NOTE]
> Als u werkt met Microsoft Dynamics 365 for Operations, versie 1611, is KB 4011327 een voorwaarde voor gebruik van deze volgende Power BI-inhoud: Nadat u zich bij LCS hebt aangemeld, kunt u de KB hier openen: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De volgende gegevens wordt gebruikt om de rapportpagina's in de Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md). 

De samengevoegde metingen in deze inhoud zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Verkoop-cube in Microsoft Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3. Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken. Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). 

De volgende belangrijke samengevoegde metingen van de entiteit Factuurregels worden gebruikt als basis voor de inhoud.

| Entiteit        | Belangrijke samengevoegde metingen                   | Gegevensbron voor Dynamics 365                    | Veld                                        | Omschrijving                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Factuurregels | Opbrengst                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Het bedrag in de valuta voor boekhouding.            |
|               | Kosten van verkochte goederen                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | De som van het kostenbedrag en de correctie.    |
|               | Provisieregelbedrag – valuta voor boekhouding | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Het provisiebedrag in de boekhoudvaluta. |

In de volgende tabel ziet u de belangrijkste samengevoegde metingen van de entiteit Factuurregel die worden gebruikt om verschillende berekende eenheden te maken in de gegevensset van de inhoud.

| Maat           | Berekening                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Brutowinst      | SUM(Opbrengst – COGS – Provisie – btw (opgenomen in bedrag klantfactuurregel))          |
| Brutomarge      | SUM(Brutowinst / (Opbrengst - btw (opgenomen in bedrag klantfactuurregel)))             |
| Opbrengst vorig jaar | Opbrengst vorig jaar = CALCULATE(SUM('Factuurregels\[Opbrengst\]), SAMEPERIODLASTYEAR(Datums\[Datum\])) |

De volgende belangrijke dimensies in de Verkoop-cube worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.

| Entiteit           | Voorbeelden van kenmerken                               |
|------------------|------------------------------------------------------|
| Klanten        | Klantengroepen, klantregio's, adressen, bedrijfstak |
| Producten         | Productnummer, Productnaam, Naam van artikelengroep       |
| Verkoopcategorieën | Namen verkoopcategorieën                                 |
| Rechtspersonen   | Namen rechtspersonen                                   |
| Datums            | Datums                                                |

Standaard worden gegevens in de inhoud weergegeven voor het huidige kalenderjaar. U kunt echter het datumfilter in de sectie rapportfilters wijzigen. U kunt ook het bedrijfsfilter wijzigen.
