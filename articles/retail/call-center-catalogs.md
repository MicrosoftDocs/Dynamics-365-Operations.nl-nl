---
title: Callcentercatalogi
description: In dit artikel wordt de callcenterspecifieke functionaliteit voor catalogi beschreven in Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9df8682769254f44cc23675fe2237080b447925
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="call-center-catalogs"></a><span data-ttu-id="e4d6e-103">Callcentercatalogi</span><span class="sxs-lookup"><span data-stu-id="e4d6e-103">Call center catalogs</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="e4d6e-104">In dit artikel wordt de callcenterspecifieke functionaliteit voor catalogi beschreven in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="e4d6e-105">In een callcenter kunt u productcatalogi gebruiken voor de identificatie van de producten die u aan klanten wilt aanbieden.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="e4d6e-106">Callcenters gebruiken meestal afgedrukte catalogi.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="e4d6e-107">Het ontwerp en de productie van een afgedrukte catalogus vinden buiten Dynamics 365 for Retail plaats.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="e4d6e-108">U kunt echter een digitaal formulier van een catalogus maken en opslaan met dezelfde pagina's die u gebruikt om online detailhandelcatalogi in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="e4d6e-109">Voordat u een catalogus kunt maken, moet u de productassortimenten instellen en de assortimenten toewijzen aan een callcenter.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="e4d6e-110">U voegt vervolgens producten toe aan de catalogus door producten uit deze assortimenten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="e4d6e-111">Nadat de producten aan de catalogus zijn toegevoegd, en de catalogus is voltooid, moet u de catalogus valideren om de gegevens te controleren.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="e4d6e-112">U moet vervolgens de catalogus indienen ter beoordeling en goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="e4d6e-113">Nadat de catalogus is goedgekeurd, kan deze worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="e4d6e-114">Wanneer een callcentercatalogus wordt gemaakt, kunt u een momentopname van de catalogusgegevens nemen op het moment dat de catalogus wordt gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="e4d6e-115">Met deze momentopnamefunctionaliteit kunt u een bepaalde versie van de catalogus openen, zelfs als de catalogus later wordt gewijzigd en bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="e4d6e-116">De callcentercatalogi kunnen ook worden ingesteld om de volgende optionele functies te bevatten:</span><span class="sxs-lookup"><span data-stu-id="e4d6e-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="e4d6e-117">**Broncodes** – Broncodes worden gebruikt om de klantrespons op bepaalde specifieke catalogusmailings bij te houden.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="e4d6e-118">**Gratis producten** – Producten kunnen zonder extra kosten worden opgenomen in de order van een klant.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="e4d6e-119">Deze producten worden automatisch aan een order toegevoegd wanneer de broncode voor de catalogus in de order wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="e4d6e-120">**Scripts** – Scripts zijn teksten die een callcenterwerknemer voorleest aan een klant wanneer een verkooporder wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="e4d6e-121">Scripts kunnen groeten of aankoopsuggesties omvatten.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="e4d6e-122">**Pagina-indeling** - Een pagina-indeling bevat de paginapositie van producten in de afgedrukte catalogus.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="e4d6e-123">Deze informatie wordt gebruikt voor het analyserapport van het catalogusgebied.</span><span class="sxs-lookup"><span data-stu-id="e4d6e-123">This information is used for the catalog area analysis report.</span></span>





