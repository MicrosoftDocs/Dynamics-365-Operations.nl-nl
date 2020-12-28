---
title: Land van oorsprong
description: Veel organisaties verlenen certificaten aan leveranciers om ervoor te zorgen dat producten voldoen aan specifieke certificeringsnormen. Deze certificaten zijn vaak afhankelijk van het land van oorsprong. Dit onderwerp biedt informatie over de functie voor het land van oorsprong, waarmee u een product kunt koppelen aan het land van oorsprong en de bijbehorende productcertificaten kunt bijhouden.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425107"
---
# <a name="country-of-origin"></a><span data-ttu-id="8c9e6-105">Land van oorsprong</span><span class="sxs-lookup"><span data-stu-id="8c9e6-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8c9e6-106">Veel organisaties verlenen certificaten aan leveranciers om ervoor te zorgen dat producten voldoen aan specifieke certificeringsnormen.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="8c9e6-107">Deze certificaten zijn vaak afhankelijk van het land van oorsprong.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="8c9e6-108">Met de functie voor het land van oorsprong kunt u een product koppelen aan het land van oorsprong en de bijbehorende productcertificaten bijhouden.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="8c9e6-109">De functie voor land van oorsprong inschakelen</span><span class="sxs-lookup"><span data-stu-id="8c9e6-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="8c9e6-110">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="8c9e6-111">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="8c9e6-112">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="8c9e6-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8c9e6-113">**Module:** *Productgegevensbeheer*</span><span class="sxs-lookup"><span data-stu-id="8c9e6-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="8c9e6-114">**Functienaam:** *beheerfunctie Land van oorsprong*</span><span class="sxs-lookup"><span data-stu-id="8c9e6-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="8c9e6-115">Bron- en doellanden configureren</span><span class="sxs-lookup"><span data-stu-id="8c9e6-115">Configure source and destination countries</span></span>

