---
title: Opties voor het voorkomen van kortingen voor detailhandelproducten
description: Er zijn verschillende redenen waarom detailhandelaren willen voorkomen dat voor bepaalde producten korting wordt verleend, zoals bij een promotie of tijdens de verkoop op het POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6a683ffce487dc4388711ad160c2e8dc55a690dd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057459"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>Opties voor het voorkomen van kortingen voor detailhandelproducten

[!include [banner](includes/banner.md)]

Er zijn verschillende redenen waarom detailhandelaren willen voorkomen dat voor bepaalde producten korting wordt verleend, zoals bij een promotie of tijdens de verkoop op het POS.

De volgende opties vindt u op het tabblad **Commerce** van uitgegeven producten. Hiermee kunt u het product configureren om alle of handmatige kortingen te voorkomen. De instellingen kunnen ook worden opgegeven op categorieniveau vanuit de hiërarchie van categorieën.

- **Alle kortingen voorkomen**: selecteer deze optie om te voorkomen dat alle soorten kortingen worden toegepast op dit product. Het gaat hierbij om acties zoals combinatiekortingen, volume- en drempelkortingen, en handmatige regel- en transactiekortingen die tijdens een verkoop worden toegepast door een POS-gebruiker.
- **Handmatige kortingen voorkomen**: selecteer deze optie alleen om handmatige regel- of transactiekortingen te voorkomen die tijdens een verkoop worden toegepast door een POS-gebruiker. Producten waarvoor deze optie is geselecteerd, komen nog steeds in aanmerking voor promoties, combinatiekortingen en volume- en drempelkortingen.

> [!NOTE]
> Deze instellingen beperken niet de werking van prijsoverschrijvingen omdat die de basisprijs instellen en niet als een korting gelden.

[![Veld Kortingen voorkomen](./media/prevent-discounts.png)](./media/prevent-discounts.png)
