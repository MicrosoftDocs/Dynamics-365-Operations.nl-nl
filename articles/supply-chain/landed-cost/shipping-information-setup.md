---
title: Instellingen van verzendgegevens
description: In dit onderwerp wordt beschreven hoe u verzendgegevens kunt instellen voor de module Francoprijzen.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 74ac7e0eac545369eef1a48f0085c820a4728e75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833684"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="eb8b0-103">Instellingen van verzendgegevens</span><span class="sxs-lookup"><span data-stu-id="eb8b0-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb8b0-104">In dit onderwerp wordt beschreven hoe u verzendgegevens kunt instellen voor de module **Francoprijzen**.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="eb8b0-105">Beschrijving van goederen</span><span class="sxs-lookup"><span data-stu-id="eb8b0-105">Description of goods</span></span>

<span data-ttu-id="eb8b0-106">Beschrijvingen van goederen helpen bij het identificeren van een transport, verzendcontainer of folio van goederen en de goederen die deze bevatten.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="eb8b0-107">U kunt een beschrijving van goederen selecteren in de koptekst van de verzendcontainer of in de foliokoptekst.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="eb8b0-108">Als u wilt werken met beschrijvingen van goederen, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Beschrijving van goederen**.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="eb8b0-109">Hier kunt u records voor beschrijvingen van goederen weergeven, openen, maken en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="eb8b0-110">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="eb8b0-111">Veld</span><span class="sxs-lookup"><span data-stu-id="eb8b0-111">Field</span></span> | <span data-ttu-id="eb8b0-112">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-112">Description</span></span> |
|---|---|
| <span data-ttu-id="eb8b0-113">Beschrijving van goederen</span><span class="sxs-lookup"><span data-stu-id="eb8b0-113">Description of goods</span></span> | <span data-ttu-id="eb8b0-114">Voer een unieke identificatienaam/-nummer in voor het type goederen dat deze beschrijving gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="eb8b0-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-115">Description</span></span> | <span data-ttu-id="eb8b0-116">Voer een beschrijving in van het type goederen in deze categorie.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="eb8b0-117">Vaartuigen</span><span class="sxs-lookup"><span data-stu-id="eb8b0-117">Vessels</span></span>

<span data-ttu-id="eb8b0-118">Een vaartuig is de unieke naam van een schip of vaartuig dat door een expeditiebedrijf of instantie wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="eb8b0-119">Wanneer u een transport maakt, moet u hiervoor altijd een vaartuig selecteren of invoeren.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="eb8b0-120">Als u vaak dezelfde vaartuigen gebruikt, kunt u het sneller en eenvoudiger maken om een nieuw transport te maken door een vaartuigrecord voor elk daarvan te maken, zodat gebruikers het vaartuig kunnen selecteren uit een lijst in plaats van steeds de naam of het nummer handmatig te moeten invoeren.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="eb8b0-121">Als u wilt werken met vaartuigen, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Vaartuigen**.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="eb8b0-122">Hier kunt u records voor vaartuigen weergeven, openen, maken en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="eb8b0-123">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="eb8b0-124">Veld</span><span class="sxs-lookup"><span data-stu-id="eb8b0-124">Field</span></span> | <span data-ttu-id="eb8b0-125">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-125">Description</span></span> |
|---|---|
| <span data-ttu-id="eb8b0-126">Vaartuig</span><span class="sxs-lookup"><span data-stu-id="eb8b0-126">Vessel</span></span> | <span data-ttu-id="eb8b0-127">Voer een unieke identificatienaam/-nummer in voor het schip dat zal worden gebruikt om goederen tijdens een transport te vervoeren.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="eb8b0-128">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-128">Description</span></span> | <span data-ttu-id="eb8b0-129">Voer een beschrijving van het vaartuig in.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-129">Enter a description of the vessel.</span></span> <span data-ttu-id="eb8b0-130">Deze beschrijving geeft normaal gesproken de naam van het schip en van het expeditiebedrijf/de agent aan.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="eb8b0-131">Leveringsmethode</span><span class="sxs-lookup"><span data-stu-id="eb8b0-131">Mode of delivery</span></span> | <span data-ttu-id="eb8b0-132">Selecteer de leveringsmodus die door het vaartuig wordt gebruikt (zoals _Lucht_, _Oceaan_ of _Trein_).</span><span class="sxs-lookup"><span data-stu-id="eb8b0-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="eb8b0-133">Exporteurs</span><span class="sxs-lookup"><span data-stu-id="eb8b0-133">Exporters</span></span>

