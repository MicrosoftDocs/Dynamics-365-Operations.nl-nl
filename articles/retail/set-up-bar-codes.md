---
title: Streepjescodes instellen
description: In dit artikel wordt beschreven hoe u barcodes in Dynamics 365 Retail gebruikt.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b7a668f8b44c5f573957a91ab19a8b7fac7a95ba
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024885"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="18cd8-103">Streepjescodes instellen</span><span class="sxs-lookup"><span data-stu-id="18cd8-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18cd8-104">In dit artikel wordt beschreven hoe u barcodes in Dynamics 365 Retail gebruikt.</span><span class="sxs-lookup"><span data-stu-id="18cd8-104">This article describes how to use bar codes in Dynamics 365 Retail.</span></span>

<span data-ttu-id="18cd8-105">U kunt streepjescodes gebruiken voor het kopen en verkopen van producten, om productvarianten bij te houden en om klanten en werknemers in te stellen.</span><span class="sxs-lookup"><span data-stu-id="18cd8-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="18cd8-106">U kunt streepjescodes gebruiken om kortingbonnen, cadeaubonnen en creditnota's uit te geven en te verwerken.</span><span class="sxs-lookup"><span data-stu-id="18cd8-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="18cd8-107">U kunt detailhandelproducten instellen met standaardstreepjescodes of met op maat gemaakte, interne streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="18cd8-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="18cd8-108">Producten kunnen meer dan één streepjescode hebben.</span><span class="sxs-lookup"><span data-stu-id="18cd8-108">Products can have more than one bar code.</span></span> <span data-ttu-id="18cd8-109">Een product kan bijvoorbeeld meerdere streepjescodes hebben indien het afkomstig is van verschillende fabrikanten of indien er varianten zijn op basis van grootte, stijl of kleur.</span><span class="sxs-lookup"><span data-stu-id="18cd8-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="18cd8-110">Streepjescodes kunnen het gewicht of de prijs van het product bevatten.</span><span class="sxs-lookup"><span data-stu-id="18cd8-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="18cd8-111">Streepjescodemaskers zijn sjablonen die worden gebruikt voor het maken van streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="18cd8-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="18cd8-112">Als u aan elke variantcombinatie een unieke streepjescode toewijst, kunt u de streepjescode van het artikel bij de kassa scannen en het programma laten bepalen welke variant van het product wordt verkocht.</span><span class="sxs-lookup"><span data-stu-id="18cd8-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="18cd8-113">Op die manier kunt u ook verkoopstatistieken op basis van varianten verzamelen en weergeven.</span><span class="sxs-lookup"><span data-stu-id="18cd8-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="18cd8-114">Aan elke grootte-, kleur- en stijlgroep kan een uniek nummer worden toegewezen dat die groep in de streepjescode identificeert.</span><span class="sxs-lookup"><span data-stu-id="18cd8-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="18cd8-115">Retail gebruikt het streepjescodemasker om automatisch voor elke variantcombinatie streepjescodes te genereren.</span><span class="sxs-lookup"><span data-stu-id="18cd8-115">Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="18cd8-116">Deze functionaliteit kan nuttig zijn als er veel maten, kleuren en stijlen zijn, aangezien het aantal combinaties aanzienlijk kan oplopen met elke extra toegevoegde variantcode.</span><span class="sxs-lookup"><span data-stu-id="18cd8-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="18cd8-117">Als deze functie niet wordt gebruikt, moeten streepjescodes handmatig worden toegewezen aan elke combinatie die een productvariant representeert.</span><span class="sxs-lookup"><span data-stu-id="18cd8-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="18cd8-118">U kunt de streepjescodes handmatig of automatisch maken.</span><span class="sxs-lookup"><span data-stu-id="18cd8-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="18cd8-119">Om streepjescodes te maken, voert u de volgende taken uit in de volgorde waarin ze zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="18cd8-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="18cd8-120">[Stel tekens van streepjescodemaskers in](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="18cd8-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="18cd8-121">[Stel streepjescodemaskers in](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="18cd8-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="18cd8-122">Stel de instellingen voor streepjescodes in.</span><span class="sxs-lookup"><span data-stu-id="18cd8-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="18cd8-123">Maak streepjescodes voor producten.</span><span class="sxs-lookup"><span data-stu-id="18cd8-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18cd8-124">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="18cd8-124">Additional resources</span></span>

[<span data-ttu-id="18cd8-125">Streepjescodemaskers instellen</span><span class="sxs-lookup"><span data-stu-id="18cd8-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
