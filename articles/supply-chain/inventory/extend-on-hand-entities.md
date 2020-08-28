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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: e276348a63bfdb9e712c0ea86e6c2a68c50872c0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665399"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="74c7e-103">Gegevensentiteiten voor voorhanden voorraad uitbreiden</span><span class="sxs-lookup"><span data-stu-id="74c7e-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74c7e-104">Microsoft Dynamics 365 Supply Chain Management biedt [uitbreidings](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)functies waarmee u [velden aan tabellen kunt toevoegen via extensies](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span><span class="sxs-lookup"><span data-stu-id="74c7e-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="74c7e-105">In dit onderwerp vindt u een voorbeeld waarin wordt aangegeven hoe u uitgebreide velden aan de weergaven `INVENTORSITEONHANDENTITY` en `INVENTWAREHOUSEONHANDENTITY` kunt toevoegen, zodat de voorzieningen van voorhanden voorraad van gegevensentiteiten met extensies kunnen werken.</span><span class="sxs-lookup"><span data-stu-id="74c7e-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="74c7e-106">Zie [Overzicht van Gegevensbeheer](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) voor meer informatie over gegevensentiteiten.</span><span class="sxs-lookup"><span data-stu-id="74c7e-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="74c7e-107">Hier volgt een lijst met een aantal gegevensentiteiten voor voorhanden voorraad:</span><span class="sxs-lookup"><span data-stu-id="74c7e-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="74c7e-108">Voorhanden voorraad op locatie</span><span class="sxs-lookup"><span data-stu-id="74c7e-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="74c7e-109">Voorhanden voorraad op locatie V2</span><span class="sxs-lookup"><span data-stu-id="74c7e-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="74c7e-110">Voorhanden voorraad per magazijn</span><span class="sxs-lookup"><span data-stu-id="74c7e-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="74c7e-111">Voorhanden voorraad per magazijn V2</span><span class="sxs-lookup"><span data-stu-id="74c7e-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="74c7e-112">Nadat u velden hebt toegevoegd aan tabellen die in de weergave `inventSiteOnHandView` worden gebruikt, moet u de engine synchroniseren zodat de extensies correct worden herkend.</span><span class="sxs-lookup"><span data-stu-id="74c7e-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="74c7e-113">Breid de weergave `InventSiteOnHandView` uit door het extensieveld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="74c7e-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="74c7e-114">Breid de weergave `InventSiteOnHandAggregatedView` uit met de extensievelden.</span><span class="sxs-lookup"><span data-stu-id="74c7e-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="74c7e-115">Breid de viewBuilder-klasse `InventSiteOnHandAggregatedViewBuilder` uit door de `getExtensionFields()`-methode te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="74c7e-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="74c7e-116">Op deze manier wijst u oude weergavevelden toe aan nieuwe weergavevelden wanneer viewBuilder-synchronisatie wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="74c7e-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="74c7e-117">U hebt bijvoorbeeld de volgende vier velden aan de `InventTable`-tabel toegevoegd:</span><span class="sxs-lookup"><span data-stu-id="74c7e-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="74c7e-118">Aangepast veld 1</span><span class="sxs-lookup"><span data-stu-id="74c7e-118">Custom field 1</span></span>
- <span data-ttu-id="74c7e-119">Aangepast veld 2</span><span class="sxs-lookup"><span data-stu-id="74c7e-119">Custom field 2</span></span>
- <span data-ttu-id="74c7e-120">Aangepast veld 3</span><span class="sxs-lookup"><span data-stu-id="74c7e-120">Custom field 3</span></span>
- <span data-ttu-id="74c7e-121">Aangepast veld 4</span><span class="sxs-lookup"><span data-stu-id="74c7e-121">Custom field 4</span></span>

<span data-ttu-id="74c7e-122">In dit geval moet u de `getExtensionFields()`-methode op de volgende manier wijzigen.</span><span class="sxs-lookup"><span data-stu-id="74c7e-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

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

<span data-ttu-id="74c7e-123">Nadat u deze stappen hebt voltooid, kunt u de voorhanden voorraad per de locatie en de voorhanden voorraad per magazijn uitbreiden door de nieuwe velden toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="74c7e-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="74c7e-124">Op deze manier zorgt u ervoor dat de uitgebreide velden worden herkend en opgenomen in de gegevensmigratie waarbij deze gegevensentiteiten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="74c7e-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
