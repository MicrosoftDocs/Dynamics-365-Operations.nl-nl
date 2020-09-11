---
title: Lijst met ER-functies in de logische categorie
description: Dit onderwerp biedt informatie over de logische functies die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705090"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="f5ff9-103">Lijst met ER-functies in de logische categorie</span><span class="sxs-lookup"><span data-stu-id="f5ff9-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5ff9-104">Logische ER-functies kunnen worden gebruikt om met logische waarden te werken om meer dan één vergelijking in één expressie uit te voeren of meerdere voorwaarden te testen.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="f5ff9-105">In dit onderwerp vindt u een overzicht van deze functies.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="f5ff9-106">Lijst met ondersteunde functies</span><span class="sxs-lookup"><span data-stu-id="f5ff9-106">List of supported functions</span></span>

| <span data-ttu-id="f5ff9-107">Functie</span><span class="sxs-lookup"><span data-stu-id="f5ff9-107">Function</span></span> | <span data-ttu-id="f5ff9-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f5ff9-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="f5ff9-109">En</span><span class="sxs-lookup"><span data-stu-id="f5ff9-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="f5ff9-110">Deze functie retourneert de *Booleaanse* waarde **TRUE** als alle opgegeven voorwaarden waar zijn.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="f5ff9-111">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="f5ff9-112">Doos</span><span class="sxs-lookup"><span data-stu-id="f5ff9-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="f5ff9-113">Deze functie evalueert de waarde van de opgegeven expressie ten opzichte van de opgegeven alternatieve opties en retourneert het resultaat van de eerste optie die gelijk is aan de waarde van de opgegeven expressie.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="f5ff9-114">Anders wordt een optioneel standaardresultaat geretourneerd, als een standaardresultaat is opgegeven als het laatste argument van de aangeroepen functie die niet wordt voorafgegaan door een optie.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="f5ff9-115">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="f5ff9-116">Als</span><span class="sxs-lookup"><span data-stu-id="f5ff9-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="f5ff9-117">Deze functie retourneert de eerste opgegeven waarde als aan de opgegeven voorwaarde is voldaan.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="f5ff9-118">Anders wordt de tweede opgegeven waarde als resultaat gegeven.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="f5ff9-119">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="f5ff9-120">Niet</span><span class="sxs-lookup"><span data-stu-id="f5ff9-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="f5ff9-121">Deze functie retourneert de omgekeerde logische waarde van de opgegeven voorwaarde als een *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="f5ff9-122">Or</span><span class="sxs-lookup"><span data-stu-id="f5ff9-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="f5ff9-123">Deze functie retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="f5ff9-124">De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="f5ff9-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="f5ff9-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="f5ff9-126">Deze functie bepaalt of de opgegeven invoer overeenkomt met een waarde van een opgegeven item in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="f5ff9-127">Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="f5ff9-128">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="f5ff9-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="f5ff9-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="f5ff9-130">Deze functie bepaalt of de opgegeven invoer van het type *Int64* of *Integer* overeenkomt met een waarde van een opgegeven item in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="f5ff9-131">Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="f5ff9-132">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f5ff9-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="f5ff9-133">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f5ff9-133">Additional resources</span></span>

[<span data-ttu-id="f5ff9-134">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="f5ff9-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="f5ff9-135">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="f5ff9-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="f5ff9-136">Formuletaal in Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="f5ff9-136">Electronic reporting formula language</span></span>](er-formula-language.md)