<span data-ttu-id="eb8b0-134">Elke exporteurrecord identificeert een leverancier of exporteur die als leverancier voor een transport kan worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="eb8b0-135">De exporteur kan aan een transport worden gekoppeld en voor rapportage worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="eb8b0-136">Als u wilt werken met exporteurs, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Exporteurs**.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="eb8b0-137">Hier kunt u records voor exporteurs weergeven, openen, maken en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="eb8b0-138">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="eb8b0-139">Veld</span><span class="sxs-lookup"><span data-stu-id="eb8b0-139">Field</span></span> | <span data-ttu-id="eb8b0-140">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-140">Description</span></span> |
|---|---|
| <span data-ttu-id="eb8b0-141">Exporteur</span><span class="sxs-lookup"><span data-stu-id="eb8b0-141">Exporter</span></span> | <span data-ttu-id="eb8b0-142">Voer een unieke identificatienaam/-nummer in voor de exporteur van goederen die tijdens een transport worden vervoerd.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="eb8b0-143">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-143">Description</span></span> | <span data-ttu-id="eb8b0-144">Voer een beschrijving van de exporteur in.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-144">Enter a description of the exporter.</span></span> <span data-ttu-id="eb8b0-145">Deze beschrijving geeft normaal gesproken de volledige naam van het expeditiebedrijf/de agent aan.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="eb8b0-146">Basisproductcodes</span><span class="sxs-lookup"><span data-stu-id="eb8b0-146">Commodity codes</span></span>

<span data-ttu-id="eb8b0-147">U gebruikt basisproductcodes om te helpen bij de douane-identificatie en de berekening van accijnstarieven voor goederen tijdens een transport.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="eb8b0-148">U kunt basisproductcodes selecteren op de pagina **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="eb8b0-149">Als u wilt werken met basisproductcodes, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Basisproductcodes**.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="eb8b0-150">Hier kunt u records voor basisproductcodes weergeven, openen, maken en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="eb8b0-151">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="eb8b0-152">Veld</span><span class="sxs-lookup"><span data-stu-id="eb8b0-152">Field</span></span> | <span data-ttu-id="eb8b0-153">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-153">Description</span></span> |
|---|---|
| <span data-ttu-id="eb8b0-154">Basisproductcode</span><span class="sxs-lookup"><span data-stu-id="eb8b0-154">Commodity code</span></span> | <span data-ttu-id="eb8b0-155">Voer een unieke code in voor dit type basisproduct.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="eb8b0-156">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-156">Description</span></span> | <span data-ttu-id="eb8b0-157">Voer een beschrijving van het type basisproduct in.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="eb8b0-158">Douanebeschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-158">Customs description</span></span>

<span data-ttu-id="eb8b0-159">Douanebeschrijvingen helpen bij het identificeren van goederen voor douanedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="eb8b0-160">U kunt een douanebeschrijving selecteren op de pagina **Vrijgegeven producten** of op inkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="eb8b0-161">Als u wilt werken met douanebeschrijvingen, gaat u naar **Francoprijzen \> Verzendgegevens instellen \> Douanebeschrijving**.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="eb8b0-162">Hier kunt u records voor douanebeschrijvingen weergeven, openen, maken en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="eb8b0-163">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="eb8b0-164">Veld</span><span class="sxs-lookup"><span data-stu-id="eb8b0-164">Field</span></span> | <span data-ttu-id="eb8b0-165">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-165">Description</span></span> |
|---|---|
| <span data-ttu-id="eb8b0-166">Douanebeschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-166">Customs description</span></span> | <span data-ttu-id="eb8b0-167">Voer een unieke code in voor dit type douaneclassificatie.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="eb8b0-168">Vaak is deze code de officiële beschrijving die door een douane-instantie wordt verstrekt voor de beschrijving en kwalitatieve waarde van de goederen.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="eb8b0-169">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="eb8b0-169">Description</span></span> | <span data-ttu-id="eb8b0-170">Voer een beschrijving van de douaneclassificatie in.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-170">Enter a description of the customs classification.</span></span> |
