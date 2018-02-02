--- 
title: Een werknemer inschrijven voor een vaste honoreringsregeling
description: De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: 581224623f3f2bb7c6ebd082f1301474549c3289
ms.contentlocale: nl-nl
ms.lasthandoff: 02/02/2018

---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="23838-103">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="23838-103">Enroll an employee in a fixed compensation plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23838-104">De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.</span><span class="sxs-lookup"><span data-stu-id="23838-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="23838-105">Bij deze procedure wordt ervan uitgegaan dat een vast plan is gemaakt en actief is, en dat beschikbaarheidregels zijn ingesteld voor het plan.</span><span class="sxs-lookup"><span data-stu-id="23838-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="23838-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="23838-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="23838-107">U kunt beginnen met de procedure door naar Human resources > Werknemers > Werknemers > Compensatie > Vast plan te gaan</span><span class="sxs-lookup"><span data-stu-id="23838-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="23838-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="23838-108">Click New.</span></span>
2. <span data-ttu-id="23838-109">Selecteer in het veld Actie een actie Vaste compensatie van het type Inhuren/opnieuw inhuren om de wijziging in de compensatie van de werknemer te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="23838-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="23838-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="23838-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="23838-111">Klik in het veld Positie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="23838-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="23838-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="23838-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23838-113">Het niveau dat wordt weergegeven is van het Compensatieniveau van de taak op de positie.</span><span class="sxs-lookup"><span data-stu-id="23838-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="23838-114">Het niveau moet worden ingesteld op de taak voordat compensatie kan worden toegewezen aan de werknemer.</span><span class="sxs-lookup"><span data-stu-id="23838-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="23838-115">Selecteer in het veld Plannen het vastecompensatieplan voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="23838-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="23838-116">De zoekopdracht voor het plannen wordt gefilterd om alleen de plannen weer te geven waarvoor de werknemer in aanmerking komt op basis van de beschikbaarheidregels.</span><span class="sxs-lookup"><span data-stu-id="23838-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="23838-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="23838-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="23838-118">De ingangsdatum en vervaldatum voor de compensatie wordt standaard ingesteld op de begin- en einddatum voor de positietoewijzing van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="23838-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="23838-119">U kunt deze datums indien nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="23838-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="23838-120">Als het Vastecompensatieplan een stappenplan is, selecteert u de stap die het juiste salaristarief voor de werknemer bevat.</span><span class="sxs-lookup"><span data-stu-id="23838-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="23838-121">Als het vastecompensatieplan een schaal- of bandplan is, voert u het salaristarief voor de werknemer in.</span><span class="sxs-lookup"><span data-stu-id="23838-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="23838-122">Het salaristarief wordt gevalideerd op basis van de tolerantie-instellingen voor het plan en de minimale en maximale referentiepunten voor het compensatieniveau van de taak.</span><span class="sxs-lookup"><span data-stu-id="23838-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="23838-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23838-123">Click OK.</span></span>


