---
title: Een gepostdateerde cheque voor een leverancier vereffenen
description: Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d66caa83df693445c1b1d40ffdc11e8d10cf7426
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239622"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="9c88c-103">Een gepostdateerde cheque voor een leverancier vereffenen</span><span class="sxs-lookup"><span data-stu-id="9c88c-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c88c-104">Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend.</span><span class="sxs-lookup"><span data-stu-id="9c88c-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="9c88c-105">Voer de volgende procedures uit voordat u deze start.</span><span class="sxs-lookup"><span data-stu-id="9c88c-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="9c88c-106">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="9c88c-106">Set up postdated checks</span></span>

2) <span data-ttu-id="9c88c-107">Een gepostdateerde cheque voor een leverancier registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="9c88c-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="9c88c-108">De rol van deze procedure is penningmeester.</span><span class="sxs-lookup"><span data-stu-id="9c88c-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="9c88c-109">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9c88c-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9c88c-110">Ga naar Leveranciers > Betalingen > Gepostdateerde cheques van leverancier.</span><span class="sxs-lookup"><span data-stu-id="9c88c-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="9c88c-111">Klik op Vereffenen.</span><span class="sxs-lookup"><span data-stu-id="9c88c-111">Click Settle.</span></span>
3. <span data-ttu-id="9c88c-112">Klik op Aflossingstransacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="9c88c-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="9c88c-113">Vereffen de leveranciersrekening voor de chequetransactie.</span><span class="sxs-lookup"><span data-stu-id="9c88c-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="9c88c-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9c88c-114">Close the page.</span></span>
5. <span data-ttu-id="9c88c-115">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="9c88c-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="9c88c-116">Selecteer 'Alle' in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="9c88c-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="9c88c-117">Schakel het selectievakje Alleen door de gebruiker gemaakte journalen weergeven in of uit.</span><span class="sxs-lookup"><span data-stu-id="9c88c-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="9c88c-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9c88c-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9c88c-119">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="9c88c-119">Click Lines.</span></span>
10. <span data-ttu-id="9c88c-120">Klik op Boekstuk.</span><span class="sxs-lookup"><span data-stu-id="9c88c-120">Click Voucher.</span></span>
11. <span data-ttu-id="9c88c-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9c88c-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]