---
title: Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen
description: In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: febef3bcc06dc1b5868a0decebee33d76110c505
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533339"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="81488-103">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="81488-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="81488-104">In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="81488-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="81488-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="81488-105">Overview</span></span>

<span data-ttu-id="81488-106">Wanneer u een e-commerce-omgeving instelt in Dynamics 365 Commerce, kunt u deze configureren om met uw CDN-service te werken.</span><span class="sxs-lookup"><span data-stu-id="81488-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="81488-107">Het aangepaste domein kan tijdens het inrichtingsproces voor uw e-commerce-omgeving worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="81488-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="81488-108">U kunt ook een serviceaanvraag gebruiken om deze in te stellen nadat het inrichtingsproces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="81488-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="81488-109">Het inrichtingsproces voor de e-commerce-omgeving genereert een hostnaam die aan de omgeving wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="81488-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="81488-110">Deze hostnaam heeft de volgende indeling, waarbij *e-commerce-tenant-name* de naam van uw omgeving is:</span><span class="sxs-lookup"><span data-stu-id="81488-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="81488-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="81488-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="81488-112">De hostnaam of het eindpunt dat tijdens het inrichtingsproces wordt gegenereerd, ondersteunt alleen een Secure Sockets Layer-certificaat (SSL) voor \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="81488-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="81488-113">SSL wordt niet ondersteund voor aangepaste domeinen.</span><span class="sxs-lookup"><span data-stu-id="81488-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="81488-114">Daarom moet u SSL beëindigen voor aangepaste domeinen in uw CDN en verkeer doorsturen van de CDN naar de hostnaam of het eindpunt dat door Commerce wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="81488-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="81488-115">Bovendien worden de *statische* onderdelen (Javascript- of \[CSS\]-bestanden (Cascading Style Sheets)) van Commerce verzonden vanaf het eindpunt dat door Commerce wordt gegenereerd (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="81488-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="81488-116">De statische onderdelen kunnen alleen in de cache worden geplaatst, als de hostnaam of het eindpunt dat door Commerce gegenereerd wordt, achter het CDN wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="81488-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="81488-117">SSL instellen</span><span class="sxs-lookup"><span data-stu-id="81488-117">Set up SSL</span></span>

<span data-ttu-id="81488-118">Om ervoor te zorgen dat de SSL-configuratie wordt ingesteld en dat de statische onderdelen in de cache worden opgeslagen, moet u uw CDN zo configureren dat dit is gekoppeld aan de hostnaam die door Commerce wordt gegenereerd voor uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="81488-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="81488-119">U moet ook het volgende patroon in cache opslaan, alleen voor statische onderdelen:</span><span class="sxs-lookup"><span data-stu-id="81488-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="81488-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="81488-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="81488-121">Nadat u uw Commerce-omgeving hebt ingericht met het aangepaste domein dat is opgegeven of nadat u het aangepaste domein voor uw omgeving hebt opgegeven met behulp van een serviceaanvraag, wijst u uw aangepaste domein toe aan de hostnaam of het eindpunt dat door Commerce is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="81488-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="81488-122">Zoals eerder is vermeld, ondersteunt de gegenereerde hostnaam of het eindpunt alleen een SSL-certificaat voor \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="81488-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="81488-123">SSL wordt niet ondersteund voor aangepaste domeinen.</span><span class="sxs-lookup"><span data-stu-id="81488-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="81488-124">CDN-services</span><span class="sxs-lookup"><span data-stu-id="81488-124">CDN services</span></span>

<span data-ttu-id="81488-125">Een CDN-service kan met een Commerce-omgeving worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="81488-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="81488-126">Hieronder vindt u twee voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="81488-126">Here are two examples:</span></span>

- <span data-ttu-id="81488-127">**Microsoft Azure Front Door Service**: de Azure CDN-oplossing.</span><span class="sxs-lookup"><span data-stu-id="81488-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="81488-128">Meer informatie over de Azure Front Door Service vindt u in [Documentatie bij Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="81488-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="81488-129">**Akamai Dynamic Site Accelerator**: zie voor meer informatie [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="81488-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="81488-130">CDN-instellingen</span><span class="sxs-lookup"><span data-stu-id="81488-130">CDN setup</span></span>

<span data-ttu-id="81488-131">Het CDN-installatieproces bestaat uit de volgende algemene stappen:</span><span class="sxs-lookup"><span data-stu-id="81488-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="81488-132">Een front-endhost toevoegen.</span><span class="sxs-lookup"><span data-stu-id="81488-132">Add a front-end host.</span></span>
1. <span data-ttu-id="81488-133">Een back-endgroep configureren.</span><span class="sxs-lookup"><span data-stu-id="81488-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="81488-134">Regels voor routering en caching instellen.</span><span class="sxs-lookup"><span data-stu-id="81488-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="81488-135">Een front-endhost toevoegen</span><span class="sxs-lookup"><span data-stu-id="81488-135">Add a front-end host</span></span>

<span data-ttu-id="81488-136">U kunt elke CDN-service gebruiken, maar voor het voorbeeld in dit onderwerp wordt de Azure Front Door Service gebruikt.</span><span class="sxs-lookup"><span data-stu-id="81488-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="81488-137">Voor informatie over het instellen van de Azure Front Door Service raadpleegt u [Beknopte gids voor Front Door Service voor een algemene webtoepassing met hoge beschikbaarheid](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="81488-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="81488-138">Een back-endgroep configureren in Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="81488-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="81488-139">Volg deze stappen om een back-endgroep te configureren in Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="81488-140">Voeg **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** toe aan een back-endgroep als een aangepaste host met een lege koptekst voor de back-endhost.</span><span class="sxs-lookup"><span data-stu-id="81488-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="81488-141">Voer onder **Statusprobes** in het veld **Pad** **/keepalive** in.</span><span class="sxs-lookup"><span data-stu-id="81488-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="81488-142">Voer in het veld **Intervallen (seconden)** **255** in.</span><span class="sxs-lookup"><span data-stu-id="81488-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="81488-143">Laat de standaardwaarden staan onder **Taakverdeling**.</span><span class="sxs-lookup"><span data-stu-id="81488-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="81488-144">In de volgende afbeelding ziet u het dialoogvenster **Een backend-groep toevoegen** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Het dialoogvenster Een backend-groep toevoegen](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="81488-146">Regels in de Azure Front Door Service instellen</span><span class="sxs-lookup"><span data-stu-id="81488-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="81488-147">Voer de volgende stappen uit om een routeringsregel in te stellen in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="81488-148">Voeg een routeringregel toe.</span><span class="sxs-lookup"><span data-stu-id="81488-148">Add a routing rule.</span></span>
1. <span data-ttu-id="81488-149">Voer in het veld **Naam** de tekst **standaard** in.</span><span class="sxs-lookup"><span data-stu-id="81488-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="81488-150">Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.</span><span class="sxs-lookup"><span data-stu-id="81488-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="81488-151">Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.</span><span class="sxs-lookup"><span data-stu-id="81488-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="81488-152">Voer onder **Af te stemmen patronen** in het bovenste veld **/\*** in.</span><span class="sxs-lookup"><span data-stu-id="81488-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="81488-153">Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.</span><span class="sxs-lookup"><span data-stu-id="81488-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="81488-154">Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="81488-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="81488-155">Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**.</span><span class="sxs-lookup"><span data-stu-id="81488-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="81488-156">Stel de optie **URL herschrijven** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="81488-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="81488-157">Stel de optie **Caching** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="81488-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="81488-158">Voer de volgende stappen uit om een cachingregel in te stellen in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="81488-159">Voeg een cachingregel toe.</span><span class="sxs-lookup"><span data-stu-id="81488-159">Add a caching rule.</span></span>
1. <span data-ttu-id="81488-160">Voer in het veld **Naam** de tekst **statics** in.</span><span class="sxs-lookup"><span data-stu-id="81488-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="81488-161">Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.</span><span class="sxs-lookup"><span data-stu-id="81488-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="81488-162">Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.</span><span class="sxs-lookup"><span data-stu-id="81488-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="81488-163">Voer onder **Af te stemmen patronen** in het bovenste veld **/\_msdyn365/\_scnr/\*** in.</span><span class="sxs-lookup"><span data-stu-id="81488-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="81488-164">Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.</span><span class="sxs-lookup"><span data-stu-id="81488-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="81488-165">Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="81488-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="81488-166">Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**.</span><span class="sxs-lookup"><span data-stu-id="81488-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="81488-167">Stel de optie **URL herschrijven** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="81488-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="81488-168">Stel de optie **Caching** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="81488-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="81488-169">Selecteer in het veld **Cachegedrag queryreeks** de optie **Elke unieke URL in cache plaatsen**.</span><span class="sxs-lookup"><span data-stu-id="81488-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="81488-170">Selecteer de optie **Ingeschakeld** in de veldgroep **Dynamische compressie**.</span><span class="sxs-lookup"><span data-stu-id="81488-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="81488-171">In de volgende afbeelding ziet u het dialoogvenster **Een regel toevoegen** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Het dialoogvenster Regel toevoegen](./media/CDN_CachingRule.png)

<span data-ttu-id="81488-173">Nadat deze eerste configuratie is geïmplementeerd, moet u uw aangepaste domein toevoegen aan de configuratie voor de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="81488-174">Als u het aangepaste domein wilt toevoegen (bijvoorbeeld `www.fabrikam.com`), moet u een canonieke naam (CNAME) voor het domein configureren.</span><span class="sxs-lookup"><span data-stu-id="81488-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="81488-175">In de volgende afbeelding ziet u het dialoogvenster **CNAME-configuratie** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialoogvenster CNAME-configuratie](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="81488-177">Als het domein dat u gaat gebruiken al actief en live is, neemt u contact op met de ondersteuning om dit domein als test in te schakelen met de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="81488-178">U kunt de Azure Front Door Service gebruiken om het certificaat te beheren of u kunt uw eigen certificaat voor het aangepaste domein gebruiken.</span><span class="sxs-lookup"><span data-stu-id="81488-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="81488-179">In de volgende afbeelding ziet u het dialoogvenster **Aangepast domein HTTPS** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="81488-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialoogvenster Aangepast domein HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="81488-181">Uw CDN is nu correct geconfigureerd voor gebruik met uw Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="81488-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81488-182">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="81488-182">Additional resources</span></span>

[<span data-ttu-id="81488-183">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="81488-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="81488-184">Een nieuwe e-commerce-site implementeren</span><span class="sxs-lookup"><span data-stu-id="81488-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="81488-185">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="81488-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="81488-186">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="81488-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="81488-187">Robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="81488-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="81488-188">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="81488-188">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="81488-189">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="81488-189">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="81488-190">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="81488-190">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="81488-191">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="81488-191">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="81488-192">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="81488-192">Enable location-based store detection</span></span>](enable-store-detection.md)
