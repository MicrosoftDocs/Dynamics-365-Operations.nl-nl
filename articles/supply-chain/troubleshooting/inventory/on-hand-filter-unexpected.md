---
title: Het filterdeelvenster van de lijst Voorhanden voorraad werkt niet zoals verwacht.
description: Met de filters in het filterdeelvenster op de pagina Voorhanden voorraad worden de resultaten niet gefilterd zoals verwacht.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920493"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Het filterdeelvenster van de lijst Voorhanden voorraad werkt niet zoals verwacht.

## <a name="symptoms"></a>Symptomen

Met de filters in het filterdeelvenster op de pagina **Voorhanden voorraad** worden de resultaten niet gefilterd zoals verwacht.

## <a name="resolution"></a>Oplossing

De pagina **Voorhanden voorraad** wordt samengesteld uit een gedetailleerde tabel met voorhanden voorraad waarin alle beschikbare dimensies zijn opgenomen. De lijst op deze pagina is echter een overzicht. Daarom kunnen rijen uit de brontabel worden gecombineerd door waarden te aggregeren op basis van de dimensies die worden weergegeven.

De filters die in het filterdeelvenster zijn ingesteld, zijn van toepassing op de brontabel en niet op de samengevoegde lijst. Dit gedrag kan soms onverwachte resultaten opleveren, zoals in [deze voorbeelden](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples) wordt getoond.

De [filters die in het raster worden vermeld](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) hebben echter *wel* betrekking op de samengevoegde lijst. Deze filters bevatten zowel het snelfilter boven aan het raster als het filter voor elke kolomkop.
