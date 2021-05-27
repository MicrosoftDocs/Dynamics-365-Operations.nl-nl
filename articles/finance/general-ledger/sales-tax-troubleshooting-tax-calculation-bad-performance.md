---
title: Prestatie van de belastingberekening heeft gevolgen voor transacties
description: Dit onderwerp bevat informatie over het oplossen van problemen die betrekking hebben op de prestatie van de belastingberekening en de gevolgen ervan op transacties.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020134"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="26784-103">Prestatie van de belastingberekening heeft gevolgen voor transacties</span><span class="sxs-lookup"><span data-stu-id="26784-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26784-104">Soms ondervindt een transactie gevolgen door prestatieproblemen van de belastingberekening.</span><span class="sxs-lookup"><span data-stu-id="26784-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="26784-105">Volg de stappen in de volgende secties zoals vereist om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="26784-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="26784-106">Bekijk het aantal transactieregels</span><span class="sxs-lookup"><span data-stu-id="26784-106">Review the transaction line count</span></span>

<span data-ttu-id="26784-107">Bepaal of de transactie een groot aantal regels heeft (bijvoorbeeld meer dan honderd).</span><span class="sxs-lookup"><span data-stu-id="26784-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="26784-108">Als dat niet zo is, gaat u verder met de volgende sectie.</span><span class="sxs-lookup"><span data-stu-id="26784-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="26784-109">Als de transactie meerdere honderden regels heeft, stel de belastingberekening uit.</span><span class="sxs-lookup"><span data-stu-id="26784-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="26784-110">Zie [Uitgestelde belastingberekening inschakelen in journalen](enable-delayed-tax-calculation.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="26784-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="26784-111">Vervolgens kunt u bepalen of aan een van de volgende voorwaarden wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="26784-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="26784-112">Er zijn importtransacties uit grote bestanden.</span><span class="sxs-lookup"><span data-stu-id="26784-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="26784-113">Dezelfde transactie voor belastingberekening wordt tegelijkertijd verwerkt in meerdere sessies.</span><span class="sxs-lookup"><span data-stu-id="26784-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="26784-114">De transactie heeft meerdere regels en de weergaven worden realtime bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="26784-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="26784-115">Het veld **Berekend btw-bedrag** op de pagina **Algemeen journaal** wordt bijvoorbeeld in realtime bijgewerkt als er regelvelden worden veranderd.</span><span class="sxs-lookup"><span data-stu-id="26784-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="26784-116">[![Het veld Berekend btw-bedrag op de pagina Journaalboekstuk](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="26784-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="26784-117">Als aan een van deze voorwaarden is voldaan, stel de belastingberekening uit.</span><span class="sxs-lookup"><span data-stu-id="26784-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="26784-118">Controleer de aanroepstapel</span><span class="sxs-lookup"><span data-stu-id="26784-118">Review the call stack</span></span>

<span data-ttu-id="26784-119">Controleer de aanroepstapel om te bepalen of de belastingberekening meerdere keren wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="26784-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="26784-120">Als dit niet zo is, gaat u verder met de volgende sectie.</span><span class="sxs-lookup"><span data-stu-id="26784-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="26784-121">Als de aanroepstapel meerdere keren wordt aangeroepen, volgt u deze stappen om de belastingberekeningstijden te verminderen.</span><span class="sxs-lookup"><span data-stu-id="26784-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="26784-122">Als er in het journaal rekening is gehouden met de transactie, stel dan de belastingberekening uit.</span><span class="sxs-lookup"><span data-stu-id="26784-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="26784-123">Zie [Uitgestelde belastingberekening inschakelen in journalen](enable-delayed-tax-calculation.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="26784-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="26784-124">Als de transactie een inkooporder is en de toepassingsversie is hoger dan 10.0.15, kunt u de belastingberekening uitstellen tot de definitieve berekening door het inschakelen van de flighting voor **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="26784-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="26784-125">Controleer de tijdlijn van de aanroepstapel</span><span class="sxs-lookup"><span data-stu-id="26784-125">Review the call stack timeline</span></span>

<span data-ttu-id="26784-126">Controleer de tijdlijn van de aanroepstapel om te bepalen of de volgende problemen bestaan.</span><span class="sxs-lookup"><span data-stu-id="26784-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="26784-127">Als dat zo is, kunt u het probleem oplossen door flighting in te schakelen voor **TaxUncommittedDoIsolateScopeFlighting**.</span><span class="sxs-lookup"><span data-stu-id="26784-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="26784-128">De transactie zorgt ervoor dat het systeem niet meer reageert totdat de sessie is beëindigd.</span><span class="sxs-lookup"><span data-stu-id="26784-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="26784-129">Daarom kan de transactie het belastingresultaat niet berekenen.</span><span class="sxs-lookup"><span data-stu-id="26784-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="26784-130">In de volgende afbeelding ziet u het bericht 'Sessie beëindigd' dat u ontvangt.</span><span class="sxs-lookup"><span data-stu-id="26784-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="26784-131">[![Bericht Sessie beëindigd](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="26784-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="26784-132">De methoden **TaxUncommitted** hebben meer tijd nodig dan andere methoden.</span><span class="sxs-lookup"><span data-stu-id="26784-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="26784-133">In de volgende afbeelding heeft bijvoorbeeld de methode **TaxUncommitted::updateTaxUncommitted()** 43.347,42 seconden nodig, terwijl andere methoden maar 0,09 seconde nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="26784-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="26784-134">[![Duur van methode](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="26784-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="26784-135">Belastingberekening aanpassen en aanroepen</span><span class="sxs-lookup"><span data-stu-id="26784-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="26784-136">Wanneer u een aanpassing maakt, moet u de belastingberekening bij de methode **insert()** of **update()** niet bij elke regel aanroepen.</span><span class="sxs-lookup"><span data-stu-id="26784-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="26784-137">Belastingberekening moet worden aangeroepen op transactieniveau.</span><span class="sxs-lookup"><span data-stu-id="26784-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="26784-138">Bekijk of er een aanpassing bestaat</span><span class="sxs-lookup"><span data-stu-id="26784-138">Determine whether customization exists</span></span>

<span data-ttu-id="26784-139">Als u de stappen in de vorige secties hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat.</span><span class="sxs-lookup"><span data-stu-id="26784-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="26784-140">Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="26784-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
