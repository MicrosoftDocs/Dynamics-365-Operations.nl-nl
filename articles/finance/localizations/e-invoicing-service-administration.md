---
title: Beheeronderdelen voor elektronische facturering
description: Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de functie voor elektronische facturering.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980918"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="81193-103">Beheeronderdelen voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="81193-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="81193-104">Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de functie voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="81193-105">Daarnaast vindt u hier informatie over het configureren van de service voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="81193-106">Azure</span><span class="sxs-lookup"><span data-stu-id="81193-106">Azure</span></span>

<span data-ttu-id="81193-107">Gebruik Microsoft Azure om de geheimen voor de Key Vault en het opslagaccount te maken.</span><span class="sxs-lookup"><span data-stu-id="81193-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="81193-108">Gebruik de geheimen vervolgens in de configuratie van Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="81193-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="81193-109">Lifecycle Services</span></span>

<span data-ttu-id="81193-110">Gebruik Microsoft Dynamics Lifecycle Services (LCS) om de microservices voor het LCS-implementatieproject in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="81193-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="81193-111">Voor de installatie van de microservice in LCS is ten minste een Tier 2 virtuele machine vereist.</span><span class="sxs-lookup"><span data-stu-id="81193-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="81193-112">Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie over omgevingsplanning.</span><span class="sxs-lookup"><span data-stu-id="81193-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="81193-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="81193-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="81193-114">Dynamics 365 Regulatory Configuration Services (RCS) is de interface waarmee u Elektronische facturering configureert.</span><span class="sxs-lookup"><span data-stu-id="81193-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="81193-115">Resources, zoals omgevingen en functies voor elektronische facturering, worden gemaakt, beheerd en gehost in RCS.</span><span class="sxs-lookup"><span data-stu-id="81193-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="81193-116">Wanneer de resources gereed zijn, worden ze gepubliceerd in de service voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="81193-117">Zie [Wettelijke services](https://marketing.configure.global.dynamics.com/) voor registratie bij RCS.</span><span class="sxs-lookup"><span data-stu-id="81193-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="81193-118">Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie over RCS</span><span class="sxs-lookup"><span data-stu-id="81193-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="81193-119">Integratie met Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="81193-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="81193-120">Voordat u RCS kunt gebruiken voor het configureren van elektronische facturen, moet u RCS zo configureren dat communicatie met Elektronische facturering is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="81193-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="81193-121">U voltooit deze configuratie op het tabblad **Elektronische facturering** van de pagina **Parameters voor elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="81193-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="81193-122">Service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="81193-122">Service endpoint</span></span>

<span data-ttu-id="81193-123">Elektronische facturering is beschikbaar in verschillende Azure-datacentergeografieën.</span><span class="sxs-lookup"><span data-stu-id="81193-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="81193-124">In de volgende tabel wordt de beschikbaarheid per regio vermeld.</span><span class="sxs-lookup"><span data-stu-id="81193-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="81193-125">Geografie Azure-datacenter</span><span class="sxs-lookup"><span data-stu-id="81193-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="81193-126">Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="81193-126">United States</span></span>              |
| <span data-ttu-id="81193-127">Europa</span><span class="sxs-lookup"><span data-stu-id="81193-127">Europe</span></span>                     |
| <span data-ttu-id="81193-128">Verenigd Koninkrijk</span><span class="sxs-lookup"><span data-stu-id="81193-128">United Kingdom</span></span>             |
| <span data-ttu-id="81193-129">Azië</span><span class="sxs-lookup"><span data-stu-id="81193-129">Asia</span></span>                       |

### <a name="service-environments"></a><span data-ttu-id="81193-130">Serviceomgevingen</span><span class="sxs-lookup"><span data-stu-id="81193-130">Service environments</span></span>

