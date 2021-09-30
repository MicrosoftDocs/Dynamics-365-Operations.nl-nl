---
title: Overzicht financiële rapportage
description: In dit onderwerp wordt beschreven waar u toegang kunt krijgen tot financiële rapportage in Microsoft Dynamics 365 Finance en hoe u de financiële rapportagemogelijkheden kunt gebruiken.
author: aprilolson
ms.date: 07/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 464092ae2fdcdfd8a0ada254e88f4418c825c1f9
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486965"
---
# <a name="get-started-with-financial-reporting"></a>Aan de slag met financiële rapportage 

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven waar u toegang kunt krijgen tot Financial reporting en hoe u de financiële rapportagemogelijkheden kunt gebruiken. Het bevat ook een omschrijving van de financiële standaardrapporten die worden geleverd.

## <a name="accessing-financial-reporting"></a>Toegang verkrijgen tot financiële rapportage

U vindt het menu **Financiële rapportage** op de volgende locaties:

- **Grootboek** &gt; **Query's en rapporten**
- **Budgettering** &gt; **Query's en rapporten** &gt; **Basisbudgettering**
- **Budgettering** &gt; **Query's en rapporten** &gt; **Budgetplanning**
- **Budgettering** &gt; **Query's en rapporten** &gt; **Budgetbeheer**
- Consolidaties

Als u financiële rapporten voor een rechtspersoon wilt maken en genereren, moet u de volgende informatie voor die rechtspersoon instellen:

- Fiscale kalender
- Ledger
- Rekeningschema
- Valuta
- Een transactie naar ten minste één rekening boeken
- MainAccount wordt weergegeven in de kolom **Geselecteerd** op de pagina **Instellingen Financial reporting** (**Grootboek > Instellingen grootboek > Instellingen financiële rapportage**)

## <a name="granting-security-access-to-financial-reporting"></a>Beveiligingstoegang verlenen tot Financial reporting

De functies voor financiële rapportage zijn beschikbaar voor gebruikers aan wie de juiste bevoegdheden en functies zijn toegewezen via hun beveiligingsrollen. De volgende secties beschrijven bevoegdheden en functies, samen met de gekoppelde rollen.

### <a name="duties"></a>Functies

| Functielabel                            | Beschrijving                                                             | AOT-naam                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Beveiliging van financiële rapporten onderhouden | Beveiliging van Financial reporting onderhouden en administratieve taken uitvoeren. | FinancialReportsSecurityMaintain |
| Financiële rapporten onderhouden            | Financiële rapporten ontwerpen en onderhouden.                                  | FinancialReportsMaintain         |
| Financiële rapporten genereren            | Financiële rapporten genereren en vernieuwen.                                 | FinancialReportsGenerate         |
| Financiële prestaties beoordelen          | Financiële prestaties beoordelen en analyseren.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Bevoegdheden

| Bevoegdheidslabel                       | Beschrijving                                                             | AOT-naam                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Beveiliging van financiële rapporten onderhouden | Beveiliging van Financial reporting onderhouden en administratieve taken uitvoeren. | FinancialReportsSecuritySystemMaintain |
| Financiële rapporten onderhouden            | Financiële rapporten ontwerpen en onderhouden.                                  | FinancialReportsMaintainReports  |
| Financiële rapporten genereren            | Financiële rapporten genereren en vernieuwen.                                 | FinancialReportsGenerateReports  |
| Financiële rapporten weergeven                | Financiële rapporten weergeven.                                                 | FinancialReportsView             |

### <a name="roles"></a>Rollen

| Bevoegdheidslabel                       | Verplichting                                  | Rollen                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Beveiliging van financiële rapporten onderhouden | Beveiliging van Financial reporting onderhouden | Beveiligingsbeheerder                                                          |
| Financiële rapporten onderhouden            | Financiële rapporten onderhouden            | Accounting manager, Supervisor boekhouding, Financieel controller, Budgetbeheerder |
| Financiële rapporten genereren            | Financiële rapporten genereren            | CEO, CFO, accountant                                                            |
| Financiële rapporten weergeven                | Financiële prestaties beoordelen          | Niet toegewezen                                                                   |

Nadat een gebruiker is toegevoegd aan een rol of een rol is gewijzigd, moet de gebruiker binnen enkele minuten toegang hebben tot Financial reporting. 

> [!NOTE]
> De rol sysadmin wordt toegevoegd aan alle rollen in de financiële rapportage.

## <a name="report-deletions-and-expirations"></a>Verwijderde en verlopen rapporten

