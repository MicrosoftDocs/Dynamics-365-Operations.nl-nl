---
title: Aanmelden om beoordelingen en recensies te gebruiken
description: In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697975"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="95d7c-103">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="95d7c-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="95d7c-104">In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="95d7c-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="95d7c-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="95d7c-105">Overview</span></span>

<span data-ttu-id="95d7c-106">De oplossing voor beoordelingen en recensies is een omnichannel-oplossing die u beschikbaar kunt maken in Dynamics 365 Commerce met behulp van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="95d7c-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="95d7c-107">LCS is een beheerportal die door detailhandelaren wordt gebruikt voor het beheren voor hun omgevingen van inrichten tot het uit bedrijf nemen.</span><span class="sxs-lookup"><span data-stu-id="95d7c-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="95d7c-108">Als u de oplossing voor beoordelingen en recensies op uw commerce-website wilt gebruiken, moet u zich eerst aanmelden.</span><span class="sxs-lookup"><span data-stu-id="95d7c-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="95d7c-109">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="95d7c-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="95d7c-110">Voer de volgende stappen uit om u aan te melden voor beoordelingen en recensies op uw site.</span><span class="sxs-lookup"><span data-stu-id="95d7c-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="95d7c-111">Volg de stappen in [Een nieuwe e-commerce-site implementeren](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="95d7c-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="95d7c-112">Terwijl u nog bezig bent in LCS, gaat u naar **Implementatie Retail instellen \> Overige instellingen**.</span><span class="sxs-lookup"><span data-stu-id="95d7c-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="95d7c-113">Stel de optie **Service voor beoordelingen en recensies inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="95d7c-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="95d7c-114">Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies (beveiligingsgroepsobject-id)** de id in van de Microsoft Azure Active Directory (Azure AD)-beveiligingsgroep die de moderators voor beoordelingen en recensies bevat.</span><span class="sxs-lookup"><span data-stu-id="95d7c-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Aanmelden om beoordelingen en recensies te gebruiken](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="95d7c-116">Voltooi het initialisatieproces voor e-commerce.</span><span class="sxs-lookup"><span data-stu-id="95d7c-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95d7c-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="95d7c-117">Additional resources</span></span>

[<span data-ttu-id="95d7c-118">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="95d7c-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="95d7c-119">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="95d7c-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="95d7c-120">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="95d7c-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="95d7c-121">Productbeoordelingen synchroniseren in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="95d7c-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
