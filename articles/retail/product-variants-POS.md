---
title: Zoeken in voorraad op het verkooppunt (POS)
description: In dit onderwerp worden de opties beschreven die beschikbaar zijn voor het weergeven van voorraadgegevens in het verkooppunt (POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: cd2dc460c9e862503ebbf1942dcf998d67829d86
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "314412"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="21fda-103">Zoeken in voorraad op het verkooppunt (POS)</span><span class="sxs-lookup"><span data-stu-id="21fda-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="21fda-104">Met Zoeken in voorraad in het verkooppunt kunnen detailhandelaren operationele successen behalen in real-time en inzicht krijgen door verbinding te maken tussen winkels, het POS en de backoffice.</span><span class="sxs-lookup"><span data-stu-id="21fda-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="21fda-105">Deze functionaliteit biedt een nauwkeurige realtime weergave van de productvoorraad in winkels en distributiecentra.</span><span class="sxs-lookup"><span data-stu-id="21fda-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="21fda-106">Het helpt detailhandelaren ook om de efficiëntie te vergroten en kosten te besparen door de voorraadplanning in realtime te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="21fda-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="21fda-107">Een nauwkeurige realtime weergave van de voorraad binnen een organisatie helpt het winkelpersoneel om op tijd een uitstekende klantenservice te bieden.</span><span class="sxs-lookup"><span data-stu-id="21fda-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="21fda-108">Het moment dat er het meest toe doet, is het tijdstip waarop de klant is gereed om een aankoopbeslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="21fda-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="21fda-109">Het is belangrijk dat kassiers in de winkel realtime voorraadinformatie bij de hand hebben zodat ze correct een levering van producten kunnen beloven.</span><span class="sxs-lookup"><span data-stu-id="21fda-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="21fda-110">U kunt de pagina **Zoeken in voorraad** openen vanuit het werkgebied **Retail Modern POS** of **Retail Cloud POS**.</span><span class="sxs-lookup"><span data-stu-id="21fda-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Tegel Zoeken in voorraad op POS-startpagina](media/POSHomepage.png)

<span data-ttu-id="21fda-112">Op de pagina **Zoeken in voorraad** kunt u met het numerieke toetsenbord een productnummer invoeren.</span><span class="sxs-lookup"><span data-stu-id="21fda-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="21fda-113">U ziet vervolgens de hoeveelheid voorhanden voorrad voor meerdere winkels en magazijnen.</span><span class="sxs-lookup"><span data-stu-id="21fda-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standaardzoekpagina voor voorraad](media/InventoryLookUp.png)

