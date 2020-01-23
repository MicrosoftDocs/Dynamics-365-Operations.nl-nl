---
title: De ER-functie TODAY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c7e9917dcdc45a52e0ad490f5fa194d5390cc437
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917414"
---
# <span data-ttu-id="55894-103"><a name="TODAY">De ER-functie TODAY</a></span><span class="sxs-lookup"><span data-stu-id="55894-103"><a name="TODAY">TODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55894-104">De functie `TODAY` retourneert een *datumwaarde* die voor de huidige datum van de toepassingsserver staat.</span><span class="sxs-lookup"><span data-stu-id="55894-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="55894-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="55894-105">Syntax</span></span>

```
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="55894-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="55894-106">Return values</span></span>

<span data-ttu-id="55894-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="55894-107">*Date*</span></span>

<span data-ttu-id="55894-108">De resulterende datumwaarde.</span><span class="sxs-lookup"><span data-stu-id="55894-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="55894-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="55894-109">Example</span></span>

<span data-ttu-id="55894-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="55894-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55894-111">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="55894-111">Additional resources</span></span>

[<span data-ttu-id="55894-112">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="55894-112">Date and time functions</span></span>](er-functions-category-datetime.md)
