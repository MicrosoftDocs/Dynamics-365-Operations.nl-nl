---
title: Demogegevens voor productaanbevelingen voor meerdere kanalen
description: Dit document biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872321"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Demogegevens voor productaanbevelingen voor meerdere kanalen

Dit document biedt richtlijnen over het gebruik van productaanbevelingen voor meerdere kanalen in Tier 1-omgevingen met een enkel systeem via vooraf ingevulde, aanpasbare demogegevens.

Productaanbevelingen voor meerdere kanalen bieden een reeks redactioneel samengestelde of door het programma gegenereerde, geordende lijsten met producten. Deze lijsten kunnen worden gebruikt in verschillende scenario's, afhankelijk van de zakelijke behoefte. Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](../commerce/product-recommendations.md).

Productaanbevelingen voor Dynamics-omgevingen van Tier 2 en hoger worden automatisch berekend op basis van klantgegevens.
Door het gebruik van demogegevens voor productaanbevelingen worden geen productaanbevelingen uitgeschakeld die al in de omgeving zijn ingericht, en er zijn geen kosten verbonden aan het gebruik.

Voor Tier 1-omgevingen zijn productaanbevelingen alleen gebaseerd op de statische demogegevens die zijn opgeslagen in een CSV-bestand.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Demogegevens voor productaanbevelingen inschakelen in een omgeving

Klanten moeten de **demo-uitbreiding voor Dynamics 365 Commerce-preview** implementeren in de respectievelijke omgeving, waarmee automatisch demogegevens voor productaanbevelingen worden ingeschakeld.

## <a name="default-demo-data"></a>Standaard demogegevens
Elke omgeving van het Onebox-type bevat een vooraf geladen set met productaanbevelingen die zijn opgeslagen in het bestand met door komma's gescheiden waarden **'reco_demo_data. csv'**, dat zich in dezelfde map als dit document bevindt op Retail Server.

Deze gegevens zijn onderverdeeld in de volgende kolommen

| Kolomnaam         | Verplicht          | Beschrijving                                                                                                                                 | Mogelijke waarden                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Het specifieke lijsttype voor productaanbevelingen dat door het demogegevenspunt moet worden gegenereerd.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Het specifieke nummer van de operationele eenheid waar de productaanbevelingen naar verwachting zullen worden opgehaald.                                        |                                                                              |
| Categorie            |                    |    De categorie waarvoor de specifieke lijst moet worden geretourneerd. Als er geen categorie is opgegeven, wordt de lijst alleen boven de navigatiehiërarchie weergegeven.    |                                                                              |
| SeedItemId          |                    |    Voor-lijsten waarvoor Seed (RecoPeopleAlsoBuy en RecoCart) is vereist, moeten in die lijsten extra producten worden weergegeven.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Een of meer producten die als resultaat moeten worden geretourneerd, gescheiden door **';'**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Demogegevens aanpassen
Klanten kunnen de standaard demogegevens bewerken met product- en categoriegegevens die in HQ zijn geconfigureerd. Zodra het CSV-bestand is bijgewerkt, worden de wijzigingen direct doorgevoerd in de productaanbevelingen die aan klanten zijn verstrekt.

De extensie bevat een gegevensbestand met de naam RecoMockDataset.csv waarmee de klant de gegevensset kan beheren die wordt gebruikt om de onechte aanbevelingsgegevens te leveren. De bestandsnaam kan via de extensieconfiguratie worden beheerd met de instelling **ext. Recommendations.DemoFilePath**. Hierdoor kunnen de klanten meerdere gegevenssets beschikbaar hebben waartussen gemakkelijk kan worden omgeschakeld via de configuratie.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van productaanbevelingen](../commerce/product-recommendations.md)

[Omgevingsplanning](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
