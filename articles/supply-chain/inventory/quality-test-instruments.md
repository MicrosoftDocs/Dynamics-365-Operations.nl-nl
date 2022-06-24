---
title: Testinstrumenten voor kwaliteitsbeheer
description: In dit artikel wordt beschreven hoe u testinstrumenten maakt die kunnen worden gebruikt voor het testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36b712e6a99a0625af28ef121d0c9c39c1e32603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857658"
---
# <a name="quality-management-test-instruments"></a>Testinstrumenten voor kwaliteitsbeheer

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u testinstrumenten maakt die kunnen worden gebruikt voor het testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.

U gebruikt de pagina **Testinstrumenten** voor het definiëren en weergeven van details over de apparaten die worden gebruikt om kwaliteitsorders te testen. Testinstrumenten zijn optioneel. Ze kunnen kwaliteitsmedewerkers echter wel helpen om erachter te komen welk apparaat of hulpprogramma ze moeten gebruiken om een specifieke test uit te voeren.

## <a name="test-instrument-example"></a>Voorbeeld van testinstrument

U voert verschillende tests uit op elektrische onderdelen. Sommige tests zijn bedoeld om het voltage van de onderdelen te testen, één test is er om de temperatuur te testen en één test is er om hun gewicht te testen. Er worden verschillende hulpmiddelen, apparaten of apparatuur gebruikt om elke test uit te voeren. Een voltmeter wordt bijvoorbeeld gebruikt om het voltage te meten, een thermometer wordt gebruikt om de temperatuur te meten en een weegschaal wordt gebruikt om het gewicht te meten. U kunt elk van deze apparaten configureren als een testinstrument en de maateenheid aangeven waarin de testresultaten moeten worden vastgelegd. Resultaten van de voltmeter worden bijvoorbeeld vastgelegd in volt, resultaten van de thermometer worden vastgelegd in graden Fahrenheit of Celsius en de resultaten van de weegschaal worden vastgelegd in ponden of kilogrammen.

## <a name="create-a-test-instrument"></a>Een testinstrument maken

1. Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Testinstrumenten**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Testinstrument**: voer een unieke id of naam voor het testinstrument in.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor het testinstrument in.
    - **Eenheid**: selecteer de eenheid waarin het instrument de resultaten meet. Het veld **Precisie** wordt automatisch ingesteld op basis van de eenheid die u selecteert.

1. Sluit de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Kwaliteitsbeheertests](quality-tests.md)
- [Testgroepen voor kwaliteitsbeheer](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
