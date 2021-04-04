---
title: Aan de slag met de serviceadministratie voor de invoegtoepassing voor elektronische facturering
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de invoegtoepassing voor elektronische facturering.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592521"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="0c2de-103">Aan de slag met de serviceadministratie voor de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="0c2de-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="0c2de-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="0c2de-104">Prerequisites</span></span>

<span data-ttu-id="0c2de-105">Voordat u de procedures in dit onderwerp voltooit, moet aan de volgende vereisten zijn voldaan:</span><span class="sxs-lookup"><span data-stu-id="0c2de-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="0c2de-106">U moet toegang hebben tot uw Microsoft Dynamics Lifecycle Services-account (LCS).</span><span class="sxs-lookup"><span data-stu-id="0c2de-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="0c2de-107">U moet een LCS-project hebben dat versie 10.0.17 of hoger van Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management bevat.</span><span class="sxs-lookup"><span data-stu-id="0c2de-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0c2de-108">Daarnaast moeten deze apps worden geïmplementeerd in een van de volgende Azure-geografische gebieden:</span><span class="sxs-lookup"><span data-stu-id="0c2de-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="0c2de-109">VS - oost</span><span class="sxs-lookup"><span data-stu-id="0c2de-109">East US</span></span>
    - <span data-ttu-id="0c2de-110">VS - west</span><span class="sxs-lookup"><span data-stu-id="0c2de-110">West US</span></span>
    - <span data-ttu-id="0c2de-111">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="0c2de-111">North EU</span></span>
    - <span data-ttu-id="0c2de-112">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="0c2de-112">West EU</span></span>

- <span data-ttu-id="0c2de-113">U moet toegang hebben tot uw Dynamics 365 Regulatory Configuration Services-account (RCS).</span><span class="sxs-lookup"><span data-stu-id="0c2de-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="0c2de-114">U moet de functie Globalisatie voor uw RCS-account in Functiebeheer activeren.</span><span class="sxs-lookup"><span data-stu-id="0c2de-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="0c2de-115">Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0c2de-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="0c2de-116">U moet een Key Vault-resource en een opslagaccount in Azure maken.</span><span class="sxs-lookup"><span data-stu-id="0c2de-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="0c2de-117">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0c2de-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="0c2de-118">De invoegtoepassing voor microservices in Lifecycle Services installeren</span><span class="sxs-lookup"><span data-stu-id="0c2de-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="0c2de-119">Meld u aan bij uw LCS-account.</span><span class="sxs-lookup"><span data-stu-id="0c2de-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="0c2de-120">Selecteer de tegel **Beheer van voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="0c2de-121">Selecteer **e-Factureringsservice** in het gedeelte **Openbare voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="0c2de-122">Controleer of de optie **Voorbeeldfunctie ingeschakeld** op **Ja** is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0c2de-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="0c2de-123">Selecteer uw LCS-implementatieproject op uw LCS-dashboard.</span><span class="sxs-lookup"><span data-stu-id="0c2de-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="0c2de-124">Het LCS-project moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0c2de-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="0c2de-125">Selecteer op het tabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="0c2de-126">Selecteer **Services voor elektronische facturering** en voer in het veld **AAD-toepassings-id** **091c98b0-a1c9-4b02-b62c-7753395ccabe** in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="0c2de-127">Dit is een vaste waarde.</span><span class="sxs-lookup"><span data-stu-id="0c2de-127">This is a fixed value.</span></span>
10. <span data-ttu-id="0c2de-128">Voer in het veld **AAD-tenant-id** de tenant-id van uw Azure-abonnementsaccount in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="0c2de-129">Neem de algemene voorwaarden door en schakel vervolgens het selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="0c2de-130">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="0c2de-131">De parameters voor RCS-integratie met de invoegtoepassing voor elektronisch factureren instellen</span><span class="sxs-lookup"><span data-stu-id="0c2de-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="0c2de-132">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="0c2de-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0c2de-133">Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="0c2de-134">Voer op het tabblad **e-Factureringsservice** in het veld **Service-eindpunt URI** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="0c2de-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="0c2de-135">Datacenter Azure-geografie</span><span class="sxs-lookup"><span data-stu-id="0c2de-135">Datacenter Azure geography</span></span> | <span data-ttu-id="0c2de-136">URI van service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="0c2de-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="0c2de-137">VS - oost</span><span class="sxs-lookup"><span data-stu-id="0c2de-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c2de-138">VS - west</span><span class="sxs-lookup"><span data-stu-id="0c2de-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c2de-139">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="0c2de-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c2de-140">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="0c2de-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="0c2de-141">Controleer of het veld **Toepassings-id** is ingesteld op **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="0c2de-142">Dit is een vaste waarde.</span><span class="sxs-lookup"><span data-stu-id="0c2de-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="0c2de-143">Voer in het veld **LCS-omgevings-id** de id van uw LCS-abonnementsaccount in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="0c2de-144">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c2de-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="0c2de-145">Key Vault-geheim maken</span><span class="sxs-lookup"><span data-stu-id="0c2de-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="0c2de-146">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="0c2de-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0c2de-147">Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Invoegtoepassing voor elektronische facturering**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="0c2de-148">Selecteer op de pagina **Omgevingsinstellingen** op het actiedeelvenster de optie **Serviceomgeving** en selecteer **Key Vault-parameters**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="0c2de-149">Selecteer **Nieuw** om een Key Vault-geheim te maken.</span><span class="sxs-lookup"><span data-stu-id="0c2de-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="0c2de-150">Voer in het veld **Naam** de naam in voor het Key Vault-geheim.</span><span class="sxs-lookup"><span data-stu-id="0c2de-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="0c2de-151">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="0c2de-152">Plak in het veld **Key Vault-URI** het geheim van Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0c2de-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="0c2de-153">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="0c2de-154">Een opslagaccountgeheim maken</span><span class="sxs-lookup"><span data-stu-id="0c2de-154">Create Storage account secret</span></span>

