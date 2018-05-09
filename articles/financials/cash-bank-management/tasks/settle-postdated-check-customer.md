--- 
title: Een gepostdateerde cheque van een klant vereffenen
description: U kunt een gepostdateerde cheque vereffenen nadat de cheque is verrekend door de bank.
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 95651e602bd4f576a7fcf96379f61252cdf392f6
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="0eff2-103">Een gepostdateerde cheque van een klant vereffenen</span><span class="sxs-lookup"><span data-stu-id="0eff2-103">Settle a postdated check from a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0eff2-104">U kunt een gepostdateerde cheque vereffenen nadat de cheque is verrekend door de bank.</span><span class="sxs-lookup"><span data-stu-id="0eff2-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="0eff2-105">Met deze financiële transactie boekt u ook de overbruggingsrekeningtransactie over voor de gepostdateerde cheque.</span><span class="sxs-lookup"><span data-stu-id="0eff2-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="0eff2-106">De volgende taken moeten zijn voltooid voordat u deze start.</span><span class="sxs-lookup"><span data-stu-id="0eff2-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="0eff2-107">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="0eff2-107">Set up postdated checks</span></span>

2) <span data-ttu-id="0eff2-108">Een gepostdateerde cheque voor een klant registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="0eff2-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="0eff2-109">De rol van deze taakbegeleidingen is penningmeester.</span><span class="sxs-lookup"><span data-stu-id="0eff2-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="0eff2-110">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0eff2-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="0eff2-111">Ga naar Crediteringen en aanmaningen > Query's en rapporten > Betalingen > Gepostdateerde cheques van klant.</span><span class="sxs-lookup"><span data-stu-id="0eff2-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="0eff2-112">Klik op Vereffenen.</span><span class="sxs-lookup"><span data-stu-id="0eff2-112">Click Settle.</span></span>
3. <span data-ttu-id="0eff2-113">Klik op Aflossingstransacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="0eff2-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="0eff2-114">Vereffen de klantrekening voor de chequetransactie.</span><span class="sxs-lookup"><span data-stu-id="0eff2-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="0eff2-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0eff2-115">Close the page.</span></span>
5. <span data-ttu-id="0eff2-116">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="0eff2-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="0eff2-117">Selecteer een optie in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="0eff2-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="0eff2-118">Schakel het selectievakje Alleen door de gebruiker gemaakte journalen weergeven in of uit.</span><span class="sxs-lookup"><span data-stu-id="0eff2-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="0eff2-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0eff2-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="0eff2-120">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="0eff2-120">Click Lines.</span></span>
10. <span data-ttu-id="0eff2-121">Klik op Boekstuk.</span><span class="sxs-lookup"><span data-stu-id="0eff2-121">Click Voucher.</span></span>
11. <span data-ttu-id="0eff2-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0eff2-122">Close the page.</span></span>


