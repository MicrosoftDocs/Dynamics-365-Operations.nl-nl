---
title: Een werknemer inschrijven voor een vaste honoreringsregeling
description: De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ba197ee47d2a2da2372b12291e5625ddc9ba1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190506"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="10768-103">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="10768-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10768-104">De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.</span><span class="sxs-lookup"><span data-stu-id="10768-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="10768-105">Bij deze procedure wordt ervan uitgegaan dat een vast plan is gemaakt en actief is, en dat beschikbaarheidregels zijn ingesteld voor het plan.</span><span class="sxs-lookup"><span data-stu-id="10768-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="10768-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="10768-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="10768-107">U kunt beginnen met de procedure door naar Human resources > Werknemers > Werknemers > Compensatie > Vast plan te gaan</span><span class="sxs-lookup"><span data-stu-id="10768-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="10768-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="10768-108">Click New.</span></span>
2. <span data-ttu-id="10768-109">Selecteer in het veld Actie een actie Vaste compensatie van het type Inhuren/opnieuw inhuren om de wijziging in de compensatie van de werknemer te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="10768-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="10768-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="10768-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="10768-111">Klik in het veld Positie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="10768-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="10768-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="10768-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="10768-113">Het niveau dat wordt weergegeven is van het Compensatieniveau van de taak op de positie.</span><span class="sxs-lookup"><span data-stu-id="10768-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="10768-114">Het niveau moet worden ingesteld op de taak voordat compensatie kan worden toegewezen aan de werknemer.</span><span class="sxs-lookup"><span data-stu-id="10768-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="10768-115">Selecteer in het veld Plannen het vastecompensatieplan voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="10768-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="10768-116">De zoekopdracht voor het plannen wordt gefilterd om alleen de plannen weer te geven waarvoor de werknemer in aanmerking komt op basis van de beschikbaarheidregels.</span><span class="sxs-lookup"><span data-stu-id="10768-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="10768-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="10768-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="10768-118">De ingangsdatum en vervaldatum voor de compensatie wordt standaard ingesteld op de begin- en einddatum voor de positietoewijzing van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="10768-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="10768-119">U kunt deze datums indien nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="10768-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="10768-120">Als het Vastecompensatieplan een stappenplan is, selecteert u de stap die het juiste salaristarief voor de werknemer bevat.</span><span class="sxs-lookup"><span data-stu-id="10768-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="10768-121">Als het vastecompensatieplan een schaal- of bandplan is, voert u het salaristarief voor de werknemer in.</span><span class="sxs-lookup"><span data-stu-id="10768-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="10768-122">Het salaristarief wordt gevalideerd op basis van de tolerantie-instellingen voor het plan en de minimale en maximale referentiepunten voor het compensatieniveau van de taak.</span><span class="sxs-lookup"><span data-stu-id="10768-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="10768-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="10768-123">Click OK.</span></span>
