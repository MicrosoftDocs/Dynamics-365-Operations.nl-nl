---
title: Redencodes voor voorraadtelling
description: Dit onderwerp beschrijft hoe u redencodes instelt en toepast voor teltaken.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0d787dac50374af11d878652103145c9ae9b6877
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="adc64-103">Redencodes voor voorraadtelling</span><span class="sxs-lookup"><span data-stu-id="adc64-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adc64-104">Met redencodes kunt u de resultaten analyseren van een tellingsproces en eventuele verschillen die tijdens dat proces optreden.</span><span class="sxs-lookup"><span data-stu-id="adc64-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="adc64-105">U kunt de reden voor het uitvoeren van de telling opgeven, zoals een gebroken pallet of een voorraadcorrectie die is gebaseerd op voorraadmonsters.</span><span class="sxs-lookup"><span data-stu-id="adc64-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="adc64-106">Aanbeveling</span><span class="sxs-lookup"><span data-stu-id="adc64-106">Recommendation</span></span>

<span data-ttu-id="adc64-107">Voordat u het systeem instelt, wordt aangeraden om een strategie voor het werken met redencodes te definiëren.</span><span class="sxs-lookup"><span data-stu-id="adc64-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="adc64-108">Probeer bijvoorbeeld de volgende vragen te beantwoorden:</span><span class="sxs-lookup"><span data-stu-id="adc64-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="adc64-109">Moeten redencodes verplicht zijn in magazijnen?</span><span class="sxs-lookup"><span data-stu-id="adc64-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="adc64-110">Moeten redencodes verplicht of optioneel zijn voor bepaalde artikelen?</span><span class="sxs-lookup"><span data-stu-id="adc64-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="adc64-111">Hoeveel redencodes hebt u nodig?</span><span class="sxs-lookup"><span data-stu-id="adc64-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="adc64-112">Hoe moeten gebruikers van streepjescodescanners redencodes gebruiken?</span><span class="sxs-lookup"><span data-stu-id="adc64-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="adc64-113">Moeten de redencodes vooraf worden geselecteerd, verplicht zijjn en niet kunnen worden bewerkt?</span><span class="sxs-lookup"><span data-stu-id="adc64-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="adc64-114">Hebben magazijnmedewerkers andere redencodegedrag nodig voor mobiele scanners?</span><span class="sxs-lookup"><span data-stu-id="adc64-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="adc64-115">Als het antwoord Ja is, kunt u meer menu-items maken en deze toewijzen aan verschillende personen.</span><span class="sxs-lookup"><span data-stu-id="adc64-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="adc64-116">Waar redencodes toepassen</span><span class="sxs-lookup"><span data-stu-id="adc64-116">Where reason codes apply</span></span>

<span data-ttu-id="adc64-117">U kunt meerdere redencodebeleidsregels maken en elk redencodebeleid kan twee redencodebeleidsregels voor tellingen hebben.</span><span class="sxs-lookup"><span data-stu-id="adc64-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="adc64-118">Het redencodebeleid voor tellingen kan worden gebruikt op magazijn- of artikelniveau.</span><span class="sxs-lookup"><span data-stu-id="adc64-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="adc64-119">Redencodebeleid instellen</span><span class="sxs-lookup"><span data-stu-id="adc64-119">Set up reason code policies</span></span>

1. <span data-ttu-id="adc64-120">Selecteer **Voorraadbeheer** \> **Instellen** \> **Voorraad** \> **Beleid van redencode voor telling** en maak een nieuw beleid voor de redencode.</span><span class="sxs-lookup"><span data-stu-id="adc64-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="adc64-121">Selecteer in het veld **Type redencode voor telling** de optie **Verplicht** of **Optioneel** om op te geven of de selectie van een redencode een optionele of verplichte actie moet zijn in een van de volgende tellijsten:</span><span class="sxs-lookup"><span data-stu-id="adc64-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="adc64-122">Cyclustelling (mobiel apparaat)</span><span class="sxs-lookup"><span data-stu-id="adc64-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="adc64-123">Plaatscyclustelling (mobiel apparaat)</span><span class="sxs-lookup"><span data-stu-id="adc64-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="adc64-124">Drempeltelling (mobiel apparaat)</span><span class="sxs-lookup"><span data-stu-id="adc64-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="adc64-125">Correctie-invoer (mobiel apparaat)</span><span class="sxs-lookup"><span data-stu-id="adc64-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="adc64-126">Correctie-uitvoer (mobiel apparaat)</span><span class="sxs-lookup"><span data-stu-id="adc64-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="adc64-127">Tellijst (rich client)</span><span class="sxs-lookup"><span data-stu-id="adc64-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="adc64-128">U kunt ook redencodes instellen voor afzonderlijke magazijnen en producten.</span><span class="sxs-lookup"><span data-stu-id="adc64-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="adc64-129">De instelling van redencodes voor producten kunt de instelling voor magazijnen negeren.</span><span class="sxs-lookup"><span data-stu-id="adc64-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="adc64-130">Verplichte redencodes</span><span class="sxs-lookup"><span data-stu-id="adc64-130">Mandatory reason codes</span></span>