Gebruikers die een rapport genereren, kunnen hun eigen rapporten verwijderen. Gebruikers met de functie **Beveiliging van financiële rapporten onderhouden** kunnen rapporten van anderen verwijderen. 

In release 10.0.8 is het concept van de vervaldatum geïntroduceerd. Een nieuwe vereiste functie wordt ingeschakeld op de pagina **Alles** binnen het werkgebied van Functiebeheer. De functie **Beleid voor het bewaren van financiële rapporten** bevat de volgende wijzigingen:
* Nieuwe gegenereerde rapporten krijgen automatisch een vervaldatum van 90 dagen vanaf het moment dat ze worden gegenereerd.
* Alle bestaande rapporten van vóór de installatie van de functie krijgen een vervalperiode van 90 dagen. De datum kan gedurende een korte periode als leeg worden weergegeven totdat de service voor Financial reporting wordt uitgevoerd, er een rapport wordt gegenereerd en de service de update uitvoert op bestaande rapporten met een lege vervaldatum. 
* Gebruikers met de functie **Beveiliging van financiële rapporten onderhouden** hebben toegang tot deze functionaliteit. Elke gebruiker met de functie **Financiële rapporten onderhouden** met de bevoegdheid **Vervaldatum van financiële rapporten onderhouden** kan ook de vervalperiode wijzigen. Momenteel zijn er twee opties beschikbaar: 

    * Een vervalperiode van 90 dagen.
    * Een optie om in te stellen dat het rapport nooit vervalt.

Wanneer een vervaldatum, bijvoorbeeld 90 dagen, is geselecteerd, wordt deze 90 dagen na vandaag toegepast. Dit is een andere werking dan de 90 dagen vanaf de oorspronkelijke datum van genereren die is ingesteld op het moment dat het rapport werd gegenereerd. 

Aanvullende opties worden in toekomstige functies opgenomen. De vervalperiode van 90 dagen is de standaardwaarde en gebruikers met de juiste machtigingen kunnen de standaardwaarde op de lijstpagina **Financiële rapporten** overschrijven.

## <a name="default-reports"></a>Standaardrapporten

