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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144230"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="90a26-103">Een gepostdateerde cheque voor een leverancier vereffenen</span><span class="sxs-lookup"><span data-stu-id="90a26-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90a26-104">Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend.</span><span class="sxs-lookup"><span data-stu-id="90a26-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="90a26-105">Voer de volgende procedures uit voordat u deze start.</span><span class="sxs-lookup"><span data-stu-id="90a26-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="90a26-106">Gepostdateerde cheques instellen</span><span class="sxs-lookup"><span data-stu-id="90a26-106">Set up postdated checks</span></span>

2) <span data-ttu-id="90a26-107">Een gepostdateerde cheque voor een leverancier registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="90a26-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="90a26-108">De rol van deze procedure is penningmeester.</span><span class="sxs-lookup"><span data-stu-id="90a26-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="90a26-109">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="90a26-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="90a26-110">Ga naar Leveranciers > Betalingen > Gepostdateerde cheques van leverancier.</span><span class="sxs-lookup"><span data-stu-id="90a26-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="90a26-111">Klik op Vereffenen.</span><span class="sxs-lookup"><span data-stu-id="90a26-111">Click Settle.</span></span>
3. <span data-ttu-id="90a26-112">Klik op Aflossingstransacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="90a26-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="90a26-113">Vereffen de leveranciersrekening voor de chequetransactie.</span><span class="sxs-lookup"><span data-stu-id="90a26-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="90a26-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="90a26-114">Close the page.</span></span>
5. <span data-ttu-id="90a26-115">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="90a26-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="90a26-116">Selecteer 'Alle' in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="90a26-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="90a26-117">Schakel het selectievakje Alleen door de gebruiker gemaakte journalen weergeven in of uit.</span><span class="sxs-lookup"><span data-stu-id="90a26-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="90a26-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="90a26-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="90a26-119">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="90a26-119">Click Lines.</span></span>
10. <span data-ttu-id="90a26-120">Klik op Boekstuk.</span><span class="sxs-lookup"><span data-stu-id="90a26-120">Click Voucher.</span></span>
11. <span data-ttu-id="90a26-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="90a26-121">Close the page.</span></span>

