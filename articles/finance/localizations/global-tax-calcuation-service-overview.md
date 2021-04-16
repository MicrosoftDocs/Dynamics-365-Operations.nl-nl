---
title: Service voor belastingberekening (Preview)
description: In dit onderwerp worden het algehele bereik en de functies van de service voor belastingberekening uitgelegd.
author: wangchen
ms.date: 03/02/2021
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
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818219"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="7dd7e-103">Service voor belastingberekening (Preview)</span><span class="sxs-lookup"><span data-stu-id="7dd7e-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7dd7e-104">De service voor belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="7dd7e-105">De belastingengine kan volledig worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="7dd7e-106">De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="7dd7e-107">De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="7dd7e-108">De service voor het berekenen van belastingen wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="7dd7e-109">Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="7dd7e-110">De service voor belastingberekening is een op Microsoft gebaseerde belastingengine die exponentiële schaalbaarheid biedt.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="7dd7e-111">Hiermee kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="7dd7e-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="7dd7e-112">Configureer de service voor belastingberekening via Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="7dd7e-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="7dd7e-113">RCS is een verbeterde versie van de ER-ontwerper (Electronic Reporting) en is beschikbaar als zelfstandig service.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="7dd7e-114">Configureer de belastingmatrix om automatisch belastingcodes en -tarieven te bepalen.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="7dd7e-115">Configureer de belastingmatrix om automatisch het belastingregistratienummer te bepalen.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="7dd7e-116">Configureer de ontwerper voor belastingberekening om formules en voorwaarden te definiëren.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="7dd7e-117">Deel de oplossing voor belastingbepaling en -berekening voor rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="7dd7e-118">Als u de service voor belastingberekening wilt gebruiken, installeert u de invoegtoepassing voor de service vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7dd7e-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7dd7e-119">Voltooi vervolgens de instellingen in RCS en schakel de service voor belastingberekeningsservice in Finance en Supply Chain Management in.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="7dd7e-120">Zie [Aan de slag met belastingservice](https://go.microsoft.com/fwlink/?linkid=2138482) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="7dd7e-121">Beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="7dd7e-121">Availability</span></span>

<span data-ttu-id="7dd7e-122">De service voor belastingberekening is alleen beschikbaar in sandbox-omgevingen en voor bepaalde klanten, via een openbaar preview-programma.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="7dd7e-123">Uiteindelijk wordt deze algemeen beschikbaar voor alle klanten en in productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="7dd7e-124">Nieuwe functies blijven geleverd worden in de service voor belastingberekening.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="7dd7e-125">Controleer daarom regelmatig de meest actuele documentatie voor meer informatie over de dekking en het bereik van ondersteunde functies.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="7dd7e-126">De service voor belastingberekening wordt geïmplementeerd in de volgende geografische regio's van Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="7dd7e-127">Deze wordt daarnaast geïmplementeerd in andere Azure-regio's op basis van klantbehoeften:</span><span class="sxs-lookup"><span data-stu-id="7dd7e-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="7dd7e-128">Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="7dd7e-128">United States</span></span>
- <span data-ttu-id="7dd7e-129">Europa</span><span class="sxs-lookup"><span data-stu-id="7dd7e-129">Europe</span></span>
- <span data-ttu-id="7dd7e-130">Frankrijk</span><span class="sxs-lookup"><span data-stu-id="7dd7e-130">France</span></span>
- <span data-ttu-id="7dd7e-131">Verenigd Koninkrijk</span><span class="sxs-lookup"><span data-stu-id="7dd7e-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="7dd7e-132">De service voor belastingberekening ondersteunt geen on-premises implementaties van Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="7dd7e-133">Ook eerdere versies, zoals Dynamics AX 2012, worden niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="7dd7e-134">Belangrijkste functies</span><span class="sxs-lookup"><span data-stu-id="7dd7e-134">Feature highlights</span></span>

- <span data-ttu-id="7dd7e-135">Een configureerbare belastingmatrix om automatisch belasting te bepalen en te berekenen</span><span class="sxs-lookup"><span data-stu-id="7dd7e-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="7dd7e-136">Ondersteuning voor meerdere btw-registratienummers</span><span class="sxs-lookup"><span data-stu-id="7dd7e-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="7dd7e-137">Ondersteuning van transferorders voor het bepalen en berekenen van btw</span><span class="sxs-lookup"><span data-stu-id="7dd7e-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="7dd7e-138">Ondersteuning van transferorder voor het bepalen van meerdere btw-registratienummers</span><span class="sxs-lookup"><span data-stu-id="7dd7e-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="7dd7e-139">Ondersteunde transacties</span><span class="sxs-lookup"><span data-stu-id="7dd7e-139">Supported transactions</span></span>

<span data-ttu-id="7dd7e-140">De service voor belastingberekening kan worden ingeschakeld per rechtspersoon en transactie.</span><span class="sxs-lookup"><span data-stu-id="7dd7e-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="7dd7e-141">De volgende transacties worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="7dd7e-141">The following transactions are supported:</span></span>

- <span data-ttu-id="7dd7e-142">Verkoopproces</span><span class="sxs-lookup"><span data-stu-id="7dd7e-142">Sales process</span></span>

    - <span data-ttu-id="7dd7e-143">Verkoopofferte</span><span class="sxs-lookup"><span data-stu-id="7dd7e-143">Sales quotation</span></span>
    - <span data-ttu-id="7dd7e-144">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="7dd7e-144">Sales order</span></span>
    - <span data-ttu-id="7dd7e-145">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="7dd7e-145">Confirmation</span></span>
    - <span data-ttu-id="7dd7e-146">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="7dd7e-146">Picking list</span></span>
    - <span data-ttu-id="7dd7e-147">Pakbon</span><span class="sxs-lookup"><span data-stu-id="7dd7e-147">Packing slip</span></span>
    - <span data-ttu-id="7dd7e-148">Verkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="7dd7e-148">Sales invoice</span></span>
    - <span data-ttu-id="7dd7e-149">Creditnota</span><span class="sxs-lookup"><span data-stu-id="7dd7e-149">Credit note</span></span>
    - <span data-ttu-id="7dd7e-150">Retourorder</span><span class="sxs-lookup"><span data-stu-id="7dd7e-150">Return order</span></span>
    - <span data-ttu-id="7dd7e-151">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="7dd7e-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="7dd7e-152">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="7dd7e-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="7dd7e-153">Aankoopproces</span><span class="sxs-lookup"><span data-stu-id="7dd7e-153">Purchase process</span></span>

    - <span data-ttu-id="7dd7e-154">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="7dd7e-154">Purchase order</span></span>
    - <span data-ttu-id="7dd7e-155">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="7dd7e-155">Confirmation</span></span>
    - <span data-ttu-id="7dd7e-156">Ontvangstlijst</span><span class="sxs-lookup"><span data-stu-id="7dd7e-156">Receipts list</span></span>
    - <span data-ttu-id="7dd7e-157">Ontvangst van producten</span><span class="sxs-lookup"><span data-stu-id="7dd7e-157">Product receipt</span></span>
    - <span data-ttu-id="7dd7e-158">Inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="7dd7e-158">Purchase invoice</span></span>
    - <span data-ttu-id="7dd7e-159">Diverse toeslagen voor koptekst</span><span class="sxs-lookup"><span data-stu-id="7dd7e-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="7dd7e-160">Diverse toeslagen voor regels</span><span class="sxs-lookup"><span data-stu-id="7dd7e-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="7dd7e-161">Creditnota</span><span class="sxs-lookup"><span data-stu-id="7dd7e-161">Credit note</span></span>
    - <span data-ttu-id="7dd7e-162">Retourorder</span><span class="sxs-lookup"><span data-stu-id="7dd7e-162">Return order</span></span>
    - <span data-ttu-id="7dd7e-163">Opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="7dd7e-163">Purchase requisition</span></span>
    - <span data-ttu-id="7dd7e-164">Diverse toeslagen voor regel van opdracht tot inkoop</span><span class="sxs-lookup"><span data-stu-id="7dd7e-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="7dd7e-165">Offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="7dd7e-165">Request for quotation</span></span>
    - <span data-ttu-id="7dd7e-166">Diverse toeslagen voor koptekst van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="7dd7e-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="7dd7e-167">Diverse toeslagen voor regel van offerteaanvraag</span><span class="sxs-lookup"><span data-stu-id="7dd7e-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="7dd7e-168">Voorraadproces</span><span class="sxs-lookup"><span data-stu-id="7dd7e-168">Inventory process</span></span>

    - <span data-ttu-id="7dd7e-169">Transferorder – verzenden</span><span class="sxs-lookup"><span data-stu-id="7dd7e-169">Transfer order – ship</span></span>
    - <span data-ttu-id="7dd7e-170">Transferorder – ontvangen</span><span class="sxs-lookup"><span data-stu-id="7dd7e-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="7dd7e-171">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="7dd7e-171">Related resources</span></span>

[<span data-ttu-id="7dd7e-172">Aan de slag met belastingservice</span><span class="sxs-lookup"><span data-stu-id="7dd7e-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="7dd7e-173">Meerdere btw-registratienummers</span><span class="sxs-lookup"><span data-stu-id="7dd7e-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="7dd7e-174">Ondersteuning voor belastingfunctie voor transferorder</span><span class="sxs-lookup"><span data-stu-id="7dd7e-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="7dd7e-175">Uitbreiding in belastingservice maken</span><span class="sxs-lookup"><span data-stu-id="7dd7e-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
