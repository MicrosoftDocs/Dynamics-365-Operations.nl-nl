---
title: Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen
description: In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936825"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="7df96-103">Ondersteuning voor een CDN (netwerk voor contentlevering) toevoegen</span><span class="sxs-lookup"><span data-stu-id="7df96-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7df96-104">In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="7df96-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="7df96-105">Wanneer u een e-commerce-omgeving instelt in Dynamics 365 Commerce, kunt u deze configureren om met uw CDN-service te werken.</span><span class="sxs-lookup"><span data-stu-id="7df96-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="7df96-106">Het aangepaste domein kan tijdens het inrichtingsproces voor uw e-commerce-omgeving worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="7df96-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="7df96-107">U kunt ook een serviceaanvraag gebruiken om deze in te stellen nadat het inrichtingsproces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="7df96-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="7df96-108">Het inrichtingsproces voor de e-commerce-omgeving genereert een hostnaam die aan de omgeving wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7df96-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="7df96-109">Deze hostnaam heeft de volgende indeling, waarbij \<*e-commerce-tenant-name*\> de naam van uw omgeving is:</span><span class="sxs-lookup"><span data-stu-id="7df96-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="7df96-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="7df96-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="7df96-111">De hostnaam of het eindpunt dat tijdens het inrichtingsproces wordt gegenereerd, ondersteunt alleen een Secure Sockets Layer-certificaat (SSL) voor \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="7df96-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="7df96-112">SSL wordt niet ondersteund voor aangepaste domeinen.</span><span class="sxs-lookup"><span data-stu-id="7df96-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="7df96-113">Daarom moet u SSL beëindigen voor aangepaste domeinen in uw CDN en verkeer doorsturen van de CDN naar de hostnaam of het eindpunt dat door Commerce wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="7df96-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="7df96-114">Bovendien worden de *statische* onderdelen (Javascript- of \[CSS\]-bestanden (Cascading Style Sheets)) van Commerce verzonden vanaf het eindpunt dat door Commerce wordt gegenereerd (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="7df96-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="7df96-115">De statische onderdelen kunnen alleen in de cache worden geplaatst, als de hostnaam of het eindpunt dat door Commerce gegenereerd wordt, achter het CDN wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="7df96-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="7df96-116">SSL instellen</span><span class="sxs-lookup"><span data-stu-id="7df96-116">Set up SSL</span></span>

<span data-ttu-id="7df96-117">Nadat u uw Commerce-omgeving hebt ingericht met het aangepaste domein dat is opgegeven of nadat u het aangepaste domein voor uw omgeving hebt opgegeven met behulp van een serviceaanvraag, moet u de DNS-wijzigingen samen met het onboardingteam voor Commerce plannen.</span><span class="sxs-lookup"><span data-stu-id="7df96-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="7df96-118">Zoals eerder is vermeld, ondersteunt de gegenereerde hostnaam of het eindpunt alleen een SSL-certificaat voor \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="7df96-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="7df96-119">SSL wordt niet ondersteund voor aangepaste domeinen.</span><span class="sxs-lookup"><span data-stu-id="7df96-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="7df96-120">CDN-services</span><span class="sxs-lookup"><span data-stu-id="7df96-120">CDN services</span></span>

<span data-ttu-id="7df96-121">Een CDN-service kan met een Commerce-omgeving worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7df96-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="7df96-122">Hieronder vindt u twee voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="7df96-122">Here are two examples:</span></span>

