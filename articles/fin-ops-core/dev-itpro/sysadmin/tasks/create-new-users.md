---
title: Nieuwe gebruikers maken
description: Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken uit te voeren.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570516"
---
# <a name="create-new-users"></a><span data-ttu-id="529e9-103">Nieuwe gebruikers maken</span><span class="sxs-lookup"><span data-stu-id="529e9-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="529e9-104">Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken te doen.</span><span class="sxs-lookup"><span data-stu-id="529e9-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="529e9-105">Een gebruiker aan een licentie koppelen (alleen nieuwe licentietypen)</span><span class="sxs-lookup"><span data-stu-id="529e9-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="529e9-106">Voor klanten met een van de nieuwe licentietypen die zijn toegevoegd in oktober 2019, moeten gebruikers aan een licentie zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="529e9-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="529e9-107">Gebruikers die aan een licentie zijn gekoppeld, worden automatisch toegevoegd als systeemgebruikers die geen rollen hebben wanneer ze zich voor de eerste keer aanmelden.</span><span class="sxs-lookup"><span data-stu-id="529e9-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="529e9-108">Gebruikers die niet aan een licentie zijn gekoppeld, ontvangen een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="529e9-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="529e9-109">Systeembeheerders [kunnen licenties aan gebruikers toewijzen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in het [Microsoft 365-beheercentrum](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="529e9-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="529e9-110">Een nieuwe gebruiker toevoegen</span><span class="sxs-lookup"><span data-stu-id="529e9-110">Add a new user</span></span>
1. <span data-ttu-id="529e9-111">Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="529e9-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="529e9-112">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="529e9-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="529e9-113">Voer in het veld **Gebruikers-id** een unieke id voor de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="529e9-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="529e9-114">Een gebruikers-id is vereist.</span><span class="sxs-lookup"><span data-stu-id="529e9-114">A user ID is required.</span></span>  
4. <span data-ttu-id="529e9-115">Voer in het veld **Gebruikersnaam** de naam van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="529e9-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="529e9-116">Voer in het veld **Domein** het domein van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="529e9-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="529e9-117">Voer in het veld **Alias** de alias van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="529e9-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="529e9-118">Selecteer het gewenste bedrijf in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="529e9-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="529e9-119">Selecteer op het sneltabblad **Rollen van gebruiker** de optie **Rollen toewijzen** om [gebruikers aan beveiligingsrollen toe te wijzen](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="529e9-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="529e9-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="529e9-120">Select **OK**.</span></span>
10. <span data-ttu-id="529e9-121">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="529e9-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="529e9-122">Gebruikers importeren</span><span class="sxs-lookup"><span data-stu-id="529e9-122">Import users</span></span>
1. <span data-ttu-id="529e9-123">Selecteer **Gebruikers importeren** in het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="529e9-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="529e9-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="529e9-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="529e9-125">Selecteer **Gebruikers importeren**.</span><span class="sxs-lookup"><span data-stu-id="529e9-125">Select **Import users**.</span></span>
4. <span data-ttu-id="529e9-126">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="529e9-126">Select **Close**.</span></span>

