---
title: Adviesprijsrapporten
description: Dit onderwerp biedt een overzicht van de prijsrapportfunctie die kan worden gebruikt om de komende prijswijzigingen voor de verschillende producten weer te geven.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: e14b029a1420eda6af6e83392f295a071a29842a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972425"
---
# <a name="retail-price-reports"></a><span data-ttu-id="75b6e-103">Adviesprijsrapporten</span><span class="sxs-lookup"><span data-stu-id="75b6e-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="75b6e-104">Om concurrerende prijzen aan hun klanten te bieden wijzigen winkeliers vaak prijzen van hun producten.</span><span class="sxs-lookup"><span data-stu-id="75b6e-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="75b6e-105">Winkelmanagers willen eenvoudig toegang tot recente of komende prijswijzigingen zodat ze de vereiste resources kunnen plannen om de prijsetiketten op de winkelschappen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="75b6e-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="75b6e-106">Met release 10.0 van Retail kan een winkelmanager het rapport **Prijs** openen door te navigeren naar **Alle winkels \> Winkel \> Prijsrapport** en de bijgewerkte prijzen weer te geven voor de producten die zijn gekoppeld aan de winkel.</span><span class="sxs-lookup"><span data-stu-id="75b6e-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="75b6e-107">Om het prijsrapport in te schakelen moet de parameter **Prijsrapport inschakelen voor winkel** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="75b6e-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="75b6e-108">Deze parameter bevindt zich op het tabblad **Commerce-parameters \> Kortingen \> Diversen**. Als de pagina **Prijsrapport** wordt geopend, wordt een dialoogvenster weergegeven met verschillende configuraties.</span><span class="sxs-lookup"><span data-stu-id="75b6e-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="75b6e-109">Hieronder staan de beschikbare configuraties.</span><span class="sxs-lookup"><span data-stu-id="75b6e-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="75b6e-110">Configuratie</span><span class="sxs-lookup"><span data-stu-id="75b6e-110">Configuration</span></span> | <span data-ttu-id="75b6e-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="75b6e-111">Description</span></span> |
|---|---|
| <span data-ttu-id="75b6e-112">Vanaf datum / Tot datum</span><span class="sxs-lookup"><span data-stu-id="75b6e-112">From date / To date</span></span>| <span data-ttu-id="75b6e-113">Het datumbereik waarvoor het prijsrapport moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="75b6e-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="75b6e-114">De duur is momenteel beperkt tot 7 dagen.</span><span class="sxs-lookup"><span data-stu-id="75b6e-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="75b6e-115">Kanaal</span><span class="sxs-lookup"><span data-stu-id="75b6e-115">Channel</span></span>| <span data-ttu-id="75b6e-116">De winkel waarvoor het prijsrapport moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="75b6e-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="75b6e-117">Producten met beschikbare voorraad weergeven</span><span class="sxs-lookup"><span data-stu-id="75b6e-117">Display products with available inventory</span></span>| <span data-ttu-id="75b6e-118">Als u dit op **Ja** instelt, worden de prijzen weergegeven voor alleen die producten die momenteel beschikbare voorraad in de winkel hebben.</span><span class="sxs-lookup"><span data-stu-id="75b6e-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="75b6e-119">Prijzen voor varianten weergeven</span><span class="sxs-lookup"><span data-stu-id="75b6e-119">Display prices for variants</span></span> | <span data-ttu-id="75b6e-120">Als u dit op **Ja** instelt, worden de prijzen van varianten weergegeven met de productmodellen.</span><span class="sxs-lookup"><span data-stu-id="75b6e-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="75b6e-121">Dit moet alleen op **Aan** worden gezet als u variantspecifieke prijzen hebt, omdat het aantal rijen zeer groot kan worden.</span><span class="sxs-lookup"><span data-stu-id="75b6e-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="75b6e-122">In toekomstige versies schakelen we op dimensies gebaseerde prijzen in, zodat de winkelmanager de dimensies kan kiezen waarvoor de prijzen moeten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="75b6e-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="75b6e-123">Producten met prijswijzigingen weergeven</span><span class="sxs-lookup"><span data-stu-id="75b6e-123">Display products with price changes</span></span> | <span data-ttu-id="75b6e-124">Als u dit op **Ja** instelt, verschijnen de prijzen alleen voor datums waarop de prijs is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="75b6e-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="75b6e-125">De prijs voor *één dag vóór* de geselecteerde **vanaf-datum** wordt altijd weergegeven, zodat de winkelmanager eenvoudig kan zien van welke producten de prijs de hele geselecteerde duur lang niet is gewijzigd en ook de huidige prijs kan weergeven.</span><span class="sxs-lookup"><span data-stu-id="75b6e-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="75b6e-126">Nadat het rapport is gegenereerd, kunt u het Excel-bestand downloaden voor extra filtermogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="75b6e-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="75b6e-127">Het prijsrapport kan ook worden gebruikt om de historische prijzen te controleren van producten op datums in het verleden.</span><span class="sxs-lookup"><span data-stu-id="75b6e-127">The price report can also be used to check the historical prices of products for past dates.</span></span>
