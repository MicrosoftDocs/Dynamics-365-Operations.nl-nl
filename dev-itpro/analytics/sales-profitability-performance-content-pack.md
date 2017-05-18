---
title: Power BI-inhoud voor verkoop- en winstgevendheidsprestaties
description: In dit onderwerp wordt beschreven wat het Microsoft Power BI-inhoudpakket Verkoop- en winstgevendheidsprestaties voor Dynamics 365 for Operations bevat. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 35d34f9a356f8a041f2abf0aa8d6c3a6d9ca4a46
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI-inhoud voor verkoop- en winstgevendheidsprestaties

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven wat het Microsoft Power BI-inhoudpakket Verkoop- en winstgevendheidsprestaties voor Dynamics 365 for Operations bevat. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.

<a name="overview"></a>Overzicht
--------

Dit inhoudpakket is opgesteld voor verkoopmanagers, zodat zij de belangrijkste verkoopmeetwaarden voor opbrengsten, brutowinst en winstmarge kunnen bewaken. Op basis van gegevens voor verkooptransacties uit Dynamics 365 for Operations biedt het zowel een samengevoegde weergave van de verkoopcijfers uit het hele bedrijf en een analyse van de verkoopprestaties voor klanten en producten. Wijzigingen in de groei van de opbrengsten en winsten in het verloop van de tijd worden gemarkeerd in rapporten, zodat managers worden gewaarschuwd over positieve en negatieve trends voor afzonderlijke klanten en producten. Categorie- en regiomanagers profiteren van grafieken waarin opbrengsten en winstgevendheid van verschillende productcategorieën en klantengroepen met elkaar worden vergeleken, zodat zij achterblijvers en goedlopende categorieën kunnen identificeren. Met een uitgebreid rapport waarin de opbrengsten en winstmarge van individuele klanten tegen elkaar worden afgezet, vinden accountmanagers de gegevens om hun inspanningen voor verkoop en marketing af te stemmen op de afzonderlijke profielen van hun klanten. Met het inhoudpakket Verkoop- en winstgevendheidprestaties kunnen verkoopmanagers verkoopprestaties analyseren op de volgende factoren:

-   Opbrengst, boekjaar tot heden (op klantengroep en individuele klanten, verkoopcategorieën en afzonderlijke producten en regio's)
-   Opbrengstwijziging, jaar op jaar (op klantenregio en verkoopcategorieën)

De winstgevendheid kan worden geanalyseerd op de volgende factoren:

-   Brutowinst en winstmarge (op klantengroepen en categorieën van productverkoop)
-   Wijziging brutowinst wijziging, jaar op jaar
-   Winstgevendheid klant (op opbrengst versus brutomarge)

## <a name="accessing-the-content-pack"></a>Toegang tot het inhoudpakket
Het Power BI-inhoudpakket Verkoop- en winstgevendheidprestaties wordt gepubliceerd als een implementatieactivum in Lifecycle Services (LCS). U hebt er toegang toe vanuit Dynamics 365 for Operations. Zie voor meer informatie over toegang tot en het openen van Power BI-rapporten [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).
**Opmerking:** KB 4011327 is een vereiste voor deze Power BI-inhoud. Nadat u zich bij Lifecycle Services hebt aangemeld, kunt u de KB hier openen: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>.

## <a name="metrics-included-in-the-content-pack"></a>Metrische gegevens die zijn opgenomen in het inhoudpakket
Het inhoudpakket bevat een rapport dat uit reeks metrische gegevens bestaat, die worden gevisualiseerd als diagrammen, tegels en tabellen. In de volgende tabel vindt u een overzicht van de visualisaties die in het inhoudpakket worden gebruikt.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapportpagina**        | **Diagrammen**                                 | **Tegels**                                               |
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

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Met gegevens in Dynamics 365 for Operations worden de rapporten gevuld in het inhoudpakket Verkoop- en winstgevendheidsprestaties. Deze gegevens worden weergegeven als samengevoegde metingen die worden klaargezet in de Entiteitopslag. Dit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Meer informatie over dit onderwerp vindt u in de blog [Power BI-integratie met de Entiteitopslag in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De samengevoegde metingen in dit inhoudpakket zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Verkoop-cube in Microsoft Dynamics AX 2012 en AX 2012 R3. Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken. Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Power BI-integratie met de Entiteitopslag in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De volgende belangrijke samengevoegde metingen van de entiteit Factuurregels worden gebruikt als basis voor het inhoudpakket.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entiteit**    | **Belangrijke samengevoegde metingen**               | **Gegevensbron voor Dynamics 365 for Operations** | **Veld**                                    | **Beschrijving**                          |
| Factuurregels | Opbrengst                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Bedrag in valuta voor boekhouding            |
|               | Kosten van verkochte goederen                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Kostenbedrag + aanpassing                 |
|               | Provisieregelbedrag – valuta voor boekhouding | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Provisieregelbedrag in valuta voor boekhouding |

In de volgende tabel ziet u de belangrijkste samengevoegde metingen van de entiteit Factuurregel die worden gebruikt om verschillende berekende eenheden te maken in de gegevensset van het inhoudpakket.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Meeteenheid**       | **Berekend als**                                                                                |
| Brutowinst      | SUM(Opbrengst – COGS – Provisie – btw (opgenomen in bedrag klantfactuurregel))          |
| Brutomarge      | SUM(Brutowinst / (Opbrengst - btw (opgenomen in bedrag klantfactuurregel)))             |
| Opbrengst vorig jaar | Opbrengst vorig jaar = CALCULATE(SUM('Factuurregels\[Opbrengst\]), SAMEPERIODLASTYEAR(Datums\[Datum\])) |

De volgende belangrijke dimensies in de **Verkoop-cube** worden gebruikt als filters voor het segmenteren van de samengevoegde metingen om een grotere mate van granulatie te bereiken en analytischere inzichten te bieden.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entiteit**       | **Voorbeelden van kenmerken**                           |
| Klanten        | Klantengroepen, klantregio's, adressen, bedrijfstak |
| Producten         | Productnummer, Productnaam, Naam van artikelengroep       |
| Verkoopcategorieën | Namen verkoopcategorieën                                 |
| Rechtspersonen   | Namen rechtspersonen                                   |
| Datums            | Datums                                                |

Standaard geeft het inhoudpakket gegevens weer voor het huidige kalenderjaar, maar u kunt de sectie rapportfilters openen en het datumfilter wijzigen. U kunt ook het bedrijfsfilter wijzigen.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)





