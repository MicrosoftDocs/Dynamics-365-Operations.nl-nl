---
title: "Financiële rapportage"
description: "In dit onderwerp wordt beschreven waar u toegang kunt krijgen tot financiële rapportage in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition en hoe u de financiële rapportagemogelijkheden kunt gebruiken. Het bevat een omschrijving van de financiële standaardrapporten die worden geleverd."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fedde78a563939fd7080e748c412c89c71586823
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="financial-reporting"></a>Financiële rapportage

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven waar u toegang kunt krijgen tot financiële rapportage in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition en hoe u de financiële rapportagemogelijkheden kunt gebruiken. Het bevat een omschrijving van de financiële standaardrapporten die worden geleverd.

<a name="accessing-financial-reporting"></a>Toegang verkrijgen tot financiële rapportage
-----------------------------

U vindt het menu **Financiële rapportage** op de volgende locaties in Finance and Operations:

-   **Grootboek** &gt; **Query's en rapporten**
-   **Budgettering** &gt; **Query's en rapporten** &gt; **Basisbudgettering**
-   **Budgettering** &gt; **Query's en rapporten** &gt; **Budgetplanning**
-   **Budgettering** &gt; **Query's en rapporten** &gt; **Budgetbeheer**
-   Consolidaties

Als u financiële rapporten voor een rechtspersoon wilt maken en genereren, moet u de volgende informatie voor die rechtspersoon instellen:

-   Fiscale kalender
-   Grootboek
-   Rekeningschema
-   Valuta

De functies voor financiële rapportage zijn beschikbaar voor gebruikers aan wie de juiste bevoegdheden en functies zijn toegewezen via hun beveiligingsrollen. De volgende secties beschrijven bevoegdheden en functies, samen met de gekoppelde rollen.

### <a name="duties"></a>Functies

| Functielabel                            | Beschrijving                                                             | AOT-naam                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Beveiliging van financiële rapporten onderhouden | Beveiliging van financiële rapportage onderhouden en administratieve taken uitvoeren. | FinancialReportsSecurityMaintain |
| Financiële rapporten onderhouden            | Financiële rapporten ontwerpen en onderhouden.                                  | FinancialReportsMaintain         |
| Financiële rapporten genereren            | Financiële rapporten genereren en vernieuwen.                                 | FinancialReportsGenerate         |
| Financiële prestaties beoordelen          | Financiële prestaties beoordelen en analyseren.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Bevoegdheden

| Bevoegdheidslabel                       | Beschrijving                                                             | AOT-naam                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Beveiliging van financiële rapporten onderhouden | Beveiliging van financiële rapportage onderhouden en administratieve taken uitvoeren. | FinancialReportsSecurityMaintain |
| Financiële rapporten onderhouden            | Financiële rapporten ontwerpen en onderhouden.                                  | FinancialReportsMaintainReports  |
| Financiële rapporten genereren            | Financiële rapporten genereren en vernieuwen.                                 | FinancialReportsGenerateReports  |
| Financiële rapporten weergeven                | Financiële rapporten weergeven.                                                 | FinancialReportsView             |

### <a name="roles"></a>Rollen

| Bevoegdheidslabel                       | Functie                                  | Rollen                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Beveiliging van financiële rapporten onderhouden | Beveiliging van financiële rapporten onderhouden | Beveiligingsbeheerder                                                          |
| Financiële rapporten onderhouden            | Financiële rapporten onderhouden            | Accounting manager, Supervisor boekhouding, Financieel controller, Budgetbeheerder |
| Financiële rapporten genereren            | Financiële rapporten genereren            | CEO, CFO, accountant                                                            |
| Financiële rapporten weergeven                | Financiële prestaties beoordelen          | Niet toegewezen                                                                   |

Nadat een gebruiker is toegevoegd of een rol is gewijzigd, moet de gebruiker binnen enkele minuten toegang hebben tot financiële rapportage. **Opmerking:** de rol sysadmin wordt toegevoegd aan alle rollen in de financiële rapportage.

## <a name="default-reports"></a>Standaardrapporten
Financiële rapportage bevat 22 standaard financiële rapporten. Elk rapport gebruikt de standaardcategorieën van de hoofdrekening in Finance and Operations. U kunt deze rapporten ongewijzigd of als starpunt voor uw financiële rapportagevereisten gebruiken. Naast de normale financiële overzichten, zoals Inkomensoverzicht en Balans, bevatten deze standaardrapporten ook rapporten waarop de verschillende typen financiële rapporten die u kunt maken, worden weergegeven. Elk rapport in de volgende tabel is gekoppeld aan een Office Mix-presentatie over het rapport.

