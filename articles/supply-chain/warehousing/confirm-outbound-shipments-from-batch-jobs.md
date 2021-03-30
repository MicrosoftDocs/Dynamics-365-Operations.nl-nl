---
title: Uitgaande zendingen vanuit batchtaken bevestigen
description: In dit onderwerp wordt beschreven hoe u een batchtaak instelt waarmee automatisch uitgaande transferorderzendingen worden bevestigd voor ladingen die gereed zijn om te verzenden.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4c4fd5e8cdea9a7fc05ec9cbc7866c44c6f78b2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243962"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="3443a-103">Uitgaande zendingen vanuit batchtaken bevestigen</span><span class="sxs-lookup"><span data-stu-id="3443a-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3443a-104">In dit onderwerp wordt beschreven hoe u een batchtaak instelt waarmee automatisch uitgaande transferorderzendingen worden bevestigd voor ladingen die gereed zijn om te verzenden.</span><span class="sxs-lookup"><span data-stu-id="3443a-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="3443a-105">De batchtaak die hier wordt beschreven, is alleen van toepassing op transferorders, niet op verkooporders.</span><span class="sxs-lookup"><span data-stu-id="3443a-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="3443a-106">Schakel de functie Uitgaande zendingen vanuit batchtaken bevestigen in</span><span class="sxs-lookup"><span data-stu-id="3443a-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="3443a-107">Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem.</span><span class="sxs-lookup"><span data-stu-id="3443a-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="3443a-108">Beheerders kunnen gebruikmaken van de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="3443a-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="3443a-109">U ziet de functie als:</span><span class="sxs-lookup"><span data-stu-id="3443a-109">The feature is listed as:</span></span>

- <span data-ttu-id="3443a-110">**Module** - *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="3443a-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="3443a-111">**Functienaam** - *Uitgaande zendingen vanuit batchtaken bevestigen*</span><span class="sxs-lookup"><span data-stu-id="3443a-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="3443a-112">Uitgaande zendingen verwerken</span><span class="sxs-lookup"><span data-stu-id="3443a-112">Process outbound shipments</span></span>

<span data-ttu-id="3443a-113">Een geplande batchtaak instellen voor het uitvoeren van de bevestiging van de uitgaande zending voor ladingen die gereed zijn voor verzending:</span><span class="sxs-lookup"><span data-stu-id="3443a-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="3443a-114">Ga naar **Magazijnbeheer \> Periodieke taken \> Uitgaande zendingen verwerken**.</span><span class="sxs-lookup"><span data-stu-id="3443a-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="3443a-115">Het dialoogvenster **Verzending bevestigen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="3443a-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="3443a-116">Selecteer **Filter** op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="3443a-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="3443a-117">Het dialoogvenster Query-editor wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="3443a-117">The query editor dialog box opens.</span></span> <span data-ttu-id="3443a-118">Voeg op het tabblad **Bereik** een rij met de volgende waarden toe.</span><span class="sxs-lookup"><span data-stu-id="3443a-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="3443a-119">**Tabel** - *Ladingen*</span><span class="sxs-lookup"><span data-stu-id="3443a-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="3443a-120">**Afgeleide tabel** - *Ladingen*</span><span class="sxs-lookup"><span data-stu-id="3443a-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="3443a-121">**Veld** - *Status lading*</span><span class="sxs-lookup"><span data-stu-id="3443a-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="3443a-122">**Criteria** - *Geladen*</span><span class="sxs-lookup"><span data-stu-id="3443a-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="3443a-123">Selecteer **OK** om terug te gaan naar het dialoogvenster **Verzending bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="3443a-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="3443a-124">Stel op het sneltabblad **Op de achtergrond uitvoeren** **Batchverwerking** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3443a-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="3443a-125">Selecteer op het tabblad **Op de achtergrond uitvoeren** de optie **Terugkeer**.</span><span class="sxs-lookup"><span data-stu-id="3443a-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="3443a-126">Het dialoogvenster **Terugkeerpatroon definiëren** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="3443a-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="3443a-127">Stel het uitvoeringsschema in voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3443a-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="3443a-128">Selecteer **OK** om terug te gaan naar het dialoogvenster **Verzending bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="3443a-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="3443a-129">Selecteer **OK** in het dialoogvenster **Verzending bevestigen** om de batchtaak aan de batchwachtrij toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3443a-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="3443a-130">Zie voor meer informatie [Overzicht van batchverwerking](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3443a-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]