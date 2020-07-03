---
title: Voorraadbeschikbaarheid in Twee keer wegschrijven
description: Dit onderwerp biedt informatie over het controleren van de voorraadbeschikbaarheid in Twee keer wegschrijven.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443867"
---
# <a name="inventory-availability-in-dual-write"></a>Voorraadbeschikbaarheid in Twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

Op basis van voorraadbeschikbaarheid kunt u uw voorraad controleren voordat u een product toevoegt aan de pagina **Offertes**, **Orders** of **Facturen** in Microsoft Dynamics 365 Sales. Het controleren van de voorraad en het bepalen van een afhandelingsdatum zijn bijvoorbeeld belangrijke taken in het proces [Prospect naar contant geld](dual-write-prospect-to-cash.md).

Als u niet voldoende voorraad hebt, kunt u een leveringsdatum schatten op basis van verwachte voorraadontvangsten en -uitgiften. U kunt ook de ATP-informatie (available to promise) van het product controleren, waar u de ATP-hoeveelheid kunt vinden in de vooraf gedefinieerde time fence.

## <a name="on-hand-inventory"></a>Terhanden voorraad

In de koptekst van de pagina's **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt een nieuwe knop **Voorhanden voorraad** toegevoegd. Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u kunt het bedrijf en het product kunt opgeven waarvoor u de voorhanden voorraad wilt controleren. In dit dialoogvenster wordt dezelfde informatie weergegeven als [voorhanden voorraad](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

In het dialoogvenster worden de voorraadgegevens opgehaald uit Dynamics 365 Supply Chain Management. Deze informatie bevat de volgende hoeveelheden:

- Voorhanden hoeveelheid
- Gereserveerde voorhanden hoeveelheid
- Beschikbare voorhanden hoeveelheid
- Bestelde hoeveelheid
- Hoeveelheid in bestelling
- Gereserveerde bestelde hoeveelheid
- Totale beschikbare hoeveelheid

## <a name="atp-information"></a>ATP-informatie

In Sales is een nieuwe knop **ATP-informatie** toegevoegd aan regelartikelen op de pagina's **Offertes**, **Orders** en **Facturen**. Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u het bedrijf, het product, de voorraadvestiging, het voorraadmagazijn en de bestelhoeveelheid kunt opgeven. Dit dialoogvenster heeft dezelfde instellingen als worden beschreven bij [Orderbelofte](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

In het dialoogvenster worden de ATP-gegevens uit Supply Chain Management geretourneerd. Deze informatie bevat de volgende hoeveelheden:

- ATP-hoeveelheid
- Ontvangsthoeveelheid
- Uitgiftehoeveelheid
- Voorhanden hoeveelheid