<span data-ttu-id="adc64-131">Als de parameter **Verplicht** is ingesteld in de configuratie van redencodes voor magazijnen of artikelen, kan de tellijst niet worden voltooid en afgesloten tot een redencode is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="adc64-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="adc64-132">Redencodes instellen voor magazijnen</span><span class="sxs-lookup"><span data-stu-id="adc64-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="adc64-133">Slecteer **Voorraadbeheer** \> **Instellingen** \> **Opsplitsing van voorraad** \> **Magazijnen**</span><span class="sxs-lookup"><span data-stu-id="adc64-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="adc64-134">Op het tabblad **Magazijn** in het veld **Beleid van redencode voor telling** selecteert u een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="adc64-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="adc64-135">**Leeg**: de parameter die is ingesteld voor het artikel wordt gebruikt om te bepalen of de tellijsten verplicht zijn voor het product.</span><span class="sxs-lookup"><span data-stu-id="adc64-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="adc64-136">**Verplicht**: een redencode is altijd vereist voor tellijsten voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="adc64-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="adc64-137">**Optioneel**: een redencode is niet vereist voor tellijsten voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="adc64-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="adc64-138">Redencodes instellen voor producten</span><span class="sxs-lookup"><span data-stu-id="adc64-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="adc64-139">Selecteer **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="adc64-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="adc64-140">Op het tabblad **Product** selecteert u **Beleid van redencode voor telling** en vervolgens een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="adc64-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="adc64-141">**Leeg**: de parameter die is ingesteld voor het magazijn wordt gebruikt om te bepalen of de tellijsten verplicht zijn voor het product.</span><span class="sxs-lookup"><span data-stu-id="adc64-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="adc64-142">**Verplicht**: een redencode is altijd vereist voor tellijsten voor het product.</span><span class="sxs-lookup"><span data-stu-id="adc64-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="adc64-143">Deze instelling overschrijft de instelling van redencodes op magazijnniveau.</span><span class="sxs-lookup"><span data-stu-id="adc64-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="adc64-144">**Optioneel**: een redencode is niet vereist voor tellijsten voor het product.</span><span class="sxs-lookup"><span data-stu-id="adc64-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="adc64-145">Deze instelling overschrijft de instelling van redencodes op magazijnniveau.</span><span class="sxs-lookup"><span data-stu-id="adc64-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="adc64-146">Redencodes gebruiken in tellijsten</span><span class="sxs-lookup"><span data-stu-id="adc64-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="adc64-147">In een tellijst kunt u redencodes van de volgende typen toevoegen:</span><span class="sxs-lookup"><span data-stu-id="adc64-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="adc64-148">Cyclustelling</span><span class="sxs-lookup"><span data-stu-id="adc64-148">Cycle Count</span></span>
- <span data-ttu-id="adc64-149">Spotcyclustelling</span><span class="sxs-lookup"><span data-stu-id="adc64-149">Spot Count</span></span>
- <span data-ttu-id="adc64-150">Drempeltelling</span><span class="sxs-lookup"><span data-stu-id="adc64-150">Threshold Count</span></span>
- <span data-ttu-id="adc64-151">Correctie-invoer</span><span class="sxs-lookup"><span data-stu-id="adc64-151">Adjustment In</span></span>
- <span data-ttu-id="adc64-152">Correctie-uitvoer</span><span class="sxs-lookup"><span data-stu-id="adc64-152">Adjustment Out</span></span>

