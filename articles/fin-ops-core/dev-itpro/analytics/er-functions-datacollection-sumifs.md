---
title: De ER-functie SUMIFS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SUMIFS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 6820be1976e722f7b108b3e9303c8ed4d822ae9b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917598"
---
# <span data-ttu-id="55f72-103"><a name="SUMIFS">De ER-functie SUMIFS</a></span><span class="sxs-lookup"><span data-stu-id="55f72-103"><a name="SUMIFS">SUMIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55f72-104">De functie `SUMIFS` retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="55f72-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="55f72-105">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="55f72-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f72-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="55f72-106">Syntax</span></span>

```
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="55f72-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="55f72-107">Arguments</span></span>

<span data-ttu-id="55f72-108">`key name for summing`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="55f72-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="55f72-109">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel (Elektronische rapportage) waardoor de waarde van de binding moet worden gebruikt voor optellen.</span><span class="sxs-lookup"><span data-stu-id="55f72-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="55f72-110">De eigenschap **Sleutelnaam verzamelde gegevens** kan worden geconfigureerd voor een onderdeel **Numeriek** of **Tekenreeks** van een ER-indeling onder het onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="55f72-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="55f72-111">`condition 1 range`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="55f72-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="55f72-112">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="55f72-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="55f72-113">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="55f72-113">This argument is mandatory.</span></span>

<span data-ttu-id="55f72-114">De eigenschap **Sleutelnaam verzamelde gegevens** kan worden geconfigureerd voor een onderdeel **Volgorde** of **XML-element** van een ER-indeling onder het onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="55f72-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="55f72-115">`condition 1 value`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="55f72-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="55f72-116">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="55f72-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="55f72-117">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="55f72-117">This argument is mandatory.</span></span>

<span data-ttu-id="55f72-118">De eigenschap **Sleutelwaarde verzamelde gegevens** kan worden geconfigureerd voor een onderdeel **Volgorde** of **XML-element** van een ER-indeling onder het onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="55f72-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="55f72-119">`condition N range`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="55f72-119">`condition N range`: *String*</span></span>

<span data-ttu-id="55f72-120">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="55f72-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="55f72-121">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="55f72-121">These additional arguments are optional.</span></span>

<span data-ttu-id="55f72-122">De eigenschap **Sleutelnaam verzamelde gegevens** kan worden geconfigureerd voor een onderdeel **Volgorde** of **XML-element** van een ER-indeling onder het onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="55f72-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="55f72-123">`condition N value`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="55f72-123">`condition N value`: *String*</span></span>

<span data-ttu-id="55f72-124">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="55f72-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="55f72-125">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="55f72-125">These additional arguments are optional.</span></span>

<span data-ttu-id="55f72-126">De eigenschap **Sleutelwaarde verzamelde gegevens** kan worden geconfigureerd voor een onderdeel **Volgorde** of **XML-element** van een ER-indeling onder het onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="55f72-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="55f72-127">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="55f72-127">Return values</span></span>

<span data-ttu-id="55f72-128">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="55f72-128">*Real*</span></span>

<span data-ttu-id="55f72-129">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="55f72-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="55f72-130">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="55f72-130">Usage notes</span></span>

<span data-ttu-id="55f72-131">Deze functie retourneert een waarde van **0** (nul) als de optie **Uitvoerdetails verzamelen** van het onderdeel **Common\\File** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="55f72-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="55f72-132">In de `condition range`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="55f72-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="55f72-133">In de `condition value`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="55f72-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="55f72-134">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="55f72-134">Example</span></span>

<span data-ttu-id="55f72-135">Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.</span><span class="sxs-lookup"><span data-stu-id="55f72-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55f72-136">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="55f72-136">Additional resources</span></span>

[<span data-ttu-id="55f72-137">Functies voor gegevensverzameling</span><span class="sxs-lookup"><span data-stu-id="55f72-137">Data collection functions</span></span>](er-functions-category-data-collection.md)