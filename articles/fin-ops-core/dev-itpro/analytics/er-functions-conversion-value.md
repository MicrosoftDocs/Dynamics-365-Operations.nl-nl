---
title: De ER-functie VALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUE.
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752575"
---
# <a name="value-er-function"></a><span data-ttu-id="182d8-103">De ER-functie VALUE</span><span class="sxs-lookup"><span data-stu-id="182d8-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="182d8-104">De functie `VALUE` retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="182d8-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="182d8-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="182d8-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="182d8-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="182d8-106">Arguments</span></span>

<span data-ttu-id="182d8-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="182d8-107">`text`: *String*</span></span>

<span data-ttu-id="182d8-108">Een tekenreekswaarde die moet worden geconverteerd naar een numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="182d8-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="182d8-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="182d8-109">Return values</span></span>

<span data-ttu-id="182d8-110">*Real-modus*</span><span class="sxs-lookup"><span data-stu-id="182d8-110">*Real*</span></span>

<span data-ttu-id="182d8-111">De resulterende numerieke waarde.</span><span class="sxs-lookup"><span data-stu-id="182d8-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="182d8-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="182d8-112">Usage notes</span></span>

<span data-ttu-id="182d8-113">De komma's en punttekens (.) worden beschouwd als decimale scheidingstekens en er wordt een koppelteken (-) vooraan gebruikt als minteken.</span><span class="sxs-lookup"><span data-stu-id="182d8-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="182d8-114">Tijdens runtime treedt een uitzondering op als andere niet-numerieke tekens worden aangetroffen in de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="182d8-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="182d8-115">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="182d8-115">Example 1</span></span>

<span data-ttu-id="182d8-116">`VALUE ("1 234,56")` leidt tot een uitzondering.</span><span class="sxs-lookup"><span data-stu-id="182d8-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="182d8-117">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="182d8-117">Example 2</span></span>

<span data-ttu-id="182d8-118">`VALUE ("1234,56")` retourneert **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="182d8-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="182d8-119">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="182d8-119">Additional resources</span></span>

[<span data-ttu-id="182d8-120">Type conversiefuncties</span><span class="sxs-lookup"><span data-stu-id="182d8-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]