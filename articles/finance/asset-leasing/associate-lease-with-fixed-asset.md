---
title: Vaste activa koppelen met leases
description: In dit onderwerp wordt uitgelegd hoe u een bestaand vast activum aan een nieuwe lease koppelt.
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
ms.openlocfilehash: 274fcc73b48282a8025a210dd488105500609d5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971423"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="9d596-103">Vaste activa koppelen met leases</span><span class="sxs-lookup"><span data-stu-id="9d596-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d596-104">In dit onderwerp wordt uitgelegd hoe u een bestaand vast activum aan een nieuwe lease koppelt.</span><span class="sxs-lookup"><span data-stu-id="9d596-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="9d596-105">Wanneer u een vast activum koppelt aan een lease, wordt de waarde van het activum met gebruiksrecht (RoU) bij de eerste toerekening gebruikt als de verwervingskosten van het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="9d596-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="9d596-106">Voordat u een vast activum aan een lease kunt koppelen, moet u een record voor het vaste activum maken in Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9d596-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="9d596-107">Vervolgens maakt u op de pagina **Leaseoverzicht** een lease en koppelt u het activum aan die lease.</span><span class="sxs-lookup"><span data-stu-id="9d596-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="9d596-108">Voeg een lease toe door de stappen te volgen in [Leases toevoegen of kopiëren](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="9d596-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="9d596-109">Selecteer op de pagina **Lease toevoegen** in het veld **Vaste-activanummer** het activum dat nog niet is aangeschaft.</span><span class="sxs-lookup"><span data-stu-id="9d596-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="9d596-110">Selecteer **Boeken** en bevestig het betalingsschema.</span><span class="sxs-lookup"><span data-stu-id="9d596-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="9d596-111">Selecteer **Initiële toerekening**.</span><span class="sxs-lookup"><span data-stu-id="9d596-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="9d596-112">Selecteer **Activaleasejournaal**.</span><span class="sxs-lookup"><span data-stu-id="9d596-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="9d596-113">Met de journaalpost voor eerste toerekening van de lease wordt het vaste activum gedebiteerd voor het bedrag dat meestal wordt gedebiteerd van de rekening voor het RoU-activum.</span><span class="sxs-lookup"><span data-stu-id="9d596-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="9d596-114">U kunt nu het transactietype en boek voor het vaste activum weergeven.</span><span class="sxs-lookup"><span data-stu-id="9d596-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="9d596-115">Selecteer **Journaaldetails**.</span><span class="sxs-lookup"><span data-stu-id="9d596-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="9d596-116">Selecteer **Regels** om de afzonderlijke regels voor de journaalboeking weer te geven.</span><span class="sxs-lookup"><span data-stu-id="9d596-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="9d596-117">Selecteer de journaalregel die de activa bevat en selecteer vervolgens het tabblad **Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="9d596-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="9d596-118">Op het tabblad **Vaste activa** ziet u het transactietype en het boek.</span><span class="sxs-lookup"><span data-stu-id="9d596-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="9d596-119">Standaard wordt het veld **Transactietype** ingesteld op **Verwerving** en het veld **Boek** op het huidige boek voor het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="9d596-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="9d596-120">Nadat u de journaalboeking voor de eerste toerekening hebt uitgevoerd, wordt de transactie weergegeven als een verwervingstransactie voor het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="9d596-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="9d596-121">Als u de transactietabel wilt weergeven, gaat u naar **Vaste activa \> Vaste activa \> Vaste activa**, selecteert u het betreffende activum en vervolgens **Waarderingen**.</span><span class="sxs-lookup"><span data-stu-id="9d596-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="9d596-122">U kunt zien dat met de journaalboeking voor de eerste toerekening een verwervingstransactie is gemaakt voor het opgegeven vaste activum.</span><span class="sxs-lookup"><span data-stu-id="9d596-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="9d596-123">De vaste activa kunnen nu worden afgeschreven met de standaard afschrijvingsfunctionaliteit in Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9d596-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="9d596-124">Zie voor meer informatie [Afschrijvingsmethoden en conventies](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="9d596-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9d596-125">Als u een vast activum aan een lease koppelt, worden de knoppen **Afschrijving van activa** en **Leasewaardevermindering** uitgeschakeld in Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="9d596-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="9d596-126">U kunt transacties voor afschrijvingen van activa en waardevermindering voor leases weergeven in Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9d596-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="9d596-127">De knop **Activatransacties**, waarmee een queryformulier wordt geopend, wordt ook uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="9d596-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="9d596-128">U kunt het queryformulier **Activatransacties** ook openen in Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9d596-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  
