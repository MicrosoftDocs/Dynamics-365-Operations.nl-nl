---
title: De kwaliteit van goederen inspecteren
description: In dit onderwerp wordt uitgelegd hoe u een kwaliteitsorder verwerkt.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee5f83b2dad60567341f33a73ce63d01e9da8289
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213970"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="54dfb-103">De kwaliteit van goederen inspecteren</span><span class="sxs-lookup"><span data-stu-id="54dfb-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54dfb-104">In dit onderwerp wordt uitgelegd hoe u een kwaliteitsorder verwerkt.</span><span class="sxs-lookup"><span data-stu-id="54dfb-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="54dfb-105">U kunt deze handleiding uitvoeren in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="54dfb-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="54dfb-106">Voordat u deze voorbeeldprocedure start, moet u aankooporder 000016 bevestigen en een productontvangst boeken.</span><span class="sxs-lookup"><span data-stu-id="54dfb-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="54dfb-107">Hiermee wordt automatisch een kwaliteitsorder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="54dfb-107">This will automatically create a quality order.</span></span> <span data-ttu-id="54dfb-108">Kwaliteitscontroles worden gewoonlijk uitgevoerd door een kwaliteitsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="54dfb-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="54dfb-109">Een kwaliteitsorder selecteren</span><span class="sxs-lookup"><span data-stu-id="54dfb-109">Select a quality order</span></span>
1. <span data-ttu-id="54dfb-110">Ga in het navigatievenster naar **Modules > Voorraadbeheer > Periodieke taken > Kwaliteitsbeheer > Kwaliteitsorders**.</span><span class="sxs-lookup"><span data-stu-id="54dfb-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="54dfb-111">Selecteer de kwaliteitsorder die is gemaakt voordat u deze procedure hebt gestart.</span><span class="sxs-lookup"><span data-stu-id="54dfb-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="54dfb-112">Testresultaten vastleggen</span><span class="sxs-lookup"><span data-stu-id="54dfb-112">Record test results</span></span>
1. <span data-ttu-id="54dfb-113">Selecteer **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="54dfb-113">Select **Results**.</span></span>
2. <span data-ttu-id="54dfb-114">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="54dfb-114">Select **Edit**.</span></span>
3. <span data-ttu-id="54dfb-115">Voer in het veld **Resultaathoeveelheid** een getal in.</span><span class="sxs-lookup"><span data-stu-id="54dfb-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="54dfb-116">Selecteer in het veld **Resultaat** de gewenste record in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="54dfb-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="54dfb-117">In dit voorbeeld is het resultaat gebaseerd op een vooraf gedefinieerd resultaat.</span><span class="sxs-lookup"><span data-stu-id="54dfb-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="54dfb-118">Normaliter registreert u een specifieker testresultaat, bijvoorbeeld een formaat of andere dimensie.</span><span class="sxs-lookup"><span data-stu-id="54dfb-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="54dfb-119">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="54dfb-119">Select **Save**.</span></span>
6. <span data-ttu-id="54dfb-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="54dfb-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="54dfb-121">De kwaliteitsorder valideren</span><span class="sxs-lookup"><span data-stu-id="54dfb-121">Validate the quality order</span></span>
1. <span data-ttu-id="54dfb-122">Selecteer **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="54dfb-122">Select **Validate**.</span></span>
2. <span data-ttu-id="54dfb-123">Selecteer in het veld **Gevalideerd door** de gebruiker die de inspectie uitvoert in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="54dfb-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="54dfb-124">Klik op **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="54dfb-124">Click **Select**.</span></span>
4. <span data-ttu-id="54dfb-125">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="54dfb-125">Select **OK**.</span></span>
5. <span data-ttu-id="54dfb-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="54dfb-126">Close the page.</span></span>

