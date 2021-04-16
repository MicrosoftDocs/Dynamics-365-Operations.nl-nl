---
title: Aan de slag met servicebeheer voor Elektronische facturering
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met Elektronische facturering.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840143"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="6e729-103">Aan de slag met servicebeheer voor Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="6e729-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="6e729-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="6e729-104">Prerequisites</span></span>

<span data-ttu-id="6e729-105">Voordat u de procedures in dit onderwerp voltooit, moet aan de volgende vereisten zijn voldaan:</span><span class="sxs-lookup"><span data-stu-id="6e729-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="6e729-106">U moet toegang hebben tot uw Microsoft Dynamics Lifecycle Services-account (LCS).</span><span class="sxs-lookup"><span data-stu-id="6e729-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="6e729-107">U moet een LCS-project hebben dat versie 10.0.17 of hoger van Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management bevat.</span><span class="sxs-lookup"><span data-stu-id="6e729-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6e729-108">Daarnaast moeten deze apps worden geïmplementeerd in een van de volgende Azure-geografische gebieden:</span><span class="sxs-lookup"><span data-stu-id="6e729-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="6e729-109">VS - oost</span><span class="sxs-lookup"><span data-stu-id="6e729-109">East US</span></span>
    - <span data-ttu-id="6e729-110">VS - west</span><span class="sxs-lookup"><span data-stu-id="6e729-110">West US</span></span>
    - <span data-ttu-id="6e729-111">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="6e729-111">North EU</span></span>
    - <span data-ttu-id="6e729-112">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="6e729-112">West EU</span></span>

- <span data-ttu-id="6e729-113">U moet toegang hebben tot uw Dynamics 365 Regulatory Configuration Services-account (RCS).</span><span class="sxs-lookup"><span data-stu-id="6e729-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="6e729-114">U moet de functie Globalisatie voor uw RCS-account in Functiebeheer activeren.</span><span class="sxs-lookup"><span data-stu-id="6e729-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="6e729-115">Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6e729-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="6e729-116">U moet een Key Vault-resource en een opslagaccount in Azure maken.</span><span class="sxs-lookup"><span data-stu-id="6e729-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="6e729-117">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6e729-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="6e729-118">De invoegtoepassing voor microservices in Lifecycle Services installeren</span><span class="sxs-lookup"><span data-stu-id="6e729-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="6e729-119">Meld u aan bij uw LCS-account.</span><span class="sxs-lookup"><span data-stu-id="6e729-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="6e729-120">Selecteer de tegel **Beheer van voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="6e729-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="6e729-121">Selecteer **e-Factureringsservice** in het gedeelte **Openbare voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="6e729-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="6e729-122">Controleer of de optie **Voorbeeldfunctie ingeschakeld** op **Ja** is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6e729-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="6e729-123">Selecteer uw LCS-implementatieproject op uw LCS-dashboard.</span><span class="sxs-lookup"><span data-stu-id="6e729-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="6e729-124">Het LCS-project moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6e729-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="6e729-125">Selecteer op het tabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="6e729-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="6e729-126">Selecteer **Services voor elektronische facturering**.</span><span class="sxs-lookup"><span data-stu-id="6e729-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="6e729-127">Voer in het veld **AAD-toepassings-id** **091c98b0-a1c9-4b02-b62c-7753395ccabe** in.</span><span class="sxs-lookup"><span data-stu-id="6e729-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="6e729-128">Dit is een vaste waarde.</span><span class="sxs-lookup"><span data-stu-id="6e729-128">This is a fixed value.</span></span>
10. <span data-ttu-id="6e729-129">Voer in het veld **AAD-tenant-id** de tenant-id van uw Azure-abonnementsaccount in.</span><span class="sxs-lookup"><span data-stu-id="6e729-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="6e729-130">Neem de algemene voorwaarden door en schakel vervolgens het selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="6e729-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="6e729-131">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="6e729-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="6e729-132">De parameters voor RCS-integratie met Elektronisch facturering instellen</span><span class="sxs-lookup"><span data-stu-id="6e729-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="6e729-133">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="6e729-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="6e729-134">Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="6e729-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="6e729-135">Voer op het tabblad **e-Factureringsservice** in het veld **Service-eindpunt URI** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6e729-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="6e729-136">Datacenter Azure-geografie</span><span class="sxs-lookup"><span data-stu-id="6e729-136">Datacenter Azure geography</span></span> | <span data-ttu-id="6e729-137">URI van service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="6e729-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="6e729-138">VS - oost</span><span class="sxs-lookup"><span data-stu-id="6e729-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="6e729-139">VS - west</span><span class="sxs-lookup"><span data-stu-id="6e729-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="6e729-140">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="6e729-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="6e729-141">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="6e729-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="6e729-142">Controleer of het veld **Toepassings-id** is ingesteld op **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="6e729-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="6e729-143">Dit is een vaste waarde.</span><span class="sxs-lookup"><span data-stu-id="6e729-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="6e729-144">Voer in het veld **LCS-omgevings-id** de id van uw LCS-omgeving in.</span><span class="sxs-lookup"><span data-stu-id="6e729-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="6e729-145">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e729-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="6e729-146">Key Vault-verwijzingen maken</span><span class="sxs-lookup"><span data-stu-id="6e729-146">Create Key Vault references</span></span>

