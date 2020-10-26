---
title: Nieuwe gebruikers maken
description: Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken uit te voeren.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e84130ff2b1cf83b7d2b95eefc72175dc57743c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982497"
---
# <a name="create-new-users"></a><span data-ttu-id="dd4e2-103">Nieuwe gebruikers maken</span><span class="sxs-lookup"><span data-stu-id="dd4e2-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd4e2-104">Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken te doen.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="dd4e2-105">Een gebruiker aan een licentie koppelen (alleen nieuwe licentietypen)</span><span class="sxs-lookup"><span data-stu-id="dd4e2-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="dd4e2-106">Voor klanten met een van de nieuwe licentietypen die zijn toegevoegd in oktober 2019, moeten gebruikers aan een licentie zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="dd4e2-107">Gebruikers die aan een licentie zijn gekoppeld, worden automatisch toegevoegd als systeemgebruikers die geen rollen hebben wanneer ze zich voor de eerste keer aanmelden.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="dd4e2-108">Systeembeheerders [kunnen licenties aan gebruikers toewijzen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in het [Microsoft 365-beheercentrum](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="dd4e2-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="dd4e2-109">Een externe gebruiker aan een licentie koppelen (alleen nieuwe licentietypen)</span><span class="sxs-lookup"><span data-stu-id="dd4e2-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="dd4e2-110">Gebruikers buiten de tenant waarin de omgeving is geïmplementeerd, moeten worden weergegeven in de tenant-directory van de host (Azure Active Directory (Azure AD)), zodat hieraan licenties kunnen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="dd4e2-111">Deze externe gebruikers moeten aan de tenant in Azure AD als gast gebruikers worden toegevoegd en vervolgens de vereiste licenties toegewezen krijgen.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="dd4e2-112">Zie [Gebruikers van Azure Active Directory B2B-samenwerking toevoegen in de Azure Portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="dd4e2-113">Een nieuwe gebruiker toevoegen</span><span class="sxs-lookup"><span data-stu-id="dd4e2-113">Add a new user</span></span>
1. <span data-ttu-id="dd4e2-114">Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="dd4e2-115">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="dd4e2-116">Voer in het veld **Gebruikers-id** een unieke id voor de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="dd4e2-117">Een gebruikers-id is vereist.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-117">A user ID is required.</span></span>  
4. <span data-ttu-id="dd4e2-118">Voer in het veld **Gebruikersnaam** de naam van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="dd4e2-119">Voer in het veld **Domein** het domein van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="dd4e2-120">Voer in het veld **Alias** de alias van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="dd4e2-121">Selecteer het gewenste bedrijf in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="dd4e2-122">Selecteer op het sneltabblad **Rollen van gebruiker** de optie **Rollen toewijzen** om gebruikers aan beveiligingsrollen toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="dd4e2-123">Zie [Gebruikers aan beveiligingsrollen toewijzen](assign-users-security-roles.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="dd4e2-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-124">Select **OK**.</span></span>
10. <span data-ttu-id="dd4e2-125">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="dd4e2-126">Gebruikers importeren</span><span class="sxs-lookup"><span data-stu-id="dd4e2-126">Import users</span></span>
1. <span data-ttu-id="dd4e2-127">Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="dd4e2-128">Selecteer **Gebruikers importeren** in het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="dd4e2-129">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dd4e2-130">Selecteer **Gebruikers importeren**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-130">Select **Import users**.</span></span>
5. <span data-ttu-id="dd4e2-131">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-131">Select **Close**.</span></span>

