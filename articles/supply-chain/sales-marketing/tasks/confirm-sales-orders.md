---
title: Verkooporders bevestigen
description: Deze procedure demonstreert hoe verkooporders worden bevestigd.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "323980"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="97aee-103">Verkooporders bevestigen</span><span class="sxs-lookup"><span data-stu-id="97aee-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97aee-104">Deze procedure demonstreert hoe verkooporders worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="97aee-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="97aee-105">U ziet hoe u één order bevestigt en hoe u meerdere orders tegelijk bevestigt.</span><span class="sxs-lookup"><span data-stu-id="97aee-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="97aee-106">Deze taken worden meestal uitgevoerd door een verkooporderverwerker.</span><span class="sxs-lookup"><span data-stu-id="97aee-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="97aee-107">U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="97aee-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="97aee-108">Voordat u begint, moet u ervoor zorgen dat er meerdere openstaande verkooporders voor dezelfde klant zijn.</span><span class="sxs-lookup"><span data-stu-id="97aee-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="97aee-109">Als u USMF gebruikt, kunt u klant US-027 gebruiken.</span><span class="sxs-lookup"><span data-stu-id="97aee-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="97aee-110">Eén verkooporder bevestigen</span><span class="sxs-lookup"><span data-stu-id="97aee-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="97aee-111">Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="97aee-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="97aee-112">Zoek en selecteer in de lijst de order die u wilt bevestigen.</span><span class="sxs-lookup"><span data-stu-id="97aee-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="97aee-113">Klik op de koppeling in het verkoopordernummer om de geselecteerde order te openen.</span><span class="sxs-lookup"><span data-stu-id="97aee-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="97aee-114">Klik in het actievenster op Verkopen.</span><span class="sxs-lookup"><span data-stu-id="97aee-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="97aee-115">Klik op Verkooporder bevestigen.</span><span class="sxs-lookup"><span data-stu-id="97aee-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="97aee-116">Vouw de sectie Parameters uit of samen.</span><span class="sxs-lookup"><span data-stu-id="97aee-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="97aee-117">Zorg dat het veld Boeking Ja actief is.</span><span class="sxs-lookup"><span data-stu-id="97aee-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="97aee-118">Stel de optie Bevestiging afdrukken in op Ja.</span><span class="sxs-lookup"><span data-stu-id="97aee-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="97aee-119">Het veld Kredietlimiet controleren geeft de methode op die wordt gebruikt om het resterende krediet van een klant te berekenen.</span><span class="sxs-lookup"><span data-stu-id="97aee-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="97aee-120">Dit wordt standaard gekopieerd van de pagina Parameters van module Klanten.</span><span class="sxs-lookup"><span data-stu-id="97aee-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="97aee-121">Als u de kredietlimietcontrole wilt overslaan wanneer u een specifieke verkooporder bevestigt, stelt u Kredietlimiet controleren in op Geen.</span><span class="sxs-lookup"><span data-stu-id="97aee-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="97aee-122">U moet er echter rekening mee houden dat ook als dit veld is ingesteld op Geen, de kredietlimietcontrole nog steeds wordt uitgevoerd als de optie Verplichte kredietlimiet is geselecteerd in de klanthoofdgegevens.</span><span class="sxs-lookup"><span data-stu-id="97aee-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="97aee-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="97aee-123">Click OK.</span></span>
9. <span data-ttu-id="97aee-124">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="97aee-124">Click Yes.</span></span>
10. <span data-ttu-id="97aee-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="97aee-125">Close the page.</span></span>
11. <span data-ttu-id="97aee-126">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="97aee-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="97aee-127">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="97aee-127">Click Change view.</span></span>
13. <span data-ttu-id="97aee-128">Klik op Weergave kopteksten.</span><span class="sxs-lookup"><span data-stu-id="97aee-128">Click Header view.</span></span>
    * <span data-ttu-id="97aee-129">Wanneer een order wordt bevestigd, wordt de Documentstatus ingesteld op Bevestiging.</span><span class="sxs-lookup"><span data-stu-id="97aee-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="97aee-130">Klik in het actievenster op Verkopen.</span><span class="sxs-lookup"><span data-stu-id="97aee-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="97aee-131">Klik op Bevestiging verkooporder.</span><span class="sxs-lookup"><span data-stu-id="97aee-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="97aee-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="97aee-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="97aee-133">Meerdere verkooporders in één keer bevestigen</span><span class="sxs-lookup"><span data-stu-id="97aee-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="97aee-134">Ga naar Verkoop en marketing > Verkooporders > Orderbevestiging > Verkooporder bevestigen.</span><span class="sxs-lookup"><span data-stu-id="97aee-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="97aee-135">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="97aee-135">Click Select.</span></span>
3. <span data-ttu-id="97aee-136">Zoek en selecteer in de lijst op het tabblad Bereik de record die verwijst naar het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="97aee-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="97aee-137">Klik in het veld Criteria op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="97aee-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="97aee-138">Zoek en selecteer in de lijst de klantrekening die meerdere orders heeft die u massaal wilt bevestigen.</span><span class="sxs-lookup"><span data-stu-id="97aee-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="97aee-139">Als u USMF gebruikt, kunt u rekening US-027 selecteren.</span><span class="sxs-lookup"><span data-stu-id="97aee-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="97aee-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="97aee-140">Click OK.</span></span>
    * <span data-ttu-id="97aee-141">Het tabblad Overzicht bevat een lijst met orders die aan de querycriteria voldoen.</span><span class="sxs-lookup"><span data-stu-id="97aee-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="97aee-142">Deze worden in de bevestiging opgenomen.</span><span class="sxs-lookup"><span data-stu-id="97aee-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="97aee-143">Het veld Overzicht bijwerken voor geeft de parameter op waarmee meerdere orders worden samengevat in één bevestigingsdocument.</span><span class="sxs-lookup"><span data-stu-id="97aee-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="97aee-144">Standaard wordt de optie gekopieerd van de instelling Standaardwaarden voor bijwerking van samenvatting op de pagina Parameters van module Klanten.</span><span class="sxs-lookup"><span data-stu-id="97aee-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="97aee-145">Selecteer 'Order' in het veld Overzicht bijwerken voor.</span><span class="sxs-lookup"><span data-stu-id="97aee-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="97aee-146">De minimale parameters die vereist zijn voor het maken van overzichtsupdates, zijn Factuurrekening en Valuta.</span><span class="sxs-lookup"><span data-stu-id="97aee-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="97aee-147">Dit betekent dat overzichtsupdates die verschillende factuurrekeningen en verschillende valuta hebben, niet zijn toegestaan.</span><span class="sxs-lookup"><span data-stu-id="97aee-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="97aee-148">Extra parameters kunnen worden ingesteld op de pagina Overzicht van updateparameters, die vanaf de pagina Parameters van module Klanten toegankelijk is.</span><span class="sxs-lookup"><span data-stu-id="97aee-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="97aee-149">Klik in het veld Verkooporder op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="97aee-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="97aee-150">Selecteer in de lijst het verkoopordernummer dat u in de overzichtsorder wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="97aee-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="97aee-151">Klik op Schikken.</span><span class="sxs-lookup"><span data-stu-id="97aee-151">Click Arrange.</span></span>
11. <span data-ttu-id="97aee-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="97aee-152">Click OK.</span></span>
12. <span data-ttu-id="97aee-153">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="97aee-153">Click OK.</span></span>

