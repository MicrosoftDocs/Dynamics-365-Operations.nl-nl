---
title: Wijzigingen van levensgebeurtenissen verwerken
description: U kunt wijzigingen in levensgebeurtenissen verwerken in Microsoft Dynamics 365 Human Resources bij wijzigingen in levensgebeurtenissen.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d32d6ba893a99149e27f644ac80e430db3c08fa0
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112104"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="1b13d-103">Wijzigingen van levensgebeurtenissen verwerken</span><span class="sxs-lookup"><span data-stu-id="1b13d-103">Process life event changes</span></span>

<span data-ttu-id="1b13d-104">U kunt wijzigingen in levensgebeurtenissen verwerken in Microsoft Dynamics 365 Human Resources voor twee levensgebeurtenissen:</span><span class="sxs-lookup"><span data-stu-id="1b13d-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="1b13d-105">Verjaardagswijzigingen</span><span class="sxs-lookup"><span data-stu-id="1b13d-105">Birthday changes</span></span>
- <span data-ttu-id="1b13d-106">Wijzigingen in de vervaldatum voor het negeren van een geschiktheidsregel</span><span class="sxs-lookup"><span data-stu-id="1b13d-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="1b13d-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Wijziging in levensgebeurtenis verwerken**.</span><span class="sxs-lookup"><span data-stu-id="1b13d-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="1b13d-108">Geef in het dialoogvenster **Wijzigingsproces voor levensgebeurtenissen uitvoeren** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="1b13d-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="1b13d-109">Veld</span><span class="sxs-lookup"><span data-stu-id="1b13d-109">Field</span></span> | <span data-ttu-id="1b13d-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1b13d-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1b13d-111">Inschrijvingsperiode</span><span class="sxs-lookup"><span data-stu-id="1b13d-111">Enrollment period</span></span> | <span data-ttu-id="1b13d-112">De inschrijvingsperiode waarvoor de wijzigingen in de levensgebeurtenis moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="1b13d-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="1b13d-113">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="1b13d-113">Legal entity</span></span> | <span data-ttu-id="1b13d-114">De rechtspersoon waarvoor de wijzigingen in de levensgebeurtenis moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="1b13d-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="1b13d-115">Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="1b13d-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="1b13d-116">Voer gegevens in voor het proces.</span><span class="sxs-lookup"><span data-stu-id="1b13d-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="1b13d-117">Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b13d-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="1b13d-118">Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b13d-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="1b13d-119">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b13d-119">Select **OK**.</span></span> <span data-ttu-id="1b13d-120">Het proces wordt uitgevoerd met de parameters die u instelt.</span><span class="sxs-lookup"><span data-stu-id="1b13d-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="1b13d-121">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b13d-121">Select **OK**.</span></span>
