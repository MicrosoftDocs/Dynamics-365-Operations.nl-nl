---
title: De ER-functie NULLDATETIME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLDATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 3cd4c152d4e220a2f6315265ed5e44d148134279
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042248"
---
# <span data-ttu-id="57af0-103"><a name="NULLDATETIME">De ER-functie NULLDATETIME</a></span><span class="sxs-lookup"><span data-stu-id="57af0-103"><a name="NULLDATETIME">NULLDATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57af0-104">De functie `NULLDATETIME` retourneert een waarde van het type *DateTime* die voor de **null**-datum en -tijd staat (1 januari 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="57af0-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="57af0-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="57af0-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="57af0-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="57af0-106">Return values</span></span>

<span data-ttu-id="57af0-107">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="57af0-107">*DateTime*</span></span>

<span data-ttu-id="57af0-108">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="57af0-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="57af0-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="57af0-109">Example</span></span>

<span data-ttu-id="57af0-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` retourneert de tekenreekswaarde **1900-01-01T00:00:00.0000000+00:00** wanneer deze wordt aangeroepen tijdens een proces dat is geïnitieerd door een toepassingsgebruiker met de tijdzonewaarde **(GMT) Coordinated Universal Time** in de sectie **Voorkeuren voor taal en land/regio**.</span><span class="sxs-lookup"><span data-stu-id="57af0-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57af0-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="57af0-111">Additional resources</span></span>

[<span data-ttu-id="57af0-112">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="57af0-112">Date and time functions</span></span>](er-functions-category-datetime.md)
