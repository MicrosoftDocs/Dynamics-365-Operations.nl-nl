---
title: Verwijderde of afgeschafte functies in eerdere releases
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die gepland zijn om te verwijderen uit Dynamics 365 for Finance and Operations en eerdere versies van dat product.
author: sericks007
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ce6b3fb5217ad5d5228841a91d0b0406c305969
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679951"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>Verwijderde of afgeschafte functies in eerdere releases

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> Dit onderwerp wordt niet meer bijgewerkt. Als u een actuele lijst met functies wilt weergeven die zijn verwijderd of afgeschaft in Finance and Operations-apps, zoekt u naar de inhoud **Verwijderde of afgeschafte functies** die betrekking heeft op de app die u gebruikt.

In dit onderwerp worden de functies beschreven die zijn verwijderd of afgeschaft in Dynamics 365 for Finance and Operations en eerdere versies van dat product.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="finance-1007-with-platform-update-31"></a>Finance 10.0.7 met Platformupdate 31

### <a name="chinese-voucher-types-without-account-groups-selection"></a>Chinese boekstuktypen zonder selectie van rekeninggroepen
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Gewijzigd in de functie met selectie van rekeninggroepen. |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Aanvraag |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: op 1 december 2020 worden Chinese boekingstypen niet meer ondersteund zonder dat rekeninggroepen zijn geselecteerd. Meer informatie over het nieuwe functieontwerp is te vinden in Nieuwe functies in 10.0.7 |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>Finance and Operations 10.0.6 met platformupdate 30


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Windows schaft het gebruik van SHA1 af, zoals is gedocumenteerd in [Afdwinging van SHA1-certificaten in Windows](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Aanvraag |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 april 2020 moeten ontwikkelaars de platform-API's gebruiken uit de klasse **HasFunction**. |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(string message)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Windows schaft het gebruik van SHA1 af, zoals is gedocumenteerd in [Afdwinging van SHA1-certificaten in Windows](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Platform |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf 1 april 2020 moeten ontwikkelaars de platform-API's gebruiken uit de klasse **HasFunction**. |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De methode **setUtcString ()** wordt buiten gebruik gesteld, omdat er een betere vervangingsmethode beschikbaar is. |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Platform |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: op 1 oktober 2020 wordt de methode **setUtcString()** niet meer ondersteund. Ontwikkelaars moeten in plaats daarvan de methode **setUtcDateTime()** gebruiken. |

### <a name="blacklist-report-it--feature-reference-it-00001"></a>Zwarte-lijstrapport (IT) – functieverwijzing IT-00001

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Niet wettelijk vereist. |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Italiaanse lokalisatie |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: op 1 oktober 2020 wordt het **Zwarte-lijstrapport (IT) – functieverwijzing IT-00001** niet meer ondersteund. |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>Binnenlandse belastingaangifte – functieverwijzing IT-00003

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Niet wettelijk vereist. |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Italiaanse lokalisatie |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: op 1 oktober 2020 wordt het **Binnenlandse belastingaangifte – functieverwijzing IT-00003** niet meer ondersteund. |


## <a name="finance-and-operations-1005-with-platform-update-29"></a>Finance and Operations 10.0.5 met platformupdate 29

### <a name="us-payroll-tax-updates"></a>Updates van Amerikaanse payroll-belasting

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | We gaan belastingupdates voor de Amerikaanse payroll-functionaliteit afschaffen omdat deze te weinig wordt gebruikt en omdat er nu door strategische integraties verbeterde functionaliteit wordt aangeboden.  |
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Salaris |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: op 31 juli 2024 zijn we van plan geen belastingupdates meer te verstrekken aan Amerikaanse Payroll-klanten. De functionaliteit blijft in het product bestaan, maar de functionaliteit zal niet meer up-to-date blijven en eventuele productdefecten worden per geval geëvalueerd. |

>[!NOTE]
> Dit is een wijziging van de oorspronkelijke beëindigingsdatum van 1 oktober 2021. Zie [Belastingupdates voor Amerikaanse Payroll-functie in Microsoft Dynamics 365 for Finance and Operations worden afgeschaft](https://aka.ms/financepayrollfaq) voor meer informatie.


### <a name="data-management-staging-clean-up"></a>Fasering gegevensbeheer opschonen
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Voldoet niet aan de kernvereisten die nodig zijn voor het plannen van periodieke opschoning. |
| **Vervangen door een andere functie?**   | Ja, de functie Taakhistorie opschonen wordt toegevoegd om holistisch aan de scenario's te voldoen. |
| **Betrokken productgebieden**         | Gegevensbeheer |
| **Implementatieoptie**              | Alle  |
| **Status**                         | Afgeschaft: de verwijdering van de functionaliteit staat gepland voor december 2020. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>Finance and Operations 10.0.4 met platformupdate 28

### <a name="france-fec-accounting-data-export-in-xml"></a>Frankrijk: FEC-boekhoudingsgegevens exporteren in XML

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door TXT-indeling, **Frans FEC-auditbestand** is beschikbaar via **Grootboek** \> **Periodieke taken** \> **Gegevensexport**.
| **Vervangen door een andere functie?**   | Ja |
| **Betrokken productgebieden**         | Grootboek |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft. De verwijdering van de functionaliteit staat gepland voor juli 2020. |


### <a name="legacy-navigation-bar"></a>Verouderde navigatiebalk

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Koptekst uitgelijnd met andere Dynamics- en Office-producten. Zie [Bijgewerkte navigatiebalk die is uitgelijnd met de Office-koptekst](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar)voor meer informatie.
| **Vervangen door een andere functie?**   | Vanaf platformupdate 24 is een opnieuw vormgegeven navigatiebalk met zoekfunctie beschikbaar. |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf april 2020 is de oude navigatiebalk niet meer beschikbaar. Tot dat kunnen klanten nog de oude navigatiebalk herstellen via de pagina **Prestatieopties van client**. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>Finance and Operations 10.0.2 met platformupdate 26


### <a name="legacy-default-action-behavior"></a>Oud standaardgedrag voor acties

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het oude gedrag van standaardacties in rasters resulteert in een onverwachte kolom waarbij de standaardactiekoppeling na rasterkolommen opnieuw zijn geordend via aanpassing. Met de nieuwe standaardplakactiefunctie wordt dit gecorrigeerd. Zie voor meer informatie [Standaardplakacties in rasters](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Vervangen door een andere functie?**   | Vanaf platformupdate 21 is een functie voor 'standaardplakacties' geïntroduceerd. Deze functie kan worden ingeschakeld op de pagina **Prestatieopties van client**. |
| **Betrokken productgebieden**         | Rasters in de webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: in april 2020 vormen standaardplakacties het standaardgedrag zonder een mechanisme om terug te keren naar het oude gedrag. |

### <a name="legacy-is-one-of-filtering-experience"></a>Oud is de filterervaring "is één van"

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Op de filterervaring "is één van" is een nieuw ontwerp in platformupdate 22 toegepast, met het plan dat dit ontwerp uiteindelijk de enige filterervaring "is één van" zou worden. |
| **Vervangen door een andere functie?**   | Vanaf platformupdate 22 is een verbeterde filterervaring "is één van" beschikbaar geworden op de pagina **Prestatieopties van client**. Zie [Geoptimaliseerde filterervaring "is één van"](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering) voor meer informatie. |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf april 2020 wordt de verbeterde filterervaring "is één van" het standaardgedrag zonder een mechanisme om terug te keren naar het oude gedrag. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parameter om verkooporders met meerdere financieringsbronnen van projectcontracten in te schakelen
Ondersteuning voor het maken van projectgebaseerde verkooporders waarbij het projectcontract meerdere financieringsbronnen heeft, is ingeschakeld met de **Parameters voor projectbeheer**-instelling **Verkooporders voor projecten met meerdere financieringsbronnen toestaan**. Deze parameter is standaard niet ingeschakeld. 

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De functionaliteit wordt altijd ingeschakeld nadat de parameter is verwijderd. |
| **Vervangen door een andere functie?**   | Nr. De functionaliteit om projectgebaseerde verkooporders met meerdere financieringsbronnen te ondersteunen, wordt altijd ingeschakeld.   |
| **Betrokken productgebieden**         |De parameter **Verkooporders voor projecten met meerdere financieringsbronnen** wordt verwijderd. De volgende methoden worden gewijzigd wanneer de parameter wordt verwijderd: de methode **ctrlSalesOrderTable** in de klasse **ProjStatusType**, de methode **validate** voor het veld **ProjId** en de methode **run** in het formulier **SalescreateOrder**. De volgende methoden worden afgeschaft wanneer de parameter wordt verwijderd: **IsSalesOrderAllowedForMultipleFundingSources** in tabelbestand **ProjTable**, de methode **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** in tabelbestand **ProjTable**, het gegevensveld **AllowSalesOrdersForMultipleFundingSources** in het formulier **ProjParameters** en **ProjParameterEntity**-bestanden, de persoonlijke methode **IsAssociatedToMultipleFundingSourcesContract** in het tabelbestand **ProjTable**. |
| **Implementatieoptie**              | Alle  |
| **Status**                         | Afschaffinf is gepland voor rijving is voor de releasewave van april 2020. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Oude workflowrapporten voor status van tracering en exemplaar

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De oude workflowrapporten voor tracerings- en exemplaarstatus worden afgeschaft omdat er niet meer naar wordt verwezen via de navigatie. De rapportnamen zijn WorkflowWorkflowInstanceByStatusReport en WorkflowWorkflowTrackingReport. |
| **Vervangen door een andere functie?**   | Het workflowhistorieformulier kan in plaats daarvan worden gebruikt. |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: de verwijdering van de functionaliteit staat gepland voor april 2020. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>Finance and Operations 10.0.1 met platformupdate 25

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Afgeschafte API's en potentiële ingrijpende wijzigingen


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Afleiden van interne klassen is afgeschaft

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vóór platformupdate 25 was het mogelijk om een klasse of tabel te maken die was afgeleid van een interne klasse/tabel die was gedefinieerd in een ander pakket of een andere module. Dit is geen veilige codering. Vanaf platformupdate 25 geeft de compiler een waarschuwing weer. |
| **Vervangen door een andere functie?**   | De compilerwaarschuwing wordt vervangen door een fout in platformupdate 26. Deze wijziging is achterwaarts compatibel tijdens runtime, wat betekent dat als u platformupdate 25 of nieuwer uitvoert, deze wijziging kan worden geïmplementeerd in een willekeurige sandbox- of productieomgeving zonder dat u aangepaste code hoeft te wijzigen. Deze wijziging is alleen van invloed op ontwikkel- en compilatietijd.|
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: de waarschuwing wordt een compilatiefout in platformupdate 26. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Overschrijven van interne methoden is afgeschaft

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vóór platformupdate 25 was het mogelijk om een interne methode te overschrijven in een afgeleide klasse die was gedefinieerd in een ander pakket of een andere module. Dit is geen veilige codering. Vanaf platformupdate 25 geeft de compiler een waarschuwing weer. |
| **Vervangen door een andere functie?**   | Deze compilerwaarschuwing wordt vervangen door een compilerfout in platformupdate 26. Deze wijziging is achterwaarts compatibel tijdens runtime, wat betekent dat als u platformupdate 25 of nieuwer uitvoert, deze wijziging kan worden geïmplementeerd in een willekeurige sandbox- of productieomgeving zonder dat u aangepaste code hoeft te wijzigen. Deze wijziging is alleen van invloed op ontwikkel- en compilatietijd. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: de waarschuwing wordt een compilatiefout in platformupdate 26. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>Finance and Operations 10.0.0 met platformupdate 24

### <a name="renaming-released-products"></a>Naam wijzigen van vrijgegeven producten 
| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Wanneer u de functie **Naam van primaire sleutel wijzigen** gebruikt om de Itemid van een vrijgegeven product te wijzigen, worden alleen directe verwijzingen naar externe sleutels bijgewerkt. Eventuele andere verwijzingen naar het vrijgegeven product, zoals vanuit productie orders, behouden de oude ItemId. Hierdoor kunnen er inconsistente gegevens zijn die uiteindelijk de bedrijfsprocessen zullen blokkeren. |
| **Vervangen door een andere functie?**   | Nr. |
| **Betrokken productgebieden**         | Productgegevensbeheer |
| **Implementatieoptie**              | Alle  |
| **Status**                         | Verwijderd sinds Finance and Operations 10.0.0 met Platform update 24.|


## <a name="finance-and-operations-813-with-platform-update-23"></a>Finance and Operations 8.1.3 met platformupdate 23

### <a name="sql-server-reporting-services-reportviewer-control"></a>SQL Server Reporting Services ReportViewer-besturingselement
Klanten kunnen de actie **Exporteren** gebruiken die wordt verschaft door het SQL Server Reporting Services (SSRS) ReportViewer-besturingselement om documenten te downloaden die door Finance and Operations-toepassingen zijn gemaakt. Deze op HTML gebaseerde presentatie van het rapport biedt gebruikers een voorbeeld van het document zonder pagina´s.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dit op HTML gebaseerde voorbeeld zonder pagina´s levert **niet** de kwaliteit van de fysieke documenten die uiteindelijk door Finance and Operations worden geleverd. Door PDF volledig als de standaardindeling voor bedrijfsdocumenten te gebruiken, kunnen gebruikers profiteren van een moderne weergave-ervaring met betere prestaties bij het produceren van toepassingsrapporten. |
| **Vervangen door een andere functie?**   | In de toekomst zullen PDF-documenten de standaardindeling voor rapporten worden die door Finance and Operations worden weergegeven.   |
| **Betrokken productgebieden**         | Deze wijziging is **niet** van invloed op klantscenario's waarin rapporten elektronisch worden verspreid of rechtstreeks naar printers worden verzonden.    |
| **Implementatieoptie**              | Alle  |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. De functionaliteit om van toepassingsrapporten automatisch een voorbeeld te bekijken met een ingesloten PDF-viewer is gepland voor de platformupdate van mei 2019. |

### <a name="client-kpi-controls"></a>Client-KPI-besturingselementen
Ingesloten prestatie-indicatoren (KPI's) kunnen worden gemodelleerd in Visual Studio door een ontwikkelaar en verder worden aangepast door de eindgebruiker.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De native client-besturingselementen waarmee KPI's worden gedefinieerd, hebben een lage klanttoepassing en zijn voor het toevoegen van herleidbare metrische gegevens afhankelijk van een ontwikkelaar. |
| **Vervangen door een andere functie?**   | PowerBI.com-service levert hoogwaardige programma´s voor het definiëren en beheren van KPI's op basis van gegevens uit externe bronnen.  In een toekomstige versie willen we mogelijk maken dat u oplossingen kunt insluiten die worden gehost op PowerBI.com in toepassingswerkgebieden.   |
| **Betrokken productgebieden**         | Met deze update kunnen ontwikkelaars geen nieuwe KPI-besturingselementen in Visual Studio-ontwerper introduceren.    |
| **Implementatieoptie**              | Alle  |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Afgeschafte API's en toekomstige ingrijpende wijzigingen

#### <a name="field-groups-containing-invalid-field-references"></a>Veldgroepen die ongeldige veldverwijzingen bevatten

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het is mogelijk dat tabelmetagegevensdefinities veldgroepen bevatten met verwijzingen naar ongeldige veldverwijzingen. Bij implementatie kan dit probleem runtime-fouten veroorzaken in de financiële rapportage en SQL Server Reporting Services (SSRS). Dit probleem wordt momenteel geclassificeerd als een *compilerwaarschuwing* in plaats van een *fout*, wat betekent dat het implementeerbare pakket kan worden gemaakt en geïmplementeerd zonder dat het probleem wordt opgelost. Ga als volgt te werk om dit probleem op te lossen:<br><br>1. Verwijder de ongeldige veldverwijzing uit de groepsdefinitie van het tabelveld.<br><br>2. Compileer opnieuw.<br><br>3. Zorg ervoor dat eventuele waarschuwingen of fouten worden opgelost. |
| **Vervangen door een andere functie?**   | Deze waarschuwing wordt in de toekomst vervangen door een compilatiefout. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: De waarschuwing is een compilatiefout in platform updates voor versie 10.0.11 van Finance and Operations-apps. |

#### <a name="complete-list"></a>Volledige lijst
Raadpleeg voor toegang tot de volledige lijst met API's [Afschaffing van methoden en metagegevenselementen](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>Finance and Operations 8.1 met platformupdate 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Batchoverboekingsregels voor journaalregels in subadministratie
De modus voor synchrone overdracht wordt afgeschaft in de grootboekparameters.  Deze modus wordt vervangen door asynchrone overdrachten en geplande batches, die al bestaan als overdrachtopties. Zie voor meer informatie het blog [Grootboekparameters: regels voor batchoverboeking](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | We verwijderen de synchrone optie vanwege de invloed op de systeemprestaties. |
| **Vervangen door een andere functie?**   | Asynchroon en geplande batch zijn opties die kunnen worden gebruikt in plaats van synchroon.   |
| **Betrokken productgebieden**         | Grootboek, Leveranciers, Klanten, Inkoop, Onkosten    |
| **Implementatieoptie**              | Alle  |
| **Status**                         | Afgeschaft: de verwijdering van de functionaliteit staat gepland voor versie 10.0.|

### <a name="electronic-reporting-for-russia"></a>Elektronische rapportage voor Rusland
Functie voor het configureren van bestandsindelingen .txt en .xml van aangiften. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door Elektronische rapportage. |
| **Vervangen door een andere functie?**   | Ja. |
| **Betrokken productgebieden**         | Grootboek |
| **Implementatieoptie**              | Alle |
| **Status**                         | Verwijderd sinds Finance and Operations 8.1 met Platform update 20. |

### <a name="financial-reports-generator-for-russia"></a>Aanmaker van financiële rapporten voor Rusland
Een hulpmiddel om gegevensverzameling in te stellen voor boekhouding en belastingaangiften, en gegevens te exporteren naar XLS- en DOC-rapportsjablonen. Functionele onderdelen: gegevens exporteren naar XLS- en DOC-rapportsjablonen, query's, vaste vereisten worden verwijderd. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Verwijderde onderdelen worden vervangen door Elektronische rapportage. |
| **Vervangen door een andere functie?**   | Ja. De gebruikersinterface voor de instelling van financiële rapportage moet worden gebruikt voor het instellen van regels voor het verzamelen van gegevens door grootboekrekeningen of belastingregisters. Exportgegevens in verschillende bestandstypen, vaste vereisten en queryregels voor het verzamelen van gegevens moeten worden geconfigureerd in Elektronische rapportage. |
| **Betrokken productgebieden**         | Grootboek. |
| **Implementatieoptie**              | Alle |
| **Status**                         | Verwijderd sinds Finance and Operations 8.1 met Platform update 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integratie met externe providers voor het verzenden via communicatiekanalen van elektronische rapportage voor Rusland
Functie voor het exporteren van gegenereerde elektronische aangiftebestanden naar de map voor doorsturen naar officiële aanbieders van elektronische rapportage en het importeren van de status.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door configureerbare functie voor elektronische berichten. |
| **Vervangen door een andere functie?**   | Ja.  |
| **Betrokken productgebieden**         | Grootboek, Belasting |
| **Implementatieoptie**              | Alle |
| **Status**                         | Verwijderd sinds Finance and Operations 8.1 met Platform update 20. |


### <a name="profit-tax-register-wizard"></a>Wizard voor winstbelastingregister
Functie voor het maken van sjablonen voor nieuwe winstbelastingregisters. Met deze functie maakt u X++-objecten voor nieuwe registers, die vervolgens als sjablonen worden gemaakt met de betreffende berekeningslogica.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Functie is niet compatibel met het Finance and Operations uitbreidbare model. |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Belasting |
| **Implementatieoptie**              | Alle |
| **Status**                         | Verwijderd sinds Finance and Operations 8.1 met Platform update 20. |


## <a name="finance-and-operations-80-with-platform-update-15"></a>Finance and Operations 8.0 met platformupdate 15
Er zijn geen onderdelen verwijderd of vervangen in deze versie. Platformupdate 15 is cumulatief en bevat nieuwe of gewijzigde functies van platformupdate 13, platformupdate 14 en platformupdate 15.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Finance and Operations, Enterprise edition 7.3 met Platform update 12

### <a name="personalized-product-recommendations"></a>Gepersonaliseerde productaanbevelingen 
Vanaf 15 februari 2018 kunnen detailhandelaren geen persoonlijke productaanbevelingen meer weergeven op een POS-apparaat (Point Of Sale). Zie voor meer informatie [Overzicht met productaanbevelingen](../../../commerce/product-recommendations.md).  

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | We verwijderen de huidige versie van de productaanbevelingsservice aangezien we deze opnieuw willen ontwerpen met een beter algoritme en nieuwe mogelijkheden voor detailhandelaren.  |
| **Vervangen door een andere functie?**   | Nr. Na het voorjaar van 2018 komen we echter met een nieuwe aanbevelingsservice.   |
| **Betrokken productgebieden**         | Persoonlijke productaanbevelingen in POS.                                                    |
| **Implementatieoptie**              | Alles                                                                                      |
| **Status**                         |Verwijderd sinds 15 februari 2018. Dit geldt voor klanten met Dynamics 365 for Operations 1611 en hoger.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Uitbreiding van de lijst met functies voor elektronische rapportage (ER)
De mogelijkheid om aangepaste functies te introduceren voor gebruik in de ER-opbouwfunctie (zie voor meer informatie [De lijst met functies voor elektronische rapportage (ER) uitbreiden](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) wordt niet meer ondersteund. Als gevolg van wijzigingen in de ER-API's is de API voor het aanroepen van ingebouwde functies vanuit de ER-opbouwfunctie nu een interne API die niet meer kan worden uitgebreid.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Initiatief voor codeverzegeling  |
| **Vervangen door een andere functie?**   | Geen. Wanneer u een nieuwe ingebouwde functie nodig hebt, moet u een nieuwe uitbreidingsaanvraag richten aan het team van het ER-framework.<br><br>Als tijdelijke oplossing terwijl de aangevraagde functie wordt ontwikkeld door het ER-team kan de vereiste logica worden geprogrammeerd als een methode van een aangepaste toepassingsklasse. Deze methode kan in een ER-expressie worden geopend als een eigenschap van de toegevoegde ER-gegevensbron van het type **Toepassing\Klasse** dat naar die aangepaste toepassingsklasse verwijst.  |
| **Betrokken productgebieden**         | Framework voor elektronische rapportage                                                      |
| **Implementatieoptie**              | Alles                                                                                      |
| **Status**                         | Verwijderd sinds Finance and Operations, Enterprise edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>De rapporten Voorraad op naar ouderdom gerangschikte artikelengroep en Voorraad op naar ouderdom gerangschikte voorraaddimensie

Deze twee rapporten worden niet meer ondersteund in Finance and Operations. In plaats daarvan kan het rapport **Naar ouderdom rangschikken van voorraad** worden gebruikt voor het verbeteren van de gebruikerservaring.

| &nbsp;  | &nbsp; |
|--------------|-----------------------|
| **Reden voor afschrijving**       | Dubbele functionaliteit.  |
| **Vervangen door een andere functie?** | Ja. De twee rapporten zijn vervangen door het rapport **Naar ouderdom rangschikken van voorraad**.     |
| **Betrokken productgebieden**       | Voorraadbeheer, Kostenbeheer        |
| **Implementatieoptie**        | Alles|
| **Status**                       | Afgeschaft: de menu-items voor de twee rapporten zijn verwijderd in versie 7.3. De code voor de rapporten blijft echter in het product. Het plan is om de code in een toekomstige versie te verwijderen. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI-inhoudspakketten beschikbaar op AppSource
De inhoudspakketten **Kostenbeheer**, **Financiële prestaties** en **Prestaties detailhandelafzetkanaal**, die beschikbaar zijn op de site [Microsoft AppSource](https://appsource.microsoft.com), zijn afgeschaft als gevolg van productupdates in Microsoft Power BI. Systeembeheerformulieren voor het implementeren van deze inhoudpakketten op PowerBI.com worden ook afgeschaft in Finance and Operations.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Productupdates in Microsoft Power BI. |
| **Vervangen door een andere functie?**   | De inhoudspakketten **Kostenbeheer**, **Financiële prestaties** en **Prestaties detailhandelafzetkanaal**, beschikbaar op de site [AppSource](https://appsource.microsoft.com), worden vervangen door analytische toepassingen die oplossingsintegratie op databaseniveau mogelijk maken. Zie [Ingesloten Power BI in werkruimten](../../dev-itpro/analytics/embed-power-bi-workspaces.md) voor meer informatie over analytische toepassingen.    |
| **Betrokken productgebieden**         | Kostenbeheer, Finance en Retail                                                                                               |
| **Implementatieoptie**              | Alleen cloud (integratie met PowerBI.com wordt niet ondersteund in on-premises implementaties.)                                                                                                            |
| **Status**                         | Afgeschaft: de verwijdering van de functionaliteit staat gepland voor het tweede kwartaal van 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standaardgebruikersinterface in werkgebied Gegevensbeheer

De standaardgebruikersinterface in Gegevensbeheer is de verouderde gebruikersinterface, de standaardgebruikersinterface voor gebruikers wanneer ze het werkgebied Gegevensbeheer bezoeken.

| &nbsp;  | &nbsp; |
|------------------|-------------------------|
| **Reden voor afschaffing/verwijdering** | We investeren in het bieden van nieuwe gebruikerservaringen in de nieuwe gebruikersinterface.             |
| **Vervangen door een andere functie?**   | De nieuwe gebruikersinterface *Verbeterde weergaven* vervangt de oude gebruikersinterface.            |
| **Betrokken productgebieden**         | Werkgebied Gegevensbeheer                                                     |
| **Implementatieoptie**              | Alles                                                                           |
| **Status**                         | Afgeschaft: de verwijdering van de functionaliteit staat gepland voor het eerste kwartaal van 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Accijns, Btw, Btw voor India

Deze belastingen zijn opgenomen in Indiase GST.

|  &nbsp;                                           |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Reden voor verwijdering of afschaffing**       | Deze belastingen zijn opgenomen in Indiase GST.                          |
| **Vervangen door een andere functie?**            | Indiase GST                                                              |
| **Betrokken productgebieden**                  | Btw                                                                     |
| **Implementatieoptie**                       | Alle modules                                                   |
| **Status**                                  | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |    

### <a name="file-validation-utility-fvu-for-india"></a>Hulpprogramma voor bestandsvalidatie voor India

|              &nbsp;                               |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Reden voor verwijdering of afschaffing**       | Gebrek aan klantgebruik                                                  |
| **Vervangen door een andere functie?**            | Nee                                                                      |
| **Betrokken productgebieden**                  | Indiase bronbelasting                                                  |
| **Implementatieoptie**                       | Alle modules                                                                    |
| **Status**                                  | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS-certificaat voor India

Gebruikers kunnen dit certificaat downloaden vanuit de overheidsportal.

|             &nbsp;                                |    &nbsp;                                                                     |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Reden voor verwijdering of afschaffing**       | Gebrek aan klantgebruik                                                  |
| **Vervangen door een andere functie?**            | Nee                                                                      |
| **Betrokken productgebieden**                  | Indiase bronbelasting                                                  |
| **Implementatieoptie**                       | Alle modules                                                                   |
| **Status**                                  | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>EXIM-beloningsregeling (exporteren/importeren) voor India


|              &nbsp;                               |        &nbsp;                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Reden voor verwijdering of afschaffing**       | Gebrek aan klantgebruik                                                  |
| **Vervangen door een andere functie?**            | Nee                                                                      |
| **Betrokken productgebieden**                  | Importeren en exporteren                                                       |
| **Implementatieoptie**                       | Alle modules                                                                    |
| **Status**                                  | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Gepersonaliseerde productaanbevelingen 
Vanaf 15 februari 2018 kunnen detailhandelaren geen persoonlijke productaanbevelingen meer weergeven op een POS-apparaat (Point Of Sale). Zie voor meer informatie [Overzicht met productaanbevelingen](../../../commerce/product-recommendations.md).  

|  &nbsp; |  &nbsp;|
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | We verwijderen de huidige versie van de productaanbevelingsservice aangezien we deze opnieuw willen ontwerpen met een beter algoritme en nieuwe mogelijkheden voor detailhandelaren.  |
| **Vervangen door een andere functie?**   | Nr. Na het voorjaar van 2018 komen we echter met een nieuwe aanbevelingsservice.   |
| **Betrokken productgebieden**         | Persoonlijke productaanbevelingen in POS.                                                    |
| **Implementatieoptie**              | Alles                                                                                      |
| **Status**                         |Verwijderd sinds 15 februari 2018. Dit geldt voor klanten met Dynamics 365 for Retail 7.2 en hoger. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Finance and Operations, Enterprise edition juli 2017 met Platform update 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Omrekening van valuta voor boekhouding en rapportage van valuta's

Omrekening van valuta voor boekhouding en rapportage van valuta's werd ingevoerd toen de euro werd ingevoerd.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Beperkt gebruik en toevoeging van de functionaliteit Rechtspersoon kopiëren als een vervanging.      |
| **Vervangen door een andere functie?**   | Nee, maar de functies Rechtspersoon kopiëren en Configuraties zijn toegevoegd om het gemakkelijker te maken over te gaan naar een bedrijf dat veranderende kernvereisten heeft. |
| **Betrokken productgebieden**         | Financieel beheer     |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.   |


### <a name="warehouse-mobile-devices-portal"></a>Portal voor mobiele apparaten voor magazijnbeheer

Portal voor mobiele apparaten voor magazijnbeheer (WMDP) is een zelfstandig onderdeel dat is bedoeld voor on-premises zelfimplementatie. Dit onderdeel wordt niet meer ondersteund in Finance and Operations. De functionaliteit van WMDP is vervangen door een native app waarmee de gebruikerservaring wordt verbeterd.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dubbele functionaliteit.       |
| **Vervangen door een andere functie?**   | Ja. Deze functie is vervangen door Finance and Operations - Magazijnbeheer. Zie [Overzicht van het installeren en configureren van de Warehousing-app](../../../supply-chain/warehousing/install-configure-warehousing-app.md) voor meer informatie over instellingen en vereisten. |
| **Betrokken productgebieden**         | Magazijnbeheer, Transportbeheer     |
| **Implementatieoptie**              | Portal voor mobiele apparaten voor magazijnbeheer (WMDP) is een zelfstandig onderdeel dat is bedoeld voor on-premises zelfimplementatie.               |
| **Status**                         | Afgeschaft: doeltijd voor verwijdering van de functionaliteit is kwartaal 4 van 2019.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Afstemmingsregel voor geavanceerde bankafstemming voor handmatig afstemmen

Er is een afstemmingsregel gebruikt voor het selecteren en markeren van een bankdocument bij het handmatig afstemmen van documenten in het werkblad voor afstemming.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Beperkt gebruik.                                                                         |
| **Vervangen door een andere functie?**   | Nr. Kolomfilteropties moeten worden gebruikt om documenten te vinden voor afstemming. |
| **Betrokken productgebieden**         | Contanten en bankbeheer                                                               |
| **Implementatieoptie**              | Alle                                                                                    |
| **Status**                         | Verwijderd sinds juli 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 met platformupdate 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-betalingsindelingen voor Spanje

CSB-betalingsindelingen (Consejo Superior Bancario) werden gebruikt om remisebestanden naar de bank te verzenden voor klant- en leveranciersbetalingen. De inhoud van deze indelingen werd bepaald door de Asociación Española de Banca (AEB). Dit dekt Cuaderno 19, 32, 58, 34.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                                  |
| **Vervangen door een andere functie?**   | Ja, ISO20022-indelingen voor kredietoverdracht en automatische overschrijvingen voor Spanje |
| **Betrokken productgebieden**         | Leveranciers, Klanten                                    |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Overboeking van bankbetalingen voor Litouwen

Bankbetalingsoverboekingen werden gegenereerd en afgedrukt met de exportindeling voor betalingsoverboekingen (LT) voor Litouwen. De Litouwse markt gebruikt vanaf 2005 LITAS, het universele elektronische bankiersysteem.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                        |
| **Vervangen door een andere functie?**   | Ja, ISO20022-indeling voor kredietoverdrachtbetalingen voor Litouwen     |
| **Betrokken productgebieden**         | Crediteuren                                               |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Betalingsindelingen van BBS Direkte voor Remittering voor Noorwegen

Betalingsindelingen voor BBS Direkte Remittering omvatten export van incasso met klantbetalingen (automatische afschrijving) en import van retourbericht.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.  |
| **Vervangen door een andere functie?**   | De AvtaleGiro-klantbetalingsindeling voor Noorwegen kan worden gebruikt om berichten voor automatische afschrijving te genereren. Het importeren van het retourbericht wordt geïmplementeerd in toekomstige versies. |
| **Betrokken productgebieden**         | Leveranciers, Klanten   |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Rekeningschematool voor Spanje

Deze tool wordt gebruikt wanneer een rekeningschema in Spanje belangrijke wijzigingen vereist. Gebruikers kunnen een nieuw rekeningschema in Microsoft Excel- of tekstindeling importeren, en kunnen ook financiële overzichten importeren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Beperkt gebruik                                                  |
| **Vervangen door een andere functie?**   | Nee                                                             |
| **Betrokken productgebieden**         | Grootboek                                                 |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80-betalingsindeling voor België

Verouderde Belgische betalingsindeling voor het innen van betalingen (automatische afschrijving).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindeling wordt niet meer gebruikt.                          |
| **Vervangen door een andere functie?**   | Ja, ISO 20022-betalingsindeling voor automatische afschrijving voor België         |
| **Betrokken productgebieden**         | Debiteuren                                            |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG-betalingsindelingen voor Zwitserland

DTA/EZAG-indelingen worden geïntegreerd in het ESR-systeem omdat ze een referentienummer kunnen hebben. Omdat de referentienummers niet verplicht zijn, kunnen alle leveranciersbetalingen worden verwerkt met deze indelingen. Deze indelingen worden gebruikt door bedrijven die een bankrekening op een locatie buiten Postfinance hebben.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                        |
| **Vervangen door een andere functie?**   | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Zwitserland   |
| **Betrokken productgebieden**         | Crediteuren                                               |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-betalingsindeling voor voor Oostenrijk

EDIFACT-DIRDEB-betalingsindeling voor het innen van betalingen (automatische afschrijving).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindeling wordt niet meer gebruikt.                          |
| **Vervangen door een andere functie?**   | Ja, ISO 20022-betalingsindeling voor automatische afschrijving voor Oostenrijk         |
| **Betrokken productgebieden**         | Debiteuren                                            |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="edivat-for-belgium"></a>EDIVAT voor België

EDIVAT is een verouderde Belgische standaard voor elektronische aangifte via beveiligde post. Dynamics AX 2012 behoudt de alleen-lezen oplossing om toegang tot de historische gegevens mogelijk te maken.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De functionaliteit wordt niet meer gebruikt.                           |
| **Vervangen door een andere functie?**   | Nee                                                             |
| **Betrokken productgebieden**         | Grootboek                                                 |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro Edifact CREMUL-importindeling voor betalingen in Noorwegen

eGiro is gebaseerd op de internationale UN-standaard EDIFACT CREMUL (Multiple Credit Advice Message) die voor het automatisch boeken van klantbetalingen wordt gebruikt. In Dynamics AX is eGiro geïmplementeerd als importindeling voor klantbetalingen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindeling wordt niet meer gebruikt.                                                     |
| **Vervangen door een andere functie?**   | Ja, het importeren van ISO20022 Camt.054-meldingen. |
| **Betrokken productgebieden**         | Debiteuren                                                                       |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                            |

### <a name="external-inventory-for-poland"></a>Externe voorraad voor Polen

Bewijs van goederen die zijn verkregen van een leverancier voor verkopen zonder inkoop. Goederen die in externe voorraad worden verwerkt, zijn niet van invloed op de standaardvoorraad en kunnen worden verkocht en vervolgens automatisch worden ingekocht. Dit proces zorgt voor echte voorraadmutaties.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een andere functie                                    |
| **Vervangen door een andere functie?**   | Ja, de kernfunctionaliteit van Inkomende consignatie                |
| **Betrokken productgebieden**         | Leveranciers, Voorraadbeheer                         |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Generator Financiële rapporten voor Oost-Europa

Een hulpmiddel om een gegevensverzameling in te stellen voor boekhouding en belastingaangiften, en om gegevens te exporteren naar XLS- en DOC-rapportsjablonen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Beperkt gebruik                                                                            |
| **Vervangen door een andere functie?**   | Nr. Het hulpmiddel wordt vervangen door Elektronische rapportageconfiguraties in toekomstige versies. |
| **Betrokken productgebieden**         | Grootboek                                                                           |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Importeren van de transacties van klantbetalingen voor Finland

U kunt een importindeling voor Finse betalingen selecteren om de transacties van klantbetalingen te importeren uit een extern bestand dat de bank heeft gegeven.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindeling wordt niet meer gebruikt.                                                     |
| **Vervangen door een andere functie?**   | Ja, het importeren van ISO20022 Camt.054-meldingen. |
| **Betrokken productgebieden**         | Debiteuren                                                                       |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Importeren van betalingstransacties in een grootboekjournaal voor Finland

Een indeling die specifiek is voor Finland, wordt gebruikt voor het importeren van boekhoudingstransacties in het grootboek.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindeling wordt niet meer gebruikt.                                                     |
| **Vervangen door een andere functie?**   | Ja, het importeren van ISO20022 Camt.053-bankafschriften met geavanceerde bankafstemming. |
| **Betrokken productgebieden**         | Debiteuren                                                                       |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integratie met Isabel gesynchroniseerd (CIS) voor België

Isabel is het framework voor elektronisch bankieren in Europa en een de facto-standaard in België.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Integratie met Isabel-client is beëindigd.   |
| **Vervangen door een andere functie?**   | Nr. De betalingsindelingen die niet meer worden gebruikt, worden vervangen door ISO20022-betalingsindeling voor kredietoverdracht voor België. |
| **Betrokken productgebieden**         | Crediteuren     |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Wijzigingen in het rekeningschema en boekhoudregels voor Spanje

Deze functie wordt gebruikt voor wijzigingen in het rekeningschema en boekhoudregels voor Spanje. Het koppelt rekeningen om het oude rekeningschema te transformeren in het nieuwe rekeningschema, en vergelijkt het vorige boekjaar met het nieuwe boekjaar, zelfs als ze op verschillende rekeningnummers zijn geboekt.

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Beperkt gebruik                                                  |
| **Vervangen door een andere functie?**   | Nee                                                             |
| **Betrokken productgebieden**         | Grootboek                                                 |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>De betalingsindeling Pagamento Fornittori voor leveranciersbetalingen

Verouderde Italiaanse betalingsindeling voor kredietoverdrachten.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindeling wordt niet meer gebruikt.                          |
| **Vervangen door een andere functie?**   | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Italië         |
| **Betrokken productgebieden**         | Crediteuren                                               |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="payment-export-formats-for-estonia"></a>Opmaak voor betalingsexport voor Estland

De indelingen Telehansa en Teleservice worden gebruikt voor het exporteren van bankbetalingen.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                        |
| **Vervangen door een andere functie?**   | Ja, ISO20022-betalingsindeling voor kredietoverdrachten voor Estland       |
| **Betrokken productgebieden**         | Crediteuren                                               |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="payment-file-archive-for-norway"></a>Betalingsbestandsarchief Noorwegen

Wanneer betalingsbestanden worden gegenereerd, archiveert het bestandarchief automatisch alle bestanden die worden gemaakt, zelfs bestanden die eerder zijn geschreven of gelezen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een andere functie                                        |
| **Vervangen door een andere functie?**   | Ja, Gearchiveerde taken elektronische rapportage                            |
| **Betrokken productgebieden**         | Leveranciers, Klanten, Organisatiebeheer |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.     |

### <a name="payment-import-formats-for-estonia"></a>Betalingsindelingen voor import voor Estland

De indelingen Telehansa en TeleTeenus worden gebruikt voor het importeren van bankbetalingen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                                                    |
| **Vervangen door een andere functie?**   | Ja, het importeren van ISO20022 Camt.054-bankmeldingen. |
| **Betrokken productgebieden**         | Debiteuren                                                                        |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                             |

### <a name="payroll-information-in-human-resources"></a>Salarisgegevens in Human Resources

Salarisgegevens in Human Resources

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Deze functionaliteit is vervangen door basispagina´s van Salarisadministratie en Human Resources.  |
| **Vervangen door een andere functie?**   | **Vergoedingen**, **Inkomsten** en andere gerelateerde pagina's die eerder deel uitmaakten van Salaris VS, zijn opnieuw geconfigureerd en maken nu deel uit van de basisconfiguratie van Human Resources en helpen externe loonlijstverwerking te ondersteunen. Deze functionaliteit is toegankelijk door de configuratiesleutel **Human Resources 1** \> **Salaris** te gebruiken. |
| **Betrokken productgebieden**         | Human Resources, Salaris   |
| **Status**                         | Verwijderd sinds Dynamics 365 for Operations-versie 1611.    |

### <a name="performance-management-goal-workflow"></a>Werkstroom doel prestatiebeheer

Prestatiebeheer omvat het beheren van het doel en integratie met beoordelingsgesprekken.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Prestatiebeheer is opnieuw opgezet en het aantal doelpagina's is verminderd om het proces te vereenvoudigen.                 |
| **Vervangen door een andere functie?**   | Nr. De doelen zijn zichtbaar voor managers via de portal Selfservice manager, en kunnen door de manager worden gewijzigd en weergegeven. |
| **Betrokken productgebieden**         | Human Capital-beheer       |
| **Status**                         | Verwijderd sinds Dynamics 365 for Operations-versie 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>De betalingsindelingen Postgirot en Utland Postgirot van Zweden

De betalingsindelingen Postgirot en Utland Postgirot van Zweden.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                        |
| **Vervangen door een andere functie?**   | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Zweden        |
| **Betrokken productgebieden**         | Crediteuren                                               |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="radio-frequency-identifier"></a>Radiofrequentie-identificatie

Radio Frequency Identification (RFID) is een gegevensverzamelingstechnologie waarbij elektronische tags worden gebruikt om identificatiegegevens op te slaan en er een reader zonder line-of-sight wordt gebruikt om de identificatiegegevens te lezen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Laag klantgebruik en een beperkte functieset.   |
| **Vervangen door een andere functie?**   | Nee                                              |
| **Betrokken productgebieden**         | Voorraadbeheer                            |
| **Status**                         | Verwijderd sinds Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Rapport over nummering van verkoopfacturen voor Letland

De Letse wetgeving kent specifieke regels voor het nummeren van verkoopfacturen. Met deze functionaliteit kunt u specifieke nummers toewijzen aan verkoopfacturen, op basis van de gebruiker of gebruikersgroep. U kunt vervolgens een rapport of een XML-bestand genereren. U kunt ook een rapport afdrukken over factuurnummers die worden gebruikt.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De statusnummering van de factuur hoeft niet meer te worden onderhouden. Het rapport over gebruikte factuurnummers is niet meer nodig. |
| **Vervangen door een andere functie?**   | Nee       |
| **Betrokken productgebieden**         | Debiteuren    |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>De namen van de manager en de algemene boekhouder instellen van een bedrijf voor Litouwen

De namen van de manager en de algemene boekhouder van een bedrijf kunnen in de bedrijfsgegevens zijn opgegeven en in verschillende lokale rapportafdrukken worden gebruikt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vervangen door een andere functie                                     |
| **Vervangen door een andere functie?**   | Ja, het instellen van de functionarissen kan voor hetzelfde doel worden gebruikt.   |
| **Betrokken productgebieden**         | Leveranciers, Klanten, Contant- en bankbeheer |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.  |

### <a name="shipping-carrier-interface"></a>Vervoerders interface

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dubbele functionaliteit.   |
| **Vervangen door een andere functie?**   | Gedeeltelijk vervangen door Transportbeheer |
| **Betrokken productgebieden**         | Verkoop en marketing, Voorraadbeheer  |
| **Status**                         | Verwijderd sinds Dynamics 365 for Operations-versie 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Betalingsindelingen voor Telepay voor Noorwegen

De Telepay-betalingsindelingen omvatten export van leveranciersbetalingen (kredietoverdracht) en het innen van klantbetalingen (automatische afschrijving).

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                                                        |
| **Vervangen door een andere functie?**   | Ja, het importeren van de ISO20022-indeling voor kredietoverdrachtbetalingen en Indeling voor AvtaleGiro-klantbetalingen voor Noorwegen, evenals retourbestanden voor pain.002- en camt.054-bankmeldingen importeren. |
| **Betrokken productgebieden**         | Leveranciers, Klanten                                                          |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Exportindelingen voor leveranciersbetalingen voor Finland

Twee indelingen voor het exporteren van betalingen zijn beschikbaar voor Finland. LM02 (FI) wordt gebruikt voor nationale betalingen en LUM2 (FI) wordt gebruikt voor buitenlandse betalingen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De betalingsindelingen worden niet meer gebruikt.                        |
| **Vervangen door een andere functie?**   | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Finland       |
| **Betrokken productgebieden**         | Crediteuren                                               |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="warehouse-management-ii"></a>Magazijnbeheer II

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De oplossing Magazijnbeheer II (WMS II) die beschikbaar was in de module **Voorraadbeheer** dupliceert functionaliteit in de module **Magazijnbeheer** die werd gepubliceerd in Dynamics AX 2012 R3.                                                                         |
| **Vervangen door een andere functie?**   | De module **Magazijnbeheer** die is gepubliceerd in AX 2012 R3, Dynamics AX 2012 R3 CU8 en Dynamics AX 2012 R3 CU9 vervangt de functies van Magazijnbeheer II. De nieuwe module heeft meer geavanceerde functies en flexibelere magazijnbeheerprocessen dan Magazijnbeheer II. |
| **Betrokken productgebieden**         | Voorraadbeheer, Verkoop en marketing, Inkoop en sourcing   |
| **Status**                         | Verwijderd sinds Dynamics 365 for Operations-versie 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Herinneringen voor werknemers in Human Resources

Salarisgegevens in Human Resources

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Laag gebruik                                                           |
| **Vervangen door een andere functie?**   | Nee                                                                  |
| **Betrokken productgebieden**         | Human Resources                                                     |
| **Status**                         | Verwijderd sinds Dynamics 365 for Operations-versie 1611 |

### <a name="workflow-for-creating-goals"></a>Workflow voor het maken van doelen

Een workflow voor het beheren van het maken van werknemerdoelstellingen is een van meerdere workflows die beschikbaar zijn om het prestatiebeheerproces te coördineren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Prestatiebeheer is volledig opnieuw ontworpen in Finance and Operations.     |
| **Vervangen door een andere functie?**   | De functie Prestatiebeheer is volledig opnieuw ontworpen en geeft meer controle over de inhoud van de doelen, de metingen die worden gebruikt om de voortgang bij te houden en het bijvoegen van ondersteunende documentatie. Doelen kunnen als sjablonen worden opgeslagen en opnieuw worden gebruikt. Deze functie kan u helpen om sneller extra doelen voor uw werknemers op te zetten. |
| **Betrokken productgebieden**         | Human Capital-beheer                 |
| **Status**                         | Verwijderd sinds Dynamics 365 for Operations-versie 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Mogelijkheid om wijzigingen aan een leveranciersfactuur te annuleren

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Prestatieverbeteringen        |
| **Vervangen door een andere functie?**   | Nee                             |
| **Betrokken productgebieden**         | Leveranciers               |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>Integraties met AIF, AxD en AxBC

In Application Integration Framework (AIF) kunnen gegevens worden uitgewisseld met externe systemen door bedrijfslogica die als services beschikbaar is. Dynamics AX bevat services die op documenten en .NET Business Connector (AxBC) zijn gebaseerd. Een document wordt gemaakt door XML te gebruiken. De XML bevat koptekstinformatie die wordt toegevoegd om een *bericht* te maken dat naar of uit Dynamics AX kan worden overgebracht. Voorbeelden van documenten zijn verkooporders en inkooporders. Bijna elke entiteit, zoals een klant, kan echter door een document worden weergegeven. Services die op documenten zijn gebaseerd, gebruiken de **Axd \<Document\>**-klassen.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De architectuur van AIF en AxDs kon niet aan de schaal van een cloudservice worden aangepast. Dit leidde tot prestatieproblemen met de bulkimport.                                        |
| **Vervangen door een andere functie?**   | Deze functie is vervangen door het raamwerk voor gegevensimport/-export, dat herhalende bulkimport/-export ondersteunt. Voor AxBC is het raadzaam om de werkelijke tabellen te gebruiken. |
| **Betrokken productgebieden**         | AxDs, AxBCs en AIF   |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.   |

### <a name="billing-code-rate-scripts"></a>Wisselkoersscripts voor factureringscode

Factureringsscripts werden gebruikt voor het berekenen van factureringstarieven voor factureringscodes. Voor deze scripts was een aangepaste ontwikkeling vereist in de programmeertaal C Sharp of Visual Basic. In de huidige versie van Dynamics AX worden de **wisselkoersscripts voor factureringscode** niet ondersteund.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De ondersteuning voor de aangepaste C Sharp- of Visual Basic-scripts is niet toegevoegd in Dynamics AX 7.0. |
| **Vervangen door een andere functie?**   | Nee                                                                                      |
| **Betrokken productgebieden**         | Publieke sector, Klanten                                    |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                                                          |

### <a name="boms-without-bom-versions"></a>Stuklijsten zonder stuklijstversies

Wanneer de configuratiesleutel **Stuklijstversies** werd uitgeschakeld, werden de stuklijstversies verborgen in alle formulieren en het systeem dwong een 1:1-relatie af tussen vrijgegeven producten en stuklijsten. In de huidige versie van Dynamics AX kan de configuratiesleutel **Stuklijstversies** niet worden uitgeschakeld.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Gebruik van een configuratiesleutel voor controle van de stuklijstversies kon niet worden aangepast aan een cloudomgeving. |
| **Vervangen door een andere functie?**   | Nee                                                                                      |
| **Betrokken productgebieden**         | Productgegevensbeheer, Voorraadbeheer                                    |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Braziliaanse Bordero

Specifieke betalingsmethode voor Braziliaanse bedrijven

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De ondersteuning voor de Braziliaanse Bordero-betalingsmethode is verwijderd uit de Braziliaanse lokalisatie |
| **Vervangen door een andere functie?**   | Nee   |
| **Betrokken productgebieden**         | Crediteuren   |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="brazilian-sintegra-statement"></a>Braziliaans Sintegra-overzicht

Federaal belastingoverzicht voor ICMS-belasting

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Deze instructie is niet meer van toepassing in sommige Braziliaanse staten. |
| **Vervangen door een andere functie?**   | Nr. Gebruikers kunnen het Algemene elektronische rapportagehulpmiddel (GER) gebruiken om indien nodig het overzicht in specifieke situaties te configureren. |
| **Betrokken productgebieden**         | Belastingboeken    |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Braziliaanse SCAN contingentiemous voor NF-e

(SCAN) wordt gebruikt voor het genereren, exporteren en importeren van de status van een Nota Fiscal eletrônica (NF-e)wanneer de omgeving van Secretaria Da fazenda (SEFAZ) niet beschikbaar is.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Deze contingentiemethode is niet langer van toepassing in alle Braziliaanse staten |
| **Vervangen door een andere functie?**   | Nee                                                                          |
| **Betrokken productgebieden**         | Debiteuren                                                         |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.              |

### <a name="business-analyzer"></a>Bedrijfsanalyse

Deze mobiele toepassing laat gebruikers belangrijke zakelijke maatstaven controleren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De functionaliteit is vervangen door een andere functie.   |
| **Vervangen door een andere functie?**   | Het inhoudspakket Financiële prestaties controleren voor Microsoft Power BI bevat belangrijke financiële maatstaven die eerder beschikbaar waren in Business Analyzer. |
| **Betrokken productgebieden**         | Grootboek      |
| **Status**                         | Afgeschaft: Bedrijfsanalyse is afgeschaft.    |

### <a name="business-statistics"></a>Zakelijke statistieken

De instelling van query's voor zakelijke statistieken waarmee u de prestaties van uw organisatie kunt analyseren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Verouderde benadering voor Business Intelligence (BI), laag klantgebruik en een beperkte functieset |
| **Vervangen door een andere functie?**   | Nieuwe BI-oplossingen voor de huidige versie van Dynamics AX                                      |
| **Betrokken productgebieden**         | Inkoopbeheer, Leveranciers, Verkoop en marketing, Klanten         |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Functie voor wijzigen van documentdatum het Factuurgoedkeuringsjournaal

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Laag gebruik                                                               |
| **Vervangen door een andere functie?**   | Ja. De documentdatum op de geboekte leverancierstransactie kan worden gewijzigd. |
| **Betrokken productgebieden**         | Leveranciers                                                        |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Betalingsindeling ClieOp03 voor Nederland

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De indeling is niet meer geldig in Nederland omdat het is vervangen door de functionaliteit voor de gemeenschappelijke betalingsruimte voor de euro (SEPA). |
| **Vervangen door een andere functie?**   | SEPA-betalingen exporteren  |
| **Betrokken productgebieden**         | Alle modules     |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.   |

### <a name="compliance-center"></a>Help bij conformiteit

Help bij conformiteit was een site van Enterprise Portal voor het beheren van de documentatiebehoeften voor conformiteitsinitiatieven die verband houden met de Sarbanes Oxley Act.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Gebrek aan klantgebruik. Microsoft SharePoint bevat dezelfde mogelijkheid die in Help bij conformiteit beschikbaar was. |
| **Vervangen door een andere functie?**   | Nee   |
| **Betrokken productgebieden**         | Conformiteit en interne controles  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Connector voor Microsoft Dynamics

Deze tool is gebruikt om belangrijke gegevens van Microsoft Dynamics CRM te integreren in Dynamics ERP-toepassingen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De functionaliteit is vervangen door een andere functie. |
| **Vervangen door een andere functie?**   | Common data service                                      |
| **Betrokken productgebieden**         | Connector voor Dynamics                         |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Containereenheid en meerdere dimensies voorhanden

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dubbele functionaliteit. |
| **Vervangen door een andere functie?**   | Ja. Sinds AX 2012 is deze functionaliteit vervangen door de geconsolideerde batchorderfunctieset. Deze functieset bevat de geconsolideerde voorhanden weergave. |
| **Betrokken productgebieden**         | Productgegevensbeheer, Productiebeheer, Voorraadbeheer, Verkoop en marketing  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Metagegevens van hintgroep

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De hintgroepen werden gebruikt om één of meer hints in het feitenblokgebied weer te geven. Er was maar weinig gebruik, en er waren ook problemen met de prestaties doordat een recordwijziging in een bovenliggend formulier één query per hint in de hintgroep veroorzaakte. |
| **Vervangen door een andere functie?**   | Nee      |
| **Betrokken productgebieden**         | Alle modules    |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Hint-metagegevens

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De hint-metagegevens zijn beperkt tot gegevens voor som of aantal.    |
| **Vervangen door een andere functie?**   | De tegelmetagegevens zijn geïntroduceerd om meer flexibiliteit voor modellering te bieden. U kunt bijvoorbeeld actuele tellingen, navigatie en Key Performance Indicators (KPI's) modelleren. De metagegevens van de tellingstegel zijn de directe vervanging van de hintmetagegevens. |
| **Betrokken productgebieden**         | Alle modules           |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Deense cheque-indeling

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Ondersteuning voor de Deense cheque-indeling is beëindigd, en het rapport is verwijderd uit de Deense lokalisatie. |
| **Vervangen door een andere functie?**   | Nee    |
| **Betrokken productgebieden**         | Alle modules    |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.  |

### <a name="data-partitions"></a>Gegevenspartities

Gegevenspartities bieden een logische scheiding van gegevens in de Dynamics AX-database.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | In Dynamics AX 2012 R2 werden gegevenspartities geïntroduceerd om de isolatie van gegevens mogelijk te maken. In een gebruikelijk scenario heeft een bedrijf dochterondernemingen en mogen de gegevens van de ene vestiging niet zichtbaar zijn voor een andere vestiging, hoewel beide dochterondernemingen worden beheerd door dezelfde IT-afdeling. Er waren echter extra scripts en beheeroverhead in het hele programma vereist om nieuwe partities maken en deze te vullen met gegevens, en om back-ups van partitiegegevens te maken. In de cloud, waar we toegang hebben tot PaaS-databaseservices (platform als een service) (Microsoft Azure SQL-database), is het veel efficiënter gebruik te maken van een database als de isolatiecontainer dan om isolatie uit te voeren in het programma. Ongeacht of partitioneren van gegevens vereist is voor dochterondernemingen, voor meerdere tenants of gewoon voor schaal, geloven wij dat de scenario's beter kunnen worden verwerkt via meerdere exemplaren van Finance and Operations. |
| **Vervangen door een andere functie?**   | Klanten die gebruikmaken van gegevenspartities moeten meerdere exemplaren van Finance and Operations gebruiken als scheiding op databaseniveau een kritiek punt is.    |
| **Betrokken productgebieden**         | Alle modules  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Opslag in database en bestandsshare voor bijlagen

In Dynamics AX 2012 was opslag van bijlagen in de database en bestandsshares toegestaan. Beide opties worden niet langer ondersteund.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Opslag in bestandsshares wordt niet langer ondersteund omdat in de cloud gehoste omgevingen niet kunnen communiceren met lokale bestandsshares. Database-opslag is vervangen door een Azure Blob-opslag. Azure Blob-opslag is vergelijkbaar met opslag in de database, omdat documenten alleen toegankelijk zijn via clientformulieren van Finance and Operations. Dit biedt als extra voordeel dat opslagcapaciteit wordt geboden die geen nadelige invloed heeft op de prestaties van de database. Blobopslag is het standaardopslagmechanisme voor Documentbeheer en werkt onmiddellijk. |
| **Vervangen door een andere functie?**   | Database-opslag is vervangen door een Azure Blob-opslag.   |
| **Betrokken productgebieden**         | Alle modules  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.   |

### <a name="delimitation"></a>Begrenzing

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Geen gebruik van de functionaliteit gevonden. |
| **Vervangen door een andere functie?**   | Nee                                     |
| **Betrokken productgebieden**         | Tijd en aanwezigheid                    |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Bureaubladclient

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De ervaring met de Dynamics AX-client is opnieuw ontworpen om bruikbaarheid over meerdere platformen en apparaten te verbeteren.                      |
| **Vervangen door een andere functie?**   | De nieuwe webclient is gebaseerd op het metagegevens en programmeringsmodel van het bureaubladformulier, die zijn aangepast om een rijk webplatform te bieden. |
| **Betrokken productgebieden**         | Alle modules  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Directe databaseverbinding

In Dynamics AX 2012 R3 kan Retail Modern POS direct verbinding maken met de afzetkanaal-DB op soortgelijke wijze als Enterprise POS. Dit was een aanvulling op de standaardcommunicatiemethode van communicatie van Retail Modern POS via Retail Server.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Voor een directe databaseverbinding waren lagere beveiligingsprotocollen vereist en deze methode werd voornamelijk gebruikt voor het behalen van optimale prestaties. Door de prestatie- en beveiligingsverbeteringen in Finance and Operations levert deze functionaliteit nu meer problemen op dan ermee worden opgelost. |
| **Vervangen door een andere functie?**   | Nr. Alleen standaard Retail Server-communicatie wordt nu ondersteund.  |
| **Betrokken productgebieden**         | Afzetkanaal-DB/Retail Modern POS   |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Nederlandse SWIFT MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Algemene functionaliteit wordt nu gebruikt in plaats van gelokaliseerde functionaliteit.                    |
| **Vervangen door een andere functie?**   | Ja, deze functionaliteit is vervangen door de functionaliteit Geavanceerde bankafstemming. |
| **Betrokken productgebieden**         | Alle modules                                                                              |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL voor Duitsland)

Deze functionaliteit bood uitvoer in eXtensible Business Reporting Language (XBRL) die voor de Duitse eBilanz-taxonomie is bedoeld.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Gebrek aan klantgebruik  |
| **Vervangen door een andere functie?**   | Deze functie is niet vervangen door een andere functie, maar meerdere gespecialiseerde XBRL-pakketten die uitgebreide XBRL-functionaliteit bieden, zijn beschikbaar voor de Duitse markt. |
| **Betrokken productgebieden**         | Management Reporter      |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.  |

### <a name="enterprise-portal-client"></a>Enterprise Portal-client

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Een enkel clientplatform wordt geboden.  |
| **Vervangen door een andere functie?**   | De nieuwe webclient is gebaseerd op de metagegevens en het programmeringsmodel van het bureaubladformulier, die zijn aangepast om een rijk webplatform te bieden. |
| **Betrokken productgebieden**         | Alle modules  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Milieuduurzaamheid

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Laag klantgebruik en een beperkte functieset  |
| **Vervangen door een andere functie?**   | Nee              |
| **Betrokken productgebieden**         | Conformiteit en interne controles, Leveranciers  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Besturingselementen in formulier-ActiveX en Managed Host

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De besturingselementen voor ActiveX en de Managed Host zijn gebaseerd op de verouderde bureaubladclient. |
| **Vervangen door een andere functie?**   | Het uitbreidbare besturingselementraamwerk ondersteunt het maken van nieuwe besturingselementen die op HTML, CSS en JavaScript zijn gebaseerd en is een prima besturingselement in de Microsoft Visual Studio Tooling-omgeving. |
| **Betrokken productgebieden**         | Alle modules     |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Voorafmeldingen genereren door een batch te gebruiken

Het genereren van voorafmeldingen kan niet worden uitgevoerd door een batch te gebruiken, maar kan nog wel door een gebruiker worden gedaan.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Er bestaat geen formulier om het resulterende voorafmeldingenbestand permanent op te slaan en weer te geven wanneer het wordt gegenereerd door een batch te gebruiken. |
| **Vervangen door een andere functie?**   | Voorafmeldingen kunnen nog steeds worden gegenereerd, en de gebruiker kan bepalen waar het bestand wordt opgeslagen.   |
| **Betrokken productgebieden**         | Leveranciers, Klanten, Contant- en bankbeheer  |
| **Status**                         | Verwijderd sinds AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Duitse DTAUS-betalingsexport en rekeningoverzichtimport (totalen en transacties)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De indeling is niet meer geldig in Duitsland, omdat het is vervangen door de functionaliteit voor de gemeenschappelijke betalingsruimte voor de euro (SEPA).                    |
| **Vervangen door een andere functie?**   | Ja, deze functionaliteit is vervangen door de functionaliteit voor export van SEPA-betalingen en geavanceerde bankafstemming bij het importeren van rekeningoverzichten. |
| **Betrokken productgebieden**         | Alle modules  |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>Indeling van Duitse DTAZV-betalingen in binnenlandse valuta

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De indeling is niet meer geldig in Duitsland omdat het is vervangen door de functionaliteit voor de gemeenschappelijke betalingsruimte voor de euro (SEPA). |
| **Vervangen door een andere functie?**   | SEPA-betalingen exporteren    |
| **Betrokken productgebieden**         | Crediteuren   |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.    |

### <a name="german-mt940-import"></a>Duitse MT940-import

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Algemene functionaliteit wordt nu gebruikt in plaats van gelokaliseerde functionaliteit.                    |
| **Vervangen door een andere functie?**   | Ja, deze functionaliteit is vervangen door de functionaliteit Geavanceerde bankafstemming. |
| **Betrokken productgebieden**         | Alle modules                                                                              |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.                           |

### <a name="german-xml-eu-sales-list"></a>XML-indeling voor Duitse ICL-lijst

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De XML-indeling voor de rapportage van de Duitse ICL-lijst wordt niet meer ondersteund. Alleen de ELMA5-tekstbestandsindeling kan worden gebruikt om het rapport van de ICL-lijst bij de Duitse belastingdienst in te dienen. |
| **Vervangen door een andere functie?**   | Nee         |
| **Betrokken productgebieden**         | Btw        |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.   |

### <a name="gl-ssrs-reports"></a>GL SSRS-rapporten

Rapporten die de volgende menu-items bevatten, zijn verwijderd: **Proefbalans overzicht**, **Gedetailleerde proefbalans**, **Rekeningschema**, **Audittrail**, **Saldi** en **Saldilijst**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Financiële rapporten van Microsoft SQL Server Reporting Services (SSRS) zijn vervangen door de mogelijkheden en standaardrapporten van Management Reporter. |
| **Vervangen door een andere functie?**   | Management Reporter (in de huidige versie van Dynamics AX aangeduid als **Financiële rapportage**)    |
| **Betrokken productgebieden**         | Grootboek   |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>Metagegevens voor InfoPart en FormPart

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Metagegevens voor InfoPart en FormPart maakten het mogelijk om feitenblokken voor twee verschillende clients te maken. |
| **Vervangen door een andere functie?**   | De InfoPart-metagegevens, die een vereenvoudigde formulierdefinitie zijn, zijn omgezet in een formulier met upgrade-tooling. De FormPart-metagegevens, die naar een formulier verwezen, zijn vervangen door een directere verwijzing die door upgrade-tooling wordt aangemaakt. |
| **Betrokken productgebieden**         | Alle modules    |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Lijstpagina Hoofdrekening

Een lijst met rekeningen voor de rechtspersoon en de gerelateerde saldogegevens

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Saldoinformatie is beschikbaar op de lijstpagina **Proefbalans** per rekening en dimensie.  |
| **Vervangen door een andere functie?**   | **Hoofdrekeningen** bevat dezelfde lijst met rekeningen die de lijstpagina **Hoofdrekening** bevatte. In de rasterweergave ook **Hoofdrekeningen** wordt nog een kleinere, rasterachtige weergave getoond. |
| **Betrokken productgebieden**         | Grootboek      |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Bankcashflowrapport voor Maleisië en Singapore

Met deze functie kan de gebruiker een cashflowrapport afdrukken waarop de transacties en details van de kasinkomsten en -uitgaven in een bepaald datumbereik worden weergegeven voor geselecteerde bankrekeningen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dezelfde informatie kan uit de query banktransacties worden verkregen. |
| **Vervangen door een andere functie?**   | Banktransactie opvragen                                            |
| **Betrokken productgebieden**         | Contanten en bankbeheer                                                |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie.          |

### <a name="mexican-cfd-electronic-invoice"></a>Mexicaanse CFD elektronische factuur

Deze functie maakte het mogelijk Mexicaanse elektronische facturen te genereren door de Comprobante Fiscales Digitales-methode (CFD) te gebruiken, waarin het bedrijf de factuur ondertekent door de gerelateerde autorisatie bij de overheid aan te vragen. Deze functie bevat ook een maandelijks rapport dat alle elektronische facturen bevat die zijn uitgegeven in de periode.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De methode is niet langer van toepassing. Het genereren van elektronische facturen via de CFD-methode is beëindigd door de belastingdienst en vervangen door de methode Comprobante Fiscal Digital a través de Internet (CFDI), waarin het ondertekenen aan de externe provider (PAC)wordt gedelegeerd. Het maandelijkse rapport is verwijderd, en een queryoptie geeft gebruikers de mogelijkheid om historische transacties op te vragen. |
| **Vervangen door een andere functie?**   | Nee    |
| **Betrokken productgebieden**         | Klanten, Project   |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="mexico-realized-and-unrealized-vat"></a>Gerealiseerde en niet-gerealiseerde btw voor Mexico

In Dynamics AX 2012 beheerde, niet-gerealiseerde btw door specifiek voor Mexico bedoelde functionaliteit voor niet-gerealiseerde btw te gebruiken.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dubbele functionaliteit.  |
| **Vervangen door een andere functie?**   | Ja, deze functionaliteit is vervangen door standaard voorwaardelijke btw-functionaliteit die in het kernsysteem wordt verschaft. |
| **Betrokken productgebieden**         | Btw   |
| **Status**                         | Afgeschaft: er is nog geen datum voor verwijdering bepaald voor deze functie. |

### <a name="microsoft-outlook-integration"></a>Integratie Microsoft Outlook


| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Deze functionaliteit is vervangen door Microsoft Exchange Server-integratie. |
| **Vervangen door een andere functie?**   | Ja                                                                            |
| **Betrokken productgebieden**         | Verkoopbeheer en marketing                                                            |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Als privé blokkeren van journalen voor voorraad- en magazijnbeheer

De voorraad- en magazijnjournalen ondersteunen niet meer de mogelijkheid om een journaal te markeren als privé voor een geselecteerde gebruiker. Alleen het proces om journalen te blokkeren als privé voor gebruikersgroepen en blokkeren tijdens het bewerken wordt ondersteund.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Geen gebruik van de functionaliteit gevonden. |
| **Vervangen door een andere functie?**   | Nee                                     |
| **Betrokken productgebieden**         | Voorraadbeheer                   |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.         |

### <a name="product-builder"></a>Product Builder

Product Builder werd gebruikt om dynamisch items te configureren vanuit een verkooporder, inkooporder, productieorder, verkoopofferte, projectofferte of artikelbehoefte. Op basis van een productmodel dat modelvariabelen had, kon de gebruiker waarden selecteren om te voldoen aan klantbehoeften en een unieke productvariant te krijgen die een stuklijst en een route had.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Product Builder liet gebruikers X++-code zien en wordt niet ondersteund in de huidige versie van Dynamics AX. Het is verwijderd om dubbele onderhoudsinspanningen te voorkomen in overlappende codebases van aanzienlijke omvang.  |
| **Vervangen door een andere functie?**   | Ja. De op beperkingen gebaseerde configuratie werd geïntroduceerd in Dynamics AX 2012, waarin al werd aangekondigd dat Product Builder in toekomstige versies zou worden afgeschaft. De op beperkingen gebaseerde configuratie wordt geselecteerd in productmodellen om de configuratie mogelijk te maken. Zie [Overzicht van productconfiguratie](../../../supply-chain/pim/build-product-configuration-model.md) voor meer informatie. |
| **Betrokken productgebieden**         | Productiegegevensbeheer, Verkoop en marketing  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Production Floor-app
Dit is de app voor tablets met Windows 8.1 RT en Windows 8.1 Pro.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met de wijziging naar een webclient is het mogelijk om vergelijkbare functionaliteit te bieden via de native Dynamics AX 7.0-client. Het apparaat voor taakkaarten biedt een gebruikersinterface voor de productievloer die is geoptimaliseerd voor touchscreens en tablets. |
| **Vervangen door een andere functie?**   | Ja. Het apparaat voor taakkaarten, een native onderdeel van Dynamics AX 7.0.                                                                           |
| **Betrokken productgebieden**         | Productiebeheer                                                |
| **Status**                         | Afgeschaft: voor deze functie is nog geen datum voor verwijdering uit de Microsoft Store ingesteld.                                                |


### <a name="rename-product-dimension"></a>Productdimensie hernoemen

Met deze functie kon u de naam van een van de drie standaardproductdimensies (grootte, kleur of stijl) wijzigen in een naam die beter aansloot op uw zakelijke behoeften. Hernoemen omvatte alle labels waar de productdimensienaam werd gebruikt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De huidige versie van Dynamics AX ondersteunt geen labelwijzigingen tijdens runtime. |
| **Vervangen door een andere functie?**   | Nee                                                                            |
| **Betrokken productgebieden**         | Productgegevensbeheer                                                |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Retail Server-verbinding via HTTP

In Dynamics AX 2012 R3 kon de Retail Server functioneren met behulp van HTTP-communicatie (niet-beveiligd). Dit was naast de standaardcommunicatie via HTTPS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Als gevolg van nieuwe beveiligingsvereisten, wordt nu alleen beveiligde communicatie via TLS 1.2 (of hoger, indien beschikbaar) ondersteund. Het installatieprogramma Self-service configureert automatisch de computer voor deze communicatie. |
| **Vervangen door een andere functie?**   | Nr. Alleen standaard HTTPS-communicatie wordt nu ondersteund. |
| **Betrokken productgebieden**         | Detailhandelserver  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Pagina's van rollencentrums

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Rollencentrum-pagina's zijn gebaseerd op het verouderd Enterprise Portal-platform, dat door het nieuwe webclientplatform in de huidige versie van Dynamics AX is vervangen. |
| **Vervangen door een andere functie?**   | Het patroon van het nieuwe Werkruimteformulier biedt gebruikers een proces-gecentreerd ontwerp, dat eenvoudig toegang biedt tot vaak gebruikte taken binnen dat proces.                       |
| **Betrokken productgebieden**         | Alle modules    |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Btw-jurisdictie

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Laag klantgebruik en een beperkte functieset |
| **Vervangen door een andere functie?**   | Nee                                           |
| **Betrokken productgebieden**         | VS btw                                 |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.               |

### <a name="sites-services"></a>Sites Services

Met Sites Services kunt u websites maken die uw bedrijfsprocessen naar internet uitbreiden zonder IT-ondersteuning.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De Microsoft Azure-infrastructuur die door Dynamics AX wordt gebruikt, heeft nieuwe mogelijkheden die in plaats daarvan kunnen worden gebruikt (bijvoorbeeld Azure-sites). |
| **Vervangen door een andere functie?**   | Nee   |
| **Betrokken productgebieden**         | HR-werving, Aanvraagbeheer, Offerteaanvragen, Leveranciersregistratie, werkgebieden voor samenwerking voor verkoopkansen en campagnes  |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS-vraagprognosestrategie

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het ontwerp van de functie kan niet worden ondersteund in de nieuwe cloudarchitectuur. |
| **Vervangen door een andere functie?**   | Azure Machine Learning-vraagprognosestrategie                           |
| **Betrokken productgebieden**         | Hoofdplanning                                                              |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Leveranciersfactuurpool met uitzondering van boekingsdetails

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Laag gebruik. Deze functionaliteit is vervangen door het factuurjournaal dat workflowfunctionaliteit heeft. |
| **Vervangen door een andere functie?**   | Workflowmogelijkheden van het factuurjournaal.     |
| **Betrokken productgebieden**         | Leveranciers |
| **Status**                         | Verwijderd sinds Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Virtuele bedrijfsrekeningen

De functie voor virtuele bedrijven wordt niet meer ondersteund in Dynamics AX. Met de functie Virtuele konden gebruikers tabellen instellen die konden worden gedeeld door een reeks bedrijven. Zie voor een omschrijving van de functie [Bedrijfsrekeningen en virtuele bedrijfsrekeningen](https://msdn.microsoft.com/library/aa834382(v=ax.10).aspx). De functie werkt door tabellen in verzamelingen te groeperen die aan virtuele bedrijven zijn toegewezen, die groepen van bestaande "echte" bedrijven zijn. Query's worden gemaakt zodat alle bedrijven in het virtuele bedrijf toegang hebben tot de gegevens in de tabellen van de gekoppelde tabelverzamelingen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | - Virtuele bedrijven moeten worden ingericht voordat gegevens in de tabellen worden opgeslagen. Retroactief invoegen van virtuele bedrijven in een bestaande implementatie is zeer moeilijk.<br><br>- Omdat er zoveel gegevensnormalisatie in de huidige versie van Dynamics AX is doorgevoerd, is het lastig geworden om te weten wat aan de tabelverzamelingen moet worden toegevoegd. Het is bijvoorbeeld moeilijk te bepalen welke tabellen moeten worden gedeeld. Alle tabellen waarnaar wordt verwezen vanuit tabellen die deel uitmaken van een virtueel bedrijf, moeten ook worden toegevoegd. Vanwege tabelnormalisatie moeten zelfs eenvoudige hoofdgegevens die zijn verdeeld over meerdere tabellen, deel uitmaken van het virtuele bedrijf. Eventuele fouten die hier worden gemaakt, leiden tot functionele problemen.<br><br>- Wanneer een tabel deel uitmaakt van een virtueel bedrijf, verliest het informatie over de oorsprong van de gegevens en wordt alleen het virtuele bedrijf geregistreerd.   |
| **Vervangen door een andere functie?** | Algemene tabellen kunnen worden gebruikt om tabellen toegankelijk te maken vanuit alle bedrijven. Momenteel is er geen vervanging. |   
| **Betrokken productgebieden**       | Alle modules |   
| **Status**                       | Verwijderd sinds Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8-tabletapp

De Windows 8-tabletapp leverde functionaliteit voor het invoeren van onkosten en goedkeuring.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Finance and Operations is compatibel met tablets. De tablet-app is niet langer vereist.    |
| **Vervangen door een andere functie?**   | Nr.          |
| **Betrokken productgebieden**         | Onkostenbeheer   |
| **Status**                         | Verwijderd: deze functionaliteit is alleen beschikbaar voor Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Werkplanner

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Laag gebruik |
| **Vervangen door een andere functie?**   | Nee, maar de pagina **Profielrelatie** die wordt geopend via de pagina **Profielgroepen** ondersteunt hetzelfde bedrijfsscenario als de afgeschafte pagina **Werkplanner**. |
| **Betrokken productgebieden**         | Tijd en aanwezigheid     |
| **Status**                         | De code is niet verwijderd. Het formulier, JmgWorkPlanner, is echter niet gemigreerd.    |

### <a name="x-financial-statements"></a>X++ in financiële overzichten

| &nbsp;  | &nbsp; |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Reden voor afschaffing/verwijdering</strong> |                         De functionaliteit is vervangen door een andere functie.                         |
|  <strong>Vervangen door een andere functie?</strong>  | Management Reporter (in de huidige versie van Dynamics AX aangeduid als <strong>Financiële rapportage</strong>) |
|     <strong>Betrokken productgebieden</strong>     |                                              Grootboek                                              |
|             <strong>Status</strong>             |                                      Verwijderd sinds Dynamics AX 2012                                      |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]