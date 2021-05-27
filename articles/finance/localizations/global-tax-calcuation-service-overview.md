---
title: Belastingberekening (Preview)
description: In dit onderwerp worden het algehele bereik en de functies voor belastingberekening uitgelegd.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021927"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="eec02-103">Belastingberekening (Preview)</span><span class="sxs-lookup"><span data-stu-id="eec02-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="eec02-104">Belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="eec02-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="eec02-105">De belastingengine kan volledig worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="eec02-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="eec02-106">De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting.</span><span class="sxs-lookup"><span data-stu-id="eec02-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="eec02-107">De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.</span><span class="sxs-lookup"><span data-stu-id="eec02-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="eec02-108">Belastingberekening wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eec02-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="eec02-109">Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.</span><span class="sxs-lookup"><span data-stu-id="eec02-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="eec02-110">Belastingberekening is een op microservices gebaseerde belastingengine die exponentiële schaalbaarheid biedt.</span><span class="sxs-lookup"><span data-stu-id="eec02-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="eec02-111">Hiermee kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="eec02-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="eec02-112">Configureer Belastingberekening via Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="eec02-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="eec02-113">RCS is een verbeterde versie van de ER-ontwerper (Electronic Reporting) en is beschikbaar als zelfstandig service.</span><span class="sxs-lookup"><span data-stu-id="eec02-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="eec02-114">Configureer de belastingmatrix om automatisch belastingcodes en -tarieven te bepalen.</span><span class="sxs-lookup"><span data-stu-id="eec02-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="eec02-115">Configureer de belastingmatrix om automatisch het belastingregistratienummer te bepalen.</span><span class="sxs-lookup"><span data-stu-id="eec02-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="eec02-116">Configureer de ontwerper voor belastingberekening om formules en voorwaarden te definiëren.</span><span class="sxs-lookup"><span data-stu-id="eec02-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="eec02-117">Deel de oplossing voor belastingbepaling en -berekening voor rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="eec02-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="eec02-118">Als u de service voor belastingberekening wilt gebruiken, installeert u de invoegtoepassing voor de service vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="eec02-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="eec02-119">Voltooi vervolgens de instellingen in RCS en schakel de service voor belastingberekeningsservice in Finance en Supply Chain Management in.</span><span class="sxs-lookup"><span data-stu-id="eec02-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="eec02-120">Zie [Aan de slag met belastingservice](./global-get-started-with-tax-calculation-service.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eec02-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="eec02-121">Beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="eec02-121">Availability</span></span>

<span data-ttu-id="eec02-122">Belastingberekening is alleen beschikbaar in sandbox-omgevingen en voor bepaalde klanten, via een openbaar preview-programma.</span><span class="sxs-lookup"><span data-stu-id="eec02-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="eec02-123">Uiteindelijk wordt deze algemeen beschikbaar voor alle klanten en in productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="eec02-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="eec02-124">Er wordt steeds nieuwe functies geleverd. Controleer daarom regelmatig de meest actuele documentatie voor meer informatie over de dekking en het bereik van ondersteunde functies.</span><span class="sxs-lookup"><span data-stu-id="eec02-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="eec02-125">Belastingberekening wordt geïmplementeerd in de volgende geografische regio's van Azure.</span><span class="sxs-lookup"><span data-stu-id="eec02-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="eec02-126">Deze wordt daarnaast geïmplementeerd in andere Azure-regio's op basis van klantbehoeften:</span><span class="sxs-lookup"><span data-stu-id="eec02-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="eec02-127">Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="eec02-127">United States</span></span>
- <span data-ttu-id="eec02-128">Europa</span><span class="sxs-lookup"><span data-stu-id="eec02-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="eec02-129">Belastingberekening ondersteunt geen on-premises implementaties van Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="eec02-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="eec02-130">Ook eerdere versies, zoals Dynamics AX 2012, worden niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="eec02-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="eec02-131">Belangrijkste functies</span><span class="sxs-lookup"><span data-stu-id="eec02-131">Feature highlights</span></span>

- <span data-ttu-id="eec02-132">Een configureerbare belastingmatrix om automatisch belasting te bepalen en te berekenen</span><span class="sxs-lookup"><span data-stu-id="eec02-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="eec02-133">Ondersteuning voor meerdere belastingregistratienummers</span><span class="sxs-lookup"><span data-stu-id="eec02-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="eec02-134">Ondersteuning van transferorders voor het bepalen en berekenen van btw</span><span class="sxs-lookup"><span data-stu-id="eec02-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="eec02-135">Ondersteuning van transferorder voor het bepalen van meerdere belastingregistratienummers</span><span class="sxs-lookup"><span data-stu-id="eec02-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="eec02-136">Ondersteunde transacties</span><span class="sxs-lookup"><span data-stu-id="eec02-136">Supported transactions</span></span>

