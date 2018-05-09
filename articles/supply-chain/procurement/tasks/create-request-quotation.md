--- 
title: Een offerteaanvraag maken
description: Deze procedure laat u zien hoe u een offerteaanvraag maakt.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9e7deb10cc0e5669d209ad7340108911a37bbc89
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="17489-103">Een offerteaanvraag maken</span><span class="sxs-lookup"><span data-stu-id="17489-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17489-104">Deze procedure laat u zien hoe u een offerteaanvraag maakt.</span><span class="sxs-lookup"><span data-stu-id="17489-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="17489-105">Dit wordt gewoonlijk gedaan door een inkoper.</span><span class="sxs-lookup"><span data-stu-id="17489-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="17489-106">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="17489-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="17489-107">U moet de verzoektypen hebben ingesteld voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="17489-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="17489-108">Zodra u deze taak hebt voltooid en een offerteaanvraag hebt gemaakt en verzonden, kunt u de antwoorden per leverancier invoeren, deze vergelijken en het contract toekennen.</span><span class="sxs-lookup"><span data-stu-id="17489-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="17489-109">Een nieuwe offerteaanvraag voorbereiden</span><span class="sxs-lookup"><span data-stu-id="17489-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="17489-110">Ga naar Inkoop en sourcing > Offerteaanvragen > Alle offerteaanvragen.</span><span class="sxs-lookup"><span data-stu-id="17489-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="17489-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="17489-111">Click New.</span></span>
    * <span data-ttu-id="17489-112">De volgende inkooptypen zijn beschikbaar: Inkooporder (dit is de standaard): een document dat het aanbod om producten te kopen of de acceptatie van een aanbod om producten te verkopen tegen een betaling bevestigt.</span><span class="sxs-lookup"><span data-stu-id="17489-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="17489-113">Opdracht tot inkoop: dit type wordt automatisch geselecteerd als u een offerteaanvraag rechtstreeks vanuit een opdracht tot inkoop maakt.</span><span class="sxs-lookup"><span data-stu-id="17489-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="17489-114">Als u deze optie handmatig selecteert, verschijnt er een foutmelding.</span><span class="sxs-lookup"><span data-stu-id="17489-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="17489-115">Inkoopovereenkomst: een overeenkomst voor de aanschaf van een bepaalde hoeveelheid of waarde van een product in een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="17489-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="17489-116">Als u deze optie selecteert, moet u het datumbereik selecteren dat van toepassing is op de inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="17489-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="17489-117">Typ een waarde in het veld Documenttitel.</span><span class="sxs-lookup"><span data-stu-id="17489-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="17489-118">Typ of selecteer een waarde in het veld Verzoektype.</span><span class="sxs-lookup"><span data-stu-id="17489-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="17489-119">Als een beoordelingsmethode aan het verzoektype is gekoppeld, wordt dit de standaardbeoordelingsmethode voor de offerteaanvraag die u maakt.</span><span class="sxs-lookup"><span data-stu-id="17489-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="17489-120">Het is mogelijk om de beoordelingsmethode later te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="17489-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="17489-121">Typ een datum in het veld Leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="17489-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="17489-122">Selecteer de datum waarop u de artikelen wilt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="17489-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="17489-123">Voer in het veld Vervaldatum en -tijd een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="17489-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="17489-124">Geef de datum en tijd op wanneer leveranciers de offerteaanvraag moeten beantwoorden.</span><span class="sxs-lookup"><span data-stu-id="17489-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="17489-125">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="17489-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="17489-126">Het afleveradres wordt standaard ingesteld op het magazijnadres.</span><span class="sxs-lookup"><span data-stu-id="17489-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="17489-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="17489-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="17489-128">Regels toevoegen</span><span class="sxs-lookup"><span data-stu-id="17489-128">Add lines</span></span>
    * <span data-ttu-id="17489-129">Nadat u de basisgegevens over uw offerteaanvraag hebt opgegeven, geeft u de goederen of services op waarop u wilt dat leveranciers bieden.</span><span class="sxs-lookup"><span data-stu-id="17489-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="17489-130">Artikel is het standaardregeltype.</span><span class="sxs-lookup"><span data-stu-id="17489-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="17489-131">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="17489-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="17489-132">Als u USMF gebruikt, kunt u T0020 selecteren.</span><span class="sxs-lookup"><span data-stu-id="17489-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="17489-133">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="17489-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="17489-134">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="17489-134">Click Add line.</span></span>
