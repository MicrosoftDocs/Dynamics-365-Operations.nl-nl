---
title: Een gepostdateerde cheque van een klant vereffenen
description: U kunt een gepostdateerde cheque vereffenen nadat de cheque is verrekend door de bank.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abcd6532c294223e768d1a01d97309e35c30edbe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217405"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="03f56-103">Een gepostdateerde cheque van een klant vereffenen</span><span class="sxs-lookup"><span data-stu-id="03f56-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03f56-104">U kunt een gepostdateerde cheque vereffenen nadat de cheque is verrekend door de bank.</span><span class="sxs-lookup"><span data-stu-id="03f56-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="03f56-105">Met deze financiële transactie boekt u ook de overbruggingsrekeningtransactie over voor de gepostdateerde cheque.</span><span class="sxs-lookup"><span data-stu-id="03f56-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="03f56-106">De volgende taken moeten zijn voltooid voordat u deze start.</span><span class="sxs-lookup"><span data-stu-id="03f56-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="03f56-107">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="03f56-107">Set up postdated checks</span></span>

2) <span data-ttu-id="03f56-108">Een gepostdateerde cheque voor een klant registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="03f56-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="03f56-109">De rol van deze taakbegeleidingen is penningmeester.</span><span class="sxs-lookup"><span data-stu-id="03f56-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="03f56-110">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="03f56-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="03f56-111">Ga naar Crediteringen en aanmaningen > Query's en rapporten > Betalingen > Gepostdateerde cheques van klant.</span><span class="sxs-lookup"><span data-stu-id="03f56-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="03f56-112">Klik op Vereffenen.</span><span class="sxs-lookup"><span data-stu-id="03f56-112">Click Settle.</span></span>
3. <span data-ttu-id="03f56-113">Klik op Aflossingstransacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="03f56-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="03f56-114">Vereffen de klantrekening voor de chequetransactie.</span><span class="sxs-lookup"><span data-stu-id="03f56-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="03f56-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="03f56-115">Close the page.</span></span>
5. <span data-ttu-id="03f56-116">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="03f56-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="03f56-117">Selecteer een optie in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="03f56-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="03f56-118">Schakel het selectievakje Alleen door de gebruiker gemaakte journalen weergeven in of uit.</span><span class="sxs-lookup"><span data-stu-id="03f56-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="03f56-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="03f56-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="03f56-120">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="03f56-120">Click Lines.</span></span>
10. <span data-ttu-id="03f56-121">Klik op Boekstuk.</span><span class="sxs-lookup"><span data-stu-id="03f56-121">Click Voucher.</span></span>
11. <span data-ttu-id="03f56-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="03f56-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]