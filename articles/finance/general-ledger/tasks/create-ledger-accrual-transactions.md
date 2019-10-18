---
title: Toenametransacties voor grootboek maken
description: Deze taakbegeleiding helpt u bij het genereren van transitorische posten voor het grootboek die zijn gebaseerd op toerekeningsschema's.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186182"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="b2f88-103">Toenametransacties voor grootboek maken</span><span class="sxs-lookup"><span data-stu-id="b2f88-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2f88-104">Deze taakbegeleiding helpt u bij het genereren van transitorische posten voor het grootboek die zijn gebaseerd op toerekeningsschema's</span><span class="sxs-lookup"><span data-stu-id="b2f88-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="b2f88-105">Ga naar Grootboek > Journaalboekingen > Algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="b2f88-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="b2f88-106">Zoek en selecteer het gewenste journaal in de lijst of maak een nieuw.</span><span class="sxs-lookup"><span data-stu-id="b2f88-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="b2f88-107">Klik om de koppeling in het veld Journaalbatchnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="b2f88-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="b2f88-108">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b2f88-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b2f88-109">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="b2f88-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="b2f88-110">In dit voorbeeld definiëren we de uitgaven voor de verzekering.</span><span class="sxs-lookup"><span data-stu-id="b2f88-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="b2f88-111">Deze worden een periodiek onkostenbedrag.</span><span class="sxs-lookup"><span data-stu-id="b2f88-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="b2f88-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="b2f88-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="b2f88-113">Voer een nummer in het veld Debet in.</span><span class="sxs-lookup"><span data-stu-id="b2f88-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="b2f88-114">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="b2f88-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="b2f88-115">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="b2f88-115">Click Functions.</span></span>
10. <span data-ttu-id="b2f88-116">Klik op Transitorische grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="b2f88-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="b2f88-117">Klik in het veld Toerekeningsidentificatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b2f88-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b2f88-118">Zoek en selecteer in de lijst het toerekeningsschema dat u wilt toepassen.</span><span class="sxs-lookup"><span data-stu-id="b2f88-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="b2f88-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b2f88-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b2f88-120">Voer een datum in het veld Startdatum in.</span><span class="sxs-lookup"><span data-stu-id="b2f88-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="b2f88-121">Klik op Transacties.</span><span class="sxs-lookup"><span data-stu-id="b2f88-121">Click Transactions.</span></span>
16. <span data-ttu-id="b2f88-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b2f88-122">Close the page.</span></span>
17. <span data-ttu-id="b2f88-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b2f88-123">Click OK.</span></span>
18. <span data-ttu-id="b2f88-124">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="b2f88-124">Click Post.</span></span>

