---
title: Aansprakelijkheids-, activa- en onkostentransacties weergeven
description: In dit onderwerp wordt uitgelegd hoe u transacties voor een geleasd activum kunt weergeven. Deze transacties omvatten transacties met leaseverplichtingen en uitgevoerde onkostentransacties die zijn geboekt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 76c7eff17df92b01317544112099e391fd05d105
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995363"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="eeafc-104">Aansprakelijkheids-, activa- en onkostentransacties weergeven</span><span class="sxs-lookup"><span data-stu-id="eeafc-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eeafc-105">In dit onderwerp wordt uitgelegd hoe u transacties voor een geleasd activum kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="eeafc-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="eeafc-106">Deze transacties omvatten transacties met leaseverplichtingen en uitgevoerde onkostentransacties die zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="eeafc-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="eeafc-107">De boekwaarden van het aansprakelijkheidsactivum en het activum met gebruiksrecht worden in verschillende rapporten gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eeafc-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="eeafc-108">Ze worden ook gebruikt om correctiewaarden te berekenen.</span><span class="sxs-lookup"><span data-stu-id="eeafc-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="eeafc-109">Transacties voor leaseverplichtingen</span><span class="sxs-lookup"><span data-stu-id="eeafc-109">Liability transactions</span></span>

<span data-ttu-id="eeafc-110">Als u de transacties voor leaseverplichtingen wilt weergeven, selecteert u een lease op de pagina **Leaseoverzicht** en selecteert u **Boeken** om de boeken te openen die aan de leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eeafc-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="eeafc-111">Nadat een eerste toerekening, een factuur of een rentejournaal is geboekt, selecteert u **Transacties verplichtingen**.</span><span class="sxs-lookup"><span data-stu-id="eeafc-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="eeafc-112">Op de pagina **Transacties verplichtingen** worden de transacties weergegeven waarmee de leaseverplichting wordt verhoogd of verlaagd.</span><span class="sxs-lookup"><span data-stu-id="eeafc-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="eeafc-113">Negatieve bedragen op deze pagina staan voor krediettransacties in de standaardtoepassing.</span><span class="sxs-lookup"><span data-stu-id="eeafc-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="eeafc-114">Rentetoerekeningen worden als negatieve waarden weergegeven en verhogen de totale leaseverplichting.</span><span class="sxs-lookup"><span data-stu-id="eeafc-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="eeafc-115">Eventuele leasewijzigingen worden weergegeven als positieve of negatieve waarden, afhankelijk van de aard en de impact van het leaseboek.</span><span class="sxs-lookup"><span data-stu-id="eeafc-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="eeafc-116">Het huidige netto totaalsaldo van de leaseverplichting voor de geselecteerde lease wordt linksonder op de pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eeafc-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="eeafc-117">Activatransacties</span><span class="sxs-lookup"><span data-stu-id="eeafc-117">Asset transactions</span></span>

<span data-ttu-id="eeafc-118">Als u de transacties voor het leaseactivum wilt weergeven, selecteert u een lease op de pagina **Leaseoverzicht** en selecteert u **Boeken** om de leaseboeken te openen die aan de leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eeafc-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="eeafc-119">Selecteer vervolgens **Activatransacties**.</span><span class="sxs-lookup"><span data-stu-id="eeafc-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="eeafc-120">Op de pagina **Activatransacties** worden de transacties weergegeven die het leaseactivum en geaccumuleerde afschrijvingsrekeningen verhogen of verlagen.</span><span class="sxs-lookup"><span data-stu-id="eeafc-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="eeafc-121">Debetbedragen worden als positieve waarden weergegeven en kredietbedragen worden weergegeven als negatieve waarden, zoals op de pagina **Transacties verplichtingen**.</span><span class="sxs-lookup"><span data-stu-id="eeafc-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="eeafc-122">De geboekte eerste toerekening en de volgende samengevoegde afschrijving worden in de linkerbenedenhoek van de pagina weergegeven als het activasaldo.</span><span class="sxs-lookup"><span data-stu-id="eeafc-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="eeafc-123">Onkostentransacties</span><span class="sxs-lookup"><span data-stu-id="eeafc-123">Expenses transactions</span></span>

<span data-ttu-id="eeafc-124">Als u de onkostentransacties voor de lease wilt weergeven, selecteert u een lease op de pagina **Leaseoverzicht** en selecteert u **Boeken** om de leaseboeken te openen die aan de leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eeafc-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="eeafc-125">Slecteer vervolgens **Onkostentransacties**.</span><span class="sxs-lookup"><span data-stu-id="eeafc-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="eeafc-126">Op de pagina **Onkostentransacties** worden alle onkosten weergegeven die zijn geboekt tegen de lease, zoals rentelasten, afschrijvingskosten en de administratieve kosten.</span><span class="sxs-lookup"><span data-stu-id="eeafc-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>
