---
title: Behoefteplanningsinstellingen
description: Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a><span data-ttu-id="1a0f6-103">Behoefteplanningsinstellingen</span><span class="sxs-lookup"><span data-stu-id="1a0f6-103">Coverage settings</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1a0f6-104">Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="1a0f6-105">U kunt behoefteplanningsinstellingen op verschillende manieren instellen:</span><span class="sxs-lookup"><span data-stu-id="1a0f6-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="1a0f6-106">Geef de behoefteplanningsinstellingen voor een behoefteplanningsgroep op.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="1a0f6-107">U kunt een behoefteplanningsgroep maken die instellingen bevat voor alle producten die zijn gekoppeld aan de behoefteplanningsgroep.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="1a0f6-108">Klik op **Hoofdplanning &gt; Instellen &gt; Behoefteplanning &gt; Dekking Behoefteplanning** om een behoefteplanningsgroep te maken.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="1a0f6-109">U kunt een behoefteplanningsgroep koppelen aan een product.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="1a0f6-110">Als de koppeling specifiek is voor een locatie, magazijn of productdimensie, gebruikt u het veld **Behoefteplanningsgroep** op de pagina **Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="1a0f6-111">Als de koppeling generisch is, ongeacht de productdimensies, gebruikt u **Behoefteplanningsgroep** op het sneltabblad **Plannen** op de pagina **Productgegevens**.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="1a0f6-112">Als u geen behoefteplanningsgroep aan een product koppelt, maakt de hoofdplanning gebruik van de **Algemene behoefteplanningsgroep** die is als standaard is opgegeven op de pagina **Parameters hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="1a0f6-113">Geef behoefteplanningsinstellingen op voor een product.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="1a0f6-114">U kunt behoefteplanningsinstellingen maken voor een bepaald product.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="1a0f6-115">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="1a0f6-116">Selecteer het product in het **Actievenster** en klik op het tabblad **Plannen** in de **Behoefteplanningsgroep** op **Artikelbehoefteplanning** om de pagina **Artikelbehoefteplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="1a0f6-117">Als het product al aan een behoefteplanningsgroep is gekoppeld, kunt u de behoefteplanningsgroepsinstellingen negeren door het veld **Overschrijven** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="1a0f6-118">De behoefteplanningsinstellingen op de pagina **Artikelbehoefteplanning** hebben voorrang op de instellingen op de pagina **Behoefteplanningsgroep**.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="1a0f6-119">Geef behoefteplanningsinstellingen voor een product op met behulp van een wizard.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="1a0f6-120">De wizard is een stapsgewijze ondersteuning bij het instellen van de primaire artikelbehoefteplanningsparameters.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="1a0f6-121">Klik op de pagina **Artikelbehoefteplanning** op **Wizard** om de **Wizard Artikelbehoefteplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="1a0f6-122">Geef behoefteplanningsinstellingen op voor een dimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="1a0f6-123">Klik op <strong>Productgegevensbeheer &gt; Algemeen &gt; Vrijgegeven producten</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-123">Click <strong>Product information management &gt; Common &gt; Released products</strong>.</span></span> <span data-ttu-id="1a0f6-124">Klik op de pagina <strong>Vrijgegeven productdetail **op het tabblad **Algemeen</strong>, in de groep <strong>Administratie</strong> op de koppeling <strong>Opslagdimensiegroep</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-124">On the <strong>Released product detail **page, on the **General</strong> tab, in the <strong>Administration</strong> group, click the <strong>Storage dimension group</strong> link.</span></span> <span data-ttu-id="1a0f6-125">Selecteer op de pagina <strong>Opslagdimensiegroep</strong> het veld <strong>In behoefteplan opnemen volgens dimensie</strong> om de behoefteplanningsinstellingen voor een dimensie in de opslagdimensiegroep te maken.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-125">On the <strong>Storage dimension group</strong> page, select the <strong>Coverage plan by dimension</strong> field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="1a0f6-126">Alle productdimensies, zoals configuratie, kleur, grootte, stijl, moeten het veld <strong>In behoefteplan opnemen volgens dimensie</strong> hebben geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1a0f6-126">All product dimensions, such as configuration, color, size, style, must have the <strong>Coverage plan by dimension</strong> field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="1a0f6-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1a0f6-127">See also</span></span>
--------

[<span data-ttu-id="1a0f6-128">Hoofdplannen</span><span class="sxs-lookup"><span data-stu-id="1a0f6-128">Master plans</span></span>](master-plans.md)




