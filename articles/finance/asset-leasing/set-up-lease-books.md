---
title: Leaseboeken instellen
description: In dit onderwerp wordt de informatie beschreven die in leaseboeken wordt bijgehouden. Leaseboeken bevatten de boekhoudbeleidsregels die bepalen hoe een lease wordt verwerkt in het systeem.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442161"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="3bea1-104">Leaseboeken instellen</span><span class="sxs-lookup"><span data-stu-id="3bea1-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bea1-105">Leaseboeken bevatten de boekhoudbeleidsregels die bepalen hoe een lease wordt verwerkt in het systeem.</span><span class="sxs-lookup"><span data-stu-id="3bea1-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="3bea1-106">Behalve boekhouden op basis van contante betaling, ondersteunt Activa leasen de volgende standaarden:</span><span class="sxs-lookup"><span data-stu-id="3bea1-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="3bea1-107">Algemeen geaccepteerde boekhoudprincipes in de Verenigde Staten (VS GAAP)</span><span class="sxs-lookup"><span data-stu-id="3bea1-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="3bea1-108">Accounting Standards Codification Topic 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="3bea1-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="3bea1-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="3bea1-109">ASC 840</span></span>
- <span data-ttu-id="3bea1-110">International Financial Reporting Standard 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="3bea1-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="3bea1-111">International Accounting Standard 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="3bea1-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="3bea1-112">Volg deze stappen om een nieuw leaseboek te maken.</span><span class="sxs-lookup"><span data-stu-id="3bea1-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="3bea1-113">Ga naar **Activa leasen \> Instellen \> Leaseboeken**.</span><span class="sxs-lookup"><span data-stu-id="3bea1-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="3bea1-114">Selecteer **Nieuw** om een boek toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3bea1-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="3bea1-115">Stel de volgende velden in.</span><span class="sxs-lookup"><span data-stu-id="3bea1-115">Set the following fields.</span></span>

    | <span data-ttu-id="3bea1-116">Naam</span><span class="sxs-lookup"><span data-stu-id="3bea1-116">Name</span></span>                                     | <span data-ttu-id="3bea1-117">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3bea1-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="3bea1-118">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="3bea1-118">Posting layer</span></span>                            | <span data-ttu-id="3bea1-119">Selecteer de boekingslaag die moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3bea1-119">Select the posting layer to use.</span></span> <span data-ttu-id="3bea1-120">Elk boek dat aan een lease is gekoppeld, wordt ingesteld voor een bepaalde boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="3bea1-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="3bea1-121">Elke boekingslaag heeft verschillende boekingsdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="3bea1-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="3bea1-122">Leasetype</span><span class="sxs-lookup"><span data-stu-id="3bea1-122">Lease type</span></span>                               | <span data-ttu-id="3bea1-123">Selecteer of de lease automatisch moet worden geclassificeerd of dat deze vooraf moet worden gedefinieerd als een financiële of operationele lease.</span><span class="sxs-lookup"><span data-stu-id="3bea1-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="3bea1-124">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="3bea1-124">Accounting framework</span></span>                     | <span data-ttu-id="3bea1-125">Selecteer het kader dat is gekoppeld aan het boek.</span><span class="sxs-lookup"><span data-stu-id="3bea1-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="3bea1-126">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="3bea1-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="3bea1-127">De lease wordt door het systeem geclassificeerd als een financiële lease als het leasetype is ingesteld op **Automatisch** en als de leasetermijn voor de economische levensduur van het activum groter is dan of gelijk is aan het percentage dat is ingevoerd in dit veld.</span><span class="sxs-lookup"><span data-stu-id="3bea1-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="3bea1-128">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="3bea1-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="3bea1-129">Voer een geheel getal in om de drempel te definiëren waarmee het leasetype wordt bepaald.</span><span class="sxs-lookup"><span data-stu-id="3bea1-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="3bea1-130">Als de huidige waarde van de toekomstige minimale leasebetalingen meer is dan de door de gebruiker gedefinieerde waarde in de boekinstelling, en als de leaseclassificatie van het boek is ingesteld op automatisch, wordt de lease door het systeem geclassificeerd als een financiële lease.</span><span class="sxs-lookup"><span data-stu-id="3bea1-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="3bea1-131">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="3bea1-131">Short-term threshold</span></span>                     | <span data-ttu-id="3bea1-132">Voer het aantal maanden in dat moet worden gebruikt als drempel voor leases op korte termijn.</span><span class="sxs-lookup"><span data-stu-id="3bea1-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="3bea1-133">Als de leaseperiode kleiner is dan of gelijk is aan het aantal maanden dat u hier invoert, wordt de lease door het systeem geclassificeerd als een lease op korte termijn en wordt de behandeling uitgestelde gebruiksvergoeding toegepast.</span><span class="sxs-lookup"><span data-stu-id="3bea1-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="3bea1-134">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="3bea1-134">Low value threshold</span></span>                      | <span data-ttu-id="3bea1-135">Voer een bedrag in dat u wilt gebruiken als drempelwaarde voor leases met geringe waarde.</span><span class="sxs-lookup"><span data-stu-id="3bea1-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="3bea1-136">Als de reële waarde van het activum kleiner is dan of gelijk is aan de waarde die u hier invoert, wordt de lease door het systeem geclassificeerd als een lease met geringe waarde en wordt de behandeling uitgestelde gebruiksvergoeding toegepast.</span><span class="sxs-lookup"><span data-stu-id="3bea1-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="3bea1-137">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="3bea1-137">Pay to vendor</span></span>                            | <span data-ttu-id="3bea1-138">Stel deze optie in op **Ja** als u wilt toestaan dat leasebetalingen als een factuur worden geboekt naar de leveranciersrekening die op elke lease is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="3bea1-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="3bea1-139">Wanneer een leasebetaling wordt geboekt, wordt de leveranciersrekening gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="3bea1-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="3bea1-140">Als deze optie is ingesteld op **Nee**, wordt de rekening die is opgegeven voor het boekingstype **Leasebetaling** op de pagina **Leaseboekingsparameters** in plaats daarvan gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="3bea1-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
