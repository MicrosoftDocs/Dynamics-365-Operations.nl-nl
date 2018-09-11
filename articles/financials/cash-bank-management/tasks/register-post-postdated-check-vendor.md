--- 
title: Een gepostdateerde cheque voor een leverancier registreren en boeken
description: U kunt de details van een gepostdateerde cheque registreren voordat u de cheque aan een leverancier uitschrijft door het journaalboekstuk te gebruiken.
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3b69178124e0bced65232277c422ceb5986e1a76
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="a5daf-103">Een gepostdateerde cheque voor een leverancier registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="a5daf-103">Register and post a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5daf-104">U kunt de details van een gepostdateerde cheque registreren voordat u de cheque aan een leverancier uitschrijft door het journaalboekstuk te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a5daf-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="a5daf-105">U kunt de gepostdateerde cheque ook boeken en financiële transacties genereren.</span><span class="sxs-lookup"><span data-stu-id="a5daf-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="a5daf-106">Voordat u een gepostdateerde cheque die u van een leverancier hebt ontvangen, registreert en boekt, voert u de volgende taak uit:</span><span class="sxs-lookup"><span data-stu-id="a5daf-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="a5daf-107">Stel gepostdateerde cheques in op de pagina Contanten en bankbeheer.</span><span class="sxs-lookup"><span data-stu-id="a5daf-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="a5daf-108">De rol van deze taakbegeleidingen is penningmeester.</span><span class="sxs-lookup"><span data-stu-id="a5daf-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="a5daf-109">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a5daf-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a5daf-110">Ga naar Leveranciers > Betalingen > Betalingsjournaal</span><span class="sxs-lookup"><span data-stu-id="a5daf-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="a5daf-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a5daf-111">Click New.</span></span>
3. <span data-ttu-id="a5daf-112">Typ 'VendPay' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a5daf-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="a5daf-113">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="a5daf-113">Click Lines.</span></span>
5. <span data-ttu-id="a5daf-114">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="a5daf-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="a5daf-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a5daf-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a5daf-116">Voer een nummer in het veld Debet in.</span><span class="sxs-lookup"><span data-stu-id="a5daf-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="a5daf-117">Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="a5daf-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a5daf-118">Selecteer de betalingsmethode voor de gepostdateerde cheque</span><span class="sxs-lookup"><span data-stu-id="a5daf-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="a5daf-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5daf-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a5daf-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a5daf-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a5daf-121">Klik op het tabblad Gepostdateerde cheques.</span><span class="sxs-lookup"><span data-stu-id="a5daf-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="a5daf-122">Typ een waarde in het veld Chequenummer.</span><span class="sxs-lookup"><span data-stu-id="a5daf-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="a5daf-123">Typ of wijzig het nummer van de gepostdateerde cheque.</span><span class="sxs-lookup"><span data-stu-id="a5daf-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="a5daf-124">Typ een waarde in het veld Naam van uitgevende bank.</span><span class="sxs-lookup"><span data-stu-id="a5daf-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="a5daf-125">Voer de bankgegevens in voor de uitgevende bank.</span><span class="sxs-lookup"><span data-stu-id="a5daf-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="a5daf-126">Klik op het tabblad Lijst.</span><span class="sxs-lookup"><span data-stu-id="a5daf-126">Click the List tab.</span></span>
15. <span data-ttu-id="a5daf-127">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="a5daf-127">Click Post.</span></span>
16. <span data-ttu-id="a5daf-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a5daf-128">Close the page.</span></span>
17. <span data-ttu-id="a5daf-129">Klik op het tabblad Gepostdateerde cheques.</span><span class="sxs-lookup"><span data-stu-id="a5daf-129">Click the Postdated checks tab.</span></span>


