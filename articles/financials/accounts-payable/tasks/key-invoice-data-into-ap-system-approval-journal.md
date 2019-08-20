---
title: Belangrijke factuurgegevens in leverancierssysteem met goedkeuringsjournaal
description: Deze taakbegeleiding toont hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837031"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="625bc-103">Belangrijke factuurgegevens in leverancierssysteem met goedkeuringsjournaal</span><span class="sxs-lookup"><span data-stu-id="625bc-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="625bc-104">Deze taakbegeleiding toont hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="625bc-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="625bc-105">Een factuur maken en boeken</span><span class="sxs-lookup"><span data-stu-id="625bc-105">Create and post and invoice</span></span>
1. <span data-ttu-id="625bc-106">Ga naar Leveranciers > Facturen > Facturenregister.</span><span class="sxs-lookup"><span data-stu-id="625bc-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="625bc-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="625bc-107">Click New.</span></span>
3. <span data-ttu-id="625bc-108">Selecteer de naam van het facturenregister dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="625bc-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="625bc-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="625bc-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="625bc-110">Klik op Regels om het register te openen en onkostenregels in te voeren.</span><span class="sxs-lookup"><span data-stu-id="625bc-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="625bc-111">Selecteer een leverancier.</span><span class="sxs-lookup"><span data-stu-id="625bc-111">Select a vendor.</span></span> <span data-ttu-id="625bc-112">Typ of selecteer bijvoorbeeld US-104</span><span class="sxs-lookup"><span data-stu-id="625bc-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="625bc-113">Typ een waarde in het veld Factuur.</span><span class="sxs-lookup"><span data-stu-id="625bc-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="625bc-114">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="625bc-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="625bc-115">Voer een nummer in het veld Credit in.</span><span class="sxs-lookup"><span data-stu-id="625bc-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="625bc-116">Klik in het veld Goedgekeurd door op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="625bc-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="625bc-117">Markeer een fiatteur en klik op Selecteren om die fiatteur te selecteren.</span><span class="sxs-lookup"><span data-stu-id="625bc-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="625bc-118">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="625bc-118">Click Post.</span></span>
13. <span data-ttu-id="625bc-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="625bc-119">Close the page.</span></span>
14. <span data-ttu-id="625bc-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="625bc-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="625bc-121">Een factuur goedkeuren</span><span class="sxs-lookup"><span data-stu-id="625bc-121">Approve an invoice</span></span>
1. <span data-ttu-id="625bc-122">Ga naar Leveranciers > Facturen > Factuurgoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="625bc-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="625bc-123">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="625bc-123">Click New.</span></span>
3. <span data-ttu-id="625bc-124">Selecteer de naam van het factuurgoedkeuringsjournaal dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="625bc-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="625bc-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="625bc-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="625bc-126">Klik op regels om een pagina weer te geven waarin u de facturen kunt selecteren die u wilt goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="625bc-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="625bc-127">Selecteer Boekstukken zoeken om alle facturen weer te geven die klaar staan voor goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="625bc-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="625bc-128">Markeer de factuur die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="625bc-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="625bc-129">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="625bc-129">Click Select.</span></span>
    * <span data-ttu-id="625bc-130">De boekstukken die u boven hebt geselecteerd worden naar deze lijst verplaatst nadat u ze selecteert.</span><span class="sxs-lookup"><span data-stu-id="625bc-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="625bc-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="625bc-131">Click OK.</span></span>
10. <span data-ttu-id="625bc-132">Klik op het rekeningnummerveld om een onkostenrekening aan de factuur toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="625bc-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="625bc-133">Geef een rekeningnummer op en ga met Tab uit het veld.</span><span class="sxs-lookup"><span data-stu-id="625bc-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="625bc-134">Voer bijvoorbeeld 600120 in.</span><span class="sxs-lookup"><span data-stu-id="625bc-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="625bc-135">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="625bc-135">Click Post.</span></span>
13. <span data-ttu-id="625bc-136">Klik op Boekstuk om de gegevens weer te geven die zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="625bc-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="625bc-137">De rekening Facturen in afwachting van goedkeuring wordt tegengeboekt en vervangen door de werkelijke onkostenrekening.</span><span class="sxs-lookup"><span data-stu-id="625bc-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

