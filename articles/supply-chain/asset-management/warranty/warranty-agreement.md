---
title: Garantieovereenkomsten
description: In dit onderwerp worden garantieovereenkomsten in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425583"
---
# <a name="warranty-agreements"></a><span data-ttu-id="d707e-103">Garantieovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="d707e-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="d707e-104">In Asset Management kunt u garantievoorwaarden instellen die kunnen worden verbonden met een activum of een activatype.</span><span class="sxs-lookup"><span data-stu-id="d707e-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="d707e-105">Er worden garantievoorwaarden gemaakt voor een specifieke periode.</span><span class="sxs-lookup"><span data-stu-id="d707e-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="d707e-106">U kunt de garantie instellen om volledige dekking of een deel van de dekking te bieden en u kunt voorwaarden instellen die zijn gerelateerd aan uren, onkosten en artikelen.</span><span class="sxs-lookup"><span data-stu-id="d707e-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="d707e-107">De eerste stap is het maken van garantieovereenkomsten voor leveranciers die u voor uw apparatuur hebt.</span><span class="sxs-lookup"><span data-stu-id="d707e-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="d707e-108">Vervolgens koppelt u garantieovereenkomsten aan activa of activatypen.</span><span class="sxs-lookup"><span data-stu-id="d707e-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="d707e-109">Garantieovereenkomsten met leveranciers worden alleen voor informatieve doeleinden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d707e-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="d707e-110">Als er een leveranciersgarantie is ingesteld voor een activum, ziet u de dekkingsperiode van de garantie op de activa.</span><span class="sxs-lookup"><span data-stu-id="d707e-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="d707e-111">Een garantieovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="d707e-111">Create a warranty agreement</span></span>

<span data-ttu-id="d707e-112">Een garantieovereenkomst kan meerdere overeenkomstregels bevatten om de garantie voor werkuren, onkosten en artikelen te dekken.</span><span class="sxs-lookup"><span data-stu-id="d707e-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="d707e-113">Selecteer **Activabeheer** \> **Instellen** \> **Activa** \> **Garantie**.</span><span class="sxs-lookup"><span data-stu-id="d707e-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="d707e-114">Selecteer **Nieuw** om een product te maken.</span><span class="sxs-lookup"><span data-stu-id="d707e-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="d707e-115">Voer in het veld **Garantie** een garantie-id in.</span><span class="sxs-lookup"><span data-stu-id="d707e-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="d707e-116">Voer in het veld **Naam** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="d707e-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="d707e-117">Het Sneltabblad **Details** geeft het veld **Activa** het aantal actieve activa weer dat de garantieovereenkomst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d707e-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="d707e-118">Voer op het sneltabblad **Garantieregels** de volgende stappen uit om regels toe te voegen die moeten worden opgenomen in een garantieovereenkomst:</span><span class="sxs-lookup"><span data-stu-id="d707e-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="d707e-119">Selecteer **Regel toevoegen** om een nieuwe voorwaarde toe te voegen aan de groep.</span><span class="sxs-lookup"><span data-stu-id="d707e-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="d707e-120">In het veld **Regel** wordt automatisch een volgnummer voor de regel ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="d707e-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="d707e-121">Selecteer in het veld **Periode** het type garantieperiode.</span><span class="sxs-lookup"><span data-stu-id="d707e-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="d707e-122">Typ een getal in het veld **Interval**.</span><span class="sxs-lookup"><span data-stu-id="d707e-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="d707e-123">Dit veld bepaalt het aantal Perioden waarvoor de garantie geldig moet zijn.</span><span class="sxs-lookup"><span data-stu-id="d707e-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="d707e-124">Voer in veld **Percentage** het dekkingspercentage voor de garantieregel in.</span><span class="sxs-lookup"><span data-stu-id="d707e-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="d707e-125">Het percentage geeft aan hoeveel door uw bedrijf wordt gedekt.</span><span class="sxs-lookup"><span data-stu-id="d707e-125">The percentage indicates how much is covered by your company.</span></span>

![Pagina Garantie](media/01-warranty.png)
