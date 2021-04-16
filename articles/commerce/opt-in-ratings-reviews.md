---
title: Aanmelden om beoordelingen en recensies te gebruiken
description: In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9e3f2a17e182c0e3efc8b90380eff74f350c3278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804644"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9dc32-103">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="9dc32-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9dc32-104">In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="9dc32-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="9dc32-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="9dc32-105">Overview</span></span>

<span data-ttu-id="9dc32-106">De oplossing voor beoordelingen en recensies is een oplossing voor meerdere kanalen die u beschikbaar kunt maken in Dynamics 365 Commerce met behulp van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9dc32-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9dc32-107">LCS is een beheerportal die door detailhandelaren wordt gebruikt voor het beheren voor hun omgevingen van inrichten tot het uit bedrijf nemen.</span><span class="sxs-lookup"><span data-stu-id="9dc32-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="9dc32-108">Als u de oplossing voor beoordelingen en recensies op uw Commerce-website wilt gebruiken, moet u zich aanmelden voor beoordelingen en recensies tijdens de implementatie van uw e-Commercesite op Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9dc32-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9dc32-109">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="9dc32-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="9dc32-110">Voer de volgende stappen uit om u aan te melden voor beoordelingen en recensies op uw site.</span><span class="sxs-lookup"><span data-stu-id="9dc32-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="9dc32-111">Volg de stappen in [Een nieuwe e-commerce-site implementeren](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9dc32-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="9dc32-112">Terwijl u nog bezig bent in LCS, gaat u naar **Implementatie Retail instellen \> Overige instellingen**.</span><span class="sxs-lookup"><span data-stu-id="9dc32-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="9dc32-113">Stel de optie **Service voor beoordelingen en recensies inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9dc32-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="9dc32-114">Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies (beveiligingsgroepsobject-id)** de id in van de Microsoft Azure Active Directory (Azure AD)-beveiligingsgroep die de moderators voor beoordelingen en recensies bevat.</span><span class="sxs-lookup"><span data-stu-id="9dc32-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Aanmelden om beoordelingen en recensies te gebruiken](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="9dc32-116">Voltooi het initialisatieproces voor e-commerce.</span><span class="sxs-lookup"><span data-stu-id="9dc32-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="9dc32-117">Als u een bestaande Dynamics 365 Commerce-klant bent die al een e-Commercesite heeft geïmplementeerd zonder zich bij beoordelingen en recensies te hebben aangemeld en nu beoordelingen en recensies uit het Dynamics 365 Commerce-pakket wil gebruiken, moet u een serviceaanvraag indienen.</span><span class="sxs-lookup"><span data-stu-id="9dc32-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="9dc32-118">Zie [Proces voor het indienen van serviceaanvragen](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json) voor informatie over het indienen van een serviceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="9dc32-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9dc32-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9dc32-119">Additional resources</span></span>

[<span data-ttu-id="9dc32-120">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="9dc32-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="9dc32-121">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="9dc32-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="9dc32-122">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="9dc32-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="9dc32-123">Productbeoordelingen synchroniseren in Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9dc32-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]