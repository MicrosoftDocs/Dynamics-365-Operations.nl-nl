---
title: De ER-functie COUNTIFS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COUNTIFS.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 554750b2dae5ec1f0fcf6fdbdf439b4dbe4fa615
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681129"
---
# <a name="countifs-er-function"></a><span data-ttu-id="a82cd-103">De ER-functie COUNTIFS</span><span class="sxs-lookup"><span data-stu-id="a82cd-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a82cd-104">De functie `COUNTIFS` retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en dat voldoet aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="a82cd-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a82cd-105">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="a82cd-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82cd-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a82cd-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="a82cd-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a82cd-107">Arguments</span></span>

<span data-ttu-id="a82cd-108">`condition 1 range`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a82cd-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="a82cd-109">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel (Elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="a82cd-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="a82cd-110">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="a82cd-110">This argument is mandatory.</span></span>

<span data-ttu-id="a82cd-111">`condition 1 value`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a82cd-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="a82cd-112">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="a82cd-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="a82cd-113">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="a82cd-113">This argument is mandatory.</span></span>

<span data-ttu-id="a82cd-114">`condition N range`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a82cd-114">`condition N range`: *String*</span></span>

<span data-ttu-id="a82cd-115">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="a82cd-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="a82cd-116">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="a82cd-116">These additional arguments are optional.</span></span>

<span data-ttu-id="a82cd-117">`condition N value`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="a82cd-117">`condition N value`: *String*</span></span>

<span data-ttu-id="a82cd-118">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="a82cd-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="a82cd-119">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="a82cd-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a82cd-120">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a82cd-120">Return values</span></span>

<span data-ttu-id="a82cd-121">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="a82cd-121">*Integer*</span></span>

<span data-ttu-id="a82cd-122">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="a82cd-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a82cd-123">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="a82cd-123">Usage notes</span></span>

<span data-ttu-id="a82cd-124">De eigenschappen **Sleutelnaam verzamelde gegevens** en **Sleutelwaarde verzamelde gegevens** kunnen worden geconfigureerd voor het onderdeel **Volgorde** of **XML-element** van een ER-indeling onder onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="a82cd-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="a82cd-125">Deze functie retourneert een waarde van **0** (nul) als de optie **Uitvoerdetails verzamelen** van het onderdeel **Common\\File** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="a82cd-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="a82cd-126">In `condition range`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="a82cd-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="a82cd-127">In `condition value`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="a82cd-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="a82cd-128">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a82cd-128">Example</span></span>

<span data-ttu-id="a82cd-129">Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.</span><span class="sxs-lookup"><span data-stu-id="a82cd-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a82cd-130">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a82cd-130">Additional resources</span></span>

[<span data-ttu-id="a82cd-131">Functies voor gegevensverzameling</span><span class="sxs-lookup"><span data-stu-id="a82cd-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
