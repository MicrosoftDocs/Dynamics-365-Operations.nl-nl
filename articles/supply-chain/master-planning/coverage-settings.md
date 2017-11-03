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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd85f89917659ac9c94590bace765b2123d6e556
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="8020e-103">Behoefteplanningsinstellingen</span><span class="sxs-lookup"><span data-stu-id="8020e-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8020e-104">Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen.</span><span class="sxs-lookup"><span data-stu-id="8020e-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="8020e-105">U kunt behoefteplanningsinstellingen op verschillende manieren instellen:</span><span class="sxs-lookup"><span data-stu-id="8020e-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="8020e-106">Geef de behoefteplanningsinstellingen voor een behoefteplanningsgroep op.</span><span class="sxs-lookup"><span data-stu-id="8020e-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="8020e-107">U kunt een behoefteplanningsgroep maken die instellingen bevat voor alle producten die zijn gekoppeld aan de behoefteplanningsgroep.</span><span class="sxs-lookup"><span data-stu-id="8020e-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="8020e-108">Klik op **Hoofdplanning &gt; Instellen &gt; Behoefteplanning &gt; Dekking Behoefteplanning** om een behoefteplanningsgroep te maken.</span><span class="sxs-lookup"><span data-stu-id="8020e-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="8020e-109">U kunt een behoefteplanningsgroep koppelen aan een product.</span><span class="sxs-lookup"><span data-stu-id="8020e-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="8020e-110">Als de koppeling specifiek is voor een locatie, magazijn of productdimensie, gebruikt u het veld **Behoefteplanningsgroep** op de pagina **Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="8020e-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="8020e-111">Als de koppeling generisch is, ongeacht de productdimensies, gebruikt u **Behoefteplanningsgroep** op het sneltabblad **Plannen** op de pagina **Productgegevens**.</span><span class="sxs-lookup"><span data-stu-id="8020e-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="8020e-112">Als u geen behoefteplanningsgroep aan een product koppelt, maakt de hoofdplanning gebruik van de **Algemene behoefteplanningsgroep** die is als standaard is opgegeven op de pagina **Parameters hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="8020e-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="8020e-113">Geef behoefteplanningsinstellingen op voor een product.</span><span class="sxs-lookup"><span data-stu-id="8020e-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="8020e-114">U kunt behoefteplanningsinstellingen maken voor een bepaald product.</span><span class="sxs-lookup"><span data-stu-id="8020e-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="8020e-115">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="8020e-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="8020e-116">Selecteer het product in het **Actievenster** en klik op het tabblad **Plannen** in de **Behoefteplanningsgroep** op **Artikelbehoefteplanning** om de pagina **Artikelbehoefteplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="8020e-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="8020e-117">Als het product al aan een behoefteplanningsgroep is gekoppeld, kunt u de behoefteplanningsgroepsinstellingen negeren door het veld **Overschrijven** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8020e-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="8020e-118">De behoefteplanningsinstellingen op de pagina **Artikelbehoefteplanning** hebben voorrang op de instellingen op de pagina **Behoefteplanningsgroep**.</span><span class="sxs-lookup"><span data-stu-id="8020e-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="8020e-119">Geef behoefteplanningsinstellingen voor een product op met behulp van een wizard.</span><span class="sxs-lookup"><span data-stu-id="8020e-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="8020e-120">De wizard is een stapsgewijze ondersteuning bij het instellen van de primaire artikelbehoefteplanningsparameters.</span><span class="sxs-lookup"><span data-stu-id="8020e-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="8020e-121">Klik op de pagina **Artikelbehoefteplanning** op **Wizard** om de **Wizard Artikelbehoefteplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="8020e-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="8020e-122">Geef behoefteplanningsinstellingen op voor een dimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="8020e-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="8020e-123">Klik op **Productgegevensbeheer &gt; Algemeen &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="8020e-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="8020e-124">Klik op de pagina **Vrijgegeven productdetail** op het tabblad **Algemeen** in de groep **Administratie** op de koppeling **Opslagdimensiegroep**.</span><span class="sxs-lookup"><span data-stu-id="8020e-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="8020e-125">Selecteer op de pagina **Opslagdimensiegroep** het veld **In behoefteplan opnemen volgens dimensie** om de behoefteplanningsinstellingen voor een dimensie in de opslagdimensiegroep te maken.</span><span class="sxs-lookup"><span data-stu-id="8020e-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="8020e-126">Alle productdimensies, zoals configuratie, kleur, grootte, stijl, moeten het veld **In behoefteplan opnemen volgens dimensie** hebben geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="8020e-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="8020e-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8020e-127">See also</span></span>
--------

[<span data-ttu-id="8020e-128">Hoofdplannen</span><span class="sxs-lookup"><span data-stu-id="8020e-128">Master plans</span></span>](master-plans.md)




