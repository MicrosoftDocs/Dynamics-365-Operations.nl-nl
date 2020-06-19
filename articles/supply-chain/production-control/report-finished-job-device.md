---
title: Gereedmelden via het apparaat voor taakkaarten
description: In dit onderwerp wordt beschreven hoe u het systeem zo configureert dat gebruikers van een apparaat voor taakkaarten producten van een productieorder naar de voorraad kunnen gereedmelden.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403257"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="783a9-103">Gereedmelden via het apparaat voor taakkaarten</span><span class="sxs-lookup"><span data-stu-id="783a9-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="783a9-104">Werknemers gebruiken de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten om voltooide hoeveelheden voor een productietaak te rapporteren.</span><span class="sxs-lookup"><span data-stu-id="783a9-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="783a9-105">Bepalen of hoeveelheden die zijn gereedgemeld, moeten worden toegevoegd aan voorraad</span><span class="sxs-lookup"><span data-stu-id="783a9-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="783a9-106">Volg deze stappen om te bepalen of en hoe de hoeveelheden die zijn gereedgemeld voor de laatste bewerking, moeten worden toegevoegd aan voorraad.</span><span class="sxs-lookup"><span data-stu-id="783a9-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="783a9-107">Ga naar **Productiebeheer \> Instellingen \> Productieregistratie \> Standaardwaarden van productieorder**.</span><span class="sxs-lookup"><span data-stu-id="783a9-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="783a9-108">Stel op het tabblad **Rapporteren als gereed** het veld **Gereedmelding online bijwerken** in op een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="783a9-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="783a9-109">**Nee**: er wordt geen hoeveelheid aan voorraad toegevoegd wanneer hoeveelheden worden gerapporteerd voor de laatste bewerking.</span><span class="sxs-lookup"><span data-stu-id="783a9-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="783a9-110">De status van de productieorder wordt nooit gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="783a9-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="783a9-111">**Status + hoeveelheid**: de status van de productieorder wordt gewijzigd in *Gereedgemeld* en de hoeveelheid wordt gereedgemeld voor de voorraad.</span><span class="sxs-lookup"><span data-stu-id="783a9-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="783a9-112">**Hoeveelheid**: de hoeveelheid wordt gereedgemeld voor de voorraad, maar de status van de productieorder wijzigt nooit.</span><span class="sxs-lookup"><span data-stu-id="783a9-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="783a9-113">**Status**: alleen de status van de productieorder wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="783a9-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="783a9-114">Er worden geen hoeveelheden aan voorraad toegevoegd wanneer hoeveelheden worden gerapporteerd voor de laatste bewerking.</span><span class="sxs-lookup"><span data-stu-id="783a9-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="783a9-115">Hoeveelheden worden niet in de voorraad bijgehouden als de bewerkingen waarvoor ze zijn gereedgemeld, niet zijn gedefinieerd als de laatste bewerking.</span><span class="sxs-lookup"><span data-stu-id="783a9-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="783a9-116">Deze hoeveelheden kunnen echter worden gebruikt om de voortgang weer te geven.</span><span class="sxs-lookup"><span data-stu-id="783a9-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="783a9-117">Ze kunnen ook worden opgenomen in regels die bepalen of werknemers de volgende bewerking kunnen starten voordat een gedefinieerde drempelwaarde van de gerapporteerde hoeveelheden voor de vorige bewerking wordt bereikt.</span><span class="sxs-lookup"><span data-stu-id="783a9-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="783a9-118">U kunt deze regels definiëren op het tabblad **Validatie hoeveelheid** van de pagina **Standaardwaarden van productieorder**.</span><span class="sxs-lookup"><span data-stu-id="783a9-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="783a9-119">Zie [Productieparameters in Productieregistratie](production-parameters-manufacturing-execution.md) voor meer informatie over het werken met de pagina **Standaardwaarden van productieorder**.</span><span class="sxs-lookup"><span data-stu-id="783a9-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="783a9-120">Batchartikelen gereedmelden</span><span class="sxs-lookup"><span data-stu-id="783a9-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="783a9-121">Het apparaat voor taakkaarten ondersteunt drie scenario's voor het rapporteren van batchartikelen.</span><span class="sxs-lookup"><span data-stu-id="783a9-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="783a9-122">Deze scenario's zijn zowel van toepassing op artikelen die zijn ingeschakeld voor geavanceerde magazijnprocessen als voor artikelen die niet zijn ingeschakeld voor geavanceerde magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="783a9-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="783a9-123">**Handmatig toegewezen batchnummers:** werknemers voeren een aangepast batchnummer in.</span><span class="sxs-lookup"><span data-stu-id="783a9-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="783a9-124">Dit batchnummer kan afkomstig zijn van een externe bron die niet bekend is bij het systeem.</span><span class="sxs-lookup"><span data-stu-id="783a9-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="783a9-125">**Vooraf gedefinieerde batchnummers:** werknemers selecteren een batchnummer in een lijst met batchnummers die automatisch door het systeem worden gegenereerd voordat de productieorder wordt vrijgegeven naar het apparaat voor taakkaarten.</span><span class="sxs-lookup"><span data-stu-id="783a9-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="783a9-126">**Vaste batchnummers:** werknemers typen of selecteren geen batchnummer.</span><span class="sxs-lookup"><span data-stu-id="783a9-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="783a9-127">In plaats daarvan wijst het systeem automatisch een batchnummer toe aan de productieorder voordat deze wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="783a9-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="783a9-128">Voer de volgende stappen uit om een scenario in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="783a9-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="783a9-129">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="783a9-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="783a9-130">Selecteer het product om te configureren.</span><span class="sxs-lookup"><span data-stu-id="783a9-130">Select the product to configure.</span></span>
1. <span data-ttu-id="783a9-131">Selecteer op het sneltabblad **Voorraad beheren** in het veld **Batchnummergroep** de traceringsnummergroep die is ingesteld om uw scenario te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="783a9-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="783a9-132">Als er geen batchnummergroep is toegewezen aan een batchproduct, biedt het apparaat voor taakkaarten tijdens het rapporteren als gereed standaard handmatige invoer voor het batchnummer.</span><span class="sxs-lookup"><span data-stu-id="783a9-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="783a9-133">In de volgende subsecties wordt beschreven hoe u traceringsnummergroepen instelt ter ondersteuning van elk van de drie scenario's voor het rapporteren van batchartikelen.</span><span class="sxs-lookup"><span data-stu-id="783a9-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="783a9-134">Rapportage van batchnummers inschakelen op het apparaat voor taakkaarten</span><span class="sxs-lookup"><span data-stu-id="783a9-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="783a9-135">Om ervoor te zorgen dat uw apparaat voor taakkaarten een batchnummer kan accepteren tijdens de gereedmelding, moet u [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de volgende functies in te schakelen (in deze volgorde):</span><span class="sxs-lookup"><span data-stu-id="783a9-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="783a9-136">Verbeterde gebruikerservaring voor het rapportvoortgangsvenster op het apparaat voor taakkaart</span><span class="sxs-lookup"><span data-stu-id="783a9-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="783a9-137">Schakel deze optie in als u batch- en serienummers wilt invoeren bij het gereedmelden vanaf het apparaat van de taakkaart (preview)</span><span class="sxs-lookup"><span data-stu-id="783a9-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="783a9-138">Een traceringsnummergroep instellen waarmee werknemers handmatig een batchnummer kunnen toewijzen</span><span class="sxs-lookup"><span data-stu-id="783a9-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="783a9-139">Voer de volgende stappen uit om een traceringsnummergroep in te stellen en handmatig toegewezen batchnummers toe te staan.</span><span class="sxs-lookup"><span data-stu-id="783a9-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="783a9-140">Ga naar **Voorraadbeheer \> Instellingen \> Dimensies \> Traceringsnummergroepen**.</span><span class="sxs-lookup"><span data-stu-id="783a9-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="783a9-141">Maak of selecteer de traceringsnummergroep die u wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="783a9-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="783a9-142">Stel op het sneltabblad **Algemeen** de optie **Handmatig** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="783a9-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="783a9-143">![De pagina Groepen traceringsnummers](media/tracking-number-group-manual.png "De pagina Groepen traceringsnummers")</span><span class="sxs-lookup"><span data-stu-id="783a9-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="783a9-144">Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als batchnummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="783a9-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="783a9-145">Wanneer u dit scenario gebruikt, is het veld **Batchnummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een tekstvak waarin werknemers een willekeurige waarde kunnen invoeren.</span><span class="sxs-lookup"><span data-stu-id="783a9-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="783a9-146">![De pagina Voortgang rapporteren met een veld voor handmatige batchnummers](media/job-card-device-batch-manual.png "De pagina Voortgang rapporteren met een veld voor handmatige batchnummers")</span><span class="sxs-lookup"><span data-stu-id="783a9-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="783a9-147">Een traceringsnummergroep instellen die een lijst met vooraf gedefinieerde batchnummers bevat</span><span class="sxs-lookup"><span data-stu-id="783a9-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="783a9-148">Voer de volgende stappen uit om een traceringsnummergroep in te stellen en een lijst met vooraf gedefinieerde batchnummers te bieden.</span><span class="sxs-lookup"><span data-stu-id="783a9-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="783a9-149">Ga naar **Voorraadbeheer \> Instellingen > Dimensies \> Traceringsnummergroepen**.</span><span class="sxs-lookup"><span data-stu-id="783a9-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="783a9-150">Maak of selecteer de traceringsnummergroep die u wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="783a9-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="783a9-151">Stel op het sneltabblad **Algemeen** de optie **Alleen voor voorraadtransacties** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="783a9-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="783a9-152">Gebruik het veld **Per hoev.** om batchnummers per hoeveelheid te splitsen op basis van de waarde die u invoert.</span><span class="sxs-lookup"><span data-stu-id="783a9-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="783a9-153">Stel dat u een productieorder hebt voor tien stuks en dat het veld **Per hoev.** is ingesteld op *2*.</span><span class="sxs-lookup"><span data-stu-id="783a9-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="783a9-154">In dit geval worden er vijf batchnummers toegewezen aan de productieorder wanneer deze wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="783a9-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="783a9-155">![De pagina Groepen traceringsnummers](media/tracking-number-group-predefined.png "De pagina Groepen traceringsnummers")</span><span class="sxs-lookup"><span data-stu-id="783a9-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="783a9-156">Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als batchnummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="783a9-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="783a9-157">Wanneer u dit scenario gebruikt, is het veld **Batchnummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een vervolgkeuzelijst is waarin werknemers een vooraf gedefinieerde waarde moeten selecteren.</span><span class="sxs-lookup"><span data-stu-id="783a9-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="783a9-158">![De pagina Voortgang rapporteren met een lijst met vooraf gedefinieerde batchnummers](media/job-card-device-batch-predefined.png "De pagina Voortgang rapporteren met een lijst met vooraf gedefinieerde batchnummers")</span><span class="sxs-lookup"><span data-stu-id="783a9-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="783a9-159">Een traceringsnummergroep instellen waarmee automatisch batchnummers worden toegewezen</span><span class="sxs-lookup"><span data-stu-id="783a9-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="783a9-160">Als batchnummers automatisch moeten worden toegewezen, zonder invoer van de werknemer, voert u deze stappen uit om een traceringsnummergroep in te stellen.</span><span class="sxs-lookup"><span data-stu-id="783a9-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="783a9-161">Ga naar **Voorraadbeheer \> Instellingen \> Dimensies \> Traceringsnummergroepen**.</span><span class="sxs-lookup"><span data-stu-id="783a9-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="783a9-162">Maak of selecteer de traceringsnummergroep die u wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="783a9-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="783a9-163">Stel op het sneltabblad **Algemeen** de optie **Alleen voor voorraadtransacties** in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="783a9-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="783a9-164">Stel de optie **Handmatig** in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="783a9-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="783a9-165">![De pagina Groepen traceringsnummers](media/tracking-number-group-fixed.png "De pagina Groepen traceringsnummers")</span><span class="sxs-lookup"><span data-stu-id="783a9-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="783a9-166">Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als batchnummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="783a9-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="783a9-167">Wanneer u dit scenario gebruikt, bevat het veld **Batchnummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een waarde, maar kunnen werknemers deze niet bewerken.</span><span class="sxs-lookup"><span data-stu-id="783a9-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="783a9-168">![De pagina Voortgang rapporteren met een vast batchnummer](media/job-card-device-batch-fixed.png "De pagina Voortgang rapporteren met een vast batchnummer")</span><span class="sxs-lookup"><span data-stu-id="783a9-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="783a9-169">Melden als voltooid aan een nummerplaat</span><span class="sxs-lookup"><span data-stu-id="783a9-169">Report as finished to a license plate</span></span>

