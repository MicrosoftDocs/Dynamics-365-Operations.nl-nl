---
title: De ER-functie ISVALIDCHARACTERISO7064
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ISVALIDCHARACTERISO7064.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041395"
---
# <span data-ttu-id="8d60f-103"><a name="ISVALIDCHARACTERISO7064">De ER-functie ISVALIDCHARACTERISO7064</a></span><span class="sxs-lookup"><span data-stu-id="8d60f-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d60f-104">De functie `ISVALIDCHARACTERISO7064` retourneert de *Booleaanse* waarde **TRUE** als de opgegeven tekenreeks staat voor een geldig internationaal bankrekeningnummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="8d60f-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="8d60f-105">Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8d60f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d60f-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="8d60f-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="8d60f-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="8d60f-107">Arguments</span></span>

<span data-ttu-id="8d60f-108">`text`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8d60f-108">`text`: *String*</span></span>

<span data-ttu-id="8d60f-109">Een tekstwaarde die een IBAN vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="8d60f-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d60f-110">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="8d60f-110">Return values</span></span>

<span data-ttu-id="8d60f-111">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="8d60f-111">*String*</span></span>

<span data-ttu-id="8d60f-112">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="8d60f-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8d60f-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="8d60f-113">Example</span></span>

<span data-ttu-id="8d60f-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` retourneert **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="8d60f-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="8d60f-115">`ISVALIDCHARACTERISO7064 ("AT61")` retourneert **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8d60f-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d60f-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8d60f-116">Additional resources</span></span>

[<span data-ttu-id="8d60f-117">Andere functies (voor specifiek zakelijk domein)</span><span class="sxs-lookup"><span data-stu-id="8d60f-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
