---
title: Informatie over ouderdom van klanten instellen en genereren
description: Deze taakbegeleiding helpt u bij de instelling van een ouderdomsperiodedefinitie, ouderdom van klantsaldi te berekenen en saldi weer te geven in de lijst Ouderdomssaldi en de pagina Aanmaningen.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fd8738cfd3466464c9fec1760e9a369ff3a4a67
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568230"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="4ef08-103">Informatie over ouderdom van klanten instellen en genereren</span><span class="sxs-lookup"><span data-stu-id="4ef08-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ef08-104">Deze taakbegeleiding helpt u bij de instelling van een ouderdomsperiodedefinitie, ouderdom van klantsaldi te berekenen en saldi weer te geven in de lijst Ouderdomssaldi en de pagina Aanmaningen.</span><span class="sxs-lookup"><span data-stu-id="4ef08-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="4ef08-105">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4ef08-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="4ef08-106">Een ouderdomsperiodedefinitie maken</span><span class="sxs-lookup"><span data-stu-id="4ef08-106">Create an aging period definition</span></span>
1. <span data-ttu-id="4ef08-107">Ga naar Crediteringen en aanmaningen > Instellingen > Ouderdomsperiodedefinities.</span><span class="sxs-lookup"><span data-stu-id="4ef08-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="4ef08-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4ef08-108">Click New.</span></span>
3. <span data-ttu-id="4ef08-109">Typ in het veld Ouderdomsperiodedefinitie een waarde.</span><span class="sxs-lookup"><span data-stu-id="4ef08-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="4ef08-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="4ef08-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4ef08-111">Klik hieronder op Toevoegen om een nieuwe ouderdomsperiode in te voegen.</span><span class="sxs-lookup"><span data-stu-id="4ef08-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="4ef08-112">Voer in het veld Periode de omschrijving in om op ouderdomsrapporten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="4ef08-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="4ef08-113">Voer een nummer in het veld Eenheid in.</span><span class="sxs-lookup"><span data-stu-id="4ef08-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="4ef08-114">Selecteer een optie in het veld Interval.</span><span class="sxs-lookup"><span data-stu-id="4ef08-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="4ef08-115">De grootboekperiode stemt de periode af op uw grootboekkalender.</span><span class="sxs-lookup"><span data-stu-id="4ef08-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="4ef08-116">Dag, week, maand, kwartaal en jaren definiëren de grootte van het interval op datumtype.</span><span class="sxs-lookup"><span data-stu-id="4ef08-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="4ef08-117">Onbeperkt selecteert alle transacties voor of na de vorige periode, afhankelijk van of het de eerste of laatste periode is.</span><span class="sxs-lookup"><span data-stu-id="4ef08-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="4ef08-118">Selecteer een optie in het veld Ouderdomsindicator.</span><span class="sxs-lookup"><span data-stu-id="4ef08-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="4ef08-119">Selecteer de periode boven in het raster.</span><span class="sxs-lookup"><span data-stu-id="4ef08-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="4ef08-120">Werk de omschrijving bij om de oudste periode in de ouderdomsperiodedefinitie te beschrijven</span><span class="sxs-lookup"><span data-stu-id="4ef08-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="4ef08-121">Voer in het veld Periode de nieuwe omschrijving van de ouderdomsperiode in.</span><span class="sxs-lookup"><span data-stu-id="4ef08-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="4ef08-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4ef08-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="4ef08-123">Ouderdom saldi berekenen</span><span class="sxs-lookup"><span data-stu-id="4ef08-123">Age the balances</span></span>
1. <span data-ttu-id="4ef08-124">Ga naar Crediteringen en aanmaningen > Periodieke taken > Ouderdom van klantsaldi berekenen.</span><span class="sxs-lookup"><span data-stu-id="4ef08-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="4ef08-125">Selecteer in het veld Ouderdomsperiodedefinitie de ouderdomsperiodedefinitie die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4ef08-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="4ef08-126">U kunt één actieve momentopname voor elke ouderdomsperiodedefinitie hebben.</span><span class="sxs-lookup"><span data-stu-id="4ef08-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="4ef08-127">Alle klanten worden standaard verwerkt.</span><span class="sxs-lookup"><span data-stu-id="4ef08-127">All customers are processed by default.</span></span> <span data-ttu-id="4ef08-128">U kunt deze selectie gebruiken om een enkele incassoverzameling klanten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="4ef08-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="4ef08-129">Selecteer de datum van de transactie die u voor de ouderdomsrangschikking wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="4ef08-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="4ef08-130">Selecteer een "vanaf" datum voor ouderdomsrangschikking.</span><span class="sxs-lookup"><span data-stu-id="4ef08-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="4ef08-131">De standaard is vandaag maar als u dit veld in Geselecteerde datum wijzigt, kunt u de gewenste datum kiezen.</span><span class="sxs-lookup"><span data-stu-id="4ef08-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="4ef08-132">Gebruik voor batchverwerking de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="4ef08-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="4ef08-133">Vouw het bereik Bedrijf uit.</span><span class="sxs-lookup"><span data-stu-id="4ef08-133">Expand the Company range.</span></span> <span data-ttu-id="4ef08-134">U kunt de bedrijven selecteren die in de momentopname worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="4ef08-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="4ef08-135">Het huidige bedrijf wordt standaard geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="4ef08-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="4ef08-136">Klik op OK om de momentopname te verwerken.</span><span class="sxs-lookup"><span data-stu-id="4ef08-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="4ef08-137">Het duurt even voor de schuifregelaar verdwijnt. Controleer het berichtencentrum op een bericht.</span><span class="sxs-lookup"><span data-stu-id="4ef08-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="4ef08-138">De saldi op de lijst Vervallen saldi en op de pagina Aanmaning weergeven</span><span class="sxs-lookup"><span data-stu-id="4ef08-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="4ef08-139">Ga naar Crediteringen en aanmaningen > Incasso's > Vervallen saldi.</span><span class="sxs-lookup"><span data-stu-id="4ef08-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="4ef08-140">De lijstpagina geeft de saldi voor de klant weer.</span><span class="sxs-lookup"><span data-stu-id="4ef08-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="4ef08-141">Het ouderdomspictogram geeft de ouderdomsperiode voor de oudste transactie weer.</span><span class="sxs-lookup"><span data-stu-id="4ef08-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="4ef08-142">Selecteer een klant met een saldo.</span><span class="sxs-lookup"><span data-stu-id="4ef08-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="4ef08-143">Vouw het feitenvakgebied Ouderdomsrangschikking uit als u de ouderdomssaldi wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="4ef08-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="4ef08-144">De ouderdomsperiodedefinitie voor het feitenvak is afkomstig van de standaardouderdomsperiodedefinitie die wordt opgegeven in de parameters.</span><span class="sxs-lookup"><span data-stu-id="4ef08-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="4ef08-145">U kunt deze wijzigen met het menu Incasso.</span><span class="sxs-lookup"><span data-stu-id="4ef08-145">You can change it using the Collect menu.</span></span>  

