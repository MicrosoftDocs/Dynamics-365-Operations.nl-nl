---
title: 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 2: Gegevensmodel uitbreiden)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage (ER) configureert om documentbeheerbestanden (bijlagen) te gebruiken in ER-uitvoer. (Deel 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092585"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="b2502-104">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 2: Gegevensmodel uitbreiden)</span><span class="sxs-lookup"><span data-stu-id="b2502-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2502-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="b2502-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b2502-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b2502-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="b2502-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de taakbegeleiding "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 1: Gegevensmodel voorbereiden)".</span><span class="sxs-lookup"><span data-stu-id="b2502-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="b2502-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="b2502-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="b2502-109">Gegevensmodel uitbreiden om de Documentbeheerbestanden erin weer te geven</span><span class="sxs-lookup"><span data-stu-id="b2502-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="b2502-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="b2502-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b2502-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="b2502-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b2502-112">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="b2502-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="b2502-113">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="b2502-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="b2502-114">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="b2502-114">Click Designer.</span></span>
6. <span data-ttu-id="b2502-115">Selecteer in de structuur Klantfactuur (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="b2502-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="b2502-116">Wij zullen dit gegevensmodel uitbreiden om daarin bestanden weer te geven die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="b2502-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="b2502-117">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b2502-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b2502-118">Typ Factuurbijlagen in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b2502-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="b2502-119">Factuurbijlagen</span><span class="sxs-lookup"><span data-stu-id="b2502-119">Invoice attachments</span></span>  
9. <span data-ttu-id="b2502-120">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="b2502-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="b2502-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b2502-121">Click Add.</span></span>
11. <span data-ttu-id="b2502-122">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b2502-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b2502-123">Typ Bestandsinhoud in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b2502-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="b2502-124">Bestandsinhoud</span><span class="sxs-lookup"><span data-stu-id="b2502-124">File content</span></span>  
13. <span data-ttu-id="b2502-125">Selecteer Container in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="b2502-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="b2502-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b2502-126">Click Add.</span></span>
15. <span data-ttu-id="b2502-127">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b2502-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="b2502-128">Typ Bestandsnaam in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b2502-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="b2502-129">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="b2502-129">File name</span></span>  
17. <span data-ttu-id="b2502-130">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="b2502-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="b2502-131">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b2502-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="b2502-132">Nieuwe gegevensmodelelementen toewijzen aan gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="b2502-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="b2502-133">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="b2502-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="b2502-134">Gebruik het snelfilter om op het veld Definitie te filteren met de waarde InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="b2502-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="b2502-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="b2502-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="b2502-136">Wij zullen nieuwe modelelementen toewijzen aan tot geschikte gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="b2502-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="b2502-137">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="b2502-137">Click Designer.</span></span>
4. <span data-ttu-id="b2502-138">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="b2502-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="b2502-139">Vouw in de structuur Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="b2502-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="b2502-140">Selecteer in de structuur Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="b2502-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="b2502-141">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b2502-141">Click Edit.</span></span>
8. <span data-ttu-id="b2502-142">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="b2502-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="b2502-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="b2502-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="b2502-144">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b2502-144">Click Save.</span></span>
10. <span data-ttu-id="b2502-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b2502-145">Close the page.</span></span>
11. <span data-ttu-id="b2502-146">Selecteer in de structuur Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="b2502-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="b2502-147">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b2502-147">Click Edit.</span></span>
13. <span data-ttu-id="b2502-148">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="b2502-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="b2502-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="b2502-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="b2502-150">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b2502-150">Click Save.</span></span>
15. <span data-ttu-id="b2502-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b2502-151">Close the page.</span></span>
16. <span data-ttu-id="b2502-152">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="b2502-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="b2502-153">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b2502-153">Click Edit.</span></span>
18. <span data-ttu-id="b2502-154">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="b2502-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="b2502-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="b2502-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="b2502-156">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b2502-156">Click Save.</span></span>
20. <span data-ttu-id="b2502-157">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b2502-157">Close the page.</span></span>
21. <span data-ttu-id="b2502-158">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b2502-158">Click Save.</span></span>
22. <span data-ttu-id="b2502-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b2502-159">Close the page.</span></span>
23. <span data-ttu-id="b2502-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b2502-160">Close the page.</span></span>
24. <span data-ttu-id="b2502-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b2502-161">Close the page.</span></span>
25. <span data-ttu-id="b2502-162">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b2502-162">Click Change status.</span></span>
26. <span data-ttu-id="b2502-163">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="b2502-163">Click Complete.</span></span>
27. <span data-ttu-id="b2502-164">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b2502-164">Click OK.</span></span>

