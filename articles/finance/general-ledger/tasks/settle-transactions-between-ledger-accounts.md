---
title: Transacties tussen grootboekrekeningen vereffenen
description: Deze procedure toont hoe u transacties tussen grootboekrekeningen vereffent en een grootboekvereffening annuleert.
author: aprilolson
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2594b90ed58a1e7f12c8a94d3c48266faef557f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817048"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="dbcc8-103">Transacties tussen grootboekrekeningen vereffenen</span><span class="sxs-lookup"><span data-stu-id="dbcc8-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbcc8-104">Deze procedure toont hoe u transacties tussen grootboekrekeningen vereffent en een grootboekvereffening annuleert.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="dbcc8-105">Deze procedure gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="dbcc8-106">Transactie tussen grootboekrekeningen vereffenen</span><span class="sxs-lookup"><span data-stu-id="dbcc8-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="dbcc8-107">Ga naar Grootboek > Periodieke taken > Grootboekvereffeningen.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="dbcc8-108">Zoek in de lijst de transactie die u wilt vereffenen.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="dbcc8-109">Het saldobedrag moet nul zijn.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="dbcc8-110">Klik op Opnemen.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-110">Click Include.</span></span>
4. <span data-ttu-id="dbcc8-111">Klik op Accepteren.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="dbcc8-112">Een grootboekvereffening annuleren</span><span class="sxs-lookup"><span data-stu-id="dbcc8-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="dbcc8-113">Ga naar Grootboek > Query´s en rapporten > Proefbalans.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="dbcc8-114">Klik op Parameters om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="dbcc8-115">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-115">Click Update.</span></span>
4. <span data-ttu-id="dbcc8-116">Zoek in de lijst de rekening met de vereffende transactie.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="dbcc8-117">Klik op Alle transacties.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-117">Click All transactions.</span></span>
6. <span data-ttu-id="dbcc8-118">Gebruik een filter om de transactie gemakkelijk terug te vinden in de lijst.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="dbcc8-119">Klik op Grootboekvereffeningen.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="dbcc8-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="dbcc8-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]