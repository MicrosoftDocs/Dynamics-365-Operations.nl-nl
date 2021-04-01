---
title: Een experiment instellen
description: In dit onderwerp wordt beschreven hoe u een experiment in een service van derden instelt.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dfd7b8cb13f4d69811b5a86b971fa1b57c75bd36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234604"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="0fec1-103">Een experiment instellen</span><span class="sxs-lookup"><span data-stu-id="0fec1-103">Set up an experiment</span></span>

<span data-ttu-id="0fec1-104">Nadat u [een hypothese hebt gedefinieerd en hebt bepaald welke metrische gegevens voor succes u wilt gebruiken](experimentation-identify.md), moet u uw experiment instellen in de service van derden.</span><span class="sxs-lookup"><span data-stu-id="0fec1-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="0fec1-105">In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0fec1-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0fec1-106">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="0fec1-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="0fec1-107">[ ![Traject van gebruiker voor experimenten - instellen](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0fec1-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="0fec1-108">Uw experiment in de service van derden instellen</span><span class="sxs-lookup"><span data-stu-id="0fec1-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="0fec1-109">U moet een service van derden hebben gekozen om uw experiment uit te voeren en te controleren en om de experimentconnector in te stellen.</span><span class="sxs-lookup"><span data-stu-id="0fec1-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="0fec1-110">Deze voorwaarden worden vermeld in [Experimenten in Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0fec1-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="0fec1-111">Voer de stappen uit die nodig zijn om uw experiment te maken in de service van derden.</span><span class="sxs-lookup"><span data-stu-id="0fec1-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="0fec1-112">Als de connector juist is geconfigureerd, wordt de volledige lijst met experimenten die u in de service van derden hebt ingesteld, binnen ongeveer 5 minuten in Commerce Site Builder weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0fec1-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="0fec1-113">Uw metrische gegevens voor succes instellen</span><span class="sxs-lookup"><span data-stu-id="0fec1-113">Set up your success metrics</span></span>
<span data-ttu-id="0fec1-114">Voor elk experiment zijn metrische gegevens nodig om de impact van de variaties te meten en de hypothese te valideren.</span><span class="sxs-lookup"><span data-stu-id="0fec1-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="0fec1-115">Voer de volgende stappen uit om de berekening van metrische gegevens in de service van derden via live telemetrie-gebeurtenissen in te schakelen in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0fec1-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0fec1-116">Voer de volgende stappen uit om uw metrische gegevens voor succes in te stellen.</span><span class="sxs-lookup"><span data-stu-id="0fec1-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="0fec1-117">Selecteer in Commerce Site Builder **Pagina's** in het linkernavigatievenster en selecteer vervolgens de pagina waarvoor u metrische gegevens wilt verzamelen.</span><span class="sxs-lookup"><span data-stu-id="0fec1-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="0fec1-118">Ga naar de sectie **Bij te houden gebeurtenis-ID´s** in het eigenschappenvenster aan de rechterzijde van de pagina of module die u wilt bijhouden.</span><span class="sxs-lookup"><span data-stu-id="0fec1-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="0fec1-119">Selecteer **Weergeven**.</span><span class="sxs-lookup"><span data-stu-id="0fec1-119">Select **View**.</span></span> <span data-ttu-id="0fec1-120">Er wordt een lijst weergegeven met alle gebeurtenis-ID's.</span><span class="sxs-lookup"><span data-stu-id="0fec1-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="0fec1-121">Kopieer de gebeurtenis die u wilt bijhouden en plak de gebeurtenissleutel op de opgegeven locatie in de service van derden.</span><span class="sxs-lookup"><span data-stu-id="0fec1-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="0fec1-122">Als u meer dan één gebeurtenis nodig hebt, kopieert u de sleutels een voor een.</span><span class="sxs-lookup"><span data-stu-id="0fec1-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="0fec1-123">Voor meer informatie over het weergeven van alle beschikbare gebeurtenissen en kenmerken, waaronder paginaweergaven en opbrengstentracering, raadpleegt u [Commerce-onderdeelgebeurtenissen voor diagnose en probleemoplossing](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="0fec1-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="0fec1-124">Voer eventuele andere stappen uit voor het bijhouden van metrische gegevens zoals in de service van derden is vereist.</span><span class="sxs-lookup"><span data-stu-id="0fec1-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="0fec1-125">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="0fec1-125">Previous step</span></span>
[<span data-ttu-id="0fec1-126">Een hypothese opstellen en metrische gegevens bepalen voor een experiment</span><span class="sxs-lookup"><span data-stu-id="0fec1-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="0fec1-127">Volgende stap</span><span class="sxs-lookup"><span data-stu-id="0fec1-127">Next step</span></span>
[<span data-ttu-id="0fec1-128">Een experiment verbinden en bewerken</span><span class="sxs-lookup"><span data-stu-id="0fec1-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]