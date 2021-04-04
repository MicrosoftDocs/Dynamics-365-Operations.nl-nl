---
title: De ER-functie IF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) IF.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565899"
---
# <a name="if-er-function"></a><span data-ttu-id="2c1d6-103">De ER-functie IF</span><span class="sxs-lookup"><span data-stu-id="2c1d6-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c1d6-104">De functie `IF` retourneert de eerste opgegeven waarde als aan de opgegeven voorwaarde is voldaan.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="2c1d6-105">Anders wordt de tweede opgegeven waarde als resultaat gegeven.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="2c1d6-106">De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1d6-107">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="2c1d6-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="2c1d6-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="2c1d6-108">Arguments</span></span>

<span data-ttu-id="2c1d6-109">`condition`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="2c1d6-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="2c1d6-110">Een geldige voorwaardelijke expressie die moet worden getest.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="2c1d6-111">`first value`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="2c1d6-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="2c1d6-112">Het resultaat dat wordt geretourneerd als aan de voorwaarde wordt voldaan.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="2c1d6-113">`second value`: *Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="2c1d6-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="2c1d6-114">Het resultaat dat wordt geretourneerd als niet aan de voorwaarde wordt voldaan.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c1d6-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="2c1d6-115">Return values</span></span>

<span data-ttu-id="2c1d6-116">*Een van de ondersteunde gegevenstypen*</span><span class="sxs-lookup"><span data-stu-id="2c1d6-116">*Any of the supported data types*</span></span>

<span data-ttu-id="2c1d6-117">De resulterende waarde van een van de ondersteunde gegevenstypen.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2c1d6-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="2c1d6-118">Usage notes</span></span>

<span data-ttu-id="2c1d6-119">De argumenten `first value` en `second value` moeten worden opgegeven met hetzelfde gegevenstype.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="2c1d6-120">Er wordt een uitzondering gegenereerd tijdens het ontwerpen als de gegevenstypen van de geconfigureerde waarden niet overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="2c1d6-121">Als de eerste en tweede waarden van het gegevenstype *Container (record)* of *Recordlijst* zijn, bevat het resultaat alleen de velden die in beide waarden bestaan.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="2c1d6-122">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2c1d6-122">Example</span></span>

<span data-ttu-id="2c1d6-123">`IF (1=2, "condition is met", "condition is not met")` retourneert de tekenreeks **"condition is not met"**.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c1d6-124">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2c1d6-124">Additional resources</span></span>

[<span data-ttu-id="2c1d6-125">Logische functies</span><span class="sxs-lookup"><span data-stu-id="2c1d6-125">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]