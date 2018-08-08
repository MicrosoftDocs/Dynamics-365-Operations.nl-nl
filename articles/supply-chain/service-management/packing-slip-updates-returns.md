---
title: Pakbonnen bijwerken voor retouren
description: Voordat geretourneerde artikelen weer in de voorraad kunnen worden opgenomen, moet de pakbon voor de order waartoe deze artikelen behoren, worden bijgewerkt.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
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
ms.openlocfilehash: 4aba61e6acf5fb959917da9ddea94c21fe1460d1
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="4673e-103">Pakbonnen bijwerken voor retouren</span><span class="sxs-lookup"><span data-stu-id="4673e-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4673e-104">Voordat geretourneerde artikelen weer in de voorraad kunnen worden opgenomen, moet de pakbon voor de order waartoe deze artikelen behoren, worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="4673e-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="4673e-105">Net zoals u met het factuurbijwerkproces de financiële transactie bijwerkt, werkt u met het pakbonbijwerkproces fysiek de voorraadrecord bij. Dit betekent dat u met het bijwerken van de pakbon, wijzigingen in de voorraad doorvoert.</span><span class="sxs-lookup"><span data-stu-id="4673e-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="4673e-106">In het geval van geretourneerde artikelen worden de stappen die zijn toegewezen aan de beschikkingsactie, geïmplementeerd tijdens het bijwerken van de pakbon.</span><span class="sxs-lookup"><span data-stu-id="4673e-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="4673e-107">Het bijwerken van de pakbon kan worden verwerkt in het artikelontvangstjournaal of de retourorder.</span><span class="sxs-lookup"><span data-stu-id="4673e-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="4673e-108">Als onderdeel van het boekingsproces voor pakbonnen kan het referentienummer van de pakbon uit de verzenddocumenten van de klant worden gekoppeld aan de orderregels.</span><span class="sxs-lookup"><span data-stu-id="4673e-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="4673e-109">Deze koppeling is optioneel en dient alleen ter informatie.</span><span class="sxs-lookup"><span data-stu-id="4673e-109">This association is optional and for reference only.</span></span> <span data-ttu-id="4673e-110">Er worden geen transactiewijzigingen aangebracht.</span><span class="sxs-lookup"><span data-stu-id="4673e-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="4673e-111">Als niet alle verwachte geretourneerde artikelen zijn ontvangen, moet u alleen die hoeveelheid die is ontvangen, opnemen in de wijziging van de pakbon.</span><span class="sxs-lookup"><span data-stu-id="4673e-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="4673e-112">Laat de resterende artikelen op de order staat tot de rest van de retourzending is gearriveerd.</span><span class="sxs-lookup"><span data-stu-id="4673e-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="4673e-113">Als een artikel van het quarantainemagazijn wordt teruggestuurd naar de afdeling Expeditie en ontvangst, bijvoorbeeld wanneer de quarantaine-inspecteur niet weet waar het artikel in de voorraad moet worden opgeslagen, moet de bijbehorende pakbon worden bijgewerkt om de beschikkingscode juist te registreren en op te volgen, die is opgegeven als gevolg van de quarantaine.</span><span class="sxs-lookup"><span data-stu-id="4673e-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="4673e-114">Wanneer u een pakbon bijwerkt voor een geretourneerd artikel dat van een verkoopovereenkomst afkomstig is, wordt de verkoopovereenkomsttoezegging voor dat artikel automatisch bijgewerkt met de wijziging in de hoeveelheid of het bedrag.</span><span class="sxs-lookup"><span data-stu-id="4673e-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="4673e-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4673e-115">See also</span></span>

[<span data-ttu-id="4673e-116">Facturen bijwerken voor retouren</span><span class="sxs-lookup"><span data-stu-id="4673e-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  



