---
title: "Power BI-inhoud financiële prestaties"
description: "In dit onderwerp wordt het inhoudpakket van Microsoft Power BI voor financiële prestaties van Microsoft Dynamics 365 for Operations beschreven. Ook wordt beschreven hoe u het dashboard en de rapporten kunt gebruiken die in het inhoudpakket zijn opgenomen, en vindt u informatie over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bb9a12dd45e227e86ba47c19f0850a73b77bc735
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="financial-performance-power-bi-content"></a>Power BI-inhoud financiële prestaties

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt het inhoudpakket van Microsoft Power BI voor financiële prestaties van Microsoft Dynamics 365 for Operations beschreven. Ook wordt beschreven hoe u het dashboard en de rapporten kunt gebruiken die in het inhoudpakket zijn opgenomen, en vindt u informatie over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.

<a name="accessing-the-content-pack"></a>Toegang tot het inhoudpakket
--------------------------

Er zijn twee versies van het inhoudpakket voor financiële prestaties beschikbaar. Eén versie is beschikbaar via Microsoft Dynamics Lifecycle Services (LCS) en de andere versie is beschikbaar via PowerBI.com.

-   **Versie die beschikbaar is vanuit LCS:** het inhoudpakket voor financiële prestaties dat beschikbaar is via LCS, ondersteunt Microsoft Dynamics 365 for Operations versie 1611. U kunt het inhoudpakket vinden in de bibliotheek met gedeelde activa in LCS. Zie voor meer informatie over hoe u het inhoudpakket downloadt en koppelt aan uw Microsoft Dynamics 365 for Operations-gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).
-   **Versie die beschikbaar is vanuit PowerBI.com:** het inhoudpakket voor financiële prestaties dat beschikbaar is via PowerBI.com, ondersteunt Microsoft Dynamics AX-versies 7.0 en 7.0.1. Zie voor meer informatie over het koppelen en laden van uw Microsoft Dynamics 365 for Operations-gegevens [Toegang tot Power BI-inhoud via PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Hoofdrekening instellen
De instelling van de hoofdrekeningen in Dynamics 365 for Operations is belangrijk omdat organisaties passiva- en opbrengstenbedragen willen weergeven als positieve bedragen in rapporten. Voor weergave van hoofdrekeningen als positieve bedragen moet het hoofdrekeningtype worden ingesteld op **Passiva** of **Opbrengsten**. Wanneer deze rekeningtypen worden gebruikt, wordt in de rapportage via Microsoft Power BI het teken omgekeerd en worden de bedragen als positief weergegeven.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Dashboard en rapporten die zijn opgenomen in het inhoudpakket
Nadat u het inhoudpakket aan uw Dynamics 365 for Operations-gegevens hebt gekoppeld, geven het dashboard en de rapporten uw financiële gegevens weer. Als u Power BI nog niet eerder hebt gebruikt, raadpleegt u de pagina [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Het dashboard bevat tegels met samengevatte gegevens, die zijn gebaseerd op onderliggende rapporten. Elke tegel bevat samengevatte informatie voor het huidige jaar, voor alle bedrijven binnen een organisatie. Hieronder ziet u enkele van deze tegels:

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

Elke tegel wordt ondersteund door een ondersteunend rapport. Deze rapporten bevatten grafieken en tabellen met meer informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                      | Informatie in het rapport                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analyse contanten               | Contanten per rechtspersoon, contanten per kwartaal, totaal contanten en contanten per rekening **Opmerking:** in het rapport **Contanten per kwartaal** bevat het totaal geen beginsaldi voor het eerste kwartaal. Wel wordt het totaal van nieuwe transacties weergegeven die zijn geboekt in elk kwartaal.                                                                                |
| Analyse huidige verhouding      | Huidige verhouding op rechtspersoon; huidige verhouding op kwartaal; saldi voor huidige activa en de huidige verplichtingen                                                                                                                                                                                                                              |
| Snelle verhoudingsanalyse        | Snelle verhouding per rechtspersoon; snelle verhouding per kwartaal en saldi voor contanten, klanten en vlottende passiva                                                                                                                                                                                                                      |
| Analyse van kosten van verkochte goederen | Kosten van verkochte goederen (COGS) op rechtspersoon; COGS dit jaar en vorig jaar, op kwartaal; COGS t.o.v. verkopen op rechtspersoon; totale COGS en percentage COGS t.o.v. verkoop                                                                                                                                                                                   |
| Analyse werkkapitaal    | Werkkapitaal op rechtspersoon; werkkapitaal op kwartaal, huidige activa, huidige verplichtingen en totaal werkkapitaal                                                                                                                                                                                                                   |
| Analyse activa en schulden     | Rendement op totale activa en schulden t.o.v. totale activa, op rechtspersoon; schulden t.o.v. totale activa; rendement op totale activa in kwartaal tot heden, activa en verplichtingen                                                                                                                                                                                     |
| Analyse winstmarge      | Werkelijke en gebudgetteerde winstmarge op rechtspersoon; winstmarge per kwartaal; winstmargepercentage en winstmarge                                                                                                                                                                                                                       |
| Analyse netto-inkomsten         | Werkelijke en gebudgetteerde netto-inkomsten op rechtspersoon; netto-inkomsten dit jaar en vorig jaar; percentage onkosten tegen netto-inkomsten                                                                                                                                                                                                                       |
| Inkomstenanalyse           | Werkelijke en gebudgetteerde inkomsten vóór rente en belastingen (EBIT) op rechtspersoon; EBIT dit jaar en vorig jaar; percentage onkosten tegen omzet; werkelijke en gebudgetteerde onkosten t.o.v. omzet                                                                                                                                                          |
| Opbrengstenanalyse            | Totale opbrengsten; werkelijke en gebudgetteerde totale opbrengsten op rechtspersoon; totale opbrengsten dit jaar en vorig jaar; de afwijking voor inkomstenbudgetten op rechtspersoon; totale opbrengsten deze periode en vorige periode                                                                                                                                                 |
| Onkostenanalyse            | Totale onkosten; werkelijke tegen gebudgetteerde totale onkosten op rechtspersoon; werkelijke en gebudgetteerde totale onkosten op kwartaal; totale onkosten op rekeningcategorie; verhouding exploitatiekosten                                                                                                                                                                 |
| Analyse gefactureerde omzet     | Totaal klanten, totaal klanten per rechtspersoon, totaal klanten per kwartaal en saldi voor klantrekeningen **Opmerking:** de rapporten bevatten geen beginsaldi voor de grootboekrekeningen van klanten. Wel wordt het totaal van nieuwe transacties weergegeven die zijn geboekt naar Klanten. |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over het filteren en vastmaken in Power BI het onderwerp [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De gegevens waarmee het dashboard en de rapporten in het inhoudpakket voor financiële prestaties worden gevuld, zijn Dynamics 365 for Operations-gegevens. De volgende entiteiten zijn gebruikt als basis voor het inhoudpakket: **Samengevoegde gegevensentiteiten**

-   **GeneralLedgerActivities**: met deze entiteit worden grootboeksaldi per rekeningcategorie samengevoegd.
-   **BudgetActivities**: met deze entiteit worden budgetsaldi per rekeningcategorie samengevoegd.

**Gegevensentiteiten**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Ledgers
-   ChartofAccounts

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. De berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in het inhoudpakket worden gebruikt. Standaard levert het inhoudpakket gegevens voor drie voorafgaande jaren en één jaar in de toekomst. Om extra berekeningen op te nemen in uw rapporten en dashboard, kunt u de [Microsoft Excel-werkmap](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) wijzigen. Deze werkmap is het standaardgegevensmodel, dat is gebruikt om het inhoudpakket te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)





