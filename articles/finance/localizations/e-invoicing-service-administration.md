---
title: Beheeronderdelen van de invoegtoepassing voor elektronische facturering
description: Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de invoegtoepassing voor elektronische facturering.
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592569"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="e72c2-103">Beheeronderdelen van de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="e72c2-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e72c2-104">Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="e72c2-105">Daarnaast vindt u hier informatie over het configureren van de invoegtoepassingsservice voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="e72c2-106">Azure</span><span class="sxs-lookup"><span data-stu-id="e72c2-106">Azure</span></span>

<span data-ttu-id="e72c2-107">Gebruik Microsoft Azure om de geheimen voor het Key Vault- en opslagaccount te maken.</span><span class="sxs-lookup"><span data-stu-id="e72c2-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="e72c2-108">Gebruik de geheimen vervolgens in de configuratie van de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="e72c2-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e72c2-109">Lifecycle Services</span></span>

<span data-ttu-id="e72c2-110">Gebruik Microsoft Dynamics Lifecycle Services (LCS) om de invoegtoepassing voor de microservices voor het LCS-implementatieproject in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="e72c2-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="e72c2-111">Voor de installatie van de microservice-invoegtoepassing in LCS is ten minste een Tier 2 virtuele machine vereist.</span><span class="sxs-lookup"><span data-stu-id="e72c2-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="e72c2-112">Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie over omgevingsplanning.</span><span class="sxs-lookup"><span data-stu-id="e72c2-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="e72c2-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="e72c2-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="e72c2-114">Dynamics 365 Regulatory Configuration Services (RCS) is de interface waarmee u de invoegtoepassing voor elektronische facturering configureert.</span><span class="sxs-lookup"><span data-stu-id="e72c2-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="e72c2-115">Resources, zoals omgevingen en functies voor elektronische facturering, worden gemaakt, beheerd en gehost in RCS.</span><span class="sxs-lookup"><span data-stu-id="e72c2-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="e72c2-116">Wanneer de resources gereed zijn, worden ze gepubliceerd in de invoegtoepassingsservice voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="e72c2-117">Zie [Wettelijke services](https://marketing.configure.global.dynamics.com/) voor registratie bij RCS.</span><span class="sxs-lookup"><span data-stu-id="e72c2-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="e72c2-118">Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie over RCS</span><span class="sxs-lookup"><span data-stu-id="e72c2-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="e72c2-119">Integratie met de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="e72c2-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="e72c2-120">Voordat u RCS kunt gebruiken voor het configureren van elektronische facturen, moet u RCS zo configureren dat communicatie met de invoegtoepassing voor elektronische facturering is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="e72c2-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="e72c2-121">U voltooit deze configuratie op het tabblad **Invoegtoepassing voor elektronische facturering** van de pagina **Parameters voor elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="e72c2-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="e72c2-122">Service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="e72c2-122">Service endpoint</span></span>

<span data-ttu-id="e72c2-123">De invoegtoepassing voor elektronische facturering is beschikbaar in verschillende Azure-datacentergeografieën.</span><span class="sxs-lookup"><span data-stu-id="e72c2-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="e72c2-124">In de volgende tabel wordt de beschikbaarheid per regio vermeld.</span><span class="sxs-lookup"><span data-stu-id="e72c2-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="e72c2-125">Geografie Azure-datacenter</span><span class="sxs-lookup"><span data-stu-id="e72c2-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="e72c2-126">VS - oost</span><span class="sxs-lookup"><span data-stu-id="e72c2-126">East US</span></span>                    |
| <span data-ttu-id="e72c2-127">VS - west</span><span class="sxs-lookup"><span data-stu-id="e72c2-127">West US</span></span>                    |
| <span data-ttu-id="e72c2-128">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="e72c2-128">North EU</span></span>                   |
| <span data-ttu-id="e72c2-129">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="e72c2-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="e72c2-130">Serviceomgevingen</span><span class="sxs-lookup"><span data-stu-id="e72c2-130">Service environments</span></span>

