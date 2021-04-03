---
title: Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen
description: In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582714"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="bff8d-103">Ondersteuning voor een CDN (netwerk voor contentlevering) toevoegen</span><span class="sxs-lookup"><span data-stu-id="bff8d-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bff8d-104">In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="bff8d-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="bff8d-105">Wanneer u een e-commerce-omgeving instelt in Dynamics 365 Commerce, kunt u deze configureren om met uw CDN-service te werken.</span><span class="sxs-lookup"><span data-stu-id="bff8d-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="bff8d-106">Het aangepaste domein kan tijdens het inrichtingsproces voor uw e-commerce-omgeving worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="bff8d-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="bff8d-107">U kunt ook een serviceaanvraag gebruiken om deze in te stellen nadat het inrichtingsproces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="bff8d-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="bff8d-108">Het inrichtingsproces voor de e-commerce-omgeving genereert een hostnaam die aan de omgeving wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="bff8d-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="bff8d-109">Deze hostnaam heeft de volgende indeling, waarbij \<*e-commerce-tenant-name*\> de naam van uw omgeving is:</span><span class="sxs-lookup"><span data-stu-id="bff8d-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="bff8d-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="bff8d-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="bff8d-111">De hostnaam of het eindpunt dat tijdens het inrichtingsproces wordt gegenereerd, ondersteunt alleen een Secure Sockets Layer-certificaat (SSL) voor \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="bff8d-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="bff8d-112">SSL wordt niet ondersteund voor aangepaste domeinen.</span><span class="sxs-lookup"><span data-stu-id="bff8d-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="bff8d-113">Daarom moet u SSL beëindigen voor aangepaste domeinen in uw CDN en verkeer doorsturen van de CDN naar de hostnaam of het eindpunt dat door Commerce wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="bff8d-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="bff8d-114">Bovendien worden de *statische* onderdelen (Javascript- of \[CSS\]-bestanden (Cascading Style Sheets)) van Commerce verzonden vanaf het eindpunt dat door Commerce wordt gegenereerd (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="bff8d-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="bff8d-115">De statische onderdelen kunnen alleen in de cache worden geplaatst, als de hostnaam of het eindpunt dat door Commerce gegenereerd wordt, achter het CDN wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="bff8d-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="bff8d-116">SSL instellen</span><span class="sxs-lookup"><span data-stu-id="bff8d-116">Set up SSL</span></span>

<span data-ttu-id="bff8d-117">Om ervoor te zorgen dat de SSL-configuratie wordt ingesteld en dat de statische onderdelen in de cache worden opgeslagen, moet u uw CDN zo configureren dat dit is gekoppeld aan de hostnaam die door Commerce wordt gegenereerd voor uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="bff8d-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="bff8d-118">U moet ook het volgende patroon in cache opslaan, alleen voor statische onderdelen:</span><span class="sxs-lookup"><span data-stu-id="bff8d-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="bff8d-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="bff8d-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="bff8d-120">Nadat u uw Commerce-omgeving hebt ingericht met het aangepaste domein dat is opgegeven of nadat u het aangepaste domein voor uw omgeving hebt opgegeven met behulp van een serviceaanvraag, wijst u uw aangepaste domein toe aan de hostnaam of het eindpunt dat door Commerce is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="bff8d-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="bff8d-121">Zoals eerder is vermeld, ondersteunt de gegenereerde hostnaam of het eindpunt alleen een SSL-certificaat voor \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="bff8d-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="bff8d-122">SSL wordt niet ondersteund voor aangepaste domeinen.</span><span class="sxs-lookup"><span data-stu-id="bff8d-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="bff8d-123">CDN-services</span><span class="sxs-lookup"><span data-stu-id="bff8d-123">CDN services</span></span>

<span data-ttu-id="bff8d-124">Een CDN-service kan met een Commerce-omgeving worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bff8d-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="bff8d-125">Hieronder vindt u twee voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="bff8d-125">Here are two examples:</span></span>

- <span data-ttu-id="bff8d-126">**Microsoft Azure Front Door Service**: de Azure CDN-oplossing.</span><span class="sxs-lookup"><span data-stu-id="bff8d-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="bff8d-127">Meer informatie over de Azure Front Door Service vindt u in [Documentatie bij Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="bff8d-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="bff8d-128">**Akamai Dynamic Site Accelerator**: zie voor meer informatie [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="bff8d-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="bff8d-129">CDN-instellingen</span><span class="sxs-lookup"><span data-stu-id="bff8d-129">CDN setup</span></span>

<span data-ttu-id="bff8d-130">Het CDN-installatieproces bestaat uit de volgende algemene stappen:</span><span class="sxs-lookup"><span data-stu-id="bff8d-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="bff8d-131">Een front-endhost toevoegen.</span><span class="sxs-lookup"><span data-stu-id="bff8d-131">Add a front-end host.</span></span>
1. <span data-ttu-id="bff8d-132">Een back-endpool configureren.</span><span class="sxs-lookup"><span data-stu-id="bff8d-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="bff8d-133">Regels voor routering en caching instellen.</span><span class="sxs-lookup"><span data-stu-id="bff8d-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="bff8d-134">Een front-endhost toevoegen</span><span class="sxs-lookup"><span data-stu-id="bff8d-134">Add a front-end host</span></span>

<span data-ttu-id="bff8d-135">U kunt elke CDN-service gebruiken, maar voor het voorbeeld in dit onderwerp wordt de Azure Front Door Service gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bff8d-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="bff8d-136">Voor informatie over het instellen van de Azure Front Door Service raadpleegt u [Beknopte gids voor Front Door Service voor een algemene webtoepassing met hoge beschikbaarheid](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="bff8d-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="bff8d-137">Een back-endpool configureren in Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="bff8d-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="bff8d-138">Volg deze stappen om een back-endpool te configureren in Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="bff8d-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="bff8d-139">Voeg **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** toe aan een back-endpool als een aangepaste host met een lege koptekst voor de back-endhost.</span><span class="sxs-lookup"><span data-stu-id="bff8d-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="bff8d-140">Laat de standaardwaarden staan onder **Taakverdeling**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="bff8d-141">In de volgende afbeelding ziet u het dialoogvenster **Een backend toevoegen** in de Azure Front Door Service met de naam van de back-endhost ingevuld.</span><span class="sxs-lookup"><span data-stu-id="bff8d-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Het dialoogvenster Een backend-groep toevoegen](./media/CDN_BackendPool.png)

<span data-ttu-id="bff8d-143">In de volgende afbeelding ziet u het dialoogvenster **Een back-endpool toevoegen** in de Azure Front Door Service met de standaardwaarden voor taakverdeling.</span><span class="sxs-lookup"><span data-stu-id="bff8d-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Dialoogvenster Een back-endpool toevoegen (vervolg)](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="bff8d-145">Regels in de Azure Front Door Service instellen</span><span class="sxs-lookup"><span data-stu-id="bff8d-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="bff8d-146">Voer de volgende stappen uit om een routeringsregel in te stellen in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="bff8d-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="bff8d-147">Voeg een routeringregel toe.</span><span class="sxs-lookup"><span data-stu-id="bff8d-147">Add a routing rule.</span></span>
1. <span data-ttu-id="bff8d-148">Voer in het veld **Naam** de tekst **standaard** in.</span><span class="sxs-lookup"><span data-stu-id="bff8d-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="bff8d-149">Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="bff8d-150">Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.</span><span class="sxs-lookup"><span data-stu-id="bff8d-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="bff8d-151">Voer onder **Af te stemmen patronen** in het bovenste veld **/\*** in.</span><span class="sxs-lookup"><span data-stu-id="bff8d-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="bff8d-152">Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="bff8d-153">Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="bff8d-154">Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="bff8d-155">Stel de optie **URL herschrijven** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="bff8d-156">Stel de optie **Caching** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="bff8d-157">Voer de volgende stappen uit om een cachingregel in te stellen in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="bff8d-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="bff8d-158">Voeg een cachingregel toe.</span><span class="sxs-lookup"><span data-stu-id="bff8d-158">Add a caching rule.</span></span>
1. <span data-ttu-id="bff8d-159">Voer in het veld **Naam** de tekst **statics** in.</span><span class="sxs-lookup"><span data-stu-id="bff8d-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="bff8d-160">Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="bff8d-161">Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.</span><span class="sxs-lookup"><span data-stu-id="bff8d-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="bff8d-162">Voer onder **Af te stemmen patronen** in het bovenste veld **/\_msdyn365/\_scnr/\*** in.</span><span class="sxs-lookup"><span data-stu-id="bff8d-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="bff8d-163">Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="bff8d-164">Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="bff8d-165">Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="bff8d-166">Stel de optie **URL herschrijven** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="bff8d-167">Stel de optie **Caching** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="bff8d-168">Selecteer in het veld **Cachegedrag queryreeks** de optie **Elke unieke URL in cache plaatsen**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="bff8d-169">Selecteer de optie **Ingeschakeld** in de veldgroep **Dynamische compressie**.</span><span class="sxs-lookup"><span data-stu-id="bff8d-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="bff8d-170">In de volgende afbeelding ziet u het dialoogvenster **Een regel toevoegen** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="bff8d-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Het dialoogvenster Regel toevoegen](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="bff8d-172">Als het domein dat u gaat gebruiken al actief en live is, maakt u een ondersteuningsticket vanuit de tegel **Ondersteuning** in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) om hulp te krijgen bij uw volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="bff8d-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="bff8d-173">Zie [Ondersteuning voor Finance and Operations-apps of Lifecycle Services (LCS) krijgen voor meer informatie](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="bff8d-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="bff8d-174">Als uw domein nieuw is en geen reeds bestaand live domein is, kunt u uw aangepaste domein toevoegen aan de configuratie voor de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="bff8d-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="bff8d-175">Hierdoor wordt webverkeer via het Azure Front Door-exemplaar naar uw site geleid.</span><span class="sxs-lookup"><span data-stu-id="bff8d-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="bff8d-176">Als u het aangepaste domein wilt toevoegen (bijvoorbeeld `www.fabrikam.com`), moet u een canonieke naam (CNAME) voor het domein configureren.</span><span class="sxs-lookup"><span data-stu-id="bff8d-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="bff8d-177">In de volgende afbeelding ziet u het dialoogvenster **CNAME-configuratie** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="bff8d-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialoogvenster CNAME-configuratie](./media/CNAME_Configuration.png)

<span data-ttu-id="bff8d-179">U kunt de Azure Front Door Service gebruiken om het certificaat te beheren of u kunt uw eigen certificaat voor het aangepaste domein gebruiken.</span><span class="sxs-lookup"><span data-stu-id="bff8d-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="bff8d-180">In de volgende afbeelding ziet u het dialoogvenster **Aangepast domein HTTPS** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="bff8d-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialoogvenster Aangepast domein HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="bff8d-182">Zie voor gedetailleerde instructies voor het toevoegen van een aangepast domein aan uw Azure Front Door [Een aangepast domein toevoegen aan uw Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="bff8d-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="bff8d-183">Uw CDN is nu correct geconfigureerd voor gebruik met uw Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="bff8d-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bff8d-184">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="bff8d-184">Additional resources</span></span>

[<span data-ttu-id="bff8d-185">Implementatieopties voor netwerk voor contentlevering</span><span class="sxs-lookup"><span data-stu-id="bff8d-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
