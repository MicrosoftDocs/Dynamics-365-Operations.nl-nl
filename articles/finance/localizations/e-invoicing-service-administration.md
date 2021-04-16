---
title: Beheeronderdelen voor elektronische facturering
description: Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de functie voor elektronische facturering.
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840023"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="adbfe-103">Beheeronderdelen voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="adbfe-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="adbfe-104">Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de functie voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="adbfe-105">Daarnaast vindt u hier informatie over het configureren van de service voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="adbfe-106">Azure</span><span class="sxs-lookup"><span data-stu-id="adbfe-106">Azure</span></span>

<span data-ttu-id="adbfe-107">Gebruik Microsoft Azure om de geheimen voor het Key Vault- en opslagaccount te maken.</span><span class="sxs-lookup"><span data-stu-id="adbfe-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="adbfe-108">Gebruik de geheimen vervolgens in de configuratie van Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="adbfe-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="adbfe-109">Lifecycle Services</span></span>

<span data-ttu-id="adbfe-110">Gebruik Microsoft Dynamics Lifecycle Services (LCS) om de microservices voor het LCS-implementatieproject in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="adbfe-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="adbfe-111">Voor de installatie van de microservice in LCS is ten minste een Tier 2 virtuele machine vereist.</span><span class="sxs-lookup"><span data-stu-id="adbfe-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="adbfe-112">Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie over omgevingsplanning.</span><span class="sxs-lookup"><span data-stu-id="adbfe-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="adbfe-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="adbfe-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="adbfe-114">Dynamics 365 Regulatory Configuration Services (RCS) is de interface waarmee u Elektronische facturering configureert.</span><span class="sxs-lookup"><span data-stu-id="adbfe-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="adbfe-115">Resources, zoals omgevingen en functies voor elektronische facturering, worden gemaakt, beheerd en gehost in RCS.</span><span class="sxs-lookup"><span data-stu-id="adbfe-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="adbfe-116">Wanneer de resources gereed zijn, worden ze gepubliceerd in de service voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="adbfe-117">Zie [Wettelijke services](https://marketing.configure.global.dynamics.com/) voor registratie bij RCS.</span><span class="sxs-lookup"><span data-stu-id="adbfe-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="adbfe-118">Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie over RCS</span><span class="sxs-lookup"><span data-stu-id="adbfe-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="adbfe-119">Integratie met Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="adbfe-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="adbfe-120">Voordat u RCS kunt gebruiken voor het configureren van elektronische facturen, moet u RCS zo configureren dat communicatie met Elektronische facturering is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="adbfe-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="adbfe-121">U voltooit deze configuratie op het tabblad **Elektronische facturering** van de pagina **Parameters voor elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="adbfe-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="adbfe-122">Service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="adbfe-122">Service endpoint</span></span>

<span data-ttu-id="adbfe-123">Elektronische facturering is beschikbaar in verschillende Azure-datacentergeografieën.</span><span class="sxs-lookup"><span data-stu-id="adbfe-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="adbfe-124">In de volgende tabel wordt de beschikbaarheid per regio vermeld.</span><span class="sxs-lookup"><span data-stu-id="adbfe-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="adbfe-125">Geografie Azure-datacenter</span><span class="sxs-lookup"><span data-stu-id="adbfe-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="adbfe-126">VS - oost</span><span class="sxs-lookup"><span data-stu-id="adbfe-126">East US</span></span>                    |
| <span data-ttu-id="adbfe-127">VS - west</span><span class="sxs-lookup"><span data-stu-id="adbfe-127">West US</span></span>                    |
| <span data-ttu-id="adbfe-128">Noordelijke EU</span><span class="sxs-lookup"><span data-stu-id="adbfe-128">North EU</span></span>                   |
| <span data-ttu-id="adbfe-129">Westelijke EU</span><span class="sxs-lookup"><span data-stu-id="adbfe-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="adbfe-130">Serviceomgevingen</span><span class="sxs-lookup"><span data-stu-id="adbfe-130">Service environments</span></span>

