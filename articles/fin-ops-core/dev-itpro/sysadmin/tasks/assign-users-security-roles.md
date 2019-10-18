---
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot Finance and Operations-apps moeten gebruikers worden toegewezen aan beveiligingsrollen.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180962"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="03611-103">Gebruikers aan beveiligingsrollen toewijzen</span><span class="sxs-lookup"><span data-stu-id="03611-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03611-104">Als u andere dan algemene mogelijkheden wilt gebruiken, moeten gebruikers aan beveiligingsrollen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="03611-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="03611-105">In deze procedure wordt beschreven hoe systeembeheerders gebruikers automatisch aan rollen kunnen toewijzen op basis van bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="03611-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="03611-106">Gebruikers automatisch aan rollen toewijzen</span><span class="sxs-lookup"><span data-stu-id="03611-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="03611-107">Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="03611-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="03611-108">Selecteer Supervisor boekhouding in de structuur.</span><span class="sxs-lookup"><span data-stu-id="03611-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="03611-109">Selecteer de rol waarvoor u de regel wilt configureren</span><span class="sxs-lookup"><span data-stu-id="03611-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="03611-110">Selecteer voor dit voorbeeld Supervisor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="03611-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="03611-111">Klik op **Regel toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="03611-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="03611-112">Zoek en selecteer de gewenste record in de lijst **Selecteer een query**.</span><span class="sxs-lookup"><span data-stu-id="03611-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="03611-113">Selecteer de query die u voor deze regel wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="03611-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="03611-114">Klik in de lijst **Regelnaam lidmaatschap** op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="03611-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="03611-115">Klik op **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="03611-115">Click **Edit query**.</span></span> <span data-ttu-id="03611-116">Bewerk de query indien nodig.</span><span class="sxs-lookup"><span data-stu-id="03611-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="03611-117">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="03611-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="03611-118">Gebruikers uitsluiten van automatische roltoewijzing</span><span class="sxs-lookup"><span data-stu-id="03611-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="03611-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="03611-119">Close the page.</span></span>
2. <span data-ttu-id="03611-120">Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="03611-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="03611-121">Selecteer Supervisor boekhouding in de structuur.</span><span class="sxs-lookup"><span data-stu-id="03611-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="03611-122">Hier kunt u een rol selecteren.</span><span class="sxs-lookup"><span data-stu-id="03611-122">Select a role.</span></span> <span data-ttu-id="03611-123">Selecteer voor dit voorbeeld Supervisor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="03611-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="03611-124">Selecteer in het menu **Gebruikers die aan rol zijn toegewezen** de optie **Gebruikers handmatig toewijzen / uitsluiten**.</span><span class="sxs-lookup"><span data-stu-id="03611-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="03611-125">Markeer in de geselecteerde rij in de lijst **Gebruikers toewijzen aan of uitsluiten voor rol**.</span><span class="sxs-lookup"><span data-stu-id="03611-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="03611-126">Selecteer een gebruiker.</span><span class="sxs-lookup"><span data-stu-id="03611-126">Select a user.</span></span>  
6. <span data-ttu-id="03611-127">Selecteer **Uitsluiten voor rol** in het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="03611-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="03611-128">Klik op **Uitsluiten voor rol** om de geselecteerde gebruikers voor de rol uit te sluiten.</span><span class="sxs-lookup"><span data-stu-id="03611-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="03611-129">Om uitsluitingen te verwijderen, selecteert u de gebruikers voor wie u uitsluitingen wilt verwijderen. Vervolgens klikt u op **Status opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="03611-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="03611-130">Wanneer u een uitsluiting verwijdert door de status van de gebruiker opnieuw in te stellen, wordt de rol van de gebruiker automatisch opnieuw toegewezen.</span><span class="sxs-lookup"><span data-stu-id="03611-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="03611-131">De gebruiker wordt echter niet onmiddellijk aan de rol toegewezen of van de rol uitgesloten wanneer u de status opnieuw instelt.</span><span class="sxs-lookup"><span data-stu-id="03611-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="03611-132">In plaats daarvan wordt de gebruiker de volgende keer dat de regels voor automatische roltoewijzing worden uitgevoerd, aan de rol toegewezen of van de rol verwijderd.</span><span class="sxs-lookup"><span data-stu-id="03611-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
