---
title: De kwaliteit van goederen inspecteren
description: In dit onderwerp wordt beschreven hoe u kwaliteitsorders verwerkt.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956129"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="e0522-103">De kwaliteit van goederen inspecteren</span><span class="sxs-lookup"><span data-stu-id="e0522-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0522-104">In dit onderwerp wordt beschreven hoe u kwaliteitsorders verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e0522-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="e0522-105">Kwaliteitscontroles worden gewoonlijk uitgevoerd door een kwaliteitsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="e0522-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="e0522-106">Als de standaarddemogegevens zijn geïnstalleerd, kunt u deze gebruiken om de procedures in dit onderwerp uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="e0522-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="e0522-107">Om de demogegevens te gebruiken, selecteert u de rechtspersoon *USMF* voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="e0522-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="e0522-108">Vervolgens moet u inkooporder *000016* bevestigen en een productontvangstbon boeken.</span><span class="sxs-lookup"><span data-stu-id="e0522-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="e0522-109">Een kwaliteitsorder wordt automatisch gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e0522-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="e0522-110">Stap 1: Een kwaliteitsorder selecteren</span><span class="sxs-lookup"><span data-stu-id="e0522-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="e0522-111">Volg deze stappen om een kwaliteitsorder te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e0522-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="e0522-112">Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.</span><span class="sxs-lookup"><span data-stu-id="e0522-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="e0522-113">Selecteer de kwaliteitsorder die is gegenereerd voordat u deze procedure startte.</span><span class="sxs-lookup"><span data-stu-id="e0522-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="e0522-114">Stap 2: Testresultaten vastleggen</span><span class="sxs-lookup"><span data-stu-id="e0522-114">Step 2: Record test results</span></span>

<span data-ttu-id="e0522-115">Volg deze stappen om testresultaten te registreren.</span><span class="sxs-lookup"><span data-stu-id="e0522-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="e0522-116">Selecteer **Resultaten**.</span><span class="sxs-lookup"><span data-stu-id="e0522-116">Select **Results**.</span></span>
1. <span data-ttu-id="e0522-117">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="e0522-117">Select **Edit**.</span></span>
1. <span data-ttu-id="e0522-118">Voer in het veld **Resultaathoeveelheid** een getal in.</span><span class="sxs-lookup"><span data-stu-id="e0522-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="e0522-119">Selecteer de gewenste record in het veld **Resultaat**.</span><span class="sxs-lookup"><span data-stu-id="e0522-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="e0522-120">In dit voorbeeld is het resultaat gebaseerd op een vooraf gedefinieerd resultaat.</span><span class="sxs-lookup"><span data-stu-id="e0522-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="e0522-121">Normaliter registreert u een specifieker testresultaat, bijvoorbeeld een afmeting of andere dimensie.</span><span class="sxs-lookup"><span data-stu-id="e0522-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="e0522-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e0522-122">Select **Save**.</span></span>
1. <span data-ttu-id="e0522-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e0522-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="e0522-124">Stap 3: De kwaliteitsorder valideren</span><span class="sxs-lookup"><span data-stu-id="e0522-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="e0522-125">Volg deze stappen om de kwaliteitsorder te valideren.</span><span class="sxs-lookup"><span data-stu-id="e0522-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="e0522-126">Selecteer **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="e0522-126">Select **Validate**.</span></span>
1. <span data-ttu-id="e0522-127">Selecteer in het veld **Gevalideerd door** de gebruiker die de inspectie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="e0522-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="e0522-128">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="e0522-128">Select **Select**.</span></span>
1. <span data-ttu-id="e0522-129">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0522-129">Select **OK**.</span></span>
1. <span data-ttu-id="e0522-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e0522-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