<span data-ttu-id="adbfe-131">Serviceomgevingen zijn logische partities die worden gemaakt om de uitvoering van de elektronische factureringsfuncties in Elektronische facturering te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="adbfe-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="adbfe-132">De beveiligingsrechten en digitale certificaten en de governance (toegangsmachtigingen) moeten worden geconfigureerd op het niveau van de serviceomgeving.</span><span class="sxs-lookup"><span data-stu-id="adbfe-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="adbfe-133">Klanten kunnen net zo veel serviceomgevingen maken als zij willen.</span><span class="sxs-lookup"><span data-stu-id="adbfe-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="adbfe-134">Alle serviceomgevingen die door een klant worden gemaakt, zijn onafhankelijk van elkaar.</span><span class="sxs-lookup"><span data-stu-id="adbfe-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="adbfe-135">Serviceomgevingen moeten worden gemaakt en onderhouden in RCS.</span><span class="sxs-lookup"><span data-stu-id="adbfe-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="adbfe-136">Wanneer de serviceomgevingen gereed zijn, moeten ze worden gepubliceerd in Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="adbfe-137">Status van de serviceomgeving</span><span class="sxs-lookup"><span data-stu-id="adbfe-137">Service environment status</span></span>

<span data-ttu-id="adbfe-138">Serviceomgevingen kunnen worden beheerd via de status.</span><span class="sxs-lookup"><span data-stu-id="adbfe-138">Service environments can be managed through status.</span></span> <span data-ttu-id="adbfe-139">De mogelijke opties zijn:</span><span class="sxs-lookup"><span data-stu-id="adbfe-139">The possible options are:</span></span>

- <span data-ttu-id="adbfe-140">**Niet gepubliceerd**: de omgeving is gemaakt, maar nog niet gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="adbfe-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="adbfe-141">**Gepubliceerd**: de omgeving is gepubliceerd in Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="adbfe-142">**Gewijzigd**: de kenmerken van een gepubliceerde omgeving zijn gewijzigd, maar de wijzigingen zijn nog niet gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="adbfe-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="adbfe-143">Klantgeheimen</span><span class="sxs-lookup"><span data-stu-id="adbfe-143">Customer secrets</span></span>

<span data-ttu-id="adbfe-144">De service voor elektronische facturering is verantwoordelijk voor het opslaan van al uw bedrijfsgegevens in de Azure-resources die uw bedrijf bezit.</span><span class="sxs-lookup"><span data-stu-id="adbfe-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="adbfe-145">Om er zeker van te zijn dat de service correct werkt en dat alle bedrijfsgegevens die nodig zijn voor en die worden gegenereerd door Elektronische facturering correct worden gebruikt, moet u twee hoofd Azure-resources maken:</span><span class="sxs-lookup"><span data-stu-id="adbfe-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="adbfe-146">Een Azure-opslagaccount (Blob-opslag) waarin elektronische facturen worden opgeslagen</span><span class="sxs-lookup"><span data-stu-id="adbfe-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="adbfe-147">Een Azure Key Vault voor de opslag van certificaten en de URI (Uniform Resource Identifier) van het opslagaccount</span><span class="sxs-lookup"><span data-stu-id="adbfe-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="adbfe-148">Een speciale Key Vault en een opslagaccount van de klant moeten specifiek worden toegewezen voor gebruik met Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing .</span></span>

<span data-ttu-id="adbfe-149">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="adbfe-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="adbfe-150">Gebruikers</span><span class="sxs-lookup"><span data-stu-id="adbfe-150">Users</span></span>

<span data-ttu-id="adbfe-151">Elke serviceomgeving moet een lijst maken met de gebruikers die verbinding kunnen maken vanuit Dynamics 365 Finance en Dynamics 365 Supply Chain Management in Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="adbfe-152">Publicatie</span><span class="sxs-lookup"><span data-stu-id="adbfe-152">Publication</span></span>

