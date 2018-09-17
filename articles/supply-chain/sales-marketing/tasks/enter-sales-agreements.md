--- 
title: Verkoopovereenkomsten invoeren
description: Deze procedure toont hoe u een verkoopovereenkomst maakt waarmee een van uw klanten toezegt in een bepaalde periode een product voor een bepaald bedrag te kopen in ruil voor speciale kortingen.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 025c9fe2f769f37b63bd79c6c3afedc31a955310
ms.contentlocale: nl-nl
ms.lasthandoff: 09/17/2018

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="c4321-103">Verkoopovereenkomsten invoeren</span><span class="sxs-lookup"><span data-stu-id="c4321-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4321-104">Deze procedure toont hoe u een verkoopovereenkomst maakt waarmee een van uw klanten toezegt in een bepaalde periode een product voor een bepaald bedrag te kopen in ruil voor speciale kortingen.</span><span class="sxs-lookup"><span data-stu-id="c4321-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="c4321-105">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="c4321-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="c4321-106">Koptekst van de verkoopovereenkomst instellen</span><span class="sxs-lookup"><span data-stu-id="c4321-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="c4321-107">Ga naar Verkoop en marketing > Verkoopovereenkomsten > Verkoopovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="c4321-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="c4321-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c4321-108">Click New.</span></span>
3. <span data-ttu-id="c4321-109">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4321-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c4321-110">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c4321-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c4321-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4321-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c4321-112">Klik in het veld Classificatie van verkoopovereenkomst op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4321-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c4321-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4321-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c4321-114">Vouw de sectie Algemeen uit.</span><span class="sxs-lookup"><span data-stu-id="c4321-114">Expand the General section.</span></span>
9. <span data-ttu-id="c4321-115">Selecteer 'Toezegging productwaarde' in het veld Standaardtoezegging.</span><span class="sxs-lookup"><span data-stu-id="c4321-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="c4321-116">Een toezeggingstype is een verplicht criterium dat u aan de overeenkomst moet toewijzen om te bepalen hoe het contact van de overeenkomst wordt afgehandeld.</span><span class="sxs-lookup"><span data-stu-id="c4321-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="c4321-117">Met de vier vooraf gedefinieerde typen kunt u het toezeggingsdoel van de klant instellen, dat als een hoeveelheid of waarde wordt uitgedrukt.</span><span class="sxs-lookup"><span data-stu-id="c4321-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="c4321-118">Het toezeggingstype voor hoeveelheid kan alleen voor een bepaald product worden toegepast, maar op de op waarde gebaseerde typen zijn van toepassing op verkoop van zowel specifieke als niet-specifieke producten.</span><span class="sxs-lookup"><span data-stu-id="c4321-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="c4321-119">Stel in het veld Vervaldatum de datum in op een toekomstige datum waarop u wilt dat de overeenkomst vervalt.</span><span class="sxs-lookup"><span data-stu-id="c4321-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="c4321-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c4321-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="c4321-121">Toezeggingsregels voor productwaarde instellen</span><span class="sxs-lookup"><span data-stu-id="c4321-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="c4321-122">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c4321-122">Click Add line.</span></span>
2. <span data-ttu-id="c4321-123">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4321-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c4321-124">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c4321-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c4321-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4321-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c4321-126">Het type van toezegging dat u voor de overeenkomst hebt gekozen beïnvloedt het soort informatie dat u voor de overeenkomstregels kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="c4321-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="c4321-127">Bij een op waarde gebaseerde overeenkomst moet u bijvoorbeeld het totale nettobedrag (in de goedgekeurde valuta) opgeven waartoe de klant zich verbindt om bij u goederen te kopen.</span><span class="sxs-lookup"><span data-stu-id="c4321-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="c4321-128">In dit voorbeeld zijn de velden Hoeveelheid en Eenheid op de regel niet beschikbaar omdat u een overeenkomst voor de klant maakt om een specifieke waarde van een product te kopen.</span><span class="sxs-lookup"><span data-stu-id="c4321-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="c4321-129">Typ in het veld Nettobedrag het monetaire bedrag waartoe de klant zich verbindt om te kopen.</span><span class="sxs-lookup"><span data-stu-id="c4321-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="c4321-130">Typ in het veld Kortingspercentage een procentuele waarde die van toepassing zal zijn op de verkooporderregels van de klant die aan deze overeenkomst zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c4321-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="c4321-131">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="c4321-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="c4321-132">Selecteer Ja het veld Max is afgedwongen.</span><span class="sxs-lookup"><span data-stu-id="c4321-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="c4321-133">Als u Max is afgedwongen selecteert, mag het totale bedrag alle verkooporderregels die de speciale prijzen, kortingen en/of betalingsvoorwaarden van de toezegging gebruiken het bedrag niet overschrijden dat op de toezegging wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c4321-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="c4321-134">De minimum- en maximumvrijgavebedragen geven een waardebereik op dat moet worden verkocht bij elke verkooporder die de geselecteerde overeenkomst gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c4321-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="c4321-135">Vouw de sectie Koptekst verkoopovereenkomst uit.</span><span class="sxs-lookup"><span data-stu-id="c4321-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="c4321-136">Tenzij de status van de overeenkomst is ingesteld op Van kracht, kunnen verkooporders niet aan de overeenkomst worden gekoppeld en daarom niet bijdragen aan de voltooiing van die overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="c4321-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="c4321-137">U kunt de status op dit moment handmatig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c4321-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="c4321-138">De status wijzigt echter normaal wanneer u de overeenkomst voor de klant bevestigt.</span><span class="sxs-lookup"><span data-stu-id="c4321-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="c4321-139">Klik in het actievenster op Verkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="c4321-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="c4321-140">Klik op Bevestiging.</span><span class="sxs-lookup"><span data-stu-id="c4321-140">Click Confirmation.</span></span>
    * <span data-ttu-id="c4321-141">Zorg ervoor dat de optie Overeenkomst als effectief markeren is ingesteld op Ja.</span><span class="sxs-lookup"><span data-stu-id="c4321-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="c4321-142">Selecteer Ja in het veld Rapport afdrukken.</span><span class="sxs-lookup"><span data-stu-id="c4321-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="c4321-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c4321-143">Click OK.</span></span>
14. <span data-ttu-id="c4321-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c4321-144">Close the page.</span></span>
    * <span data-ttu-id="c4321-145">De overeenkomst is nu van kracht en u kunt de orders van de klant beginnen te koppelen aan de overeenkomst voor het starten, om het toegezegde doel te verrekenen.</span><span class="sxs-lookup"><span data-stu-id="c4321-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


