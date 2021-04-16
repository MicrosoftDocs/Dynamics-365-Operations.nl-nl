---
title: Module ophaalinformatie
description: In dit onderwerp wordt beschreven wat de ophaalinformatiemodule is en hoe u deze toevoegt aan uitcheckpagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 063701d5cd5714febeb32907346d9f6e5c2a2ca1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804400"
---
# <a name="pickup-information-module"></a><span data-ttu-id="ff8fa-103">Module met afhaalinformatie</span><span class="sxs-lookup"><span data-stu-id="ff8fa-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff8fa-104">In dit onderwerp wordt beschreven wat de ophaalinformatiemodule is en hoe u deze toevoegt aan uitcheckpagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ff8fa-105">De module ophaalinformatie kan worden gebruikt in een uitcheckmodule om informatie over het ophalen van orders weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="ff8fa-106">Klanten kunnen de beschikbare ophaaldatums en tijdvakken weergeven en vervolgens een geschikte tijd selecteren om de order op te halen.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="ff8fa-107">Een klant kan bijvoorbeeld kiezen om een order op te halen op 21 maart om 15.00 uur in de winkel in San Francisco.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="ff8fa-108">Tijdvakken voor ophalen in de desbetreffende winkels moeten worden geconfigureerd in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="ff8fa-109">Zie [Tijdvakken voor ophalen door klanten maken en bijwerken](dev-itpro/pickup-timeslots.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="ff8fa-110">Als er een ophaalinformatiemodule is gemaakt op een uitcheckpagina, maar er geen tijdvakken zijn gedefinieerd voor de winkel die is geselecteerd voor ophalen, wordt in de module informatie weergegeven, maar kan de gebruiker geen tijdvakken selecteren.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="ff8fa-111">Tijdvakken zijn optioneel en niet nodig om een order te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="ff8fa-112">Als er meerdere artikelen zijn geselecteerd om te worden opgehaald in meerdere winkels, kan de gebruiker in de ophaalinformatiemodule een tijdvak selecteren voor elke winkel, mits er tijdvakken beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="ff8fa-113">Ondersteuning voor tijdvakken en de ophaalinformatiemodule is beschikbaar in Dynamics 365 Commerce versie 10.0.15 en hoger.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="ff8fa-114">In de volgende afbeelding ziet u een voorbeeld van een tijdvakselectie via de ophaalinformatiemodule op een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Voorbeeld van een ophaalinformatiemodule voor verzendadressen op een betalingspagina](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="ff8fa-116">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="ff8fa-116">Module properties</span></span>

- <span data-ttu-id="ff8fa-117">**Koptekst** - Voer een koptekst in voor de module.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="ff8fa-118">Informatie over tijdvakken weergeven nadat een order is geplaatst</span><span class="sxs-lookup"><span data-stu-id="ff8fa-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="ff8fa-119">Nadat een order is geplaatst, kunt u informatie over het geselecteerde tijdvak weergeven in de [module orderbevestiging](order-confirmation-module.md) en de [module orderdetails](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="ff8fa-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="ff8fa-120">Beide modules hebben de eigenschap **Tijdvakinformatie weergeven**.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="ff8fa-121">Voordat ze de geselecteerde tijdvakken kunnen weergeven tijdens het orderproces, moet deze eigenschap worden ingesteld op **Waar**.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="ff8fa-122">Een ophaalinformatiemodule toevoegen op een betalingspagina</span><span class="sxs-lookup"><span data-stu-id="ff8fa-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="ff8fa-123">Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een ophaalinformatiemodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="ff8fa-124">In de volgende afbeelding ziet u een voorbeeld van een e-commerce uitcheckpagina met tijdvakken voor het ophalen van artikelen.</span><span class="sxs-lookup"><span data-stu-id="ff8fa-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Voorbeeld van een e-commerce uitcheckpagina met tijdvakken voor het ophalen van artikelen](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="ff8fa-126">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ff8fa-126">Additional resources</span></span>

[<span data-ttu-id="ff8fa-127">Tijdvakken voor het ophalen door klanten maken en bijwerken</span><span class="sxs-lookup"><span data-stu-id="ff8fa-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="ff8fa-128">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="ff8fa-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ff8fa-129">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="ff8fa-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ff8fa-130">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="ff8fa-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]