1. <span data-ttu-id="6e729-147">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="6e729-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="6e729-148">Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Elektronische facturering**.</span><span class="sxs-lookup"><span data-stu-id="6e729-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="6e729-149">Selecteer op de pagina **Omgevingsinstellingen** op het actiedeelvenster de optie **Serviceomgeving** en selecteer **Key Vault-parameters**.</span><span class="sxs-lookup"><span data-stu-id="6e729-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="6e729-150">Selecteer **Nieuw** om een Key Vault-verwijzing te maken.</span><span class="sxs-lookup"><span data-stu-id="6e729-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="6e729-151">Voer in het veld **Naam** de naam in voor de Key Vault-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="6e729-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="6e729-152">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="6e729-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="6e729-153">Plak in het veld **Key Vault-URI** het Key Vault-geheim van Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="6e729-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="6e729-154">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6e729-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="6e729-155">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6e729-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="6e729-156">Een opslagaccountgeheim maken</span><span class="sxs-lookup"><span data-stu-id="6e729-156">Create Storage account secret</span></span>

1. <span data-ttu-id="6e729-157">Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Serviceomgeving** > **Key Vault-parameters**.</span><span class="sxs-lookup"><span data-stu-id="6e729-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="6e729-158">Selecteer een **Key Vault-verwijzing** en selecteer **Toevoegen** in de sectie **Certificaten**.</span><span class="sxs-lookup"><span data-stu-id="6e729-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="6e729-159">Voer in het veld **Naam** de naam in voor het opslagaccountgeheim.</span><span class="sxs-lookup"><span data-stu-id="6e729-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="6e729-160">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6e729-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="6e729-161">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="6e729-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="6e729-162">Selecteer in het veld **Type** de optie **Geheim**.</span><span class="sxs-lookup"><span data-stu-id="6e729-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="6e729-163">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e729-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="6e729-164">Een digitaal certificaatgeheim maken</span><span class="sxs-lookup"><span data-stu-id="6e729-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="6e729-165">Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Serviceomgeving** en selecteer **Key Vault-parameters**.</span><span class="sxs-lookup"><span data-stu-id="6e729-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="6e729-166">Selecteer een **Key Vault-verwijzing** en selecteer **Toevoegen** in de sectie **Certificaten**.</span><span class="sxs-lookup"><span data-stu-id="6e729-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="6e729-167">Voer in het veld **Naam** de naam in voor het digitale certificaatgeheim.</span><span class="sxs-lookup"><span data-stu-id="6e729-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="6e729-168">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6e729-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="6e729-169">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="6e729-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="6e729-170">Selecteer in het veld **Type** de optie **Certificaat**.</span><span class="sxs-lookup"><span data-stu-id="6e729-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="6e729-171">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e729-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="6e729-172">Een serviceomgeving maken</span><span class="sxs-lookup"><span data-stu-id="6e729-172">Create a service environment</span></span>

