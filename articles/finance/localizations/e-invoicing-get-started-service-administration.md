---
title: Aan de slag met de serviceadministratie voor de invoegtoepassing voor elektronische facturering
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de invoegtoepassing voor elektronische facturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104363"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="e7c83-103">Aan de slag met de serviceadministratie voor de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="e7c83-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e7c83-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="e7c83-104">Prerequisites</span></span>

<span data-ttu-id="e7c83-105">Voordat u de procedures in dit onderwerp voltooit, moet aan de volgende vereisten zijn voldaan:</span><span class="sxs-lookup"><span data-stu-id="e7c83-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="e7c83-106">U moet toegang hebben tot uw Microsoft Dynamics Lifecycle Services-account (LCS).</span><span class="sxs-lookup"><span data-stu-id="e7c83-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="e7c83-107">U moet een LCS-project hebben dat versie 10.0.13 of hoger van Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management bevat.</span><span class="sxs-lookup"><span data-stu-id="e7c83-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e7c83-108">Daarnaast moeten deze apps worden geïmplementeerd in een van de volgende Azure-geografische gebieden:</span><span class="sxs-lookup"><span data-stu-id="e7c83-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="e7c83-109">VS - oost</span><span class="sxs-lookup"><span data-stu-id="e7c83-109">East US</span></span>
    - <span data-ttu-id="e7c83-110">VS - west</span><span class="sxs-lookup"><span data-stu-id="e7c83-110">West US</span></span>
    - <span data-ttu-id="e7c83-111">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="e7c83-111">North EU</span></span>
    - <span data-ttu-id="e7c83-112">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="e7c83-112">West EU</span></span>

- <span data-ttu-id="e7c83-113">U moet toegang hebben tot uw Dynamics 365 Regulatory Configuration Services-account (RCS).</span><span class="sxs-lookup"><span data-stu-id="e7c83-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="e7c83-114">U moet de functie Globalisatie voor uw RCS-account in Functiebeheer activeren.</span><span class="sxs-lookup"><span data-stu-id="e7c83-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="e7c83-115">Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e7c83-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="e7c83-116">U moet een Key Vault-resource en een opslagaccount in Azure maken.</span><span class="sxs-lookup"><span data-stu-id="e7c83-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="e7c83-117">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e7c83-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="e7c83-118">De invoegtoepassing voor microservices in Lifecycle Services installeren</span><span class="sxs-lookup"><span data-stu-id="e7c83-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="e7c83-119">Meld u aan bij uw LCS-account.</span><span class="sxs-lookup"><span data-stu-id="e7c83-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="e7c83-120">Selecteer de tegel **Beheer van voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="e7c83-121">Selecteer **e-Factureringsservice** in het gedeelte **Openbare voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="e7c83-122">Controleer of de optie **Voorbeeldfunctie ingeschakeld** op **Ja** is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e7c83-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="e7c83-123">De parameters voor RCS-integratie met de invoegtoepassing voor elektronisch factureren instellen</span><span class="sxs-lookup"><span data-stu-id="e7c83-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="e7c83-124">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="e7c83-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e7c83-125">Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="e7c83-126">Voer op het tabblad **e-Factureringsservice** in het veld **Service-eindpunt URI** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e7c83-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="e7c83-127">Datacenter Azure-geografie</span><span class="sxs-lookup"><span data-stu-id="e7c83-127">Datacenter Azure geography</span></span> | <span data-ttu-id="e7c83-128">URI van service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="e7c83-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="e7c83-129">VS - oost</span><span class="sxs-lookup"><span data-stu-id="e7c83-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e7c83-130">VS - west</span><span class="sxs-lookup"><span data-stu-id="e7c83-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e7c83-131">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="e7c83-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e7c83-132">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="e7c83-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="e7c83-133">Controleer of het veld **Toepassings-id** is ingesteld op **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="e7c83-134">Dit is een vaste waarde.</span><span class="sxs-lookup"><span data-stu-id="e7c83-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="e7c83-135">Voer in het veld **LCS-omgevings-id** de id van uw LCS-abonnementsaccount in.</span><span class="sxs-lookup"><span data-stu-id="e7c83-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="e7c83-136">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7c83-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="e7c83-137">Key Vault-geheim maken</span><span class="sxs-lookup"><span data-stu-id="e7c83-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="e7c83-138">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="e7c83-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e7c83-139">Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **e-Facturering**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="e7c83-140">Selecteer op de pagina **Omgevingsinstellingen** op het actiedeelvenster de optie **Serviceomgeving** en selecteer **Key Vault-parameters**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="e7c83-141">Selecteer **Nieuw** om een Key Vault-geheim te maken.</span><span class="sxs-lookup"><span data-stu-id="e7c83-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="e7c83-142">Voer in het veld **Naam** de naam in voor het Key Vault-geheim.</span><span class="sxs-lookup"><span data-stu-id="e7c83-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="e7c83-143">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="e7c83-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="e7c83-144">Plak in het veld **Key Vault-URI** het geheim van Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e7c83-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="e7c83-145">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="e7c83-146">Een opslagaccountgeheim maken</span><span class="sxs-lookup"><span data-stu-id="e7c83-146">Create Storage account secret</span></span>

