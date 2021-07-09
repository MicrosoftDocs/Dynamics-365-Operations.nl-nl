---
title: Aan de slag met Algemene voorraadboekhouding (Global Inventory Accounting)
description: In dit onderwerp wordt beschreven hoe u aan de slag gaat met Algemene voorraadboekhouding.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301693"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="7c59c-103">Aan de slag met Algemene voorraadboekhouding (Global Inventory Accounting)</span><span class="sxs-lookup"><span data-stu-id="7c59c-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="7c59c-104">Met Algemene voorraadboekhouding kunt u meerdere voorraadboekingen uitvoeren in de grootboeken voor Algemene voorraadboekhouding die u hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="7c59c-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="7c59c-105">U moet elk grootboek voor Algemene voorraadboekhouding aan een *conventie* koppelen.</span><span class="sxs-lookup"><span data-stu-id="7c59c-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="7c59c-106">Een conventie is een verzameling van de volgende typen boekhoudbeleidsregels:</span><span class="sxs-lookup"><span data-stu-id="7c59c-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="7c59c-107">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7c59c-107">Cost object</span></span>
- <span data-ttu-id="7c59c-108">Basis van invoermeting</span><span class="sxs-lookup"><span data-stu-id="7c59c-108">Input measurement basis</span></span>
- <span data-ttu-id="7c59c-109">Veronderstelling van kostenstroom</span><span class="sxs-lookup"><span data-stu-id="7c59c-109">Cost flow assumption</span></span>
- <span data-ttu-id="7c59c-110">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7c59c-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="7c59c-111">Zelfs nadat u Algemene voorraadboekhouding hebt ingeschakeld, kunt u nog gewoon voorraadboekhouding uitvoeren in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7c59c-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="7c59c-112">Algemene voorraadboekhouding is een invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="7c59c-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="7c59c-113">Om de functies beschikbaar te maken, moet u deze installeren vanuit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7c59c-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7c59c-114">U kunt ervoor kiezen om deze te evalueren in een testomgeving voordat u ze voor productie-omgevingen inschakelt.</span><span class="sxs-lookup"><span data-stu-id="7c59c-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="7c59c-115">Algemene voorraadboekhouding ondersteunt momenteel niet alle kostenbeheerfuncties die in Supply Chain Management zijn ingebouwd.</span><span class="sxs-lookup"><span data-stu-id="7c59c-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="7c59c-116">Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is, voldoet aan uw behoeften.</span><span class="sxs-lookup"><span data-stu-id="7c59c-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="7c59c-117">Procedure voor het ophalen van de preview van Algemene voorraadboekhouding</span><span class="sxs-lookup"><span data-stu-id="7c59c-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c59c-118">Als u Algemene voorraadboekhouding wilt gebruiken, moet u een omgeving met hoge beschikbaarheid voor LCS hebben (niet in een OneBox-omgeving).</span><span class="sxs-lookup"><span data-stu-id="7c59c-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="7c59c-119">Daarnaast moet u Supply Chain Management versie 10.0.19 of hoger uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="7c59c-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="7c59c-120">Als u zich wilt aanmelden voor de preview van Algemene voorraadboekhouding, verzendt u uw LCS-omgevings-id per e-mail naar het [team voor Algemene voorraadboekhouding](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7c59c-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="7c59c-121">Nadat u bent goedgekeurd voor het programma, verzendt het team u een opvolgings-e-mail met de bètasleutel voor Algemene voorraadboekhouding en uw service-eindpunten.</span><span class="sxs-lookup"><span data-stu-id="7c59c-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="7c59c-122">Nadat u de bètasleutel hebt ontvangen, kunt u [de invoegtoepassing installeren](#install).</span><span class="sxs-lookup"><span data-stu-id="7c59c-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="7c59c-123">Licenties</span><span class="sxs-lookup"><span data-stu-id="7c59c-123">Licensing</span></span>

<span data-ttu-id="7c59c-124">Algemene voorraadboekhouding wordt samengevoegd met de standaardfuncties van kostenbeheer die beschikbaar zijn voor Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7c59c-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="7c59c-125">U hoeft geen extra licentie aan te schaffen voor het gebruik van Algemene voorraadboekhouding.</span><span class="sxs-lookup"><span data-stu-id="7c59c-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7c59c-126">Vereisten</span><span class="sxs-lookup"><span data-stu-id="7c59c-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="7c59c-127">Microsoft Power Platform-integratie instellen</span><span class="sxs-lookup"><span data-stu-id="7c59c-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="7c59c-128">Voordat u de functionaliteit van de invoegtoepassing kunt inschakelen, moet u deze als volgt integreren in Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="7c59c-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="7c59c-129">Open de LCS-omgeving waar u de service wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7c59c-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="7c59c-130">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="7c59c-131">Selecteer **Instellingen** in de sectie **Power Platform**-integratie.</span><span class="sxs-lookup"><span data-stu-id="7c59c-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="7c59c-132">Schakel het selectievakje **Power Platformomgeving instellen** in het dialoogvenster in en selecteer **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="7c59c-133">Het instellen duurt doorgaans tussen de 60 en 90 minuten.</span><span class="sxs-lookup"><span data-stu-id="7c59c-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="7c59c-134">Nadat de instelling van de Microsoft Power Platform-omgeving is voltooid, wordt op de pagina de naam van uw omgeving weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7c59c-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="7c59c-135">Verder wordt in de sectie **Power Platform-integratie** de melding 'De instelling van de Power Platform-omgeving is voltooid' weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7c59c-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="7c59c-136">Voor Algemene voorraadboekhouding is geen toepassing voor twee keer wegschrijven vereist.</span><span class="sxs-lookup"><span data-stu-id="7c59c-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="7c59c-137">Zie [Instellen na de implementatie van de omgeving](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7c59c-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="7c59c-138">Dataverse instellen</span><span class="sxs-lookup"><span data-stu-id="7c59c-138">Set up Dataverse</span></span>

<span data-ttu-id="7c59c-139">Voer, voordat u Dataverse instelt, de volgende stappen uit om de serviceprincipes voor Algemene voorraadboekhouding toe te voegen aan uw tenant.</span><span class="sxs-lookup"><span data-stu-id="7c59c-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="7c59c-140">Installeer Azure AD-module voor Windows PowerShell v2, zoals beschreven in [Azure Active Directory PowerShell for Graph installeren](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="7c59c-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="7c59c-141">Voer de volgende PowerShell-opdracht uit.</span><span class="sxs-lookup"><span data-stu-id="7c59c-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="7c59c-142">Maak vervolgens met de volgende stappen toepassingsgebruikers voor Algemene voorraadboekhouding in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7c59c-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="7c59c-143">Open de URL van uw Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="7c59c-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="7c59c-144">Ga naar **Geavanceerde instellingen \> Systeem \> \> Gebruikers** en maak een toepassingsgebruiker.</span><span class="sxs-lookup"><span data-stu-id="7c59c-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="7c59c-145">Gebruik het veld **Weergeven** om de paginaweergave te wijzigen in *Toepassingsgebruikers*.</span><span class="sxs-lookup"><span data-stu-id="7c59c-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="7c59c-146">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-146">Select **New**.</span></span>
1. <span data-ttu-id="7c59c-147">Stel het veld **Toepassings-ID** in op *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="7c59c-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="7c59c-148">Selecteer **Rol toewijzen** en selecteer vervolgens *Systeembeheerder*.</span><span class="sxs-lookup"><span data-stu-id="7c59c-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="7c59c-149">Als er een rol is met de naam *Common Data Service-gebruiker*, selecteert u ook deze rol.</span><span class="sxs-lookup"><span data-stu-id="7c59c-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="7c59c-150">Herhaal de voorgaande stappen, maar stel het veld **Toepassings-id** in op *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="7c59c-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="7c59c-151">Zie [Een toepassingsgebruiker maken](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7c59c-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="7c59c-152">Als de standaardtaal van uw Dataverse-installatie niet Engels is, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="7c59c-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="7c59c-153">Ga naar **Geavanceerde instelling \> Beheer \> Talen**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="7c59c-154">Selecteer *Engels* (*LanguageCode=1033*) en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="7c59c-155">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="7c59c-155">Install the add-in</span></span>

<span data-ttu-id="7c59c-156">Voer deze stappen uit om de invoegtoepassing te installeren zodat u Algemene voorraadboekhouding kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7c59c-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="7c59c-157">[Registreer u](#sign-up) voor de preview van Algemene voorraadboekhouding.</span><span class="sxs-lookup"><span data-stu-id="7c59c-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="7c59c-158">Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="7c59c-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="7c59c-159">Ga naar **Beheer van previewfuncties**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="7c59c-160">Selecteer het plusteken (**+**).</span><span class="sxs-lookup"><span data-stu-id="7c59c-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="7c59c-161">Voer in het veld **Code** uw bètasleutel voor de invoegtoepassing Algemene voorraadboekhouding in.</span><span class="sxs-lookup"><span data-stu-id="7c59c-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="7c59c-162">(U zou uw bètasleutel per e-mail moeten hebben ontvangen toen u zich registreerde.)</span><span class="sxs-lookup"><span data-stu-id="7c59c-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="7c59c-163">Selecteer **Deblokkeren**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="7c59c-164">Open de LCS-omgeving waar u de service wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7c59c-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="7c59c-165">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="7c59c-166">Ga naar **Power Platform-integratie** en selecteer **Instelling**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="7c59c-167">Schakel het selectievakje **Power Platformomgeving instellen** in het dialoogvenster in en selecteer **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="7c59c-168">Het instellen duurt doorgaans tussen de 60 en 90 minuten.</span><span class="sxs-lookup"><span data-stu-id="7c59c-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="7c59c-169">Nadat u de Microsoft Power Platform-omgeving hebt ingesteld, selecteert u op het sneltabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="7c59c-170">Selecteer **Global Inventory Accounting** (Algemene voorraadboekhouding).</span><span class="sxs-lookup"><span data-stu-id="7c59c-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="7c59c-171">Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.</span><span class="sxs-lookup"><span data-stu-id="7c59c-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="7c59c-172">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-172">Select **Install**.</span></span>
1. <span data-ttu-id="7c59c-173">Op het sneltabblad **Invoegtoepassingen voor omgeving** ziet u dat Algemene voorraadboekhouding wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="7c59c-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="7c59c-174">Na enkele minuten verandert de status van *Bezig met installeren* in *Geïnstalleerd*.</span><span class="sxs-lookup"><span data-stu-id="7c59c-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="7c59c-175">(Mogelijk moet u de pagina vernieuwen om deze wijziging te zien.) Op dat moment is Algemene voorraadboekhouding klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="7c59c-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="7c59c-176">De integratie instellen</span><span class="sxs-lookup"><span data-stu-id="7c59c-176">Set up the integration</span></span>

<span data-ttu-id="7c59c-177">Volg deze stappen om de integratie in te stellen tussen Global Inventory Accounting en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7c59c-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="7c59c-178">Meld u aan bij Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7c59c-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="7c59c-179">Ga naar **Systeembeheer \> Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="7c59c-180">Selecteer **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="7c59c-181">Zoek op het tabblad **Alle** naar de functie genaamd *Algemene voorraadboekhouding*.</span><span class="sxs-lookup"><span data-stu-id="7c59c-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="7c59c-182">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="7c59c-183">Ga naar voor **Algemene voorraadboekhouding \> Instellen \> Parameters algemene voorraadboekhouding \> Integratieparameters**.</span><span class="sxs-lookup"><span data-stu-id="7c59c-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="7c59c-184">In de velden **Dataservice-eindpunt** en **Eindpunt voor algemene voorraadboekhouding** voert u de URL's in uit de e-mail die het team van Global Inventory Accounting heeft verzonden toen u zich hebt geregistreerd voor de preview.</span><span class="sxs-lookup"><span data-stu-id="7c59c-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="7c59c-185">Global Inventory Accounting is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="7c59c-185">Global Inventory Accounting is now ready to use.</span></span>
