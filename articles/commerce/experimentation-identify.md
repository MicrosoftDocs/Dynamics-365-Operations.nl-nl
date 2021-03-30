---
title: Een hypothese opstellen en metrische gegevens bepalen voor een experiment
description: In dit onderwerp wordt beschreven hoe u de hypothese en metrische gegevens voor succes kunt identificeren voor een experiment dat u uitvoert op een e-Commerce-website in Dynamics 365 Commerce.
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
ms.openlocfilehash: 91614cda804cae4574fce4c9cfb31c63d876f19b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238625"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="bb3bd-103">Een hypothese opstellen en metrische gegevens voor succes bepalen voor een experiment</span><span class="sxs-lookup"><span data-stu-id="bb3bd-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="bb3bd-104">De eerste fase in de levenscyclus van het experiment omvat de identificatie van de hypothese voor het experiment en het bepalen van de metrische gegevens die u zult volgen om succes te beoordelen.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="bb3bd-105">In het volgende diagram ziet u alle stappen voor het [instellen en uitvoeren van een experiment](experimentation-overview.md) op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bb3bd-106">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="bb3bd-107">[ ![Traject van gebruiker voor experimenten - identificeren](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bb3bd-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="bb3bd-108">Een hypothese is een verklaring waarin u het resultaat van het experiment voorspelt.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="bb3bd-109">Veel factoren zijn aan de orde bij het definiëren van een hypothese, bijvoorbeeld bij onderzoek naar gebruikersgedrag en websitegegevens die u hebt verzameld.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="bb3bd-110">Met de hypothese definieert u de veronderstelling of theorie die u met uw experiment wilt valideren.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="bb3bd-111">Een voorbeeld van een hypothese voor uw experiment is: "*tijdens de zomermaanden zorgt een afbeelding van een wit t-shirt op mijn startpagina voor een hogere doorkliksnelheid dan een blauwe sweater, omdat mensen in de zomer iets met een licht gewicht en lichte kleur willen dragen.*"</span><span class="sxs-lookup"><span data-stu-id="bb3bd-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="bb3bd-112">In dat geval maakt u variaties die een wit t-shirt en een blauwe sweater bevatten en publiceert u beide tegelijkertijd.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="bb3bd-113">Om een hypothese te valideren moet het slagen of mislukken van een experiment rechtstreeks aan de acties van gebruikers zijn gekoppeld. Bijvoorbeeld als de gebruiker van de website op een koppeling of knop klikt.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="bb3bd-114">Deze acties moeten overeenkomen met gebeurtenissen die worden gerapporteerd aan de service van derden waarmee het experiment wordt gevolgd.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="bb3bd-115">Na verloop van tijd wordt het percentage gebruikers dat de actie uitvoert, geregistreerd als een metrisch gegeven dat u kunt gebruiken om rapporten te genereren en analyses uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="bb3bd-116">Raadpleeg het onderwerp [Commerce-onderdeelgebeurtenissen voor diagnose en probleemoplossing](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) als u alle beschikbare gebeurtenissen en kenmerken wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="bb3bd-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="bb3bd-117">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="bb3bd-117">Previous step</span></span>
[<span data-ttu-id="bb3bd-118">Experimenten in Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb3bd-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="bb3bd-119">Volgende stap</span><span class="sxs-lookup"><span data-stu-id="bb3bd-119">Next step</span></span>
[<span data-ttu-id="bb3bd-120">Een experiment opzetten</span><span class="sxs-lookup"><span data-stu-id="bb3bd-120">Set up an experiment</span></span>](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]