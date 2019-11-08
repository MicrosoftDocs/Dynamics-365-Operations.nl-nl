---
title: Rapporteringsrelaties voor een positie wijzigen
description: Deze procedure toont hoe u de rapporteringsrelatie voor een werknemer wijzigt.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a1afd2c1cdc2ebaa303030d01b3bbe5fd2af44f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177258"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="5cddd-103">Rapporteringsrelaties voor een positie wijzigen</span><span class="sxs-lookup"><span data-stu-id="5cddd-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5cddd-104">Deze procedure toont hoe u de rapporteringsrelatie voor een werknemer wijzigt.</span><span class="sxs-lookup"><span data-stu-id="5cddd-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="5cddd-105">De rapporteringsrelatie kan worden gebruikt voor de routering van documenten door workflow.</span><span class="sxs-lookup"><span data-stu-id="5cddd-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="5cddd-106">De procedure toont ook hoe u de werknemer aan aanvullende hiërarchieën toewijst.</span><span class="sxs-lookup"><span data-stu-id="5cddd-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="5cddd-107">Een werknemer kan bijvoorbeeld deel uitmaken van een projectteam met een informele rapporteringsrelatie met een projectsupervisor.</span><span class="sxs-lookup"><span data-stu-id="5cddd-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="5cddd-108">U kunt extra rapporteringsrelaties bepalen op de functie om diverse project- of matrixscenario's te bevatten.</span><span class="sxs-lookup"><span data-stu-id="5cddd-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="5cddd-109">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="5cddd-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5cddd-110">Ga naar Human resources > Functies > Functies.</span><span class="sxs-lookup"><span data-stu-id="5cddd-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="5cddd-111">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="5cddd-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5cddd-112">Filter bijvoorbeeld op het veld Functie met de waarde '000091'.</span><span class="sxs-lookup"><span data-stu-id="5cddd-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="5cddd-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5cddd-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5cddd-114">Vouw de sectie Verantwoording aan positie uit.</span><span class="sxs-lookup"><span data-stu-id="5cddd-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="5cddd-115">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5cddd-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="5cddd-116">Typ of selecteer een waarde in het veld Rapporteert aan.</span><span class="sxs-lookup"><span data-stu-id="5cddd-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="5cddd-117">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="5cddd-117">Click Create.</span></span>
8. <span data-ttu-id="5cddd-118">Vouw de sectie Relaties uit of samen.</span><span class="sxs-lookup"><span data-stu-id="5cddd-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="5cddd-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5cddd-119">Click Add.</span></span>
10. <span data-ttu-id="5cddd-120">Schakel het selectievakje links van het raster in.</span><span class="sxs-lookup"><span data-stu-id="5cddd-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="5cddd-121">Typ of selecteer een waarde in het veld Hiërarchienaam.</span><span class="sxs-lookup"><span data-stu-id="5cddd-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="5cddd-122">Voorbeeld: Project</span><span class="sxs-lookup"><span data-stu-id="5cddd-122">Example: Project</span></span>  
12. <span data-ttu-id="5cddd-123">Typ of selecteer een waarde in het veld Verantwoording aan positie.</span><span class="sxs-lookup"><span data-stu-id="5cddd-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="5cddd-124">Voorbeeld: 000437</span><span class="sxs-lookup"><span data-stu-id="5cddd-124">Example:  000437</span></span>
13. <span data-ttu-id="5cddd-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5cddd-125">Click Save.</span></span>
