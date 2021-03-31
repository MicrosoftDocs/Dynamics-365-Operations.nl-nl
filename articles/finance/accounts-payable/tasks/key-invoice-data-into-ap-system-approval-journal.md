---
title: Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal
description: In dit onderwerp wordt getoond hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227179"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="e12b6-103">Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal</span><span class="sxs-lookup"><span data-stu-id="e12b6-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e12b6-104">In dit onderwerp wordt getoond hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="e12b6-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="e12b6-105">Een factuur maken en boeken</span><span class="sxs-lookup"><span data-stu-id="e12b6-105">Create and post and invoice</span></span>
1. <span data-ttu-id="e12b6-106">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Facturenregister**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="e12b6-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-107">Select **New**.</span></span>
3. <span data-ttu-id="e12b6-108">Selecteer de naam van het facturenregister dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e12b6-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="e12b6-109">Selecteer **Regels** om het register te openen en onkostenregels in te voeren.</span><span class="sxs-lookup"><span data-stu-id="e12b6-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="e12b6-110">Selecteer een leverancier.</span><span class="sxs-lookup"><span data-stu-id="e12b6-110">Select a vendor.</span></span> <span data-ttu-id="e12b6-111">Typ of selecteer bijvoorbeeld `US-104`.</span><span class="sxs-lookup"><span data-stu-id="e12b6-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="e12b6-112">Typ een waarde in het veld **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="e12b6-113">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="e12b6-114">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="e12b6-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="e12b6-115">Selecteer in het veld **Goedgekeurd door** een fiatteur in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="e12b6-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="e12b6-116">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="e12b6-117">Een factuur goedkeuren</span><span class="sxs-lookup"><span data-stu-id="e12b6-117">Approve an invoice</span></span>
1. <span data-ttu-id="e12b6-118">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Goedkeuring van facturen**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="e12b6-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-119">Select **New**.</span></span>
3. <span data-ttu-id="e12b6-120">Selecteer de naam van het factuurgoedkeuringsjournaal dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e12b6-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="e12b6-121">Selecteer **Regels** om een pagina weer te geven waarin u de facturen kunt selecteren die u wilt goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="e12b6-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="e12b6-122">Selecteer **Boekstukken zoeken** om alle facturen weer te geven die klaar staan voor goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="e12b6-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="e12b6-123">Markeer de factuur die u hebt gemaakt en klik op **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="e12b6-124">De boekstukken die u boven hebt geselecteerd worden naar deze lijst verplaatst nadat u ze selecteert.</span><span class="sxs-lookup"><span data-stu-id="e12b6-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="e12b6-125">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-125">Select **OK**.</span></span>
8. <span data-ttu-id="e12b6-126">Klik op het veld **Rekeningnummer** om een onkostenrekening aan de factuur toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e12b6-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="e12b6-127">Geef een rekeningnummer op en ga met Tab uit het veld.</span><span class="sxs-lookup"><span data-stu-id="e12b6-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="e12b6-128">Voer bijvoorbeeld `600120` in.</span><span class="sxs-lookup"><span data-stu-id="e12b6-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="e12b6-129">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="e12b6-129">Select **Post**.</span></span>
11. <span data-ttu-id="e12b6-130">Klik op **Boekstuk** om de gegevens weer te geven die zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="e12b6-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="e12b6-131">De rekening Facturen in afwachting van goedkeuring wordt tegengeboekt en vervangen door de werkelijke onkostenrekening.</span><span class="sxs-lookup"><span data-stu-id="e12b6-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]