---
title: Behoefteplanningsinstellingen
description: Dit onderwerp bevat informatie over de instellingen voor behoefteplanning die door de hoofdplanning wordt gebruikt om artikelbehoeften te berekenen.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538889"
---
# <a name="coverage-settings"></a><span data-ttu-id="6731b-103">Behoefteplanningsinstellingen</span><span class="sxs-lookup"><span data-stu-id="6731b-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6731b-104">Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen.</span><span class="sxs-lookup"><span data-stu-id="6731b-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="6731b-105">U kunt behoefteplanningsinstellingen op verschillende manieren instellen:</span><span class="sxs-lookup"><span data-stu-id="6731b-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="6731b-106">Geef de behoefteplanningsinstellingen voor een behoefteplanningsgroep op.</span><span class="sxs-lookup"><span data-stu-id="6731b-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="6731b-107">U kunt een behoefteplanningsgroep maken die instellingen bevat voor alle producten die zijn gekoppeld aan de behoefteplanningsgroep.</span><span class="sxs-lookup"><span data-stu-id="6731b-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="6731b-108">Ga naar **Hoofdplanning &gt; Instellen &gt; Behoefteplanning &gt; Behoefteplanningsgroepen** om een behoefteplanningsgroep te maken.</span><span class="sxs-lookup"><span data-stu-id="6731b-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="6731b-109">U kunt een behoefteplanningsgroep koppelen aan een product.</span><span class="sxs-lookup"><span data-stu-id="6731b-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="6731b-110">Als de koppeling specifiek is voor een locatie, magazijn of productdimensie, gebruikt u het veld **Behoefteplanningsgroep** op de pagina **Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="6731b-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="6731b-111">Als de koppeling algemeen is, ongeacht de productdimensies, gebruikt u het veld **Behoefteplanningsgroep** op het sneltabblad **Plannen** van de pagina **Productgegevens**.</span><span class="sxs-lookup"><span data-stu-id="6731b-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="6731b-112">Als u geen behoefteplanningsgroep aan een product koppelt, maakt de hoofdplanning standaard gebruik van de algemene behoefteplanningsgroep die is opgegeven op de pagina **Parameters hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="6731b-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="6731b-113">Geef behoefteplanningsinstellingen op voor een product.</span><span class="sxs-lookup"><span data-stu-id="6731b-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="6731b-114">U kunt behoefteplanningsinstellingen maken voor een bepaald product.</span><span class="sxs-lookup"><span data-stu-id="6731b-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="6731b-115">Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="6731b-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="6731b-116">Selecteer het product en selecteer vervolgens in het actievenster op het tabblad **Plannen** in de groep **Behoefteplanning** de optie **Artikelbehoefteplanning** om de pagina **Artikelbehoefteplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="6731b-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="6731b-117">Als het product al aan een behoefteplanningsgroep is gekoppeld, kunt u de behoefteplanningsgroepsinstellingen negeren door het veld **Overschrijven** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6731b-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="6731b-118">De behoefteplanningsinstellingen op de pagina **Artikelbehoefteplanning** hebben voorrang op de instellingen op de pagina **Behoefteplanningsgroep**.</span><span class="sxs-lookup"><span data-stu-id="6731b-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="6731b-119">Geef behoefteplanningsinstellingen voor een product op met behulp van een wizard.</span><span class="sxs-lookup"><span data-stu-id="6731b-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="6731b-120">De wizard leidt u stapsgewijs door het proces van het instellen van de parameters voor de primaire artikelbehoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="6731b-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="6731b-121">Selecteer op de pagina **Artikelbehoefteplanning** in het actievenster de optie **Wizard** om de **Wizard Artikelbehoefteplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="6731b-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="6731b-122">Geef behoefteplanningsinstellingen op voor een dimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="6731b-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="6731b-123">Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="6731b-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="6731b-124">Selecteer op de pagina **Vrijgegeven productdetails** op het sneltabblad **Algemeen** in de sectie **Beheer** de koppeling in het veld **Opslagdimensiegroep**.</span><span class="sxs-lookup"><span data-stu-id="6731b-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="6731b-125">Schakel op de pagina **Opslagdimensiegroepen** het selectievakje **In behoefteplan opnemen volgens dimensie** in om de behoefteplanningsinstellingen voor een dimensie in de opslagdimensiegroep te maken.</span><span class="sxs-lookup"><span data-stu-id="6731b-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="6731b-126">Het veld **In behoefteplan opnemen volgens dimensie** moet worden geselecteerd voor alle productdimensies, zoals configuratie, kleur, grootte en stijl.</span><span class="sxs-lookup"><span data-stu-id="6731b-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6731b-127">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="6731b-127">Additional resources</span></span>

[<span data-ttu-id="6731b-128">Hoofdplannen</span><span class="sxs-lookup"><span data-stu-id="6731b-128">Master plans</span></span>](master-plans.md)
