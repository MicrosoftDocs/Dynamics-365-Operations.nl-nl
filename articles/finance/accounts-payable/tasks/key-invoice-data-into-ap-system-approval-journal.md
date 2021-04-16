---
title: Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal
description: In dit onderwerp wordt getoond hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.
author: abruer
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d01c04fcf707109cd7bc6f056846506914e96dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838880"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="981ba-103">Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal</span><span class="sxs-lookup"><span data-stu-id="981ba-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="981ba-104">In dit onderwerp wordt getoond hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="981ba-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="981ba-105">Een factuur maken en boeken</span><span class="sxs-lookup"><span data-stu-id="981ba-105">Create and post and invoice</span></span>
1. <span data-ttu-id="981ba-106">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Facturenregister**.</span><span class="sxs-lookup"><span data-stu-id="981ba-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="981ba-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="981ba-107">Select **New**.</span></span>
3. <span data-ttu-id="981ba-108">Selecteer de naam van het facturenregister dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="981ba-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="981ba-109">Selecteer **Regels** om het register te openen en onkostenregels in te voeren.</span><span class="sxs-lookup"><span data-stu-id="981ba-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="981ba-110">Selecteer een leverancier.</span><span class="sxs-lookup"><span data-stu-id="981ba-110">Select a vendor.</span></span> <span data-ttu-id="981ba-111">Typ of selecteer bijvoorbeeld `US-104`.</span><span class="sxs-lookup"><span data-stu-id="981ba-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="981ba-112">Typ een waarde in het veld **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="981ba-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="981ba-113">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="981ba-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="981ba-114">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="981ba-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="981ba-115">Selecteer in het veld **Goedgekeurd door** een fiatteur in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="981ba-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="981ba-116">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="981ba-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="981ba-117">Een factuur goedkeuren</span><span class="sxs-lookup"><span data-stu-id="981ba-117">Approve an invoice</span></span>
1. <span data-ttu-id="981ba-118">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Goedkeuring van facturen**.</span><span class="sxs-lookup"><span data-stu-id="981ba-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="981ba-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="981ba-119">Select **New**.</span></span>
3. <span data-ttu-id="981ba-120">Selecteer de naam van het factuurgoedkeuringsjournaal dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="981ba-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="981ba-121">Selecteer **Regels** om een pagina weer te geven waarin u de facturen kunt selecteren die u wilt goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="981ba-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="981ba-122">Selecteer **Boekstukken zoeken** om alle facturen weer te geven die klaar staan voor goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="981ba-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="981ba-123">Markeer de factuur die u hebt gemaakt en klik op **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="981ba-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="981ba-124">De boekstukken die u boven hebt geselecteerd worden naar deze lijst verplaatst nadat u ze selecteert.</span><span class="sxs-lookup"><span data-stu-id="981ba-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="981ba-125">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="981ba-125">Select **OK**.</span></span>
8. <span data-ttu-id="981ba-126">Klik op het veld **Rekeningnummer** om een onkostenrekening aan de factuur toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="981ba-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="981ba-127">Geef een rekeningnummer op en ga met Tab uit het veld.</span><span class="sxs-lookup"><span data-stu-id="981ba-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="981ba-128">Voer bijvoorbeeld `600120` in.</span><span class="sxs-lookup"><span data-stu-id="981ba-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="981ba-129">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="981ba-129">Select **Post**.</span></span>
11. <span data-ttu-id="981ba-130">Klik op **Boekstuk** om de gegevens weer te geven die zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="981ba-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="981ba-131">De rekening Facturen in afwachting van goedkeuring wordt tegengeboekt en vervangen door de werkelijke onkostenrekening.</span><span class="sxs-lookup"><span data-stu-id="981ba-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]