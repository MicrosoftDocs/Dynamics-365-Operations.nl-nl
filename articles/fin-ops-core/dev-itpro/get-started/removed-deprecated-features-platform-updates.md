---
title: Verwijderde of afgeschafte Platform-functies
description: In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van apps voor financiën en bedrijfsactiviteiten.
author: sericks007
ms.date: 04/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0cf0d4b3ff108645c8542ce10a0be58d29cc68ed
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644602"
---
# <a name="removed-or-deprecated-platform-features"></a>Verwijderde of afgeschafte platform-functies

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van apps voor financiën en bedrijfsactiviteiten.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

Gedetailleerde informatie over objecten in apps voor financiële en bedrijfsactiviteiten is te vinden in de [Rapporten met technische naslaginformatie](/dynamics/s-e/global/axtechrefrep_61). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van apps voor financiële en bedrijfsactiviteiten.

## <a name="feature-deprecation-effective-april-2022"></a>Kennisgeving van afschaffing van functie met ingang van april 2022

### <a name="xml-url-resolution-in-data-management"></a>XML-URL-omzetting in Gegevensbeheer 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Wij verwijderen de ondersteuning voor het omzetten van XML-URL's, omdat dit is geïdentificeerd als een mogelijke beveiligingsprobleem. Dit betekent dat externe bronnen die aan XML-bestanden zijn gekoppeld, niet meer kunnen worden omgezet.  |
| **Vervangen door een andere functie?**   | Nummer |
| **Betrokken productgebieden**         | Apps voor financiële en bedrijfsactiviteiten |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft. |

## <a name="feature-deprecation-effective-march-14-2022"></a>Kennisgeving van afschaffing van functie met ingang van 14 maart 2022

### <a name="xslt-scripting-in-data-management"></a>XSLT-scripting in Gegevensbeheer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De ondersteuning van XSLT-scripting in Gegevensbeheer is afgeschaft om de beveiliging en gegevensbeveiliging binnen apps voor financiën en bedrijfsactiviteiten te verbeteren.  |
| **Vervangen door een andere functie?**   | Nummer Klanten en ISV's moeten overwegen hun oplossingen opnieuw te implementeren op basis van de X++-taal in plaats van XSLT-scripting. |
| **Betrokken productgebieden**         | Apps voor financiële en bedrijfsactiviteiten |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft <br><br>**Uitzondering:** klanten die momenteel XLST-scripting gebruiken. Ze kunnen dit blijven gebruiken totdat ze updaten naar versie 10.0.30 of hoger. Voor eerdere versies verloopt de uitzondering per 31 januari 2023. Klanten met deze uitzondering hebben een melding ontvangen in de Berichtencentrum in het Microsoft 365-beheercentrum. |

## <a name="feature-removal-effective-october-2021"></a>Functie is verwijderd in oktober 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL-rapporten in Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Alle activiteiten en monitoring worden intern uitgevoerd door het platform via automatisering. Er is geen handmatige tussenkomst nodig.|
| **Vervangen door een andere functie?**   | Ja, er is nu een geautomatiseerd systeem, die deze mogelijkheden overbodig maken. |
| **Betrokken productgebieden**         | SQL-rapporten: Huidige DTU, huidige DTU-details, Vergrendelingsdetails weergeven, Lijst met huidige planhandleiding, Lijst met query-ID's weergeven, het SQL-queryplan voor een bepaalde plan-ID opvragen, queryplannen en uitvoeringsstatus opvragen, statistieken van rapporten, statistieken weergeven en lijst met duur query's maken |
| **Implementatieoptie**              | Cloudimplementatie: heeft gevolgen voor door Microsoft beheerde productieomgevingen en Tier 2 tot en met Tier 5-sandboxomgevingen. |
| **Status**                         | Verwijderd |

