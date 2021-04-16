---
title: Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen
description: In dit onderwerp wordt beschreven hoe u integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams inschakelt.
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
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842640"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="be108-103">Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen</span><span class="sxs-lookup"><span data-stu-id="be108-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="be108-104">In dit onderwerp wordt beschreven hoe u integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams inschakelt.</span><span class="sxs-lookup"><span data-stu-id="be108-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="be108-105">Als u Teams wilt voorzien van informatie uit Dynamics 365 Commerce en de functies voor taakbeheer tussen Teams en de POS-toepassing (verkooppunt) wilt synchroniseren, moet u de integratiefuncties in Commerce Headquarters inschakelen.</span><span class="sxs-lookup"><span data-stu-id="be108-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="be108-106">Wanneer u Teams-integratie inschakelt, stemt u ermee in uw gegevens met Teams te delen.</span><span class="sxs-lookup"><span data-stu-id="be108-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="be108-107">Gegevens die met Teams worden gedeeld, bevinden zich mogelijk in een ander land dan uw Commerce-gegevens en zijn mogelijk onderworpen aan andere nalevingsnormen.</span><span class="sxs-lookup"><span data-stu-id="be108-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="be108-108">Zie het [Microsoft Vertrouwenscentrum](https://www.microsoft.com/trust-center) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="be108-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="be108-109">Zie de [privacyverklaring van Microsoft](https://aka.ms/privacy) voor informatie over het privacybeleid van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="be108-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="be108-110">Teams-integratie inschakelen</span><span class="sxs-lookup"><span data-stu-id="be108-110">Enable Teams integration</span></span>

<span data-ttu-id="be108-111">Voordat u Microsoft Teams-integratie met Commerce inschakelt, moet u de Teams-toepassing registreren bij uw tenant in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="be108-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="be108-112">Volg deze stappen om de Teams-toepassing te registreren bij uw tenant in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="be108-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="be108-113">Volg de stappen in [Snelstart: Een app registreren op het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) om de Teams-toepassing te registreren bij uw tenant in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="be108-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="be108-114">Kopieer de waarde van **Id van toepassing (client)** vanaf de pagina **Overzicht** voor de geregistreerde app.</span><span class="sxs-lookup"><span data-stu-id="be108-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="be108-115">U gebruikt deze waarde om Teams-integratie mogelijk te maken in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="be108-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="be108-116">Kopieer de certificaatwaarde die werd ingevoerd bij het [toevoegen van een certificaat](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in stap 1.</span><span class="sxs-lookup"><span data-stu-id="be108-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="be108-117">Het certificaat wordt ook wel de openbare sleutel of toepassingssleutel genoemd.</span><span class="sxs-lookup"><span data-stu-id="be108-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="be108-118">U gebruikt deze waarde om Teams-integratie mogelijk te maken in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="be108-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="be108-119">Voer de volgende stappen uit om Teams-integratie in te schakelen in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="be108-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="be108-120">Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Microsoft Teams-integratieconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="be108-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="be108-121">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="be108-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="be108-122">Stel de optie **Microsoft Teams-integratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="be108-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="be108-123">Voer in de velden **Toepassings-id** en **Toepassingssleutel** de waarden in die u hebt verkregen toen u de Teams-toepassing registreerde in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="be108-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="be108-124">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="be108-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="be108-125">In de volgende afbeelding ziet u een voorbeeld van de configuratie van Teams-integratie in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="be108-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Configuratie van Teams-integratie in Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="be108-127">Teams-integratie uitschakelen</span><span class="sxs-lookup"><span data-stu-id="be108-127">Disable Teams integration</span></span>

<span data-ttu-id="be108-128">Voer de volgende stappen uit om Microsoft Teams-integratie uit te schakelen in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="be108-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="be108-129">Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Microsoft Teams-integratieconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="be108-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="be108-130">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="be108-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="be108-131">Stel de optie **Microsoft Teams-integratie inschakelen** in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="be108-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="be108-132">Wis de waarden uit de velden **Toepassings-id** en **Toepassingssleutel**.</span><span class="sxs-lookup"><span data-stu-id="be108-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="be108-133">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="be108-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="be108-134">Nadat u Teams-integratie met Commerce hebt uitgeschakeld, worden in POS-terminals geen taken meer weergegeven die zijn gepubliceerd vanuit de Teams-toepassing.</span><span class="sxs-lookup"><span data-stu-id="be108-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be108-135">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="be108-135">Additional resources</span></span>

[<span data-ttu-id="be108-136">Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="be108-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="be108-137">Microsoft Teams inrichten vanuit Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="be108-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="be108-138">Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="be108-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="be108-139">Gebruikersrollen beheren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="be108-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="be108-140">Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn</span><span class="sxs-lookup"><span data-stu-id="be108-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="be108-141">Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="be108-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
