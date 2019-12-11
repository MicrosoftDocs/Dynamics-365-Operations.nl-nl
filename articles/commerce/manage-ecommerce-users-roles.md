---
title: e-Commerce-gebruikers en -rollen beheren
description: In dit onderwerp wordt uitgelegd hoe u gebruikerstoegang verleent voor de ontwerpomgeving voor uw Microsoft Dynamics 365 Commerce-site.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23977ddc8ef67389d088ca52c1a1bc6a9b2f7fb4
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697676"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="5a45f-103">e-Commerce-gebruikers en -rollen beheren</span><span class="sxs-lookup"><span data-stu-id="5a45f-103">Manage e-Commerce users and roles</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5a45f-104">In dit onderwerp wordt uitgelegd hoe u gebruikerstoegang verleent voor de ontwerpomgeving voor uw Microsoft Dynamics 365 Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="5a45f-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="5a45f-105">De ontwerpomgeving voor websites maakt gebruik van beveiligingsgroepen die u maakt in Microsoft Azure Active Directory (Azure AD) om gebruikerstoegang te beheren en aan gebruikers toestemming te verlenen om specifieke taken uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="5a45f-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="5a45f-106">U wijst eerst een nieuwe of bestaande beveiligingsgroep uit Azure AD toe aan elke rol in de ontwerpomgeving.</span><span class="sxs-lookup"><span data-stu-id="5a45f-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="5a45f-107">Vervolgens kunt u machtigingen verlenen of intrekken voor afzonderlijke gebruikers door deze gebruikers aan een geschikte beveiligingsgroep toe te voegen of ze uit een beveiligingsgroep te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="5a45f-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="5a45f-108">Overzicht van rollen in de ontwerpomgeving</span><span class="sxs-lookup"><span data-stu-id="5a45f-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="5a45f-109">De Dynamics 365 for Commerce-ontwerpomgeving ondersteunt de volgende rollen.</span><span class="sxs-lookup"><span data-stu-id="5a45f-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="5a45f-110">Rol</span><span class="sxs-lookup"><span data-stu-id="5a45f-110">Role</span></span>                 | <span data-ttu-id="5a45f-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5a45f-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="5a45f-112">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="5a45f-112">System Administrator</span></span> | <span data-ttu-id="5a45f-113">Gebruikers die deze rol hebben, hebben alle bevoegdheden voor alle hulpprogramma's en voor alle beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="5a45f-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="5a45f-114">Ze kunnen ook sites maken.</span><span class="sxs-lookup"><span data-stu-id="5a45f-114">They can also create sites.</span></span> |
| <span data-ttu-id="5a45f-115">Beheerder</span><span class="sxs-lookup"><span data-stu-id="5a45f-115">Administrator</span></span>   | <span data-ttu-id="5a45f-116">Gebruikers die deze rol hebben, hebben alle bevoegdheden voor alle hulpprogramma's, en beoordelingen en recensies in een bepaalde sitestructuur.</span><span class="sxs-lookup"><span data-stu-id="5a45f-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="5a45f-117">Webproducer</span><span class="sxs-lookup"><span data-stu-id="5a45f-117">Web Producer</span></span>         | <span data-ttu-id="5a45f-118">Gebruikers die deze rol hebben, kunnen pagina's, fragmenten en sjablonen maken, assets uploaden en beheren, en producten en categorieën uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="5a45f-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="5a45f-119">Lezer</span><span class="sxs-lookup"><span data-stu-id="5a45f-119">Reader</span></span>               | <span data-ttu-id="5a45f-120">Gebruikers met deze rol kunnen pagina's, sjablonen, assets, fragmenten, indelingen en instellingen weergeven, maar kunnen geen wijzigingen aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="5a45f-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="5a45f-121">RnR-moderator</span><span class="sxs-lookup"><span data-stu-id="5a45f-121">RnR Moderator</span></span>        | <span data-ttu-id="5a45f-122">Gebruikers die deze rol hebben, kunnen productbeoordelingen verwerken.</span><span class="sxs-lookup"><span data-stu-id="5a45f-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="5a45f-123">Systeembeheerdersrol</span><span class="sxs-lookup"><span data-stu-id="5a45f-123">System Administrator role</span></span>

