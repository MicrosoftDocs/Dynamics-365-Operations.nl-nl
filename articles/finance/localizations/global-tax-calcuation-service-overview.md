---
title: Belastingberekening (Preview)
description: In dit onderwerp worden het algehele bereik en de functies voor belastingberekening uitgelegd.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184096"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="547cb-103">Belastingberekening (Preview)</span><span class="sxs-lookup"><span data-stu-id="547cb-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="547cb-104">Belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="547cb-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="547cb-105">De belastingengine kan volledig worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="547cb-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="547cb-106">De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting.</span><span class="sxs-lookup"><span data-stu-id="547cb-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="547cb-107">De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.</span><span class="sxs-lookup"><span data-stu-id="547cb-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="547cb-108">Belastingberekening wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="547cb-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="547cb-109">Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.</span><span class="sxs-lookup"><span data-stu-id="547cb-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="547cb-110">Wanneer u de service voor belastingberekening inschakelt, kunnen bepaalde bewerkingen op gerelateerde gegevens worden uitgevoerd in een ander datacentrum dan het datacentrum dat uw servicegegevens onderhoudt.</span><span class="sxs-lookup"><span data-stu-id="547cb-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="547cb-111">Controleer de [Algemene voorwaarden](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) voor u de service voor belastingberekening inschakelt.</span><span class="sxs-lookup"><span data-stu-id="547cb-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="547cb-112">Uw privacy is belangrijk voor ons.</span><span class="sxs-lookup"><span data-stu-id="547cb-112">Your privacy is important to us.</span></span> <span data-ttu-id="547cb-113">Lees onze [Privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="547cb-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="547cb-114">Belastingberekening is een op microservices gebaseerde belastingengine die exponentiële schaalbaarheid biedt.</span><span class="sxs-lookup"><span data-stu-id="547cb-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="547cb-115">Hiermee kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="547cb-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="547cb-116">Configureer Belastingberekening via Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="547cb-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="547cb-117">RCS is een verbeterde versie van de ER-ontwerper (Electronic Reporting) en is beschikbaar als zelfstandig service.</span><span class="sxs-lookup"><span data-stu-id="547cb-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="547cb-118">Configureer de belastingmatrix om automatisch belastingcodes en -tarieven te bepalen.</span><span class="sxs-lookup"><span data-stu-id="547cb-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="547cb-119">Configureer de belastingmatrix om automatisch het belastingregistratienummer te bepalen.</span><span class="sxs-lookup"><span data-stu-id="547cb-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="547cb-120">Configureer de ontwerper voor belastingberekening om formules en voorwaarden te definiëren.</span><span class="sxs-lookup"><span data-stu-id="547cb-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="547cb-121">Deel de oplossing voor belastingbepaling en -berekening voor rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="547cb-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="547cb-122">Als u de service voor belastingberekening wilt gebruiken, installeert u de invoegtoepassing voor de service vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="547cb-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="547cb-123">Voltooi vervolgens de instellingen in RCS en schakel de service voor belastingberekeningsservice in Finance en Supply Chain Management in.</span><span class="sxs-lookup"><span data-stu-id="547cb-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="547cb-124">Zie [Aan de slag met belastingservice](./global-get-started-with-tax-calculation-service.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="547cb-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="547cb-125">Beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="547cb-125">Availability</span></span>

<span data-ttu-id="547cb-126">Belastingberekening is alleen beschikbaar in sandbox-omgevingen en voor bepaalde klanten, via een openbaar preview-programma.</span><span class="sxs-lookup"><span data-stu-id="547cb-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="547cb-127">Uiteindelijk wordt deze algemeen beschikbaar voor alle klanten en in productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="547cb-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="547cb-128">Er wordt steeds nieuwe functies geleverd. Controleer daarom regelmatig de meest actuele documentatie voor meer informatie over de dekking en het bereik van ondersteunde functies.</span><span class="sxs-lookup"><span data-stu-id="547cb-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="547cb-129">Belastingberekening wordt geïmplementeerd in de volgende geografische regio's van Azure.</span><span class="sxs-lookup"><span data-stu-id="547cb-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="547cb-130">Deze wordt daarnaast geïmplementeerd in andere Azure-regio's op basis van klantbehoeften:</span><span class="sxs-lookup"><span data-stu-id="547cb-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="547cb-131">Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="547cb-131">United States</span></span>
- <span data-ttu-id="547cb-132">Europa</span><span class="sxs-lookup"><span data-stu-id="547cb-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="547cb-133">Belastingberekening ondersteunt geen on-premises implementaties van Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="547cb-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="547cb-134">Ook eerdere versies, zoals Dynamics AX 2012, worden niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="547cb-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="547cb-135">Belangrijkste functies</span><span class="sxs-lookup"><span data-stu-id="547cb-135">Feature highlights</span></span>

- <span data-ttu-id="547cb-136">Een configureerbare belastingmatrix om automatisch belasting te bepalen en te berekenen</span><span class="sxs-lookup"><span data-stu-id="547cb-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="547cb-137">Ondersteuning voor meerdere belastingregistratienummers</span><span class="sxs-lookup"><span data-stu-id="547cb-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="547cb-138">Ondersteuning van transferorders voor het bepalen en berekenen van btw</span><span class="sxs-lookup"><span data-stu-id="547cb-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="547cb-139">Ondersteuning van transferorder voor het bepalen van meerdere belastingregistratienummers</span><span class="sxs-lookup"><span data-stu-id="547cb-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="547cb-140">Ondersteunde transacties</span><span class="sxs-lookup"><span data-stu-id="547cb-140">Supported transactions</span></span>

<span data-ttu-id="547cb-141">Belastingberekening kan worden ingeschakeld per rechtspersoon en transactie.</span><span class="sxs-lookup"><span data-stu-id="547cb-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="547cb-142">De volgende transacties worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="547cb-142">The following transactions are supported:</span></span>

- <span data-ttu-id="547cb-143">Verkoopproces</span><span class="sxs-lookup"><span data-stu-id="547cb-143">Sales process</span></span>

    - <span data-ttu-id="547cb-144">Verkoopofferte</span><span class="sxs-lookup"><span data-stu-id="547cb-144">Sales quotation</span></span>
    - <span data-ttu-id="547cb-145">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="547cb-145">Sales order</span></span>
    - <span data-ttu-id="547cb-146">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="547cb-146">Confirmation</span></span>
    - <span data-ttu-id="547cb-147">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="547cb-147">Picking list</span></span>
    - <span data-ttu-id="547cb-148">Pakbon</span><span class="sxs-lookup"><span data-stu-id="547cb-148">Packing slip</span></span>
    - <span data-ttu-id="547cb-149">Verkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="547cb-149">Sales invoice</span></span>
    - <span data-ttu-id="547cb-150">Creditnota</span><span class="sxs-lookup"><span data-stu-id="547cb-150">Credit note</span></span>
    - <span data-ttu-id="547cb-151">Retourorder</span><span class="sxs-lookup"><span data-stu-id="547cb-151">Return order</span></span>
    - <span data-ttu-id="547cb-152">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="547cb-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="547cb-153">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="547cb-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="547cb-154">Aankoopproces</span><span class="sxs-lookup"><span data-stu-id="547cb-154">Purchase process</span></span>

    - <span data-ttu-id="547cb-155">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="547cb-155">Purchase order</span></span>
    - <span data-ttu-id="547cb-156">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="547cb-156">Confirmation</span></span>
    - <span data-ttu-id="547cb-157">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="547cb-157">Receipts list</span></span>
    - <span data-ttu-id="547cb-158">Ontvangst van producten</span><span class="sxs-lookup"><span data-stu-id="547cb-158">Product receipt</span></span>
    - <span data-ttu-id="547cb-159">Inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="547cb-159">Purchase invoice</span></span>
    - <span data-ttu-id="547cb-160">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="547cb-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="547cb-161">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="547cb-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="547cb-162">Creditnota</span><span class="sxs-lookup"><span data-stu-id="547cb-162">Credit note</span></span>
    - <span data-ttu-id="547cb-163">Retourorder</span><span class="sxs-lookup"><span data-stu-id="547cb-163">Return order</span></span>
    - <span data-ttu-id="547cb-164">Opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="547cb-164">Purchase requisition</span></span>
    - <span data-ttu-id="547cb-165">Diverse toeslagen voor regel van opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="547cb-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="547cb-166">Offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="547cb-166">Request for quotation</span></span>
    - <span data-ttu-id="547cb-167">Diverse toeslagen voor koptekst van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="547cb-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="547cb-168">Diverse toeslagen voor regel van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="547cb-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="547cb-169">Voorraadproces</span><span class="sxs-lookup"><span data-stu-id="547cb-169">Inventory process</span></span>

    - <span data-ttu-id="547cb-170">Transferorder – verzenden</span><span class="sxs-lookup"><span data-stu-id="547cb-170">Transfer order – ship</span></span>
    - <span data-ttu-id="547cb-171">Transferorder – ontvangen</span><span class="sxs-lookup"><span data-stu-id="547cb-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="547cb-172">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="547cb-172">Related resources</span></span>

[<span data-ttu-id="547cb-173">Aan de slag met belastingservice</span><span class="sxs-lookup"><span data-stu-id="547cb-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="547cb-174">Meerdere btw-registratienummers</span><span class="sxs-lookup"><span data-stu-id="547cb-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="547cb-175">Ondersteuning voor belastingfunctie voor transferorder</span><span class="sxs-lookup"><span data-stu-id="547cb-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="547cb-176">Uitbreiding in belastingservice maken</span><span class="sxs-lookup"><span data-stu-id="547cb-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
