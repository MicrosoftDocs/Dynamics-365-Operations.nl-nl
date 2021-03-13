---
title: Een inkoopovereenkomst maken
description: Dit onderwerp begeleidt u door het maken van een inkoopovereenkomst.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92c9b429a05a2c25672cc14a0c9ee7adfef42631
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016826"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="a86c7-103">Een inkoopovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="a86c7-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a86c7-104">Dit onderwerp begeleidt u door het maken van een inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="a86c7-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="a86c7-105">Dit wordt gewoonlijk gedaan door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="a86c7-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="a86c7-106">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="a86c7-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a86c7-107">U moet de classificaties van inkoopovereenkomsten hebben ingesteld voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="a86c7-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="a86c7-108">Nadat u een overeenkomst hebt gemaakt, kunt u deze gebruiken wanneer u een inkooporder maakt. De voorwaarden van de inkoopovereenkomst worden dan gekopieerd naar de koptekst en naar regels in de order die door de overeenkomst worden beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="a86c7-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="a86c7-109">Een nieuwe inkoopovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="a86c7-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="a86c7-110">Ga naar **Navigatievenster > Modules > Inkoopbeheer > Inkoopovereenkomsten > Inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="a86c7-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-111">Click **New**.</span></span>
3. <span data-ttu-id="a86c7-112">Selecteer in het veld **Leveranciersrekening** de vervolgkeuzelijst en selecteer de nieuwe rij de gewenste record.</span><span class="sxs-lookup"><span data-stu-id="a86c7-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="a86c7-113">Selecteer in het veld **Classificatie van inkoopovereenkomst** de vervolgkeuzelijst en selecteer de nieuwe rij de gewenste record.</span><span class="sxs-lookup"><span data-stu-id="a86c7-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="a86c7-114">Vouw de het sneltabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="a86c7-115">Voer een datum in het veld **Vervaldatum** in.</span><span class="sxs-lookup"><span data-stu-id="a86c7-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="a86c7-116">Deze vervaldatum wordt de standaardwaarde voor alle toezeggingsregels zijn en bepaalt hoe lang elke specifieke toezegging geldig is.</span><span class="sxs-lookup"><span data-stu-id="a86c7-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="a86c7-117">Typ in het veld **Documenttitel** een naam voor uw inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="a86c7-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="a86c7-118">Laat het veld **Standaardtoezegging** ingesteld op **Toezegging producthoeveelheid** (of wijzig het als het hier niet op is ingesteld).</span><span class="sxs-lookup"><span data-stu-id="a86c7-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="a86c7-119">De waarde van de standaardtoezegging bepaalt uw opties op de overeenkomstregels.</span><span class="sxs-lookup"><span data-stu-id="a86c7-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="a86c7-120">Als u een nieuw toezeggingstype nodig hebt wanneer u de overeenkomstregels maakt, moet u de standaardtoezegging in de koptekst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a86c7-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="a86c7-121">Er zijn 4 typen toezeggingen: **Toezegging producthoeveelheid** - voor een bepaalde hoeveelheid van een product; **Toezegging productwaarde** - voor een specifiek valutabedrag van een product; **Waardetoezegging productcategorie** - voor een specifiek valutabedrag in een aanschaffingscategorie waar het bedrag voor een catalogusartikel of een niet-catalogus artikel kan zijn; **Waardetoezegging** - voor een specifiek valutabedrag dat kan worden afgehandeld door elk product of elke aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="a86c7-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="a86c7-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="a86c7-123">Een toezegging toevoegen</span><span class="sxs-lookup"><span data-stu-id="a86c7-123">Add a commitment</span></span>
1. <span data-ttu-id="a86c7-124">Selecteer **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-124">Select **Add line**.</span></span>
2. <span data-ttu-id="a86c7-125">Selecteer in het veld **Artikelnummer** de gewenste record in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="a86c7-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="a86c7-126">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="a86c7-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="a86c7-127">Dit is de totale hoeveelheid die u bent overeengekomen te kopen van uw leverancier.</span><span class="sxs-lookup"><span data-stu-id="a86c7-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="a86c7-128">Voer een nummer in het veld **Eenheidsprijs** in.</span><span class="sxs-lookup"><span data-stu-id="a86c7-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="a86c7-129">Vouw de sectie **Regeldetails** uit.</span><span class="sxs-lookup"><span data-stu-id="a86c7-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="a86c7-130">Stel de optie **Max is afgedwongen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="a86c7-131">De optie **Max is afgedwongen** beperkt het gebruik van de toezegging.</span><span class="sxs-lookup"><span data-stu-id="a86c7-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="a86c7-132">U kunt slechts maximaal de hoeveelheid kopen die is opgegeven in het veld **Hoeveelheid** voor de regel.</span><span class="sxs-lookup"><span data-stu-id="a86c7-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="a86c7-133">Koptekstvoorwaarden toevoegen</span><span class="sxs-lookup"><span data-stu-id="a86c7-133">Add header conditions</span></span>
1. <span data-ttu-id="a86c7-134">Selecteer **Opties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a86c7-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="a86c7-135">Selecteer **Weergave wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-135">Select **Change view**.</span></span>
3. <span data-ttu-id="a86c7-136">Selecteer **Weergave kopteksten**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-136">Select **Header view**.</span></span>
4. <span data-ttu-id="a86c7-137">Vouw de sectie **Voorwaarden** uit.</span><span class="sxs-lookup"><span data-stu-id="a86c7-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="a86c7-138">Selecteer in het veld **Betalingsmethode** de gewenste record in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="a86c7-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="a86c7-139">De betalingsvoorwaarden van de leverancierrekening worden hier standaard weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a86c7-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="a86c7-140">Selecteer in het veld **Leveringsmethode** de gewenste record in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="a86c7-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="a86c7-141">Selecteer in het veld **Leveringsvoorwaarden** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="a86c7-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="a86c7-142">De verkoopovereenkomst bevestigen en activeren</span><span class="sxs-lookup"><span data-stu-id="a86c7-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="a86c7-143">Klik in het actievenster op **Inkoopovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="a86c7-144">Selecteer **Bevestiging**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-144">Select **Confirmation**.</span></span> <span data-ttu-id="a86c7-145">Stel de optie **Overeenkomst als effectief markeren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="a86c7-146">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-146">Select **OK**.</span></span>
4. <span data-ttu-id="a86c7-147">Klik in het actievenster op **Inkoopovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="a86c7-148">Selecteer **Bevestigingen van inkoopovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="a86c7-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="a86c7-149">Met de optie **Voorbeeld/afdrukken** kunt u een document voor de inkoopovereenkomst genereren dat u vervolgens kunt afdrukken of naar de leverancier kunt verzenden.</span><span class="sxs-lookup"><span data-stu-id="a86c7-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="a86c7-150">Als u de overeenkomst later wilt bijwerken en opnieuw wilt bevestigen, worden hier beide versies weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a86c7-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="a86c7-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a86c7-151">Close the page.</span></span>

