---
title: De ER-functie DATETODATETIME
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATETODATETIME.
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916379"
---
# <span data-ttu-id="3f175-103"><a name="DATETODATETIME">De ER-functie DATETODATETIME</a></span><span class="sxs-lookup"><span data-stu-id="3f175-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f175-104">De functie `DATETODATETIME` retourneert een waarde van het type *DateTime* die wordt geconverteerd van een bepaalde datumwaarde naar een datum-/tijdwaarde in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="3f175-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f175-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="3f175-105">Syntax</span></span>

```
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="3f175-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="3f175-106">Arguments</span></span>

<span data-ttu-id="3f175-107">`date`: *Datum*</span><span class="sxs-lookup"><span data-stu-id="3f175-107">`date`: *Date*</span></span>

<span data-ttu-id="3f175-108">Een datumwaarde waarop de datum moet worden geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="3f175-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="3f175-109">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="3f175-109">Return values</span></span>

<span data-ttu-id="3f175-110">*Datum/tijd*</span><span class="sxs-lookup"><span data-stu-id="3f175-110">*DateTime*</span></span>

<span data-ttu-id="3f175-111">De resulterende datum-/tijdwaarde.</span><span class="sxs-lookup"><span data-stu-id="3f175-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3f175-112">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="3f175-112">Example 1</span></span>

<span data-ttu-id="3f175-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` retourneert de datum van de huidige Microsoft Dynamics 365 Finance-sessie, 24 december 2015, als **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="3f175-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="3f175-114">In dit voorbeeld is **CompInfo** een ER-gegevensbron van het type **Finance and Operations/Table** waarmee naar de tabel CompanyInfo wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="3f175-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="3f175-115">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="3f175-115">Example 2</span></span>

<span data-ttu-id="3f175-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` retourneert de datum-/tijdwaarde **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="3f175-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f175-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3f175-117">Additional resources</span></span>

[<span data-ttu-id="3f175-118">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="3f175-118">Date and time functions</span></span>](er-functions-category-datetime.md)
