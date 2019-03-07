---
title: Een expressiebeperking toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "360573"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="cf184-103">Een expressiebeperking toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="cf184-103">Add an expression constraint to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf184-104">Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="cf184-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="cf184-105">Deze geeft aan hoe u kunt verplicht dat de hoekbescherming moet worden toegepast op een luidspreker als de gebruiker een grill in metaal heeft geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="cf184-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="cf184-106">De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="cf184-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="cf184-107">Maak een expressiebeperking</span><span class="sxs-lookup"><span data-stu-id="cf184-107">Create an expression constraint</span></span>
1. <span data-ttu-id="cf184-108">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="cf184-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="cf184-109">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="cf184-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="cf184-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cf184-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cf184-111">In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cf184-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="cf184-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cf184-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cf184-113">Vouw de sectie Beperkingen uit.</span><span class="sxs-lookup"><span data-stu-id="cf184-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="cf184-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="cf184-114">Click Add.</span></span>
7. <span data-ttu-id="cf184-115">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="cf184-115">Click Create.</span></span>
8. <span data-ttu-id="cf184-116">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="cf184-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="cf184-117">Expressie invoeren</span><span class="sxs-lookup"><span data-stu-id="cf184-117">Enter expression</span></span>
1. <span data-ttu-id="cf184-118">Klik op Expressie bewerken.</span><span class="sxs-lookup"><span data-stu-id="cf184-118">Click Edit expression.</span></span>
    * <span data-ttu-id="cf184-119">Als u de gebruikersinterface in de taakregistratie in deze fase ontgrendelt, kunt u IntelliSense en de lijst van symbolen gebruiken om de expressie voor de beperking te maken.</span><span class="sxs-lookup"><span data-stu-id="cf184-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="cf184-120">Typ 'Implies[FrontGrill=="Metal", CornerProtection] ' in het veld ConstraintBody.</span><span class="sxs-lookup"><span data-stu-id="cf184-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="cf184-121">Deze expressielogica meldt: Als de grill van metaal is, moet de optie voor hoekbescherming worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="cf184-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="cf184-122">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="cf184-122">Click Validate.</span></span>
    * <span data-ttu-id="cf184-123">De validatiefunctie wordt uitgevoerd op de expressie voor de beperking en controleert op syntaxisfouten.</span><span class="sxs-lookup"><span data-stu-id="cf184-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="cf184-124">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="cf184-124">Click Close.</span></span>
5. <span data-ttu-id="cf184-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cf184-125">Click OK.</span></span>

