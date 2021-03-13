---
title: 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 1: Gegevensmodel voorbereiden)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage (ER) configureert om documentbeheerbestanden (bijlagen) te gebruiken in ER-uitvoer. (Deel 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bff518c60f0f36bdc88245d79bd82f0c4d0599ed
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092636"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="f5068-104">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 1: Gegevensmodel voorbereiden)</span><span class="sxs-lookup"><span data-stu-id="f5068-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5068-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="f5068-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f5068-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f5068-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f5068-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="f5068-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="f5068-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="f5068-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="f5068-109">Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd</span><span class="sxs-lookup"><span data-stu-id="f5068-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f5068-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="f5068-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="f5068-111">Zorg ervoor dat de leverancier 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="f5068-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="f5068-112">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="f5068-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="f5068-113">Selecteer 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="f5068-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="f5068-114">.</span><span class="sxs-lookup"><span data-stu-id="f5068-114">provider.</span></span>
3. <span data-ttu-id="f5068-115">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="f5068-115">Click Repositories.</span></span>

    <span data-ttu-id="f5068-116">Als een opslagplaats van het type Bron voor bedrijfsactiviteiten bestaat, slaat u de resterende stappen van de huidige deeltaak over.</span><span class="sxs-lookup"><span data-stu-id="f5068-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="f5068-117">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="f5068-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="f5068-118">Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.</span><span class="sxs-lookup"><span data-stu-id="f5068-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="f5068-119">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="f5068-119">Click Create repository.</span></span>
7. <span data-ttu-id="f5068-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f5068-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="f5068-121">Haal de Klantfactuurmodelconfiguraties op die door Microsoft zijn verstrekt</span><span class="sxs-lookup"><span data-stu-id="f5068-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f5068-122">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="f5068-122">Click Show filters.</span></span>
2. <span data-ttu-id="f5068-123">Pas de volgende filters toe: voer een filterwaarde 'Bron voor bedrijfsactiviteiten' in in het veld Naam met de filteroperator 'begint met'. Voer een filterwaarde van "" in in het veld Omschrijving met de filteroperator 'begint met'.</span><span class="sxs-lookup"><span data-stu-id="f5068-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="f5068-124">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="f5068-124">Click Show filters.</span></span>
4. <span data-ttu-id="f5068-125">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="f5068-125">Click Open.</span></span>
5. <span data-ttu-id="f5068-126">Selecteer in de structuur Klantfactuurmodel.</span><span class="sxs-lookup"><span data-stu-id="f5068-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="f5068-127">Selecteer de modelconfiguratie Klantfactuurmodel om deze te importeren.</span><span class="sxs-lookup"><span data-stu-id="f5068-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="f5068-128">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="f5068-128">Click Import.</span></span>

    <span data-ttu-id="f5068-129">Klik op Importeren voor versie 1 van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="f5068-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="f5068-130">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="f5068-130">Click Yes.</span></span>
8. <span data-ttu-id="f5068-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f5068-131">Close the page.</span></span>
9. <span data-ttu-id="f5068-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f5068-132">Close the page.</span></span>
10. <span data-ttu-id="f5068-133">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="f5068-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="f5068-134">Selecteer in de structuur Klantfactuurmodel.</span><span class="sxs-lookup"><span data-stu-id="f5068-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="f5068-135">Maak het afgeleide model om toegang tot de Documentbeheerbestanden te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="f5068-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="f5068-136">U moet een eigen configuratie van het Klantfactuurmodel maken door deze af te leiden van de configuratie die door Microsoft is aangeleverd.</span><span class="sxs-lookup"><span data-stu-id="f5068-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="f5068-137">Gebruik deze configuratie om de toegang tot de Documentbeheerbestanden te implementeren en ze beschikbaar te maken voor elektronische documenten die u op basis van dit model wilt maken.</span><span class="sxs-lookup"><span data-stu-id="f5068-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="f5068-138">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="f5068-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="f5068-139">Typ in het veld Nieuw 'Afleiden van naam: Klantfactuurmodel, Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="f5068-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="f5068-140">Typ 'Klantfactuurmodel (aangepast)' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f5068-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="f5068-141">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="f5068-141">Click Create configuration.</span></span>

