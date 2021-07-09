---
title: Werkstromen voor kortingsbeheerdeals
description: In dit onderwerp wordt uitgelegd hoe u een werkstroom voor kortingsbeheer kunt instellen om deals goed te keuren en te activeren.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270952"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="c346b-103">Werkstromen voor kortingsbeheerdeals</span><span class="sxs-lookup"><span data-stu-id="c346b-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c346b-104">Voor het goedkeuren van kortingsaanbiedingen wordt in Kortingsbeheer hetzelfde werkstroomplatform gebruikt als in andere Finance and Operations-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="c346b-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="c346b-105">Aan elke werkstroom zijn twee taakprocessen gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="c346b-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="c346b-106">Eén element van de werkstroom keurt de deal goed.</span><span class="sxs-lookup"><span data-stu-id="c346b-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="c346b-107">Eén element van de werkstroom activeert de deal zodat de gebruiker of het werkstroomproces de transacties kan goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="c346b-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="c346b-108">Voordat u een kortingsdeal kunt gebruiken, moet deze actief zijn in de module **Kortingsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="c346b-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="c346b-109">Als u een deal wilt activeren, moet u eerst een werkstroom maken en configureren voor *Werkstroom voor kortingsbeheerdeals*.</span><span class="sxs-lookup"><span data-stu-id="c346b-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="c346b-110">Gebruikers kunnen transacties niet handmatig goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="c346b-110">Users can't manually approve deals.</span></span> <span data-ttu-id="c346b-111">De werkstroom moet altijd worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c346b-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="c346b-112">Werkstromen voor kortingsbeheerdeals maken en beheren</span><span class="sxs-lookup"><span data-stu-id="c346b-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="c346b-113">Als u wilt werken met uw werkstromen voor kortingsbeheerdeals, gaat u naar **Kortingsbeheer \> Instellen \> Werkstromen voor kortingsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="c346b-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="c346b-114">Hier kunt u werkstromen weergeven, maken en bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c346b-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="c346b-115">Er kan slechts één werkstroom van dit type tegelijk actief zijn.</span><span class="sxs-lookup"><span data-stu-id="c346b-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="c346b-116">Zie [Overzicht van werkstroomsysteem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) en de gerelateerde onderwerpen voor meer informatie over werkstromen, hoe u werkt met de pagina **Werkstromen voor kortingsbeheer** en hoe u werkstromen maakt.</span><span class="sxs-lookup"><span data-stu-id="c346b-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="c346b-117">Een werkstroom gebruiken om een deal te activeren</span><span class="sxs-lookup"><span data-stu-id="c346b-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="c346b-118">Als u een deal wilt activeren via een werkstroom, opent u de deal (bijvoorbeeld op de pagina **Alle kortingsbeheerdeals**).</span><span class="sxs-lookup"><span data-stu-id="c346b-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="c346b-119">Selecteer vervolgens **Werkstroom \> Indienen** in het actievenster</span><span class="sxs-lookup"><span data-stu-id="c346b-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="c346b-120">Nadat de nieuwe deal is verwerkt en goedgekeurd via de werkstroom, is deze actief en klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="c346b-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="c346b-121">Nadat een deal is geactiveerd, kunt u de meeste instellingen ervan niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c346b-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="c346b-122">Als u een actieve deal moet wijzigen, deactiveert u deze eerst en maakt u vervolgens een nieuwe deal.</span><span class="sxs-lookup"><span data-stu-id="c346b-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="c346b-123">Als de nieuwe deal op de oude overeenkomst lijkt, kunt u deze maken door de oude deal te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="c346b-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="c346b-124">U kunt de volgende instellingen voor een deal wijzigen nadat deze is geactiveerd:</span><span class="sxs-lookup"><span data-stu-id="c346b-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="c346b-125">Afstemmen met</span><span class="sxs-lookup"><span data-stu-id="c346b-125">Reconcile by</span></span>
- <span data-ttu-id="c346b-126">Cumulatieve garantie</span><span class="sxs-lookup"><span data-stu-id="c346b-126">Cumulative guarantee</span></span>
- <span data-ttu-id="c346b-127">Boekingsprofiel</span><span class="sxs-lookup"><span data-stu-id="c346b-127">Posting profile</span></span>
- <span data-ttu-id="c346b-128">Boekingsprofiel voor garantie</span><span class="sxs-lookup"><span data-stu-id="c346b-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="c346b-129">Documentnotities</span><span class="sxs-lookup"><span data-stu-id="c346b-129">Document notes</span></span>
- <span data-ttu-id="c346b-130">Valuta</span><span class="sxs-lookup"><span data-stu-id="c346b-130">Currency</span></span>
- <span data-ttu-id="c346b-131">Begindatum</span><span class="sxs-lookup"><span data-stu-id="c346b-131">From date</span></span>
- <span data-ttu-id="c346b-132">Einddatum</span><span class="sxs-lookup"><span data-stu-id="c346b-132">To date</span></span>

<span data-ttu-id="c346b-133">Bovendien kunnen kortingregels worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="c346b-133">In addition, rebate lines can be removed.</span></span>