Financiële rapportage bevat 22 standaard financiële rapporten. Elk rapport maakt gebruik van de standaard hoofdrekeningcategorieën. U kunt deze rapporten ongewijzigd of als starpunt voor uw financiële rapportagevereisten gebruiken. Naast de normale financiële overzichten, zoals Inkomensoverzicht en Balans, bevatten deze standaardrapporten ook rapporten waarop de verschillende typen financiële rapporten die u kunt maken, worden weergegeven. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Standaardrapport                                                                                         | Beschrijving                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 maanden-samenvoeging inkomensoverzicht in één kolom – Standaard | De winstgevendheid van een organisatie over de afgelopen 12 maanden in één kolom bekijken.                                                                                                                                                                                                                                      |
| 12 maanden trendinkomensoverzicht – Standaard                 | De winstgevendheid van een organisatie voor elk van de afgelopen 12 maanden bekijken. Deze 12 maanden kunnen meer dan één boekjaar beslaan.                                                                                                                                                                                             |
| Werkelijk vs. Budget – Standaard                                | Gedetailleerde saldogegevens voor alle rekeningen voor het oorspronkelijke budget weergeven en het herziene budget vergelijken met werkelijke waarden die een afwijking hebben.                                                                                                                                                                          |
| Auditdetails – Standaard                                  | Gedetailleerde saldogegevens voor alle rekeningen bekijken. Dit rapport toont debet- en creditsaldi in de aangiftevaluta en lokale valuta, samen met aanvullende transactiegegevens, zoals de gebruikers-ID, de gebruiker die de gegevens het laatst heeft gewijzigd, de datum van de laatste wijziging en de journaal-ID. |
| Saldilijst – Standaard                                   | Gedetailleerde saldogegevens voor alle rekeningen bekijken. Dit rapport geeft openings- en eindsaldi, en debet- en creditsaldi voor de huidige periode en tot heden, samen met aanvullende transactiegegevens, zoals het boekstuk.                                                                    |
| Balans – Standaard                                   | De financiële positie van de organisatie voor het jaar weergeven.                                                                                                                                                                                                                                                             |
| Balans en Inkomensoverzicht naast elkaar - Standaard | De financiële positie en de rentabiliteit van de organisatie voor het jaar naast elkaar weergeven.                                                                                                                                                                                                                              |
| Cashflow – Standaard                                       | Inzicht verkrijgen in contact geld dat de organisatie in en uit gaat.                                                                                                                                                                                                                                   |
| Gedetailleerde JE en TB-controle – Standaard                      | Weergaveopeningssaldo en activiteitinformatie voor alle accounts.                                                                                                                                                                                                                                                      |
| [Gedetailleerde proefbalans - Standaard](trial-balance-financial-reports.md)| Saldogegevens weergeven voor alle rekeningen met debet- en creditsaldi, en het nettobedrag van deze saldi, samen met de transactiedatum, het boekstuk en de journaalomschrijving.                                                                                                                                  |
| Onkosten driejarige kwartaaltrend - Standaard             | Inzicht verkrijgen in onkosten over de afgelopen 12 kwartalen gedurende de afgelopen drie jaar.                                                                                                                                                                                                                                   |
| Financiële bijschriften JE en TB-controle – Standaard            | Een overzicht bekijken van de saldi en de activiteit voor de financiële bijschriften voor activa, aansprakelijkheid, het eigen vermogen van de eigenaar, opbrengsten, onkosten, winst of verlies.                                                                                                                                                                           |
| [Inkomensoverzicht – Standaard](income-statement-financial-report.md)| De rentabiliteit van de organisatie voor de huidige periode en het jaar tot heden weergeven.                                                                                                                                                                                                                                   |
| Grootboektransactielijst – Standaard                        | Gedetailleerde saldogegevens voor alle rekeningen bekijken. Dit rapport geeft debet- en creditsaldi, samen met aanvullende transactiegegevens, zoals de transactiedatum, het journaalnummer, het boekstuk, het boekingstype en traceringsnummer.                                                                            |
| Ratio's – Standaard                                          | De solvabiliteit, rentabiliteit en efficiëntiepercentages van de organisatie voor het jaar weergeven.                                                                                                                                                                                                                           |
| Onkosten opvolgende 12 maanden – Standaard                       | Inzicht verkrijgen in onkosten voor elk van de laatste 12 maanden. Deze 12 maanden kunnen meer dan één boekjaar beslaan.                                                                                                                                                                                                       |
| Inkomensoverzicht opvolgende kwartalen- Standaard               | De rentabiliteit van een organisatie op kwartaalbasis voor het afgelopen jaar en het jaar tot heden weergeven.                                                                                                                                                                                                                   |
| Balans naast elkaar - Standaard                      | De financiële positie van de organisatie voor het jaar weergeven. Op dit rapport worden activa en aansprakelijkheid, en het eigen vermogen van de aandeelhouder naast elkaar weergegeven.                                                                                                                                                                                |
| [Overzicht proefbalans – Standaard](trial-balance-financial-reports.md)| De saldogegevens voor alle rekeningen openings- en afsluitingssaldi hebben, en debet- en creditsaldi samen met hun netto verschil.                                                                                                                                                                  |
| [Overzicht proefbalansjaar van jaar tot jaar - Standaard](trial-balance-financial-reports.md)| Saldogegevens weergeven voor alle rekeningen die openings- en eindsaldi hebben, en debet- en creditsaldi samen met hun nettoverschil voor het huidige en afgelopen jaar.                                                                                                                           |
| Wekelijkse verkoop en kortingen - Standaard                     | Inzicht verkrijgen in verkoop en kortingen voor elke week in een maand. Dit rapport bevat een totaal van vier weken.                                                                                                                                                                                                              |
| Beschikbare budgetfondsen- Standaard                         | Een gedetailleerde vergelijking weergeven van het herziene budget, feitelijke uitgaven, budgetreserveringen en budgetfondsen die beschikbaar zijn voor alle rekeningen                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Financiële rapporten openen

Wanneer u het menu **Financiële rapportage** selecteert, wordt de lijst van financiële rapporten voor het bedrijf weergegeven. U kunt een rapport vervolgens openen of wijzigen. Als u een van de standaardrapporten wilt openen, selecteert u de rapportnaam. De eerste keer dat een rapport wordt geopend, wordt het automatisch gegenereerd voor de vorige maand. Als u bijvoorbeeld een rapport voor de eerste keer opent in augustus 2019, wordt het rapport gegenereerd voor 31 juli 2019. Nadat een rapport is geopend, kunt u beginnen met het verkennen ervan door in te zoomen op specifieke gegevensitems en rapportopties te wijzigen.

## <a name="creating-and-modifying-financial-reports"></a>Het maken en wijzigen van het financiële rapporten

