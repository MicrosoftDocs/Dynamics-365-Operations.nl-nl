--- 
title: Gegevensmodellen uitbreiden voor het gebruik van documentbeheerbestanden in ER-uitvoer
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8363dd2af728577175a620d7b645d90cea84803a
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="extend-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="71196-103">Gegevensmodellen uitbreiden voor het gebruik van documentbeheerbestanden in ER-uitvoer</span><span class="sxs-lookup"><span data-stu-id="71196-103">Extend data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71196-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="71196-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="71196-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="71196-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="71196-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de taakbegeleiding "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 1: Gegevensmodel voorbereiden)".</span><span class="sxs-lookup"><span data-stu-id="71196-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="71196-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="71196-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="71196-108">Gegevensmodel uitbreiden om de Documentbeheerbestanden erin weer te geven</span><span class="sxs-lookup"><span data-stu-id="71196-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="71196-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="71196-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="71196-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="71196-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="71196-111">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="71196-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="71196-112">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="71196-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="71196-113">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="71196-113">Click Designer.</span></span>
6. <span data-ttu-id="71196-114">Selecteer in de structuur Klantfactuur (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="71196-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="71196-115">Wij zullen dit gegevensmodel uitbreiden om daarin bestanden weer te geven die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="71196-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="71196-116">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="71196-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="71196-117">Typ Factuurbijlagen in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="71196-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="71196-118">Factuurbijlagen</span><span class="sxs-lookup"><span data-stu-id="71196-118">Invoice attachments</span></span>  
9. <span data-ttu-id="71196-119">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="71196-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="71196-120">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71196-120">Click Add.</span></span>
11. <span data-ttu-id="71196-121">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="71196-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="71196-122">Typ Bestandsinhoud in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="71196-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="71196-123">Bestandsinhoud</span><span class="sxs-lookup"><span data-stu-id="71196-123">File content</span></span>  
13. <span data-ttu-id="71196-124">Selecteer Container in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="71196-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="71196-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71196-125">Click Add.</span></span>
15. <span data-ttu-id="71196-126">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="71196-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="71196-127">Typ Bestandsnaam in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="71196-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="71196-128">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="71196-128">File name</span></span>  
17. <span data-ttu-id="71196-129">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="71196-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="71196-130">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71196-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="71196-131">Nieuwe gegevensmodelelementen toewijzen aan gegevensbronnen van Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="71196-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="71196-132">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="71196-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="71196-133">Gebruik het snelfilter om op het veld Definitie te filteren met de waarde InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="71196-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="71196-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="71196-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="71196-135">Wij zullen nieuwe modelelementen toewijzen aan tot geschikte gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="71196-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="71196-136">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="71196-136">Click Designer.</span></span>
4. <span data-ttu-id="71196-137">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="71196-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="71196-138">Vouw in de structuur Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="71196-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="71196-139">Selecteer in de structuur Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="71196-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="71196-140">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="71196-140">Click Edit.</span></span>
8. <span data-ttu-id="71196-141">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="71196-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="71196-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="71196-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="71196-143">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="71196-143">Click Save.</span></span>
10. <span data-ttu-id="71196-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71196-144">Close the page.</span></span>
11. <span data-ttu-id="71196-145">Selecteer in de structuur Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="71196-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="71196-146">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="71196-146">Click Edit.</span></span>
13. <span data-ttu-id="71196-147">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="71196-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="71196-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="71196-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="71196-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="71196-149">Click Save.</span></span>
15. <span data-ttu-id="71196-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71196-150">Close the page.</span></span>
16. <span data-ttu-id="71196-151">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="71196-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="71196-152">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="71196-152">Click Edit.</span></span>
18. <span data-ttu-id="71196-153">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="71196-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="71196-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="71196-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="71196-155">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="71196-155">Click Save.</span></span>
20. <span data-ttu-id="71196-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71196-156">Close the page.</span></span>
21. <span data-ttu-id="71196-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="71196-157">Click Save.</span></span>
22. <span data-ttu-id="71196-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71196-158">Close the page.</span></span>
23. <span data-ttu-id="71196-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71196-159">Close the page.</span></span>
24. <span data-ttu-id="71196-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71196-160">Close the page.</span></span>
25. <span data-ttu-id="71196-161">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="71196-161">Click Change status.</span></span>
26. <span data-ttu-id="71196-162">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="71196-162">Click Complete.</span></span>
27. <span data-ttu-id="71196-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="71196-163">Click OK.</span></span>


