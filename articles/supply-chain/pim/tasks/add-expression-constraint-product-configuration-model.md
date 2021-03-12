---
title: Een expressiebeperking toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 411e20bd8631b70df981c5785f502693d5ba3705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987124"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="ac09a-103">Een expressiebeperking toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="ac09a-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac09a-104">Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="ac09a-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="ac09a-105">Deze geeft aan hoe u kunt verplicht dat de hoekbescherming moet worden toegepast op een luidspreker als de gebruiker een grill in metaal heeft geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ac09a-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="ac09a-106">De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="ac09a-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="ac09a-107">Maak een expressiebeperking</span><span class="sxs-lookup"><span data-stu-id="ac09a-107">Create an expression constraint</span></span>
1. <span data-ttu-id="ac09a-108">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="ac09a-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ac09a-109">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="ac09a-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="ac09a-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ac09a-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ac09a-111">In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ac09a-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="ac09a-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ac09a-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ac09a-113">Vouw de sectie Beperkingen uit.</span><span class="sxs-lookup"><span data-stu-id="ac09a-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="ac09a-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ac09a-114">Click Add.</span></span>
7. <span data-ttu-id="ac09a-115">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="ac09a-115">Click Create.</span></span>
8. <span data-ttu-id="ac09a-116">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="ac09a-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="ac09a-117">Expressie invoeren</span><span class="sxs-lookup"><span data-stu-id="ac09a-117">Enter expression</span></span>
1. <span data-ttu-id="ac09a-118">Klik op Expressie bewerken.</span><span class="sxs-lookup"><span data-stu-id="ac09a-118">Click Edit expression.</span></span>
    * <span data-ttu-id="ac09a-119">Als u de gebruikersinterface in de taakregistratie in deze fase ontgrendelt, kunt u IntelliSense en de lijst van symbolen gebruiken om de expressie voor de beperking te maken.</span><span class="sxs-lookup"><span data-stu-id="ac09a-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="ac09a-120">Typ 'Implies[FrontGrill=="Metal", CornerProtection] ' in het veld ConstraintBody.</span><span class="sxs-lookup"><span data-stu-id="ac09a-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="ac09a-121">Deze expressielogica meldt: Als de grill van metaal is, moet de optie voor hoekbescherming worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ac09a-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="ac09a-122">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="ac09a-122">Click Validate.</span></span>
    * <span data-ttu-id="ac09a-123">De validatiefunctie wordt uitgevoerd op de expressie voor de beperking en controleert op syntaxisfouten.</span><span class="sxs-lookup"><span data-stu-id="ac09a-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="ac09a-124">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="ac09a-124">Click Close.</span></span>
5. <span data-ttu-id="ac09a-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ac09a-125">Click OK.</span></span>

