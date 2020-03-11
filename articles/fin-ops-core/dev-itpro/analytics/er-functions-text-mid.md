---
title: De ER-functie MID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) MID.
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
ms.openlocfilehash: 6fbaf5952222d90a855956fb93713e0f9ef81305
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041022"
---
# <span data-ttu-id="8013d-103"><a name="MID">De ER-functie MID</a></span><span class="sxs-lookup"><span data-stu-id="8013d-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8013d-104">De functie `MID` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf de opgegeven positie van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="8013d-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="8013d-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="8013d-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="8013d-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="8013d-106">Arguments</span></span>

<span data-ttu-id="8013d-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8013d-107">`text`: *String*</span></span>

<span data-ttu-id="8013d-108">Een *tekenreekswaarde* die de tekst aangeeft waaruit de tekens moeten worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8013d-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="8013d-109">`starting position`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="8013d-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="8013d-110">Een *geheel getal* dat de positie aangeeft van het eerste teken dat moet worden geretourneerd uit de opgegeven tekst.</span><span class="sxs-lookup"><span data-stu-id="8013d-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="8013d-111">`number of characters`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="8013d-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="8013d-112">Een *geheel getal* waarmee wordt aangegeven hoeveel tekens moeten worden geretourneerd, vanaf de opgegeven beginpositie.</span><span class="sxs-lookup"><span data-stu-id="8013d-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="8013d-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="8013d-113">Return values</span></span>

<span data-ttu-id="8013d-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8013d-114">*String*</span></span>

<span data-ttu-id="8013d-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="8013d-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8013d-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="8013d-116">Usage notes</span></span>

<span data-ttu-id="8013d-117">Als de waarde van het argument `starting position` kleiner is dan 0 (nul), worden de geretourneerde tekens geteld vanaf de eerste positie in de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="8013d-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="8013d-118">Als de waarde van het argument `starting position` groter is dan de lengte van de opgegeven tekenreeks, wordt een lege tekenreeks geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8013d-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="8013d-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="8013d-119">Example</span></span>

<span data-ttu-id="8013d-120">`MID ("Sample", 2, 3)` retourneert **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="8013d-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8013d-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8013d-121">Additional resources</span></span>

[<span data-ttu-id="8013d-122">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="8013d-122">Text functions</span></span>](er-functions-category-text.md)
