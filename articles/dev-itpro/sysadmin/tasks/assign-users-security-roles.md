---
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot Microsoft Dynamics 365 for Finance and Operations moeten gebruikers zijn toegewezen aan beveiligingsrollen.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851354"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="d680c-103">Gebruikers aan beveiligingsrollen toewijzen</span><span class="sxs-lookup"><span data-stu-id="d680c-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d680c-104">Voor toegang tot Microsoft Dynamics 365 for Finance and Operations moeten gebruikers zijn toegewezen aan beveiligingsrollen.</span><span class="sxs-lookup"><span data-stu-id="d680c-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="d680c-105">In deze procedure wordt beschreven hoe systeembeheerders gebruikers automatisch aan rollen kunnen toewijzen op basis van bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="d680c-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="d680c-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="d680c-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="d680c-107">Gebruikers automatisch aan rollen toewijzen</span><span class="sxs-lookup"><span data-stu-id="d680c-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="d680c-108">Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="d680c-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="d680c-109">Selecteer Supervisor boekhouding in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d680c-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d680c-110">Selecteer de rol waarvoor u de regel wilt configureren</span><span class="sxs-lookup"><span data-stu-id="d680c-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="d680c-111">Selecteer voor dit voorbeeld Supervisor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="d680c-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="d680c-112">Klik op **Regel toevoegen** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="d680c-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="d680c-113">Zoek en selecteer de gewenste record in de lijst **Selecteer een query**.</span><span class="sxs-lookup"><span data-stu-id="d680c-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="d680c-114">Selecteer de query die u voor deze regel wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d680c-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="d680c-115">Klik in de lijst **Regelnaam lidmaatschap** op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d680c-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d680c-116">Klik op **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d680c-116">Click **Edit query**.</span></span> <span data-ttu-id="d680c-117">Bewerk de query indien nodig.</span><span class="sxs-lookup"><span data-stu-id="d680c-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="d680c-118">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d680c-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="d680c-119">Gebruikers uitsluiten van automatische roltoewijzing</span><span class="sxs-lookup"><span data-stu-id="d680c-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="d680c-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d680c-120">Close the page.</span></span>
2. <span data-ttu-id="d680c-121">Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="d680c-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="d680c-122">Selecteer Supervisor boekhouding in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d680c-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d680c-123">Hier kunt u een rol selecteren.</span><span class="sxs-lookup"><span data-stu-id="d680c-123">Select a role.</span></span> <span data-ttu-id="d680c-124">Selecteer voor dit voorbeeld Supervisor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="d680c-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="d680c-125">Selecteer in het menu **Gebruikers die aan rol zijn toegewezen** de optie **Gebruikers handmatig toewijzen / uitsluiten**.</span><span class="sxs-lookup"><span data-stu-id="d680c-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="d680c-126">Markeer in de geselecteerde rij in de lijst **Gebruikers toewijzen aan of uitsluiten voor rol**.</span><span class="sxs-lookup"><span data-stu-id="d680c-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="d680c-127">Selecteer een gebruiker.</span><span class="sxs-lookup"><span data-stu-id="d680c-127">Select a user.</span></span>  
6. <span data-ttu-id="d680c-128">Selecteer **Uitsluiten voor rol** in het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="d680c-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="d680c-129">Klik op **Uitsluiten voor rol** om de geselecteerde gebruikers voor de rol uit te sluiten.</span><span class="sxs-lookup"><span data-stu-id="d680c-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="d680c-130">Om uitsluitingen te verwijderen, selecteert u de gebruikers voor wie u uitsluitingen wilt verwijderen. Vervolgens klikt u op **Status opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="d680c-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="d680c-131">Wanneer u een uitsluiting verwijdert door de status van de gebruiker opnieuw in te stellen, wordt de rol van de gebruiker automatisch opnieuw toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d680c-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="d680c-132">De gebruiker wordt echter niet onmiddellijk aan de rol toegewezen of van de rol uitgesloten wanneer u de status opnieuw instelt.</span><span class="sxs-lookup"><span data-stu-id="d680c-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="d680c-133">In plaats daarvan wordt de gebruiker de volgende keer dat de regels voor automatische roltoewijzing worden uitgevoerd, aan de rol toegewezen of van de rol verwijderd.</span><span class="sxs-lookup"><span data-stu-id="d680c-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
