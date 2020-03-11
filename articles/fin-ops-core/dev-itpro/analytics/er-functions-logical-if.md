---
title: De ER-functie IF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) IF.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 198210f15e75de761dbb03e5087ba7c77a95721a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041740"
---
# <span data-ttu-id="af0df-103"><a name="IF">De ER-functie IF</a></span><span class="sxs-lookup"><span data-stu-id="af0df-103"><a name="IF">IF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af0df-104">De functie `IF` retourneert de eerste opgegeven waarde als aan de opgegeven voorwaarde is voldaan.</span><span class="sxs-lookup"><span data-stu-id="af0df-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="af0df-105">Anders wordt de tweede opgegeven waarde als resultaat gegeven.</span><span class="sxs-lookup"><span data-stu-id="af0df-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="af0df-106">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="af0df-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="af0df-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="af0df-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="af0df-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="af0df-108">Arguments</span></span>

<span data-ttu-id="af0df-109">`condition`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="af0df-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="af0df-110">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="af0df-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="af0df-111">`first value`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="af0df-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="af0df-112">Het resultaat dat wordt geretourneerd als aan de voorwaarde wordt voldaan.</span><span class="sxs-lookup"><span data-stu-id="af0df-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="af0df-113">`second value`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="af0df-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="af0df-114">Het resultaat dat wordt geretourneerd als niet aan de voorwaarde wordt voldaan.</span><span class="sxs-lookup"><span data-stu-id="af0df-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="af0df-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="af0df-115">Return values</span></span>

<span data-ttu-id="af0df-116">*Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="af0df-116">*Any of the supported data types*</span></span>

<span data-ttu-id="af0df-117">De resulterende waarde van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="af0df-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="af0df-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="af0df-118">Usage notes</span></span>

<span data-ttu-id="af0df-119">De argumenten `first value` en `second value` moeten worden opgegeven met hetzelfde gegevenstype.</span><span class="sxs-lookup"><span data-stu-id="af0df-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="af0df-120">Er wordt een uitzondering gegenereerd tijdens het ontwerpen als de gegevenstypen van de geconfigureerde waarden niet overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="af0df-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="af0df-121">Als de eerste en tweede waarden van het gegevenstype *Container (record)* of *Recordlijst* zijn, bevat het resultaat alleen de velden die in beide waarden bestaan.</span><span class="sxs-lookup"><span data-stu-id="af0df-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="af0df-122">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="af0df-122">Example</span></span>

<span data-ttu-id="af0df-123">`IF (1=2, "condition is met", "condition is not met")` retourneert de tekenreeks **"condition is not met"**.</span><span class="sxs-lookup"><span data-stu-id="af0df-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af0df-124">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="af0df-124">Additional resources</span></span>

[<span data-ttu-id="af0df-125">Logische functies</span><span class="sxs-lookup"><span data-stu-id="af0df-125">Logical functions</span></span>](er-functions-category-logical.md)
