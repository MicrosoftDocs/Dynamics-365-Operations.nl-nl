---
title: Financiële prestatieoplossing PowerBI.com
description: In dit onderwerp wordt de financiële prestatieoplossing PowerBI.com besproken.
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78512e39e82e24f94dae93bbac116e6f07d25438
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "315102"
---
# <a name="financial-performance-powerbicom-solution"></a>Financiële prestatieoplossing PowerBI.com

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Deze PowerBI.com-oplossing is verouderd, zoals gedocumenteerd in [Power BI-inhoudspakketten beschikbaar op AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

In dit onderwerp wordt de **financiële prestatie**-oplossing PowerBI.com besproken. In dit onderwerp wordt een beschrijving gegeven van het dashboard en de rapporten die zijn opgenomen en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de oplossing is samengesteld.

## <a name="main-account-setup"></a>Hoofdrekening instellen
De instelling van de hoofdrekeningen is belangrijk omdat organisaties passiva- en opbrengstenbedragen willen weergeven als positieve bedragen in rapporten. Voor weergave van hoofdrekeningen als positieve bedragen moet het hoofdrekeningtype worden ingesteld op **Passiva** of **Opbrengsten**. Wanneer deze rekeningtypen worden gebruikt, wordt in de rapportage via Power BI het teken omgekeerd en worden de bedragen als positief weergegeven.

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>Dashboard en rapporten die zijn opgenomen in de oplossing PowerBI.com
Het dashboard bevat tegels met samengevatte gegevens, die zijn gebaseerd op onderliggende rapporten. Elke tegel bevat samengevatte informatie voor het huidige jaar, voor alle bedrijven binnen een organisatie. Hieronder ziet u enkele van deze tegels:

- Contant geld
- Totale omzet dit jaar
- Totale kosten dit jaar
- Netto inkomsten dit jaar
- Snelle verhouding
- Totale onkosten dit jaar op rekeningcategorie
- Huidige verhouding
- Debit in totaalaantal activa
- Werkelijke vs. geprognosticeerde omzet
- Gefactureerde omzet dit jaar
- Verhouding exploitatiekosten dit jaar
- Winstmarge dit jaar
- Werkelijke vs. gebudgetteerde kosten - alle bedrijven

Elke tegel wordt ondersteund door een ondersteunend rapport. Deze rapporten bevatten grafieken en tabellen met meer informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                      | Informatie in het rapport |
|-----------------------------|--------------------------------------|
| Analyse contanten               | Contanten, op rechtspersoon; contanten, op kwartaal; totale contanten; contanten op rekening<blockquote>[!NOTE] Kwartaalgegevens over contant geld bevatten geen beginsaldi in het totaal voor het eerste kwartaal. Wel wordt het totaal van nieuwe transacties weergegeven die zijn geboekt in elk kwartaal.</blockquote> |
| Analyse huidige verhouding      | Huidige verhouding op rechtspersoon; huidige verhouding op kwartaal; saldi voor huidige activa en de huidige verplichtingen |
| Snelle verhoudingsanalyse        | Snelle verhouding per rechtspersoon; snelle verhouding per kwartaal en saldi voor contanten, klanten en vlottende passiva |
| Analyse van kosten van verkochte goederen | Kosten van verkochte goederen (COGS) op rechtspersoon; COGS dit jaar en vorig jaar, op kwartaal; COGS t.o.v. verkopen op rechtspersoon; totale COGS en percentage COGS t.o.v. verkoop |
| Analyse werkkapitaal    | Werkkapitaal op rechtspersoon; werkkapitaal op kwartaal, huidige activa, huidige verplichtingen en totaal werkkapitaal |
| Analyse activa en schulden     | Rendement op totale activa en schulden t.o.v. totale activa, op rechtspersoon; schulden t.o.v. totale activa; rendement op totale activa in kwartaal tot heden, activa en verplichtingen |
| Analyse winstmarge      | Werkelijke en gebudgetteerde winstmarge op rechtspersoon; winstmarge per kwartaal; winstmargepercentage en winstmarge |
| Analyse netto-inkomsten         | Werkelijke en gebudgetteerde netto-inkomsten op rechtspersoon; netto-inkomsten dit jaar en vorig jaar; percentage onkosten tegen netto-inkomsten |
| Inkomstenanalyse           | Werkelijke en gebudgetteerde inkomsten vóór rente en belastingen (EBIT) op rechtspersoon; EBIT dit jaar en vorig jaar; percentage onkosten tegen omzet; werkelijke en gebudgetteerde onkosten t.o.v. omzet |
| Opbrengstenanalyse            | Totale opbrengsten; werkelijke en gebudgetteerde totale opbrengsten op rechtspersoon; totale opbrengsten dit jaar en vorig jaar; de afwijking voor inkomstenbudgetten op rechtspersoon; totale opbrengsten deze periode en vorige periode |
| Onkostenanalyse            | Totale onkosten; werkelijke tegen gebudgetteerde totale onkosten op rechtspersoon; werkelijke en gebudgetteerde totale onkosten op kwartaal; totale onkosten op rekeningcategorie; verhouding exploitatiekosten |
| Analyse gefactureerde omzet     | Totaal klanten; totaal klanten per rechtspersoon; totaal klanten per kwartaal en saldi voor klantrekeningen<blockquote>[!NOTE] De informatie bevat geen beginsaldi voor de grootboekrekeningen van klanten. Wel wordt het totaal van nieuwe transacties weergegeven die zijn geboekt naar Klanten.</blockquote> |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De volgende entiteiten zijn gebruikt als basis voor de **financiële prestatie**-oplossing PowerBI.com:

**Samengevoegde gegevensentiteiten**

- **GeneralLedgerActivities**: met deze entiteit worden grootboeksaldi per rekeningcategorie samengevoegd.
- **BudgetActivities**: met deze entiteit worden budgetsaldi per rekeningcategorie samengevoegd.

**Gegevensentiteiten**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Ledgers
- ChartofAccounts

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. De berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in de inhoud worden gebruikt. Standaard levert de inhoud gegevens voor drie voorafgaande jaren en één jaar in de toekomst. Om extra berekeningen op te nemen in uw rapporten en dashboard, kunt u de [Microsoft Excel-werkmap wijzigen](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Deze werkmap is het standaardgegevensmodel, dat is gebruikt om de inhoud te maken.
