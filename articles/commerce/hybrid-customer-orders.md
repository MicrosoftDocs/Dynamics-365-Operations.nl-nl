---
title: Hybride klantorders
description: Een hybride klantorder is een enkele order, die producten bevat die door de klant vanuit de winkel kunnen worden getransporteerd, alsmede de producten die later worden opgehaald of verzonden.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c2105aa99e0489d7643d076e84123eec628679e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022200"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="3e97d-103">Hybride klantorders</span><span class="sxs-lookup"><span data-stu-id="3e97d-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e97d-104">Een hybride klantorder is een enkele order, die producten bevat die door de klant vanuit de winkel kunnen worden getransporteerd, alsmede de producten die later worden opgehaald of verzonden.</span><span class="sxs-lookup"><span data-stu-id="3e97d-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="3e97d-105">In Commerce kunt u aangeven dat u alle producten of geselecteerde producten voor een klantorder wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3e97d-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="3e97d-106">De productregels die zijn gemarkeerd om te worden uitgevoerd, worden automatisch gefactureerd nadat de order is gemaakt. Dit geldt ook voor een order die moet worden opgehaald nadat de order is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3e97d-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="3e97d-107">Het verschuldigde bedrag op hybride orders wordt bepaald door het aanbetalingspercentage op productregels voor verzamelen en verzenden met het volledige bedrag van de uitvoerregels.</span><span class="sxs-lookup"><span data-stu-id="3e97d-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="3e97d-108">Voor hybride orders wordt als volgt geschakeld tussen de klantordermodus en de cash-and-carry-modus:</span><span class="sxs-lookup"><span data-stu-id="3e97d-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="3e97d-109">Als alle producten in de winkelwagen zijn ingesteld op **Leveringsmethode uitvoeren**, wordt de order verwerkt als een contante transactie.</span><span class="sxs-lookup"><span data-stu-id="3e97d-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="3e97d-110">Als sommige of alle regels in de winkelwagen worden ingesteld op **Verzamelen** of **Levering verzenden**, wordt de order verwerkt als een klantordertransactie.</span><span class="sxs-lookup"><span data-stu-id="3e97d-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="3e97d-111">Als een winkelwagenregel is geselecteerd en **Selectie kiezen**, **Selectie verzenden** of **Selectie uitvoeren** is ingeschakeld, wordt alleen de specifieke winkelwagenregel ingesteld met die leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="3e97d-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="3e97d-112">In dat geval blijft de downstreamflow van de bewerking doorgaan zoals gebruikelijk.</span><span class="sxs-lookup"><span data-stu-id="3e97d-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="3e97d-113">Echter als **Selectie kiezen**, **Selectie verzenden** of **Selectie uitvoeren** is geselecteerd zonder dat een winkelwagenregel wordt geselecteerd, wordt een nieuwe pagina geopend waarin alle regels van de winkelwagenregels worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3e97d-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="3e97d-114">Op dat scherm kunt u meerdere regels tegelijk selecteren voor het instellen van de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="3e97d-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="3e97d-115">Wanneer u die methode gebruikt voor het selecteren van regels, worden eventuele vorige leveringsmethoden, die zijn toegewezen aan de regel, overschreven.</span><span class="sxs-lookup"><span data-stu-id="3e97d-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e97d-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3e97d-116">Additional resources</span></span>

[<span data-ttu-id="3e97d-117">Klantorders in Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="3e97d-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)