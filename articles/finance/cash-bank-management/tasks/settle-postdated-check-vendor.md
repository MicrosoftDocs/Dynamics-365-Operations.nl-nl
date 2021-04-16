---
title: Een gepostdateerde cheque voor een leverancier vereffenen
description: Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89acad0c9421960ff4d07ed8eec798b9068424d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834566"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="3de04-103">Een gepostdateerde cheque voor een leverancier vereffenen</span><span class="sxs-lookup"><span data-stu-id="3de04-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3de04-104">Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend.</span><span class="sxs-lookup"><span data-stu-id="3de04-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="3de04-105">Voer de volgende procedures uit voordat u deze start.</span><span class="sxs-lookup"><span data-stu-id="3de04-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="3de04-106">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="3de04-106">Set up postdated checks</span></span>

2) <span data-ttu-id="3de04-107">Een gepostdateerde cheque voor een leverancier registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="3de04-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="3de04-108">De rol van deze procedure is penningmeester.</span><span class="sxs-lookup"><span data-stu-id="3de04-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="3de04-109">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3de04-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="3de04-110">Ga naar Leveranciers > Betalingen > Gepostdateerde cheques van leverancier.</span><span class="sxs-lookup"><span data-stu-id="3de04-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="3de04-111">Klik op Vereffenen.</span><span class="sxs-lookup"><span data-stu-id="3de04-111">Click Settle.</span></span>
3. <span data-ttu-id="3de04-112">Klik op Aflossingstransacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="3de04-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="3de04-113">Vereffen de leveranciersrekening voor de chequetransactie.</span><span class="sxs-lookup"><span data-stu-id="3de04-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="3de04-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3de04-114">Close the page.</span></span>
5. <span data-ttu-id="3de04-115">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="3de04-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="3de04-116">Selecteer 'Alle' in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="3de04-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="3de04-117">Schakel het selectievakje Alleen door de gebruiker gemaakte journalen weergeven in of uit.</span><span class="sxs-lookup"><span data-stu-id="3de04-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="3de04-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="3de04-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3de04-119">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="3de04-119">Click Lines.</span></span>
10. <span data-ttu-id="3de04-120">Klik op Boekstuk.</span><span class="sxs-lookup"><span data-stu-id="3de04-120">Click Voucher.</span></span>
11. <span data-ttu-id="3de04-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="3de04-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]