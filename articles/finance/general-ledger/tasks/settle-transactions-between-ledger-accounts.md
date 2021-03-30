---
title: Transacties tussen grootboekrekeningen vereffenen
description: Deze procedure toont hoe u transacties tussen grootboekrekeningen vereffent en een grootboekvereffening annuleert.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6813871a4773d39d4abfdecc896a2aa8b320cbe0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222090"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="2ae99-103">Transacties tussen grootboekrekeningen vereffenen</span><span class="sxs-lookup"><span data-stu-id="2ae99-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ae99-104">Deze procedure toont hoe u transacties tussen grootboekrekeningen vereffent en een grootboekvereffening annuleert.</span><span class="sxs-lookup"><span data-stu-id="2ae99-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="2ae99-105">Deze procedure gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="2ae99-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="2ae99-106">Transactie tussen grootboekrekeningen vereffenen</span><span class="sxs-lookup"><span data-stu-id="2ae99-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="2ae99-107">Ga naar Grootboek > Periodieke taken > Grootboekvereffeningen.</span><span class="sxs-lookup"><span data-stu-id="2ae99-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="2ae99-108">Zoek in de lijst de transactie die u wilt vereffenen.</span><span class="sxs-lookup"><span data-stu-id="2ae99-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="2ae99-109">Het saldobedrag moet nul zijn.</span><span class="sxs-lookup"><span data-stu-id="2ae99-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="2ae99-110">Klik op Opnemen.</span><span class="sxs-lookup"><span data-stu-id="2ae99-110">Click Include.</span></span>
4. <span data-ttu-id="2ae99-111">Klik op Accepteren.</span><span class="sxs-lookup"><span data-stu-id="2ae99-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="2ae99-112">Een grootboekvereffening annuleren</span><span class="sxs-lookup"><span data-stu-id="2ae99-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="2ae99-113">Ga naar Grootboek > Query´s en rapporten > Proefbalans.</span><span class="sxs-lookup"><span data-stu-id="2ae99-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="2ae99-114">Klik op Parameters om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="2ae99-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="2ae99-115">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="2ae99-115">Click Update.</span></span>
4. <span data-ttu-id="2ae99-116">Zoek in de lijst de rekening met de vereffende transactie.</span><span class="sxs-lookup"><span data-stu-id="2ae99-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="2ae99-117">Klik op Alle transacties.</span><span class="sxs-lookup"><span data-stu-id="2ae99-117">Click All transactions.</span></span>
6. <span data-ttu-id="2ae99-118">Gebruik een filter om de transactie gemakkelijk terug te vinden in de lijst.</span><span class="sxs-lookup"><span data-stu-id="2ae99-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="2ae99-119">Klik op Grootboekvereffeningen.</span><span class="sxs-lookup"><span data-stu-id="2ae99-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="2ae99-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2ae99-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]