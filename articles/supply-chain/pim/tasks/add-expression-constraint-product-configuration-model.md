---
title: Een expressiebeperking toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920876"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="0ba7b-103">Een expressiebeperking toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="0ba7b-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ba7b-104">Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="0ba7b-105">Deze geeft aan hoe u kunt verplicht dat de hoekbescherming moet worden toegepast op een luidspreker als de gebruiker een grill in metaal heeft geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="0ba7b-106">De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="0ba7b-107">Maak een expressiebeperking</span><span class="sxs-lookup"><span data-stu-id="0ba7b-107">Create an expression constraint</span></span>

1. <span data-ttu-id="0ba7b-108">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="0ba7b-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0ba7b-110">In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="0ba7b-111">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="0ba7b-112">Vouw de sectie **Beperkingen** uit.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="0ba7b-113">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-113">Select **Add**.</span></span>
7. <span data-ttu-id="0ba7b-114">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-114">Select **Create**.</span></span>
8. <span data-ttu-id="0ba7b-115">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="0ba7b-116">Expressie invoeren</span><span class="sxs-lookup"><span data-stu-id="0ba7b-116">Enter expression</span></span>

1. <span data-ttu-id="0ba7b-117">Selecteer **Expressie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="0ba7b-118">Als u de gebruikersinterface in de taakregistratie in deze fase ontgrendelt, kunt u IntelliSense en de lijst van symbolen gebruiken om de expressie voor de beperking te maken.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="0ba7b-119">Typ in het veld **ConstraintBody** de tekst 'Implies[FrontGrill=="Metal", CornerProtection] '.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="0ba7b-120">Deze expressielogica meldt: Als de grill van metaal is, moet de optie voor hoekbescherming worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="0ba7b-121">Selecteer **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-121">Select **Validate**.</span></span>
    * <span data-ttu-id="0ba7b-122">De validatiefunctie wordt uitgevoerd op de expressie voor de beperking en controleert op syntaxisfouten.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="0ba7b-123">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-123">Select **Close**.</span></span>
5. <span data-ttu-id="0ba7b-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ba7b-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]