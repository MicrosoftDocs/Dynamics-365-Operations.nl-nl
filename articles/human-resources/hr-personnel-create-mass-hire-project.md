---
title: Een project voor massaal aanstellen maken
description: Deze procedure doorloopt het proces van het instellen van een project voor massaal aanstellen.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d553c5762dcb456bd7178858c09129bc154349
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467044"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="a2c7a-103">Een project voor massaal aanstellen maken</span><span class="sxs-lookup"><span data-stu-id="a2c7a-103">Create a mass hire project</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="a2c7a-104">Deze procedure doorloopt het proces van het instellen van een project voor massaal aanstellen.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="a2c7a-105">Een werver kan projecten voor massaal aanstellen gebruiken om gemakkelijk meerdere posities te maken en een aantal werknemers aan te stellen in die functies.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="a2c7a-106">U begint deze procedure door naar Human resources > Werving > Projecten voor massaal aanstellen te gaan.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="a2c7a-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a2c7a-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-108">Click New.</span></span>
2. <span data-ttu-id="a2c7a-109">Typ een waarde in het veld Project voor massaal aanstellen.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="a2c7a-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="a2c7a-111">Voer in het veld Begin project een datum in.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="a2c7a-112">Voer in het veld Einde project een datum in.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="a2c7a-113">Klik op Project openen.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-113">Click Open project.</span></span>
7. <span data-ttu-id="a2c7a-114">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-114">Click Yes.</span></span>
8. <span data-ttu-id="a2c7a-115">Klik op Posities maken.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-115">Click Create positions.</span></span>
9. <span data-ttu-id="a2c7a-116">Voer in het veld Hoeveelheid het aantal posities in dat u wilt maken</span><span class="sxs-lookup"><span data-stu-id="a2c7a-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="a2c7a-117">De begindatum wordt de aanstellingsdatum voor de nieuwe werknemers.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="a2c7a-118">De einddatum is de ontslagdatum voor de nieuwe werknemers.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="a2c7a-119">Geef op of het bij de nieuwe werknemers om werknemers of contractanten gaat.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="a2c7a-120">Klik in het veld Taak op de vervolgkeuzelijstknop om de taak te selecteren waarvoor u de posities wilt maken.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="a2c7a-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="a2c7a-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2c7a-123">De standaard voltijdse equivalentwaarde is afkomstig van de geselecteerde taak.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="a2c7a-124">U kunt deze zo nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="a2c7a-125">Selecteer desgewenst de afdeling voor de nieuwe posities.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="a2c7a-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a2c7a-126">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]