4. <span data-ttu-id="17489-135">Selecteer 'Categorie' in het veld Regeltype.</span><span class="sxs-lookup"><span data-stu-id="17489-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="17489-136">U kunt het categorieregeltype gebruiken om offerteaanvragen voor niet-voorraadgoederen of -services te maken.</span><span class="sxs-lookup"><span data-stu-id="17489-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="17489-137">U moet vervolgens het type goederen of services van een hiërarchie van aanschaffingscategorieën selecteren.</span><span class="sxs-lookup"><span data-stu-id="17489-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="17489-138">Typ of selecteer een waarde in het veld Aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="17489-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="17489-139">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="17489-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="17489-140">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="17489-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="17489-141">Typ of selecteer een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="17489-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="17489-142">Leveranciers toevoegen</span><span class="sxs-lookup"><span data-stu-id="17489-142">Add vendors</span></span>
1. <span data-ttu-id="17489-143">Klik op Koptekst om van de weergave Regels over te schakelen naar de weergave Koptekst.</span><span class="sxs-lookup"><span data-stu-id="17489-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="17489-144">Vouw de sectie Leverancier uit.</span><span class="sxs-lookup"><span data-stu-id="17489-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="17489-145">Klik op Leveranciers automatisch toevoegen.</span><span class="sxs-lookup"><span data-stu-id="17489-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="17489-146">U kunt leveranciers automatisch aan de offerteaanvraag toevoegen op basis van de aanschaffingscategorie van de gevraagde artikelen.</span><span class="sxs-lookup"><span data-stu-id="17489-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="17489-147">Als er geen leveranciers zijn goedgekeurd voor de categorieën die zijn opgenomen in de regels, kunt u leveranciers handmatig toevoegen.</span><span class="sxs-lookup"><span data-stu-id="17489-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="17489-148">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="17489-148">Click Add.</span></span>
5. <span data-ttu-id="17489-149">Typ of selecteer een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="17489-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="17489-150">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="17489-150">Click Add.</span></span>
7. <span data-ttu-id="17489-151">Typ of selecteer een waarde in het veld Leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="17489-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="17489-152">Zodra u een leverancier hebt geselecteerd, is de status gemaakt.</span><span class="sxs-lookup"><span data-stu-id="17489-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="17489-153">Dat wil zeggen dat de leveranciersgegevens in de RFQ zijn opgeslagen, maar dat u de RFQ niet naar de leverancier hebt gezonden.</span><span class="sxs-lookup"><span data-stu-id="17489-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="17489-154">U kunt een leverancier aan een RFQ toevoegen, ongeacht de status van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="17489-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="17489-155">Offerteaanvraag verzenden naar leveranciers</span><span class="sxs-lookup"><span data-stu-id="17489-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="17489-156">Klik op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="17489-156">Click Send.</span></span>
    * <span data-ttu-id="17489-157">Controleer op de pagina Offerteaanvraag verzenden of de leveranciers in de lijst de leveranciers zijn die de offerteaanvraag moeten ontvangen.</span><span class="sxs-lookup"><span data-stu-id="17489-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="17489-158">Klik op Afdrukken.</span><span class="sxs-lookup"><span data-stu-id="17489-158">Click Print.</span></span>
    * <span data-ttu-id="17489-159">In dit dialoogvenster kunt u de offerteaanvraag afdrukken.</span><span class="sxs-lookup"><span data-stu-id="17489-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="17489-160">Als u ervoor kiest een antwoordblad af te drukken, wordt de inhoud hiervan gedefinieerd in Parameters voor inkoop en sourcing.</span><span class="sxs-lookup"><span data-stu-id="17489-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="17489-161">Om te bepalen hoe u antwoordbladen afdrukt, klikt u op Geavanceerde afdrukopties zodra u het dialoogvenster Afdrukken hebt geopend.</span><span class="sxs-lookup"><span data-stu-id="17489-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="17489-162">Er wordt voor elke leverancier een offerteaanvraag afgedrukt met de regels die de status Gemaakt of Verzonden hebben.</span><span class="sxs-lookup"><span data-stu-id="17489-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="17489-163">Geannuleerde regels en regels met geregistreerde antwoorden worden niet afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="17489-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="17489-164">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="17489-164">Click Cancel.</span></span>
4. <span data-ttu-id="17489-165">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="17489-165">Click OK.</span></span>
5. <span data-ttu-id="17489-166">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="17489-166">Close the page.</span></span>
6. <span data-ttu-id="17489-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="17489-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="17489-168">Het offerteaanvraagjournaal weergeven</span><span class="sxs-lookup"><span data-stu-id="17489-168">View the RFQ journal</span></span>
1. <span data-ttu-id="17489-169">Ga naar Inkoop en sourcing > Offerteaanvragen > Opvolging op offerteaanvragen > Offerteaanvraagjournalen.</span><span class="sxs-lookup"><span data-stu-id="17489-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="17489-170">Klik op Voorbeeld/afdrukken.</span><span class="sxs-lookup"><span data-stu-id="17489-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="17489-171">Klik op Oorspronkelijk voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="17489-171">Click Original preview.</span></span>
4. <span data-ttu-id="17489-172">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="17489-172">Close the page.</span></span>
5. <span data-ttu-id="17489-173">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="17489-173">Close the page.</span></span>