<span data-ttu-id="8c9e6-116">Voordat u een certificaat voor een product uitgeeft, moet u het product koppelen aan het land van bestemming en het land van oorsprong.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="8c9e6-117">Ga naar **Productgegevensbeheer \> Instellingen \> Productconformiteit \> Land van oorsprong \> Regels voor land van oorsprong**.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="8c9e6-118">Selecteer een bestaande landinstelling om te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe landinstelling te maken.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="8c9e6-119">Stel de volgende waarden in voor het geselecteerde of nieuwe land.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="8c9e6-120">Veld</span><span class="sxs-lookup"><span data-stu-id="8c9e6-120">Field</span></span> | <span data-ttu-id="8c9e6-121">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="8c9e6-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="8c9e6-122">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="8c9e6-122">Item number</span></span> | <span data-ttu-id="8c9e6-123">Selecteer het artikelnummer van het product.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="8c9e6-124">Bestemmingsland</span><span class="sxs-lookup"><span data-stu-id="8c9e6-124">Destination country</span></span> | <span data-ttu-id="8c9e6-125">Selecteer het land waarnaar u het product wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="8c9e6-126">Land van oorsprong</span><span class="sxs-lookup"><span data-stu-id="8c9e6-126">Origin country</span></span> | <span data-ttu-id="8c9e6-127">Selecteer het land vanwaaruit u het product wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="8c9e6-128">Het doel van deze instelling is om een stuklijstrapport te genereren waarin u het land van oorsprong kunt opnemen voor elk onderdeel waarvoor bron- en doellanden zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="8c9e6-129">Dit rapport geeft een compleet beeld van waar uw onderdelen vandaan komen en waar ze naartoe gaan.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="8c9e6-130">Leverancierscertificaten bijhouden</span><span class="sxs-lookup"><span data-stu-id="8c9e6-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="8c9e6-131">U kunt de pagina **Leverancierscertificaten voor land van oorsprong** gebruiken om certificaten bij te houden die u aan leveranciers geeft.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="8c9e6-132">U moet bepalen welke certificaatdocumenten u wilt uitgeven en hoe u deze aan klanten gaat rapporteren.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="8c9e6-133">Met deze functie kunt u uw certificaten bijhouden.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="8c9e6-134">U kunt hiermee ook kiezen of de relevante certificaatnummers worden weergegeven op facturen, pakbonnen en/of orderbevestigingen.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="8c9e6-135">Ga als volgt te werk om de certificaatgegevens in te stellen.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="8c9e6-136">Ga naar **Productgegevensbeheer \> Instellingen \> Productconformiteit \> Land van oorsprong \> Leverancierscertificaten voor land van oorsprong**.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="8c9e6-137">Selecteer een bestaande certificaatinstelling om te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe certificaatinstelling te maken.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="8c9e6-138">Stel de volgende instellingen in voor het geselecteerde of nieuwe certificaat.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="8c9e6-139">Veld</span><span class="sxs-lookup"><span data-stu-id="8c9e6-139">Field</span></span> | <span data-ttu-id="8c9e6-140">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="8c9e6-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="8c9e6-141">Leverancier</span><span class="sxs-lookup"><span data-stu-id="8c9e6-141">Vendor account</span></span> | <span data-ttu-id="8c9e6-142">Selecteer de leverancier aan wie u het certificaat hebt uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="8c9e6-143">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="8c9e6-143">Item number</span></span> | <span data-ttu-id="8c9e6-144">Selecteer het artikel waarvoor u het certificaat hebt uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="8c9e6-145">Land/regio</span><span class="sxs-lookup"><span data-stu-id="8c9e6-145">Country/region</span></span> | <span data-ttu-id="8c9e6-146">Het land of de regio van bestemming waar u dit certificaat moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="8c9e6-147">Certificaatnummer</span><span class="sxs-lookup"><span data-stu-id="8c9e6-147">Certificate number</span></span> | <span data-ttu-id="8c9e6-148">Voer het identificatienummer in van het certificaat dat u hebt uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="8c9e6-149">Geldig</span><span class="sxs-lookup"><span data-stu-id="8c9e6-149">Effective</span></span> | <span data-ttu-id="8c9e6-150">Selecteer de eerste datum waarop het huidige certificaat geldig is.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="8c9e6-151">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="8c9e6-151">Expiration</span></span> | <span data-ttu-id="8c9e6-152">Selecteer de laatste datum waarop het huidige certificaat geldig is.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="8c9e6-153">Afdrukken op factuur</span><span class="sxs-lookup"><span data-stu-id="8c9e6-153">Print on invoice</span></span> | <span data-ttu-id="8c9e6-154">Schakel dit selectievakje in om het certificaatnummer af te drukken op facturen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="8c9e6-155">Afdrukken op pakbon</span><span class="sxs-lookup"><span data-stu-id="8c9e6-155">Print on packing slip</span></span> | <span data-ttu-id="8c9e6-156">Schakel dit selectievakje in om het certificaatnummer af te drukken op pakbonnen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="8c9e6-157">Afdrukken op verkooporder</span><span class="sxs-lookup"><span data-stu-id="8c9e6-157">Print on sales order</span></span> | <span data-ttu-id="8c9e6-158">Schakel dit selectievakje in om het certificaatnummer af te drukken op verkooporders die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="8c9e6-159">Het land van oorsprong opnemen op stuklijstrapporten</span><span class="sxs-lookup"><span data-stu-id="8c9e6-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="8c9e6-160">Wanneer u een stuklijstrapport genereert, kunt u het land van oorsprong opnemen voor elk onderdeel waarvoor u de bron- en doellanden hebt opgegeven op de pagina **Regels voor land van oorsprong**.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="8c9e6-161">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8c9e6-162">Selecteer of maak een product om de pagina **Vrijgegevens productgegevens** te openen.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="8c9e6-163">Selecteer in het actievenster op het tabblad **Technicus** in de groep **Stuklijst** de optie **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="8c9e6-164">Selecteer op de pagina die verschijnt in het actievenster **Stuklijst \> Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="8c9e6-165">In het dialoogvenster **Stuklijstregels** stelt u het veld **Bestemmingsland** in op het doelland dat u in het rapport wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="8c9e6-166">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-166">Select **OK**.</span></span>

<span data-ttu-id="8c9e6-167">Er wordt een rapport gegenereerd en weergegeven met informatie over het land van oorsprong voor elk onderdeel.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="8c9e6-168">Hier volgt een voorbeeld van het rapport.</span><span class="sxs-lookup"><span data-stu-id="8c9e6-168">Here is an example of the report.</span></span>

<span data-ttu-id="8c9e6-169">![Rapport voor Land van oorsprong](media/country-of-origin-report.png "Rapport voor Land van oorsprong")</span><span class="sxs-lookup"><span data-stu-id="8c9e6-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
