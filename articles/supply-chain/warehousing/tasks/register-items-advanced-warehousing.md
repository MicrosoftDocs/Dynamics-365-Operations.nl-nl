--- 
title: Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal
description: Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 751e73be385606bc706b2e14ea83c1b56c96402c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="fba26-103">Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal</span><span class="sxs-lookup"><span data-stu-id="fba26-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fba26-104">Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fba26-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="fba26-105">Dit wordt gewoonlijk uitgevoerd door een ontvangstadministrateur.</span><span class="sxs-lookup"><span data-stu-id="fba26-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="fba26-106">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="fba26-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="fba26-107">U moet een bevestigde inkooporder met een openstaande inkooporderregel hebben voordat u deze handleiding start.</span><span class="sxs-lookup"><span data-stu-id="fba26-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="fba26-108">Het artikel op de regel moet in voorraad zijn opgeslagen, er mogen geen productvarianten worden gebruikt en het mag geen traceringsdimensies hebben.</span><span class="sxs-lookup"><span data-stu-id="fba26-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="fba26-109">En het artikel moet zijn gekoppeld aan een opslagdimensiegroep die gebruikmaakt van magazijnbeheerprocessen.</span><span class="sxs-lookup"><span data-stu-id="fba26-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="fba26-110">Het magazijn dat wordt gebruikt moet zijn ingeschakeld voor magazijnbeheerprocessen en de locatie die u voor het ontvangen gebruikt moet worden gecontroleerd op nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="fba26-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="fba26-111">Als u USMF gebruikt, kunt u bedrijfsrekening 1001, Magazijn 51 en artikel M9200 gebruiken om de IO te maken.</span><span class="sxs-lookup"><span data-stu-id="fba26-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="fba26-112">Noteer het nummer van de inkooporder die u maakt en noteer ook het artikelnummer en de site die u voor de inkooporderregel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fba26-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="fba26-113">Een koptekst voor artikelontvangstjournaal maken</span><span class="sxs-lookup"><span data-stu-id="fba26-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="fba26-114">Ga naar Artikelontvangst.</span><span class="sxs-lookup"><span data-stu-id="fba26-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="fba26-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="fba26-115">Click New.</span></span>
3. <span data-ttu-id="fba26-116">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="fba26-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fba26-117">Als u USMF gebruikt, kunt u WHS typen.</span><span class="sxs-lookup"><span data-stu-id="fba26-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="fba26-118">Als u andere gegevens gebruikt, moet het journaal waarvan u de naam kiest de volgende eigenschappen hebben: Orderverzamellocatie controleren moet zijn ingesteld op Nee en Quarantainebeheer moet zijn ingesteld op Nee.</span><span class="sxs-lookup"><span data-stu-id="fba26-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="fba26-119">Typ een waarde in het veld Nummer.</span><span class="sxs-lookup"><span data-stu-id="fba26-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="fba26-120">Typ een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="fba26-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="fba26-121">Selecteer de site die u voor de inkooporderregel hebt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fba26-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="fba26-122">Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal.</span><span class="sxs-lookup"><span data-stu-id="fba26-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="fba26-123">Als u magazijn 51 gebruikte in USMF, kiest u site 5.</span><span class="sxs-lookup"><span data-stu-id="fba26-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="fba26-124">Typ een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="fba26-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="fba26-125">Selecteer een geldig magazijn voor de site die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fba26-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="fba26-126">Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal.</span><span class="sxs-lookup"><span data-stu-id="fba26-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="fba26-127">Als u de voorbeeldwaarden in USMF gebruikt, selecteert u 51.</span><span class="sxs-lookup"><span data-stu-id="fba26-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="fba26-128">Typ een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="fba26-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="fba26-129">Selecteer een geldige locatie in het magazijn dat u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fba26-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="fba26-130">De locatie moet aan een locatieprofiel zijn gekoppeld, waar nummerplaten worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="fba26-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="fba26-131">Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal.</span><span class="sxs-lookup"><span data-stu-id="fba26-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="fba26-132">Als u de voorbeeldwaarden in USMF gebruikt, selecteert u Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="fba26-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="fba26-133">Klik met de rechtermuisknop op de vervolgkeuzepijl in het veld Nummerplaat en selecteer vervolgens Details weergeven.</span><span class="sxs-lookup"><span data-stu-id="fba26-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="fba26-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="fba26-134">Click New.</span></span>
10. <span data-ttu-id="fba26-135">Typ een waarde in het veld Nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="fba26-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="fba26-136">Noteer de waarde.</span><span class="sxs-lookup"><span data-stu-id="fba26-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="fba26-137">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fba26-137">Click Save.</span></span>
12. <span data-ttu-id="fba26-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fba26-138">Close the page.</span></span>
13. <span data-ttu-id="fba26-139">Typ een waarde in het veld Nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="fba26-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="fba26-140">Voer de waarde van de nummerplaat in die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fba26-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="fba26-141">Dit fungeert als een standaardwaarde, die standaard wordt ingesteld op alle regels in het journaal.</span><span class="sxs-lookup"><span data-stu-id="fba26-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="fba26-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fba26-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="fba26-143">Een regel toevoegen</span><span class="sxs-lookup"><span data-stu-id="fba26-143">Add a line</span></span>
1. <span data-ttu-id="fba26-144">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fba26-144">Click Add line.</span></span>
2. <span data-ttu-id="fba26-145">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="fba26-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fba26-146">Voer het artikelnummer in dat u op de inkooporderregel hebt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fba26-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="fba26-147">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="fba26-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="fba26-148">Voer de hoeveelheid in die u wilt registreren.</span><span class="sxs-lookup"><span data-stu-id="fba26-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="fba26-149">Het veld Datum bepaalt de datum waarop de voorhanden hoeveelheid van het artikel in de voorraad wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="fba26-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="fba26-150">De partij-id wordt door het systeem ingevuld als deze uniek kan worden geïdentificeerd uit de opgegeven informatie.</span><span class="sxs-lookup"><span data-stu-id="fba26-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="fba26-151">Anders moet u deze handmatig toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fba26-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="fba26-152">Dit is een verplichte veld, dat deze registratie aan een specifieke brondocumentregel koppelt.</span><span class="sxs-lookup"><span data-stu-id="fba26-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="fba26-153">De registratie voltooien</span><span class="sxs-lookup"><span data-stu-id="fba26-153">Complete the registration</span></span>
1. <span data-ttu-id="fba26-154">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="fba26-154">Click Validate.</span></span>
    * <span data-ttu-id="fba26-155">Dit controleert of het journaal gereed is om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="fba26-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="fba26-156">Als validatie mislukt, kunt u de fouten bevestigen voordat u het journaal kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="fba26-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="fba26-157">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fba26-157">Click OK.</span></span>
    * <span data-ttu-id="fba26-158">Nadat u op OK hebt geklikt, controleert u het bericht.</span><span class="sxs-lookup"><span data-stu-id="fba26-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="fba26-159">Er moet een bericht zijn dat meldt dat het journaal OK is.</span><span class="sxs-lookup"><span data-stu-id="fba26-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="fba26-160">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="fba26-160">Click Post.</span></span>
4. <span data-ttu-id="fba26-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fba26-161">Click OK.</span></span>
    * <span data-ttu-id="fba26-162">Nadat u op OK hebt geklikt, controleert u de berichtenbalk.</span><span class="sxs-lookup"><span data-stu-id="fba26-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="fba26-163">Er moet een bericht zijn dat meldt dat de bewerking voltooid is.</span><span class="sxs-lookup"><span data-stu-id="fba26-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="fba26-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fba26-164">Close the page.</span></span>


