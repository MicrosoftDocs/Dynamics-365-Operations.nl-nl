---
title: Een Excel-werkmap maken om detailhandelstransacties te bewerken
description: In dit onderwerp wordt beschreven hoe u een Excel-werkmap maakt zodat u detailhandelstransacties in Microsoft Dynamics 365 Commerce kunt bewerken.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a2d41dd0470a4abae1a8238be8f1549fb094a026
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795734"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="fc00a-103">Een Excel-werkmap maken om detailhandelstransacties te bewerken</span><span class="sxs-lookup"><span data-stu-id="fc00a-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc00a-104">In dit onderwerp wordt beschreven hoe u een Excel-werkmap maakt zodat u detailhandelstransacties in Microsoft Dynamics 365 Commerce kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="fc00a-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fc00a-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="fc00a-105">Overview</span></span>

<span data-ttu-id="fc00a-106">Er is een vooraf gedefinieerde Excel-sjabloon die door klanten kan worden geopend vanuit verschillende delen van het systeem en waarmee detailhandelstransacties kunnen worden bewerkt en gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="fc00a-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="fc00a-107">Klanten kunnen echter ook een aangepaste Excel-werkmap maken voor dit doeleinde.</span><span class="sxs-lookup"><span data-stu-id="fc00a-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="fc00a-108">Een Excel-werkmap maken en configureren</span><span class="sxs-lookup"><span data-stu-id="fc00a-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="fc00a-109">Voer de volgende stappen uit om een Excel-werkmap te maken en te configureren zodat u detailhandelstransacties kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="fc00a-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="fc00a-110">Open Excel en maak een lege werkmap.</span><span class="sxs-lookup"><span data-stu-id="fc00a-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="fc00a-111">Selecteer **Mijn invoegtoepassingen** op het tabblad **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="fc00a-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="fc00a-112">Selecteer in het rechterdeelvenster de koppeling **Serverinformatie toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fc00a-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="fc00a-113">Voer de server-URL in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc00a-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="fc00a-114">Als het foutbericht Geen appletregistraties gevonden wordt weergegeven, voert u de volgende stappen uit om het probleem op te lossen:</span><span class="sxs-lookup"><span data-stu-id="fc00a-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="fc00a-115">Ga in Commerce naar **Systeembeheer \> Instellen \> Parameters voor Office-app**.</span><span class="sxs-lookup"><span data-stu-id="fc00a-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="fc00a-116">Selecteer **App-parameters initialiseren** op het sneltabblad **Parameters voor app**.</span><span class="sxs-lookup"><span data-stu-id="fc00a-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="fc00a-117">Selecteer **OK** in het vak met het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="fc00a-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="fc00a-118">Selecteer op het sneltabblad **Geregistreerde applets** de optie **Registratie van applet initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="fc00a-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="fc00a-119">Herhaal indien nodig de vorige drie stappen.</span><span class="sxs-lookup"><span data-stu-id="fc00a-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="fc00a-120">Selecteer **Ontwerpen** en vervolgens **Tabel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fc00a-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="fc00a-121">Selecteer op basis van de gegevens die moeten worden gewijzigd, de entiteiten die voor bewerking moeten worden toegevoegd aan de Excel-werkmap.</span><span class="sxs-lookup"><span data-stu-id="fc00a-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="fc00a-122">Gebruik de volgende tabel als verwijzing.</span><span class="sxs-lookup"><span data-stu-id="fc00a-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="fc00a-123">Transactietype</span><span class="sxs-lookup"><span data-stu-id="fc00a-123">Transaction type</span></span> | <span data-ttu-id="fc00a-124">Te gebruiken gegevensentiteiten</span><span class="sxs-lookup"><span data-stu-id="fc00a-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="fc00a-125">Contante transacties, online orders, asynchrone klantorders, asynchrone klantoffertes</span><span class="sxs-lookup"><span data-stu-id="fc00a-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="fc00a-126">Transactie (controleerbaar), verkooptransactie (controleerbaar), betalingstransacties (controleerbaar), btw-transacties (controleerbaar), kortingstransacties (controleerbaar), toeslagentransacties (controleerbaar)</span><span class="sxs-lookup"><span data-stu-id="fc00a-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="fc00a-127">Bankstorting</span><span class="sxs-lookup"><span data-stu-id="fc00a-127">Bank drop</span></span> | <span data-ttu-id="fc00a-128">Transactie (controleerbaar), bankstortingstransacties (controleerbaar)</span><span class="sxs-lookup"><span data-stu-id="fc00a-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="fc00a-129">Kluisstorting</span><span class="sxs-lookup"><span data-stu-id="fc00a-129">Safe drop</span></span> | <span data-ttu-id="fc00a-130">Transactie (controleerbaar), kluisstortingstransacties (controleerbaar)</span><span class="sxs-lookup"><span data-stu-id="fc00a-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="fc00a-131">Kascontrole</span><span class="sxs-lookup"><span data-stu-id="fc00a-131">Tender declaration</span></span> | <span data-ttu-id="fc00a-132">Transactie (controleerbaar), kascontroletransacties (controleerbaar)</span><span class="sxs-lookup"><span data-stu-id="fc00a-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="fc00a-133">Inkomsten, onkosten</span><span class="sxs-lookup"><span data-stu-id="fc00a-133">Income, Expense</span></span> | <span data-ttu-id="fc00a-134">Transactie (controleerbaar), inkomsten-/onkostentransacties (controleerbaar), betalingstransacties (controleerbaar)</span><span class="sxs-lookup"><span data-stu-id="fc00a-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="fc00a-135">Beginbedrag declareren, betalingsmethode verwijderen, wisselgeldinvoer, betalingsmethode wijzigen, factuurbetaling, klantstorting</span><span class="sxs-lookup"><span data-stu-id="fc00a-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="fc00a-136">Transactie (controleerbaar), betalingstransacties (controleerbaar)</span><span class="sxs-lookup"><span data-stu-id="fc00a-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="fc00a-137">Het is belangrijk dat u slechts één gegevensentiteit toevoegt aan elke Excel-werkmap.</span><span class="sxs-lookup"><span data-stu-id="fc00a-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="fc00a-138">Bovendien moeten alle velden die met een sleutelsymbool zijn gemarkeerd, aan de desbetreffende werkmap worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fc00a-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="fc00a-139">Nadat de werkmap is geconfigureerd, past u de vereiste filters toe.</span><span class="sxs-lookup"><span data-stu-id="fc00a-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="fc00a-140">Zorg ervoor dat u dezelfde filters toepast op alle werkbladen in het bestand.</span><span class="sxs-lookup"><span data-stu-id="fc00a-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="fc00a-141">Vermijd het laden van zeer grote hoeveelheden gegevens in het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="fc00a-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="fc00a-142">Anders kan dit gevolgen hebben voor de prestaties en kunnen Excel en het systeem trager worden.</span><span class="sxs-lookup"><span data-stu-id="fc00a-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="fc00a-143">Het is raadzaam om altijd Bedrijf en Overzichtsnummer of Transactienummer te gebruiken als filters voor uw bestand.</span><span class="sxs-lookup"><span data-stu-id="fc00a-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="fc00a-144">Nadat de filters zijn geconfigureerd, selecteert u **Vernieuwen** om de gegevens te laden.</span><span class="sxs-lookup"><span data-stu-id="fc00a-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="fc00a-145">Bewerk de vereiste gegevens en publiceer ze.</span><span class="sxs-lookup"><span data-stu-id="fc00a-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="fc00a-146">Als de knop **Publiceren** niet beschikbaar is, zijn sommige belangrijke velden waarschijnlijk niet toegevoegd aan de Excel-werkmap.</span><span class="sxs-lookup"><span data-stu-id="fc00a-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc00a-147">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="fc00a-147">Additional resources</span></span>

[<span data-ttu-id="fc00a-148">Beheer van contante transacties bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="fc00a-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="fc00a-149">Online orders en asynchrone ordertransacties van klanten bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="fc00a-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="fc00a-150">Financiële dimensies voor detailhandelstransacties bewerken</span><span class="sxs-lookup"><span data-stu-id="fc00a-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="fc00a-151">Velden toevoegen aan een Excel-werkmap om detailhandelstransacties te bewerken</span><span class="sxs-lookup"><span data-stu-id="fc00a-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]