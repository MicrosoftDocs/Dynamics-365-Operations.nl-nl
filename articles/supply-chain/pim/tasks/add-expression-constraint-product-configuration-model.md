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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43d7f768069c5ef201a2823a9aa626b38220073
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425457"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="55575-103">Een expressiebeperking toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="55575-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55575-104">Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="55575-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="55575-105">Deze geeft aan hoe u kunt verplicht dat de hoekbescherming moet worden toegepast op een luidspreker als de gebruiker een grill in metaal heeft geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="55575-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="55575-106">De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="55575-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="55575-107">Maak een expressiebeperking</span><span class="sxs-lookup"><span data-stu-id="55575-107">Create an expression constraint</span></span>
1. <span data-ttu-id="55575-108">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="55575-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="55575-109">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="55575-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="55575-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="55575-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="55575-111">In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt.</span><span class="sxs-lookup"><span data-stu-id="55575-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="55575-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="55575-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="55575-113">Vouw de sectie Beperkingen uit.</span><span class="sxs-lookup"><span data-stu-id="55575-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="55575-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="55575-114">Click Add.</span></span>
7. <span data-ttu-id="55575-115">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="55575-115">Click Create.</span></span>
8. <span data-ttu-id="55575-116">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="55575-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="55575-117">Expressie invoeren</span><span class="sxs-lookup"><span data-stu-id="55575-117">Enter expression</span></span>
1. <span data-ttu-id="55575-118">Klik op Expressie bewerken.</span><span class="sxs-lookup"><span data-stu-id="55575-118">Click Edit expression.</span></span>
    * <span data-ttu-id="55575-119">Als u de gebruikersinterface in de taakregistratie in deze fase ontgrendelt, kunt u IntelliSense en de lijst van symbolen gebruiken om de expressie voor de beperking te maken.</span><span class="sxs-lookup"><span data-stu-id="55575-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="55575-120">Typ 'Implies[FrontGrill=="Metal", CornerProtection] ' in het veld ConstraintBody.</span><span class="sxs-lookup"><span data-stu-id="55575-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="55575-121">Deze expressielogica meldt: Als de grill van metaal is, moet de optie voor hoekbescherming worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="55575-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="55575-122">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="55575-122">Click Validate.</span></span>
    * <span data-ttu-id="55575-123">De validatiefunctie wordt uitgevoerd op de expressie voor de beperking en controleert op syntaxisfouten.</span><span class="sxs-lookup"><span data-stu-id="55575-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="55575-124">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="55575-124">Click Close.</span></span>
5. <span data-ttu-id="55575-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="55575-125">Click OK.</span></span>

