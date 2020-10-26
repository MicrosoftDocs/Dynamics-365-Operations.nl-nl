---
title: Een medewerker configureren met het mobiele taakapparaat
description: In dit onderwerp wordt uitgelegd hoe u de juiste rollen toewijst aan de gebruikersaccount van een medewerker, en de medewerker vervolgens de mogelijk biedt om werkvloerregistraties te doen.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ada42a98a8a87e377f939d063b17f9904f6b3408
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978229"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="a6583-103">Een medewerker configureren met het mobiele taakapparaat</span><span class="sxs-lookup"><span data-stu-id="a6583-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6583-104">In dit onderwerp wordt uitgelegd hoe u de juiste rollen toewijst aan de gebruikersaccount van een medewerker, en de medewerker vervolgens de mogelijk biedt om werkvloerregistraties te doen.</span><span class="sxs-lookup"><span data-stu-id="a6583-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="a6583-105">Controleren of aan een medewerker een bepaalde rol is toegewezen</span><span class="sxs-lookup"><span data-stu-id="a6583-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="a6583-106">Voor dit voorbeeld controleert u of aan gebruiker SHANNON de rol van machineoperator is toegewezen voordat u de medewerkersaccount configureert.</span><span class="sxs-lookup"><span data-stu-id="a6583-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="a6583-107">Ga naar **Navigatievenster > Modules > Systeembeheer > Gebruikers > Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="a6583-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="a6583-108">Zoek naar een gebruiker in het snelfilter.</span><span class="sxs-lookup"><span data-stu-id="a6583-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="a6583-109">Voer voor dit voorbeeld `shannon` in.</span><span class="sxs-lookup"><span data-stu-id="a6583-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="a6583-110">Selecteer de koppeling in de kolom **Gebruikers-id** van het gebruikersaccount dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a6583-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="a6583-111">Selecteer in de structuur **Rollen van gebruiker** de optie **Rollen > Machineoperator**.</span><span class="sxs-lookup"><span data-stu-id="a6583-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="a6583-112">Sluit de pagina's **Gebruikersgegevens** en **Gebruikers** om terug te keren naar de startpagina.</span><span class="sxs-lookup"><span data-stu-id="a6583-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="a6583-113">Medewerkersaccount configureren</span><span class="sxs-lookup"><span data-stu-id="a6583-113">Configure worker account</span></span>
1. <span data-ttu-id="a6583-114">Ga naar **Navigatievenster > Modules > Human Resources > Medewerkers > Medewerkers**.</span><span class="sxs-lookup"><span data-stu-id="a6583-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="a6583-115">Zoek naar een gebruiker in het snelfilter.</span><span class="sxs-lookup"><span data-stu-id="a6583-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="a6583-116">Voer voor dit voorbeeld `shannon` in.</span><span class="sxs-lookup"><span data-stu-id="a6583-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="a6583-117">Selecteer de koppeling in de kolom **Naam** van het gebruikersaccount dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a6583-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="a6583-118">Selecteer het tabblad **Tijdregistratie**.</span><span class="sxs-lookup"><span data-stu-id="a6583-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="a6583-119">Selecteer **Activeren op registratieterminals**.</span><span class="sxs-lookup"><span data-stu-id="a6583-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="a6583-120">Typ of selecteer waarden in de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="a6583-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="a6583-121">**Berekeningsgroep**</span><span class="sxs-lookup"><span data-stu-id="a6583-121">**Calculation group**</span></span>  
    - <span data-ttu-id="a6583-122">**Standaardberekeningsgroep**</span><span class="sxs-lookup"><span data-stu-id="a6583-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="a6583-123">**Goedkeuringsgroep**</span><span class="sxs-lookup"><span data-stu-id="a6583-123">**Approval group**</span></span>  
    - <span data-ttu-id="a6583-124">**Standaardprofiel**</span><span class="sxs-lookup"><span data-stu-id="a6583-124">**Standard profile**</span></span>  
    - <span data-ttu-id="a6583-125">**Profielgroep**</span><span class="sxs-lookup"><span data-stu-id="a6583-125">**Profile group**</span></span>  

7. <span data-ttu-id="a6583-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6583-126">Select **OK**.</span></span>
8. <span data-ttu-id="a6583-127">Selecteer **Bewerken** om een badgenummer voor de nieuwe tijdregistratiemedewerker in te voeren.</span><span class="sxs-lookup"><span data-stu-id="a6583-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="a6583-128">Voer een waarde in het veld **Badge-id** in.</span><span class="sxs-lookup"><span data-stu-id="a6583-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="a6583-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="a6583-129">Select **Save**.</span></span>
10. <span data-ttu-id="a6583-130">Sluit de pagina's **Medewerkersgegevens** en **Medewerkers**.</span><span class="sxs-lookup"><span data-stu-id="a6583-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="a6583-131">Medewerker toewijzen aan apparaatgroep</span><span class="sxs-lookup"><span data-stu-id="a6583-131">Assign worker to device group</span></span>
1. <span data-ttu-id="a6583-132">Ga naar **Productiebeheer > Instellen > Productie-uitvoering > Taakkaart configureren voor apparaten**.</span><span class="sxs-lookup"><span data-stu-id="a6583-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="a6583-133">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a6583-133">Select **Add**.</span></span>
3. <span data-ttu-id="a6583-134">Selecteer de gewenste medewerker in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a6583-134">In the list, select the desired worker.</span></span> <span data-ttu-id="a6583-135">Voor dit voorbeeld selecteert u **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="a6583-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="a6583-136">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6583-136">Select **OK**.</span></span>
5. <span data-ttu-id="a6583-137">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="a6583-137">Select **Edit**.</span></span>
6. <span data-ttu-id="a6583-138">In het veld **Productie-eenheid** kunt u het standaardfilter voor de medewerker instellen.</span><span class="sxs-lookup"><span data-stu-id="a6583-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="a6583-139">Dit zorgt ervoor dat alleen productietaken voor de geselecteerde productie-eenheid worden weergegeven wanneer de medewerker zich bij het apparaat aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="a6583-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="a6583-140">Voer de gewenste waarde in.</span><span class="sxs-lookup"><span data-stu-id="a6583-140">Enter the desired value.</span></span>
7. <span data-ttu-id="a6583-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a6583-141">Close the page.</span></span>

