---
title: Azure-resources instellen voor IoT-intelligentie
description: In dit onderwerp wordt uitgelegd hoe u de Microsoft Azure-resources maakt en configureert die u nodig hebt voor IoT-intelligentie.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 431ad6766f1e7f2035d6d5ed87bed4856e58e098
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597259"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="c072f-103">Azure-resources instellen voor IoT-intelligentie</span><span class="sxs-lookup"><span data-stu-id="c072f-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c072f-104">In dit onderwerp wordt uitgelegd hoe u de Microsoft Azure-resources maakt en configureert die u nodig hebt voor IoT-intelligentie.</span><span class="sxs-lookup"><span data-stu-id="c072f-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="c072f-105">Azure-resources maken</span><span class="sxs-lookup"><span data-stu-id="c072f-105">Create Azure resources</span></span>

<span data-ttu-id="c072f-106">Voer de volgende stappen uit om een IoT-hub, een Redis-cache en een sleutelkluis te maken die toegankelijk zijn voor Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c072f-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="c072f-107">Controleren of de app-id voor de Microsoft Dynamics ERP Microservices first-party app in uw tenant is opgenomen</span><span class="sxs-lookup"><span data-stu-id="c072f-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="c072f-108">Ga als volgt te werk om te controleren of de app-id voor de Microsoft Dynamics ERP Microservices first-party app in uw tenant is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c072f-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="c072f-109">Meld u aan bij de Azure-portal op <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="c072f-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="c072f-110">Ga naar **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="c072f-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="c072f-111">Ga naar **ondernemingstoepassingen**.</span><span class="sxs-lookup"><span data-stu-id="c072f-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="c072f-112">Selecteer in het veld **Toepassingstype** de optie **Microsoft-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="c072f-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="c072f-113">Voer in het zoekveld **Microsoft Dynamics ERP Microservices** in.</span><span class="sxs-lookup"><span data-stu-id="c072f-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="c072f-114">Controleer of **Microsoft Dynamics ERP Microservices** in de lijst staat.</span><span class="sxs-lookup"><span data-stu-id="c072f-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="c072f-115">Andere toepassingen hebben vergelijkbare namen.</span><span class="sxs-lookup"><span data-stu-id="c072f-115">Other applications have similar names.</span></span> <span data-ttu-id="c072f-116">Let er daarom op dat u de juiste toepassing zoekt.</span><span class="sxs-lookup"><span data-stu-id="c072f-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="c072f-117">De app-id is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="c072f-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="c072f-118">Als de toepassing niet in de lijst staat, moet u deze aan uw tenant toevoegen:</span><span class="sxs-lookup"><span data-stu-id="c072f-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="c072f-119">Selecteer in de Azure-portal op de werkbalk de knop om Azure Cloud Shell te openen.</span><span class="sxs-lookup"><span data-stu-id="c072f-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="c072f-120">Voer de opdracht **install-module AzureAD** uit.</span><span class="sxs-lookup"><span data-stu-id="c072f-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="c072f-121">Voer **Y** in om de module te installeren.</span><span class="sxs-lookup"><span data-stu-id="c072f-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="c072f-122">Voer de opdracht **Get-InstalledModule-name "AzureAD"** uit om te controleren of de module is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="c072f-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="c072f-123">Voer de opdracht **Connect-AzureAD-confirm** uit om de verificatie uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="c072f-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="c072f-124">Voer de opdracht **New-AzureADServicePrincipal-AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** uit.</span><span class="sxs-lookup"><span data-stu-id="c072f-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="c072f-125">U kunt nu stap 1 tot en met 6 herhalen om te controleren of de app-id zich in uw tenant bevindt.</span><span class="sxs-lookup"><span data-stu-id="c072f-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="c072f-126">Een sleutelkluisresource maken</span><span class="sxs-lookup"><span data-stu-id="c072f-126">Create a key vault resource</span></span>