| Standaardrapport                                                                                         | Omschrijving                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 maanden-samenvoeging inkomensoverzicht in één kolom – Standaard](https://mix.office.com/watch/76kc7bm3wnt1) | De winstgevendheid van een organisatie over de afgelopen 12 maanden in één kolom bekijken.                                                                                                                                                                                                                                      |
| [12 maanden trendinkomensoverzicht – Standaard](https://mix.office.com/watch/12brmfge5p8r)                 | De winstgevendheid van een organisatie voor elk van de afgelopen 12 maanden bekijken. Deze 12 maanden kunnen meer dan één boekjaar beslaan.                                                                                                                                                                                             |
| [Werkelijk vs. Budget – Standaard](https://mix.office.com/watch/fi439lkwr0no)                                | Gedetailleerde saldogegevens voor alle rekeningen voor het oorspronkelijke budget weergeven en het herziene budget vergelijken met werkelijke waarden die een afwijking hebben.                                                                                                                                                                          |
| [Auditdetails – Standaard](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Gedetailleerde saldogegevens voor alle rekeningen bekijken. Dit rapport toont debet- en creditsaldi in de aangiftevaluta en lokale valuta, samen met aanvullende transactiegegevens, zoals de gebruikers-ID, de gebruiker die de gegevens het laatst heeft gewijzigd, de datum van de laatste wijziging en de journaal-ID. |
| [Saldilijst – Standaard](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Gedetailleerde saldogegevens voor alle rekeningen bekijken. Dit rapport geeft openings- en eindsaldi, en debet- en creditsaldi voor de huidige periode en tot heden, samen met aanvullende transactiegegevens, zoals het boekstuk.                                                                    |
| [Balans – Standaard](https://mix.office.com/watch/zkgq0u7visw9)                                   | De financiële positie van de organisatie voor het jaar weergeven.                                                                                                                                                                                                                                                             |
| [Balans en Inkomensoverzicht naast elkaar - Standaard](https://mix.office.com/watch/zkgq0u7visw9) | De financiële positie en de rentabiliteit van de organisatie voor het jaar naast elkaar weergeven.                                                                                                                                                                                                                              |
| [Cashflow – Standaard](https://mix.office.com/watch/jd3go9pz6390)                                       | Inzicht verkrijgen in contact geld dat de organisatie in en uit gaat.                                                                                                                                                                                                                                   |
| [Gedetailleerde JE en TB-controle – Standaard](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Weergaveopeningssaldo en activiteitinformatie voor alle accounts.                                                                                                                                                                                                                                                      |
| [Gedetailleerde proefbalans - Standaard](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Saldogegevens weergeven voor alle rekeningen met debet- en creditsaldi, en het nettobedrag van deze saldi, samen met de transactiedatum, het boekstuk en de journaalomschrijving.                                                                                                                                  |
| [Onkosten driejarige kwartaaltrend - Standaard](https://mix.office.com/watch/gwm4zu7tmtj8)             | Inzicht verkrijgen in onkosten over de afgelopen 12 kwartalen gedurende de afgelopen drie jaar.                                                                                                                                                                                                                                   |
| [Financiële bijschriften JE en TB-controle – Standaard](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Een overzicht bekijken van de saldi en de activiteit voor de financiële bijschriften voor activa, aansprakelijkheid, het eigen vermogen van de eigenaar, opbrengsten, onkosten, winst of verlies.                                                                                                                                                                           |
| [Inkomensoverzicht – Standaard](https://mix.office.com/watch/sbuhgl5hzuhi)                                | De rentabiliteit van de organisatie voor de huidige periode en het jaar tot heden weergeven.                                                                                                                                                                                                                                   |
| [Grootboektransactielijst – Standaard](https://mix.office.com/watch/19h9v2rmh48vy)                        | Gedetailleerde saldogegevens voor alle rekeningen bekijken. Dit rapport geeft debet- en creditsaldi, samen met aanvullende transactiegegevens, zoals de transactiedatum, het journaalnummer, het boekstuk, het boekingstype en traceringsnummer.                                                                            |
| [Ratio's – Standaard](https://mix.office.com/watch/b08hfc5h92me)                                          | De solvabiliteit, rentabiliteit en efficiëntiepercentages van de organisatie voor het jaar weergeven.                                                                                                                                                                                                                           |
| [Onkosten opvolgende 12 maanden – Standaard](https://mix.office.com/watch/iywod5qmqhz7)                       | Inzicht verkrijgen in onkosten voor elk van de laatste 12 maanden. Deze 12 maanden kunnen meer dan één boekjaar beslaan.                                                                                                                                                                                                       |
| [Inkomensoverzicht opvolgende kwartalen- Standaard](https://mix.office.com/watch/1k4yl6a6oyxqc)               | De rentabiliteit van een organisatie op kwartaalbasis voor het afgelopen jaar en het jaar tot heden weergeven.                                                                                                                                                                                                                   |
| [Balans naast elkaar - Standaard](https://mix.office.com/watch/zkgq0u7visw9)                      | De financiële positie van de organisatie voor het jaar weergeven. Op dit rapport worden activa en aansprakelijkheid, en het eigen vermogen van de aandeelhouder naast elkaar weergegeven.                                                                                                                                                                                |
| [Overzicht proefbalans – Standaard](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | De saldogegevens voor alle rekeningen openings- en afsluitingssaldi hebben, en debet- en creditsaldi samen met hun netto verschil.                                                                                                                                                                  |
| [Overzicht proefbalansjaar van jaar tot jaar - Standaard](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Saldogegevens weergeven voor alle rekeningen die openings- en eindsaldi hebben, en debet- en creditsaldi samen met hun nettoverschil voor het huidige en afgelopen jaar.                                                                                                                           |
| [Wekelijkse verkoop en kortingen - Standaard](https://mix.office.com/watch/112ng0hy5de0j)                     | Inzicht verkrijgen in verkoop en kortingen voor elke week in een maand. Dit rapport bevat een totaal van vier weken.                                                                                                                                                                                                              |
| [Beschikbare budgetfondsen- Standaard](https://mix.office.com/watch/15hcpezcbx7tv)                         | Een gedetailleerde vergelijking weergeven van het herziene budget, feitelijke uitgaven, budgetreserveringen en budgetfondsen die beschikbaar zijn voor alle rekeningen                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Financiële rapporten openen
Wanneer u op het menu **Financiële rapportage** klikt, wordt de lijst van financiële rapporten voor het bedrijf weergegeven. U kunt een rapport vervolgens openen of wijzigen. Als u een van de standaardrapporten wilt openen, selecteert u de rapportnaam. De eerste keer dat een rapport wordt geopend, wordt het automatisch gegenereerd voor de vorige maand. Als u bijvoorbeeld een rapport voor de eerste keer opent in augustus 2016, wordt het rapport gegenereerd voor 31 juli 2016. Nadat een rapport is geopend, kunt u beginnen met het verkennen ervan door in te zoomen op specifieke gegevensitems en rapportopties te wijzigen.

## <a name="creating-and-modifying-financial-reports"></a>Het maken en wijzigen van het financiële rapporten
Via de financiële verslagenlijst kunt u een nieuw rapport maken of een bestaand rapport wijzigen. Als u de juiste machtigingen hebt, kunt u een nieuwe financieel rapport maken door te klikken op **Nieuw** in het actievenster. Er wordt een rapportontwerpersprogramma gedownload naar uw apparaat. Nadat de rapportontwerper is gestart, kunt u vervolgens het nieuwe rapport maken. Nadat u het nieuwe rapport hebt opgeslagen, verschijnt het in de lijst met financiële rapporten. De lijst bevat alleen rapporten die voor het bedrijf zijn gemaakt en die u in Finance and Operations gebruikt. Raadpleeg voor meer informatie over het maken en wijzigen van financiële rapporten in Finance and Operations deze [blogberichten](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) uit de blog voor financiële rapportage van Dynamics. **Opmerking:** op de computer waarop u de rapportontwerpersclient downloadt, moet versie 4.6.2 van Microsoft .NET Framework zijn geïnstalleerd. Deze versie van Microsoft .NET Framework kan worden gedownload en geïnstalleerd vanaf [hier](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Als u Chrome gebruikt, moet u een ClickOnce-extensie installeren om de rapportontwerpersclient te downloaden. Als u in de incognito modus werkt, moet u ervoor zorgen dat de ClickOnce-extensie voor de incognito modus is ingeschakeld. U kunt ook een rapport wijzigen dat in de lijst met financiële rapporten verschijnt. Wanneer u het gebied rond de rapportnaam hebt geselecteerd, klikt u op **Bewerken** in het Actievenster. Het rapportontwerperprogramma wordt gestart.

<a name="see-also"></a>Zie ook
--------

[Financiële rapporten weergeven](view-financial-reports.md)

[Blog met financiële rapportage van Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)