### <a name="azure-sql-actions-in-lcs"></a>SQL-acties voor Azure in LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Sommige SQL-acties in LCS worden afgeschaft. Alle activiteiten en monitoring worden intern uitgevoerd door het platform via automatisering. Er is geen handmatige tussenkomst nodig. |
| **Vervangen door een andere functie?**   | Ja, er is nu een geautomatiseerd systeem, die deze mogelijkheden overbodig maken. |
| **Betrokken productgebieden**         | SQL-acties: een planningshandleiding maken om Plan-ID af te dwingen, Een planhandleiding maken om tabelin hints toe te voegen, Planhandleiding verwijderen, paginavergrendelingen uitschakelen/inschakelen en escalatie vergrendelen, Statistieken van een tabel bijwerken, Index opnieuw maken, Index maken |
| **Implementatieoptie**              | Cloudimplementatie: heeft gevolgen voor door Microsoft beheerde productieomgevingen en Tier 2 tot en met Tier 5-sandboxomgevingen. |
| **Status**                         | Verwijderd |


## <a name="feature-deprecation-effective-october-2021"></a>Functie is afgeschaft in oktober 2021

### <a name="show-related-document-attachments-feature"></a>Functie 'Gerelateerde documentbijlagen tonen'

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De functie retourneerde onverwachte resultaten. |
| **Vervangen door een andere functie?**   | Nee. Verdere plannen met betrekking tot deze functionaliteit worden doorgegeven via het openbaarmakingsproces van onze standaard releasewave. |
| **Betrokken productgebieden**         | Webclient - Voorziening voor documentbijlagen |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.23 van apps voor financiën en bedrijfsactiviteiten

### <a name="ondbsynchronize-event"></a>Gebeurtenis OnDBSynchronize

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Er is geen besturingselement om deze gebeurtenis uit te voeren. |
| **Vervangen door een andere functie?**   | Ja, verplaats bestaande methoden waarop de gebeurtenis **OnDBSynchronize** is gegrondvest, naar een uitgebreide SysSetup-klasse. |
| **Betrokken productgebieden**         | Databasesynchronisatie |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft. De geplande verwijderingsdatum is in oktober 2022. |


### <a name="systemnotificationsmanageraddnotification-api"></a>API SystemNotificationsManager.AddNotification

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Microsoft heeft extra parameters nodig bij het toevoegen van meldingen. |
| **Vervangen door een andere functie?**   | Ja, de API **SystemNotificationsManager.AddSystemNotification()**. Voor deze API moet u ExpirationDateTime en RuleID expliciet instellen voor gegenereerde meldingen. |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft. De geplande verwijderingsdatum is in april 2023. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.21 van apps voor financiën en bedrijfsactiviteiten

### <a name="skype-for-business-online-support"></a>Online ondersteuning voor Skype voor Bedrijven

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Skype voor Bedrijven Online is buiten gebruik gesteld. Zie [De service Skype voor Bedrijven Online is buiten gebruik gesteld](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601) voor meer informatie. |
| **Vervangen door een andere functie?**   | We overwegen de mogelijk om in de toekomst Teams toe te voegen.|
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft. De instelling **Skype is ingeschakeld** is uitgeschakeld vanaf versie 10.0.21. Het verwijderen van deze instelling is gepland voor april 2022. De functie werkt echter niet meer nadat het Skype-team de service stopt. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Kennisgeving van afschaffing van functie met ingang van augustus 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL-rapporten in Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Alle activiteiten en monitoring worden intern uitgevoerd door het platform via automatisering. Er is geen handmatige tussenkomst nodig.|
| **Vervangen door een andere functie?**   | Ja, er is nu een geautomatiseerd systeem, die deze mogelijkheden overbodig maken. |
| **Betrokken productgebieden**         | SQL-rapporten: Huidige DTU, huidige DTU-details, Vergrendelingsdetails weergeven, Lijst met huidige planhandleiding, Lijst met query-ID's weergeven, het SQL-queryplan voor een bepaalde plan-ID opvragen, queryplannen en uitvoeringsstatus opvragen, statistieken van rapporten, statistieken weergeven en lijst met duur query's maken |
| **Implementatieoptie**              | Cloudimplementatie: heeft gevolgen voor door Microsoft beheerde productieomgevingen en Tier 2 tot en met Tier 5-sandboxomgevingen. |
| **Status**                         | Afgeschaft: de geplande verwijderingsdatum is in oktober 2021. |

