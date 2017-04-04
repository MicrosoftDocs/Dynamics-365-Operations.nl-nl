---
title: "Financiële prestaties Power BI-inhoud"
description: "Dit onderwerp beschrijft de Microsoft Dynamics 365 voor bedrijfsactiviteiten financiële prestaties content pack voor Microsoft Power BI. Deze beschrijving van het dashboard en rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Financiële prestaties Power BI-inhoud

Dit onderwerp beschrijft de Microsoft Dynamics 365 voor bedrijfsactiviteiten financiële prestaties content pack voor Microsoft Power BI. Deze beschrijving van het dashboard en rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de content pack.

<a name="accessing-the-content-pack"></a>Toegang tot de content pack
--------------------------

Er zijn twee versies van de financiële prestaties content pack beschikbaar. Één versie is beschikbaar vanuit Microsoft Dynamics Lifecycle Services (LCS) en de andere is beschikbaar vanuit PowerBI.com.

-   **Versie die beschikbaar is vanuit LCS:** de financiële prestaties content pack die beschikbaar is vanuit LCS ondersteunt Microsoft Dynamics 365 voor bewerkingen versie 1611. U kunt de inhoud pack vinden in de bibliotheek met gedeelde elementen in LCS. Zie voor meer informatie over het downloaden van de content pack en deze verbinden met uw Microsoft Dynamics 365 voor bewerkingen gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).
-   **Versie die beschikbaar is in PowerBI.com:** Microsoft Dynamics AX-versie 7.0 en 7.0.1 biedt ondersteuning voor de financiële prestaties content pack die beschikbaar is in PowerBI.com. Zie voor meer informatie over het maken en uw Dynamics 365 voor bewerkingen gegevens laden, [toegang Power BI-inhoud van PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Instelling van hoofdrekening
De instelling van de hoofdrekeningen in Dynamics 365 for Operations is belangrijk omdat organisaties passiva en opbrengstbedragen weergegeven als positieve bedragen in rapporten kunnen. Voor deze hoofdrekeningen worden weergegeven als positieve bedragen, het hoofdrekeningtype moet worden ingesteld op **passiva** of **opbrengsten**. Wanneer deze rekeningtypen worden gebruikt, rapportage via Microsoft Power BI het teken omkeren en de bedragen als positief.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Dashboard en rapporten die zijn opgenomen in de content pack
Nadat u het inhoudpakket aan uw Dynamics 365 for Operations-gegevens hebt gekoppeld, geven het dashboard en de rapporten uw financiële gegevens weer. Als u Power BI vóór nooit hebt gebruikt, kunt u meer informatie op de [cursuspagina voor Power BI begeleide](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Het dashboard bevat tegels met samengevatte gegevens, die zijn gebaseerd op onderliggende rapporten. Elke tegel bevat samengevatte informatie voor het huidige jaar, voor alle bedrijven binnen een organisatie. Hier volgen enkele van de tegels:

-   Contant geld
-   Totale omzet dit jaar
-   Totale kosten dit jaar
-   Netto inkomsten dit jaar
-   Snelle verhouding
-   Totale onkosten dit jaar op rekeningcategorie
-   Huidige verhouding
-   Debit in totaalaantal activa
-   Werkelijke vs. geprognosticeerde omzet
-   Gefactureerde omzet dit jaar
-   Verhouding exploitatiekosten dit jaar
-   Winstmarge dit jaar
-   Werkelijke vs. gebudgetteerde kosten - alle bedrijven

Elke tegel wordt voorgesteld door een ondersteunende rapport. Deze rapporten bevatten grafieken en tabellen met meer informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                      | Informatie in het rapport                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analyse contanten               | Contanten, door de rechtspersoon, cash per kwartaal, Totaal contanten en contanten, door rekening **opmerking:** de **contant per kwartaal** niet opgenomen in lijst beginsaldi in het totaal voor het eerste kwartaal. Deze bevat het totaal van nieuwe transacties die zijn geboekt per kwartaal.                                                                                |
| Analyse huidige verhouding      | Huidige verhouding op rechtspersoon; huidige verhouding op kwartaal; saldi voor huidige activa en de huidige verplichtingen                                                                                                                                                                                                                              |
| Snelle verhoudingsanalyse        | Snelle verhouding per rechtspersoon, snelle verhouding per kwartaal en saldi voor contant geld, rekeningen klanten en huidige verplichtingen                                                                                                                                                                                                                      |
| Analyse van kosten van verkochte goederen | Kosten van verkochte goederen (COGS) op rechtspersoon; COGS dit jaar en vorig jaar, op kwartaal; COGS t.o.v. verkopen op rechtspersoon; totale COGS en percentage COGS t.o.v. verkoop                                                                                                                                                                                   |
| Analyse werkkapitaal    | Werkkapitaal op rechtspersoon; werkkapitaal op kwartaal, huidige activa, huidige verplichtingen en totaal werkkapitaal                                                                                                                                                                                                                   |
| Analyse activa en schulden     | Rendement op totale activa en schulden t.o.v. totale activa, op rechtspersoon; schulden t.o.v. totale activa; rendement op totale activa in kwartaal tot heden, activa en verplichtingen                                                                                                                                                                                     |
| Analyse winstmarge      | Werkelijke en gebudgetteerde winstmarge op rechtspersoon; winstmarge per kwartaal; winstmargepercentage en winstmarge                                                                                                                                                                                                                       |
| Analyse netto-inkomsten         | Werkelijke en gebudgetteerde netto-inkomsten op rechtspersoon; netto-inkomsten dit jaar en vorig jaar; percentage onkosten tegen netto-inkomsten                                                                                                                                                                                                                       |
| Inkomstenanalyse           | Werkelijke en gebudgetteerde inkomsten vóór rente en belastingen (EBIT) op rechtspersoon; EBIT dit jaar en vorig jaar; percentage onkosten tegen omzet; werkelijke en gebudgetteerde onkosten t.o.v. omzet                                                                                                                                                          |
| Opbrengstenanalyse            | Totale opbrengsten; werkelijke en gebudgetteerde totale opbrengsten op rechtspersoon; totale opbrengsten dit jaar en vorig jaar; de afwijking voor inkomstenbudgetten op rechtspersoon; totale opbrengsten deze periode en vorige periode                                                                                                                                                 |
| Onkostenanalyse            | Totale onkosten; werkelijke tegen gebudgetteerde totale onkosten op rechtspersoon; werkelijke en gebudgetteerde totale onkosten op kwartaal; totale onkosten op rekeningcategorie; verhouding exploitatiekosten                                                                                                                                                                 |
| Analyse gefactureerde omzet     | Totaalaantal debiteuren, totaal klanten per rechtspersoon, totaal klanten per kwartaal en saldi voor debiteurenrekeningen **opmerking:** de rapporten bevatten geen beginsaldi voor de accounts receivable grootboekrekeningen. Deze kleuren geven aan het totaal van nieuwe transacties die zijn geboekt naar rekeningen te ontvangen. |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over het filteren en vastmaken in Power BI het onderwerp [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De gegevens die u invult op de dashboard en rapporten in de financiële prestaties content pack is Dynamics 365 voor operationele gegevens. De volgende entiteiten zijn gebruikt als basis voor de content pack: **gegevensentiteiten samenvoegen**

-   **GeneralLedgerActivities** : deze entiteit aggregeert grootboeksaldi op rekeningcategorie.
-   **budgetActivities** : deze entiteit aggregeert budgetsaldi op rekeningcategorie.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Ledgers
-   ChartofAccounts

Deze entiteiten zijn gebruikt voor het maken van berekende eenheden in het gegevensmodel. De berekende eenheden worden gebruikt voor het berekenen van de key performance indicators (KPI's) en rapporten die worden gebruikt in de content pack. Standaard levert het inhoudpakket gegevens voor drie voorafgaande jaren en één jaar in de toekomst. Om extra berekeningen op te nemen in uw rapporten en dashboard, kunt u de [Microsoft Excel-werkmap](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) wijzigen. Deze werkmap is het standaardgegevensmodel, dat is gebruikt om het inhoudpakket te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)



