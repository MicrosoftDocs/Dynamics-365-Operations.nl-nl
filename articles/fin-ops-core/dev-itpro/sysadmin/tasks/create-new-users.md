---
title: Nieuwe gebruikers maken
description: Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken uit te voeren.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
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
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180939"
---
# <a name="create-new-users"></a><span data-ttu-id="0e7fb-103">Nieuwe gebruikers maken</span><span class="sxs-lookup"><span data-stu-id="0e7fb-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0e7fb-104">Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken te doen.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="0e7fb-105">Een gebruiker aan een licentie koppelen (alleen nieuwe licentietypen)</span><span class="sxs-lookup"><span data-stu-id="0e7fb-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="0e7fb-106">Voor klanten met een van de nieuwe licentietypen die zijn toegevoegd in oktober 2019, moeten gebruikers aan een licentie zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="0e7fb-107">Gebruikers die aan een licentie zijn gekoppeld, worden automatisch toegevoegd als systeemgebruikers die geen rollen hebben wanneer ze zich voor de eerste keer aanmelden.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="0e7fb-108">Gebruikers die niet aan een licentie zijn gekoppeld, ontvangen een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="0e7fb-109">Systeembeheerders [kunnen licenties aan gebruikers toewijzen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in het [Microsoft 365-beheercentrum](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="0e7fb-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="0e7fb-110">Een nieuwe gebruiker toevoegen</span><span class="sxs-lookup"><span data-stu-id="0e7fb-110">Add a new user</span></span>
1. <span data-ttu-id="0e7fb-111">Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="0e7fb-112">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="0e7fb-113">Voer in het veld **Gebruikers-id** een unieke id voor de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="0e7fb-114">Een gebruikers-id is vereist.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-114">A user ID is required.</span></span>  
4. <span data-ttu-id="0e7fb-115">Voer in het veld **Gebruikersnaam** de naam van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="0e7fb-116">Voer in het veld **Domein** het domein van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="0e7fb-117">Voer in het veld **Alias** de alias van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="0e7fb-118">Selecteer het gewenste bedrijf in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="0e7fb-119">Selecteer op het sneltabblad **Rollen van gebruiker** de optie **Rollen toewijzen** om [gebruikers aan beveiligingsrollen toe te wijzen](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0e7fb-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="0e7fb-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-120">Select **OK**.</span></span>
10. <span data-ttu-id="0e7fb-121">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="0e7fb-122">Gebruikers importeren</span><span class="sxs-lookup"><span data-stu-id="0e7fb-122">Import users</span></span>
1. <span data-ttu-id="0e7fb-123">Selecteer **Gebruikers importeren** in het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="0e7fb-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0e7fb-125">Selecteer **Gebruikers importeren**.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-125">Select **Import users**.</span></span>
4. <span data-ttu-id="0e7fb-126">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-126">Select **Close**.</span></span>