<span data-ttu-id="c072f-127">Volg deze stappen om een sleutelkluisresource te maken.</span><span class="sxs-lookup"><span data-stu-id="c072f-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="c072f-128">Maak of zoek een resourcegroep in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="c072f-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="c072f-129">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c072f-129">Select **Add**.</span></span>
3. <span data-ttu-id="c072f-130">Voer op de pagina **Nieuw** in het zoekveld de term **sleutelkluis** in.</span><span class="sxs-lookup"><span data-stu-id="c072f-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="c072f-131">Selecteer vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-131">Then select **Create**.</span></span>
4. <span data-ttu-id="c072f-132">Voer op de pagina **Sleutelkluis maken** in het veld **Naam sleutelkluis** een naam in.</span><span class="sxs-lookup"><span data-stu-id="c072f-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="c072f-133">Controleer de standaardwaarden en selecteer vervolgens **Controleren + maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="c072f-134">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-134">Select **Create**.</span></span>

<span data-ttu-id="c072f-135">De sleutelkluis wordt op de achtergrond gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c072f-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="c072f-136">Een IoT-hub-resource maken</span><span class="sxs-lookup"><span data-stu-id="c072f-136">Create an IoT hub resource</span></span>

<span data-ttu-id="c072f-137">Volg deze stappen om een IoT-hub-resource te maken.</span><span class="sxs-lookup"><span data-stu-id="c072f-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="c072f-138">Maak of zoek een resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="c072f-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="c072f-139">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c072f-139">Select **Add**.</span></span>
3. <span data-ttu-id="c072f-140">Voer op de pagina **Nieuw** in het zoekveld de term **IoT-hub** in.</span><span class="sxs-lookup"><span data-stu-id="c072f-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="c072f-141">Selecteer vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-141">Then select **Create**.</span></span>
4. <span data-ttu-id="c072f-142">Voer vervolgens in het veld **Naam IoT-hub** een naam in.</span><span class="sxs-lookup"><span data-stu-id="c072f-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="c072f-143">Controleer de standaardwaarden en selecteer vervolgens **Controleren + maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="c072f-144">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-144">Select **Create**.</span></span>

<span data-ttu-id="c072f-145">De IoT-hub wordt op de achtergrond gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c072f-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="c072f-146">We raden u aan om slechts één IoT-hub-resource per omgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="c072f-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="c072f-147">Een Redis-cacheresource maken</span><span class="sxs-lookup"><span data-stu-id="c072f-147">Create a Redis cache resource</span></span>

<span data-ttu-id="c072f-148">Volg deze stappen om een Redis-cacheresource te maken.</span><span class="sxs-lookup"><span data-stu-id="c072f-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="c072f-149">Maak of zoek een resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="c072f-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="c072f-150">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c072f-150">Select **Add**.</span></span>
3. <span data-ttu-id="c072f-151">Voer op de pagina **Nieuw** in het zoekveld de term **Azure-cache voor Redis** in.</span><span class="sxs-lookup"><span data-stu-id="c072f-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="c072f-152">Selecteer vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-152">Then select **Create**.</span></span>
4. <span data-ttu-id="c072f-153">Voer in het veld **DNS-naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="c072f-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="c072f-154">Controleer de standaardwaarden en selecteer vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="c072f-155">De Redis-cache wordt op de achtergrond gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c072f-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="c072f-156">We raden u aan om slechts één Redis-cache per omgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="c072f-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="c072f-157">Alle resources zijn nu gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c072f-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="c072f-158">De Azure-resources configureren</span><span class="sxs-lookup"><span data-stu-id="c072f-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="c072f-159">De IoT-hub configureren</span><span class="sxs-lookup"><span data-stu-id="c072f-159">Configure the IoT hub</span></span>

<span data-ttu-id="c072f-160">Volg deze stappen om de IoT-hub te configureren.</span><span class="sxs-lookup"><span data-stu-id="c072f-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="c072f-161">Selecteer de IoT-hub-resource in uw resources.</span><span class="sxs-lookup"><span data-stu-id="c072f-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="c072f-162">Selecteer **Ingebouwde eindpunten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="c072f-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="c072f-163">Plak onder **Consumentengroepen** de volgende consumentengroepen.</span><span class="sxs-lookup"><span data-stu-id="c072f-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="c072f-164">Deze consumentengroepen komen overeen met de kant-en-klare scenario's.</span><span class="sxs-lookup"><span data-stu-id="c072f-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="c072f-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="c072f-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="c072f-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="c072f-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="c072f-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="c072f-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="c072f-168">De sleutelkluis configureren</span><span class="sxs-lookup"><span data-stu-id="c072f-168">Configure the key vault</span></span>

