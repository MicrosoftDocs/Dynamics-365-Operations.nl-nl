---
title: Verwijderde of afgeschafte functies in Dynamics 365 Commerce
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.
author: josaw
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b582b8b95fcf2ad45aa1bb49eb5594d30874e0f4
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559554"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Verwijderde of afgeschafte functies in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

> [!NOTE]
> Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](/dynamics/s-e/). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Verwijderde of verouderde functies in versie 10.0.21 van Commerce

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Instelling voor het verwerken van overlappende kortingen in Commerce-parameters

De instelling **Verwerking van overlappende kortingen** op de pagina **Commerce-parameters** is afgeschaft in de Commerce-versie 10.0.21. In de toekomst gebruikt de Commerce-prijsengine één algoritme om de optimale combinatie van overlappende kortingen te bepalen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | <p>De instelling **Verwerking van overlappende kortingen** in de Commerce-parameters bepaalt hoe de Commerce-prijsengine zoekt en de optimale combinatie van overlappende kortingen bepaalt. De instelling biedt momenteel drie opties:<p><ul><li> **Beste prestaties** – Met deze optie wordt een geavanceerd heuristiek algoritme en een [marginale-waardeclassificatie](../optimal-combination-overlapping-discounts.md) gebruikt om de prioriteit te bepalen, te evalueren en tijdig de beste kortingscombinatie te bepalen.</li><li>**Vereffende berekening** – In de huidige codebasis werkt deze optie op dezelfde manier als de optie **Beste prestaties**. Daarom is het in wezen een gedupliceerde optie.</li><li>**Volledige berekening**: deze optie maakt gebruik van een oud algoritme die alle mogelijke kortingscombinaties doorloopt tijdens de prijsberekening. Voor orders met grote regels en hoeveelheden kan deze optie prestatieproblemen veroorzaken.</li></ul><p>Om de configuratie te vereenvoudigen, de prestaties te verbeteren en incidenten te verminderen die worden veroorzaakt door het oude algoritme, verwijderen we de instelling **Verwerking van overlappende kortingen** volledig en werken we de interne logica van de Commerce-prijsengine bij zodat nu alleen het geavanceerde algoritme wordt gebruikt (dat wil zeggen, het algoritme achter de optie **Beste prestaties**).</p> |
| **Vervangen door een andere functie?**   | Nee. Organisaties die de optie **Vereffende berekening** of **Volledige berekening** gebruiken, wordt aangeraden om over te schakelen op de optie **Beste prestaties** voordat deze functie wordt verwijderd. |
| **Betrokken productgebieden**         | Prijzen en kortingen |
| **Implementatieoptie**              | Alle |
| **Status**                         | Vanaf release 10.0.21 in oktober 2022 wordt de instelling **Verwerking van overlappende kortingen** verwijderd uit de Commerce-parameters. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Retail SDK gedistribueerd met behulp van Lifecycle Services

