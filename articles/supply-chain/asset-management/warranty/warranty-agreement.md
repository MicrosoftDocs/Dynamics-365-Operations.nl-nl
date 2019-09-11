---
title: Garantieovereenkomsten
description: In dit onderwerp worden garantieovereenkomsten in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71905d5b362c80d48b78210b59cacfb1e7899757
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874688"
---
# <a name="warranty-agreements"></a><span data-ttu-id="d76dd-103">Garantieovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="d76dd-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="d76dd-104">In Asset Management kunt u garantievoorwaarden instellen die kunnen worden verbonden met een activum of een activatype.</span><span class="sxs-lookup"><span data-stu-id="d76dd-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="d76dd-105">Er worden garantievoorwaarden gemaakt voor een specifieke periode.</span><span class="sxs-lookup"><span data-stu-id="d76dd-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="d76dd-106">U kunt de garantie instellen om volledige dekking of een deel van de dekking te bieden en u kunt voorwaarden instellen die zijn gerelateerd aan uren, onkosten en artikelen.</span><span class="sxs-lookup"><span data-stu-id="d76dd-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="d76dd-107">De eerste stap is het maken van garantieovereenkomsten voor leveranciers die u voor uw apparatuur hebt.</span><span class="sxs-lookup"><span data-stu-id="d76dd-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="d76dd-108">Vervolgens koppelt u garantieovereenkomsten aan activa of activatypen.</span><span class="sxs-lookup"><span data-stu-id="d76dd-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="d76dd-109">Garantieovereenkomsten met leveranciers worden alleen voor informatieve doeleinden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d76dd-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="d76dd-110">Als er een leveranciersgarantie is ingesteld voor een activum, ziet u de dekkingsperiode van de garantie op de activa.</span><span class="sxs-lookup"><span data-stu-id="d76dd-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="d76dd-111">Een garantieovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="d76dd-111">Create a warranty agreement</span></span>

<span data-ttu-id="d76dd-112">Een garantieovereenkomst kan meerdere overeenkomstregels bevatten om de garantie voor werkuren, onkosten en artikelen te dekken.</span><span class="sxs-lookup"><span data-stu-id="d76dd-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="d76dd-113">Selecteer **Activabeheer** \> **Instellen** \> **Activa** \> **Garantie**.</span><span class="sxs-lookup"><span data-stu-id="d76dd-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="d76dd-114">Selecteer **Nieuw** om een product te maken.</span><span class="sxs-lookup"><span data-stu-id="d76dd-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="d76dd-115">Voer in het veld **Garantie** een garantie-id in.</span><span class="sxs-lookup"><span data-stu-id="d76dd-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="d76dd-116">Voer in het veld **Naam** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="d76dd-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="d76dd-117">Het Sneltabblad **Details** geeft het veld **Activa** het aantal actieve activa weer dat de garantieovereenkomst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d76dd-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="d76dd-118">Voer op de Sneltabbladen **Urengarantie** en **Artikelgarantie** de volgende stappen uit om regels toe te voegen die moeten worden opgenomen in een garantieovereenkomst die betrekking heeft op uren of artikelen:</span><span class="sxs-lookup"><span data-stu-id="d76dd-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="d76dd-119">Selecteer **Regel toevoegen** om een nieuwe voorwaarde toe te voegen aan de groep.</span><span class="sxs-lookup"><span data-stu-id="d76dd-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="d76dd-120">In het veld **Regel** wordt automatisch een volgnummer voor de regel ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="d76dd-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="d76dd-121">Selecteer in het veld **Periode** het type garantieperiode.</span><span class="sxs-lookup"><span data-stu-id="d76dd-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="d76dd-122">Typ een getal in het veld **Interval**.</span><span class="sxs-lookup"><span data-stu-id="d76dd-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="d76dd-123">Dit veld bepaalt het aantal Perioden waarvoor de garantie geldig moet zijn.</span><span class="sxs-lookup"><span data-stu-id="d76dd-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="d76dd-124">Voer in veld **Percentage** het dekkingspercentage voor de garantieregel in.</span><span class="sxs-lookup"><span data-stu-id="d76dd-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="d76dd-125">Het percentage geeft aan hoeveel door uw bedrijf wordt gedekt.</span><span class="sxs-lookup"><span data-stu-id="d76dd-125">The percentage indicates how much is covered by your company.</span></span>

![Figuur 1](media/01-warranty.png)