<span data-ttu-id="81193-131">Serviceomgevingen zijn logische partities die worden gemaakt om de uitvoering van de elektronische factureringsfuncties in Elektronische facturering te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="81193-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="81193-132">De beveiligingsrechten en digitale certificaten en de governance (toegangsmachtigingen) moeten worden geconfigureerd op het niveau van de serviceomgeving.</span><span class="sxs-lookup"><span data-stu-id="81193-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="81193-133">Klanten kunnen net zo veel serviceomgevingen maken als zij willen.</span><span class="sxs-lookup"><span data-stu-id="81193-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="81193-134">Alle serviceomgevingen die door een klant worden gemaakt, zijn onafhankelijk van elkaar.</span><span class="sxs-lookup"><span data-stu-id="81193-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="81193-135">Serviceomgevingen moeten worden gemaakt en onderhouden in RCS.</span><span class="sxs-lookup"><span data-stu-id="81193-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="81193-136">Wanneer de serviceomgevingen gereed zijn, moeten ze worden gepubliceerd in Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="81193-137">Status van de serviceomgeving</span><span class="sxs-lookup"><span data-stu-id="81193-137">Service environment status</span></span>

<span data-ttu-id="81193-138">Serviceomgevingen kunnen worden beheerd via de status.</span><span class="sxs-lookup"><span data-stu-id="81193-138">Service environments can be managed through status.</span></span> <span data-ttu-id="81193-139">De mogelijke opties zijn:</span><span class="sxs-lookup"><span data-stu-id="81193-139">The possible options are:</span></span>

- <span data-ttu-id="81193-140">**Niet gepubliceerd**: de omgeving is gemaakt, maar nog niet gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="81193-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="81193-141">**Gepubliceerd**: de omgeving is gepubliceerd in Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="81193-142">**Gewijzigd**: de kenmerken van een gepubliceerde omgeving zijn gewijzigd, maar de wijzigingen zijn nog niet gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="81193-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="81193-143">Klantgeheimen</span><span class="sxs-lookup"><span data-stu-id="81193-143">Customer secrets</span></span>

<span data-ttu-id="81193-144">De service voor elektronische facturering is verantwoordelijk voor het opslaan van al uw bedrijfsgegevens in de Azure-resources die uw bedrijf bezit.</span><span class="sxs-lookup"><span data-stu-id="81193-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="81193-145">Om er zeker van te zijn dat de service correct werkt en dat alle bedrijfsgegevens die nodig zijn voor en die worden gegenereerd door Elektronische facturering correct worden gebruikt, moet u twee hoofd Azure-resources maken:</span><span class="sxs-lookup"><span data-stu-id="81193-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="81193-146">Een Azure-opslagaccount (Blob-opslag) waarin elektronische facturen worden opgeslagen</span><span class="sxs-lookup"><span data-stu-id="81193-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="81193-147">Een Azure Key Vault voor de opslag van certificaten en de URI (Uniform Resource Identifier) van het opslagaccount</span><span class="sxs-lookup"><span data-stu-id="81193-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="81193-148">Een speciale Key Vault en een opslagaccount van de klant moeten specifiek worden toegewezen voor gebruik met Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="81193-149">Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="81193-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="81193-150">Om de status van uw Key Vault te bewaken en waarschuwingen te ontvangen, configureert u Azure Monitor voor Key Vault.</span><span class="sxs-lookup"><span data-stu-id="81193-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="81193-151">Als u logboekregistratie inschakelt voor Key Vault, kunt u controleren hoe, wanneer en door wie uw Key Vaults worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="81193-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="81193-152">Meer informatie over dit onderwerp vindt u in [Bewaking en waarschuwingen ontvangen voor Azure Key Vault](/azure/key-vault/general/alert) en [Logboekregistratie inschakelen voor Key Vault](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="81193-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="81193-153">Het wordt aangeraden om de geheimen regelmatig te wisselen.</span><span class="sxs-lookup"><span data-stu-id="81193-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="81193-154">Zie de [Documentatie voor geheimen](/azure/key-vault/secrets/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="81193-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="81193-155">Gebruikers</span><span class="sxs-lookup"><span data-stu-id="81193-155">Users</span></span>

<span data-ttu-id="81193-156">Elke serviceomgeving moet een lijst maken met de gebruikers die verbinding kunnen maken vanuit Dynamics 365 Finance en Dynamics 365 Supply Chain Management in Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="81193-157">Publicatie</span><span class="sxs-lookup"><span data-stu-id="81193-157">Publication</span></span>

