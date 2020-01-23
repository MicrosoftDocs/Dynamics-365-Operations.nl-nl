---
title: De ER-functie SUMIF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SUMIF.
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
ms.openlocfilehash: 579b14c713bc5f9831c5e012d16bb3b6f97b1035
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916425"
---
# <span data-ttu-id="48246-103"><a name="SUMIF">De ER-functie SUMIF</a></span><span class="sxs-lookup"><span data-stu-id="48246-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48246-104">De functie `SUMIF` retourneert een waarde van het type *Werkelijk* voor de som van de waarden die zijn geretourneerd door bindingen van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaand document te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="48246-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="48246-105">De voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="48246-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="48246-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="48246-106">Syntax</span></span>

```
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="48246-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="48246-107">Arguments</span></span>

<span data-ttu-id="48246-108">`key name for summing`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="48246-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="48246-109">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel (Elektronische rapportage) waardoor de waarde van de binding moet worden gebruikt voor optellen.</span><span class="sxs-lookup"><span data-stu-id="48246-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="48246-110">De eigenschap **Sleutelwaarde verzamelde gegevens** kan worden geconfigureerd voor een onderdeel **Volgorde** of **XML-element** van een ER-indeling onder het onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="48246-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="48246-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="48246-111">Return values</span></span>

<span data-ttu-id="48246-112">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="48246-112">*Real*</span></span>

<span data-ttu-id="48246-113">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="48246-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="48246-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="48246-114">Usage notes</span></span>

<span data-ttu-id="48246-115">Deze functie retourneert een waarde van **0** (nul) als de optie **Uitvoerdetails verzamelen** van het onderdeel **Common\\File** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="48246-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="48246-116">In het argument `condition range` kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="48246-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="48246-117">In het argument `condition value` kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="48246-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="48246-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="48246-118">Example</span></span>

<span data-ttu-id="48246-119">Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.</span><span class="sxs-lookup"><span data-stu-id="48246-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48246-120">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="48246-120">Additional resources</span></span>

[<span data-ttu-id="48246-121">Functies voor gegevensverzameling</span><span class="sxs-lookup"><span data-stu-id="48246-121">Data collection functions</span></span>](er-functions-category-data-collection.md)
