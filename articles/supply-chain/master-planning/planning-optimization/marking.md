---
title: Voorraadmarkering met Planningsoptimalisatie
description: Dit onderwerp biedt informatie over de opties die beschikbaar zijn voor voorraadmarkering in gefiatteerde orders wanneer u Planningsoptimalisatie gebruikt.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3b139673ddf17e13d6687db485208e1aeb3908dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809489"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="c2ac0-103">Voorraadmarkering met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="c2ac0-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2ac0-104">Dit onderwerp biedt informatie over de opties die beschikbaar zijn voor voorraadmarkering in gefiatteerde orders wanneer u Planningsoptimalisatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="c2ac0-105">*Markering* wordt gebruikt om vraag en aanbod te koppelen.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="c2ac0-106">Het lijkt op *tracering van de behoefte* waarmee wordt aangegeven hoe de hoofdplanning de vraag verwacht te dekken.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="c2ac0-107">Vanuit het oogpunt van planning is het belangrijkste verschil dat markering permanenter is dan tracering van de behoefte.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="c2ac0-108">Markering is geïntroduceerd ter ondersteuning van speciale kostprijsberekeningsscenario's voor first in, first out (FIFO) en last in, first out (LIFO).</span><span class="sxs-lookup"><span data-stu-id="c2ac0-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="c2ac0-109">Deze wordt nu echter ook gebruikt voor sommige niet-kostprijsberekeningsscenario's.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="c2ac0-110">Markering tussen vraag en aanbod is optioneel en bijna permanent.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="c2ac0-111">Markering kan handmatig worden verwijderd door een gebruiker of worden verwijderd door een explosie van verkooporderregels uit te voeren, waarbij de optie **Markering verwijderen** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="c2ac0-112">Tracering van de behoefte wordt geregeld door de hoofdplanning tijdens dekking om de vraag te koppelen aan het vereiste aanbod.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="c2ac0-113">Tracering van de behoefte kan worden bijgewerkt voor elke planningsuitvoering om het aanbod te optimaliseren dat nodig is om de vraag te dekken.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="c2ac0-114">Wanneer hoofdplanning informatie over de tracering van de behoefte bijwerkt, wordt er rekening gehouden met bestaande markering.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="c2ac0-115">Tracering van de behoefte begint met het opnemen van relevante markering, reserveringen voor voorhanden voorraad en reserveringen voor in bestelling in de volgende volgorde:</span><span class="sxs-lookup"><span data-stu-id="c2ac0-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="c2ac0-116">Markering tussen vraag en aanbod</span><span class="sxs-lookup"><span data-stu-id="c2ac0-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="c2ac0-117">Reserveringen voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="c2ac0-117">On-hand reservations</span></span>
1. <span data-ttu-id="c2ac0-118">Reserveringen voor in bestelling</span><span class="sxs-lookup"><span data-stu-id="c2ac0-118">On-order reservations</span></span>

<span data-ttu-id="c2ac0-119">Wanneer u een geplande order fiatteert, bevat het dialoogvenster **Fiattering** een veld **Markering bijwerken** dat u gebruikt om opties voor markering in te stellen voor de orders die tijdens het fiatteren worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="c2ac0-120">Selecteer een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="c2ac0-120">Select one of the following values:</span></span>

- <span data-ttu-id="c2ac0-121">**Nee** – Er wordt geen voorraadmarkering toegepast.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="c2ac0-122">**Standaard** – De voorraadmarkering wordt bijgewerkt volgens de tracering van de behoefte.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="c2ac0-123">Een behoefteorder (vraag) wordt aan de hand van een vervullingsorder (aanbod) gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="c2ac0-124">Als een bepaalde hoeveelheid op de vervullingsorder blijft staan, wordt deze niet gemarkeerd en wordt de verwijzingsinformatie leeg gelaten.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="c2ac0-125">Als bijvoorbeeld een verkooporder voor 100 EA wordt vastgelegd voor een inkooporder voor 150 EA, wordt verwijzingsinformatie alleen aan de verkooporder toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="c2ac0-126">**Uitgebreid** – Zowel de behoefteorder (vraag) als de vervullingsorder (aanbod) worden gemarkeerd, ongeacht of er hoeveelheid op de vervullingsorder overblijft.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="c2ac0-127">Als bijvoorbeeld een verkooporder voor 100 EA wordt vastgelegd voor een inkooporder voor 150 EA, wordt verwijzingsinformatie aan de verkooporder en de inkooporder toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]