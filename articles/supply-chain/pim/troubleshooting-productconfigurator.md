---
title: Problemen met de productconfigurator oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met de productconfigurator.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999601"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="a3ce8-103">Problemen met de productconfigurator oplossen</span><span class="sxs-lookup"><span data-stu-id="a3ce8-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="a3ce8-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met de productconfigurator.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="a3ce8-105">De tekst van een artikel wordt overschreven wanneer ik een product configureer op een verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a3ce8-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="a3ce8-106">Issue description</span></span>

<span data-ttu-id="a3ce8-107">Dit probleem doet zich voor wanneer u een verkooporderregel voor een configureerbaar artikel maakt en vervolgens de tekst van het artikel wijzigt.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="a3ce8-108">Wanneer u het artikel configureert en vervolgens **OK** selecteert, wordt de tekst overschreven met de standaardtekst.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a3ce8-109">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="a3ce8-109">Issue resolution</span></span>

<span data-ttu-id="a3ce8-110">Dit gedrag is verwacht.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-110">This behavior is expected.</span></span> <span data-ttu-id="a3ce8-111">Het tekstveld bevat de variantnaam, die alleen wordt ingevuld nadat u de regel hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="a3ce8-112">Daarom moet u de tekst wijzigen nadat u de regel hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="a3ce8-113">De kenmerken van gehele getallen worden onjuist afgerond wanneer de productconfiguratiemodellen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a3ce8-114">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="a3ce8-114">Issue description</span></span>

<span data-ttu-id="a3ce8-115">Dit probleem kan optreden wanneer u de volgende reeks acties uitvoert:</span><span class="sxs-lookup"><span data-stu-id="a3ce8-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="a3ce8-116">Stel de volgende kenmerken in op een productieconfiguratiemodel:</span><span class="sxs-lookup"><span data-stu-id="a3ce8-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="a3ce8-117">Invoer (geheel getal)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-117">Input (integer)</span></span>
    - <span data-ttu-id="a3ce8-118">Percentage (decimaal)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-118">Percent (decimal)</span></span>
    - <span data-ttu-id="a3ce8-119">Resultaat (geheel getal)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-119">Result (integer)</span></span>

2. <span data-ttu-id="a3ce8-120">Maak een berekening die de volgende expressie bevat:</span><span class="sxs-lookup"><span data-stu-id="a3ce8-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="a3ce8-121">*Resultaat* = *invoer* × *procent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="a3ce8-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="a3ce8-122">In dit geval wordt het resultaat van het gehele getal niet altijd juist afgerond.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="a3ce8-123">De invoer is bijvoorbeeld 1000 en het percentage is 2,40.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="a3ce8-124">Daarom verwacht u dat het resultaat van een geheel getal 24 is, omdat 2,40 procent van 1000 24 is (of 24,00 in decimale notatie).</span><span class="sxs-lookup"><span data-stu-id="a3ce8-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="a3ce8-125">In plaats daarvan wordt het resultaat weergegeven als 23.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="a3ce8-126">Wanneer het percentage echter 2,39 is, wordt de berekening afgerond naar 24 in plaats van 23.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="a3ce8-127">Wanneer het percentage 2,50 is, wordt de berekening afgerond naar 25, zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a3ce8-128">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="a3ce8-128">Issue resolution</span></span>

<span data-ttu-id="a3ce8-129">Dit probleem doet zich voor vanwege de manier waarop getallen door Microsoft Solver Foundation intern worden aangeduid met breuken.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="a3ce8-130">Voor het bovenstaande voorbeeld wordt het resultaat van de berekening waarbij het percentage 2,40 is, weergegeven als 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="a3ce8-131">Wanneer .NET deze waarde als een geheel getal converteert, wordt 23 geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="a3ce8-132">Dit gedrag wordt niet gewijzigd, omdat andere scenario's hiervan afhankelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="a3ce8-133">Voor het voorgaande voorbeeld kunt u het probleem oplossen door een extra, decimaal kenmerk en een berekening te introduceren.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="a3ce8-134">Stel bijvoorbeeld de volgende kenmerken in op een productieconfiguratiemodel:</span><span class="sxs-lookup"><span data-stu-id="a3ce8-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="a3ce8-135">Invoer (geheel getal)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-135">Input (integer)</span></span>
- <span data-ttu-id="a3ce8-136">Percentage (decimaal)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-136">Percent (decimal)</span></span>
- <span data-ttu-id="a3ce8-137">ResultDecimal (decimaal)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="a3ce8-138">ResultInteger (geheel getal)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-138">ResultInteger (integer)</span></span>

<span data-ttu-id="a3ce8-139">Vervolgens kunt u de volgende berekeningen toevoegen:</span><span class="sxs-lookup"><span data-stu-id="a3ce8-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="a3ce8-140">*ResultDecimal* = *invoer* × *procent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="a3ce8-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="a3ce8-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="a3ce8-141">*ResultInteger* = *ResultDecimal*</span></span>