1. <span data-ttu-id="0c2de-155">Ga naar **Systeembeheer** > **Instellingen** > **Key Vault-parameters** en selecteer een Key vault-geheim.</span><span class="sxs-lookup"><span data-stu-id="0c2de-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="0c2de-156">Selecteer **Toevoegen** in de sectie **Certificaten**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="0c2de-157">Voer in het veld **Naam** de naam van de opslagrekening en in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0c2de-158">Selecteer in het veld **Type** de optie **Certificaat**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="0c2de-159">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c2de-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="0c2de-160">Een digitaal certificaatgeheim maken</span><span class="sxs-lookup"><span data-stu-id="0c2de-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="0c2de-161">Ga naar **Systeembeheer** > **Instellingen** > **Key Vault-parameters** en selecteer een Key vault-geheim.</span><span class="sxs-lookup"><span data-stu-id="0c2de-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="0c2de-162">Selecteer **Toevoegen** in de sectie **Certificaten**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="0c2de-163">Voer in het veld **Naam** de naam van het digitale certificaatgeheim en in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0c2de-164">Selecteer in het veld **Type** de optie **Certificaat**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="0c2de-165">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c2de-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="0c2de-166">Een omgeving van de invoegtoepassing voor elektronische facturering maken</span><span class="sxs-lookup"><span data-stu-id="0c2de-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="0c2de-167">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="0c2de-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0c2de-168">Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Invoegtoepassing voor elektronische facturering**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="0c2de-169">Een serviceomgeving maken</span><span class="sxs-lookup"><span data-stu-id="0c2de-169">Create a service environment</span></span>

1. <span data-ttu-id="0c2de-170">Selecteer op de pagina **Omgevingsinstellingen** in het actievenster de optie **Serviceomgeving**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="0c2de-171">Selecteer **Nieuw** om een nieuwe serviceomgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="0c2de-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="0c2de-172">Voer in het veld **Naam** de naam in voor de omgeving voor e-facturering.</span><span class="sxs-lookup"><span data-stu-id="0c2de-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="0c2de-173">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0c2de-174">Selecteer in het veld **Opslag SAS-tokengeheim** de naam van het opslagaccountgeheim dat moet worden gebruikt om toegang tot het opslagaccount te verifiëren.</span><span class="sxs-lookup"><span data-stu-id="0c2de-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="0c2de-175">In de sectie **Gebruikers** selecteert u **Toevoegen** om een gebruiker toe te voegen die elektronische facturen via de omgeving mag indienen en ook verbinding mag maken met het opslagaccount.</span><span class="sxs-lookup"><span data-stu-id="0c2de-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="0c2de-176">Voer in het veld **Gebruikers-id** het alias van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="0c2de-177">Voer in het veld **E-mail** het e-mailadres van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="0c2de-178">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-178">Select **Save**.</span></span>
8. <span data-ttu-id="0c2de-179">Als uw land-/regiospecifieke facturen een keten certificaten vereisen om digitale handtekeningen toe te passen, selecteert u in het actiedeelvenster de optie **Key Vault-parameters** en vervolgens **Keten van certificaten** en voert u deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="0c2de-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="0c2de-180">Selecteer **Nieuw** om een keten certificaten te maken.</span><span class="sxs-lookup"><span data-stu-id="0c2de-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="0c2de-181">Voer in het veld **Naam** de naam in voor de certificaatketen.</span><span class="sxs-lookup"><span data-stu-id="0c2de-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="0c2de-182">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="0c2de-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="0c2de-183">Selecteer in het gedeelte **Certificaten** de oiptie **Toevoegen** om een certificaat aan de keten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="0c2de-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="0c2de-184">Met de knop **Omhoog** of **Omlaag** kunt u de positie van het certificaat in de keten wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0c2de-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="0c2de-185">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c2de-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="0c2de-186">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c2de-186">Close the page.</span></span>
9. <span data-ttu-id="0c2de-187">Selecteer op de pagina **Serviceomgeving** in het actiedeelvenster de optie **Publiceren** om de omgeving naar de cloud te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0c2de-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="0c2de-188">De waarde van het veld **Status** wordt gewijzigd in **Gepubliceerd**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="0c2de-189">Een verbonden toepassing maken</span><span class="sxs-lookup"><span data-stu-id="0c2de-189">Create a connected application</span></span>

