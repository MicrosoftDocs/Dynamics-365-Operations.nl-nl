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
ms.openlocfilehash: 2726dcb3c847c9af2a431358de04a27341b9e66c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464245"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="888ca-103">Wijzigingen van levensgebeurtenissen verwerken</span><span class="sxs-lookup"><span data-stu-id="888ca-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="888ca-104">U kunt wijzigingen in levensgebeurtenissen verwerken in Microsoft Dynamics 365 Human Resources voor twee levensgebeurtenissen:</span><span class="sxs-lookup"><span data-stu-id="888ca-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="888ca-105">Verjaardagswijzigingen</span><span class="sxs-lookup"><span data-stu-id="888ca-105">Birthday changes</span></span>
- <span data-ttu-id="888ca-106">Wijzigingen in de vervaldatum voor het negeren van een geschiktheidsregel</span><span class="sxs-lookup"><span data-stu-id="888ca-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="888ca-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Wijziging in levensgebeurtenis verwerken**.</span><span class="sxs-lookup"><span data-stu-id="888ca-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="888ca-108">Geef in het dialoogvenster **Wijzigingsproces voor levensgebeurtenissen uitvoeren** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="888ca-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="888ca-109">Veld</span><span class="sxs-lookup"><span data-stu-id="888ca-109">Field</span></span> | <span data-ttu-id="888ca-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="888ca-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="888ca-111">Inschrijvingsperiode</span><span class="sxs-lookup"><span data-stu-id="888ca-111">Enrollment period</span></span> | <span data-ttu-id="888ca-112">De inschrijvingsperiode waarvoor de wijzigingen in de levensgebeurtenis moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="888ca-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="888ca-113">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="888ca-113">Legal entity</span></span> | <span data-ttu-id="888ca-114">De rechtspersoon waarvoor de wijzigingen in de levensgebeurtenis moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="888ca-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="888ca-115">Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="888ca-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="888ca-116">Voer gegevens in voor het proces.</span><span class="sxs-lookup"><span data-stu-id="888ca-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="888ca-117">Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="888ca-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="888ca-118">Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="888ca-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="888ca-119">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="888ca-119">Select **OK**.</span></span> <span data-ttu-id="888ca-120">Het proces wordt uitgevoerd met de parameters die u instelt.</span><span class="sxs-lookup"><span data-stu-id="888ca-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="888ca-121">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="888ca-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]