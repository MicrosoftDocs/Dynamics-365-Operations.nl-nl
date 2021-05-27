---
title: Typen diagnose voor niet-conformeringen
description: In dit onderwerp wordt beschreven hoe u typen diagnoses kunt gebruiken en maken die kunnen worden gebruikt met niet-conformeringen.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022271"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="c5592-103">Typen diagnose voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="c5592-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5592-104">In dit onderwerp wordt beschreven hoe u typen diagnoses kunt gebruiken en maken die kunnen worden gebruikt met niet-conformeringen.</span><span class="sxs-lookup"><span data-stu-id="c5592-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="c5592-105">U gebruikt de pagina **Diagnosetypen** om een classificatie van diagnostische acties te definiëren.</span><span class="sxs-lookup"><span data-stu-id="c5592-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="c5592-106">Wanneer u vervolgens een correctie voor een niet-conformering maakt, selecteert u een diagnose.</span><span class="sxs-lookup"><span data-stu-id="c5592-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="c5592-107">Met een correctie wordt opgegeven welk type diagnostische actie moet worden uitgevoerd voor een goedgekeurde niet-conformering en wie de actie moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c5592-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="c5592-108">Ook worden de aangevraagde voltooiingsdatum en de geplande voltooiingsdatum opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c5592-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="c5592-109">Voorbeelden van typen diagnose</span><span class="sxs-lookup"><span data-stu-id="c5592-109">Examples of diagnostic types</span></span>

<span data-ttu-id="c5592-110">U werkt voor een productiebedrijf en verschillende artikelen voldoen niet aan de kwaliteitstests.</span><span class="sxs-lookup"><span data-stu-id="c5592-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="c5592-111">Die artikelen worden naar een quarantainegebied verplaatst en gemarkeerd als niet-conformeringsproducten.</span><span class="sxs-lookup"><span data-stu-id="c5592-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="c5592-112">Er wordt in Microsoft Dynamics 365 Supply Chain Management een niet-conformeringsrecord gemaakt om de details bij te houden via probleemoplossing.</span><span class="sxs-lookup"><span data-stu-id="c5592-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="c5592-113">In dit geval treden de kwaliteitsproblemen op omdat er lagers zijn in de machine waarin de artikelen worden verpakt, die oververhit zijn geraakt.</span><span class="sxs-lookup"><span data-stu-id="c5592-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="c5592-114">De correctie voor dit probleem is het vervangen van de onderdelen in de machine.</span><span class="sxs-lookup"><span data-stu-id="c5592-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="c5592-115">Wanneer u de typen diagnose configureert, kunt u meerdere records maken, die elk een verschillend type probleem vertegenwoordigen dat de machine kan hebben.</span><span class="sxs-lookup"><span data-stu-id="c5592-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="c5592-116">U kunt ook één algemeen type diagnose maken dat machinereparatie vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="c5592-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="c5592-117">Een type diagnose maken</span><span class="sxs-lookup"><span data-stu-id="c5592-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="c5592-118">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Typen diagnose**.</span><span class="sxs-lookup"><span data-stu-id="c5592-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="c5592-119">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="c5592-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c5592-120">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="c5592-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c5592-121">**Diagnose**: voer een unieke id of naam voor het type diagnose in.</span><span class="sxs-lookup"><span data-stu-id="c5592-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="c5592-122">**Beschrijving**: voer een gedetailleerde beschrijving van het type diagnose in.</span><span class="sxs-lookup"><span data-stu-id="c5592-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="c5592-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c5592-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5592-124">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c5592-124">Additional resources</span></span>

- [<span data-ttu-id="c5592-125">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="c5592-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="c5592-126">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="c5592-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="c5592-127">Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="c5592-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="c5592-128">Quarantainezones voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="c5592-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="c5592-129">Typen problemen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="c5592-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="c5592-130">Kwaliteitstoeslagen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="c5592-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="c5592-131">Bewerkingen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="c5592-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="c5592-132">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="c5592-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
