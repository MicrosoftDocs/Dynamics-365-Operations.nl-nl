---
title: Productbeoordelingen synchroniseren in Dynamics 365 Retail
description: In dit onderwerp wordt beschreven hoe u productbeoordelingen in Microsoft Dynamics 365 Retail kunt synchroniseren.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698160"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a><span data-ttu-id="61733-103">Productbeoordelingen synchroniseren in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="61733-103">Sync product ratings in Dynamics 365 Retail</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="61733-104">In dit onderwerp wordt beschreven hoe u productbeoordelingen in Microsoft Dynamics 365 Retail kunt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="61733-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="61733-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="61733-105">Overview</span></span>

<span data-ttu-id="61733-106">Als u productbeoordelingen wilt gebruiken in omnichannels, zoals op het verkooppunt (POS) en in callcenters, moeten productbeoordelingen van de beoordelings- en revisieservice worden geïmporteerd in de database met detailhandelskanalen.</span><span class="sxs-lookup"><span data-stu-id="61733-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Retail channel database.</span></span> <span data-ttu-id="61733-107">Wanneer productbeoordelingen beschikbaar worden gemaakt in omnichannels, kunnen klanten tijdens hun interactie met verkoopmedewerkers indirect worden geholpen.</span><span class="sxs-lookup"><span data-stu-id="61733-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="61733-108">In dit onderwerp worden de volgende taken beschreven:</span><span class="sxs-lookup"><span data-stu-id="61733-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="61733-109">Een batchtaak configureren om productbeoordelingen voor detailhandel te importeren.</span><span class="sxs-lookup"><span data-stu-id="61733-109">Configure a Retail batch job to import product ratings.</span></span>
1. <span data-ttu-id="61733-110">Controleren of de batchtaak voor het synchroniseren van productbeoordelingen is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="61733-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="61733-111">Productbeoordelingen beschikbaar maken op het POS.</span><span class="sxs-lookup"><span data-stu-id="61733-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a><span data-ttu-id="61733-112">Een batchtaak configureren om productbeoordelingen voor detailhandel te importeren</span><span class="sxs-lookup"><span data-stu-id="61733-112">Configure a Retail batch job to import product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61733-113">Controleer voordat u begint of versie 10.0.6 of hoger van Retail is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="61733-113">Before you start, make sure that version 10.0.6 or later of Retail is installed.</span></span>

### <a name="initialize-the-retail-scheduler"></a><span data-ttu-id="61733-114">De Detailhandelplanner initialiseren</span><span class="sxs-lookup"><span data-stu-id="61733-114">Initialize the retail scheduler</span></span>

<span data-ttu-id="61733-115">Om de Detailhandelplanner te initialiseren, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="61733-115">To initialize the retail scheduler, follow these steps.</span></span>

1. <span data-ttu-id="61733-116">Ga naar **Retail \> Instelling van hoofdkantoor \> Detailhandelplanner \> Detailhandelplanner initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="61733-116">Go to **Retail \> Headquarters setup \> Retail scheduler \> Initialize retail scheduler**.</span></span> <span data-ttu-id="61733-117">U kunt ook zoeken naar "Detailhandelplanner initialiseren".</span><span class="sxs-lookup"><span data-stu-id="61733-117">Alternatively, search for "Initialize retail scheduler."</span></span>
1. <span data-ttu-id="61733-118">Controleer in het dialoogvenster **Detailhandelplanner initialiseren** of de optie **Bestaande configuratie verwijderen** is ingesteld op **Nee** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="61733-118">In the **Initialize retail scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="61733-119">De subtaak RetailproductRating controleren</span><span class="sxs-lookup"><span data-stu-id="61733-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="61733-120">Voer de volgende stappen uit om te controleren of de subtaak **RetailproductRating** bestaat.</span><span class="sxs-lookup"><span data-stu-id="61733-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="61733-121">Ga naar **Retail \> Instelling van hoofdkantoor \> Detailhandelplanner \> Plannersubtaken**.</span><span class="sxs-lookup"><span data-stu-id="61733-121">Go to **Retail \> Headquarters setup \> Retail scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="61733-122">U kunt ook zoeken naar "Plannersubtaken".</span><span class="sxs-lookup"><span data-stu-id="61733-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="61733-123">Zoek in de lijst met subtaken naar de subtaak **RetailproductRating**.</span><span class="sxs-lookup"><span data-stu-id="61733-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="61733-124">In de volgende afbeelding ziet u een voorbeeld van subtaakdetails in Retail.</span><span class="sxs-lookup"><span data-stu-id="61733-124">The following illustration shows an example of the subjob details in Retail.</span></span>

