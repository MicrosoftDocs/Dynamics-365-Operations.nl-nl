---
title: Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal
description: In dit onderwerp wordt een scenario gepresenteerd dat laat zien hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830829"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="a459e-103">Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal</span><span class="sxs-lookup"><span data-stu-id="a459e-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a459e-104">In dit onderwerp wordt een scenario gepresenteerd dat laat zien hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a459e-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="a459e-105">Dit wordt gewoonlijk uitgevoerd door een ontvangstadministrateur.</span><span class="sxs-lookup"><span data-stu-id="a459e-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="a459e-106">Voorbeeldgegevens inschakelen</span><span class="sxs-lookup"><span data-stu-id="a459e-106">Enable sample data</span></span>

<span data-ttu-id="a459e-107">Als u dit scenario wilt doorwerken met behulp van de voorbeeldrecords en -waarden die in dit onderwerp zijn opgegeven, moet u een systeem gebruiken waarbij de standaarddemogegevens zijn geïnstalleerd en moet u de rechtspersoon *USMF* selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="a459e-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="a459e-108">U kunt in plaats daarvan dit scenario doorwerken door waarden uit uw eigen gegevens te vervangen op voorwaarde dat u over de volgende gegevens beschikt:</span><span class="sxs-lookup"><span data-stu-id="a459e-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="a459e-109">U moet een bevestigde inkooporder hebben met een openstaande inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="a459e-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="a459e-110">Het artikel op de regel moet worden opgeslagen in voorraad.</span><span class="sxs-lookup"><span data-stu-id="a459e-110">The item on the line must be stocked.</span></span> <span data-ttu-id="a459e-111">Het mag geen productvarianten gebruiken en mag geen traceringsdimensies hebben.</span><span class="sxs-lookup"><span data-stu-id="a459e-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="a459e-112">Het artikel moet zijn gekoppeld aan een opslagdimensiegroep waarvoor het magazijnbeheerproces is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="a459e-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="a459e-113">Het magazijn dat wordt gebruikt, moet zijn ingeschakeld voor magazijnbeheerprocessen en de locatie die u voor het ontvangen gebruikt, moet worden gecontroleerd op nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="a459e-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="a459e-114">Een koptekst voor het artikelontvangstjournaal maken die gebruikmaakt van magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="a459e-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="a459e-115">Het volgende scenario laat zien hoe u een koptekst van een artikelontvangstjournaal maakt die magazijnbeheer gebruikt:</span><span class="sxs-lookup"><span data-stu-id="a459e-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="a459e-116">Controleer of uw systeem een bevestigde inkooporder bevat die voldoet aan de vereisten uit de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="a459e-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="a459e-117">In dit scenario wordt een inkooporder gebruikt voor bedrijf *USMF*, leverancierrekening *1001*, magazijn *51*, met een orderregel voor *10 PL* (10 pallets) van artikelnummer *M9200*.</span><span class="sxs-lookup"><span data-stu-id="a459e-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="a459e-118">Noteer het nummer van de inkooporder die u gaat gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a459e-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="a459e-119">Ga naar **Voorraadbeheer \> Journaalposten \> Artikelontvangst \> Artikelontvangst**.</span><span class="sxs-lookup"><span data-stu-id="a459e-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="a459e-120">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a459e-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="a459e-121">Het dialoogvenster **Magazijnbeheerjournaal maken** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="a459e-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="a459e-122">Selecteer een journaalnaam in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="a459e-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="a459e-123">Als u voorbeeldgegevens van *USMF* gebruikt, selecteert u *WHS*.</span><span class="sxs-lookup"><span data-stu-id="a459e-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="a459e-124">Als u uw eigen gegevens gebruikt, moet voor het journaal dat u kiest **Orderverzamellocatie controleren** worden ingesteld op *Nee* en **Quarantainebeheer** op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="a459e-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="a459e-125">Stel **Verwijzing** in op *Inkooporder*.</span><span class="sxs-lookup"><span data-stu-id="a459e-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="a459e-126">Stel **Rekeningnummer** in op *1001*.</span><span class="sxs-lookup"><span data-stu-id="a459e-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="a459e-127">Stel **Nummer** in op het nummer van de inkooporder die u voor deze oefening hebt geïdentificeerd.</span><span class="sxs-lookup"><span data-stu-id="a459e-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="a459e-128">![Artikelontvangstjournaal](../media/item-arrival-journal-header.png "Artikelontvangstjournaal")</span><span class="sxs-lookup"><span data-stu-id="a459e-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="a459e-129">Selecteer **OK** om de journaalkop te maken.</span><span class="sxs-lookup"><span data-stu-id="a459e-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="a459e-130">Selecteer in de sectie **Journaalregels** de optie **Regels toevoegen** en voer de volgende gegevens in:</span><span class="sxs-lookup"><span data-stu-id="a459e-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="a459e-131">**Artikelnummer**: stel in op *M9200*.</span><span class="sxs-lookup"><span data-stu-id="a459e-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="a459e-132">De opties **Site**, **Magazijn** en **Hoeveelheid** worden ingesteld op basis van de voorraadtransactiegegevens voor de 10 pallets (1000 artikelen).</span><span class="sxs-lookup"><span data-stu-id="a459e-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="a459e-133">**Locatie**: stel in op *001*.</span><span class="sxs-lookup"><span data-stu-id="a459e-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="a459e-134">Deze specifieke locatie houdt geen nummerplaten bij.</span><span class="sxs-lookup"><span data-stu-id="a459e-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="a459e-135">![Artikelontvangstjournaalregel](../media/item-arrival-journal-line.png "Artikelontvangstjournaalregel")</span><span class="sxs-lookup"><span data-stu-id="a459e-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="a459e-136">Het veld **Datum** bepaalt de datum waarop de voorhanden hoeveelheid van het artikel in de voorraad wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="a459e-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="a459e-137">De **partij-id** wordt door het systeem ingevuld als deze uniek kan worden geïdentificeerd uit de opgegeven informatie.</span><span class="sxs-lookup"><span data-stu-id="a459e-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="a459e-138">Anders moet u deze handmatig invoeren.</span><span class="sxs-lookup"><span data-stu-id="a459e-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="a459e-139">Dit is een vereist veld, dat deze registratie aan een specifieke brondocumentregel koppelt.</span><span class="sxs-lookup"><span data-stu-id="a459e-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="a459e-140">Selecteer **Valideren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a459e-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="a459e-141">Dit controleert of het journaal gereed is om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="a459e-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="a459e-142">Als validatie mislukt, kunt u de fouten bevestigen voordat u het journaal kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="a459e-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="a459e-143">Het dialoogvenster **Journaal controleren** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="a459e-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="a459e-144">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a459e-144">Select **OK**.</span></span>
1. <span data-ttu-id="a459e-145">Controleer de berichtenbalk.</span><span class="sxs-lookup"><span data-stu-id="a459e-145">Review the message bar.</span></span> <span data-ttu-id="a459e-146">Er zou een bericht moeten zijn dat aangeeft dat de bewerking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="a459e-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="a459e-147">Selecteer **Boeken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a459e-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="a459e-148">Het dialoogvenster **Journaal boeken** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="a459e-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="a459e-149">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a459e-149">Select **OK**.</span></span>
1. <span data-ttu-id="a459e-150">Controleer de berichtenbalk.</span><span class="sxs-lookup"><span data-stu-id="a459e-150">Review the message bar.</span></span> <span data-ttu-id="a459e-151">Er zouden berichten moeten zijn die aangeven dat de bewerking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="a459e-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="a459e-152">Selecteer **Functies > Productontvangstbon** in het actievenster om de inkooporderregel bij te werken en een productontvangstbon te boeken.</span><span class="sxs-lookup"><span data-stu-id="a459e-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