<span data-ttu-id="e72c2-131">Serviceomgevingen zijn logische partities die worden gemaakt om de uitvoering van de elektronische factureringsfuncties in de invoegtoepassing voor elektronische facturering te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="e72c2-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="e72c2-132">De beveiligingsrechten en digitale certificaten en de governance (toegangsmachtigingen) moeten worden geconfigureerd op het niveau van de serviceomgeving.</span><span class="sxs-lookup"><span data-stu-id="e72c2-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="e72c2-133">Klanten kunnen net zo veel serviceomgevingen maken als zij willen.</span><span class="sxs-lookup"><span data-stu-id="e72c2-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="e72c2-134">Alle serviceomgevingen die door een klant worden gemaakt, zijn onafhankelijk van elkaar.</span><span class="sxs-lookup"><span data-stu-id="e72c2-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="e72c2-135">Serviceomgevingen moeten worden gemaakt en onderhouden in RCS.</span><span class="sxs-lookup"><span data-stu-id="e72c2-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="e72c2-136">Wanneer de serviceomgevingen gereed zijn, moeten ze worden gepubliceerd in de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="e72c2-137">Status van de serviceomgeving</span><span class="sxs-lookup"><span data-stu-id="e72c2-137">Service environment status</span></span>

<span data-ttu-id="e72c2-138">Serviceomgevingen kunnen worden beheerd via de status.</span><span class="sxs-lookup"><span data-stu-id="e72c2-138">Service environments can be managed through status.</span></span> <span data-ttu-id="e72c2-139">De mogelijke opties zijn:</span><span class="sxs-lookup"><span data-stu-id="e72c2-139">The possible options are:</span></span>

- <span data-ttu-id="e72c2-140">**Niet gepubliceerd**: de omgeving is gemaakt, maar nog niet gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="e72c2-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="e72c2-141">**Gepubliceerd**: de omgeving is gepubliceerd in de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="e72c2-142">**Gewijzigd**: de kenmerken van een gepubliceerde omgeving zijn gewijzigd, maar de wijzigingen zijn nog niet gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="e72c2-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="e72c2-143">Klantgeheimen</span><span class="sxs-lookup"><span data-stu-id="e72c2-143">Customer secrets</span></span>

<span data-ttu-id="e72c2-144">De invoegtoepassing voor elektronische facturering is verantwoordelijk voor het opslaan van al uw bedrijfsgegevens in de Azure-resources die uw bedrijf bezit.</span><span class="sxs-lookup"><span data-stu-id="e72c2-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="e72c2-145">Om er zeker van te zijn dat de service correct werkt en dat alle bedrijfsgegevens die vereist zijn voor en die worden gegenereerd door de invoegtoepassing voor elektronische facturering alleen worden gebruikt door de invoegtoepassing, moet u twee Azure-resources maken:</span><span class="sxs-lookup"><span data-stu-id="e72c2-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="e72c2-146">Een Azure-opslagaccount (Blob-opslag) waarin elektronische facturen worden opgeslagen</span><span class="sxs-lookup"><span data-stu-id="e72c2-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="e72c2-147">Een Azure Key Vault voor de opslag van certificaten en de URI (Uniform Resource Identifier) van het opslagaccount</span><span class="sxs-lookup"><span data-stu-id="e72c2-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="e72c2-148">Een speciale Key Vault en een opslagaccount van de klant moeten specifiek worden toegewezen voor gebruik met de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="e72c2-149">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e72c2-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="e72c2-150">Gebruikers</span><span class="sxs-lookup"><span data-stu-id="e72c2-150">Users</span></span>

<span data-ttu-id="e72c2-151">Elke serviceomgeving moet een lijst maken met de gebruikers die verbinding kunnen maken vanuit Dynamics 365 Finance en Dynamics 365 Supply Chain Management in de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="e72c2-152">Publicatie</span><span class="sxs-lookup"><span data-stu-id="e72c2-152">Publication</span></span>

