---
title: Een werknemer inschrijven voor een vaste honoreringsregeling
description: De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0eeb52bf39160bd89e2164c0dd0413f2781e7a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805605"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="ae774-103">Een werknemer inschrijven voor een vaste honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="ae774-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ae774-104">De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.</span><span class="sxs-lookup"><span data-stu-id="ae774-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="ae774-105">Bij deze procedure wordt ervan uitgegaan dat een vast plan is gemaakt en actief is, en dat beschikbaarheidregels zijn ingesteld voor het plan.</span><span class="sxs-lookup"><span data-stu-id="ae774-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="ae774-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="ae774-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ae774-107">U kunt beginnen met de procedure door naar Human resources > Werknemers > Werknemers > Compensatie > Vast plan te gaan</span><span class="sxs-lookup"><span data-stu-id="ae774-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="ae774-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ae774-108">Click New.</span></span>
2. <span data-ttu-id="ae774-109">Selecteer in het veld Actie een actie Vaste compensatie van het type Inhuren/opnieuw inhuren om de wijziging in de compensatie van de werknemer te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="ae774-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="ae774-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ae774-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ae774-111">Klik in het veld Positie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ae774-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ae774-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ae774-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ae774-113">Het niveau dat wordt weergegeven is van het Compensatieniveau van de taak op de positie.</span><span class="sxs-lookup"><span data-stu-id="ae774-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="ae774-114">Het niveau moet worden ingesteld op de taak voordat compensatie kan worden toegewezen aan de werknemer.</span><span class="sxs-lookup"><span data-stu-id="ae774-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="ae774-115">Selecteer in het veld Plannen het vastecompensatieplan voor de werknemer.</span><span class="sxs-lookup"><span data-stu-id="ae774-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="ae774-116">De zoekopdracht voor het plannen wordt gefilterd om alleen de plannen weer te geven waarvoor de werknemer in aanmerking komt op basis van de beschikbaarheidregels.</span><span class="sxs-lookup"><span data-stu-id="ae774-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="ae774-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ae774-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ae774-118">De ingangsdatum en vervaldatum voor de compensatie wordt standaard ingesteld op de begin- en einddatum voor de positietoewijzing van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="ae774-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="ae774-119">U kunt deze datums indien nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="ae774-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="ae774-120">Als het Vastecompensatieplan een stappenplan is, selecteert u de stap die het juiste salaristarief voor de werknemer bevat.</span><span class="sxs-lookup"><span data-stu-id="ae774-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="ae774-121">Als het vastecompensatieplan een schaal- of bandplan is, voert u het salaristarief voor de werknemer in.</span><span class="sxs-lookup"><span data-stu-id="ae774-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="ae774-122">Het salaristarief wordt gevalideerd op basis van de tolerantie-instellingen voor het plan en de minimale en maximale referentiepunten voor het compensatieniveau van de taak.</span><span class="sxs-lookup"><span data-stu-id="ae774-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="ae774-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ae774-123">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]