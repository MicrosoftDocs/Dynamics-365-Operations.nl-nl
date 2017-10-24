--- 
title: Indeling maken voor tellen en totaliseren voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: efdb64fa157af0d96c2ff0e5de3db5a98190bc68
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="2bd49-103">Indeling maken voor tellen en totaliseren voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="2bd49-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bd49-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="2bd49-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="2bd49-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2bd49-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="2bd49-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="2bd49-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="2bd49-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="2bd49-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="2bd49-108">Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd</span><span class="sxs-lookup"><span data-stu-id="2bd49-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="2bd49-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="2bd49-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2bd49-110">Zorg ervoor dat de leverancier 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="2bd49-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="2bd49-111">beschikbaar is en als actief gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="2bd49-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="2bd49-112">Selecteer 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="2bd49-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="2bd49-113">.</span><span class="sxs-lookup"><span data-stu-id="2bd49-113">provider.</span></span>
3. <span data-ttu-id="2bd49-114">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="2bd49-114">Click Repositories.</span></span>
    * <span data-ttu-id="2bd49-115">Als een opslagplaats van het type Bron voor bedrijfsactiviteiten bestaat, slaat u de resterende stappen van de huidige deeltaak over.</span><span class="sxs-lookup"><span data-stu-id="2bd49-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="2bd49-116">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="2bd49-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="2bd49-117">Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.</span><span class="sxs-lookup"><span data-stu-id="2bd49-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="2bd49-118">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="2bd49-118">Click Create repository.</span></span>
7. <span data-ttu-id="2bd49-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2bd49-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="2bd49-120">Intrastat-configuraties ophalen die door Microsoft worden geleverd</span><span class="sxs-lookup"><span data-stu-id="2bd49-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="2bd49-121">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="2bd49-121">Click Open.</span></span>
2. <span data-ttu-id="2bd49-122">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="2bd49-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="2bd49-123">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="2bd49-123">Click Import.</span></span>
    * <span data-ttu-id="2bd49-124">Klik op Importeren voor versie 1.1 van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="2bd49-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="2bd49-125">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="2bd49-125">Click Yes.</span></span>
5. <span data-ttu-id="2bd49-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2bd49-126">Close the page.</span></span>
6. <span data-ttu-id="2bd49-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2bd49-127">Close the page.</span></span>
7. <span data-ttu-id="2bd49-128">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="2bd49-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="2bd49-129">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="2bd49-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="2bd49-130">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="2bd49-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