### <a name="azure-sql-actions-in-lcs"></a>SQL-acties voor Azure in LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Sommige SQL-acties in LCS worden afgeschaft. Alle activiteiten en monitoring worden intern uitgevoerd door het platform via automatisering. Er is geen handmatige tussenkomst nodig. |
| **Vervangen door een andere functie?**   | Ja, er is nu een geautomatiseerd systeem, die deze mogelijkheden overbodig maken. |
| **Betrokken productgebieden**         | SQL-acties: een planningshandleiding maken om Plan-ID af te dwingen, Een planhandleiding maken om tabelin hints toe te voegen, Planhandleiding verwijderen, paginavergrendelingen uitschakelen/inschakelen en escalatie vergrendelen, Statistieken van een tabel bijwerken, Index opnieuw maken, Index maken |
| **Implementatieoptie**              | Cloudimplementatie: heeft gevolgen voor door Microsoft beheerde productieomgevingen en Tier 2 tot en met Tier 5-sandboxomgevingen. |
| **Status**                         | Afgeschaft: de geplande verwijderingsdatum is in oktober 2021. |

## <a name="feature-deprecation-effective-may-2021"></a>Kennisgeving van afschaffing van functie met ingang van mei 2021

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Globalisatie-portal in Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De Globalisatie-portal in LCS wordt afgeschaft, aangezien deze functie is vervangen door andere services die op LCS zijn gebaseerd. |
| **Vervangen door een andere functie?**   | Ja, deze functie wordt vervangen door [Problemen zoeken in LCS](../lifecycle-services/issue-search-lcs.md) en de [Dynamics-service voor het indienen van wettelijke waarschuwingen](../lcs-solutions/submit-localization-alerts.md). |
| **Betrokken productgebieden**         | Globalisatie-portal in LCS|
| **Implementatieoptie**              | Cloudimplementatie |
| **Status**                         | Afgeschaft: de geplande verwijderingsdatum is in mei 2022. |


## <a name="feature-removed-effective-january-28-2021"></a>Functie verwijderd met ingang van 28 januari 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Batchtaak voor het verwerken van defragmentatie SQL-index

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Deze functie is verwijderd om de overhead van het bedienen, controleren en onderhouden van het indexbeheer door klanten te verminderen. |
| **Vervangen door een andere functie?**   | In de toekomst wordt het indexonderhoud uitgevoerd door Microsoft-services. Dit proces vindt doorlopend plaats zonder dat dit van invloed is op de werkbelasting van de gebruiker. |
| **Betrokken productgebieden**         | Apps voor financiële en bedrijfsactiviteiten|
| **Implementatieoptie**              | Cloudimplementatie: heeft gevolgen voor door Microsoft beheerde productieomgevingen en Tier 2 tot en met Tier 5-sandboxomgevingen. |
| **Status**                         | Deze functie wordt verwijderd. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.17 van apps voor financiën en bedrijfsactiviteiten


### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Ter ondersteuning van de meest recente versies van Visual Studio moeten enkele wijzigingen worden aangebracht in de X++-extensies voor Visual Studio. Deze wijzigingen zijn niet compatibel met Visual Studio 2015. |
| **Vervangen door een andere functie?**   | Visual Studio 2017 vervangt Visual Studio 2015 als de geïmplementeerde en vereiste versie. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: bij het bijwerken worden de vorige X++-hulpprogramma's verwijderd uit Visual Studio 2015, en worden de bijgewerkte hulpprogramma's niet geïnstalleerd in Visual Studio 2015. Dit heeft geen invloed op gehoste builds. Voor het bouwen van virtuele machines moet de buildpijplijn (builddefinitie) handmatig worden bijgewerkt om de afhankelijkheid van MSBuild 14.0 (Visual Studio 2015) te wijzigen in MSBuild 15.0 (Visual Studio 2017), zoals beschreven in [Een oudere pijplijn bijwerken in Azure Pipelines](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Gebruikersavatar 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De gebruikersavatar die aan de rechterkant van de navigatiebalk wordt weergegeven, is opgehaald met een API uit het Dynamics 365-koptekstbesturingselement en die is afgeschaft. |
| **Vervangen door een andere functie?**   | Gebruikers zien in plaats daarvan hun initialen in een cirkel op de navigatiebalk. Dit is dezelfde visuele weergave die momenteel op ontwikkelapparaten wordt gebruikt. |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alles |
| **Status**                         | Verwijderd vanaf versie 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Afschaffing van Enterprise Portal (EP)  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De metagegevensartefacten die aan Dynamics AX 2012 Enterprise Portal (EP) zijn gekoppeld, zijn afgeschaft, omdat EP nooit in de apps voor financiën en bedrijfsactiviteiten werd ondersteund. |
| **Vervangen door een andere functie?**   | Nr. |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: alle EP-code moet worden verwijderd in de versie van oktober 2021. |

## <a name="deprecation-effective-december-2020"></a>Afschaffing met ingang van december 2020

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-ondersteuning voor Dynamics 365 is afgeschaft

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met ingang van december 2020 wordt Microsoft Internet Explorer 11-ondersteuning voor alle Dynamics 365-producten en Dynamics Lifecycle Services (LCS) afgeschaft en wordt Internet Explorer 11 na augustus 2021 niet meer ondersteund.<br><br>Dit heeft invloed op klanten die Dynamics 365-producten en LCS gebruiken die zijn ontworpen om via een Internet Explorer 11-interface te worden gebruikt. Na augustus 2021 wordt Internet Explorer 11 niet ondersteund voor dergelijke Dynamics 365-producten en LCS. |
| **Vervangen door een andere functie?**   | Wij raden klanten aan om overstappen op Microsoft Edge.|
| **Betrokken productgebieden**         | Alle Dynamics 365-producten en LCS |
| **Implementatieoptie**              | Alle|
| **Status**                         | Afgeschaft: Internet Explorer 11 wordt na augustus 2021 niet ondersteund.|

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.15 van apps voor financiën en bedrijfsactiviteiten

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio-invoegtoepassing voor het toepassen van hotfixes voor metagegevens

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Hotfixes voor metagegevens worden niet meer ondersteund met de updates van de [One Version](../../fin-ops/get-started/one-version.md)-service die zijn geïntroduceerd in juli 2018 en versie 8.1. |
| **Vervangen door een andere functie?**   | Er zijn geen afzonderlijke hotfixes voor metagegevens beschikbaar voor ondersteunde versies. In plaats hiervan worden cumulatieve kwaliteitsupdates toegepast. |
| **Betrokken productgebieden**         | Visual Studio-invoegtoepassingen |
| **Implementatieoptie**              | Virtuele machines voor ontwikkeling |
| **Status**                         | Met versie 10.0.15 wordt de invoegtoepassing niet meer in de Visual Studio-hulpprogramma's opgenomen. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.14 van apps voor financiën en bedrijfsactiviteiten

### <a name="online-users-page"></a>Online gebruikers (pagina) 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dit is een verouderde pagina die is gemaakt voor de vorige client/serverarchitectuur. De informatie op deze pagina is niet altijd nauwkeurig, wat verwarrend en misleidend kan zijn. |
| **Vervangen door een andere functie?**   | In een toekomstige update wordt een nieuwe pagina geleverd.|
| **Betrokken productgebieden**         | Systeembeheer |
| **Implementatieoptie**              | Alles |
| **Status**                         | In oktober 2021 wordt dit formulier verwijderd.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.13 van apps voor financiën en bedrijfsactiviteiten


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Aangepaste code gedefinieerd in SSRS-rapporteigenschappen 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | In het algemeen biedt aangepaste code beperkte voordelen, terwijl er tegelijkertijd aanzienlijke resources en berekeningen nodig zijn. Aangepaste code wordt voornamelijk gebruikt door rapportauteurs om openbare methoden aan te roepen vanuit aangepaste code-assembly's. De cloudservice biedt echter geen ondersteuning voor verwijzingen naar aangepaste assembly's voor SSRS-rapporten. |
| **Vervangen door een andere functie?**   | Rapportauteurs kunnen ervoor kiezen om door te gaan met het verwijzen naar openbare .NET API's voor wiskundige, conversie- en opmaakbewerkingen van willekeurige tekstvakexpressies. Zie [Code toevoegen aan een rapport (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs) voor meer informatie.  |
| **Betrokken productgebieden**         | Subset van ontwerpen voor toepassingsrapporten die in RDL zijn gedefinieerd en aangepaste code bevatten. |
| **Implementatieoptie**              | Alles |
| **Status**                         | Met versie 10.0.13 wordt door de compiler een waarschuwing gegeven voor gevallen waarin aangepaste code wordt aangetroffen in een SSRS-rapportdefinitie. U kunt het probleem oplossen door de ontwerpdefinitie van het rapport te openen en alle aangepaste code te verwijderen. Deze waarschuwing wordt vervangen door een compilerfout in een toekomstige update.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Upgrade van drie jQuery-componentbibliotheken 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Er worden drie jQuery-componentbibliotheken bijgewerkt voor beveiligingscorrecties en voor het onderhouden van de valuta.   
| **Vervangen door een andere functie?**   | Dit betreft de volgende bibliotheken: jQuery (naar versie 3.5.0 van versie 2.1.4), jQuery UI (naar versie 1.12.1 van versie 1.11.4), jQuery qTip (naar versie 3.0.3 van 2.2.1). De migratierichtlijnen zijn online beschikbaar via jQuery.  |
| **Betrokken productgebieden**         | Uitbreidbare besturingselementen, specifiek aangepaste JavaScript-code voor het gebruik van afgeschafte of verwijderde API's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Met versie 10.0.13/Platform update 37 kunnen klanten optioneel overstappen op de meest recente bibliotheken door de functie 'Drie jQuery-componentbibliotheken bijwerken' in te schakelen. Het overstappen op de nieuwe bibliotheken is verplicht met de release van april 2021 zodat er tijd is voor de migratie van de betrokken API's.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Bestaand rasterbesturingselement/forceLegacyGrid() API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het bestaande rasterbesturingselement wordt vervangen door het nieuwe rasterbesturingselement. |
| **Vervangen door een andere functie?**   | Het [nieuwe rasterbesturingselement](../..//fin-ops/get-started/grid-capabilities.md) |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | In versie 10.0.13 is het nieuwe rasterbesturingselement doorgaans beschikbaar en kunnen klanten deze functie eventueel inschakelen. Het nieuwe rasterbesturingselement wordt standaard gebruikt voor de versie van oktober 2021 en wordt naar verwachting verplicht in april 2022. Wanneer het nieuwe rasterbesturingselement verplicht wordt, wordt de **forceLegacyGrid()** API niet meer ondersteund. |

### <a name="personalization-without-saved-views"></a>Persoonlijke instellingen zonder opgeslagen weergaven 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het personalisatiesubsysteem is opnieuw ontworpen met de functie Opgeslagen weergaven, zodat de prestaties beter zijn en er extra mogelijkheden zijn. |
| **Vervangen door een andere functie?**   | Opgeslagen weergaven |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | In versie 10.0.13/platformupdate 37 is de functie Opgeslagen weergaven algemeen beschikbaar en kunnen klanten deze functie desgewenst inschakelen. De functie Opgeslagen weergaven wordt verplicht in de release van oktober 2021. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.12 van apps voor financiën en bedrijfsactiviteiten

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Formulieruitbreidingen voor raster- of groepsbesturingselementen met ongeldige veldverwijzingen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De gegevensgroepeigenschap voor raster- of groepsbesturingselementen wordt gebruikt om automatisch alle velden van een veldgroep weer te geven. Een raster- of groepsbesturingselement dat door een uitbreiding wordt toegevoegd, kan velden bevatten die niet meer in de veldgroep zijn gedefinieerd of er kunnen velden ontbreken die zijn gedefinieerd voor de veldgroep. Dit kan inconsistent gedrag veroorzaken tijdens runtime. Platformupdates voor versie 10.0.12 van apps voor financiën en bedrijfsactiviteiten categoriseren dit probleem nu als een *waarschuwing*. U kunt dit probleem oplossen door de formulierextensie te openen en op te slaan.
| **Vervangen door een andere functie?**   | Deze compilerwaarschuwing wordt vervangen door een compilerfout in een toekomstige update. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Een compilerwaarschuwing wordt geïntroduceerd in platformupdates voor versie 10.0.12 van apps voor financiën en bedrijfsactiviteiten. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Platformupdates voor versie 10.0.11 van apps voor financiën en bedrijfsactiviteiten

### <a name="explicit-safe-lists-for-self-service-environments"></a>Expliciete veilige lijsten voor selfservice-omgevingen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het proces voor het verplaatsen van IP naar veilige lijsten is gewijzigd. Selfservice biedt geen ondersteuning meer voor veilig IP-lijsten. |
| **Vervangen door een andere functie?**   | Zie [Voorwaardelijke toegang voor Azure Active Directory configureren](/appcenter/general/configuring-aad-conditional-access) voor meer informatie.|
| **Betrokken productgebieden**         | Beveiliging |
| **Implementatieoptie**              | Cloud |
| **Status**                         | Afgeschaft: deze functie is volledig afgeschaft voor selfservice-implementaties. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Ter ondersteuning van de meest recente versies van Visual Studio moeten enkele wijzigingen worden aangebracht in de X++-extensies voor Visual Studio. Deze wijzigingen zijn niet compatibel met Visual Studio 2015. |
| **Vervangen door een andere functie?**   | Visual Studio 2017 vervangt Visual Studio 2015 als de geïmplementeerde en vereiste versie. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alles |
| **Status**                         | Virtuele machines die zijn geïmplementeerd op versie 10.0.13 (Platformupdate 37) of hoger bevatten Visual Studio 2017. Versie 10.0.16 (Olatformupdate 40) is de laatste versie met ondersteuning voor Visual Studio 2015. Virtuele machines met alleen Visual Studio 2015 kunnen niet worden bijgewerkt naar versie 10.0.17 (Platformupdate 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Veldgroepen die ongeldige veldverwijzingen bevatten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Veldgroepen in metagegevensdefinities van tabellen kunnen veldverwijzingen bevatten die niet geldig zijn. Als deze veldgroepen worden geïmplementeerd, kan dit runtime-fouten veroorzaken in Financial Reporting en Microsoft SQL Server Reporting Services (SSRS). Platform update 23 heeft een *compilerwaarschuwing* geïntroduceerd waardoor dit metagegevensprobleem wordt opgelost. Platformupdates voor versie 10.0.11 van apps voor financiën en bedrijfsactiviteiten categoriseren dit probleem nu als een *fout*.<p>Volg deze stappen om dit probleem op te lossen.</p><ol><li>Verwijder de ongeldige veldverwijzing uit de groepsdefinitie van het tabelveld.</li><li>Compileer opnieuw.</li><li>Controleer of er fouten zijn opgelost.</li></ol> |
| **Vervangen door een andere functie?**   | Deze compilerfout vervangt permanent de compilerwaarschuwing.  |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: de compilerwaarschuwing is een compilatiefout in platformupdates voor versie 10.0.11 van apps voor financiën en bedrijfsactiviteiten. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-licenties die zijn gemaakt met het SHA1-hashalgoritme

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het proces voor het maken van ISV-licenties (Independent Software Vendor) is gewijzigd. Zie [Licenties voor onafhankelijke softwareleveranciers (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes) voor meer informatie. |
| **Vervangen door een andere functie?**   | Ja. Gebruik Windows PowerShell om licenties te maken. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: ISV-licenties die zijn gemaakt met het SHA1-hashalgoritme. Dit algoritme is afhankelijk van certificaten die zijn gemaakt met het hulpprogramma MakeCert en dit hulpprogramma is afgeschaft.<br><br>Afgeschaft: het gebruik van SHA1 voor beveiligings- of hashingdoeleinden. SHA1 wordt begin 2021 afgeschaft. Daarom moet het niet meer worden gebruikt.<br><br>Verwijderd: ondersteuning voor binnenkomende of uitgaande aanvragen van Transport Layer Security (TLS) 1.0 en TLS 1.1. |

## <a name="platform-update-32"></a>Platformupdate 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialoogvenster Wijziging in werkstroom aanvragen bevat niet langer een vervolgkeuzelijst voor gebruikersselectie

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dit was een beveiligingsprobleem omdat de aanvraag voor wijziging naar een onbedoelde gebruiker kon worden verzonden. Dit was ook een bruikbaarheidsprobleem omdat de gebruiker werd gedwongen te bepalen bij wie de werkstroom oorspronkelijk vandaan kwam en deze handmatig te selecteren.  |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Werkstroom |
| **Implementatieoptie**              | Alle |
| **Status**                         | De vervolgkeuzelijst voor gebruikersselectie werd in Platform update 32 verwijderd uit het dialoogvenster Wijziging in werkstroom aanvragen. Aanvragen voor verzoeken om wijzigingen worden automatisch naar de persoon verzonden bij wie de werkstroom oorspronkelijk vandaan kwam, zoals bedoeld. Zie [Acties in goedkeuringsprocessen voor werkstroom](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change) voor meer informatie over deze functionaliteit. |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Ingesloten drillthrough-koppelingen worden niet meer ondersteund in gepagineerde documenten die worden weergegeven door de cloudgehoste service 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Navigatie-URL's die zijn ingesloten in documenten die door de service worden weergegeven, kunnen gevoelige bedrijfsgegevens bevatten. De ondersteuning voor ingesloten drillthrough-koppelingen in documenten wordt verwijderd als een beveiligingsmaatregel om de gegevens van klanten beter te beschermen. Gebruikers profiteren ook van betere prestaties en kunnen interactief documenten genereren als gevolg van deze wijziging.  |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Rapportage |
| **Implementatieoptie**              | Alle |
| **Status**                         | Deze functie wordt actief uit de service verwijderd.<br><br>De moderne client biedt talloze opties voor het produceren van weergaven die automatisch gegenereerde koppelingen bevatten om te helpen bij het navigeren door de toepassing. Gepagineerde documenten die door de service worden weergegeven, worden aanbevolen voor externe communicatie die per e-mail wordt verzonden, gearchiveerd en afgedrukt voor ontvangers. We hebben de ervaring verbeterd voor het direct bekijken van documenten in de browser, die rechtstreeks toegang biedt tot lokale printers. Zie [PDF-documenten bekijken met een ingesloten viewer](../analytics/preview-pdf-documents.md) voor meer informatie. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies
Zie [Verwijderde of afgeschafte functies in eerdere versies](../migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
