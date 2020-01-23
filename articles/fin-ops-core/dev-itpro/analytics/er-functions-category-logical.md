---
title: Lijst met ER-functies in de logische categorie
description: Dit onderwerp biedt informatie over de logische functies die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916632"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="0c533-103">Lijst met ER-functies in de logische categorie</span><span class="sxs-lookup"><span data-stu-id="0c533-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c533-104">Logische ER-functies kunnen worden gebruikt om met logische waarden te werken om meer dan één vergelijking in één expressie uit te voeren of meerdere voorwaarden te testen.</span><span class="sxs-lookup"><span data-stu-id="0c533-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="0c533-105">In dit onderwerp vindt u een overzicht van deze functies.</span><span class="sxs-lookup"><span data-stu-id="0c533-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="0c533-106">Lijst met ondersteunde functies</span><span class="sxs-lookup"><span data-stu-id="0c533-106">List of supported functions</span></span>

| <span data-ttu-id="0c533-107">Functie</span><span class="sxs-lookup"><span data-stu-id="0c533-107">Function</span></span> | <span data-ttu-id="0c533-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0c533-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0c533-109">En</span><span class="sxs-lookup"><span data-stu-id="0c533-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="0c533-110">Deze functie retourneert de *Booleaanse* waarde **TRUE** als alle opgegeven voorwaarden waar zijn.</span><span class="sxs-lookup"><span data-stu-id="0c533-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="0c533-111">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0c533-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0c533-112">Doos</span><span class="sxs-lookup"><span data-stu-id="0c533-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="0c533-113">Deze functie evalueert de waarde van de opgegeven expressie ten opzichte van de opgegeven alternatieve opties en retourneert het resultaat van de eerste optie die gelijk is aan de waarde van de opgegeven expressie.</span><span class="sxs-lookup"><span data-stu-id="0c533-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="0c533-114">Anders wordt een optioneel standaardresultaat geretourneerd, als een standaardresultaat is opgegeven als het laatste argument van de aangeroepen functie die niet wordt voorafgegaan door een optie.</span><span class="sxs-lookup"><span data-stu-id="0c533-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="0c533-115">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="0c533-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="0c533-116">Als</span><span class="sxs-lookup"><span data-stu-id="0c533-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="0c533-117">Deze functie retourneert de eerste opgegeven waarde als aan de opgegeven voorwaarde is voldaan.</span><span class="sxs-lookup"><span data-stu-id="0c533-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="0c533-118">Anders wordt de tweede opgegeven waarde als resultaat gegeven.</span><span class="sxs-lookup"><span data-stu-id="0c533-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="0c533-119">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="0c533-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="0c533-120">Niet</span><span class="sxs-lookup"><span data-stu-id="0c533-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="0c533-121">Deze functie retourneert de omgekeerde logische waarde van de opgegeven voorwaarde als een *Booleaanse* waarde.</span><span class="sxs-lookup"><span data-stu-id="0c533-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="0c533-122">Or</span><span class="sxs-lookup"><span data-stu-id="0c533-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="0c533-123">Deze functie retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn.</span><span class="sxs-lookup"><span data-stu-id="0c533-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="0c533-124">De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is.</span><span class="sxs-lookup"><span data-stu-id="0c533-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="0c533-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="0c533-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="0c533-126">Deze functie bepaalt of de opgegeven invoer overeenkomt met een waarde van een opgegeven item in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="0c533-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0c533-127">Het resultaat is de *Booleaanse waarde* **TRUE** als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="0c533-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0c533-128">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0c533-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="0c533-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0c533-129">Additional resources</span></span>

[<span data-ttu-id="0c533-130">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="0c533-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="0c533-131">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="0c533-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="0c533-132">Formuletaal in Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="0c533-132">Electronic reporting formula language</span></span>](er-formula-language.md)