<span data-ttu-id="e72c2-153">Serviceomgevingen moeten worden gepubliceerd in de invoegtoepassing voor elektronische facturering voordat ze kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e72c2-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="e72c2-154">Alleen gepubliceerde omgevingen kunnen worden gebruikt door Finance en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e72c2-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="e72c2-155">Daarnaast moet een serviceomgeving worden gepubliceerd voordat updates van de kenmerken van kracht worden op de elektronische factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="e72c2-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="e72c2-156">Verbonden toepassingen</span><span class="sxs-lookup"><span data-stu-id="e72c2-156">Connected applications</span></span>

<span data-ttu-id="e72c2-157">Verbonden toepassingen zijn de exemplaren van Finance en Supply Chain Management die u mogelijk wilt bereiken via RCS.</span><span class="sxs-lookup"><span data-stu-id="e72c2-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="e72c2-158">Naast de URL van de toepassing en de tenant ervan, bevat een verbonden toepassing de referenties waarmee RCS verbinding kan maken met de omgeving.</span><span class="sxs-lookup"><span data-stu-id="e72c2-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="e72c2-159">Via de verbonden toepassingen kunt u een gedeelte van de elektronische factureringsfunctie in Finance en Supply Chain Management configureren om de gehele elektronische factureringsfunctie te laten werken.</span><span class="sxs-lookup"><span data-stu-id="e72c2-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="e72c2-160">Finance en Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e72c2-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="e72c2-161">Integratie met de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="e72c2-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="e72c2-162">Voordat u Finance en Supply Chain Management kunt gebruiken om elektronische facturen uit te geven via de invoegtoepassing voor elektronische facturering, moet de invoegtoepassing worden geconfigureerd zodat kan worden gecommuniceerd met de service.</span><span class="sxs-lookup"><span data-stu-id="e72c2-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="e72c2-163">Integratiefunctie van de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="e72c2-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="e72c2-164">Als u de communicatie tussen Finance en Supply Chain Management en de invoegtoepassing voor elektronische facturering wilt inschakelen, moet u de **Integratiefunctie van de invoegtoepassing voor elektronische facturering** in de werkruimte **Functiebeheer** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="e72c2-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="e72c2-165">Service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="e72c2-165">Service endpoint</span></span>

<span data-ttu-id="e72c2-166">Het service-eindpunt is de URL waar de invoegtoepassing voor elektronische facturering zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="e72c2-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="e72c2-167">Voordat elektronische facturen kunnen worden uitgegeven, moet het service-eindpunt worden geconfigureerd in Finance en Supply Chain Management om communicatie met de service mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="e72c2-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="e72c2-168">Om het service-eindpunt te configureren, gaat u naar **Organisatiebeheer \> Instellen \> Parameter voor elektronisch document** en daarna voert u op het tabblad **Indieningsservices** in het veld **URL van de invoegtoepassing voor elektronische facturering** de URL in, zoals wordt beschreven in de tabel uit de sectie **Service-eindpunt**.</span><span class="sxs-lookup"><span data-stu-id="e72c2-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="e72c2-169">Omgevingen</span><span class="sxs-lookup"><span data-stu-id="e72c2-169">Environments</span></span>

<span data-ttu-id="e72c2-170">De omgevingsnaam die wordt ingevoerd in Finance en Supply Chain Management, verwijst naar de naam van de omgeving die in RCS wordt gemaakt en gepubliceerd naar de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="e72c2-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="e72c2-171">De omgeving moet worden geconfigureerd op het tabblad **Indieningsservices** van de pagina **Parameter voor elektronisch document**, zodat elk verzoek om elektronische facturen uit te geven de omgeving bevat waarin de invoegtoepassing voor elektronische facturering kan bepalen welke functie voor elektronische facturering het verzoek moet verwerken.</span><span class="sxs-lookup"><span data-stu-id="e72c2-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e72c2-172">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e72c2-172">Additional resources</span></span>

- [<span data-ttu-id="e72c2-173">Elektronische facturen configureren in RCS</span><span class="sxs-lookup"><span data-stu-id="e72c2-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="e72c2-174">Elektronische facturen uitgeven in Finance en Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e72c2-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