1. <span data-ttu-id="6e729-173">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="6e729-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="6e729-174">Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Elektronische facturering**.</span><span class="sxs-lookup"><span data-stu-id="6e729-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="6e729-175">Selecteer op de pagina **Omgevingsinstellingen** in het actievenster de optie **Serviceomgeving**.</span><span class="sxs-lookup"><span data-stu-id="6e729-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="6e729-176">Selecteer **Nieuw** om een nieuwe serviceomgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="6e729-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="6e729-177">Voer in het veld **Naam** de naam in voor de omgeving voor e-facturering.</span><span class="sxs-lookup"><span data-stu-id="6e729-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="6e729-178">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="6e729-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="6e729-179">Selecteer in het veld **Opslag SAS-tokengeheim** de naam van het opslagaccountgeheim dat moet worden gebruikt om toegang tot het opslagaccount te verifiëren.</span><span class="sxs-lookup"><span data-stu-id="6e729-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="6e729-180">In de sectie **Gebruikers** selecteert u **Toevoegen** om een gebruiker toe te voegen die elektronische facturen via de omgeving mag indienen en ook verbinding mag maken met het opslagaccount.</span><span class="sxs-lookup"><span data-stu-id="6e729-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="6e729-181">Voer in het veld **Gebruikers-id** het alias van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="6e729-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="6e729-182">Voer in het veld **E-mail** het e-mailadres van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="6e729-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="6e729-183">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6e729-183">Select **Save**.</span></span>
10. <span data-ttu-id="6e729-184">Als uw land-/regiospecifieke facturen een keten certificaten vereisen om digitale handtekeningen toe te passen, selecteert u in het actiedeelvenster de optie **Key Vault-parameters** en vervolgens **Keten van certificaten** en voert u deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="6e729-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="6e729-185">Selecteer **Nieuw** om een keten certificaten te maken.</span><span class="sxs-lookup"><span data-stu-id="6e729-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="6e729-186">Voer in het veld **Naam** de naam in voor de certificaatketen.</span><span class="sxs-lookup"><span data-stu-id="6e729-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="6e729-187">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="6e729-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="6e729-188">Selecteer in het gedeelte **Certificaten** de oiptie **Toevoegen** om een certificaat aan de keten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="6e729-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="6e729-189">Met de knop **Omhoog** of **Omlaag** kunt u de positie van het certificaat in de keten wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6e729-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="6e729-190">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e729-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="6e729-191">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e729-191">Close the page.</span></span>
11. <span data-ttu-id="6e729-192">Selecteer op de pagina **Serviceomgeving** in het actiedeelvenster de optie **Publiceren** om de omgeving naar de cloud te publiceren.</span><span class="sxs-lookup"><span data-stu-id="6e729-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="6e729-193">De waarde van het veld **Status** wordt gewijzigd in **Gepubliceerd**.</span><span class="sxs-lookup"><span data-stu-id="6e729-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="6e729-194">Een verbonden toepassing maken</span><span class="sxs-lookup"><span data-stu-id="6e729-194">Create a connected application</span></span>

