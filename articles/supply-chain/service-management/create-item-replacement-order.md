---
title: Een order maken voor het vervangen van een artikel
description: Artikelvervangingsorders worden meestal gemaakt wanneer een product is geretourneerd en geïnspecteerd.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b92c4400f2c852af49c78e9e94fdffa2e498b45c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202877"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="b94c8-103">Een order maken voor het vervangen van een artikel</span><span class="sxs-lookup"><span data-stu-id="b94c8-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b94c8-104">Artikelvervangingsorders worden meestal gemaakt wanneer een product is geretourneerd en geïnspecteerd.</span><span class="sxs-lookup"><span data-stu-id="b94c8-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="b94c8-105">Als een artikel moet worden vervangen voordat deze is geretourneerd of als het oorspronkelijke artikel niet wordt geretourneerd, kunt u direct een artikelvervangingsorder maken nadat u een retourorder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b94c8-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="b94c8-106">Een vervangingsorder maken nadat u een artikel ontvangt dat werd geretourneerd</span><span class="sxs-lookup"><span data-stu-id="b94c8-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="b94c8-107">Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.</span><span class="sxs-lookup"><span data-stu-id="b94c8-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="b94c8-108">Maak een nieuwe retourorder of selecteer een geretourneerde order in de lijst om het formulier **Retourorder - RMA-nummer: %1, %2** te openen.</span><span class="sxs-lookup"><span data-stu-id="b94c8-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="b94c8-109">Klik op **Retourregel** en selecteer vervolgens **Vervangingsartikel**.</span><span class="sxs-lookup"><span data-stu-id="b94c8-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="b94c8-110">Selecteer het artikel om het geretourneerde artikel te vervangen.</span><span class="sxs-lookup"><span data-stu-id="b94c8-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="b94c8-111">Voer de artikelspecificaties in en klik op **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="b94c8-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="b94c8-112">Klik op **Pakbon** om de pakbon te genereren voor de retourorder.</span><span class="sxs-lookup"><span data-stu-id="b94c8-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="b94c8-113">Een verkooporder wordt gegenereerd voor het vervangende artikel dat u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b94c8-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="b94c8-114">Nadat de verkooporder is gemaakt voor het vervangingsartikel, worden verkoopovereenkomsten automatisch doorzocht en als er een toepasselijke verkoopovereenkomst is, wordt deze toegepast op de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="b94c8-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="b94c8-115">Een vervangingsorder maken voordat u een artikel ontvangt dat wordt geretourneerd</span><span class="sxs-lookup"><span data-stu-id="b94c8-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="b94c8-116">Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.</span><span class="sxs-lookup"><span data-stu-id="b94c8-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="b94c8-117">Maak een nieuwe retourorder of selecteer een retourorder in de lijst om het formulier **Retourorder - RMA-nummer: %1, %2** te openen.</span><span class="sxs-lookup"><span data-stu-id="b94c8-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="b94c8-118">Klik op **Verkooporder zoeken** als u de verkooporder voor het geretourneerde artikel wilt identificeren.</span><span class="sxs-lookup"><span data-stu-id="b94c8-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="b94c8-119">Vul het formulier **Verkooporder zoeken** in en klik vervolgens op **OK** om het formulier te sluiten en terug te keren naar het formulier **Retourorder - RMA-nummer: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="b94c8-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="b94c8-120">De verkooporderregel voor het geretourneerde artikel wordt gekopieerd naar de retourorder.</span><span class="sxs-lookup"><span data-stu-id="b94c8-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="b94c8-121">Klik op **Vervangingsorder** om het formulier **Verkooporder** te openen.</span><span class="sxs-lookup"><span data-stu-id="b94c8-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="b94c8-122">Schakel het selectievakje **Retourorderregels kopiëren** in om de gegevens van de retourorder die u hebt geselecteerd in het formulier **Retourorder - RMA-nummer: %1, %2** te kopiëren naar deze verkooporder.</span><span class="sxs-lookup"><span data-stu-id="b94c8-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="b94c8-123">Voer zo nodig gegevens in of wijzig deze.</span><span class="sxs-lookup"><span data-stu-id="b94c8-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="b94c8-124">Als u de verkooporder in stap 3 hebt geïdentificeerd en als de verkooporderregel voor het geretourneerde artikel is gekoppeld aan een verkoopovereenkomst, wordt de id van de toepasselijke verkoopovereenkomst voor de artikelvervanging automatisch weergegeven in het veld **Verkoopovereenkomst-ID**.</span><span class="sxs-lookup"><span data-stu-id="b94c8-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="b94c8-125">Klik op **OK** om het formulier **Verkooporder maken** te sluiten en het formulier **Verkooporder** te openen waar u kunt doorgaan met het invoeren van gegevens voor de nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="b94c8-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="b94c8-126">Toepasselijke retourorderregels worden gekopieerd naar de nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="b94c8-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="b94c8-127">Als de id van de verkoopovereenkomst automatisch wordt weergegeven in het veld **Verkoopovereenkomst-ID**, is de verkoopovereenkomst gekoppeld aan de koptekst van de verkooporder voor het vervangingsorder voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="b94c8-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="b94c8-128">Als er een verbintenis van toepassing is in de verkoopovereenkomst die nog niet is voldaan en de verkooporder wordt gemaakt voordat de verkoopovereenkomst verloopt, wordt een koppeling gemaakt tussen de verkoopovereenkomstregel en de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="b94c8-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="b94c8-129">Daarom wordt informatie van de verkoopovereenkomst, zoals artikelprijs, gekopieerd naar de nieuwe verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="b94c8-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