<span data-ttu-id="81193-158">Serviceomgevingen moeten worden gepubliceerd in Elektronische facturering voordat ze kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="81193-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="81193-159">Alleen gepubliceerde omgevingen kunnen worden gebruikt door Finance en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="81193-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="81193-160">Daarnaast moet een serviceomgeving worden gepubliceerd voordat updates van de kenmerken van kracht worden op de elektronische factureringsservice.</span><span class="sxs-lookup"><span data-stu-id="81193-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="81193-161">Verbonden toepassingen</span><span class="sxs-lookup"><span data-stu-id="81193-161">Connected applications</span></span>

<span data-ttu-id="81193-162">Verbonden toepassingen zijn de exemplaren van Finance en Supply Chain Management die u mogelijk wilt bereiken via RCS.</span><span class="sxs-lookup"><span data-stu-id="81193-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="81193-163">Naast de URL van de toepassing en de tenant ervan, bevat een verbonden toepassing de referenties waarmee RCS verbinding kan maken met de omgeving.</span><span class="sxs-lookup"><span data-stu-id="81193-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="81193-164">Via de verbonden toepassingen kunt u een gedeelte van de elektronische factureringsfunctie in Finance en Supply Chain Management configureren om de gehele elektronische factureringsfunctie te laten werken.</span><span class="sxs-lookup"><span data-stu-id="81193-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="81193-165">Finance en Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="81193-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="81193-166">Integratie met Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="81193-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="81193-167">Voordat u Finance en Supply Chain Management kunt gebruiken om elektronische facturen uit te geven via Elektronische facturering, moet Elektronische facturering worden geconfigureerd zodat kan worden gecommuniceerd met de service.</span><span class="sxs-lookup"><span data-stu-id="81193-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="81193-168">Integratiefunctie van Elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="81193-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="81193-169">Als u de communicatie tussen Finance en Supply Chain Management en Elektronische facturering wilt inschakelen, moet u de functie **Integratie van Elektronische facturering** in de werkruimte **Functiebeheer** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="81193-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="81193-170">Service-eindpunt</span><span class="sxs-lookup"><span data-stu-id="81193-170">Service endpoint</span></span>

<span data-ttu-id="81193-171">Het service-eindpunt is de URL waar Elektronische facturering zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="81193-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="81193-172">Voordat elektronische facturen kunnen worden uitgegeven, moet het service-eindpunt worden geconfigureerd in Finance en Supply Chain Management om communicatie met de service mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="81193-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="81193-173">Om het service-eindpunt te configureren, gaat u naar **Organisatiebeheer \> Instellen \> Parameter voor elektronisch document** en daarna voert u op het tabblad **Indieningsservices** in het veld **URL van Elektronische facturering** de URL in, zoals wordt beschreven in de tabel uit de sectie **Service-eindpunt**.</span><span class="sxs-lookup"><span data-stu-id="81193-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="81193-174">Omgevingen</span><span class="sxs-lookup"><span data-stu-id="81193-174">Environments</span></span>

<span data-ttu-id="81193-175">De omgevingsnaam die wordt ingevoerd in Finance en Supply Chain Management, verwijst naar de naam van de omgeving die in RCS wordt gemaakt en gepubliceerd naar Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="81193-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="81193-176">De omgeving moet worden geconfigureerd op het tabblad **Indieningsservices** van de pagina **Parameter voor elektronisch document**, zodat elk verzoek om elektronische facturen uit te geven de omgeving bevat waarin Elektronische facturering kan bepalen welke functie voor elektronische facturering het verzoek moet verwerken.</span><span class="sxs-lookup"><span data-stu-id="81193-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81193-177">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="81193-177">Additional resources</span></span>

- [<span data-ttu-id="81193-178">Elektronische facturen configureren in RCS</span><span class="sxs-lookup"><span data-stu-id="81193-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="81193-179">Elektronische facturen uitgeven in Finance en Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="81193-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
