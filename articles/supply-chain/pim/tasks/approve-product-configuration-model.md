---
title: Een productconfiguratiemodel goedkeuren
description: Het uitvoeren van deze procedure vereist dat er ten minste één productconfiguratiemodel beschikbaar is.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920502"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="de734-103">Een productconfiguratiemodel goedkeuren</span><span class="sxs-lookup"><span data-stu-id="de734-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de734-104">Het uitvoeren van deze procedure vereist dat er ten minste één productconfiguratiemodel beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="de734-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="de734-105">In deze procedure wordt het model Geavanceerde luidspreker gebruikt in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="de734-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="de734-106">Dit model is al goedgekeurd, maar de procedure begeleidt u door het hele proces.</span><span class="sxs-lookup"><span data-stu-id="de734-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="de734-107">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="de734-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="de734-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="de734-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="de734-109">Selecteer het model Geavanceerde luidspreker voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="de734-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="de734-110">Selecteer **Versies**.</span><span class="sxs-lookup"><span data-stu-id="de734-110">Select **Versions**.</span></span>
1. <span data-ttu-id="de734-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="de734-111">Select **New**.</span></span>
1. <span data-ttu-id="de734-112">Typ of selecteer een waarde in het veld **Productnummer**.</span><span class="sxs-lookup"><span data-stu-id="de734-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="de734-113">De verwijzing naar een product vertegenwoordigt een versie van een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="de734-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="de734-114">Alleen productmodellen die de op beperkingen gebaseerde configuratietechnologie hebben worden in deze lijst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de734-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="de734-115">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="de734-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="de734-116">Selecteer wanneer de productmodelversie beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="de734-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="de734-117">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="de734-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="de734-118">Selecteer een einddatum wanneer deze productmodelversie vervalt of selecteer Nooit.</span><span class="sxs-lookup"><span data-stu-id="de734-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="de734-119">Selecteer **Goedkeuren** om het dialoogvenster met vervolgkeuzelijst te openen.</span><span class="sxs-lookup"><span data-stu-id="de734-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="de734-120">Typ of selecteer een waarde in het veld **Goedgekeurd door**.</span><span class="sxs-lookup"><span data-stu-id="de734-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="de734-121">Selecteer de persoon die verantwoordelijk is voor het goedkeuren van productmodellen voor gebruik in bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="de734-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="de734-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="de734-122">Select **OK**.</span></span>
1. <span data-ttu-id="de734-123">Selecteer een optie in het veld **Methode voor prijscalculatie**.</span><span class="sxs-lookup"><span data-stu-id="de734-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="de734-124">Activeer de productmodelversie.</span><span class="sxs-lookup"><span data-stu-id="de734-124">Activate the product model version.</span></span> <span data-ttu-id="de734-125">Het is alleen mogelijk om één product tegelijk actief te hebben voor een productmodel.</span><span class="sxs-lookup"><span data-stu-id="de734-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="de734-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="de734-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]