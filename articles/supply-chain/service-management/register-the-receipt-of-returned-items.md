---
title: De ontvangst van retourartikelen registreren
description: U kunt de ontvangst van geretourneerde artikelen registreren met het formulier Ontvangstoverzicht of Registratie.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---


# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="d295b-103">De ontvangst van retourartikelen registreren</span><span class="sxs-lookup"><span data-stu-id="d295b-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d295b-104">Er zijn twee methoden beschikbaar voor het registreren van de ontvangst van geretourneerde artikelen.</span><span class="sxs-lookup"><span data-stu-id="d295b-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="d295b-105">De eerste methode is een ontvangstproces in het magazijn dat gebruikmaakt van het formulier **Aankomstoverzicht**.</span><span class="sxs-lookup"><span data-stu-id="d295b-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="d295b-106">De tweede gebruikt het formulier **Registratie**.</span><span class="sxs-lookup"><span data-stu-id="d295b-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="d295b-107">De ontvangst van geretourneerde artikelen registreren met het formulier Overzicht aankomst</span><span class="sxs-lookup"><span data-stu-id="d295b-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="d295b-108">U kunt het formulier **Aankomstoverzicht** gebruiken om een retourzending te identificeren volgens het bijbehorende RMA-nummer (Return Material Authorization).</span><span class="sxs-lookup"><span data-stu-id="d295b-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="d295b-109">Als een journaalnaam is gedefinieerd op het tabblad **Instellen** en de journaalregels die overeenkomen met de regels die zijn geselecteerd op het formulier **Aankomstoverzicht** bestaan, wordt een nieuwe journaalkop gemaakt wanneer u klikt op **Begin aankomst**.</span><span class="sxs-lookup"><span data-stu-id="d295b-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="d295b-110">Klik op **Voorraadbeheer** \> **Periodiek** \> **Overzicht aankomst**.</span><span class="sxs-lookup"><span data-stu-id="d295b-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="d295b-111">Selecteer in het veld **Naam instelling** **Retourorder** en klik vervolgens op **Update**.</span><span class="sxs-lookup"><span data-stu-id="d295b-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="d295b-112">U kunt de <STRONG>Bereik</STRONG>-velden gebruiken om de zoekresultaten te beperken.</span><span class="sxs-lookup"><span data-stu-id="d295b-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="d295b-113">U kunt het RMA-nummer typen of selecteren in het veld <STRONG>RMA-nummer</STRONG> voor een exact resultaat.</span><span class="sxs-lookup"><span data-stu-id="d295b-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="d295b-114">Als u een reeks filters wilt definiëren en opslaan waarmee wordt beperkt welke inkomende ontvangsten worden weergegeven, klikt u op het tabblad <STRONG>Instellen</STRONG>. De beschikbare filters zijn typen, magazijnen en docks.</span><span class="sxs-lookup"><span data-stu-id="d295b-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="d295b-115">Retourorders kunnen niet worden gecombineerd met andere aankomsttypen in het formulier <STRONG>Aankomstoverzicht</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d295b-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="d295b-116">Daarom de verkooporder altijd de referentie zijn, maar wordt er geen verkooporder-ID opgegeven op de journaalkop.</span><span class="sxs-lookup"><span data-stu-id="d295b-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="d295b-117">Zoek in het raster **Ontvangsten** naar de regel die overeenkomt met het artikel dat wordt geretourneerd en schakel het selectievakje in de kolom **Selecteren voor aankomst** in.</span><span class="sxs-lookup"><span data-stu-id="d295b-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="d295b-118">Als u bepaalde regels, zoals artikelen uit de oorspronkelijke order die niet zijn opgenomen in de retourzending, wilt uitsluiten van de retourontvangst, schakelt u de bijbehorende selectievakjes **Selecteren voor aankomst** in de tabel **Regels** in het onderste gedeelte van het formulier uit.</span><span class="sxs-lookup"><span data-stu-id="d295b-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="d295b-119">Klik op de knop **Begin aankomst** om een aankomstjournaal te maken.</span><span class="sxs-lookup"><span data-stu-id="d295b-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d295b-120">U kunt meerdere retourorders selecteren en deze opnemen in één aankomstproces.</span><span class="sxs-lookup"><span data-stu-id="d295b-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="d295b-121">Elke retourorderregel wordt gekopieerd naar een overeenkomstige aankomstjournaalregel.</span><span class="sxs-lookup"><span data-stu-id="d295b-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="d295b-122">U kunt ook handmatig een aankomstjournaal maken met het formulier <STRONG>Artikelontvangst</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d295b-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="d295b-123">Ga naar **Voorraadbeheer** \> **Journaalposten** \> **Artikelontvangst** \> **Artikelontvangst**.</span><span class="sxs-lookup"><span data-stu-id="d295b-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="d295b-124">Selecteer het aankomstjournaal dat u zojuist hebt gemaakt en klik vervolgens op **Regels** om het formulier **Journaalregels, locaties** te openen.</span><span class="sxs-lookup"><span data-stu-id="d295b-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="d295b-125">Pas op het tabblad **Algemeen** het nummer aan in het veld **Hoeveelheid** indien dit nodig is en wijs vervolgens een beschikkingscode toe in het veld **Beschikkingscode**.</span><span class="sxs-lookup"><span data-stu-id="d295b-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="d295b-126">U kunt ook het selectievakje **Quarantainebeheer** inschakelen om de geretourneerde artikelen een inspectieproces te laten ondergaan in het kader van een quarantaineorder.</span><span class="sxs-lookup"><span data-stu-id="d295b-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d295b-127">Als u de geretourneerde artikelen in quarantaine plaatst, kunt u geen beschikkingscode opgeven.</span><span class="sxs-lookup"><span data-stu-id="d295b-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="d295b-128">Klik op de knop **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="d295b-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="d295b-129">Klik op **Boeken** als het validatieproces geen fouten bevat.</span><span class="sxs-lookup"><span data-stu-id="d295b-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="d295b-130">De ontvangst van geretourneerde artikelen registreren met het registratieformulier.</span><span class="sxs-lookup"><span data-stu-id="d295b-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="d295b-131">Als alternatief voor het formulier **Aankomstoverzicht** kunt u het formulier **Registratie** gebruiken om de aankomst van geretourneerde artikelen te registreren.</span><span class="sxs-lookup"><span data-stu-id="d295b-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="d295b-132">Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.</span><span class="sxs-lookup"><span data-stu-id="d295b-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="d295b-133">Een nieuwe retourorder maken of de retourorder openen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d295b-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="d295b-134">Selecteer de retourorderregel op het sneltabblad **Regels**.</span><span class="sxs-lookup"><span data-stu-id="d295b-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="d295b-135">Klik op **Regel bijwerken** en klik vervolgens op **Registratie**.</span><span class="sxs-lookup"><span data-stu-id="d295b-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="d295b-136">Wijs een beschikkingscode toe in het veld **Beschikkingscode** en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d295b-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d295b-137">Het is niet mogelijk het artikel te verzenden voor inspectie als een quarantaineorder met het formulier <STRONG>Registratie</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d295b-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="d295b-138">Selecteer in het raster **Transacties** de transactie die moet worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="d295b-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="d295b-139">Klik in het raster **Nu registreren** op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d295b-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="d295b-140">Herhaal de vorige twee stappen totdat alle geretourneerde artikelen worden weergegeven in het raster **Nu registreren**.</span><span class="sxs-lookup"><span data-stu-id="d295b-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="d295b-141">Klik op **Alles boeken**.</span><span class="sxs-lookup"><span data-stu-id="d295b-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d295b-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d295b-142">See also</span></span>

<span data-ttu-id="d295b-143">[Overzicht aankomst (formulier)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d295b-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  