<span data-ttu-id="c072f-169">Ga als volgt te werk om de sleutelkluis te configureren.</span><span class="sxs-lookup"><span data-stu-id="c072f-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="c072f-170">Selecteer de sleutelkluisresource in uw resources.</span><span class="sxs-lookup"><span data-stu-id="c072f-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="c072f-171">Selecteer **Toegangsbeleid** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="c072f-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="c072f-172">Selecteer **Een toegangsbeleid toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c072f-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="c072f-173">Selecteer op de pagina **Toegangsbeleid toevoegen** in het veld **Geheime machtigingen** de optie **Ophalen** en **Lijst**.</span><span class="sxs-lookup"><span data-stu-id="c072f-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="c072f-174">Klik op **Principal selecteren**.</span><span class="sxs-lookup"><span data-stu-id="c072f-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="c072f-175">Zoek in het dialoogvenster **Principal** de optie **Microsoft Dynamics ERP Microservices** en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="c072f-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="c072f-176">Selecteer vervolgens **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="c072f-176">Then select **Select**.</span></span>
7. <span data-ttu-id="c072f-177">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c072f-177">Select **Add**.</span></span>
8. <span data-ttu-id="c072f-178">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c072f-178">Select **Save**.</span></span>

<span data-ttu-id="c072f-179">De app heeft nu toegang tot de geheimen in de sleutelkluis.</span><span class="sxs-lookup"><span data-stu-id="c072f-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="c072f-180">Het geheim voor de IoT-hub-verbindingsreeks opslaan</span><span class="sxs-lookup"><span data-stu-id="c072f-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="c072f-181">Voer de volgende stappen uit om het geheim voor de IoT-hub-verbindingsreeks op te slaan:</span><span class="sxs-lookup"><span data-stu-id="c072f-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="c072f-182">Selecteer de IoT-hub-resource in uw resources.</span><span class="sxs-lookup"><span data-stu-id="c072f-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="c072f-183">Selecteer **Ingebouwde eindpunten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="c072f-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="c072f-184">Kopieer de waarde in het veld **Eindpunt dat compatibel is met Event hub**.</span><span class="sxs-lookup"><span data-stu-id="c072f-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="c072f-185">Ga naar de sleutelkluisresource.</span><span class="sxs-lookup"><span data-stu-id="c072f-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="c072f-186">Selecteer **Geheimen** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="c072f-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="c072f-187">Selecteer **Genereren/Importeren**.</span><span class="sxs-lookup"><span data-stu-id="c072f-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="c072f-188">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="c072f-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="c072f-189">Plak in het veld **Waarde** de eindpuntwaarde die u eerder hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="c072f-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="c072f-190">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="c072f-191">Het geheim voor de Redis-cacheverbindingsreeks opslaan</span><span class="sxs-lookup"><span data-stu-id="c072f-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="c072f-192">Voer de volgende stappen uit om het geheim voor de Redis-cacheverbindingsreeks op te slaan:</span><span class="sxs-lookup"><span data-stu-id="c072f-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="c072f-193">Selecteer de Redis-cacheresource in uw resources.</span><span class="sxs-lookup"><span data-stu-id="c072f-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="c072f-194">Selecteer **Toegangssleutels**.</span><span class="sxs-lookup"><span data-stu-id="c072f-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="c072f-195">Kopieer de waarde in het veld **Primaire verbindingsreeks**.</span><span class="sxs-lookup"><span data-stu-id="c072f-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="c072f-196">Ga naar de sleutelkluisresource.</span><span class="sxs-lookup"><span data-stu-id="c072f-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="c072f-197">Selecteer **Geheimen** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="c072f-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="c072f-198">Selecteer **Genereren/Importeren**.</span><span class="sxs-lookup"><span data-stu-id="c072f-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="c072f-199">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="c072f-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="c072f-200">Plak in het veld **Waarde** de verbindingstekenreeks die u eerder hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="c072f-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="c072f-201">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="c072f-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="c072f-202">Telkens wanneer u een van de verbindingsreeksen bijwerkt, moet u ook de geheime waarden bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c072f-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="c072f-203">U bent nu klaar met het inrichten van de vereiste Azure-resources.</span><span class="sxs-lookup"><span data-stu-id="c072f-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="c072f-204">De volgende stap is het [installeren van de invoegtoepassing IoT-intelligentie in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="c072f-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
