---
title: De ER-functie NULLDATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLDATE.
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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744282"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="0e36b-103">De ER-functie NULLDATE</span><span class="sxs-lookup"><span data-stu-id="0e36b-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e36b-104">De functie `NULLDATE` retourneert een *datumwaarde* die voor de **nuldatum** staat (1 januari 1900).</span><span class="sxs-lookup"><span data-stu-id="0e36b-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e36b-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="0e36b-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="0e36b-106">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="0e36b-106">Return values</span></span>

<span data-ttu-id="0e36b-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="0e36b-107">*Date*</span></span>

<span data-ttu-id="0e36b-108">De resulterende datumwaarde.</span><span class="sxs-lookup"><span data-stu-id="0e36b-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0e36b-109">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="0e36b-109">Example 1</span></span>

<span data-ttu-id="0e36b-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` retourneert de **null**-datum, 1 januari 1900, als **1900-01-01**, volgens de opgegeven aangepaste notatie.</span><span class="sxs-lookup"><span data-stu-id="0e36b-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="0e36b-111">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="0e36b-111">Example 2</span></span>

<span data-ttu-id="0e36b-112">De expressie `IF( Invoice.DocumentDate = NULLDATE(), true, false)` retourneert **True** wanneer de waarde van het veld **DocumentDate** gelijk is aan de **null**-datum.</span><span class="sxs-lookup"><span data-stu-id="0e36b-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="0e36b-113">In dit voorbeeld is **Factuur** een ER-gegevensbron van het type **Finance/Tabelrecords** waarmee naar de tabel CustInvoiceJour wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="0e36b-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e36b-114">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0e36b-114">Additional resources</span></span>

[<span data-ttu-id="0e36b-115">Datum- en tijdfuncties</span><span class="sxs-lookup"><span data-stu-id="0e36b-115">Date and time functions</span></span>](er-functions-category-datetime.md)
