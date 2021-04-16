---
title: Orderwachtstanden beheren
description: In deze procedure wordt uitgelegd hoe klantverkooporders in de wachtstand kunnen worden geplaatst, hoe u een order in de wachtstand uitcheckt en hoe u orderwachtstanden verwijdert.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0a6acbc55a69f854463e72391fb0fff4dfb459c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817720"
---
# <a name="manage-order-holds"></a><span data-ttu-id="597f5-103">Orderwachtstanden beheren</span><span class="sxs-lookup"><span data-stu-id="597f5-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="597f5-104">In deze procedure wordt uitgelegd hoe klantverkooporders in de wachtstand kunnen worden geplaatst, hoe u een order in de wachtstand uitcheckt en hoe u orderwachtstanden verwijdert.</span><span class="sxs-lookup"><span data-stu-id="597f5-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="597f5-105">Een order kan in wachtstand worden geplaatst om diverse redenen.</span><span class="sxs-lookup"><span data-stu-id="597f5-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="597f5-106">U kunt bijvoorbeeld een order in de wachtstand plaatsen tot een klantadres of betalingsmethode kan worden geverifieerd of tot een manager de kredietlimiet van de klant kan controleren.</span><span class="sxs-lookup"><span data-stu-id="597f5-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="597f5-107">Zolang de order in de wachtstand staat, kan deze niet worden verwerkt door het magazijn voor verzending.</span><span class="sxs-lookup"><span data-stu-id="597f5-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="597f5-108">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="597f5-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="597f5-109">Order in wachtstand instellen</span><span class="sxs-lookup"><span data-stu-id="597f5-109">Set up order holds</span></span>
1. <span data-ttu-id="597f5-110">Ga naar **Navigatievenster > Modules > Verkoop en marketing > Instellen > Verkooporders > Orderwachtstandcodes**.</span><span class="sxs-lookup"><span data-stu-id="597f5-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="597f5-111">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="597f5-111">Click **New**.</span></span>
3. <span data-ttu-id="597f5-112">Typ een waarde in het veld **Wachtstandcode**.</span><span class="sxs-lookup"><span data-stu-id="597f5-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="597f5-113">Typ bijvoorbeeld 'Terugbellen.</span><span class="sxs-lookup"><span data-stu-id="597f5-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="597f5-114">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="597f5-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="597f5-115">Bijvoorbeeld: Order in wachtstand, wacht tot klant terugbelt.</span><span class="sxs-lookup"><span data-stu-id="597f5-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="597f5-116">Schakel eventueel het selectievakje **Reserveringen verwijderen** in, zodat alle fysieke reserveringen uit de order worden verwijderd wanneer deze wachtstandcode wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="597f5-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="597f5-117">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="597f5-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="597f5-118">Order in wachtstand plaatsen</span><span class="sxs-lookup"><span data-stu-id="597f5-118">Place order on hold</span></span>
1. <span data-ttu-id="597f5-119">Ga naar **Navigatievenster > Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="597f5-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="597f5-120">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="597f5-120">Click **New**.</span></span>
3. <span data-ttu-id="597f5-121">Typ of selecteer een waarde in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="597f5-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="597f5-122">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="597f5-122">Click **OK**.</span></span>
5. <span data-ttu-id="597f5-123">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="597f5-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="597f5-124">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="597f5-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="597f5-125">Klik in het **actievenster** op **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="597f5-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="597f5-126">Klik op **Orderwachtstanden**.</span><span class="sxs-lookup"><span data-stu-id="597f5-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="597f5-127">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="597f5-127">Click **New**.</span></span>
10. <span data-ttu-id="597f5-128">Selecteer in het veld **Orderwachtstand** de code die u hebt gemaakt in de vorige subtaak.</span><span class="sxs-lookup"><span data-stu-id="597f5-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="597f5-129">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="597f5-129">Click **Save**.</span></span>
12. <span data-ttu-id="597f5-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="597f5-130">Close the page.</span></span>
13. <span data-ttu-id="597f5-131">Ga naar **Verkoop en marketing > Verkooporders > Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="597f5-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="597f5-132">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="597f5-132">In the list, mark the selected row.</span></span> <span data-ttu-id="597f5-133">Bij orders die momenteel de status 'In wachtstand' hebben, zijn de velden 'Niet verwerken' en 'Wachtstand' gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="597f5-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="597f5-134">Klik in het actievenster op **Verzamelen en inpakken**.</span><span class="sxs-lookup"><span data-stu-id="597f5-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="597f5-135">Orderwachtstanden beheren</span><span class="sxs-lookup"><span data-stu-id="597f5-135">Manage order holds</span></span>
1. <span data-ttu-id="597f5-136">Ga naar **Verkoop en marketing > Verkooporders > Openstaande orders > Orderwachtstanden**.</span><span class="sxs-lookup"><span data-stu-id="597f5-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="597f5-137">De pagina **Orderwachtstanden** fungeert als een workbench, waarin u een overzicht kunt krijgen van alle actuele en verwerkte wachtstanden en waar u deze en de bijbehorende verkooporders kunt afhandelen.</span><span class="sxs-lookup"><span data-stu-id="597f5-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="597f5-138">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="597f5-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="597f5-139">Klik in het **actievenster** op **Uitchecken in wachtstand**.</span><span class="sxs-lookup"><span data-stu-id="597f5-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="597f5-140">Klik op **Uitchecken**.</span><span class="sxs-lookup"><span data-stu-id="597f5-140">Click **Check out**.</span></span>
5. <span data-ttu-id="597f5-141">Maak in de lijst de markering van de geselecteerde rij ongedaan.</span><span class="sxs-lookup"><span data-stu-id="597f5-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="597f5-142">In het veld **Uitgecheckt naar** wordt nu uw gebruikers-id weergegeven.</span><span class="sxs-lookup"><span data-stu-id="597f5-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="597f5-143">Klik op **Uitchecken wissen**.</span><span class="sxs-lookup"><span data-stu-id="597f5-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="597f5-144">Klik in het **actievenster** op **Wachtstand wissen**.</span><span class="sxs-lookup"><span data-stu-id="597f5-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="597f5-145">Als u de wachtstand wilt verwijderen zodat de order door kan gaan naar de volgende afhandelingsstap, moet u de wachtstand uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="597f5-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="597f5-146">Als de order geen aanpassing vereist, kunt u de actie Wachtstanden wissen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="597f5-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="597f5-147">U kunt echter de actie Wissen en aanpassen gebruiken, als bij het wissen van een wachtstand de order moet worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="597f5-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="597f5-148">De actie **Wissen en indienen** is alleen van toepassing wanneer u gebruik maakt van de Callcenterfunctionaliteit.</span><span class="sxs-lookup"><span data-stu-id="597f5-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="597f5-149">Klik op **Wachtstanden wissen**.</span><span class="sxs-lookup"><span data-stu-id="597f5-149">Click **Clear holds**.</span></span> <span data-ttu-id="597f5-150">De wachtstand is nu van de order gewist en verwijderd uit de lijst met actieve wachtstanden.</span><span class="sxs-lookup"><span data-stu-id="597f5-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="597f5-151">Als u alle wachtstanden wilt bekijken, of een subset daarvan op basis van een specifieke status, wijzigt u de waarde in het veld Weergeven.</span><span class="sxs-lookup"><span data-stu-id="597f5-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]