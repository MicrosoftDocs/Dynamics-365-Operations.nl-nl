--- 
title: Een medewerker configureren met het mobiele taakapparaat
description: Deze procedure toont hoe u de juiste rollen toewijst aan de gebruikersaccount van een medewerker, en de medewerker vervolgens de mogelijk biedt om werkvloerregistraties te doen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="fb247-103">Een medewerker configureren met het mobiele taakapparaat</span><span class="sxs-lookup"><span data-stu-id="fb247-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb247-104">Deze procedure toont hoe u de juiste rollen toewijst aan de gebruikersaccount van een medewerker, en de medewerker vervolgens de mogelijk biedt om werkvloerregistraties te doen.</span><span class="sxs-lookup"><span data-stu-id="fb247-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="fb247-105">Rollen aan gebruikersaccount toewijzen</span><span class="sxs-lookup"><span data-stu-id="fb247-105">Assign roles to user account</span></span>
1. <span data-ttu-id="fb247-106">Ga naar Systeembeheer > Gebruikers > Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="fb247-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="fb247-107">Gebruik het snelfilter om op de naam van een medewerker te filteren waarbij de gebruikersaccount aan de rol van de machineoperator is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="fb247-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="fb247-108">In de voorbeeldgegevens kan de naam Shannon zijn.</span><span class="sxs-lookup"><span data-stu-id="fb247-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="fb247-109">Markeer de gebruikersaccountrecord.</span><span class="sxs-lookup"><span data-stu-id="fb247-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="fb247-110">Klik in de lijst op de koppeling 'Naam' in de geselecteerde rij om de details van het gebruikersaccount weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fb247-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="fb247-111">Selecteer in de structuur 'Rollen\machineoperator'.</span><span class="sxs-lookup"><span data-stu-id="fb247-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="fb247-112">Sluit de detailpagina van het gebruikersaccount.</span><span class="sxs-lookup"><span data-stu-id="fb247-112">Close the user account details page.</span></span>
7. <span data-ttu-id="fb247-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fb247-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="fb247-114">Configureer medewerkersaccount.</span><span class="sxs-lookup"><span data-stu-id="fb247-114">Configure worker account.</span></span>
1. <span data-ttu-id="fb247-115">Ga naar Human resources > Medewerkers > Medewerkers.</span><span class="sxs-lookup"><span data-stu-id="fb247-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="fb247-116">Gebruik het snelfilter om op de naam van een medewerker te filteren waarbij de gebruikersaccount aan de rol van de machineoperator is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="fb247-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="fb247-117">In de voorbeeldgegevens kan de naam Shannon zijn.</span><span class="sxs-lookup"><span data-stu-id="fb247-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="fb247-118">Markeer de gebruikersaccountrecord.</span><span class="sxs-lookup"><span data-stu-id="fb247-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="fb247-119">Klik in de lijst op de koppeling 'Naam' in de geselecteerde rij om de details van het gebruikersaccount weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fb247-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="fb247-120">Klik op het tabblad Aanstelling.</span><span class="sxs-lookup"><span data-stu-id="fb247-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="fb247-121">Vouw het sneltabblad Tijdregistratie uit en klik op Activeren op registratieterminals.</span><span class="sxs-lookup"><span data-stu-id="fb247-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="fb247-122">Klik op Activeren op registratieterminals.</span><span class="sxs-lookup"><span data-stu-id="fb247-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="fb247-123">Typ of selecteer een waarde in het veld Berekeningsgroep.</span><span class="sxs-lookup"><span data-stu-id="fb247-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="fb247-124">Typ of selecteer een waarde in het veld Standaardberekeningsgroep.</span><span class="sxs-lookup"><span data-stu-id="fb247-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="fb247-125">Typ of selecteer een waarde in het veld Goedkeuringsgroep.</span><span class="sxs-lookup"><span data-stu-id="fb247-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="fb247-126">Typ of selecteer een waarde in het veld Standaardprofiel.</span><span class="sxs-lookup"><span data-stu-id="fb247-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="fb247-127">Typ of selecteer een waarde in het veld Profielgroep.</span><span class="sxs-lookup"><span data-stu-id="fb247-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="fb247-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fb247-128">Click OK.</span></span>
14. <span data-ttu-id="fb247-129">Klik op Bewerken om een badgenummer voor de nieuwe tijdregistratiemedewerker in te voeren.</span><span class="sxs-lookup"><span data-stu-id="fb247-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="fb247-130">Typ een waarde in het veld Badge-id.</span><span class="sxs-lookup"><span data-stu-id="fb247-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="fb247-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fb247-131">Click Save.</span></span>
17. <span data-ttu-id="fb247-132">Gebruik de snelkoppeling SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="fb247-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="fb247-133">Sluit de detailpagina van de medewerker.</span><span class="sxs-lookup"><span data-stu-id="fb247-133">Close the worker details page.</span></span>
19. <span data-ttu-id="fb247-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fb247-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="fb247-135">Wijs een medewerker toe aan apparaatgroep.</span><span class="sxs-lookup"><span data-stu-id="fb247-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="fb247-136">Ga naar Productiebeheer > Instellingen > Productie-uitvoering > Taakkaart configureren voor apparaten.</span><span class="sxs-lookup"><span data-stu-id="fb247-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="fb247-137">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fb247-137">Click Add.</span></span>
3. <span data-ttu-id="fb247-138">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fb247-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fb247-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fb247-139">Click OK.</span></span>
5. <span data-ttu-id="fb247-140">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="fb247-140">Click Edit.</span></span>
6. <span data-ttu-id="fb247-141">In het veld Productie-eenheid kunt u het standaardfilter voor de medewerker instellen.</span><span class="sxs-lookup"><span data-stu-id="fb247-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="fb247-142">Dit zorgt ervoor dat alleen productietaken voor de geselecteerde productie-eenheid worden weergegeven wanneer de medewerker zich bij het apparaat aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="fb247-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="fb247-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fb247-143">Close the page.</span></span>