1. <span data-ttu-id="e7c83-147">Selecteer op de pagina **Key Vault-parameters** in de sectie **Certificaten** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="e7c83-148">Voer in het veld **Naam** de naam in voor het opslagaccountgeheim.</span><span class="sxs-lookup"><span data-stu-id="e7c83-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="e7c83-149">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="e7c83-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="e7c83-150">Selecteer in het veld **Type** de optie **Certificaat**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="e7c83-151">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7c83-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="e7c83-152">Een omgeving van de invoegtoepassing voor elektronische facturering maken</span><span class="sxs-lookup"><span data-stu-id="e7c83-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="e7c83-153">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="e7c83-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e7c83-154">Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **e-Facturering**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="e7c83-155">Een serviceomgeving maken</span><span class="sxs-lookup"><span data-stu-id="e7c83-155">Create a service environment</span></span>

1. <span data-ttu-id="e7c83-156">Selecteer op de pagina **Omgevingsinstellingen** op het actiedeelvenster de optie **Serviceomgeving**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="e7c83-157">Selecteer **Nieuw** om een nieuwe serviceomgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="e7c83-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="e7c83-158">Voer in het veld **Naam** de naam in voor de omgeving voor e-facturering.</span><span class="sxs-lookup"><span data-stu-id="e7c83-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="e7c83-159">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="e7c83-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="e7c83-160">Selecteer in het veld **Opslag SAS-tokengeheim** de naam van het certificaat dat moet worden gebruikt om toegang tot het opslagaccount te verifiëren.</span><span class="sxs-lookup"><span data-stu-id="e7c83-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="e7c83-161">In de sectie **Gebruikers** selecteert u **Toevoegen** om een gebruiker toe te voegen die elektronische facturen via de omgeving mag indienen en ook verbinding mag maken met het opslagaccount.</span><span class="sxs-lookup"><span data-stu-id="e7c83-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="e7c83-162">Voer in het veld **Gebruikers-id** het alias van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="e7c83-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="e7c83-163">Voer in het veld **E-mail** het e-mailadres van de gebruiker in.</span><span class="sxs-lookup"><span data-stu-id="e7c83-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="e7c83-164">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-164">Select **Save**.</span></span>
8. <span data-ttu-id="e7c83-165">Als uw land-/regiospecifieke facturen een keten certificaten vereisen om digitale handtekeningen toe te passen, selecteert u in het actiedeelvenster de optie **Key Vault-parameters** en vervolgens **Keten van certificaten** en voert u deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="e7c83-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="e7c83-166">Selecteer **Nieuw** om een keten certificaten te maken.</span><span class="sxs-lookup"><span data-stu-id="e7c83-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="e7c83-167">Voer in het veld **Naam** de naam in voor de certificaatketen.</span><span class="sxs-lookup"><span data-stu-id="e7c83-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="e7c83-168">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="e7c83-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="e7c83-169">Selecteer in het gedeelte **Certificaten** de oiptie **Toevoegen** om een certificaat aan de keten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e7c83-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="e7c83-170">Met de knop **Omhoog** of **Omlaag** kunt u de positie van het certificaat in de keten wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e7c83-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="e7c83-171">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7c83-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="e7c83-172">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7c83-172">Close the page.</span></span>
9. <span data-ttu-id="e7c83-173">Selecteer op de pagina **Serviceomgeving** in het actiedeelvenster de optie **Publiceren** om de omgeving naar de cloud te publiceren.</span><span class="sxs-lookup"><span data-stu-id="e7c83-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="e7c83-174">De waarde van het veld **Status** wordt gewijzigd in **Gepubliceerd**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="e7c83-175">Een verbonden toepassing maken</span><span class="sxs-lookup"><span data-stu-id="e7c83-175">Create a connected application</span></span>

