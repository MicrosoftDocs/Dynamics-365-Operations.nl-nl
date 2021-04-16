---
title: De ER-functie MID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) MID.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746262"
---
# <a name="mid-er-function"></a><span data-ttu-id="71131-103">De ER-functie MID</span><span class="sxs-lookup"><span data-stu-id="71131-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71131-104">De functie `MID` retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf de opgegeven positie van de opgegeven tekenreeks bevat.</span><span class="sxs-lookup"><span data-stu-id="71131-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="71131-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="71131-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="71131-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="71131-106">Arguments</span></span>

<span data-ttu-id="71131-107">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="71131-107">`text`: *String*</span></span>

<span data-ttu-id="71131-108">Een *tekenreekswaarde* die de tekst aangeeft waaruit de tekens moeten worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="71131-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="71131-109">`starting position`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="71131-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="71131-110">Een *geheel getal* dat de positie aangeeft van het eerste teken dat moet worden geretourneerd uit de opgegeven tekst.</span><span class="sxs-lookup"><span data-stu-id="71131-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="71131-111">`number of characters`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="71131-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="71131-112">Een *geheel getal* waarmee wordt aangegeven hoeveel tekens moeten worden geretourneerd, vanaf de opgegeven beginpositie.</span><span class="sxs-lookup"><span data-stu-id="71131-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="71131-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="71131-113">Return values</span></span>

<span data-ttu-id="71131-114">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="71131-114">*String*</span></span>

<span data-ttu-id="71131-115">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="71131-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71131-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="71131-116">Usage notes</span></span>

<span data-ttu-id="71131-117">Als de waarde van het argument `starting position` kleiner is dan 0 (nul), worden de geretourneerde tekens geteld vanaf de eerste positie in de opgegeven tekenreeks.</span><span class="sxs-lookup"><span data-stu-id="71131-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="71131-118">Als de waarde van het argument `starting position` groter is dan de lengte van de opgegeven tekenreeks, wordt een lege tekenreeks geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="71131-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="71131-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="71131-119">Example</span></span>

<span data-ttu-id="71131-120">`MID ("Sample", 2, 3)` retourneert **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="71131-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71131-121">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="71131-121">Additional resources</span></span>

[<span data-ttu-id="71131-122">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="71131-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]