---
title: Toerekeningsschema's maken
description: In dit onderwerp wordt uitgelegd hoe u een toerekeningsschema maakt.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f8cf8546187ae1c65d4966887e1c5842dff431
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867554"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="88ad0-103">Toerekeningsschema's maken</span><span class="sxs-lookup"><span data-stu-id="88ad0-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88ad0-104">In dit onderwerp wordt uitgelegd hoe u een toerekeningsschema maakt.</span><span class="sxs-lookup"><span data-stu-id="88ad0-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="88ad0-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="88ad0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="88ad0-106">Ga naar **Navigatievenster > Modules > Grootboek > Journaalinstellingen > Toerekeningsschema's**.</span><span class="sxs-lookup"><span data-stu-id="88ad0-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="88ad0-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="88ad0-107">Select **New**.</span></span>
3. <span data-ttu-id="88ad0-108">Typ een waarde in het veld **Toerekeningsidentificatie**.</span><span class="sxs-lookup"><span data-stu-id="88ad0-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="88ad0-109">Typ een waarde in het veld **Omschrijving van toenameschema**.</span><span class="sxs-lookup"><span data-stu-id="88ad0-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="88ad0-110">Geef in het veld **Debet** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="88ad0-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="88ad0-111">De opgegeven hoofdrekening zal de hoofddebetrekening op de journaalboekstukregel vervangen en zal ook worden gebruikt voor de omkering van de uitstelling op basis van de transitorische grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="88ad0-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="88ad0-112">Geef in het veld **Credit** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="88ad0-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="88ad0-113">De opgegeven hoofdrekening zal de hoofdcreditrekening op de journaalboekstukregel vervangen en zal ook worden gebruikt voor de omkering van de uitstelling op basis van de transitorische grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="88ad0-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="88ad0-114">Selecteer in het veld **Boekstuk** hoe u wilt dat het boekstuk wordt bepaald wanneer de transacties worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="88ad0-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="88ad0-115">Typ in het veld **Beschrijving** een waarde om de transacties die zullen worden geboekt te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="88ad0-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="88ad0-116">Selecteer in het veld **Periodefrequentie** hoe vaak de transacties moeten voorkomen.</span><span class="sxs-lookup"><span data-stu-id="88ad0-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="88ad0-117">Voer in het veld **Aantal voorvallen per periode** een getal in.</span><span class="sxs-lookup"><span data-stu-id="88ad0-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="88ad0-118">Selecteer in het veld **Transacties boeken** wanneer de transacties moeten worden geboekt, zoals **Maandelijks**.</span><span class="sxs-lookup"><span data-stu-id="88ad0-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

