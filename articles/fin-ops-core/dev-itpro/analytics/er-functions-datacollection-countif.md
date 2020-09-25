---
title: De ER-functie COUNTIF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COUNTIF.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc857a004d988a421c32722b1f69e86b7fefeb36
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743610"
---
# <a name="countif-er-function"></a><span data-ttu-id="fd1d3-103">De ER-functie COUNTIF</span><span class="sxs-lookup"><span data-stu-id="fd1d3-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd1d3-104">De functie `COUNTIF` retourneert een waarde van het type *Geheel getal* voor het aantal indelingselementen dat is verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="fd1d3-105">De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1d3-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="fd1d3-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="fd1d3-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="fd1d3-107">Arguments</span></span>

<span data-ttu-id="fd1d3-108">`condition range`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="fd1d3-108">`condition range`: *String*</span></span>

<span data-ttu-id="fd1d3-109">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel (Elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="fd1d3-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="fd1d3-110">`condition value`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="fd1d3-110">`condition value`: *String*</span></span>

<span data-ttu-id="fd1d3-111">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd1d3-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="fd1d3-112">Return values</span></span>

<span data-ttu-id="fd1d3-113">*Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="fd1d3-113">*Integer*</span></span>

<span data-ttu-id="fd1d3-114">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fd1d3-115">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="fd1d3-115">Usage notes</span></span>

<span data-ttu-id="fd1d3-116">De eigenschappen **Sleutelnaam verzamelde gegevens** en **Sleutelwaarde verzamelde gegevens** kunnen worden geconfigureerd voor het onderdeel **Volgorde** of **XML-element** van een ER-indeling onder onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="fd1d3-117">Deze functie retourneert een waarde van **0** (nul) als de optie **Uitvoerdetails verzamelen** van het onderdeel **Common\\File** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="fd1d3-118">In het argument `condition range` kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="fd1d3-119">In het argument `condition value` kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="fd1d3-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="fd1d3-120">Example</span></span>

<span data-ttu-id="fd1d3-121">Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.</span><span class="sxs-lookup"><span data-stu-id="fd1d3-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd1d3-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fd1d3-122">Additional resources</span></span>

[<span data-ttu-id="fd1d3-123">Functies voor gegevensverzameling</span><span class="sxs-lookup"><span data-stu-id="fd1d3-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