<span data-ttu-id="21fda-115">**Gereserveerde** en **bestelde** aantallen worden ook weergegeven voor elke locatie.</span><span class="sxs-lookup"><span data-stu-id="21fda-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="21fda-116">**Gereserveerd**: deze hoeveelheid verwijst naar de waarde **Fysiek gereserveerd** uit de backoffice voor het opgegeven productnummer op de locatie.</span><span class="sxs-lookup"><span data-stu-id="21fda-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="21fda-117">**Besteld**: deze hoeveelheid verwijst naar de waarde **Totaal van order** uit de backoffice voor het opgegeven productnummer op de locatie.</span><span class="sxs-lookup"><span data-stu-id="21fda-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="21fda-118">Locaties waarvoor beschikbaarheidsgegevens voor voorraad worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="21fda-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="21fda-119">De lijst met locaties bevat twee typen entiteiten:</span><span class="sxs-lookup"><span data-stu-id="21fda-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="21fda-120">**Detailhandelwinkels**: in de lijst staan de winkels die zijn geconfigureerd met behulp van de winkellocatorgroep voor de huidige winkel in Detailhandel Hoofdkantoor.</span><span class="sxs-lookup"><span data-stu-id="21fda-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span>
- <span data-ttu-id="21fda-121">**Distributiecentra**: verschillende soorten distributiecentra (bijvoorbeeld magazijnen) kunnen worden geconfigureerd in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="21fda-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="21fda-122">In de lijst staat echter alleen de voorraadbeschikbaarheid voor distributiecentra van het type **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="21fda-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21fda-123">Informatie over de vooraadbeschikbaarheid wordt niet weergegeven voor magazijnen van het type **transit**, **quarantaine** en **goederen onderwep** voor het POS.</span><span class="sxs-lookup"><span data-stu-id="21fda-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="21fda-124">Op de pagina **Zoeken in voorraad** kunt u de ATP-hoeveelheden (available to promise) zien voor elke winkel, naast de huidige voorhanden hoeveelheden, gereserveerde hoeveelheden en bestelde hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="21fda-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="21fda-125">Selecteer de winkel waarvoor u de ATP-informatie wilt weergeven en selecteer vervolgens **Beschikbaarheid van de winkel weergeven**.</span><span class="sxs-lookup"><span data-stu-id="21fda-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP-hoeveelheden](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="21fda-127">De op dimensies gebaseerde matrixweergave openen om alle varianten te zien</span><span class="sxs-lookup"><span data-stu-id="21fda-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="21fda-128">Op de pagina **Productdetails** van een productmodel of op de pagina **Zoeken in voorraad** selecteert u **Alle varianten weergeven** in de app-balk onder aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="21fda-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="21fda-129">Als deze pagina's de eerste keer worden geopend, toont de weergave **Op dimensies gebaseerde matrix** de gegevens van de voorraadbeschikbaarheid voor alle varianten van een product voor de huidige winkel.</span><span class="sxs-lookup"><span data-stu-id="21fda-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="21fda-130">De knop **Alle varianten weergeven** is alleen beschikbaar voor productmodellen met productvarianten.</span><span class="sxs-lookup"><span data-stu-id="21fda-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="21fda-131">De knop is niet beschikbaar voor zelfstandige producten of kits.</span><span class="sxs-lookup"><span data-stu-id="21fda-131">It isn't available for standalone products or kits.</span></span>

![De knop Alle varianten weergeven op de pagina Zoeken in voorraad](media/StandardToMatrix.png)

<span data-ttu-id="21fda-133">Selecteer **Alle varianten weergeven** op de pagina **Productgegevens** van een productmodel of op de paigna **Zoeken in voorraad**, zonder een locatie te selecteren, om naar de weergave **Op dimensie gebaseerde matrix** te gaan en de voorraadbeschikbaarheidsgegevens voor alle varianten van een product voor de huidige winkel te tonen.</span><span class="sxs-lookup"><span data-stu-id="21fda-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Op dimensie gebaseerde matrix weergeven voor de pagina Zoeken in voorraad](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="21fda-135">In het voorgaande voorbeeld is de weergavevolgorde van de dimensies alfabetisch, omdat de volgorde van de dimensies niet is geconfigureerd voor het geselecteerde product.</span><span class="sxs-lookup"><span data-stu-id="21fda-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="21fda-136">In de weergave **Op dimensie gebaseerde matrix** omvatten de cellen voor de productvarianten een waarde voor voorhanden voorraad in de rechterbenedenhoek.</span><span class="sxs-lookup"><span data-stu-id="21fda-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="21fda-137">De volgende tabel beschrijft de betekenis van de verschillende waarden.</span><span class="sxs-lookup"><span data-stu-id="21fda-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="21fda-138">Waarde voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="21fda-138">On-hand value</span></span>                            | <span data-ttu-id="21fda-139">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="21fda-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="21fda-140">Numerieke waarde die groter is dan 0 (nul)</span><span class="sxs-lookup"><span data-stu-id="21fda-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="21fda-141">Een variant is vrijgegeven voor de geselecteerde locatie en u kunt aanvullende acties uitvoeren in de cel.</span><span class="sxs-lookup"><span data-stu-id="21fda-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="21fda-142">(Deze acties worden verderop in dit onderwerp nader beschreven.)</span><span class="sxs-lookup"><span data-stu-id="21fda-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="21fda-143">**0** (nul)</span><span class="sxs-lookup"><span data-stu-id="21fda-143">**0** (zero)</span></span>                             | <span data-ttu-id="21fda-144">Een variant is vrijgegeven voor de geselecteerde locatie, maar het artikel is niet beschikbaar op de geselecteerde locatie.</span><span class="sxs-lookup"><span data-stu-id="21fda-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="21fda-145">U kunt echter wel aanvullende acties uitvoeren in de cel.</span><span class="sxs-lookup"><span data-stu-id="21fda-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="21fda-146">(Deze acties worden verderop in dit onderwerp nader beschreven.)</span><span class="sxs-lookup"><span data-stu-id="21fda-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="21fda-147">**n.v.t.** of een niet-actieve cel</span><span class="sxs-lookup"><span data-stu-id="21fda-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="21fda-148">Een variant is niet vrijgegeven voor de geselecteerde locatie en u kunt geen aanvullende acties uitvoeren in de cel.</span><span class="sxs-lookup"><span data-stu-id="21fda-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="21fda-149">U kunt ook de draaitabel voor dimensies wijzigen door het selecteren van de nieuwe dimensie die moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="21fda-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![De draaitabel wijzigen](media/ChangePivot.png)

![Draaitabel gewijzigd](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="21fda-152">In de voorgaande afbeeldingen is de weergavevolgorde van de dimensies voor het geselecteerde product aangepast (niet-alfabetisch).</span><span class="sxs-lookup"><span data-stu-id="21fda-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="21fda-153">Het is gebaseerd op de weergavevolgorde van de dimensie die is ingesteld in de backoffice.</span><span class="sxs-lookup"><span data-stu-id="21fda-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="21fda-154">Verder kunnen in de weergave **Op dimensie gebaseerde matrix** meer acties worden uitgevoerd om de productiviteit van het winkelpersoneel te vergroten.</span><span class="sxs-lookup"><span data-stu-id="21fda-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="21fda-155">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="21fda-155">Here are some examples:</span></span>

- <span data-ttu-id="21fda-156">Wijzig de winkellocatie om de voorraadbeschikbaarheid van alle productvarianten op andere locaties op te zoeken.</span><span class="sxs-lookup"><span data-stu-id="21fda-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="21fda-157">Deze locaties omvatten andere winkels in de winkellocatorgroep en distributiecentra van het type **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="21fda-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="21fda-158">Verkoop een afzonderlijke productvariant aan een klant met behulp van cash-and-carry, ophalen in de winkel of verzenden naar een adres.</span><span class="sxs-lookup"><span data-stu-id="21fda-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="21fda-159">Geef de klant de ATP-informatie voor een afzonderlijke productvariant op een bepaalde locatie.</span><span class="sxs-lookup"><span data-stu-id="21fda-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Aanvullende acties op verschillende tegels](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="21fda-161">In het voorgaande voorbeeld is de weergavevolgorde van de dimensies alfabetisch, omdat de volgorde van de dimensies niet is geconfigureerd voor het geselecteerde product.</span><span class="sxs-lookup"><span data-stu-id="21fda-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="21fda-162">De volgende tabel bevat meer informatie over de aanvullende acties die beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="21fda-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="21fda-163">Actie</span><span class="sxs-lookup"><span data-stu-id="21fda-163">Action</span></span>               | <span data-ttu-id="21fda-164">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="21fda-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="21fda-165">Nu verkopen</span><span class="sxs-lookup"><span data-stu-id="21fda-165">Sell now</span></span>             | <span data-ttu-id="21fda-166">Voeg de geselecteerde artikelvariant toe aan de transactie en stuur de gebruiker door naar het transactiescherm.</span><span class="sxs-lookup"><span data-stu-id="21fda-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="21fda-167">(Deze actie is niet beschikbaar wanneer de geselecteerde locatie een distributiecentrum is.)</span><span class="sxs-lookup"><span data-stu-id="21fda-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="21fda-168">Ophalen in winkel</span><span class="sxs-lookup"><span data-stu-id="21fda-168">Pick up in store</span></span>     | <span data-ttu-id="21fda-169">Maak een klantorder voor de productvariant die wordt opgehaald bij de geselecteerde locatie en stuur de gebruiker door naar het transactiescherm.</span><span class="sxs-lookup"><span data-stu-id="21fda-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="21fda-170">(Deze actie is niet beschikbaar wanneer de geselecteerde locatie een distributiecentrum is.)</span><span class="sxs-lookup"><span data-stu-id="21fda-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="21fda-171">Product verzenden</span><span class="sxs-lookup"><span data-stu-id="21fda-171">Ship product</span></span>         | <span data-ttu-id="21fda-172">Maak een klantorder voor de productvariant die wordt verzonden naar de geselecteerde locatie en stuur de gebruiker door naar het transactiescherm.</span><span class="sxs-lookup"><span data-stu-id="21fda-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="21fda-173">Beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="21fda-173">Availability</span></span>         | <span data-ttu-id="21fda-174">Geef de ATP-informatie voor de geselecteerde combinatie van varianten voor de geselecteerde locatie weer.</span><span class="sxs-lookup"><span data-stu-id="21fda-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="21fda-175">Alle locaties weergeven</span><span class="sxs-lookup"><span data-stu-id="21fda-175">Show all locations</span></span>   | <span data-ttu-id="21fda-176">Schakel over naar de standaardzoekweergave voor voorraad en markeer de voorraadbeschikbaarheidsgegevens voor de artikelvariant voor alle winkels in de winkellocatorgroep, en ook in distributiecentra van de het type **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="21fda-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="21fda-177">Productgegevens weergeven</span><span class="sxs-lookup"><span data-stu-id="21fda-177">View product details</span></span> | <span data-ttu-id="21fda-178">Stuur de gebruiker door naar de pagina **Productdetails** van het gekoppelde productmodel.</span><span class="sxs-lookup"><span data-stu-id="21fda-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
