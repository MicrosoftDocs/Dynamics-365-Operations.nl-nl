--- 
title: Gegevensmodel uitbreiden voor gebruik van documentbeheerbestanden in uitvoerindelingen voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="70a12-103">Gegevensmodel uitbreiden voor gebruik van documentbeheerbestanden in uitvoerindelingen voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="70a12-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70a12-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="70a12-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="70a12-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="70a12-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="70a12-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de taakbegeleiding "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 1: Gegevensmodel voorbereiden)".</span><span class="sxs-lookup"><span data-stu-id="70a12-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="70a12-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="70a12-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="70a12-108">Gegevensmodel uitbreiden om de Documentbeheerbestanden erin weer te geven</span><span class="sxs-lookup"><span data-stu-id="70a12-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="70a12-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="70a12-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="70a12-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="70a12-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="70a12-111">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="70a12-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="70a12-112">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="70a12-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="70a12-113">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="70a12-113">Click Designer.</span></span>
6. <span data-ttu-id="70a12-114">Selecteer in de structuur Klantfactuur (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="70a12-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="70a12-115">Wij zullen dit gegevensmodel uitbreiden om daarin bestanden weer te geven die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="70a12-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="70a12-116">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="70a12-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="70a12-117">Typ Factuurbijlagen in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="70a12-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="70a12-118">Factuurbijlagen</span><span class="sxs-lookup"><span data-stu-id="70a12-118">Invoice attachments</span></span>  
9. <span data-ttu-id="70a12-119">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="70a12-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="70a12-120">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="70a12-120">Click Add.</span></span>
11. <span data-ttu-id="70a12-121">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="70a12-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="70a12-122">Typ Bestandsinhoud in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="70a12-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="70a12-123">Bestandsinhoud</span><span class="sxs-lookup"><span data-stu-id="70a12-123">File content</span></span>  
13. <span data-ttu-id="70a12-124">Selecteer Container in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="70a12-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="70a12-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="70a12-125">Click Add.</span></span>
15. <span data-ttu-id="70a12-126">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="70a12-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="70a12-127">Typ Bestandsnaam in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="70a12-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="70a12-128">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="70a12-128">File name</span></span>  
17. <span data-ttu-id="70a12-129">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="70a12-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="70a12-130">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="70a12-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="70a12-131">Nieuwe gegevensmodelelementen toewijzen aan gegevensbronnen van Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70a12-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="70a12-132">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="70a12-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="70a12-133">Gebruik het snelfilter om op het veld Definitie te filteren met de waarde InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="70a12-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="70a12-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="70a12-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="70a12-135">Wij zullen nieuwe modelelementen toewijzen aan tot geschikte gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="70a12-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="70a12-136">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="70a12-136">Click Designer.</span></span>
4. <span data-ttu-id="70a12-137">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="70a12-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="70a12-138">Vouw in de structuur Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="70a12-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="70a12-139">Selecteer in de structuur Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="70a12-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="70a12-140">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="70a12-140">Click Edit.</span></span>
8. <span data-ttu-id="70a12-141">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="70a12-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="70a12-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="70a12-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="70a12-143">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="70a12-143">Click Save.</span></span>
10. <span data-ttu-id="70a12-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="70a12-144">Close the page.</span></span>
11. <span data-ttu-id="70a12-145">Selecteer in de structuur Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="70a12-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="70a12-146">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="70a12-146">Click Edit.</span></span>
13. <span data-ttu-id="70a12-147">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="70a12-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="70a12-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="70a12-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="70a12-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="70a12-149">Click Save.</span></span>
15. <span data-ttu-id="70a12-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="70a12-150">Close the page.</span></span>
16. <span data-ttu-id="70a12-151">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="70a12-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="70a12-152">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="70a12-152">Click Edit.</span></span>
18. <span data-ttu-id="70a12-153">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="70a12-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="70a12-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="70a12-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="70a12-155">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="70a12-155">Click Save.</span></span>
20. <span data-ttu-id="70a12-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="70a12-156">Close the page.</span></span>
21. <span data-ttu-id="70a12-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="70a12-157">Click Save.</span></span>
22. <span data-ttu-id="70a12-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="70a12-158">Close the page.</span></span>
23. <span data-ttu-id="70a12-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="70a12-159">Close the page.</span></span>
24. <span data-ttu-id="70a12-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="70a12-160">Close the page.</span></span>
25. <span data-ttu-id="70a12-161">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="70a12-161">Click Change status.</span></span>
26. <span data-ttu-id="70a12-162">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="70a12-162">Click Complete.</span></span>
27. <span data-ttu-id="70a12-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="70a12-163">Click OK.</span></span>


