---
title: Journaalboekingen tegenboeken
description: Dit onderwerp beschrijft mogelijkheden waarmee u boekstukken kunt tegenboeken uit de lijst met boekstuktransacties of vanuit financiële journalen.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248580"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="06ca8-103">Journaalboekingen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="06ca8-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06ca8-104">In dit onderwerp worden Microsoft Dynamics 365 Finance-mogelijkheden beschreven waarmee u een volledig journaal kunt tegenboeken of een of meer boekstukken kunt tegenboeken uit de lijst met boekstuktransacties, ongeacht de oorsprong.</span><span class="sxs-lookup"><span data-stu-id="06ca8-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="06ca8-105">Journalen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="06ca8-105">Reversing journals</span></span>

<span data-ttu-id="06ca8-106">U kunt journaalregels afzonderlijk tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="06ca8-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="06ca8-107">Bij het terugdraaien van journaalboekingen kunt u ook een heel financieel journaal tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="06ca8-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="06ca8-108">Een journaal tegenboeken:</span><span class="sxs-lookup"><span data-stu-id="06ca8-108">To reverse a journal:</span></span> 
- <span data-ttu-id="06ca8-109">Open het financiële journaal en filter op geboekte journalen</span><span class="sxs-lookup"><span data-stu-id="06ca8-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="06ca8-110">Klik op het menu Tegenboeken bovenaan de pagina</span><span class="sxs-lookup"><span data-stu-id="06ca8-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="06ca8-111">Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="06ca8-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="06ca8-112">Selecteer Ja als u de bestaande transactiedatums wilt gebruiken of Nee als u een nieuwe transactiedatum wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="06ca8-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="06ca8-113">In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en wilt u een nieuwe transactiedatum voor het tegenboeken invoeren.</span><span class="sxs-lookup"><span data-stu-id="06ca8-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="06ca8-114">Als u Nee hebt geselecteerd, voert u een transactiedatum voor het tegenboeken in.</span><span class="sxs-lookup"><span data-stu-id="06ca8-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="06ca8-115">Voer een opmerking invoeren die u wilt toevoegen aan de tegenboektransactie</span><span class="sxs-lookup"><span data-stu-id="06ca8-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="06ca8-116">Klik op de knop Tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="06ca8-116">Click the Reverse button</span></span>

<span data-ttu-id="06ca8-117">De transacties worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="06ca8-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="06ca8-118">Als het aantal boekstukregels hoger is dan 100 regels, wordt het tegenboekproces uitgevoerd met het batchproces.</span><span class="sxs-lookup"><span data-stu-id="06ca8-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="06ca8-119">U kunt de resultaten van de tegenboeking bekijken door de opmerkingen in de batchtaak te bekijken die is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="06ca8-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="06ca8-120">Alle fouten worden vastgelegd in de historie van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="06ca8-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="06ca8-121">Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het tegenboekproces onmiddellijk uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="06ca8-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="06ca8-122">De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk wordt weer gegeven dat niet kan worden teruggeboekt, en de reden waarom het niet kan worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="06ca8-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="06ca8-123">Klik OK om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="06ca8-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="06ca8-124">Boekstukken tegenboeken vanuit de lijst met boekstuktransacties.</span><span class="sxs-lookup"><span data-stu-id="06ca8-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="06ca8-125">U kunt ook boekstukken omkeren uit de **Lijst met boekstuktransacties** in alle subadministraties.</span><span class="sxs-lookup"><span data-stu-id="06ca8-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="06ca8-126">Daarnaast kunt u meerdere boekstukken tegelijk tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="06ca8-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="06ca8-127">Een of meer boekstukken tegenboeken:</span><span class="sxs-lookup"><span data-stu-id="06ca8-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="06ca8-128">Klik op het menu Tegenboeken bovenaan de pagina</span><span class="sxs-lookup"><span data-stu-id="06ca8-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="06ca8-129">Het totale aantal boekstukken en boekstukregels wordt weergegeven, evenals het totale bedrag van de regels die worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="06ca8-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="06ca8-130">Selecteer Ja als u de bestaande transactiedatums wilt gebruiken of Nee als u een nieuwe transactiedatum wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="06ca8-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="06ca8-131">In sommige gevallen wordt de periode van de oorspronkelijke transactie afgesloten en wilt u een nieuwe transactiedatum voor het tegenboeken invoeren.</span><span class="sxs-lookup"><span data-stu-id="06ca8-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="06ca8-132">Als u Nee hebt geselecteerd, voert u een transactiedatum voor het tegenboeken in.</span><span class="sxs-lookup"><span data-stu-id="06ca8-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="06ca8-133">Voer een opmerking invoeren die u wilt toevoegen aan de tegenboektransactie</span><span class="sxs-lookup"><span data-stu-id="06ca8-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="06ca8-134">Klik op de knop Tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="06ca8-134">Click the Reverse button</span></span>

<span data-ttu-id="06ca8-135">De transacties worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="06ca8-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="06ca8-136">Als het aantal boekstukregels hoger is dan 100 regels, wordt het tegenboekproces uitgevoerd met het batchproces.</span><span class="sxs-lookup"><span data-stu-id="06ca8-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="06ca8-137">U kunt de resultaten van de tegenboeking bekijken door de opmerkingen in de batchtaak te bekijken die is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="06ca8-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="06ca8-138">Alle fouten worden vastgelegd in de historie van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="06ca8-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="06ca8-139">Als het aantal boekstukregels 100 regels of minder bedraagt, wordt het tegenboekproces onmiddellijk uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="06ca8-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="06ca8-140">De resultaten worden weergegeven in een dialoogvenster waarin een boekstuk wordt weer gegeven dat niet kan worden teruggeboekt, en de reden waarom het niet kan worden teruggeboekt.</span><span class="sxs-lookup"><span data-stu-id="06ca8-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="06ca8-141">Klik OK om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="06ca8-141">Click on Ok to close the dialog.</span></span>