Via de financiële verslagenlijst kunt u een nieuw rapport maken of een bestaand rapport wijzigen. Als u de juiste machtigingen hebt, kunt u een nieuwe financieel rapport maken door **Nieuw** te selecteren in het actievenster. Er wordt een rapportontwerpersprogramma gedownload naar uw apparaat. Nadat de rapportontwerper is gestart, kunt u vervolgens het nieuwe rapport maken. Nadat u het nieuwe rapport hebt opgeslagen, verschijnt het in de lijst met financiële rapporten. De lijst bevat alleen rapporten die voor het bedrijf zijn gemaakt en die u in Dynamics 365 Finance gebruikt. 

## <a name="reporting-tree-definitions"></a>Rapportagestructuurdefinities

Een van de onderdelen die wordt gebruikt om financiële rapporten te maken, is een definitie van een rapportagestructuur. Een rapportagestructuurdefinitie helpt bij het definiëren van de structuur en hiërarchie van uw organisatie. Het is een hiërarchische structuur over meerdere dimensies heen die is gebaseerd op de dimensionale relaties in uw financiële gegevens zijn gebaseerd. Het biedt informatie op het niveau van de rapportage-eenheid en op overzichtsniveau voor alle eenheden in de structuur.

U kunt een onbeperkt aantal rapportagestructuren maken om de gegevens van uw organisatie op verschillende manieren weer te geven. Elke rapportagestructuur kan een willekeurige combinatie van afdelingen en overzichtseenheden bevatten, maar een rapportdefinitie kan slechts aan één rapportagestructuur tegelijk worden gekoppeld. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>De versie van Financial reporting bijwerken via slipstreaming

Finance and Operations-apps worden elke maand bijgewerkt. Maar Financial reporting wordt niet per se in dit ritme bijgewerkt. Bovendien hebben klanten meer opties voor het tijdstip waarop ze updates voor Finance and Operations-apps implementeren. Updates van Financial reporting worden automatisch geïnstalleerd. Financial reporting heeft een bepaalde versie die in een klantenomgeving wordt verbruikt wanneer een service-update wordt geïmplementeerd, wanneer downtime wordt gestart of wanneer de omgeving van een klant in de onderhoudsmodus is. Dit proces wordt *slipstreaming* of *true-up* genoemd, omdat alle klantimplementaties worden ingesteld op dezelfde versie van Financial reporting.

U vindt de wijzigingen die in elke versie worden vrijgegeven, in [Nieuwe of gewijzigde functies in Dynamics 365 Finance](../../finance/get-started/whats-new-home-page.md). Platformupdates en bug fixes vindt u in de sectie "Aanvullende resources" onder aan de pagina voor elke release.

De geselecteerde geslipstreamde versie is een beoordeelde en gevalideerde versie van Financial reporting die gereed is voor productie. Deze versie is compatibel met elke eerdere of toekomstige versie van Dynamics 365 Finance. Financial reporting kan bijvoorbeeld de laatste build 10.0.19 hebben, terwijl de klant nog werkt met versie 10.0.16.

> [!NOTE]
> De enige situatie waarin klanten terug kunnen gaan naar een eerdere versie (een downgradescenario), is als Microsoft de uitrol van een true-up stopzet vanwege een probleem. Zodra er een oplossing beschikbaar is, wordt deze automatisch toegepast.

Het slipstreamproces is volledig geautomatiseerd en vereist geen actie van de klant. Drie topologieën verbruiken slipstream, elk op een iets andere manier:

- **On-premises** - On-premises implementaties ondersteunen slipstream en true-up niet.
- **Infrastructuur als een dienst (IaaS)** – De slipstreamlogica wordt toegepast tijdens elke bewerking die probeert om Financial reporting bij te werken. Dit omvat bevat binaire updates of broadcasts die binaire updates bevatten.
- **Self-service** – Elke bewerking waarvoor downtime van Financial reporting vereist is, past de slipstreamlogica toe:

    - Binaire updates of broadcasts die binaire updates bevatten
    - Patching of andere downtime van de infrastructuur
    - Implementatie van AOT-pakketten

## <a name="troubleshooting-issues-opening-report-designer"></a>Problemen met het openen van Report Designer oplossen

Er zijn enkele veelvoorkomende problemen wanneer u Report Designer opent. Deze problemen en de stappen om ze problemen op te lossen zijn als volgt.

Probleem 1: Report Designer start niet wanneer u **Nieuw** of **Bewerken** selecteert.

