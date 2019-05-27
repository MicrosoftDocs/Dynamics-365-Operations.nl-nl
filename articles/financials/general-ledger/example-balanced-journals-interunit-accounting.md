---
title: Evenwichtige journalen voor interunit-boekhouding
description: Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b596a2332a9ada01df7b4e718a79eb624ee52fc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549099"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="41cda-103">Evenwichtige journalen voor interunit-boekhouding</span><span class="sxs-lookup"><span data-stu-id="41cda-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41cda-104">Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina.</span><span class="sxs-lookup"><span data-stu-id="41cda-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="41cda-105">Als boekingen niet in evenwicht zijn op het niveau van de financiële dimensiewaarden, worden automatisch extra boekingen gemaakt om het journaal automatisch in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="41cda-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="41cda-106">Deze boekingen gebruiken de boekingstypen **Inter-unit - debet** en **Inter-unit - credit** op de pagina **Rekeningen voor automatische transacties** om de hoofdrekening te bepalen.</span><span class="sxs-lookup"><span data-stu-id="41cda-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="41cda-107">Bijvoorbeeld, Bedrijfseenheid, het tweede segment van de grootboekrekening, wordt geselecteerd als de financiële tegendimensie en de volgende boekingsregels staan op het punt om te worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="41cda-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="41cda-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="41cda-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="41cda-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="41cda-109">100.00 DR</span></span> |
| <span data-ttu-id="41cda-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="41cda-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="41cda-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="41cda-111">100.00 DR</span></span> |
| <span data-ttu-id="41cda-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="41cda-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="41cda-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="41cda-113">200.00 CR</span></span> |

<span data-ttu-id="41cda-114">In dit geval worden de volgende saldi gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="41cda-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="41cda-115">Voor Bedrijfseenheid MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="41cda-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="41cda-116">Voor Bedrijfseenheid MSP = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="41cda-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="41cda-117">Daarom worden de volgende posten automatisch gemaakt om het journaal op het niveau van de financiële dimensiewaarden in evenwicht te brengen.</span><span class="sxs-lookup"><span data-stu-id="41cda-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="41cda-118">(Inter-unit debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="41cda-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="41cda-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="41cda-119">100.00 DR</span></span> |
| <span data-ttu-id="41cda-120">(Inter-unit credit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="41cda-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="41cda-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="41cda-121">100.00 CR</span></span> |





