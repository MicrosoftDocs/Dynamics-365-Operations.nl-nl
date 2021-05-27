---
title: Quarantainezones voor niet-conformeringen
description: In dit onderwerp wordt beschreven hoe u quarantainezones voor niet-conformeringen maakt en gebruikt.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021799"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="6a6df-103">Quarantainezones voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6a6df-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a6df-104">In dit onderwerp wordt beschreven hoe u quarantainezones voor niet-conformeringen maakt en gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6a6df-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="6a6df-105">U kunt de pagina **Quarantainezones** gebruiken om zones te definiëren die kunnen worden toegewezen aan niet-conformeringen.</span><span class="sxs-lookup"><span data-stu-id="6a6df-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="6a6df-106">Wanneer u een niet-conformering maakt, kunt u de velden **Quarantainezone** en **Quarantainetype** instellen op het tabblad **Algemeen** van de pagina **Niet-conformeringen**.</span><span class="sxs-lookup"><span data-stu-id="6a6df-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="6a6df-107">Het veld **Quarantainezone** geeft gewoonlijk het gebied of de locatie aan waar het artikel zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="6a6df-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="6a6df-108">In het veld **Quarantainetype** wordt het artikel gedefinieerd als *Beperkt gebruik* of *Onbruikbaar*.</span><span class="sxs-lookup"><span data-stu-id="6a6df-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="6a6df-109">Wanneer u een niet-conformering of een correctierapport voor een niet-conformering afdrukt, kunt u de quarantainezone weergeven waar het artikel zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="6a6df-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="6a6df-110">U kunt ook een niet-conformeringslabel voor een niet-conformering afdrukken.</span><span class="sxs-lookup"><span data-stu-id="6a6df-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="6a6df-111">In dit rapport worden de toegewezen quarantainezone en informatie over gebruik weergegeven als richtlijn voor het verwerken van defect materiaal.</span><span class="sxs-lookup"><span data-stu-id="6a6df-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="6a6df-112">De quarantainezones corresponderen mogelijk met voorraadlocaties of bronnen voor bedrijfsactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="6a6df-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="6a6df-113">Voorbeelden van quarantainezones</span><span class="sxs-lookup"><span data-stu-id="6a6df-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="6a6df-114">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="6a6df-114">Example 1</span></span>

<span data-ttu-id="6a6df-115">U werkt in een elektronicaproductiebedrijf dat onder andere televisies, luidsprekers en mediaspelers produceert en distribueert.</span><span class="sxs-lookup"><span data-stu-id="6a6df-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="6a6df-116">In dit geval kunt u een quarantainezone configureren voor elk type product.</span><span class="sxs-lookup"><span data-stu-id="6a6df-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="6a6df-117">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="6a6df-117">Example 2</span></span>

<span data-ttu-id="6a6df-118">Er worden drie bakken en twee rekken gebruikt voor het opslaan van niet-conforme artikelen.</span><span class="sxs-lookup"><span data-stu-id="6a6df-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="6a6df-119">In dit geval kunt u vijf quarantainezones configureren, één voor elke bak en elk rek.</span><span class="sxs-lookup"><span data-stu-id="6a6df-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="6a6df-120">Een quarantainezone maken</span><span class="sxs-lookup"><span data-stu-id="6a6df-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="6a6df-121">Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Quarantainezones**.</span><span class="sxs-lookup"><span data-stu-id="6a6df-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="6a6df-122">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="6a6df-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6a6df-123">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="6a6df-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6a6df-124">**Quarantainezone**: geef een unieke id of naam op voor de quarantainezone.</span><span class="sxs-lookup"><span data-stu-id="6a6df-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="6a6df-125">**Beschrijving**: voer een gedetailleerde beschrijving voor de quarantainezone in.</span><span class="sxs-lookup"><span data-stu-id="6a6df-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="6a6df-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6a6df-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a6df-127">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="6a6df-127">Additional resources</span></span>

- [<span data-ttu-id="6a6df-128">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="6a6df-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="6a6df-129">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="6a6df-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="6a6df-130">Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6a6df-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="6a6df-131">Probleemtypen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6a6df-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="6a6df-132">Typen diagnosen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6a6df-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="6a6df-133">Kwaliteitstoeslagen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6a6df-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="6a6df-134">Bewerkingen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6a6df-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="6a6df-135">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="6a6df-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