* Selecteer **Instellingen** in Internet Explorer en selecteer vervolgens **Internetopties**. Selecteer het tabblad **Beveiliging**. Selecteer Vertrouwde sites en vervolgens **Locaties**. Voer bij **Deze website aan de zone toevoegen** "\*\.dynamics.com" in (zonder de aanhalingstekens) en selecteer vervolgens **Toevoegen**. 
* Selecteer **Instellingen** in Internet Explorer en selecteer vervolgens **Internetopties**. Selecteer het tabblad **Beveiliging**. Selecteer Vertrouwde sites. Wijzig de optie in het gebied Beveiligingsniveau voor deze zone in **Normaal-laag**.
* Schakel de pop-upblokkering uit in de browser.
* Voor werkstations moet Microsoft .NET Framework 4.6.2 of hoger worden geïnstalleerd. Deze versie van Microsoft .NET Framework kan worden gedownload en geïnstalleerd via het [Microsoft Downloadcentrum](https://www.microsoft.com/download/details.aspx?id=53345).
* Als u Chrome gebruikt, moet u een ClickOnce-extensie installeren om de Report Designer-client te downloaden. Als u in de incognito modus van Chrome werkt, moet u ervoor zorgen dat de ClickOnce-extensie voor de incognito modus is ingeschakeld. Zie [Systeemvereisten voor cloudimplementaties](../../fin-ops-core/fin-ops/get-started/system-requirements.md) voor meer informatie over de ClickOnce-extensie van Chrome.
* Als u Microsoft Edge met een Chrome-browser gebruikt, hoeft u geen ClickOnce-extensie te installeren voor Edge Chromium. U moet de optie ClickOnce echter inschakelen om de Report Designer-client te downloaden. Als u de incognitomodus gebruikt, moet u ervoor zorgen dat de ClickOnce-extensie voor de incognitomodus is ingeschakeld.

    1. Open een nieuwe browser in Microsoft Edge.
    2. Voer **edge://flags** in en selecteer **Enter**.
    3. Zoek naar de optie **ClickOnce-ondersteuning** of gebruik deze directe koppeling: **edge://flags/#edge-click-once**.
    4. Stel de optie in de vervolgkeuzelijst in op **Ingeschakeld**.
    5. Selecteer **Browser opnieuw starten**.

Probleem 2: De gebruiker beschikt niet over de vereiste machtigingen om Financial reporting te gebruiken. 

* Als u wilt controleren of de gebruiker niet over de juiste machtigingen beschikt, selecteert u **Ja** in de fout "Kan geen verbinding maken met de Financial reporting-server. Selecteer Ja als u wilt doorgaan en een ander serveradres wilt opgeven." Selecteer **Verbinding testen**. Als u niet over de juiste machtigingen beschikt, verschijnt er een bericht met de tekst "Poging tot verbinding is mislukt. De gebruiker beschikt niet over de juiste machtigingen om verbinding te maken met de server. Neem contact op met uw systeembeheerder voor ondersteuning."
* De vereiste bevoegdheden staan hierboven vermeld bij [Beveiligingstoegang verlenen tot Financial Reporting](#granting-security-access-to-financial-reporting). De beveiliging van Financial reporting is gebaseerd op deze bevoegdheden. U hebt geen toegang, tenzij deze bevoegdheden (of een andere beveiligingsrol die deze bevoegdheden bevat) aan u zijn toegewezen. 
* De integratietaak **Provider bedrijfsgebruikers met bedrijf** (die ook verantwoordelijk is voor en bekend staat als gebruikersintegratie) wordt met een interval van 5 minuten uitgevoerd. Het kan 10 minuten duren voordat wijzigingen in de machtigingen van kracht worden in Financial reporting. 

    Als een andere gebruiker Report Designer kan openen, selecteert u **Extra** en vervolgens **Integratiestatus**. Controleer of de integratietoewijzing "Provider bedrijfsgebruikers met bedrijf" is uitgevoerd omdat aan u een machtiging is toegewezen voor het gebruik van Financial reporting. 

* Mogelijk is er een andere fout opgetreden waardoor **Gebruikersintegratie van Dynamics-gebruiker met Financial reporting** niet kan worden voltooid. Het is ook mogelijk dat een datamartreset is gestart en nog niet is voltooid, of dat er een andere systeemfout is opgetreden. Probeer het proces later opnieuw uit te voeren. Neem contact op met de systeembeheerder als het probleem zich blijft voordoen.

Probleem 3: u kunt doorgaan na de aanmeldingspagina voor **ClickOnce Report Designer**, maar de aanmelding in Report Designer kan niet worden voltooid. 

* De tijd die op uw lokale computer is ingesteld wanneer u uw aanmeldingsreferenties invoert, moet binnen vijf minuten zijn na de tijd op de Financial reporting-server. Als er een verschil is van meer dan vijf minuten, is aanmelden niet toegestaan. 
* Als de tijd op uw computer verschilt van de tijd op de server waar Financial reporting op draait, raden we u aan de Windows-optie in te schakelen om de tijd van uw computer automatisch in te stellen. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Problemen met Report designer oplossen met de Logboeken

U kunt de Logboeken gebruiken om een aantal van de problemen te analyseren die zich voordoen bij het gebruik van Financial reporting. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Wat gebeurt er als er verbindingsproblemen zijn met Financial reporting? 

Hieronder staan enkele stappen die u kunt ondernemen om uw gesprek met Microsoft Ondersteuning effectiever te maken en sneller een oplossing te vinden. 
 
De volgende stappen doorlopen het proces voor het in- of uitschakelen van berichten in de Logboeken voor Financial reporting. In de logboeken die met de functie Logboeken worden gegenereerd, kunnen medewerkers van de afdeling Ondersteuning de bron van het verbindingsprobleem snel vinden. Dien kopieën van deze logboeken samen met het ticket in wanneer u contact opneemt met de afdeling Ondersteuning.


1. Kopieer het bestand RegisterETW.zip naar het client-werkstation (bij voorkeur het bureaublad) en haal [RegisterETW.zip](https://dev.azure.com/msdyneng/e6f12261-a46a-4af1-ac0c-e22bc2c5a478/_apis/git/repositories/ff923027-67f0-43fb-b63c-6d6b6423840f/Items?path=%2F.attachments%2FRegisterETW-c1a35291-6aa6-4462-a2bc-4ba117fd5f8e.zip&download=false&resolveLfs=true&%24format=octetStream&api-version=5.0-preview.1&sanitize=true&versionDescriptor.version=wikiMaster) op.
2. Zorg ervoor dat Windows Logboeken is afgesloten.
3. Open een Opdrachtprompt voor Administrator PowerShell en ga naar de map waar RegisterETW.ps1 zich bevindt.
4. Voer de volgende opdracht uit: .\RegisterETW.ps1

    Een geslaagde uitvoer in PowerShell wordt geverifieerd met het bericht: **Competed RegisterETW-script**.

    Open Logboeken opnieuw en en u ziet deze logboeken nu onder **Microsoft > Dynamics**:

    * MR-Client
    * MR-DVT
    * MR-Integration
    * MR-Logger
    * MR-Reporting
    * MR_SchedulerTasks
    * MR-Sql
    * MR-TraceManager

5. Reproduceer het probleem in de Report Designer.
6. Exporteer de gebeurtenissen in MR-Logger met behulp van de Logboeken.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Problemen met de verbinding naar Financial reporting oplossen

Probleem: u ontvangt de foutmelding "Kan geen verbinding maken met de server waar Financial reporting op draait".

* Bepaal of het probleem optreedt in de internetbrowsers Chrome en Edge.
* Als het probleem zich slechts in één browser voordoet, kan dit Het ClickOnce-probleem zijn. 
* Wanneer u het foutbericht voor de verbinding ziet, selecteer dan **Testen** om de verbinding te testen om te zien welk bericht wordt weergegeven. 
* Het probleem kan het resultaat zijn van een andere gebruiker die geen toegang heeft tot Financial reporting. Als een gebruiker geen toegang heeft, ontvangt hij of zij een bericht waarin wordt aangegeven dat hij of zij niet over de juiste bevoegdheden beschikt.
* Als het probleem zich voordoet op meerdere browsers, moet u ervoor zorgen dat de klok op het werkstation is ingesteld op Automatisch.
* Werk met een gebruiker die beschikt over de bevoegdheid beveiligingsbeheerder in Dynamics 365 Finance en beheerdersrechten voor het netwerkdomein om u aan te melden op uw werkstation om te zien of deze verbinding kan maken. Als deze verbinding kan maken, is het probleem mogelijk gerelateerd aan netwerkbevoegdheden.
* Schakel de firewall tijdelijk uit op het werkstation. Als u vervolgens verbinding kunt maken met Report Designer is het een probleem met uw firewall. Werk samen met de IT-afdeling van uw organisatie om het probleem op te lossen.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Financiële rapporten weergeven](view-financial-reports.md)
- [Rapportagestructuurdefinities in financiële rapporten](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