<span data-ttu-id="5a45f-124">Wanneer u Dynamics 365 Commerce inricht in de Microsoft Dynamics Lifecycle Services-omgeving (LCS), wordt u gevraagd een beveiligingsgroep voor de rol van **systeembeheerder** op te geven.</span><span class="sxs-lookup"><span data-stu-id="5a45f-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="5a45f-125">Deze rol wordt vervolgens automatisch toegepast op alle sites die u maakt in de omgeving die u configureert.</span><span class="sxs-lookup"><span data-stu-id="5a45f-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="5a45f-126">De beveiligingsgroep voor deze rol kan alleen worden bijgewerkt in LCS.</span><span class="sxs-lookup"><span data-stu-id="5a45f-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="5a45f-127">Op de pagina **Sitebeheer** voor alle sites wordt dit weergegeven als alleen-lezen en alleen ter informatie.</span><span class="sxs-lookup"><span data-stu-id="5a45f-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="5a45f-128">Beheerdersrol</span><span class="sxs-lookup"><span data-stu-id="5a45f-128">Administrator role</span></span>

<span data-ttu-id="5a45f-129">Wanneer u een nieuwe site maakt in Commerce, wordt u gevraagd een beveiligingsgroep voor de rol **Beheerder** op te geven.</span><span class="sxs-lookup"><span data-stu-id="5a45f-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="5a45f-130">Zie de tabel eerder in dit onderwerp voor een overzicht van de machtigingen die door deze rol worden verleend.</span><span class="sxs-lookup"><span data-stu-id="5a45f-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="5a45f-131">Beveiligingsgroepen toevoegen of bijwerken</span><span class="sxs-lookup"><span data-stu-id="5a45f-131">Add or update security groups</span></span>

<span data-ttu-id="5a45f-132">Nadat de site is gemaakt, hebben alleen gebruikers in de beveiligingsgroepen die zijn gekoppeld aan de rollen **Systeembeheerder** en **Beheerder**, toegang tot de ontwerpomgeving voor die site.</span><span class="sxs-lookup"><span data-stu-id="5a45f-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="5a45f-133">Als u gebruikers wilt toewijzen aan de rollen **Webproducer**, **RnR-moderator** en **Lezer**, moet u beveiligingsgroepen toewijzen aan deze rollen.</span><span class="sxs-lookup"><span data-stu-id="5a45f-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="5a45f-134">Voer de volgende stappen uit om een beveiligingsgroep aan een rol toe te voegen of om een beveiligingsgroep bij te werken die momenteel aan een rol is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="5a45f-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="5a45f-135">Ga naar de site die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="5a45f-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="5a45f-136">Open de pagina **Beveiliging** in **Sitebeheer**.</span><span class="sxs-lookup"><span data-stu-id="5a45f-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="5a45f-137">Selecteer de rol die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="5a45f-137">Select the role to modify.</span></span>
1. <span data-ttu-id="5a45f-138">Voeg beveiligingsgroepen aan rollen toe of verwijder beveiligingsgroepen van rollen.</span><span class="sxs-lookup"><span data-stu-id="5a45f-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a45f-139">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5a45f-139">Additional resources</span></span>

[<span data-ttu-id="5a45f-140">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="5a45f-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="5a45f-141">Overwegingen bij SEO (Search Engine Optimization) voor uw site</span><span class="sxs-lookup"><span data-stu-id="5a45f-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="5a45f-142">Beveiligingsbeleid voor inhoud (CSP) beheren</span><span class="sxs-lookup"><span data-stu-id="5a45f-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
