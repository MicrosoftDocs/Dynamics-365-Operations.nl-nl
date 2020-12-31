---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 1: Indeling maken)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1742582057cc912d8e6f90eb14e9e4cdcd193608
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684710"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="b4284-103">ER Indeling configureren voor tellen en totaliseren (deel 1: Indeling maken)</span><span class="sxs-lookup"><span data-stu-id="b4284-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4284-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="b4284-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="b4284-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b4284-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b4284-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="b4284-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="b4284-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="b4284-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="b4284-108">Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd</span><span class="sxs-lookup"><span data-stu-id="b4284-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b4284-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="b4284-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b4284-110">Zorg ervoor dat de leverancier "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="b4284-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="b4284-111">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="b4284-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="b4284-112">Selecteer "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="b4284-112">Select the "Litware, Inc."</span></span> <span data-ttu-id="b4284-113">.</span><span class="sxs-lookup"><span data-stu-id="b4284-113">provider.</span></span>
3. <span data-ttu-id="b4284-114">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="b4284-114">Click Repositories.</span></span>
    * <span data-ttu-id="b4284-115">Als een opslagplaats van het type Bron voor bedrijfsactiviteiten bestaat, slaat u de resterende stappen van de huidige deeltaak over.</span><span class="sxs-lookup"><span data-stu-id="b4284-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="b4284-116">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b4284-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="b4284-117">Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.</span><span class="sxs-lookup"><span data-stu-id="b4284-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="b4284-118">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="b4284-118">Click Create repository.</span></span>
7. <span data-ttu-id="b4284-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b4284-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="b4284-120">Intrastat-configuraties ophalen die door Microsoft worden geleverd</span><span class="sxs-lookup"><span data-stu-id="b4284-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b4284-121">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="b4284-121">Click Open.</span></span>
2. <span data-ttu-id="b4284-122">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="b4284-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="b4284-123">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="b4284-123">Click Import.</span></span>
    * <span data-ttu-id="b4284-124">Klik op Importeren voor versie 1.1 van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="b4284-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="b4284-125">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="b4284-125">Click Yes.</span></span>
5. <span data-ttu-id="b4284-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b4284-126">Close the page.</span></span>
6. <span data-ttu-id="b4284-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b4284-127">Close the page.</span></span>
7. <span data-ttu-id="b4284-128">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="b4284-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="b4284-129">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="b4284-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="b4284-130">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="b4284-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

