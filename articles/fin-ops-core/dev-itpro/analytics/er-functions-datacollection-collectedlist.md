---
title: De ER-functie COLLECTEDLIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) COLLECTEDLIST.
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 494fb0fa1000abe8d0234d512e41926103c56f05
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755319"
---
# <a name="collectedlist-er-function"></a><span data-ttu-id="6e537-103">De ER-functie COLLECTEDLIST</span><span class="sxs-lookup"><span data-stu-id="6e537-103">COLLECTEDLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e537-104">De functie `COLLECTEDLIST` retourneert een waarde van het type *Recordlijst* die de lijst met waarden bevat die zijn geretourneerd door de eigenschap **Sleutelwaarde verzamelde gegevens** van indelingselementen, zijn verzameld toen de indelingselementen werden gebruikt om een uitgaande documenten te genereren tijdens het uitvoeren van de indeling en waarmee wordt voldaan aan de opgegeven voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="6e537-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="6e537-105">Elke voorwaarde bestaat uit een sleutelbereik en een sleutelwaarde.</span><span class="sxs-lookup"><span data-stu-id="6e537-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e537-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="6e537-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="6e537-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="6e537-107">Arguments</span></span>

<span data-ttu-id="6e537-108">`condition 1 range`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="6e537-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="6e537-109">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel (Elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="6e537-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="6e537-110">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="6e537-110">This argument is mandatory.</span></span>

<span data-ttu-id="6e537-111">`condition 1 value`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="6e537-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="6e537-112">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="6e537-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="6e537-113">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="6e537-113">This argument is mandatory.</span></span>

<span data-ttu-id="6e537-114">`condition N range`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="6e537-114">`condition N range`: *String*</span></span>

<span data-ttu-id="6e537-115">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelnaam verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="6e537-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="6e537-116">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="6e537-116">These additional arguments are optional.</span></span>

<span data-ttu-id="6e537-117">`condition N value`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="6e537-117">`condition N value`: *String*</span></span>

<span data-ttu-id="6e537-118">Een waarde die wordt geretourneerd door de expressie die is geconfigureerd in de eigenschap **Sleutelwaarde verzamelde gegevens** van een ER-indelingsonderdeel.</span><span class="sxs-lookup"><span data-stu-id="6e537-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="6e537-119">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="6e537-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="6e537-120">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="6e537-120">Return values</span></span>

<span data-ttu-id="6e537-121">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="6e537-121">*Record list*</span></span>

<span data-ttu-id="6e537-122">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="6e537-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6e537-123">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="6e537-123">Usage notes</span></span>

<span data-ttu-id="6e537-124">De eigenschappen **Sleutelnaam verzamelde gegevens** en **Sleutelwaarde verzamelde gegevens** kunnen worden geconfigureerd voor het onderdeel **Volgorde** of **XML-element** van een ER-indeling onder onderdeel **Common\\File** waarvoor de optie **Uitvoerdetails verzamelen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6e537-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="6e537-125">Deze functie retourneert een lege lijst als de optie **Uitvoerdetails verzamelen** van het huidige onderdeel **Common\\File** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6e537-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="6e537-126">In `condition range`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="6e537-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="6e537-127">In `condition value`-argumenten kan het jokerteken **"\*"** worden gebruikt om voor meerdere tekens te staan.</span><span class="sxs-lookup"><span data-stu-id="6e537-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="6e537-128">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="6e537-128">Example</span></span>

<span data-ttu-id="6e537-129">Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding [ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen](tasks/er-format-counting-summing-1.md), die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**.</span><span class="sxs-lookup"><span data-stu-id="6e537-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e537-130">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6e537-130">Additional resources</span></span>

[<span data-ttu-id="6e537-131">Functies voor gegevensverzameling</span><span class="sxs-lookup"><span data-stu-id="6e537-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]