<span data-ttu-id="adc64-153">Redencodes worden toegevoegd aan de regels in tellijsten van het type **tellijst**.</span><span class="sxs-lookup"><span data-stu-id="adc64-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="adc64-154">Selecteer **Voorraadbeheer** \> **Journaalposten** \> **Artikeltelling** \> **Telling**.</span><span class="sxs-lookup"><span data-stu-id="adc64-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="adc64-155">In de regeldetails van de tellijst selecteert u een optie in het veld **Redencode voor telling**.</span><span class="sxs-lookup"><span data-stu-id="adc64-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="adc64-156">De telhistorie weergeven, zoals is vastgelegd door redencodes</span><span class="sxs-lookup"><span data-stu-id="adc64-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="adc64-157">Selecteer **Voorraadbeheer** \> **Query's en rapporten** \> **Telhistorie**, en geef in het veld **Redencode voor telling** de telhistorie weer die is geregistreerd via een redencode.</span><span class="sxs-lookup"><span data-stu-id="adc64-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="adc64-158">Een redencode gebruiken voor hoeveelheidcorrectie</span><span class="sxs-lookup"><span data-stu-id="adc64-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="adc64-159">Selecteer op de pagina **Voorhanden voorraad** **Hoeveelheid aanpassen**.</span><span class="sxs-lookup"><span data-stu-id="adc64-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="adc64-160">U kunt de pagina **Voorhanden voorraad** op verschillende manieren openen.</span><span class="sxs-lookup"><span data-stu-id="adc64-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="adc64-161">Selecteer bijvoorbeeld **Voorraadbeheer** \> **Query's en rapporten** \> **Voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="adc64-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="adc64-162">Selecteer **Hoeveelheid aanpassen** en selecteer in het veld **Redencode voor telling** een redencode.</span><span class="sxs-lookup"><span data-stu-id="adc64-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="adc64-163">Redencodes voor menuopties op mobiele apparaten configureren</span><span class="sxs-lookup"><span data-stu-id="adc64-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="adc64-164">U kunt redencodes configureren voor elk type telling in een menuoptie op een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="adc64-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="adc64-165">De configuratie van de menuoptie voor het mobiele apparaat bevat de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="adc64-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="adc64-166">Of de redencode tijdens de telling wordt weergegeven aan de werknemer met het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="adc64-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="adc64-167">De standaardredencode die wordt weergegeven in een menuoptie op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="adc64-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="adc64-168">Of de gebruiker de redencode kan bewerken.</span><span class="sxs-lookup"><span data-stu-id="adc64-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="adc64-169">Redencodes op een mobiel apparaat instellen</span><span class="sxs-lookup"><span data-stu-id="adc64-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="adc64-170">Selecteer **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="adc64-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="adc64-171">Selecteer op het tabblad **Cyclus tellen** de optie **Cyclustelling**.</span><span class="sxs-lookup"><span data-stu-id="adc64-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="adc64-172">Stel in het veld **Standaard redencode voor telling** de standaardredencode in die moet worden vastgelegd wanneer het tellen wordt uitgevoerd met behulp van de menuoptie op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="adc64-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="adc64-173">Selecteer in het veld **Redencode voor telling weergeven** de optie **Regel** om de redencode weer te geven nadat elke afwijking is vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="adc64-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="adc64-174">U kunt ook **Verbergen** selecteren als de redencode niet moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="adc64-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="adc64-175">Stel de optie **Redencode voor telling bewerken** in op **Ja** of **Nee**.</span><span class="sxs-lookup"><span data-stu-id="adc64-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="adc64-176">Als u deze optie instelt op **Ja**, kan de werknemer de redencode bewerken wanneer deze wordt weergegeven op het mobiele apparaat tijdens de telling.</span><span class="sxs-lookup"><span data-stu-id="adc64-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="adc64-177">De knop **Cyclustelling** kan worden ingeschakeld voor elke menuoptie op het mobiele apparaat waarmee de telling kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="adc64-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="adc64-178">Dit kunnen menuopties zijn voor spotcyclustellingen, door de gebruiker uitgevoerd werk of door het systeem uitgevoerd werk.</span><span class="sxs-lookup"><span data-stu-id="adc64-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="adc64-179">Cyclustelling goedkeuren</span><span class="sxs-lookup"><span data-stu-id="adc64-179">Cycle count approvals</span></span>

<span data-ttu-id="adc64-180">Voordat een telling wordt goedgekeurd, kan de gebruiker de redencode wijzigen die is gekoppeld aan de telling.</span><span class="sxs-lookup"><span data-stu-id="adc64-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="adc64-181">Als de telling is goedgekeurd, wordt de redencode ingevoerd in de regels van de tellijst.</span><span class="sxs-lookup"><span data-stu-id="adc64-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="adc64-182">Goedkeuring van cyclustelling wijzigen</span><span class="sxs-lookup"><span data-stu-id="adc64-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="adc64-183">Selecteer **Magazijnbeheer** \> **Cyclustelling** \> **Cyclustellingswerk in afwachting van controle**.</span><span class="sxs-lookup"><span data-stu-id="adc64-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="adc64-184">Selecteer **Cyclustelling** en selecteer in het veld **Redencode** een nieuwe redencode.</span><span class="sxs-lookup"><span data-stu-id="adc64-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="adc64-185">De menuoptie op het mobiele apparaat wijzigen voor Correctie-invoer en Correctie-uitvoer</span><span class="sxs-lookup"><span data-stu-id="adc64-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="adc64-186">Selecteer **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat** en selecteer vervolgens **Correctie invoer en uitvoer**.</span><span class="sxs-lookup"><span data-stu-id="adc64-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="adc64-187">Stel de optie **Bestaand werk gebruiken** in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="adc64-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="adc64-188">Selecteer in het veld **Proces van werkaanmaak** de optie **Correctie-invoer**.</span><span class="sxs-lookup"><span data-stu-id="adc64-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="adc64-189">De volgende velden worden toegevoegd aan de menuoptie op het mobiele apparaat wanneer **Correctie-invoer** of **Correctie-uitvoer** wordt geselecteerd tijdens het maken van werk:</span><span class="sxs-lookup"><span data-stu-id="adc64-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="adc64-190">Standaard redencode voor telling</span><span class="sxs-lookup"><span data-stu-id="adc64-190">Default counting reason code</span></span>
- <span data-ttu-id="adc64-191">Redencode voor telling weergeven</span><span class="sxs-lookup"><span data-stu-id="adc64-191">Display counting reason code</span></span>
- <span data-ttu-id="adc64-192">Redencode voor telling bewerken</span><span class="sxs-lookup"><span data-stu-id="adc64-192">Edit counting reason code</span></span>

