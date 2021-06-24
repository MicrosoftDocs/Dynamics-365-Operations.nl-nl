---
title: Verwijderde of afgeschafte functies in Dynamics 365 Commerce
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.
author: josaw
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f80d1509c7c363e93b83cb47c1b93ab00bf67180
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193463"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Verwijderde of afgeschafte functies in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

> [!NOTE]
> Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](/dynamics/s-e/). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

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
| **Implementatieoptie**              | Alles|
| **Status**                         | Afgeschaft. Internet Explorer 11 wordt na augustus 2021 niet ondersteund.|

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