![Details van de subtaak RetailproductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="61733-126">Als u de subtaak **RetailproductRating** niet kunt vinden, hebt u mogelijk al de taak **Productbeoordelingen synchroniseren** en de **1040 CDX**-taak uitgevoerd voordat u de detailhandelplanner hebt geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="61733-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the retail scheduler.</span></span> <span data-ttu-id="61733-127">Voer in dat geval de volgende stappen uit om de taak **Volledige gegevenssynchronisatie** uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="61733-127">In this case, follow these steps to run the **Full data sync** job.</span></span>
>
> 1. <span data-ttu-id="61733-128">Ga naar **Retail \> Instelling van hoofdkantoor \> Detailhandelplanner \> Afzetkanaaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="61733-128">Go to **Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span> <span data-ttu-id="61733-129">U kunt ook zoeken naar "Afzetkanaaldatabase".</span><span class="sxs-lookup"><span data-stu-id="61733-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="61733-130">Selecteer de afzetkanaaldatabase die u wilt synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="61733-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="61733-131">Selecteer **Volledige gegevenssynchronisatie** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="61733-131">On the Action Pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="61733-132">Selecteer in de vervolgkeuzelijst **Een distributieplanning selecteren** de optie **1040-producten** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="61733-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="61733-133">Herhaal de stappen van de vorige procedure om te controleren of de subtaak **RetailproductRating** is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="61733-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="61733-134">Productbeoordelingen importeren</span><span class="sxs-lookup"><span data-stu-id="61733-134">Import product ratings</span></span>

<span data-ttu-id="61733-135">Voer de volgende stappen uit om productbeoordelingen in Retail te importeren vanuit de service voor beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="61733-135">To import product ratings into Retail from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="61733-136">Ga naar **Retail \> Instelling van hoofdkantoor \> Detailhandelplanner \> Beoordelingstaak product synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="61733-136">Go to **Retail \> Headquarters setup \> Retail scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="61733-137">U kunt ook zoeken naar "Beoordelingstaak product synchroniseren".</span><span class="sxs-lookup"><span data-stu-id="61733-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="61733-138">Selecteer in het dialoogvenster **Productbeoordelingen ophalen** op het sneltabblad **Uitvoeren op de achtergrond** de optie **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="61733-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="61733-139">Stel in het dialoogvenster **Terugkeerpatroon definiëren** een terugkeerpatroon in.</span><span class="sxs-lookup"><span data-stu-id="61733-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="61733-140">(De voorgestelde waarde is twee uur.) Plan geen terugkeerpatroon dat minder dan een uur duurt.</span><span class="sxs-lookup"><span data-stu-id="61733-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="61733-141">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="61733-141">Select **OK**.</span></span>
1. <span data-ttu-id="61733-142">Stel de optie **Batchproces** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="61733-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="61733-143">Met deze instelling wordt gegarandeerd dat u de logboeken en de status van de uitgevoerde batchtaken kunt controleren.</span><span class="sxs-lookup"><span data-stu-id="61733-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="61733-144">Selecteer **OK** om de batchtaak te plannen.</span><span class="sxs-lookup"><span data-stu-id="61733-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="61733-145">In de volgende afbeelding ziet u een voorbeeld van batchtaakconfiguratie in Retail.</span><span class="sxs-lookup"><span data-stu-id="61733-145">The following illustration shows an example of batch job configuration in Retail.</span></span>

![Configuratie van de batchtaak voor de synchronisatie van productbeoordelingen](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="61733-147">Controleren of de batchtaak voor het synchroniseren van productbeoordelingen is geslaagd</span><span class="sxs-lookup"><span data-stu-id="61733-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="61733-148">Ga als volgt te werk om te controleren of de batchtaak voor **synchroniseren van productbeoordelingen** is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="61733-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="61733-149">G naar **Retail \> Systeembeheerder \> Query's \> Batchtaken** of als u een voorraadeenheid (SKU) alleen voor Retail gebruikt, **Retail \> Query's en rapporten \> Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="61733-149">Go to **Retail \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Retail-only stock keeping unit (SKU), **Retail \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="61733-150">U kunt ook zoeken naar "Batchtaken".</span><span class="sxs-lookup"><span data-stu-id="61733-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="61733-151">Als u de details van de batchtaak wilt weergeven, zoekt u in de lijst met batchtaken in de kolom **Taakomschrijving** naar een omschrijving die "Productbeoordelingen ophalen" bevat.</span><span class="sxs-lookup"><span data-stu-id="61733-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="61733-152">Selecteer de taak-id om de details van de batchtaak weer te geven, zoals de geplande begindatum/-tijd en de tekst van het terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="61733-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="61733-153">In de volgende afbeelding ziet u een voorbeeld van de details van de batchtaak in Retail wanneer de batchtaak wordt uitgevoerd met een interval van twee uur.</span><span class="sxs-lookup"><span data-stu-id="61733-153">The following illustration shows an example of the batch job details in Retail when the batch job is scheduled to run at two-hour intervals.</span></span>

![Details van de batchtaak voor de synchronisatie van productbeoordelingen](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="61733-155">Productbeoordelingen beschikbaar maken op het POS</span><span class="sxs-lookup"><span data-stu-id="61733-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="61733-156">De oplossing Beoordelingen en recensies in Dynamics 365 Commerce is een omnichannel-oplossing.</span><span class="sxs-lookup"><span data-stu-id="61733-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="61733-157">Productbeoordelingen worden echter niet standaard weergegeven op het POS.</span><span class="sxs-lookup"><span data-stu-id="61733-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="61733-158">Om klanten in winkels de beoordelingen en recensies te laten zien wanneer ze worden geholpen door een verkoopmedewerer, moet u productbeoordelingen inschakelen op het POS.</span><span class="sxs-lookup"><span data-stu-id="61733-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="61733-159">Voer de volgende stappen uit om productbeoordelingen in te schakelen op het POS.</span><span class="sxs-lookup"><span data-stu-id="61733-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="61733-160">Ga naar **Detailhandel \> Instelling detailhandel \> Parameters \> Detailhandelparameters**.</span><span class="sxs-lookup"><span data-stu-id="61733-160">Go to **Retail \> Retail setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="61733-161">U kunt ook zoeken naar "Detailhandelparameters".</span><span class="sxs-lookup"><span data-stu-id="61733-161">Alternatively, search for "Retail parameters."</span></span>
1. <span data-ttu-id="61733-162">Selecteer **Nieuw** op het tabblad **Configuratieparameters**.</span><span class="sxs-lookup"><span data-stu-id="61733-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="61733-163">Voer een naam in zoals **RatingsAndReviews.EnableproductRatingsForRetailStores**, en stel de waarde in op **true**.</span><span class="sxs-lookup"><span data-stu-id="61733-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="61733-164">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="61733-164">Select **Save**.</span></span>
1. <span data-ttu-id="61733-165">Klik op **Detailhandel \> IT detailhandel \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="61733-165">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span> <span data-ttu-id="61733-166">U kunt ook naar "distributieplanning" zoeken.</span><span class="sxs-lookup"><span data-stu-id="61733-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="61733-167">Selecteer in de takenlijst **1110** (**algemene configuratie**) en selecteer **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="61733-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="61733-168">Nadat de taak is uitgevoerd, controleert u of de productbeoordelingen nu op het POS worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="61733-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="61733-169">In de volgende afbeelding ziet u een voorbeeld van de configuratie van de detailhandelparameters om productbeoordelingen in te schakelen op het POS.</span><span class="sxs-lookup"><span data-stu-id="61733-169">The following illustration shows an example of the configuration of the Retail parameters to turn on product ratings at the POS.</span></span>

![Configuratie van detailhandelparameters voor productbeoordelingen op het POS](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="61733-171">In de volgende afbeelding ziet u een voorbeeld van de productbeoordelingen op het POS.</span><span class="sxs-lookup"><span data-stu-id="61733-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Productbeoordelingen op het POS](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="61733-173">In de volgende afbeelding ziet u een voorbeeld van de productbeoordelingen in callcenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="61733-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Productbeoordelingen in een callcenterkanaal](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="61733-175">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="61733-175">Additional resources</span></span>

[<span data-ttu-id="61733-176">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="61733-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="61733-177">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="61733-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="61733-178">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="61733-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="61733-179">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="61733-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