1. <span data-ttu-id="e7c83-176">Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Verbonden toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="e7c83-177">Selecteer **Nieuw** om een verbonden toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="e7c83-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="e7c83-178">Voer in het veld **Naam** de naam in voor de toepassing die moet worden verbonden.</span><span class="sxs-lookup"><span data-stu-id="e7c83-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="e7c83-179">Voer in het veld **Toepassing** de URL in van de Finance and Supply Chain Management-omgeving die u wilt verbinden.</span><span class="sxs-lookup"><span data-stu-id="e7c83-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="e7c83-180">Voer in het veld **Tenant** de tenant in van de Finance and Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e7c83-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="e7c83-181">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-181">Select **Save**.</span></span>
6. <span data-ttu-id="e7c83-182">Selecteer in het actievenster de optie **Verbinding controleren** om de verbinding met de omgeving te testen.</span><span class="sxs-lookup"><span data-stu-id="e7c83-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="e7c83-183">Sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="e7c83-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="e7c83-184">Verbonden toepassingen aan omgevingen koppelen</span><span class="sxs-lookup"><span data-stu-id="e7c83-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="e7c83-185">Selecteer op de pagina **Omgevingsinstellingen** de optie **Nieuw** om een verbonden toepassing toe te wijzen aan een omgeving.</span><span class="sxs-lookup"><span data-stu-id="e7c83-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="e7c83-186">Selecteer in het veld **Verbonden toepassing** een verbonden toepassing.</span><span class="sxs-lookup"><span data-stu-id="e7c83-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="e7c83-187">Selecteer in het veld **Serviceomgeving** een serviceomgeving.</span><span class="sxs-lookup"><span data-stu-id="e7c83-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="e7c83-188">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7c83-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="e7c83-189">De integratie van de invoegtoepassing voor elektronisch factureren instellen in Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e7c83-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="e7c83-190">De integratie van de invoegtoepassing voor elektronisch factureren inschakelen</span><span class="sxs-lookup"><span data-stu-id="e7c83-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="e7c83-191">Meld u aan bij uw Finance of Supply Chain Management-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="e7c83-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="e7c83-192">Zoek in de werkruimte **Functiebeheer** naar de functie **Integratie invoegtoepassing voor elektronisch factureren**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="e7c83-193">Als deze functie niet op de pagina wordt weergegeven, selecteert u **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="e7c83-194">Selecteer de functie en selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="e7c83-195">De URL van het service-eindpunt instellen</span><span class="sxs-lookup"><span data-stu-id="e7c83-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="e7c83-196">Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="e7c83-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="e7c83-197">Voer op het tabblad **Indieningsservice** in het veld **Service-eindpunt URL** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e7c83-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="e7c83-198">Datacenter Azure-geografie</span><span class="sxs-lookup"><span data-stu-id="e7c83-198">Datacenter Azure geography</span></span> | <span data-ttu-id="e7c83-199">URL van service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="e7c83-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="e7c83-200">VS - oost</span><span class="sxs-lookup"><span data-stu-id="e7c83-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e7c83-201">VS - west</span><span class="sxs-lookup"><span data-stu-id="e7c83-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e7c83-202">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="e7c83-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e7c83-203">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="e7c83-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="e7c83-204">Voer in het veld **Omgeving** de naam in voor de omgeving voor de invoegtoepassing voor e-facturering.</span><span class="sxs-lookup"><span data-stu-id="e7c83-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="e7c83-205">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7c83-205">Select **Save**, and then close the page.</span></span>
