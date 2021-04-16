---
title: Microsoft Teams inrichten vanuit Dynamics 365 Commerce
description: In dit onderwerp wordt beschreven hoe u Microsoft Teams inricht met behulp van organisatiegegevens vanuit Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842645"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="f4b47-103">Microsoft Teams inrichten vanuit Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f4b47-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f4b47-104">In dit onderwerp wordt beschreven hoe u Microsoft Teams inricht met behulp van organisatiegegevens vanuit Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f4b47-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f4b47-105">Dynamics 365 Commerce biedt een eenvoudige manier om Teams in te richten als u nog geen teams hebt ingesteld voor uw winkels daar.</span><span class="sxs-lookup"><span data-stu-id="f4b47-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="f4b47-106">Door gebruik te maken van goed gedefinieerde informatie uit Commerce die u wilt gebruiken in Teams, kunt u uw winkelmedewerkers helpen aan de slag te gaan in Teams.</span><span class="sxs-lookup"><span data-stu-id="f4b47-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="f4b47-107">Deze informatie omvat de organisatiehiërarchie, winkelnamen, werknemergegevens en Azure Active Directory (Azure AD) rekeningen.</span><span class="sxs-lookup"><span data-stu-id="f4b47-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="f4b47-108">Het inrichtingsproces voor Teams telt twee hoofdstappen:</span><span class="sxs-lookup"><span data-stu-id="f4b47-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="f4b47-109">Maak in Teams een team voor elke winkel en voeg winkelmedewerkers toe als leden van het relevante team.</span><span class="sxs-lookup"><span data-stu-id="f4b47-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="f4b47-110">Als een werknemer aan meerdere winkels is gekoppeld, blijkt dit uit het teamlidmaatschap.</span><span class="sxs-lookup"><span data-stu-id="f4b47-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="f4b47-111">Er wordt een communicatieteam met regionale managers als leden gemaakt om te helpen bij het publiceren van taken vanuit Teams.</span><span class="sxs-lookup"><span data-stu-id="f4b47-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="f4b47-112">Upload de organisatiehiërarchie van Commerce naar Teams.</span><span class="sxs-lookup"><span data-stu-id="f4b47-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="f4b47-113">Teams inrichten in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="f4b47-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="f4b47-114">Voltooi deze taken voordat u Microsoft Teams gaat inrichten:</span><span class="sxs-lookup"><span data-stu-id="f4b47-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="f4b47-115">Bevestig dat alle regionale managers tot communicatiemanagers zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f4b47-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="f4b47-116">Bevestig dat de Azure-rekening van elke winkelmanager en -medewerker is gekoppeld aan de werknemersrecord van die manager of medewerker in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f4b47-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="f4b47-117">Voer de volgende stappen uit om Teams in te richten in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f4b47-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f4b47-118">Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Microsoft Teams-integratieconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="f4b47-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="f4b47-119">Selecteer **Teams inrichten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f4b47-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="f4b47-120">Er wordt een batchtaak met de naam **Teams inrichten** gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f4b47-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="f4b47-121">Ga naar **Systeembeheer \> Query's \> Batchtaken** en zoek de meest recente taak met de beschrijving **Teams inrichten**.</span><span class="sxs-lookup"><span data-stu-id="f4b47-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="f4b47-122">Wacht tot deze taak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f4b47-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="f4b47-123">Als geen van uw regiomanagers, winkelmanagers en winkelmedewerkers aan een Teams-licentie is gekoppeld, ontvangt u mogelijk het volgende foutbericht: 'Het ophalen van toepasselijke Sku-categorieën voor de gebruiker is mislukt'.</span><span class="sxs-lookup"><span data-stu-id="f4b47-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="f4b47-124">U kunt dit probleem oplossen door **Teams en leden synchroniseren** te selecteren in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f4b47-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="f4b47-125">Inrichting van Teams valideren in het Teams-beheercentrum</span><span class="sxs-lookup"><span data-stu-id="f4b47-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="f4b47-126">Volg deze stappen om de inrichting van Microsoft Teams in het Microsoft Teams-beheercentrum te valideren.</span><span class="sxs-lookup"><span data-stu-id="f4b47-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="f4b47-127">Ga naar het [Teams-beheercentrum](https://admin.teams.microsoft.com/)en meld u aan als beheerder van uw e-commerce-tenant.</span><span class="sxs-lookup"><span data-stu-id="f4b47-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="f4b47-128">Selecteer in het linkernavigatievenster de optie **Teams** om deze uit te vouwen en selecteer vervolgens **Teams beheren**.</span><span class="sxs-lookup"><span data-stu-id="f4b47-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="f4b47-129">Bevestig dat er één team is gemaakt voor elke winkel van Commerce.</span><span class="sxs-lookup"><span data-stu-id="f4b47-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="f4b47-130">Selecteer een team en bevestig dat winkelmedewerkers als leden zijn toegevoegd aan het team.</span><span class="sxs-lookup"><span data-stu-id="f4b47-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="f4b47-131">Selecteer **Gebruikers** in het linkernavigatievenster en bevestig dat alle winkelwerknemers in alle winkels als gebruikers zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f4b47-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="f4b47-132">In de volgende afbeelding ziet u een voorbeeld van de pagina **Teams beheren** in het Teams-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="f4b47-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Voorbeeld van de pagina Teams beheren in het Teams-beheercentrum](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="f4b47-134">Een Commerce-organisatiehiërarchie uploaden naar Teams</span><span class="sxs-lookup"><span data-stu-id="f4b47-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="f4b47-135">De Commerce-organisatiehiërarchie kan worden gebruikt in Microsoft Teams om taken te publiceren naar alle of geselecteerde winkels met dezelfde hiërarchiestructuur.</span><span class="sxs-lookup"><span data-stu-id="f4b47-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="f4b47-136">Volg deze stappen om een Commerce-organisatiehiërarchie te uploaden naar Teams.</span><span class="sxs-lookup"><span data-stu-id="f4b47-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="f4b47-137">Ga in Commerce Headquarters naar **Retail en commerce \> Afzetkanaalinstellingen \> Configuratie van Microsoft Teams-integratie**.</span><span class="sxs-lookup"><span data-stu-id="f4b47-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="f4b47-138">Selecteer **Doelgroephiërarchie downloaden** en selecteer vervolgens **Detailhandelwinkels per regio** om een CSV-bestand (Comma Separated Values) van de organisatiehiërarchie te downloaden.</span><span class="sxs-lookup"><span data-stu-id="f4b47-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="f4b47-139">Installeer de Microsoft Teams PowerShell-module door de stappen in [Microsoft Teams PowerShell installeren](https://docs.microsoft.com/microsoftteams/teams-powershell-install) te volgen.</span><span class="sxs-lookup"><span data-stu-id="f4b47-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="f4b47-140">Wanneer u wordt gevraagd in het Teams PowerShell-venster, meldt u zich aan met het beheerdersaccount voor uw Azure AD-tenant.</span><span class="sxs-lookup"><span data-stu-id="f4b47-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="f4b47-141">Volg de stappen in [De doelgroephiërarchie voor uw team instellen](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) om het CSV-bestand voor de doelgroephiërarchie te uploaden.</span><span class="sxs-lookup"><span data-stu-id="f4b47-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="f4b47-142">Controleren of de organisatiehiërarchie naar Teams is geüpload</span><span class="sxs-lookup"><span data-stu-id="f4b47-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="f4b47-143">Volg deze stappen om te controleren of de organisatiehiërarchie is geüpload naar Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f4b47-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="f4b47-144">Meld u als communicatiemanager aan bij Teams.</span><span class="sxs-lookup"><span data-stu-id="f4b47-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="f4b47-145">Selecteer **Taken per planner** in het linkernavigatievenster.</span><span class="sxs-lookup"><span data-stu-id="f4b47-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="f4b47-146">Maak op het tabblad **Gepubliceerde lijsten** een nieuwe lijst met een dummy taak.</span><span class="sxs-lookup"><span data-stu-id="f4b47-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="f4b47-147">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="f4b47-147">Select **Publish**.</span></span> <span data-ttu-id="f4b47-148">De organisatiehiërarchie moet worden weergegeven in het dialoogvenster **Selecteren wie moet worden gepubliceerd**, zoals in het voorbeeld in de volgende afbeelding is weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4b47-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Voorbeeld van een organisatiehiërarchie in het dialoogvenster Selecteren wie moet worden gepubliceerd](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="f4b47-150">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="f4b47-150">Additional resources</span></span>

[<span data-ttu-id="f4b47-151">Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f4b47-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="f4b47-152">Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen</span><span class="sxs-lookup"><span data-stu-id="f4b47-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="f4b47-153">Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="f4b47-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="f4b47-154">Gebruikersrollen beheren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f4b47-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="f4b47-155">Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn</span><span class="sxs-lookup"><span data-stu-id="f4b47-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="f4b47-156">Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f4b47-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