<span data-ttu-id="adbfe-153">Serviceomgevingen moeten worden gepubliceerd in Elektronische facturering voordat ze kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="adbfe-153">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="adbfe-154">Alleen gepubliceerde omgevingen kunnen worden gebruikt door Finance en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="adbfe-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="adbfe-155">Daarnaast moet een serviceomgeving worden gepubliceerd voordat updates van de kenmerken van kracht worden op de elektronische factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="adbfe-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="adbfe-156">Verbonden toepassingen</span><span class="sxs-lookup"><span data-stu-id="adbfe-156">Connected applications</span></span>

<span data-ttu-id="adbfe-157">Verbonden toepassingen zijn de exemplaren van Finance en Supply Chain Management die u mogelijk wilt bereiken via RCS.</span><span class="sxs-lookup"><span data-stu-id="adbfe-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="adbfe-158">Naast de URL van de toepassing en de tenant ervan, bevat een verbonden toepassing de referenties waarmee RCS verbinding kan maken met de omgeving.</span><span class="sxs-lookup"><span data-stu-id="adbfe-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="adbfe-159">Via de verbonden toepassingen kunt u een gedeelte van de elektronische factureringsfunctie in Finance en Supply Chain Management configureren om de gehele elektronische factureringsfunctie te laten werken.</span><span class="sxs-lookup"><span data-stu-id="adbfe-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="adbfe-160">Finance en Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="adbfe-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="adbfe-161">Integratie met Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="adbfe-161">Integration with Electronic invoicing</span></span>

<span data-ttu-id="adbfe-162">Voordat u Finance en Supply Chain Management kunt gebruiken om elektronische facturen uit te geven via Elektronische facturering, moet Elektronische facturering worden geconfigureerd zodat kan worden gecommuniceerd met de service.</span><span class="sxs-lookup"><span data-stu-id="adbfe-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="adbfe-163">Integratiefunctie van Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="adbfe-163">Electronic invoicing integration feature</span></span>

<span data-ttu-id="adbfe-164">Als u de communicatie tussen Finance en Supply Chain Management en Elektronische facturering wilt inschakelen, moet u de functie **Integratie van Elektronische facturering** in de werkruimte **Functiebeheer** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="adbfe-164">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="adbfe-165">Service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="adbfe-165">Service endpoint</span></span>

<span data-ttu-id="adbfe-166">Het service-eindpunt is de URL waar Elektronische facturering zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="adbfe-166">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="adbfe-167">Voordat elektronische facturen kunnen worden uitgegeven, moet het service-eindpunt worden geconfigureerd in Finance en Supply Chain Management om communicatie met de service mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="adbfe-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="adbfe-168">Om het service-eindpunt te configureren, gaat u naar **Organisatiebeheer \> Instellen \> Parameter voor elektronisch document** en daarna voert u op het tabblad **Indieningsservices** in het veld **URL van Elektronische facturering** de URL in, zoals wordt beschreven in de tabel uit de sectie **Service-eindpunt**.</span><span class="sxs-lookup"><span data-stu-id="adbfe-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="adbfe-169">Omgevingen</span><span class="sxs-lookup"><span data-stu-id="adbfe-169">Environments</span></span>

<span data-ttu-id="adbfe-170">De omgevingsnaam die wordt ingevoerd in Finance en Supply Chain Management, verwijst naar de naam van de omgeving die in RCS wordt gemaakt en gepubliceerd naar Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="adbfe-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="adbfe-171">De omgeving moet worden geconfigureerd op het tabblad **Indieningsservices** van de pagina **Parameter voor elektronisch document**, zodat elk verzoek om elektronische facturen uit te geven de omgeving bevat waarin Elektronische facturering kan bepalen welke functie voor elektronische facturering het verzoek moet verwerken.</span><span class="sxs-lookup"><span data-stu-id="adbfe-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adbfe-172">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="adbfe-172">Additional resources</span></span>

- [<span data-ttu-id="adbfe-173">Elektronische facturen configureren in RCS</span><span class="sxs-lookup"><span data-stu-id="adbfe-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="adbfe-174">Elektronische facturen uitgeven in Finance en Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="adbfe-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
