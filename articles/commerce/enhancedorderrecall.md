---
title: Bewerking Order intrekken in POS
description: In dit onderwerp worden de functies uitgelegd die beschikbaar zijn voor de verbeterde pagina´s voor orderintrekking in POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42b11ff16757d633b868dfdf248341193a44378f
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665293"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="4c88a-103">Bewerking Order intrekken in POS</span><span class="sxs-lookup"><span data-stu-id="4c88a-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c88a-104">Met de bewerking voor het **intrekken van orders** in het Commerce Point of Sale (POS) beschikt u over gewijzigde functies om te zoeken en te filteren en over orderspecifieke informatie.</span><span class="sxs-lookup"><span data-stu-id="4c88a-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="4c88a-105">Deze functie is beschikbaar in Commerce-versies 10.0.15 en hoger.</span><span class="sxs-lookup"><span data-stu-id="4c88a-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="4c88a-106">Als u deze functie wilt inschakelen, schakelt u de functie **Verbeterde bewerking voor orderintrekking in POS** in de werkruimte **Functiebeheer** in Commerce Headquarters in.</span><span class="sxs-lookup"><span data-stu-id="4c88a-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="4c88a-107">Nadat u de functie hebt ingeschakeld, kunt u overwegen om uw [schermindelingen](pos-screen-layouts.md) in POS bij te werken zodat u kunt profiteren van een aantal van de gewijzigde mogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="4c88a-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="4c88a-108">Met de configuratie van de bewerkingsknop **Order intrekken** kunnen organisaties de bewerking implementeren met een vooraf gedefinieerde weergave.</span><span class="sxs-lookup"><span data-stu-id="4c88a-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Configuratie knoppenraster](media/recallorderbuttongrid.png)

<span data-ttu-id="4c88a-110">De weergaveopties zijn als volgt.</span><span class="sxs-lookup"><span data-stu-id="4c88a-110">The display options are as follows.</span></span>
- <span data-ttu-id="4c88a-111">**Geen**: met deze optie wordt de bewerking zonder specifieke weergave geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="4c88a-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="4c88a-112">Wanneer gebruikers de bewerking met deze configuratie openen, wordt hen gevraagd orders te zoeken of om een keuze te maken uit een vooraf gedefinieerd orderfilter.</span><span class="sxs-lookup"><span data-stu-id="4c88a-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="4c88a-113">**Af te handelen orders**: wanneer een gebruiker de bewerking start, wordt automatisch een query uitgevoerd om een lijst met orders te zoeken en weer te geven die door de winkel moeten worden afgehandeld.</span><span class="sxs-lookup"><span data-stu-id="4c88a-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="4c88a-114">Deze orders worden geconfigureerd om te worden opgehaald in de winkel of om vanuit de winkel te worden verzonden en de regels van deze orders zijn nog niet verzameld of verpakt.</span><span class="sxs-lookup"><span data-stu-id="4c88a-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="4c88a-115">**Op te halen orders**: wanneer een gebruiker de bewerking start, wordt automatisch een query uitgevoerd om een lijst met orders te zoeken en weer te geven die zijn geconfigureerd om te worden opgehaald in de huidige winkel van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="4c88a-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="4c88a-116">**Te verzenden orders**: wanneer een gebruiker de bewerking start, wordt automatisch een query uitgevoerd om een lijst met orders te zoeken en weer te geven die zijn geconfigureerd voor verzending vanuit de huidige winkel van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="4c88a-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="4c88a-117">Als de weergave is ingesteld op **Geen** , kan een gebruiker op een van de volgende manieren orders zoeken en ophalen bij het starten van de bewerking **Order intrekken**.</span><span class="sxs-lookup"><span data-stu-id="4c88a-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="4c88a-118">Streepjescodes van orders scannen.</span><span class="sxs-lookup"><span data-stu-id="4c88a-118">Scan order barcodes.</span></span> <span data-ttu-id="4c88a-119">Hiermee wordt gezocht naar overeenkomsten in de velden voor ordernummer, kanaalverwijzing en ontvangst-ID.</span><span class="sxs-lookup"><span data-stu-id="4c88a-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="4c88a-120">Selecteer **Orders zoeken** of het pictogram **Zoeken en filteren** op de AppBar om het filtermechanisme te gebruiken om orders te vinden die voldoen aan de filtercriteria.</span><span class="sxs-lookup"><span data-stu-id="4c88a-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="4c88a-121">Maak een keuze uit een vooraf gedefinieerd filter in het vervolgkeuzemenu **Orders weergeven** (af te handelen orders, op te halen orders of te verzenden orders).</span><span class="sxs-lookup"><span data-stu-id="4c88a-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="4c88a-123">Nadat de zoekcriteria zijn toegepast, wordt in de toepassing een lijst met overeenkomende verkooporders weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4c88a-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="4c88a-125">Een gebruiker kan een order in de lijst selecteren om aanvullende details weer te geven.</span><span class="sxs-lookup"><span data-stu-id="4c88a-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="4c88a-126">In het informatievenster aan de rechterkant van het scherm worden specifieke gegevens over de geselecteerde order weergegeven, waaronder orderregeldetails, leveringsdetails en afhandelingsinformatie.</span><span class="sxs-lookup"><span data-stu-id="4c88a-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="4c88a-127">Via de Appbar kan een gebruiker een bewerking selecteren.</span><span class="sxs-lookup"><span data-stu-id="4c88a-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="4c88a-128">Afhankelijk van de status van de order kunnen bepaalde bewerkingen niet worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="4c88a-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="4c88a-129">**Retourneren**: hiermee wordt een retour uitgevoerd voor een of meer facturen die aan de geselecteerde klantorder zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="4c88a-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="4c88a-130">**Annuleren**: hiermee wordt een volledige annulering van de geselecteerde verkooporder uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="4c88a-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="4c88a-131">**Afhandelen**: hiermee wordt de gebruiker overgebracht naar de pagina Order afhandelen die vooraf wordt gefilterd voor de geselecteerde order.</span><span class="sxs-lookup"><span data-stu-id="4c88a-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="4c88a-132">Alleen orderregels die open zijn voor afhandeling door de winkel van de gebruiker voor de geselecteerde order worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4c88a-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="4c88a-133">**Bewerken**: hiermee kunnen gebruikers wijzigingen aanbrengen in de geselecteerde klantorder.</span><span class="sxs-lookup"><span data-stu-id="4c88a-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="4c88a-134">**Ophalen**: hiermee wordt de ophaalstroom gestart zodat de gebruiker de producten kan kiezen die moeten worden opgehaald, en wordt de verkooptransactie voor ophalen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4c88a-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
