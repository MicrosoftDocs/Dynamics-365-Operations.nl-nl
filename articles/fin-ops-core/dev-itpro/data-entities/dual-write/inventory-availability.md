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
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426977"
---
# <a name="inventory-availability"></a>Voorraadbeschikbaarheid

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Op basis van voorraadbeschikbaarheid kunt u uw voorraad controleren voordat u een product toevoegt aan de formulieren **Offertes**, **Orders** of **Facturen** in modelgestuurde apps in Dynamics 365. Het controleren van de voorraad en het bepalen van een afhandelingsdatum zijn bijvoorbeeld belangrijke taken in het proces [Prospect naar contant geld](dual-write-prospect-to-cash.md). Als u niet voldoende voorraad hebt, kunt u een leveringsdatum schatten op basis van verwachte voorraadontvangsten en -uitgiften. U kunt ook de ATP-informatie (available to promise) van het product controleren, waar u de ATP-hoeveelheid kunt vinden in de vooraf gedefinieerde time fence.

## <a name="on-hand-inventory"></a>Voorhanden voorraad 

In de koptekst van de formulieren **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt de nieuwe knop **Voorhanden voorraad** toegevoegd. Wanneer u op de knop klikt, wordt er een dialoogvenster weergegeven en kunt u het bedrijf en het product opgeven waarvoor u de voorhanden voorraad wilt controleren. De voorraadinformatie vanuit Dynamics 365 Supply Chain Management wordt geretourneerd en dezefde als in [Voorhanden voorraad](../../../../supply-chain/inventory/tasks/check-availability-stock.md) wordt weergegeven. De informatie omvat de volgende hoeveelheden:

- **Voorhanden hoeveelheid**
- **Gereserveerde voorhanden hoeveelheid**
- **Beschikbare voorhanden hoeveelheid**
- **Bestelhoeveelheid**
- **Hoeveelheid in bestelling**
- **Gereserveerde bestelde hoeveelheid**
- **Totale beschikbare hoeveelheid**

## <a name="atp-information"></a>ATP-informatie

Op regelartikelen van de formulieren **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt de nieuwe knop **ATP-informatie** toegevoegd. Wanneer u op de knop klikt, wordt er een dialoogvenster weergegeven en kunt u het bedrijf, het product, de voorraadvestiging, het voorraadmagazijn en de bestelhoeveelheid opgeven. **ATP-informatie** wordt geretourneerd vanuit Supply Chain Management en toont de instellingen die worden beschreven in [Orderbelofte](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). De informatie omvat de **ATP-hoeveelheid**, **ontvangsthoeveelheid**, **uitgiftehoeveelheid** en **voorhanden hoeveelheid**.
