---
title: Vaardigheden toewijzen
description: U kunt een zoekopdracht voor vaardigheidstoewijzing maken om een gekwalificeerde persoon te zoeken in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076585"
---
# <a name="map-skills"></a><span data-ttu-id="72dfd-103">Vaardigheden toewijzen</span><span class="sxs-lookup"><span data-stu-id="72dfd-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="72dfd-104">U kunt een zoekopdracht voor vaardigheidstoewijzing maken om een gekwalificeerde persoon te zoeken in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="72dfd-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="72dfd-105">Met zoekopdrachten voor vaardigheidstoewijzing worden resultaten geretourneerd op basis van criteria die u invoert door de volgende informatie te doorzoeken:</span><span class="sxs-lookup"><span data-stu-id="72dfd-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="72dfd-106">Vaardigheden</span><span class="sxs-lookup"><span data-stu-id="72dfd-106">Skills</span></span>
- <span data-ttu-id="72dfd-107">Onderwijs</span><span class="sxs-lookup"><span data-stu-id="72dfd-107">Education</span></span>
- <span data-ttu-id="72dfd-108">Getuigschriften</span><span class="sxs-lookup"><span data-stu-id="72dfd-108">Certificates</span></span>
- <span data-ttu-id="72dfd-109">Posities</span><span class="sxs-lookup"><span data-stu-id="72dfd-109">Positions</span></span>
- <span data-ttu-id="72dfd-110">Projectervaring</span><span class="sxs-lookup"><span data-stu-id="72dfd-110">Project experience</span></span>

<span data-ttu-id="72dfd-111">U kunt bijvoorbeeld zoeken naar mensen in uw organisatie die hun bachelor hebben gehaald.</span><span class="sxs-lookup"><span data-stu-id="72dfd-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="72dfd-112">De profielen voor vaardigheidstoewijzing maken het mogelijk huidige werknemers of kandidaten te vinden met kwalificaties die aansluiten op zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="72dfd-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="72dfd-113">Alleen de werknemers, sollicitanten en de contactpersonen die zijn geselecteerd om in zoekopdrachten voor vaardigheidstoewijzing te worden opgenomen, worden in een resultatenlijst voor vaardigheidstoewijzing weergegeven of worden in een vaardigheidsprofiel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="72dfd-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="72dfd-114">Als u een persoon in zoekopdrachten voor vaardigheidstoewijzingen wilt opnemen, stelt u de selectie **Opnemen in vaardigheidstoewijzing** in op **Ja** op de volgende pagina's:</span><span class="sxs-lookup"><span data-stu-id="72dfd-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="72dfd-115">Werknemer</span><span class="sxs-lookup"><span data-stu-id="72dfd-115">Worker</span></span><br>
> - <span data-ttu-id="72dfd-116">Medewerker</span><span class="sxs-lookup"><span data-stu-id="72dfd-116">Employee</span></span><br>
> - <span data-ttu-id="72dfd-117">Sollicitant</span><span class="sxs-lookup"><span data-stu-id="72dfd-117">Applicant</span></span><br>
> - <span data-ttu-id="72dfd-118">Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="72dfd-118">Contacts</span></span><br>

<span data-ttu-id="72dfd-119">Als u een vaardigheidstoewijzing wilt maken, gaat u naar **Werknemersontwikkeling > Koppelingen > Vaardigheidstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="72dfd-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="72dfd-120">Als u een profiel voor vaardigheidstoewijzing wilt maken, gaat u naar **Werknemersontwikkeling > Koppelingen > Profielen voor vaardigheidstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="72dfd-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="72dfd-121">Vaardigheidshiaatanalyse en analyse van het vaardigheidsprofiel</span><span class="sxs-lookup"><span data-stu-id="72dfd-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="72dfd-122">U kunt een vaardigheidsprofielanalyse maken om een lijst met competenties van een persoon weer te geven.</span><span class="sxs-lookup"><span data-stu-id="72dfd-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="72dfd-123">U kunt een vaardigheidshiaatanalyse maken om de vaardigheden van een persoon te vergelijken met de vaardigheden die zijn vereist voor een functie.</span><span class="sxs-lookup"><span data-stu-id="72dfd-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="72dfd-124">Als u een hiaatanalyse wilt maken, gaat u naar **Werknemerontwikkeling > Koppelingen > Vaardigheidshiaatanalyse functie - persoon**.</span><span class="sxs-lookup"><span data-stu-id="72dfd-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="72dfd-125">Als u een vaardigheidsprofielanalyse wilt maken, gaat u naar **Werknemersontwikkeling > Koppelingen > Vaardigheidsprofielanalyse**.</span><span class="sxs-lookup"><span data-stu-id="72dfd-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="72dfd-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="72dfd-126">See also</span></span>

[<span data-ttu-id="72dfd-127">Vaardigheden configureren</span><span class="sxs-lookup"><span data-stu-id="72dfd-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="72dfd-128">Vaardigheden invoeren</span><span class="sxs-lookup"><span data-stu-id="72dfd-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]