<span data-ttu-id="783a9-170">Met geavanceerde magazijnprocessen kan de nummerplaatdimensie worden gebruikt om de voorraad bij te houden voor magazijnlocaties die voor dit doel zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="783a9-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="783a9-171">In dat geval is het nummerplaatnummer vereist wanneer een werknemer hoeveelheden meldt als voltooid.</span><span class="sxs-lookup"><span data-stu-id="783a9-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="783a9-172">Afdrukken van nummerplaatrapportgae en -label inschakelen</span><span class="sxs-lookup"><span data-stu-id="783a9-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="783a9-173">Als u de functies wilt gebruiken die in deze sectie worden beschreven, moet u [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de volgende functies in te schakelen (in deze volgorde):</span><span class="sxs-lookup"><span data-stu-id="783a9-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="783a9-174">Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten</span><span class="sxs-lookup"><span data-stu-id="783a9-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="783a9-175">Het automatisch genereren van nummerplaatnummers inschakelen bij het gereedmelden in het apparaat voor taakkaarten</span><span class="sxs-lookup"><span data-stu-id="783a9-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="783a9-176">Label afdrukken vanaf apparaat voor taakkaart</span><span class="sxs-lookup"><span data-stu-id="783a9-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="783a9-177">Melden als voltooid aan een nummerplaat instellen</span><span class="sxs-lookup"><span data-stu-id="783a9-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="783a9-178">Voer de volgende stappen uit om te bepalen of werknemers een bestaande nummerplaat opnieuw moeten gebruiken of een nieuwe nummerplaat moeten genereren wanneer ze hoeveelheden gereedmelden.</span><span class="sxs-lookup"><span data-stu-id="783a9-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="783a9-179">Ga naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Taakkaart configureren voor apparaten**.</span><span class="sxs-lookup"><span data-stu-id="783a9-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="783a9-180">Stel voor elk apparaat de volgende opties in:</span><span class="sxs-lookup"><span data-stu-id="783a9-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="783a9-181">**Nummerplaat maken**: stel deze optie in op **Ja** om voor elke gereedmelding een nieuwe nummerplaat te genereren.</span><span class="sxs-lookup"><span data-stu-id="783a9-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="783a9-182">Stel de optie in op **Nee** als een bestaande nummerplaat moet worden gebruikt voor elke gereedmelding.</span><span class="sxs-lookup"><span data-stu-id="783a9-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="783a9-183">**Label afdrukken**: stel deze optie in op **Ja** als de werknemer een nummerplaatlabel voor elke gereedmelding moet afdrukken.</span><span class="sxs-lookup"><span data-stu-id="783a9-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="783a9-184">Stel deze optie in op **Nee** als geen label vereist is.</span><span class="sxs-lookup"><span data-stu-id="783a9-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="783a9-185">![De pagina Taakkaart configureren voor apparaten](media/config-job-card-raf.png "De pagina Taakkaart configureren voor apparaten")</span><span class="sxs-lookup"><span data-stu-id="783a9-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="783a9-186">Ga naar **Magazijnbeheer \> Instellen \> Documentroutering \> Documentroutering** om het label te configureren.</span><span class="sxs-lookup"><span data-stu-id="783a9-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="783a9-187">Zie [Afdrukken van nummerplaatlabel inschakelen](../warehousing/tasks/license-plate-label-printing.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="783a9-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
