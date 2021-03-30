---
title: Gegevensentiteiten voor voorhanden voorraad uitbreiden
description: In dit onderwerp vindt u een voorbeeld waarin wordt aangegeven hoe u uitgebreide velden aan de weergaven INVENTORSITEONHANDENTITY en INVENTWAREHOUSEONHANDENTITY kunt toevoegen, zodat de voorzieningen van voorhanden voorraad van gegevensentiteiten met extensies kunnen werken.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0f48e424a9ab3349d3c114ecbd01424005b9a9c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219336"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Gegevensentiteiten voor voorhanden voorraad uitbreiden

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management biedt [uitbreidings](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)functies waarmee u [velden aan tabellen kunt toevoegen via extensies](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). In dit onderwerp vindt u een voorbeeld waarin wordt aangegeven hoe u uitgebreide velden aan de weergaven `INVENTORSITEONHANDENTITY` en `INVENTWAREHOUSEONHANDENTITY` kunt toevoegen, zodat de voorzieningen van voorhanden voorraad van gegevensentiteiten met extensies kunnen werken. Zie [Overzicht van Gegevensbeheer](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) voor meer informatie over gegevensentiteiten.

> [!NOTE]
> Hier volgt een lijst met een aantal gegevensentiteiten voor voorhanden voorraad:
>
> - Voorhanden voorraad op locatie
> - Voorhanden voorraad op locatie V2
> - Voorhanden voorraad per magazijn
> - Voorhanden voorraad per magazijn V2

Nadat u velden hebt toegevoegd aan tabellen die in de weergave `inventSiteOnHandView` worden gebruikt, moet u de engine synchroniseren zodat de extensies correct worden herkend.

1. Breid de weergave `InventSiteOnHandView` uit door het extensieveld toe te voegen.
1. Breid de weergave `InventSiteOnHandAggregatedView` uit met de extensievelden.
1. Breid de viewBuilder-klasse `InventSiteOnHandAggregatedViewBuilder` uit door de `getExtensionFields()`-methode te wijzigen. Op deze manier wijst u oude weergavevelden toe aan nieuwe weergavevelden wanneer viewBuilder-synchronisatie wordt uitgevoerd.

U hebt bijvoorbeeld de volgende vier velden aan de `InventTable`-tabel toegevoegd:

- Aangepast veld 1
- Aangepast veld 2
- Aangepast veld 3
- Aangepast veld 4

In dit geval moet u de `getExtensionFields()`-methode op de volgende manier wijzigen.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Nadat u deze stappen hebt voltooid, kunt u de voorhanden voorraad per de locatie en de voorhanden voorraad per magazijn uitbreiden door de nieuwe velden toe te voegen. Op deze manier zorgt u ervoor dat de uitgebreide velden worden herkend en opgenomen in de gegevensmigratie waarbij deze gegevensentiteiten worden gebruikt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]