---
title: Belastingberekening (Preview)
description: In dit onderwerp worden het algehele bereik en de functies voor belastingberekening uitgelegd.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892344"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="92f01-103">Belastingberekening (Preview)</span><span class="sxs-lookup"><span data-stu-id="92f01-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="92f01-104">Belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="92f01-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="92f01-105">De belastingengine kan volledig worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="92f01-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="92f01-106">De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting.</span><span class="sxs-lookup"><span data-stu-id="92f01-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="92f01-107">De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.</span><span class="sxs-lookup"><span data-stu-id="92f01-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="92f01-108">Belastingberekening wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="92f01-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="92f01-109">Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.</span><span class="sxs-lookup"><span data-stu-id="92f01-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="92f01-110">Belastingberekening is een op microservices gebaseerde belastingengine die exponentiële schaalbaarheid biedt.</span><span class="sxs-lookup"><span data-stu-id="92f01-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="92f01-111">Hiermee kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="92f01-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="92f01-112">Configureer Belastingberekening via Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="92f01-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="92f01-113">RCS is een verbeterde versie van de ER-ontwerper (Electronic Reporting) en is beschikbaar als zelfstandig service.</span><span class="sxs-lookup"><span data-stu-id="92f01-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="92f01-114">Configureer de belastingmatrix om automatisch belastingcodes en -tarieven te bepalen.</span><span class="sxs-lookup"><span data-stu-id="92f01-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="92f01-115">Configureer de belastingmatrix om automatisch het belastingregistratienummer te bepalen.</span><span class="sxs-lookup"><span data-stu-id="92f01-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="92f01-116">Configureer de ontwerper voor belastingberekening om formules en voorwaarden te definiëren.</span><span class="sxs-lookup"><span data-stu-id="92f01-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="92f01-117">Deel de oplossing voor belastingbepaling en -berekening voor rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="92f01-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="92f01-118">Als u de service voor belastingberekening wilt gebruiken, installeert u de invoegtoepassing voor de service vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="92f01-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="92f01-119">Voltooi vervolgens de instellingen in RCS en schakel de service voor belastingberekeningsservice in Finance en Supply Chain Management in.</span><span class="sxs-lookup"><span data-stu-id="92f01-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="92f01-120">Zie [Aan de slag met belastingservice](./global-get-started-with-tax-calculation-service.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="92f01-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="92f01-121">Beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="92f01-121">Availability</span></span>

<span data-ttu-id="92f01-122">Belastingberekening is alleen beschikbaar in sandbox-omgevingen en voor bepaalde klanten, via een openbaar preview-programma.</span><span class="sxs-lookup"><span data-stu-id="92f01-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="92f01-123">Uiteindelijk wordt deze algemeen beschikbaar voor alle klanten en in productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="92f01-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="92f01-124">Er wordt steeds nieuwe functies geleverd. Controleer daarom regelmatig de meest actuele documentatie voor meer informatie over de dekking en het bereik van ondersteunde functies.</span><span class="sxs-lookup"><span data-stu-id="92f01-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="92f01-125">Belastingberekening wordt geïmplementeerd in de volgende geografische regio's van Azure.</span><span class="sxs-lookup"><span data-stu-id="92f01-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="92f01-126">Deze wordt daarnaast geïmplementeerd in andere Azure-regio's op basis van klantbehoeften:</span><span class="sxs-lookup"><span data-stu-id="92f01-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="92f01-127">Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="92f01-127">United States</span></span>
- <span data-ttu-id="92f01-128">Europa</span><span class="sxs-lookup"><span data-stu-id="92f01-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="92f01-129">Belastingberekening ondersteunt geen on-premises implementaties van Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="92f01-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="92f01-130">Ook eerdere versies, zoals Dynamics AX 2012, worden niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="92f01-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="92f01-131">Belangrijkste functies</span><span class="sxs-lookup"><span data-stu-id="92f01-131">Feature highlights</span></span>

- <span data-ttu-id="92f01-132">Een configureerbare belastingmatrix om automatisch belasting te bepalen en te berekenen</span><span class="sxs-lookup"><span data-stu-id="92f01-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="92f01-133">Ondersteuning voor meerdere belastingregistratienummers</span><span class="sxs-lookup"><span data-stu-id="92f01-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="92f01-134">Ondersteuning van transferorders voor het bepalen en berekenen van btw</span><span class="sxs-lookup"><span data-stu-id="92f01-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="92f01-135">Ondersteuning van transferorder voor het bepalen van meerdere belastingregistratienummers</span><span class="sxs-lookup"><span data-stu-id="92f01-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="92f01-136">Ondersteunde transacties</span><span class="sxs-lookup"><span data-stu-id="92f01-136">Supported transactions</span></span>

<span data-ttu-id="92f01-137">Belastingberekening kan worden ingeschakeld per rechtspersoon en transactie.</span><span class="sxs-lookup"><span data-stu-id="92f01-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="92f01-138">De volgende transacties worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="92f01-138">The following transactions are supported:</span></span>

- <span data-ttu-id="92f01-139">Verkoopproces</span><span class="sxs-lookup"><span data-stu-id="92f01-139">Sales process</span></span>

    - <span data-ttu-id="92f01-140">Verkoopofferte</span><span class="sxs-lookup"><span data-stu-id="92f01-140">Sales quotation</span></span>
    - <span data-ttu-id="92f01-141">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="92f01-141">Sales order</span></span>
    - <span data-ttu-id="92f01-142">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="92f01-142">Confirmation</span></span>
    - <span data-ttu-id="92f01-143">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="92f01-143">Picking list</span></span>
    - <span data-ttu-id="92f01-144">Pakbon</span><span class="sxs-lookup"><span data-stu-id="92f01-144">Packing slip</span></span>
    - <span data-ttu-id="92f01-145">Verkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="92f01-145">Sales invoice</span></span>
    - <span data-ttu-id="92f01-146">Creditnota</span><span class="sxs-lookup"><span data-stu-id="92f01-146">Credit note</span></span>
    - <span data-ttu-id="92f01-147">Retourorder</span><span class="sxs-lookup"><span data-stu-id="92f01-147">Return order</span></span>
    - <span data-ttu-id="92f01-148">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="92f01-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="92f01-149">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="92f01-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="92f01-150">Aankoopproces</span><span class="sxs-lookup"><span data-stu-id="92f01-150">Purchase process</span></span>

    - <span data-ttu-id="92f01-151">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="92f01-151">Purchase order</span></span>
    - <span data-ttu-id="92f01-152">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="92f01-152">Confirmation</span></span>
    - <span data-ttu-id="92f01-153">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="92f01-153">Receipts list</span></span>
    - <span data-ttu-id="92f01-154">Ontvangst van producten</span><span class="sxs-lookup"><span data-stu-id="92f01-154">Product receipt</span></span>
    - <span data-ttu-id="92f01-155">Inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="92f01-155">Purchase invoice</span></span>
    - <span data-ttu-id="92f01-156">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="92f01-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="92f01-157">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="92f01-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="92f01-158">Creditnota</span><span class="sxs-lookup"><span data-stu-id="92f01-158">Credit note</span></span>
    - <span data-ttu-id="92f01-159">Retourorder</span><span class="sxs-lookup"><span data-stu-id="92f01-159">Return order</span></span>
    - <span data-ttu-id="92f01-160">Opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="92f01-160">Purchase requisition</span></span>
    - <span data-ttu-id="92f01-161">Diverse toeslagen voor regel van opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="92f01-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="92f01-162">Offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="92f01-162">Request for quotation</span></span>
    - <span data-ttu-id="92f01-163">Diverse toeslagen voor koptekst van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="92f01-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="92f01-164">Diverse toeslagen voor regel van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="92f01-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="92f01-165">Voorraadproces</span><span class="sxs-lookup"><span data-stu-id="92f01-165">Inventory process</span></span>

    - <span data-ttu-id="92f01-166">Transferorder – verzenden</span><span class="sxs-lookup"><span data-stu-id="92f01-166">Transfer order – ship</span></span>
    - <span data-ttu-id="92f01-167">Transferorder – ontvangen</span><span class="sxs-lookup"><span data-stu-id="92f01-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="92f01-168">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="92f01-168">Related resources</span></span>

[<span data-ttu-id="92f01-169">Aan de slag met belastingservice</span><span class="sxs-lookup"><span data-stu-id="92f01-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="92f01-170">Meerdere btw-registratienummers</span><span class="sxs-lookup"><span data-stu-id="92f01-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="92f01-171">Ondersteuning voor belastingfunctie voor transferorder</span><span class="sxs-lookup"><span data-stu-id="92f01-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="92f01-172">Uitbreiding in belastingservice maken</span><span class="sxs-lookup"><span data-stu-id="92f01-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)