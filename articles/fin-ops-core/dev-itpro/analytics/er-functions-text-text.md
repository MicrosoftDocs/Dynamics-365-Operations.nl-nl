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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915551"
---
# <span data-ttu-id="14ebd-103"><a name="TEXT">De ER-functie TEXT</a></span><span class="sxs-lookup"><span data-stu-id="14ebd-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14ebd-104">De functie `TEXT` retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="14ebd-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ebd-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="14ebd-105">Syntax</span></span>

```
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="14ebd-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="14ebd-106">Arguments</span></span>

<span data-ttu-id="14ebd-107">`number`: *Geheel getal* of *Werkelijk*</span><span class="sxs-lookup"><span data-stu-id="14ebd-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="14ebd-108">Een numerieke waarde die moet worden geconverteerd naar een tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="14ebd-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="14ebd-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="14ebd-109">Return values</span></span>

<span data-ttu-id="14ebd-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="14ebd-110">*String*</span></span>

<span data-ttu-id="14ebd-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="14ebd-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="14ebd-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="14ebd-112">Usage notes</span></span>

<span data-ttu-id="14ebd-113">Voor waarden van het type *Werkelijk* wordt de tekenreeksconversie beperkt tot twee decimalen.</span><span class="sxs-lookup"><span data-stu-id="14ebd-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="14ebd-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="14ebd-114">Example</span></span>

<span data-ttu-id="14ebd-115">Als de landinstelling van het Microsoft Dynamics 365 Finance-exemplaar is gedefinieerd als **EN-US**, retourneert `TEXT (NOW ())` de datum van de huidige Finance-sessie, 17 december 2015, als de tekenreeks **12/17/2015 07:59:23 AM**.</span><span class="sxs-lookup"><span data-stu-id="14ebd-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="14ebd-116">`TEXT (1/3)` retourneert **0,33**.</span><span class="sxs-lookup"><span data-stu-id="14ebd-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14ebd-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="14ebd-117">Additional resources</span></span>

[<span data-ttu-id="14ebd-118">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="14ebd-118">Text functions</span></span>](er-functions-category-text.md)