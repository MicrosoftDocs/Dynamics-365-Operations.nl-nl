---
title: 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 2: Gegevensmodel uitbreiden)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd56ad01b00dfd0fe67f2d8eb36fb2bd39e04f1c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142588"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="e5a6c-103">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 2: Gegevensmodel uitbreiden)</span><span class="sxs-lookup"><span data-stu-id="e5a6c-103">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5a6c-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e5a6c-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e5a6c-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de taakbegeleiding "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 1: Gegevensmodel voorbereiden)".</span><span class="sxs-lookup"><span data-stu-id="e5a6c-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="e5a6c-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="e5a6c-108">Gegevensmodel uitbreiden om de Documentbeheerbestanden erin weer te geven</span><span class="sxs-lookup"><span data-stu-id="e5a6c-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="e5a6c-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e5a6c-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e5a6c-111">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="e5a6c-112">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="e5a6c-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="e5a6c-113">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-113">Click Designer.</span></span>
6. <span data-ttu-id="e5a6c-114">Selecteer in de structuur Klantfactuur (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="e5a6c-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="e5a6c-115">Wij zullen dit gegevensmodel uitbreiden om daarin bestanden weer te geven die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="e5a6c-116">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e5a6c-117">Typ Factuurbijlagen in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="e5a6c-118">Factuurbijlagen</span><span class="sxs-lookup"><span data-stu-id="e5a6c-118">Invoice attachments</span></span>  
9. <span data-ttu-id="e5a6c-119">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="e5a6c-120">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-120">Click Add.</span></span>
11. <span data-ttu-id="e5a6c-121">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e5a6c-122">Typ Bestandsinhoud in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="e5a6c-123">Bestandsinhoud</span><span class="sxs-lookup"><span data-stu-id="e5a6c-123">File content</span></span>  
13. <span data-ttu-id="e5a6c-124">Selecteer Container in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="e5a6c-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-125">Click Add.</span></span>
15. <span data-ttu-id="e5a6c-126">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="e5a6c-127">Typ Bestandsnaam in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e5a6c-128">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="e5a6c-128">File name</span></span>  
17. <span data-ttu-id="e5a6c-129">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="e5a6c-130">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="e5a6c-131">Nieuwe gegevensmodelelementen toewijzen aan gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="e5a6c-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="e5a6c-132">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="e5a6c-133">Gebruik het snelfilter om op het veld Definitie te filteren met de waarde InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="e5a6c-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="e5a6c-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="e5a6c-135">Wij zullen nieuwe modelelementen toewijzen aan tot geschikte gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="e5a6c-136">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-136">Click Designer.</span></span>
4. <span data-ttu-id="e5a6c-137">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="e5a6c-138">Vouw in de structuur Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="e5a6c-139">Selecteer in de structuur Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="e5a6c-140">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-140">Click Edit.</span></span>
8. <span data-ttu-id="e5a6c-141">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="e5a6c-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="e5a6c-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="e5a6c-143">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-143">Click Save.</span></span>
10. <span data-ttu-id="e5a6c-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-144">Close the page.</span></span>
11. <span data-ttu-id="e5a6c-145">Selecteer in de structuur Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="e5a6c-146">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-146">Click Edit.</span></span>
13. <span data-ttu-id="e5a6c-147">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="e5a6c-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="e5a6c-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="e5a6c-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-149">Click Save.</span></span>
15. <span data-ttu-id="e5a6c-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-150">Close the page.</span></span>
16. <span data-ttu-id="e5a6c-151">Selecteer in de structuur Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="e5a6c-152">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-152">Click Edit.</span></span>
18. <span data-ttu-id="e5a6c-153">Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="e5a6c-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="e5a6c-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="e5a6c-155">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-155">Click Save.</span></span>
20. <span data-ttu-id="e5a6c-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-156">Close the page.</span></span>
21. <span data-ttu-id="e5a6c-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-157">Click Save.</span></span>
22. <span data-ttu-id="e5a6c-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-158">Close the page.</span></span>
23. <span data-ttu-id="e5a6c-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-159">Close the page.</span></span>
24. <span data-ttu-id="e5a6c-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-160">Close the page.</span></span>
25. <span data-ttu-id="e5a6c-161">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-161">Click Change status.</span></span>
26. <span data-ttu-id="e5a6c-162">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-162">Click Complete.</span></span>
27. <span data-ttu-id="e5a6c-163">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-163">Click OK.</span></span>

