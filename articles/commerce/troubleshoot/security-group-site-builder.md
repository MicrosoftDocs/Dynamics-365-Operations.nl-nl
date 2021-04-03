---
title: Kan een beveiligingsgroep voor Commerce Site Builder niet configureren tijdens de initiële implementatie
description: Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer de Microsoft Azure Active Directory (Azure AD) beveiligingsgroep voor Commerce Site Builder niet als optie wordt weergegeven wanneer u e-commerce-onderdelen maakt in Microsoft Dynamics Lifecycle Services (LCS) tijdens de initiële implementatie van een nieuwe e-commerce-tenant.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585270"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="dfa2a-103">Kan een beveiligingsgroep voor Commerce Site Builder niet configureren tijdens de initiële implementatie</span><span class="sxs-lookup"><span data-stu-id="dfa2a-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfa2a-104">Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer de Microsoft Azure Active Directory (Azure AD) beveiligingsgroep voor Commerce Site Builder niet als optie wordt weergegeven wanneer u e-commerce-onderdelen maakt in Microsoft Dynamics Lifecycle Services (LCS) tijdens de initiële implementatie van een nieuwe e-commerce-tenant.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="dfa2a-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dfa2a-105">Description</span></span>

<span data-ttu-id="dfa2a-106">Wanneer u de e-commerce-onderdelen maakt als onderdeel van het proces voor de implementatie van een nieuwe e-commerce-tenant die het onderdeel Commerce Site Builder bevat, wordt de Azure AD-beveiligingsgroep niet weergegeven als een optie in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="dfa2a-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="dfa2a-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="dfa2a-108">De e-commercesite inrichten met een gebruiker in de juiste tenant</span><span class="sxs-lookup"><span data-stu-id="dfa2a-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="dfa2a-109">Ga naar de [Azure-portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="dfa2a-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="dfa2a-110">Volg onder de tenant waarvoor het LCS-project voor uw e-commercesite is ingericht de instructies in [Een basisgroep maken en leden toevoegen via Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="dfa2a-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="dfa2a-111">Ga naar [LCS](https://lcs.dynamics.com/) en meld u aan met een account die dezelfde tenant heeft als de Azure AD-beveiligingsgroep die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="dfa2a-112">De account moet toegang hebben om de Azure AD-beveiligingsgroep weer te geven.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="dfa2a-113">Voltooi de instellingsstappen om de e-commercesite te configureren.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="dfa2a-114">Bij de levering van de e-commerce-onderdelen moet de beveiligingsgroep nu als een optie in het dialoogvenster worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="dfa2a-115">Als u ervoor wilt zorgen dat het veld in het dialoogvenster wordt gevuld met de lijst met beveiligingsgroepen, moet u **Enter** selecteren nadat u de naam hebt ingevuld van de Azure AD-beveiligingsgroep die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="dfa2a-116">In de zoekresultaten worden alle Azure AD-beveiligingsgroepen weergegeven die beginnen met de zoektekst en waartoe de gebruiker toegang heeft.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="dfa2a-117">U kunt een kortere zoekterm gebruiken voor bredere zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="dfa2a-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dfa2a-118">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="dfa2a-118">Additional resources</span></span>

[<span data-ttu-id="dfa2a-119">Een basisgroep maken en leden toevoegen met Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="dfa2a-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="dfa2a-120">Een nieuwe e-commercetenant implementeren</span><span class="sxs-lookup"><span data-stu-id="dfa2a-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
