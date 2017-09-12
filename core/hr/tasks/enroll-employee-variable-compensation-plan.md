--- 
title: Een werknemer inschrijven voor een variabele honoreringsregeling
description: De manager Compensatie en emolumenten kan werknemers inschrijven op plannen voor variabele compensatie inschrijven om contante en niet-contante toekenningen voor werknemers te berekenen.
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: eb162e22276fc19cf11999380d551b29ba6a6d45
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="22428-103">Een werknemer inschrijven voor een variabele honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="22428-103">Enroll an employee in a variable compensation plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22428-104">De manager Compensatie en emolumenten kan werknemers inschrijven op plannen voor variabele compensatie inschrijven om contante en niet-contante toekenningen voor werknemers te berekenen.</span><span class="sxs-lookup"><span data-stu-id="22428-104">The Compensation and Benefits manager can enrol employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="22428-105">Bij deze procedure wordt aangenomen dat een plan voor variabele compensatie is gemaakt met het veld Inschrijving inschakelen ingesteld op Ja en dat beschikbaarheidregels zijn gemaakt voor dit plan voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="22428-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="22428-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="22428-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="22428-107">U kunt beginnen met deze procedure door naar Human resources > Medewerkers > Werknemers > Compensatie > Inschrijving op variabel plan te gaan</span><span class="sxs-lookup"><span data-stu-id="22428-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="22428-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22428-108">Click New.</span></span>
2. <span data-ttu-id="22428-109">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="22428-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="22428-110">De zoekopdracht voor het plannen wordt gefilterd zodat alleen de plannen voor variabele compensatie worden weergegeven waarvoor de werknemer in aanmerking komt op basis van de beschikbaarheidregels.</span><span class="sxs-lookup"><span data-stu-id="22428-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="22428-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="22428-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="22428-112">Schakel de uitbreiding van de sectie Algemeen om.</span><span class="sxs-lookup"><span data-stu-id="22428-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="22428-113">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="22428-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="22428-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="22428-114">Click Save.</span></span>
7. <span data-ttu-id="22428-115">Schakel de uitbreiding van de sectie Overschrijvingen om.</span><span class="sxs-lookup"><span data-stu-id="22428-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="22428-116">Desgewenst, kan een datum aanstellingsregel worden ingesteld om de aanstellingsdatum voor een werknemer te overschrijven wanneer de aanstellingsregel voor het geselecteerde variabele plan Percentage is.</span><span class="sxs-lookup"><span data-stu-id="22428-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="22428-117">Als het variabele plan een percentage van het basisplan is, kan het toekenningspercentage voor de werknemer worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="22428-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="22428-118">Als het variabele compensatieplan een plan met een aantal eenheden is, kan het aantal eenheden voor de werknemer worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="22428-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="22428-119">Als aan de werknemer een vast bedrag voor hun toekenningen moet worden verstrekt, kan het bedrag hier worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="22428-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="22428-120">Schakel de uitbreiding van de sectie Organisatieoverschrijvingen om.</span><span class="sxs-lookup"><span data-stu-id="22428-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="22428-121">Als rekening moeten worden gehouden met de prestaties van de werknemer kunnen de prestaties van verschillende afdelingen of een andere afdeling dan de afdeling die is toegewezen aan de functie van de werknemer worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="22428-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="22428-122">De kolom Percentage met 100 in totaal zijn.</span><span class="sxs-lookup"><span data-stu-id="22428-122">The Percent column should total 100.</span></span>  