<span data-ttu-id="eec02-137">Belastingberekening kan worden ingeschakeld per rechtspersoon en transactie.</span><span class="sxs-lookup"><span data-stu-id="eec02-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="eec02-138">De volgende transacties worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="eec02-138">The following transactions are supported:</span></span>

- <span data-ttu-id="eec02-139">Verkoopproces</span><span class="sxs-lookup"><span data-stu-id="eec02-139">Sales process</span></span>

    - <span data-ttu-id="eec02-140">Verkoopofferte</span><span class="sxs-lookup"><span data-stu-id="eec02-140">Sales quotation</span></span>
    - <span data-ttu-id="eec02-141">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="eec02-141">Sales order</span></span>
    - <span data-ttu-id="eec02-142">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="eec02-142">Confirmation</span></span>
    - <span data-ttu-id="eec02-143">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="eec02-143">Picking list</span></span>
    - <span data-ttu-id="eec02-144">Pakbon</span><span class="sxs-lookup"><span data-stu-id="eec02-144">Packing slip</span></span>
    - <span data-ttu-id="eec02-145">Verkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="eec02-145">Sales invoice</span></span>
    - <span data-ttu-id="eec02-146">Creditnota</span><span class="sxs-lookup"><span data-stu-id="eec02-146">Credit note</span></span>
    - <span data-ttu-id="eec02-147">Retourorder</span><span class="sxs-lookup"><span data-stu-id="eec02-147">Return order</span></span>
    - <span data-ttu-id="eec02-148">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="eec02-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="eec02-149">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="eec02-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="eec02-150">Aankoopproces</span><span class="sxs-lookup"><span data-stu-id="eec02-150">Purchase process</span></span>

    - <span data-ttu-id="eec02-151">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="eec02-151">Purchase order</span></span>
    - <span data-ttu-id="eec02-152">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="eec02-152">Confirmation</span></span>
    - <span data-ttu-id="eec02-153">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="eec02-153">Receipts list</span></span>
    - <span data-ttu-id="eec02-154">Ontvangst van producten</span><span class="sxs-lookup"><span data-stu-id="eec02-154">Product receipt</span></span>
    - <span data-ttu-id="eec02-155">Inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="eec02-155">Purchase invoice</span></span>
    - <span data-ttu-id="eec02-156">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="eec02-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="eec02-157">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="eec02-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="eec02-158">Creditnota</span><span class="sxs-lookup"><span data-stu-id="eec02-158">Credit note</span></span>
    - <span data-ttu-id="eec02-159">Retourorder</span><span class="sxs-lookup"><span data-stu-id="eec02-159">Return order</span></span>
    - <span data-ttu-id="eec02-160">Opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="eec02-160">Purchase requisition</span></span>
    - <span data-ttu-id="eec02-161">Diverse toeslagen voor regel van opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="eec02-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="eec02-162">Offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="eec02-162">Request for quotation</span></span>
    - <span data-ttu-id="eec02-163">Diverse toeslagen voor koptekst van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="eec02-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="eec02-164">Diverse toeslagen voor regel van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="eec02-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="eec02-165">Voorraadproces</span><span class="sxs-lookup"><span data-stu-id="eec02-165">Inventory process</span></span>

    - <span data-ttu-id="eec02-166">Transferorder – verzenden</span><span class="sxs-lookup"><span data-stu-id="eec02-166">Transfer order – ship</span></span>
    - <span data-ttu-id="eec02-167">Transferorder – ontvangen</span><span class="sxs-lookup"><span data-stu-id="eec02-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="eec02-168">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="eec02-168">Related resources</span></span>

[<span data-ttu-id="eec02-169">Aan de slag met belastingservice</span><span class="sxs-lookup"><span data-stu-id="eec02-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="eec02-170">Meerdere btw-registratienummers</span><span class="sxs-lookup"><span data-stu-id="eec02-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="eec02-171">Ondersteuning voor belastingfunctie voor transferorder</span><span class="sxs-lookup"><span data-stu-id="eec02-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="eec02-172">Uitbreiding in belastingservice maken</span><span class="sxs-lookup"><span data-stu-id="eec02-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)