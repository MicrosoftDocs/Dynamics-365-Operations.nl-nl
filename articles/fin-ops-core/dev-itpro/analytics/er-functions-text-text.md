---
title: De ER-functie TEXT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TEXT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682890"
---
# <a name="text-er-function"></a><span data-ttu-id="43b7d-103">De ER-functie TEXT</span><span class="sxs-lookup"><span data-stu-id="43b7d-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43b7d-104">De functie `TEXT` retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="43b7d-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b7d-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="43b7d-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="43b7d-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="43b7d-106">Arguments</span></span>

<span data-ttu-id="43b7d-107">`number`: *Geheel getal* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="43b7d-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="43b7d-108">Een numerieke waarde die moet worden geconverteerd naar een tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="43b7d-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="43b7d-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="43b7d-109">Return values</span></span>

<span data-ttu-id="43b7d-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="43b7d-110">*String*</span></span>

<span data-ttu-id="43b7d-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="43b7d-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="43b7d-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="43b7d-112">Usage notes</span></span>

<span data-ttu-id="43b7d-113">Voor waarden van het type *Werkelijk* wordt de tekenreeksconversie beperkt tot twee decimalen.</span><span class="sxs-lookup"><span data-stu-id="43b7d-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="43b7d-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="43b7d-114">Example</span></span>

<span data-ttu-id="43b7d-115">Als de landinstelling van het Microsoft Dynamics 365 Finance-exemplaar is gedefinieerd als **EN-US**, retourneert `TEXT (NOW ())` de datum van de huidige Finance-sessie, 17 december 2015, als de tekenreeks **12/17/2015 07:59:23 AM**.</span><span class="sxs-lookup"><span data-stu-id="43b7d-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="43b7d-116">`TEXT (1/3)` retourneert **0,33**.</span><span class="sxs-lookup"><span data-stu-id="43b7d-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43b7d-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="43b7d-117">Additional resources</span></span>

[<span data-ttu-id="43b7d-118">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="43b7d-118">Text functions</span></span>](er-functions-category-text.md)
