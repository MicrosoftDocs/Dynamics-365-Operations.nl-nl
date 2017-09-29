---
title: Hybride klantorders
description: Een hybride klantorder is een enkele order, die producten bevat die door de klant vanuit de winkel kunnen worden getransporteerd, alsmede de producten die later worden opgehaald of verzonden.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3b330b64c1427517866b17b62ac441a4a8bed2f0
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="hybrid-customer-orders"></a><span data-ttu-id="24b4c-103">Hybride klantorders</span><span class="sxs-lookup"><span data-stu-id="24b4c-103">Hybrid customer orders</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="24b4c-104">Een hybride klantorder is een enkele order, die producten bevat die door de klant vanuit de winkel kunnen worden getransporteerd, alsmede de producten die later worden opgehaald of verzonden.</span><span class="sxs-lookup"><span data-stu-id="24b4c-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="24b4c-105">In Microsoft Dynamics 365 for Retail kunt u aangeven dat u alle producten of geselecteerde producten voor een klantorder wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="24b4c-105">In Microsoft Dynamics 365 for Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="24b4c-106">De productregels die zijn gemarkeerd om te worden uitgevoerd, worden automatisch gefactureerd nadat de order is gemaakt. Dit geldt ook voor een order die moet worden opgehaald nadat de order is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="24b4c-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="24b4c-107">Het verschuldigde bedrag op hybride orders wordt bepaald door het aanbetalingspercentage op productregels voor verzamelen en verzenden met het volledige bedrag van de uitvoerregels.</span><span class="sxs-lookup"><span data-stu-id="24b4c-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="24b4c-108">Voor hybride orders wordt als volgt geschakeld tussen de klantordermodus en de cash-and-carry-modus:</span><span class="sxs-lookup"><span data-stu-id="24b4c-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

-   <span data-ttu-id="24b4c-109">Als alle producten in de winkelwagen zijn ingesteld op **Leveringsmethode uitvoeren**, wordt de order verwerkt als een contante transactie.</span><span class="sxs-lookup"><span data-stu-id="24b4c-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
-   <span data-ttu-id="24b4c-110">Als sommige of alle regels in de winkelwagen worden ingesteld op **Verzamelen** of **Levering verzenden**, wordt de order verwerkt als een klantordertransactie.</span><span class="sxs-lookup"><span data-stu-id="24b4c-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="24b4c-111">Als een winkelwagenregel is geselecteerd en **Selectie kiezen**, **Selectie verzenden** of **Selectie uitvoeren** is ingeschakeld, wordt alleen de specifieke winkelwagenregel ingesteld met die leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="24b4c-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="24b4c-112">In dat geval blijft de downstreamflow van de bewerking doorgaan zoals gebruikelijk.</span><span class="sxs-lookup"><span data-stu-id="24b4c-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="24b4c-113">Echter als **Selectie kiezen**, **Selectie verzenden** of **Selectie uitvoeren** is geselecteerd zonder dat een winkelwagenregel wordt geselecteerd, wordt een nieuwe pagina geopend waarin alle regels van de winkelwagenregels worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="24b4c-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="24b4c-114">Op dat scherm kunt u meerdere regels tegelijk selecteren voor het instellen van de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="24b4c-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="24b4c-115">Wanneer u die methode gebruikt voor het selecteren van regels, worden eventuele vorige leveringsmethoden, die zijn toegewezen aan de regel, overschreven.</span><span class="sxs-lookup"><span data-stu-id="24b4c-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

<a name="see-also"></a><span data-ttu-id="24b4c-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="24b4c-116">See also</span></span>
--------

[<span data-ttu-id="24b4c-117">Overzicht van klantbestellingen</span><span class="sxs-lookup"><span data-stu-id="24b4c-117">Customer orders overview</span></span>](customer-orders-overview.md)




