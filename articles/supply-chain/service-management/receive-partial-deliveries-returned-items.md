---
title: Deelleveringen van geretourneerde artikelen ontvangen
description: Gedeeltelijke leveringen worden gedefinieerd aan de hand van retourorderregels en niet aan de hand van retourorderleveringen.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f9f596d31f2438a353b02bf939786b284937db86
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="bd2d1-103">Deelleveringen van geretourneerde artikelen ontvangen</span><span class="sxs-lookup"><span data-stu-id="bd2d1-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bd2d1-104">Gedeeltelijke leveringen worden gedefinieerd aan de hand van retourorderregels en niet aan de hand van retourorderleveringen.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="bd2d1-105">Dit betekent dat wanneer u de volledige hoeveelheid ontvangt die is aangegeven op één retourorderregel, maar u niets van de andere regels in de retourorder ontvangt, de levering geen gedeeltelijke levering is.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="bd2d1-106">Als echter voor een retourorderregel bijvoorbeeld tien eenheden van een bepaald artikel moeten worden geretourneerd en u maar vier eenheden ontvangt, is dit een gedeeltelijke levering.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="bd2d1-107">Als een retourzending minder bevat dan de volledige hoeveelheid van een retourorderregel, kunt u wachten totdat u de rest van de te retourneren hoeveelheid ontvangt of u kunt de gedeeltelijke hoeveelheid registreren en boeken.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="bd2d1-108">Een gedeeltelijke hoeveelheid registreren en boeken</span><span class="sxs-lookup"><span data-stu-id="bd2d1-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="bd2d1-109">Nadat u een retourorder voor aankomst in het formulier **Aankomstoverzicht - Magazijn: %1, Dok: %2, Journaalnaam: %3** hebt geselecteerd, klikt u op **Begin aankomst** om het ontvangstjournaal te maken en klikt u vervolgens op **Journalen** \> **Aankomsten van ontvangsten tonen** om het formulier **Locatiejournaal** te openen.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="bd2d1-110">Selecteer de regel van het journaal waarmee u wilt werken en klik op **Regels** om het formulier **Journaalregels, locaties** te openen.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="bd2d1-111">Selecteer de regel van het artikelnummer waarvoor slechts een gedeeltelijke hoeveelheid is gearriveerd en klik op **Functies** \> **Splitsen** om het formulier **Splitsen** te openen.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="bd2d1-112">Voer in het veld **Gesplitste hoeveelheid** de hoeveelheid in voor het totaal aantal artikelen dat is ontvangen en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="bd2d1-113">Selecteer in het formulier **Journaalregels, locaties** de regel voor de hoeveelheid artikelen die is ontvangen en klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="bd2d1-114">U kunt de regel voor de extra hoeveelheid boeken nadat de artikelen zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="bd2d1-114">You can post the line for the additional quantity after the items have arrived.</span></span>





