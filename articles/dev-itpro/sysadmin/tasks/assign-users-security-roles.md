--- 
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot Microsoft Dynamics 365 for Finance and Operations, Enterprise edition moeten gebruikers worden toegewezen aan beveiligingsrollen.
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c08c9ee27bef3ec8c51df558766f55d3ea4ac48a
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="32873-103">Gebruikers aan beveiligingsrollen toewijzen</span><span class="sxs-lookup"><span data-stu-id="32873-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32873-104">Voor toegang tot Microsoft Dynamics 365 for Finance and Operations, Enterprise edition moeten gebruikers worden toegewezen aan beveiligingsrollen.</span><span class="sxs-lookup"><span data-stu-id="32873-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="32873-105">In deze procedure wordt beschreven hoe systeembeheerders gebruikers automatisch aan rollen kunnen toewijzen op basis van bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="32873-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="32873-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="32873-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="32873-107">Gebruikers automatisch aan rollen toewijzen</span><span class="sxs-lookup"><span data-stu-id="32873-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="32873-108">Ga naar Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="32873-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="32873-109">Selecteer Supervisor boekhouding in de structuur.</span><span class="sxs-lookup"><span data-stu-id="32873-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="32873-110">Selecteer de rol waarvoor u de regel wilt configureren</span><span class="sxs-lookup"><span data-stu-id="32873-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="32873-111">Selecteer voor dit voorbeeld Supervisor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="32873-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="32873-112">Klik op Regel toevoegen om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="32873-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="32873-113">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="32873-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="32873-114">Selecteer de query die u voor deze regel wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="32873-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="32873-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="32873-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="32873-116">Klik op Query bewerken.</span><span class="sxs-lookup"><span data-stu-id="32873-116">Click Edit query.</span></span>
    * <span data-ttu-id="32873-117">Bewerk de query indien nodig.</span><span class="sxs-lookup"><span data-stu-id="32873-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="32873-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="32873-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="32873-119">Gebruikers uitsluiten van automatische roltoewijzing</span><span class="sxs-lookup"><span data-stu-id="32873-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="32873-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="32873-120">Close the page.</span></span>
2. <span data-ttu-id="32873-121">Ga naar Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="32873-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="32873-122">Selecteer Supervisor boekhouding in de structuur.</span><span class="sxs-lookup"><span data-stu-id="32873-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="32873-123">Hier kunt u een rol selecteren.</span><span class="sxs-lookup"><span data-stu-id="32873-123">Select a role.</span></span> <span data-ttu-id="32873-124">Selecteer voor dit voorbeeld Supervisor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="32873-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="32873-125">Klik op Gebruikers handmatig toewijzen / uitsluiten.</span><span class="sxs-lookup"><span data-stu-id="32873-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="32873-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="32873-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="32873-127">Selecteer een gebruiker.</span><span class="sxs-lookup"><span data-stu-id="32873-127">Select a user.</span></span>  
6. <span data-ttu-id="32873-128">Klik op Uitsluiten van rol.</span><span class="sxs-lookup"><span data-stu-id="32873-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="32873-129">Klik op Uitsluiten van rol om de geselecteerde gebruikers van de rol uit te sluiten.</span><span class="sxs-lookup"><span data-stu-id="32873-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="32873-130">Om uitsluitingen te verwijderen, selecteert u de gebruikers voor wie u uitsluitingen wilt verwijderen. Vervolgens klikt u op Status opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="32873-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="32873-131">Wanneer u een uitsluiting verwijdert door de status van de gebruiker opnieuw in te stellen, wordt de rol van de gebruiker automatisch opnieuw toegewezen.</span><span class="sxs-lookup"><span data-stu-id="32873-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="32873-132">De gebruiker wordt echter niet onmiddellijk aan de rol toegewezen of van de rol uitgesloten wanneer u de status opnieuw instelt.</span><span class="sxs-lookup"><span data-stu-id="32873-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="32873-133">In plaats daarvan wordt de gebruiker de volgende keer dat de regels voor automatische roltoewijzing worden uitgevoerd, aan de rol toegewezen of van de rol verwijderd.</span><span class="sxs-lookup"><span data-stu-id="32873-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