1. <span data-ttu-id="0c2de-190">Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Verbonden toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="0c2de-191">Selecteer **Nieuw** om een verbonden toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="0c2de-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="0c2de-192">Voer in het veld **Naam** de naam in voor de toepassing die moet worden verbonden.</span><span class="sxs-lookup"><span data-stu-id="0c2de-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="0c2de-193">Voer in het veld **Toepassing** de URL in van de Finance and Supply Chain Management-omgeving die u wilt verbinden.</span><span class="sxs-lookup"><span data-stu-id="0c2de-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="0c2de-194">Voer in het veld **Tenant** de tenant in van de Finance and Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="0c2de-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="0c2de-195">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-195">Select **Save**.</span></span>
6. <span data-ttu-id="0c2de-196">Selecteer in het actievenster de optie **Verbinding controleren** om de verbinding met de omgeving te testen.</span><span class="sxs-lookup"><span data-stu-id="0c2de-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="0c2de-197">Sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="0c2de-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="0c2de-198">Verbonden toepassingen aan omgevingen koppelen</span><span class="sxs-lookup"><span data-stu-id="0c2de-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="0c2de-199">Selecteer op de pagina **Omgevingsinstellingen** de optie **Nieuw** om een verbonden toepassing toe te wijzen aan een omgeving.</span><span class="sxs-lookup"><span data-stu-id="0c2de-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="0c2de-200">Selecteer in het veld **Verbonden toepassing** een verbonden toepassing.</span><span class="sxs-lookup"><span data-stu-id="0c2de-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="0c2de-201">Selecteer in het veld **Serviceomgeving** een serviceomgeving.</span><span class="sxs-lookup"><span data-stu-id="0c2de-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="0c2de-202">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c2de-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="0c2de-203">De integratie van de invoegtoepassing voor elektronisch factureren instellen in Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0c2de-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="0c2de-204">De integratie van de invoegtoepassing voor elektronisch factureren inschakelen</span><span class="sxs-lookup"><span data-stu-id="0c2de-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="0c2de-205">Meld u aan bij uw Finance of Supply Chain Management-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="0c2de-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="0c2de-206">Zoek in de werkruimte **Functiebeheer** naar de functie **Integratie invoegtoepassing voor elektronisch factureren**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="0c2de-207">Als deze functie niet op de pagina wordt weergegeven, selecteert u **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="0c2de-208">Selecteer de functie en selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="0c2de-209">De URL van het service-eindpunt instellen</span><span class="sxs-lookup"><span data-stu-id="0c2de-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="0c2de-210">Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="0c2de-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="0c2de-211">Voer op het tabblad **Indieningsservice** in het veld **Service-eindpunt URL** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="0c2de-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="0c2de-212">Datacenter Azure-geografie</span><span class="sxs-lookup"><span data-stu-id="0c2de-212">Datacenter Azure geography</span></span> | <span data-ttu-id="0c2de-213">URL van service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="0c2de-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="0c2de-214">VS - oost</span><span class="sxs-lookup"><span data-stu-id="0c2de-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c2de-215">VS - west</span><span class="sxs-lookup"><span data-stu-id="0c2de-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c2de-216">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="0c2de-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c2de-217">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="0c2de-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="0c2de-218">Voer in het veld **Omgeving** de naam in voor de omgeving voor de invoegtoepassing voor e-facturering.</span><span class="sxs-lookup"><span data-stu-id="0c2de-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="0c2de-219">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c2de-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
