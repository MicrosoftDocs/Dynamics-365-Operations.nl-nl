---
title: Een werknemer inschrijven voor een variabele honoreringsregeling
description: De manager Compensatie en emolumenten kan werknemers inschrijven op plannen voor variabele compensatie inschrijven om contante en niet-contante toekenningen voor werknemers te berekenen.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a173403e79212be5e4aac36d99f349da159e08
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112086"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="0c1d5-103">Een werknemer inschrijven voor een variabele honoreringsregeling</span><span class="sxs-lookup"><span data-stu-id="0c1d5-103">Enroll an employee in a variable compensation plan</span></span>

<span data-ttu-id="0c1d5-104">De manager Compensatie en emolumenten kan werknemers inschrijven op plannen voor variabele compensatie inschrijven om contante en niet-contante toekenningen voor werknemers te berekenen.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="0c1d5-105">Bij deze procedure wordt aangenomen dat een plan voor variabele compensatie is gemaakt met het veld Inschrijving inschakelen ingesteld op Ja en dat beschikbaarheidregels zijn gemaakt voor dit plan voor variabele compensatie.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="0c1d5-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0c1d5-107">U kunt beginnen met deze procedure door naar Human resources > Medewerkers > Werknemers > Compensatie > Inschrijving op variabel plan te gaan</span><span class="sxs-lookup"><span data-stu-id="0c1d5-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="0c1d5-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-108">Click New.</span></span>
2. <span data-ttu-id="0c1d5-109">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0c1d5-110">De zoekopdracht voor het plannen wordt gefilterd zodat alleen de plannen voor variabele compensatie worden weergegeven waarvoor de werknemer in aanmerking komt op basis van de beschikbaarheidregels.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="0c1d5-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0c1d5-112">Schakel de uitbreiding van de sectie Algemeen om.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="0c1d5-113">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="0c1d5-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-114">Click Save.</span></span>
7. <span data-ttu-id="0c1d5-115">Schakel de uitbreiding van de sectie Overschrijvingen om.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="0c1d5-116">Desgewenst, kan een datum aanstellingsregel worden ingesteld om de aanstellingsdatum voor een werknemer te overschrijven wanneer de aanstellingsregel voor het geselecteerde variabele plan Percentage is.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="0c1d5-117">Als het variabele plan een percentage van het basisplan is, kan het toekenningspercentage voor de werknemer worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="0c1d5-118">Als het variabele compensatieplan een plan met een aantal eenheden is, kan het aantal eenheden voor de werknemer worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="0c1d5-119">Als aan de werknemer een vast bedrag voor hun toekenningen moet worden verstrekt, kan het bedrag hier worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="0c1d5-120">Schakel de uitbreiding van de sectie Organisatieoverschrijvingen om.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="0c1d5-121">Als rekening moeten worden gehouden met de prestaties van de werknemer kunnen de prestaties van verschillende afdelingen of een andere afdeling dan de afdeling die is toegewezen aan de functie van de werknemer worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="0c1d5-122">De kolom Percentage met 100 in totaal zijn.</span><span class="sxs-lookup"><span data-stu-id="0c1d5-122">The Percent column should total 100.</span></span>  

