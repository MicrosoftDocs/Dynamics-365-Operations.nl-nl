---
title: Productie-uitvoeringsworkloads voor cloud- en edge-schaaleenheden
description: In dit onderwerp wordt beschreven hoe productie-uitvoeringsworkloads werken met cloud- en edge-schaaleenheden.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cd7dd8b9241171bdfdb3cc1379211a2fe99bbe1
ms.sourcegitcommit: 8d50c905a0c9d4347519549b587bdebab8ffc628
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2021
ms.locfileid: "6183991"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="b9641-103">Werkbelasting voor productie-uitvoering voor cloud- en randschaaleenheden</span><span class="sxs-lookup"><span data-stu-id="b9641-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="b9641-104">De werkbelasting voor productie-uitvoering is op dit moment als voorbeeld beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="b9641-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="b9641-105">Sommige bedrijfsfuncties worden niet volledig ondersteund in de openbare preview wanneer workloadschaaleenheden worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b9641-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="b9641-106">In de productie-uitvoering leveren schaaleenheden de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="b9641-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="b9641-107">Machineoperators en werkvloersupervisors kunnen toegang krijgen tot het operationele productieplan.</span><span class="sxs-lookup"><span data-stu-id="b9641-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="b9641-108">Machineoperators kunnen het plan up-to-date houden door afzonderlijke en procesproductietaken uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b9641-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="b9641-109">De werkvloersupervisor kan het operationele plan aanpassen.</span><span class="sxs-lookup"><span data-stu-id="b9641-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="b9641-110">Medewerkers hebben toegang tot tijd en aanwezigheid voor in- en uitklokken op de edge, om de juiste salarisberekening voor medewerkers te garanderen.</span><span class="sxs-lookup"><span data-stu-id="b9641-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="b9641-111">In dit onderwerp wordt beschreven hoe productie-uitvoeringsworkloads werken met cloud- en edge-schaaleenheden.</span><span class="sxs-lookup"><span data-stu-id="b9641-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="b9641-112">De levenscyclus van productie</span><span class="sxs-lookup"><span data-stu-id="b9641-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="b9641-113">Zoals in de volgende afbeelding wordt weergegeven, is de productielevenscyclus onderverdeeld in drie fasen: *Plannen*, *Uitvoeren* en *Voltooien*.</span><span class="sxs-lookup"><span data-stu-id="b9641-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="b9641-114">[![Productie-uitvoeringsfasen wanneer één omgeving wordt gebruikt](media/mes-phases.png "Productie-uitvoeringsfasen wanneer één omgeving wordt gebruikt")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="b9641-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="b9641-115">De _planfase_ omvat productdefinitie, planning, het maken en plannen van orders en vrijgave.</span><span class="sxs-lookup"><span data-stu-id="b9641-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="b9641-116">De vrijgavestap geeft de overgang van de _planfase_ naar de _uitvoeringsfase_ aan.</span><span class="sxs-lookup"><span data-stu-id="b9641-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="b9641-117">Wanneer een productieorder wordt vrijgegeven, worden de productieordertaken weergegeven op de productievloer en zijn ze klaar voor uitvoering.</span><span class="sxs-lookup"><span data-stu-id="b9641-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="b9641-118">Wanneer een productietaak is gemarkeerd als voltooid, wordt deze verplaatst van _uitvoeringsfase_ naar de _voltooiingsfase_.</span><span class="sxs-lookup"><span data-stu-id="b9641-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="b9641-119">In de _voltooiingsfase_ gaan de registraties van de *uitvoeringsfase* door een goedkeuringswerkstroom, waar ze worden berekend, goedgekeurd en overgebracht.</span><span class="sxs-lookup"><span data-stu-id="b9641-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="b9641-120">Op dat moment is de productieorder voltooid.</span><span class="sxs-lookup"><span data-stu-id="b9641-120">At that point, the production order is completed.</span></span> <span data-ttu-id="b9641-121">Dan wordt de basis voor het salaris van de medewerkers gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="b9641-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="b9641-122">De uitvoeringsfase opsplitsen in een afzonderlijke workload</span><span class="sxs-lookup"><span data-stu-id="b9641-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="b9641-123">Zoals u in de volgende afbeelding kunt zien, wordt de _uitvoeringsfase_ een afzonderlijke workload opgesplitst wanneer er schaaleenheden worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b9641-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="b9641-124">[![Productie-uitvoeringsfasen wanneer er schaaleenheden worden gebruikt](media/mes-phases-workloads.png "Productie-uitvoeringsfasen wanneer er schaaleenheden worden gebruikt")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="b9641-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="b9641-125">Het model gaat nu van een installatie met één exemplaar naar een model dat is gebaseerd op hub en schaaleenheden.</span><span class="sxs-lookup"><span data-stu-id="b9641-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="b9641-126">De _planfase_ en _voltooiingsfase_ worden uitgevoerd als back-upbewerkingen op de hub en de productie-uitvoeringsworkload wordt uitgevoerd op de schaaleenheden.</span><span class="sxs-lookup"><span data-stu-id="b9641-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="b9641-127">Gegevens worden asynchroon overgebracht tussen de hub en schaaleenheden.</span><span class="sxs-lookup"><span data-stu-id="b9641-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="b9641-128">Wanneer een productieorder op de hub wordt vrijgegeven, worden alle gegevens die nodig zijn voor het verwerken van productietaken, overgebracht naar de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="b9641-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="b9641-129">Deze gegevens omvatten productieorders, productieroutes, stuklijsten en producten.</span><span class="sxs-lookup"><span data-stu-id="b9641-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="b9641-130">Gegevens die niet zijn gerelateerd aan een productieorder (zoals indirecte activiteiten, verzuimcodes en productieparameters), worden ook van de hub overgezet naar de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="b9641-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="b9641-131">In de regel kunnen gegevens die afkomstig zijn van de hub en die worden overgebracht naar de schaaleenheid, alleen op de hub worden gemaakt of bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b9641-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="b9641-132">Er kan bijvoorbeeld geen nieuwe verzuimcode of indirecte activiteit worden gemaakt op de schaaleenheid&mdash;die kan alleen voor registratie worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b9641-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="b9641-133">De registraties die tijdens de uitvoering op de schaaleenheid worden uitgevoerd, worden vervolgens naar de hub overgebracht, waar tijd- en aanwezigheidsgoedkeuring, voorraad en financiële updates worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="b9641-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="b9641-134">Productie-uitvoeringstaken die kunnen worden uitgevoerd op workloads</span><span class="sxs-lookup"><span data-stu-id="b9641-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="b9641-135">De volgende productie-uitvoeringstaken kunnen momenteel worden uitgevoerd op workloads wanneer er schaaleenheden worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="b9641-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="b9641-136">Inklokken, aanmelden, uitklokken en verzuim</span><span class="sxs-lookup"><span data-stu-id="b9641-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="b9641-137">Taak beginnen</span><span class="sxs-lookup"><span data-stu-id="b9641-137">Start job</span></span>
- <span data-ttu-id="b9641-138">Taken bundelen</span><span class="sxs-lookup"><span data-stu-id="b9641-138">Bundle jobs</span></span>
- <span data-ttu-id="b9641-139">Voortgang melden</span><span class="sxs-lookup"><span data-stu-id="b9641-139">Report progress</span></span>
- <span data-ttu-id="b9641-140">Uitval rapporteren</span><span class="sxs-lookup"><span data-stu-id="b9641-140">Report scrap</span></span>
- <span data-ttu-id="b9641-141">Indirecte activiteit</span><span class="sxs-lookup"><span data-stu-id="b9641-141">Indirect activity</span></span>
- <span data-ttu-id="b9641-142">Pauze</span><span class="sxs-lookup"><span data-stu-id="b9641-142">Break</span></span>
- <span data-ttu-id="b9641-143">Gereedmelden en wegzetten (vereist dat u ook de werkbelasting van de magazijnuitvoering op uw schaaleenheid uitvoert, zie ook [Gereedmelden en wegzetten in een schaaleenheid](#RAF))</span><span class="sxs-lookup"><span data-stu-id="b9641-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="b9641-144">Werken met productie-uitvoeringsworkloads op de hub</span><span class="sxs-lookup"><span data-stu-id="b9641-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="b9641-145">Gewoonlijk worden de processen die nodig zijn om de productie-uitvoeringsworkloads uit te voeren, automatisch uitgevoerd om de hub en alle schaaleenheden waar nodig synchroon te houden.</span><span class="sxs-lookup"><span data-stu-id="b9641-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b9641-146">Als u echter problemen ondervindt, kunt u handmatig de verwerking van onbewerkte registraties activeren die worden ontvangen van workloads en/of het registratieverwerkingslogbestand controleren.</span><span class="sxs-lookup"><span data-stu-id="b9641-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="b9641-147">Onbewerkte registraties handmatig verwerken</span><span class="sxs-lookup"><span data-stu-id="b9641-147">Manually process raw registrations</span></span>

<span data-ttu-id="b9641-148">Een batchtaak in Supply Chain Management wordt automatisch uitgevoerd om alle registraties te verwerken die van de workloads zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="b9641-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="b9641-149">Met deze taak worden de vereiste productiejournalen en logbestandsvermeldingen gemaakt wanneer een registratie wordt verwerkt voor een voltooide taak in de workload.</span><span class="sxs-lookup"><span data-stu-id="b9641-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="b9641-150">Hoewel de taak normaal gesproken automatisch wordt uitgevoerd, kunt u deze op elk gewenst moment handmatig uitvoeren door u aan te melden bij de hub en naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Onbewerkte registraties verwerken** te gaan.</span><span class="sxs-lookup"><span data-stu-id="b9641-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="b9641-151">Het verwerkingslogbestand voor onbewerkte registraties controleren</span><span class="sxs-lookup"><span data-stu-id="b9641-151">Check the raw registration processing log</span></span>

<span data-ttu-id="b9641-152">Als u het registratieverwerkingslogbestand wilt bekijken, meldt u zich aan bij de hub en gaat u naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Logbestand onbewerkte registratieverwerking**.</span><span class="sxs-lookup"><span data-stu-id="b9641-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="b9641-153">Op de pagina **Logbestand voor onbewerkte registratieverwerking** wordt een lijst met verwerkte onbewerkte registraties en de status van elke registratie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b9641-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="b9641-154">![De pagina Logbestand voor onbewerkte registratieverwerking](media/mes-processing-log.png "De pagina Logbestand voor onbewerkte registratieverwerking")</span><span class="sxs-lookup"><span data-stu-id="b9641-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="b9641-155">U kunt aan elke registratie in de lijst werken door deze te selecteren en vervolgens een van de volgende knoppen in het actiedeelvenster te selecteren:</span><span class="sxs-lookup"><span data-stu-id="b9641-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b9641-156">**Verwerken**: de geselecteerde registratie handmatig verwerken.</span><span class="sxs-lookup"><span data-stu-id="b9641-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="b9641-157">Deze actie kan handig zijn als de taak _Onbewerkte registraties verwerken_ niet is uitgevoerd of als deze is mislukt.</span><span class="sxs-lookup"><span data-stu-id="b9641-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="b9641-158">**Annuleren**: de geselecteerde registratie annuleren.</span><span class="sxs-lookup"><span data-stu-id="b9641-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="b9641-159">Werken met productie-uitvoeringsworkloads op een schaaleenheid</span><span class="sxs-lookup"><span data-stu-id="b9641-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="b9641-160">Gewoonlijk worden de processen die nodig zijn om de productie-uitvoeringsworkloads uit te voeren, automatisch uitgevoerd om de hub en alle schaaleenheden waar nodig synchroon te houden.</span><span class="sxs-lookup"><span data-stu-id="b9641-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b9641-161">Als u echter problemen ondervindt, kunt u de geschiedenis van orders controleren die op een schaaleenheid zijn verwerkt of handmatig de taak _Berichtverwerker productiehub naar schaaleenheid_ uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b9641-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="b9641-162">De geschiedenis weergeven van de productietaken die op een schaaleenheid zijn verwerkt</span><span class="sxs-lookup"><span data-stu-id="b9641-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="b9641-163">Als u de geschiedenis wilt weergeven van de productietaken die op een schaaleenheid zijn verwerkt, meldt u zich aan bij de computer voor de schaaleenheid en gaat u naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Verwerkingsgeschiedenis van productietaken**.</span><span class="sxs-lookup"><span data-stu-id="b9641-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="b9641-164">Op de pagina **Verwerkingsgeschiedenis van productietaken** wordt de verwerkingsgeschiedenis van de productieorders op de schaaleenheid weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b9641-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="b9641-165">U kunt aan elke productieorder in de lijst werken door deze te selecteren en vervolgens een van de volgende knoppen in het actiedeelvenster te selecteren:</span><span class="sxs-lookup"><span data-stu-id="b9641-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b9641-166">**Verwerken**: de geselecteerde productieorder handmatig verwerken.</span><span class="sxs-lookup"><span data-stu-id="b9641-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="b9641-167">**Annuleren**: de geselecteerde productieorder annuleren.</span><span class="sxs-lookup"><span data-stu-id="b9641-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="b9641-168">De taak Berichtverwerker productiehub naar schaaleenheid</span><span class="sxs-lookup"><span data-stu-id="b9641-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="b9641-169">De taak _Berichtverwerker productiehub naar schaaleenheid_ verwerkt gegevens van de hub naar de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="b9641-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="b9641-170">Deze taak wordt automatisch gestart wanneer de productie-uitvoeringsworkload wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="b9641-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="b9641-171">U kunt dit echter op elk gewenst moment handmatig uitvoeren door naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Berichtverwerker productiehub naar schaaleenheid** te gaan.</span><span class="sxs-lookup"><span data-stu-id="b9641-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="b9641-172">Gereedmelden en wegzetten in een schaaleenheid</span><span class="sxs-lookup"><span data-stu-id="b9641-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="b9641-173">In de huidige versie worden de bewerkingen voor gereedmelden en wegzetten (voor eindproducten, coproducten en bijproducten) ondersteund door de [werkbelasting voor magazijnuitvoering](cloud-edge-workload-warehousing.md) (niet door de werkbelasting van de productie-uitvoering).</span><span class="sxs-lookup"><span data-stu-id="b9641-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="b9641-174">Als u deze functionaliteit wilt gebruiken wanneer deze is gekoppeld aan een schaaleenheid, moet u daarom het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="b9641-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="b9641-175">Installeer zowel de werkbelasting voor magazijnuitvoering als de werkbelasting voor de productie-uitvoering in uw schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="b9641-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="b9641-176">Gebruik de mobiele app Warehouse Management om gereed te melden en het wegzetwerk te verwerken.</span><span class="sxs-lookup"><span data-stu-id="b9641-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="b9641-177">Deze processen worden momenteel niet ondersteund in de uitvoeringsinterface voor de productievloer.</span><span class="sxs-lookup"><span data-stu-id="b9641-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