De Retail SDK wordt gedistribueerd in Lifecycle Services (LCS). Deze distributiemodus is afgeschaft in versie 10.0.21. In de toekomst worden Retail SDK-referentiepakketten, bibliotheken en voorbeelden gepubliceerd in openbare registers op GitHub.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De Retail SDK wordt in LCS gedistribueerd. Het LCS-proces neemt een paar uur in beslag en het proces moet voor elke update worden herhaald. In de toekomst worden Retail SDK-referentiepakketten, bibliotheken en voorbeelden gepubliceerd in openbare registers op GitHub. Extensievoorbeelden en referentiepakketten kunnen eenvoudig worden verbruikt en de updates nemen enkele minuten in beslag. |
| **Vervangen door een andere functie?**   |  [Retail SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Betrokken productgebieden**         | Retail-SDK |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: de SDK die gedistribueerd wordt via de LCS VMs, wordt in oktober 2022 verwijderd vanaf versie 10.0.21. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Implementeerbare pakketten voor de detailhandel en gecombineerde installatieprogramma's voor POS, Hardware Station en Cloud Scale Unit

Implementeerbare pakketten voor de detailhandel die gegenereerd zijn met de Retail SDK MSBuild, worden in versie 10.0.21 afgeschaft. Gebruik in de toekomst het CSU-pakket (Cloud Scale Unit) voor Cloud Scale Unit-extensies (Commerce Runtime, kanaaldatabase, API's voor headless commerce, betalingen en Cloud Point of Sale (POS)) Gebruik installatieprogramma's die speciaal bedoeld zijn voor extensies voor POS, Hardware Station en Cloud scale unit die als host worden gebruikt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Een implementeerbaar retailpakket is een gecombineerd pakket dat uit een complete set extensiepakketten en installatieprogramma's bestaat. Dit gecombineerde pakket maakt de implementatie complex, omdat CSU-extensies naar Cloud Scale Unit gaan en installatieprogramma's in winkels worden geïmplementeerd. De installatieprogramma's bevatten het extensie- en basisproduct, wat de updates lastig maakt. Bij elke upgrade is codesamenvoeging en pakketgeneratie vereist. Om dit proces te vereenvoudigen, worden de extensiepakketten nu opgesplitst in onderdelen voor eenvoudige implementatie en beheer. Bij de nieuwe benadering worden extensies en installieprogramma's van elkaar gescheiden en kunnen ze onafhankelijk worden gebruikt en bijgewerkt zonder samenvoegcode of zonder ze opnieuw als pakket te verpakken.|
| **Vervangen door een andere functie?**   | CSU-extensies, installatieprogramma's voor POS-extensies, installatieprogramma's voor Hardware Station-extensies |
| **Betrokken productgebieden**         | Dynamics 365 Commerce-extensie en implementatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: vanaf versie 10.0.21 wordt de ondersteuning voor de implementatie van RetailDeployablePackage in LCS in oktober 2022 verwijderd. |

Ga voor meer informatie naar:

+ [Een afzonderlijk pakket genereren voor CSU (Commerce Cloud Scale Unit)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Een Modern POS-uitbreidingspakket maken](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [POS integreren met een nieuw hardwareapparaat](../dev-itpro/hardware-device-extension.md)
+ Codevoorbeelden
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU en Hardware station](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln en cloudPOs.sln in de Retail SDK

Ontwikkeling van POS-extensie met behulp van ModernPos.sln, CloudPOs.sln, POS.Extension.csproj en de POS-map is afgeschaft in versie 10.0.21. Gebruik in de toekomst de POS-onafhankelijke verpakking SDK voor POS-extensies.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | In eerdere versies van de Retail SDK is er voor het bijwerken naar de laatste versie van het POS, als er POS-extensies zijn, een code nodig die samenvoegt en opnieuw verpakt. Het code samenvoegen was een tijdrovend upgradeproces en u moest de volledige Retail SDK goed onderhouden. U moest ook het basis-POS. App-project compileren. Door het onafhankelijke verpakkingsmodel te gebruiken, moet u alleen uw extensie onderhouden. Het bijwerken naar de laatste versie van de POS-extensies is net zo eenvoudig als het bijwerken van de versie van het NuGet-pakket dat uw project verbruikt. Extensies kunnen onafhankelijk worden geïmplementeerd en de services gebruiken de installatieprogramma's voor extensies. De basis-POS kan afzonderlijk worden geïmplementeerd en onderhouden. Er is geen code voor samenvoeging of opnieuw verpakken nodig voor het basisprogramma of de code. |
| **Vervangen door een andere functie?**   | [POS-onafhankelijke verpakking SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Betrokken productgebieden**         | Dynamics 365 Commerce POS-extensie en implementatie |
| **Implementatieoptie**              | Alles |
| **Status**                         | Afgeschaft: vanaf versie 10.0.21 wordt de ondersteuning voor gecombineerde POS-pakketten en het extensiemodel dat gebruikmaakt van de ModernPos.Sln, cloudPOs.sln en POS.Extensons.csproj in Retail SDK in oktober 2022 verwijderd. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Verwijderde of verouderde functies in versie 10.0.17 van Commerce

### <a name="full-dataset-generation-interval-is-deprecated"></a>Interval voor genereren van volledige gegevensset wordt afgeschaft

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Vanaf deze versie is het veld **Interval voor genereren van volledige gegevensset in dagen** in het formulier **Parameters voor handelplanner** in Dynamics 365 Headquarters afgeschaft. In deze versie is het veld ook niet meer zichtbaar, zodat de waarde niet kan worden bewerkt. De waarde blijft **0**. |
| **Vervangen door een andere functie?**   | No |
| **Betrokken productgebieden**         | Dynamics 365 Commerce |
| **Implementatieoptie**              | Alles|
| **Status**                         | Afgeschaft. Gebruik dit veld niet of wijzig de waarde niet.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Verwijderde of verouderde functies in versie 10.0.15 van Commerce

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-ondersteuning voor Dynamics 365 is afgeschaft

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met ingang van december 2020 wordt Microsoft Internet Explorer 11-ondersteuning voor alle Dynamics 365-producten afgeschaft en wordt Internet Explorer 11 na augustus 2021 niet meer ondersteund.<br><br>Dit heeft invloed op klanten die Dynamics 365-producten gebruiken die zijn ontworpen om via een Internet Explorer 11-interface te worden gebruikt. Na augustus 2021 wordt Internet Explorer 11 niet ondersteund voor dergelijke Dynamics 365-producten. |
| **Vervangen door een andere functie?**   | Wij raden klanten aan om overstappen op Microsoft Edge.|
| **Betrokken productgebieden**         | Alle Dynamics 365-producten |
| **Implementatieoptie**              | Alle|
| **Status**                         | Afgeschaft. Internet Explorer 11 wordt na augustus 2021 niet meer ondersteund.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Verwijderde of verouderde functies in versie 10.0.11 van Commerce
### <a name="data-action-hooks"></a>Gegevensactie-hooks
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De functie Gegevensactie-hooks is afgeschaft vanwege prestatieproblemen. |
| **Vervangen door een andere functie?**   | U wordt aangeraden [gegevensacties te overschrijven](../e-commerce-extensibility/data-action-overrides.md) om bedrijfslogica in de gegevensactielaag te wijzigen.|
| **Betrokken productgebieden**         | Uitbreidbaarheid van gegevensacties in e-Commerce |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf versie 10.0.11. |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Ondersteuning van Retail SDK voor Visual Studio 2015, msbuild 14.0 en Retail SDK\naslagbibliotheken en hulpmiddelen
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De ondersteuning voor Retail SDK voor Visual Studio 2015 is afgeschaft en bijgewerkt tot ondersteuning van 2017, msbuild 15.0. Alle naslagbibliotheken en hulpmiddelen voor Commerce-proxygenerator in de map RetailSDK\References zijn verplaatst naar NuGet-pakketten om het uitbreidingsmodel en het SDK-upgradeproces te vereenvoudigen.|
| **Vervangen door een andere functie?**   | We raden u aan de informatie in [De Retail SDK migreren van Visual Studio 2015 naar Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) te volgen om uw systeem bij te werken. |
| **Betrokken productgebieden**         | Retail SDK-extensies |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf versie 10.0.11. |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server Extension met IEdmModelExtender en CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De Retail Server-extensie met IEdmModelExtender en CommerceController is afgeschaft om een vereenvoudigd uitbreidingsmodel te leveren. De nieuwe implementatie bevat alleen de controllerklasse zonder implementatie van een extra IEdmModelExtender-klasse. Hierdoor wordt ook de afhankelijkheid van een bepaalde OData-versie voorkomen (als de OData-versie wordt bijgewerkt, worden de extensies mogelijk uitgeschakeld.) |
| **Vervangen door een andere functie?**   |  We raden u aan om het uitbreidingsmodel voor de IController-klasse te gebruiken door het NuGet-pakket (Microsoft.Dynamics.Commerce.Hosting.Contracts) te importeren. |
| **Betrokken productgebieden**         | Retail Server-extensies |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf versie 10.0.11. |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Hardware Station-extensie met IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Hardware Station-extensie met IHardwareStationController is afgeschaft voor een vereenvoudigd uitbreidingsmodel. De nieuwe implementatie heeft alleen de IController-klasse zonder verdere implementatie van de klasse en om de afhankelijkheid van de kernbibliotheken voor Hardware Stations te voorkomen. Eerdere extensie verwees naar meerdere bibliotheken. |
| **Vervangen door een andere functie?**   | We raden u aan om het uitbreidingsmodel voor de IController-klasse te gebruiken door het NuGet-pakket (Microsoft.Dynamics.Commerce.Hosting.Contracts) te importeren. |
| **Betrokken productgebieden**         | Extensies van Hardware Station |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf versie 10.0.11. |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Verwijderde of verouderde functies in versie 10.0.10 van Commerce
### <a name="pos-operation-803---picking-and-receiving"></a>POS-bewerking 803 - Verzamelen en ontvangen
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De bewerkingen voor orderverzameling en ontvangst zijn verouderd vanwege een nieuwe bewerking. |
| **Vervangen door een andere functie?**   | Ja. Ze worden vervangen door twee nieuwe POS-bewerkingen: inkomende bewerking (804) en uitgaande bewerking (805).|
| **Betrokken productgebieden**         | Verkooppunttoepassing (POS) |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf release 10.0.10 worden voor de bewerking orderverzameling en ontvangst geen functie-updates meer ontvangen. Alleen kritieke fouten worden in toekomstige versies opgelost voor deze bewerking. Alle klanten wordt aangeraden om naar de nieuwe [inkomende bewerkingen](../pos-inbound-inventory-operation.md) en [uitgaande transacties](../pos-outbound-inventory-operation.md) over te stappen, die deel blijven uitmaken van onze productroutekaart voor de lange termijn. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Verwijderde of verouderde functies in versie 10.0.7 van Commerce
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities en GetAvailableInventoryNearby API's
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Nieuwe geoptimaliseerde API's zijn gemaakt ter vervanging van de API's GetProductAvailabilities en GetAvailableInventoryNearby. |
| **Vervangen door een andere functie?**   | Ja: dit wordt vervangen door de API's GetEstimatedAvailability en GetEstimatedproductWarehouseAvailability. |
| **Betrokken productgebieden**         | SDK met e-Commerce-toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf de release 10.0.7 wordt geen technische investering meer gedaan voor GetproductAvailabilities en GetAvailableInventoryNearby. Organisaties die deze API's gebruiken in hun e-Commerce-implementaties, moeten overstappen op de nieuwe API's GetEstimatedAvailability en GetEstimatedproductWarehouseAvailability en de [geoptimaliseerde berekeningsfunctie voor productbeschikbaarheid](../calculated-inventory-retail-channels.md) inschakelen.  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies
Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
