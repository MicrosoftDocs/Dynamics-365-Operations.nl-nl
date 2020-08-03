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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596218"
---
# <a name="country-of-origin"></a><span data-ttu-id="6dfd6-105">Land van oorsprong</span><span class="sxs-lookup"><span data-stu-id="6dfd6-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dfd6-106">Veel organisaties verlenen certificaten aan leveranciers om ervoor te zorgen dat producten voldoen aan specifieke certificeringsnormen.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="6dfd6-107">Deze certificaten zijn vaak afhankelijk van het land van oorsprong.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="6dfd6-108">Met de functie voor het land van oorsprong kunt u een product koppelen aan het land van oorsprong en de bijbehorende productcertificaten bijhouden.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="6dfd6-109">Bron- en doellanden configureren</span><span class="sxs-lookup"><span data-stu-id="6dfd6-109">Configure source and destination countries</span></span>

<span data-ttu-id="6dfd6-110">Voordat u een certificaat voor een product uitgeeft, moet u het product koppelen aan het land van bestemming en het land van oorsprong.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="6dfd6-111">Ga naar **Productgegevensbeheer \> Instellingen \> Productconformiteit \> Land van oorsprong \> Regels voor land van oorsprong**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="6dfd6-112">Selecteer een bestaande landinstelling om te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe landinstelling te maken.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="6dfd6-113">Stel de volgende waarden in voor het geselecteerde of nieuwe land.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="6dfd6-114">Veld</span><span class="sxs-lookup"><span data-stu-id="6dfd6-114">Field</span></span> | <span data-ttu-id="6dfd6-115">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6dfd6-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="6dfd6-116">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="6dfd6-116">Item number</span></span> | <span data-ttu-id="6dfd6-117">Selecteer het artikelnummer van het product.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="6dfd6-118">Bestemmingsland</span><span class="sxs-lookup"><span data-stu-id="6dfd6-118">Destination country</span></span> | <span data-ttu-id="6dfd6-119">Selecteer het land waarnaar u het product wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="6dfd6-120">Land van oorsprong</span><span class="sxs-lookup"><span data-stu-id="6dfd6-120">Origin country</span></span> | <span data-ttu-id="6dfd6-121">Selecteer het land vanwaaruit u het product wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="6dfd6-122">Het doel van deze instelling is om een stuklijstrapport te genereren waarin u het land van oorsprong kunt opnemen voor elk onderdeel waarvoor bron- en doellanden zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="6dfd6-123">Dit rapport geeft een compleet beeld van waar uw onderdelen vandaan komen en waar ze naartoe gaan.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="6dfd6-124">Leverancierscertificaten bijhouden</span><span class="sxs-lookup"><span data-stu-id="6dfd6-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="6dfd6-125">U kunt de pagina **Leverancierscertificaten voor land van oorsprong** gebruiken om certificaten bij te houden die u aan leveranciers geeft.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="6dfd6-126">U moet bepalen welke certificaatdocumenten u wilt uitgeven en hoe u deze aan klanten gaat rapporteren.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="6dfd6-127">Met deze functie kunt u uw certificaten bijhouden.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="6dfd6-128">U kunt hiermee ook kiezen of de relevante certificaatnummers worden weergegeven op facturen, pakbonnen en/of orderbevestigingen.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="6dfd6-129">Ga als volgt te werk om de certificaatgegevens in te stellen.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="6dfd6-130">Ga naar **Productgegevensbeheer \> Instellingen \> Productconformiteit \> Land van oorsprong \> Leverancierscertificaten voor land van oorsprong**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="6dfd6-131">Selecteer een bestaande certificaatinstelling om te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe certificaatinstelling te maken.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="6dfd6-132">Stel de volgende instellingen in voor het geselecteerde of nieuwe certificaat.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="6dfd6-133">Veld</span><span class="sxs-lookup"><span data-stu-id="6dfd6-133">Field</span></span> | <span data-ttu-id="6dfd6-134">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="6dfd6-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="6dfd6-135">Leverancier</span><span class="sxs-lookup"><span data-stu-id="6dfd6-135">Vendor account</span></span> | <span data-ttu-id="6dfd6-136">Selecteer de leverancier aan wie u het certificaat hebt uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="6dfd6-137">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="6dfd6-137">Item number</span></span> | <span data-ttu-id="6dfd6-138">Selecteer het artikel waarvoor u het certificaat hebt uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="6dfd6-139">Land/regio</span><span class="sxs-lookup"><span data-stu-id="6dfd6-139">Country/region</span></span> | <span data-ttu-id="6dfd6-140">Het land of de regio van bestemming waar u dit certificaat moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="6dfd6-141">Certificaatnummer</span><span class="sxs-lookup"><span data-stu-id="6dfd6-141">Certificate number</span></span> | <span data-ttu-id="6dfd6-142">Voer het identificatienummer in van het certificaat dat u hebt uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="6dfd6-143">Geldig</span><span class="sxs-lookup"><span data-stu-id="6dfd6-143">Effective</span></span> | <span data-ttu-id="6dfd6-144">Selecteer de eerste datum waarop het huidige certificaat geldig is.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="6dfd6-145">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="6dfd6-145">Expiration</span></span> | <span data-ttu-id="6dfd6-146">Selecteer de laatste datum waarop het huidige certificaat geldig is.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="6dfd6-147">Afdrukken op factuur</span><span class="sxs-lookup"><span data-stu-id="6dfd6-147">Print on invoice</span></span> | <span data-ttu-id="6dfd6-148">Schakel dit selectievakje in om het certificaatnummer af te drukken op facturen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="6dfd6-149">Afdrukken op pakbon</span><span class="sxs-lookup"><span data-stu-id="6dfd6-149">Print on packing slip</span></span> | <span data-ttu-id="6dfd6-150">Schakel dit selectievakje in om het certificaatnummer af te drukken op pakbonnen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="6dfd6-151">Afdrukken op verkooporder</span><span class="sxs-lookup"><span data-stu-id="6dfd6-151">Print on sales order</span></span> | <span data-ttu-id="6dfd6-152">Schakel dit selectievakje in om het certificaatnummer af te drukken op verkooporders die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="6dfd6-153">Het land van oorsprong opnemen op stuklijstrapporten</span><span class="sxs-lookup"><span data-stu-id="6dfd6-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="6dfd6-154">Wanneer u een stuklijstrapport genereert, kunt u het land van oorsprong opnemen voor elk onderdeel waarvoor u de bron- en doellanden hebt opgegeven op de pagina **Regels voor land van oorsprong**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="6dfd6-155">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6dfd6-156">Selecteer of maak een product om de pagina **Vrijgegevens productgegevens** te openen.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="6dfd6-157">Selecteer in het actievenster op het tabblad **Technicus** in de groep **Stuklijst** de optie **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="6dfd6-158">Selecteer op de pagina die verschijnt in het actievenster **Stuklijst \> Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="6dfd6-159">In het dialoogvenster **Stuklijstregels** stelt u het veld **Bestemmingsland** in op het doelland dat u in het rapport wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="6dfd6-160">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-160">Select **OK**.</span></span>

<span data-ttu-id="6dfd6-161">Er wordt een rapport gegenereerd en weergegeven met informatie over het land van oorsprong voor elk onderdeel.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="6dfd6-162">Hier volgt een voorbeeld van het rapport.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-162">Here is an example of the report.</span></span>

<span data-ttu-id="6dfd6-163">![Rapport voor Land van oorsprong](media/country-of-origin-report.png "Rapport voor Land van oorsprong")</span><span class="sxs-lookup"><span data-stu-id="6dfd6-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
