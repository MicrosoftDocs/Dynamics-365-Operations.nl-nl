---
title: Verwijderde of afgeschafte Platform-functies
description: In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van Finance and Operations-apps.
author: sericks007
manager: AnnBe
ms.date: 07/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 393349240d16636d3eec747126cc1ee6f6f9998d
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651661"
---
# <a name="removed-or-deprecated-platform-features"></a>Verwijderde of afgeschafte Platform-functies

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd waarvoor de verwijdering is gepland in platformupdates van Finance and Operations-apps.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Platform updates voor versie 10.0.13 van Finance and Operations-apps

> [!NOTE]
> Versie 10.0.13 is een preview-versie. De inhoud en de functies kunnen worden gewijzigd. Meer informatie over preview-versies vindt u in [Beschikbaarheid van serviceupdate](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/public-preview-releases).

### <a name="upgrade-of-three-jquery-component-libraries"></a>Upgrade van drie jQuery-componentbibliotheken 

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Er worden drie jQuery-componentbibliotheken bijgewerkt voor beveiligingscorrecties en voor het onderhouden van de valuta.   
| **Vervangen door een andere functie?**   | Dit betreft de volgende bibliotheken: jQuery (naar versie 3.5.0 van versie 2.1.4), jQuery UI (naar versie 1.12.1 van versie 1.11.4), jQuery qTip (naar versie 3.0.3 van 2.2.1). De migratierichtlijnen zijn online beschikbaar via jQuery.  |
| **Betrokken productgebieden**         | Uitbreidbare besturingselementen, specifiek aangepaste JavaScript-code voor het gebruik van afgeschafte of verwijderde API's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Met versie 10.0.13/Platform update 37 kunnen klanten optioneel overstappen op de meest recente bibliotheken door de functie 'Drie jQuery-componentbibliotheken bijwerken' in te schakelen. Het overstappen op de nieuwe bibliotheken is verplicht met de release van april 2021 zodat er tijd is voor de migratie van de betrokken API's.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Bestaand rasterbesturingselement/forceLegacyGrid() API

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het bestaande rasterbesturingselement wordt vervangen door het nieuwe rasterbesturingselement. |
| **Vervangen door een andere functie?**   | Het [nieuwe rasterbesturingselement](../..//fin-ops/get-started/grid-capabilities.md) |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | In versie 10.0.13 is het nieuwe rasterbesturingselement doorgaans beschikbaar en kunnen klanten deze functie eventueel inschakelen. Het nieuwe rasterbesturingselement wordt verplicht in de release van oktober 2021. Wanneer het nieuwe rasterbesturingselement verplicht wordt, wordt de **forceLegacyGrid()** API niet meer ondersteund. |

### <a name="personalization-without-saved-views"></a>Persoonlijke instellingen zonder opgeslagen weergaven 

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het personalisatiesubsysteem is opnieuw ontworpen met de functie Opgeslagen weergaven, zodat de prestaties beter zijn en er extra mogelijkheden zijn. |
| **Vervangen door een andere functie?**   | Opgeslagen weergaven |
| **Betrokken productgebieden**         | Webclient |
| **Implementatieoptie**              | Alle |
| **Status**                         | In versie 10.0.13/platformupdate 37 is de functie Opgeslagen weergaven algemeen beschikbaar en kunnen klanten deze functie desgewenst inschakelen. De functie Opgeslagen weergaven wordt verplicht in de release van oktober 2021. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Platform updates voor versie 10.0.12 van Finance and Operations-apps

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Formulieruitbreidingen voor raster- of groepsbesturingselementen met ongeldige veldverwijzingen

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De gegevensgroepeigenschap voor raster- of groepsbesturingselementen wordt gebruikt om automatisch alle velden van een veldgroep weer te geven. Een raster- of groepsbesturingselement dat door een uitbreiding wordt toegevoegd, kan velden bevatten die niet meer in de veldgroep zijn gedefinieerd of er kunnen velden ontbreken die zijn gedefinieerd voor de veldgroep. Dit kan inconsistent gedrag veroorzaken tijdens runtime. Platformupdates voor versie 10.0.12 van Finance and Operations-apps categoriseren dit probleem nu als een *waarschuwing*. U kunt dit probleem oplossen door de formulierextensie te openen en op te slaan.
| **Vervangen door een andere functie?**   | Deze compilerwaarschuwing wordt vervangen door een compilerfout in een toekomstige update. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Een compilerwaarschuwing wordt geïntroduceerd in platformupdates voor versie 10.0.12 van Finance and Operations-apps. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Platform updates voor versie 10.0.11 van Finance and Operations-apps

### <a name="explicit-safe-lists-for-self-service-environments"></a>Expliciete veilige lijsten voor selfservice-omgevingen

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het proces voor het verplaatsen van IP naar veilige lijsten is gewijzigd. Selfservice biedt geen ondersteuning meer voor veilig IP-lijsten. |
| **Vervangen door een andere functie?**   | Zie [Voorwaardelijke toegang voor Azure Active Directory configureren](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access) voor meer informatie.|
| **Betrokken productgebieden**         | Beveiliging |
| **Implementatieoptie**              | Cloud |
| **Status**                         | **Afgeschaft:** deze functie is volledig afgeschaft voor selfservice-implementaties. |

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Ter ondersteuning van de meest recente versies van Visual Studio moeten enkele wijzigingen worden aangebracht in de X++-extensies voor Visual Studio. Deze wijzigingen zijn niet compatibel met Visual Studio 2015. |
| **Vervangen door een andere functie?**   | Visual Studio 2017 vervangt Visual Studio 2015 als de geïmplementeerde en vereiste versie. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | Zodra de beschikbaarheid van nieuwe virtuele machines (VM's) met Visual Studio 2017 wordt aangekondigd, moeten bestaande VM's met alleen Visual Studio 2015 opnieuw worden geïmplementeerd via releasewave 1 van 2021. |

### <a name="field-groups-containing-invalid-field-references"></a>Veldgroepen die ongeldige veldverwijzingen bevatten

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Veldgroepen in metagegevensdefinities van tabellen kunnen veldverwijzingen bevatten die niet geldig zijn. Als deze veldgroepen worden geïmplementeerd, kan dit runtime-fouten veroorzaken in Financial Reporting en Microsoft SQL Server Reporting Services (SSRS). Platform update 23 heeft een *compilerwaarschuwing* geïntroduceerd waardoor dit metagegevensprobleem wordt opgelost. Platform updates voor versie 10.0.11 van Finance and Operations-apps categoriseren dit probleem als een *compilerfout*.<p>Volg deze stappen om dit probleem op te lossen.</p><ol><li>Verwijder de ongeldige veldverwijzing uit de groepsdefinitie van het tabelveld.</li><li>Compileer opnieuw.</li><li>Controleer of er fouten zijn opgelost.</li></ol> |
| **Vervangen door een andere functie?**   | Deze compilerfout vervangt permanent de compilerwaarschuwing.  |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | **Afgeschaft**: de compilerwaarschuwing is een compilatiefout in platform updates voor versie 10.0.11 van Finance and Operations-apps. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-licenties die zijn gemaakt met het SHA1-hashalgoritme

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Het proces voor het maken van ISV-licenties (Independent Software Vendor) is gewijzigd. Zie [Licenties voor onafhankelijke softwareleveranciers (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes) voor meer informatie. |
| **Vervangen door een andere functie?**   | Ja. Gebruik Windows PowerShell om licenties te maken. |
| **Betrokken productgebieden**         | Visual Studio-ontwikkelprogramma's |
| **Implementatieoptie**              | Alle |
| **Status**                         | <strong>Afgeschaft:</strong> ISV-licenties die zijn gemaakt met het SHA1-hashalgoritme. Dit algoritme is afhankelijk van certificaten die zijn gemaakt met het hulpprogramma MakeCert en dit hulpprogramma is afgeschaft.<p><strong>Afgeschaft:</strong> het gebruik van SHA1 voor beveiligings- of hashingdoeleinden. SHA1 wordt begin 2021 afgeschaft. Daarom moet het niet meer worden gebruikt.<p><strong>Verwijderd:</strong> ondersteuning voor binnenkomende of uitgaande aanvragen van Transport Layer Security (TLS) 1.0 en TLS 1.1. |

## <a name="platform-update-32"></a>Platformupdate 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialoogvenster Wijziging in werkstroom aanvragen bevat niet langer een vervolgkeuzelijst voor gebruikersselectie
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Dit was een beveiligingsprobleem omdat de aanvraag voor wijziging naar een onbedoelde gebruiker kon worden verzonden. Dit was ook een bruikbaarheidsprobleem omdat de gebruiker werd gedwongen te bepalen bij wie de werkstroom oorspronkelijk vandaan kwam en deze handmatig te selecteren.  |
| **Vervangen door een andere functie?**   | Nee |
| **Betrokken productgebieden**         | Werkstroom |
| **Implementatieoptie**              | Alle |
| **Status**                         | De vervolgkeuzelijst voor gebruikersselectie werd in Platform update 32 verwijderd uit het dialoogvenster Wijziging in werkstroom aanvragen. Aanvragen voor verzoeken om wijzigingen worden automatisch naar de persoon verzonden bij wie de werkstroom oorspronkelijk vandaan kwam, zoals bedoeld. Zie [Acties in goedkeuringsprocessen voor werkstroom](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change) voor meer informatie over deze functionaliteit. |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Ingesloten drillthrough-koppelingen worden niet meer ondersteund in gepagineerde documenten die worden weergegeven door de cloudgehoste service 
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Navigatie-URL's die zijn ingesloten in documenten die door de service worden weergegeven, kunnen gevoelige bedrijfsgegevens bevatten. De ondersteuning voor ingesloten drillthrough-koppelingen in documenten wordt verwijderd als een beveiligingsmaatregel om de gegevens van klanten beter te beschermen. Gebruikers profiteren ook van betere prestaties en kunnen interactief documenten genereren als gevolg van deze wijziging.  |
| **Vervangen door een andere functie?**   | No |
| **Betrokken productgebieden**         | Rapportage |
| **Implementatieoptie**              | Alle |
| **Status**                         | Deze functie wordt actief uit de service verwijderd.<br><br>De moderne client biedt talloze opties voor het produceren van weergaven die automatisch gegenereerde koppelingen bevatten om te helpen bij het navigeren door de toepassing. Gepagineerde documenten die door de service worden weergegeven, worden aanbevolen voor externe communicatie die per e-mail wordt verzonden, gearchiveerd en afgedrukt voor ontvangers. We hebben de ervaring verbeterd voor het direct bekijken van documenten in de browser, die rechtstreeks toegang biedt tot lokale printers. Zie [PDF-documenten bekijken met een ingesloten viewer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents) voor meer informatie. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies
Zie [Verwijderde of afgeschafte functies in eerdere versies](../migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.