- <span data-ttu-id="7df96-123">**Microsoft Azure Front Door Service**: de Azure CDN-oplossing.</span><span class="sxs-lookup"><span data-stu-id="7df96-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="7df96-124">Meer informatie over de Azure Front Door Service vindt u in [Documentatie bij Azure Front Door Service](/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="7df96-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](/azure/frontdoor/).</span></span>
- <span data-ttu-id="7df96-125">**Akamai Dynamic Site Accelerator**: zie voor meer informatie [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="7df96-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="7df96-126">CDN-instellingen</span><span class="sxs-lookup"><span data-stu-id="7df96-126">CDN setup</span></span>

<span data-ttu-id="7df96-127">Het CDN-installatieproces bestaat uit de volgende algemene stappen:</span><span class="sxs-lookup"><span data-stu-id="7df96-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="7df96-128">Een front-endhost toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7df96-128">Add a front-end host.</span></span>
1. <span data-ttu-id="7df96-129">Een back-endgroep configureren.</span><span class="sxs-lookup"><span data-stu-id="7df96-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="7df96-130">Stel regels voor doorsturen in.</span><span class="sxs-lookup"><span data-stu-id="7df96-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="7df96-131">Een front-endhost toevoegen</span><span class="sxs-lookup"><span data-stu-id="7df96-131">Add a front-end host</span></span>

<span data-ttu-id="7df96-132">U kunt elke CDN-service gebruiken, maar voor het voorbeeld in dit onderwerp wordt de Azure Front Door Service gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7df96-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="7df96-133">Voor informatie over het instellen van de Azure Front Door Service raadpleegt u [Beknopte gids voor Front Door Service voor een algemene webtoepassing met hoge beschikbaarheid](/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="7df96-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="7df96-134">Een back-endpool configureren in Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="7df96-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="7df96-135">Volg deze stappen om een back-endpool te configureren in Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="7df96-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="7df96-136">Voeg **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** toe aan een back-endgroep als een aangepaste host met een koptekst voor de back-endhost die hetzelfde is als **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="7df96-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="7df96-137">Laat de standaardwaarden staan onder **Taakverdeling**.</span><span class="sxs-lookup"><span data-stu-id="7df96-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="7df96-138">Schakel statuscontroles voor de back-endgroep uit.</span><span class="sxs-lookup"><span data-stu-id="7df96-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="7df96-139">In de volgende afbeelding ziet u het dialoogvenster **Een back-end toevoegen** in de Azure Front Door Service met de naam van de back-endhost ingevuld.</span><span class="sxs-lookup"><span data-stu-id="7df96-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Het dialoogvenster Een backend-groep toevoegen](./media/CDN_BackendPool.png)

<span data-ttu-id="7df96-141">In de volgende afbeelding ziet u het dialoogvenster **Een back-endgroep toevoegen** in de Azure Front Door Service met de standaardwaarden voor taakverdeling.</span><span class="sxs-lookup"><span data-stu-id="7df96-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Dialoogvenster Een back-endgroep toevoegen (vervolg)](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="7df96-143">Zorg ervoor dat u **Statusprobes** uitschakelt bij het instellen van uw eigen Azure Front Door Service voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="7df96-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="7df96-144">Regels in de Azure Front Door Service instellen</span><span class="sxs-lookup"><span data-stu-id="7df96-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="7df96-145">Voer de volgende stappen uit om een regel voor doorsturen in te stellen in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="7df96-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="7df96-146">Voeg een regel voor doorsturen toe.</span><span class="sxs-lookup"><span data-stu-id="7df96-146">Add a routing rule.</span></span>
1. <span data-ttu-id="7df96-147">Voer in het veld **Naam** de tekst **standaard** in.</span><span class="sxs-lookup"><span data-stu-id="7df96-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="7df96-148">Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.</span><span class="sxs-lookup"><span data-stu-id="7df96-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="7df96-149">Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.</span><span class="sxs-lookup"><span data-stu-id="7df96-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="7df96-150">Voer onder **Af te stemmen patronen** in het bovenste veld **/\*** in.</span><span class="sxs-lookup"><span data-stu-id="7df96-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="7df96-151">Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.</span><span class="sxs-lookup"><span data-stu-id="7df96-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="7df96-152">Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="7df96-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="7df96-153">Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**.</span><span class="sxs-lookup"><span data-stu-id="7df96-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="7df96-154">Stel de optie **URL herschrijven** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="7df96-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="7df96-155">Stel de optie **Caching** in op **Uitgeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="7df96-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="7df96-156">Als het domein dat u gaat gebruiken al actief en live is, maakt u een ondersteuningsticket vanuit de tegel **Ondersteuning** in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) om hulp te krijgen bij uw volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="7df96-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="7df96-157">Zie [Ondersteuning voor Finance and Operations-apps of Lifecycle Services (LCS) krijgen voor meer informatie](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="7df96-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="7df96-158">Als uw domein nieuw is en geen reeds bestaand live domein is, kunt u uw aangepaste domein toevoegen aan de configuratie voor de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="7df96-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="7df96-159">Hierdoor wordt webverkeer via het Azure Front Door-exemplaar naar uw site geleid.</span><span class="sxs-lookup"><span data-stu-id="7df96-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="7df96-160">Als u het aangepaste domein wilt toevoegen (bijvoorbeeld `www.fabrikam.com`), moet u een canonieke naam (CNAME) voor het domein configureren.</span><span class="sxs-lookup"><span data-stu-id="7df96-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="7df96-161">In de volgende afbeelding ziet u het dialoogvenster **CNAME-configuratie** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="7df96-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialoogvenster CNAME-configuratie](./media/CNAME_Configuration.png)

<span data-ttu-id="7df96-163">U kunt de Azure Front Door Service gebruiken om het certificaat te beheren of u kunt uw eigen certificaat voor het aangepaste domein gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7df96-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="7df96-164">In de volgende afbeelding ziet u het dialoogvenster **Aangepast domein HTTPS** in de Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="7df96-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialoogvenster Aangepast domein HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="7df96-166">Zie voor gedetailleerde instructies voor het toevoegen van een aangepast domein aan uw Azure Front Door [Een aangepast domein toevoegen aan uw Front Door](/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="7df96-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="7df96-167">Uw CDN is nu correct geconfigureerd voor gebruik met uw Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="7df96-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7df96-168">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7df96-168">Additional resources</span></span>

[<span data-ttu-id="7df96-169">Implementatieopties voor netwerk voor contentlevering</span><span class="sxs-lookup"><span data-stu-id="7df96-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]