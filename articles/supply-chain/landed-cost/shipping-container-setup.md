---
title: Verzendcontainers
description: In dit onderwerp wordt beschreven hoe u verzendcontainers kunt instellen voor de module Francoprijzen.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c13102ac1c852aabd25c54e4b51d2f14548290a3d6b90090425aa37e5bde110b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727889"
---
# <a name="shipping-container-setup"></a>Verzendingscontainer instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u verzendcontainers kunt instellen voor de module **Francoprijzen**.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Verzendcontainertypen instellen

Met verzendcontainertypen worden de typen containers bepaald die kunnen worden gebruikt tijdens verzending en transport.

Als u wilt werken met de verzendcontainertypen, gaat u naar **Francoprijzen \> Containers instellen \> Verzendcontainertypen**. Hier kunt u records voor uw containertypen weergeven, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Type verzendcontainer | Voer een unieke identificatienaam/-nummer voor het verzendcontainertype in. |
| Beschrijving | Voer een beschrijving van het verzendcontainertype in. |
| Volume | Voer het maximale volume in dat is toegestaan in verzendcontainers van dit type. |
| Gewicht | Voer het maximale gewicht in dat is toegestaan in verzendcontainers van dit type. |
| Retourneerbaar | Geef op of verzendingscontainers van dit type naar de leverancier kunnen worden geretourneerd nadat ze tijdens een levering zijn gebruikt. Als deze optie is ingesteld op *Ja*, zijn er mogelijk extra kosten van toepassing op het retourneren van containers van dit type naar de haven van oorsprong. |

## <a name="set-up-shipping-containers"></a>Verzendcontainers instellen

U gebruikt verzendcontainerrecords om elke container te identificeren die u tijdens het transport gebruikt. Wanneer u een transport maakt, kunt u er een specifieke container voor selecteren in de lijst met alle verzendcontainerrecords die u hier hebt gedefinieerd. Deze functie is vooral nuttig als uw bedrijf eigenaar is van zijn eigen verzendcontainers.

U hoeft geen verzendcontainernummers in te voeren voor verzendcontainers die slechts één keer worden gebruikt. In plaats daarvan kunt u het verzendcontainernummer toevoegen wanneer u een transport maakt.

Verzendcontainerrecords worden alleen gebruikt in Francoprijzen. Ze zijn niet beschikbaar in de standaardmodule **Transportbeheer** (TMS).

Als u wilt werken met verzendcontainers, gaat u naar **Francoprijzen \> Containers instellen \> Verzendcontainers**. Hier kunt u records voor uw verzendcontainers weergeven, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Verzendcontainer | Voer een unieke identificatienaam/-nummer voor de verzendcontainer in. |
| Type verzendcontainer | Selecteer het type verzendcontainer. Zie de sectie [Verzendcontainertypen instellen](#shipping-container-types) eerder in dit onderwerp voor meer informatie. |

> [!NOTE]
> - Het instellen van verzendcontainers is optioneel. Meestal gebruikt u deze alleen als uw bedrijf zelf verzendcontainers in eigendom heeft of vaak dezelfde verzendcontainers gebruikt.
> - Voor het verzenden van verzendcontainernummers worden geen controlecijfers berekend.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Eenheidstypen instellen

Eenheidstypen vormen extra groeperingen en identificatiemethoden voor verzendcontainers. Het eenheidstype wordt meestal gebruikt om het type container aan te geven waarin goederen zijn verpakt, zoals pallets of vaten. U kunt een eenheidstype selecteren wanneer u een container instelt op de pagina **Alle verzendcontainers**.

Eenheidstypen worden alleen gebruikt in Francoprijzen. Ze zijn niet beschikbaar in TMS.

Als u wilt werken met eenheidstypen, gaat u naar **Francoprijzen \> Containers instellen \> Eenheidstypen**. Hier kunt u records voor uw eenheidstypen weergeven, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Eenheidstype | Voer een unieke identificatienaam/-nummer voor het eenheidstype in. |
| Beschrijving | Voer een beschrijving van het eenheidstype in. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Koelingstypen instellen

Koelingstypen vormen extra groeperingen en identificatiemethoden voor verzendcontainers (gewoonlijk koelcontainers). U kunt een koelingstype selecteren wanneer u een container instelt op de pagina **Alle verzendcontainers**.

Als u wilt werken met koelingstypen, gaat u naar **Francoprijzen \> Containers instellen \> Koelingstypen**. Hier kunt u records voor uw koelingstypen weergeven, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Koelingstype | Voer een unieke identificatienaam/-nummer voor het koelingstype in. |
| Beschrijving | Voer een beschrijving van het koelingstype in. |
