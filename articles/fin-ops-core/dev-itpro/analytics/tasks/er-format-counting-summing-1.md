---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 1: Indeling maken)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert voor tellen en totaliseren op basis van de gegevens van de reeds gegenereerde tekstuitvoer. (Deel 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 64bf9f48319029e835f9e3fe2b888625100cc408
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565137"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="0a3be-104">ER Indeling configureren voor tellen en totaliseren (deel 1: Indeling maken)</span><span class="sxs-lookup"><span data-stu-id="0a3be-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a3be-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="0a3be-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="0a3be-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0a3be-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="0a3be-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="0a3be-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="0a3be-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="0a3be-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="0a3be-109">Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd</span><span class="sxs-lookup"><span data-stu-id="0a3be-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0a3be-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="0a3be-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0a3be-111">Zorg ervoor dat de leverancier "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="0a3be-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="0a3be-112">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="0a3be-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="0a3be-113">Selecteer "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="0a3be-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="0a3be-114">.</span><span class="sxs-lookup"><span data-stu-id="0a3be-114">provider.</span></span>
3. <span data-ttu-id="0a3be-115">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="0a3be-115">Click Repositories.</span></span>
    * <span data-ttu-id="0a3be-116">Als een opslagplaats van het type Bron voor bedrijfsactiviteiten bestaat, slaat u de resterende stappen van de huidige deeltaak over.</span><span class="sxs-lookup"><span data-stu-id="0a3be-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="0a3be-117">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="0a3be-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="0a3be-118">Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.</span><span class="sxs-lookup"><span data-stu-id="0a3be-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="0a3be-119">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="0a3be-119">Click Create repository.</span></span>
7. <span data-ttu-id="0a3be-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0a3be-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="0a3be-121">Intrastat-configuraties ophalen die door Microsoft worden geleverd</span><span class="sxs-lookup"><span data-stu-id="0a3be-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0a3be-122">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="0a3be-122">Click Open.</span></span>
2. <span data-ttu-id="0a3be-123">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="0a3be-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="0a3be-124">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="0a3be-124">Click Import.</span></span>
    * <span data-ttu-id="0a3be-125">Klik op Importeren voor versie 1.1 van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="0a3be-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="0a3be-126">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="0a3be-126">Click Yes.</span></span>
5. <span data-ttu-id="0a3be-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0a3be-127">Close the page.</span></span>
6. <span data-ttu-id="0a3be-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0a3be-128">Close the page.</span></span>
7. <span data-ttu-id="0a3be-129">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="0a3be-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="0a3be-130">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="0a3be-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="0a3be-131">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="0a3be-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]