1. <span data-ttu-id="6e729-195">Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Verbonden toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="6e729-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="6e729-196">Selecteer **Nieuw** om een verbonden toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="6e729-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="6e729-197">Voer in het veld **Naam** de naam in voor de toepassing die moet worden verbonden.</span><span class="sxs-lookup"><span data-stu-id="6e729-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="6e729-198">Voer in het veld **Toepassing** de URL in van de Finance and Supply Chain Management-omgeving die u wilt verbinden.</span><span class="sxs-lookup"><span data-stu-id="6e729-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="6e729-199">Voer in het veld **Tenant** de tenant in van de Finance and Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6e729-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="6e729-200">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6e729-200">Select **Save**.</span></span>
6. <span data-ttu-id="6e729-201">Selecteer in het actievenster de optie **Verbinding controleren** om de verbinding met de omgeving te testen.</span><span class="sxs-lookup"><span data-stu-id="6e729-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="6e729-202">Sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="6e729-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="6e729-203">Verbonden toepassingen aan omgevingen koppelen</span><span class="sxs-lookup"><span data-stu-id="6e729-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="6e729-204">Selecteer op de pagina **Omgevingsinstellingen** de optie **Nieuw** om een verbonden toepassing toe te wijzen aan een omgeving.</span><span class="sxs-lookup"><span data-stu-id="6e729-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="6e729-205">Selecteer in het veld **Verbonden toepassing** een verbonden toepassing.</span><span class="sxs-lookup"><span data-stu-id="6e729-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="6e729-206">Selecteer in het veld **Serviceomgeving** een serviceomgeving.</span><span class="sxs-lookup"><span data-stu-id="6e729-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="6e729-207">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e729-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="6e729-208">De integratie van Elektronische facturering instellen in Finance en Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6e729-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="6e729-209">De functie voor integratie van Elektronische facturering inschakelen</span><span class="sxs-lookup"><span data-stu-id="6e729-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="6e729-210">Meld u aan bij uw Finance of Supply Chain Management-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="6e729-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="6e729-211">Zoek in de werkruimte **Functiebeheer** naar de functie **Integratie voor elektronisch factureren**.</span><span class="sxs-lookup"><span data-stu-id="6e729-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="6e729-212">Als deze functie niet op de pagina wordt weergegeven, selecteert u **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="6e729-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="6e729-213">Selecteer de functie en selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="6e729-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="6e729-214">De URL van het service-eindpunt instellen</span><span class="sxs-lookup"><span data-stu-id="6e729-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="6e729-215">Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="6e729-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="6e729-216">Voer op het tabblad **Indieningsservice** in het veld **Service-eindpunt URL** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6e729-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="6e729-217">Datacenter Azure-geografie</span><span class="sxs-lookup"><span data-stu-id="6e729-217">Datacenter Azure geography</span></span> | <span data-ttu-id="6e729-218">URL van service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="6e729-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="6e729-219">VS - oost</span><span class="sxs-lookup"><span data-stu-id="6e729-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="6e729-220">VS - west</span><span class="sxs-lookup"><span data-stu-id="6e729-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="6e729-221">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="6e729-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="6e729-222">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="6e729-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="6e729-223">Voer in het veld **Omgeving** de naam in voor de serviceomgeving die is gepubliceerd in Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="6e729-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="6e729-224">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6e729-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="6e729-225">Flighting-codes inschakelen</span><span class="sxs-lookup"><span data-stu-id="6e729-225">Enable Flighting keys</span></span>

<span data-ttu-id="6e729-226">Schakel flighting-codes in voor Microsoft Dynamics 365 Finance of Microsoft Dynamics 365 Supply Chain Management 10.0.17 of lager.</span><span class="sxs-lookup"><span data-stu-id="6e729-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="6e729-227">Voer de volgende SQL-opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="6e729-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="6e729-228">INVOEGEN IN SYSFLIGHTING-WAARDEN (FLIGHT-NAAM, INGESCHAKELD) ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="6e729-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="6e729-229">INVOEGEN IN SYSFLIGHTING-WAARDEN (FLIGHT-NAAM, INGESCHAKELD) ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="6e729-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="6e729-230">Voer een IISreset-opdracht uit voor alle AOS's.</span><span class="sxs-lookup"><span data-stu-id="6e729-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
