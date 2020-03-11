---
title: De ER-functie CHAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CHAR.
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041223"
---
# <span data-ttu-id="5eb24-103"><a name="CHAR">De ER-functie CHAR</a></span><span class="sxs-lookup"><span data-stu-id="5eb24-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eb24-104">De functie `CHAR` retourneert een waarde van het type *Tekenreeks* van één teken waarnaar wordt verwezen door het opgegeven Unicode-nummer.</span><span class="sxs-lookup"><span data-stu-id="5eb24-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb24-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="5eb24-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="5eb24-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="5eb24-106">Arguments</span></span>

<span data-ttu-id="5eb24-107">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="5eb24-107">`number`: *Integer*</span></span>

<span data-ttu-id="5eb24-108">Een getal dat overeenkomt met een verwacht enkel teken.</span><span class="sxs-lookup"><span data-stu-id="5eb24-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="5eb24-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="5eb24-109">Return values</span></span>

<span data-ttu-id="5eb24-110">*Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="5eb24-110">*String*</span></span>

<span data-ttu-id="5eb24-111">De resulterende tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="5eb24-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5eb24-112">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="5eb24-112">Usage notes</span></span>

<span data-ttu-id="5eb24-113">De door deze functie geretourneerde tekenreeks is afhankelijk van de codering die in het bovenliggende indelingselement **FILE** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="5eb24-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="5eb24-114">Zie voor een overzicht van ondersteunde coderingen [Coderingsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="5eb24-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="5eb24-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5eb24-115">Example</span></span>

<span data-ttu-id="5eb24-116">`CHAR (255)` retourneert **ÿ**.</span><span class="sxs-lookup"><span data-stu-id="5eb24-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eb24-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5eb24-117">Additional resources</span></span>

[<span data-ttu-id="5eb24-118">Tekstfuncties</span><span class="sxs-lookup"><span data-stu-id="5eb24-118">Text functions</span></span>](er-functions-category-text.md)
