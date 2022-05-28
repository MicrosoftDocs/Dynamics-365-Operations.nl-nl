---
title: Instellingen van verzendgegevens
description: In dit onderwerp wordt beschreven hoe u verzendgegevens kunt instellen voor de module Francoprijzen.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1ee099b923f3e2140f7f6962795fc6b6e87b913a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690297"
---
# <a name="shipping-information-setup"></a>Instellingen van verzendgegevens

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u verzendgegevens kunt instellen voor de module **Francoprijzen**.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Beschrijving van goederen

Beschrijvingen van goederen helpen bij het identificeren van een transport, verzendcontainer of folio van goederen en de goederen die deze bevatten. U kunt een beschrijving van goederen selecteren in de koptekst van de verzendcontainer of in de foliokoptekst.

Als u wilt werken met beschrijvingen van goederen, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Beschrijving van goederen**. Hier kunt u records voor beschrijvingen van goederen weergeven, openen, maken en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Beschrijving van goederen | Voer een unieke identificatienaam/-nummer in voor het type goederen dat deze beschrijving gebruikt. |
| Beschrijving | Voer een beschrijving in van het type goederen in deze categorie. |

## <a name="vessels"></a><a name="vessels"></a>Vaartuigen

Een vaartuig is de unieke naam van een schip of vaartuig dat door een expeditiebedrijf of instantie wordt gebruikt. Wanneer u een transport maakt, moet u hiervoor altijd een vaartuig selecteren of invoeren. Als u vaak dezelfde vaartuigen gebruikt, kunt u het sneller en eenvoudiger maken om een nieuw transport te maken door een vaartuigrecord voor elk daarvan te maken, zodat gebruikers het vaartuig kunnen selecteren uit een lijst in plaats van steeds de naam of het nummer handmatig te moeten invoeren.

Als u wilt werken met vaartuigen, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Vaartuigen**. Hier kunt u records voor vaartuigen weergeven, openen, maken en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Vaartuig | Voer een unieke identificatienaam/-nummer in voor het schip dat zal worden gebruikt om goederen tijdens een transport te vervoeren. |
| Beschrijving | Voer een beschrijving van het vaartuig in. Deze beschrijving geeft normaal gesproken de naam van het schip en van het expeditiebedrijf/de agent aan. |
| Leveringsmethode | Selecteer de leveringsmodus die door het vaartuig wordt gebruikt (zoals _Lucht_, _Oceaan_ of _Trein_). |

## <a name="exporters"></a>Exporteurs

Elke exporteurrecord identificeert een leverancier of exporteur die als leverancier voor een transport kan worden gedefinieerd. De exporteur kan aan een transport worden gekoppeld en voor rapportage worden gebruikt.

Als u wilt werken met exporteurs, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Exporteurs**. Hier kunt u records voor exporteurs weergeven, openen, maken en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Exporteur | Voer een unieke identificatienaam/-nummer in voor de exporteur van goederen die tijdens een transport worden vervoerd. |
| Beschrijving | Voer een beschrijving van de exporteur in. Deze beschrijving geeft normaal gesproken de volledige naam van het expeditiebedrijf/de agent aan. |

## <a name="commodity-codes"></a>Basisproductcodes

U gebruikt basisproductcodes om te helpen bij de douane-identificatie en de berekening van accijnstarieven voor goederen tijdens een transport. U kunt basisproductcodes selecteren op de pagina **Vrijgegeven producten**.

Als u wilt werken met basisproductcodes, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Basisproductcodes**. Hier kunt u records voor basisproductcodes weergeven, openen, maken en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Basisproductcode | Voer een unieke code in voor dit type basisproduct. |
| Beschrijving | Voer een beschrijving van het type basisproduct in. |

## <a name="customs-description"></a>Douanebeschrijving

Douanebeschrijvingen helpen bij het identificeren van goederen voor douanedoeleinden. U kunt een douanebeschrijving selecteren op de pagina **Vrijgegeven producten** of op inkooporderregels.

Als u wilt werken met douanebeschrijvingen, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Douanebeschrijving**. Hier kunt u records voor douanebeschrijvingen weergeven, openen, maken en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Douanebeschrijving | Voer een unieke code in voor dit type douaneclassificatie. Vaak is deze code de officiële beschrijving die door een douane-instantie wordt verstrekt voor de beschrijving en kwalitatieve waarde van de goederen. |
| Beschrijving | Voer een beschrijving van de douaneclassificatie in. |
