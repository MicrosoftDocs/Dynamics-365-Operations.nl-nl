---
title: De ER-functie SPLIT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLIT.
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
ms.openlocfilehash: c171509353fed92b14ca0d7473742e4a9a54bad1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745268"
---
# <a name="split-er-function"></a><span data-ttu-id="3f604-103">De ER-functie SPLIT</span><span class="sxs-lookup"><span data-stu-id="3f604-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f604-104">De functie `SPLIT` splitst de opgegeven invoertekenreeks in subtekenreeksen en retourneert het resultaat als een nieuwe waarde van het type *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="3f604-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="3f604-105">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="3f604-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="3f604-106">Deze syntaxis wordt gebuikt om de opgegeven invoertekenreeks te splitsen in subreeksen, waarvan elk de opgegeven lengte heeft.</span><span class="sxs-lookup"><span data-stu-id="3f604-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="3f604-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="3f604-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="3f604-108">Deze syntaxis wordt gebruikt om de opgegeven invoertekenreeks te splitsen in subreeksen, op basis van het opgegeven scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="3f604-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="3f604-109">Argumenten</span><span class="sxs-lookup"><span data-stu-id="3f604-109">Arguments</span></span>

<span data-ttu-id="3f604-110">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3f604-110">`input`: *String*</span></span>

<span data-ttu-id="3f604-111">De tekst die moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="3f604-111">The text to split.</span></span>

<span data-ttu-id="3f604-112">`length`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="3f604-112">`length`: *Integer*</span></span>

<span data-ttu-id="3f604-113">De maximale lengte van één subtekenreeks.</span><span class="sxs-lookup"><span data-stu-id="3f604-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="3f604-114">`delimiter`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="3f604-114">`delimiter`: *String*</span></span>

<span data-ttu-id="3f604-115">Een scheidingsteken dat wordt gebruikt om subtekenreeksen te scheiden.</span><span class="sxs-lookup"><span data-stu-id="3f604-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="3f604-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="3f604-116">Return values</span></span>

<span data-ttu-id="3f604-117">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="3f604-117">*Record list*</span></span>

<span data-ttu-id="3f604-118">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="3f604-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3f604-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="3f604-119">Usage notes</span></span>

<span data-ttu-id="3f604-120">De recordstructuur van de lijst die wordt geretourneerd, bestaat uit het veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="3f604-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="3f604-121">Elke record van de lijst die wordt geretourneerd, bevat gegenereerde subtekenreeksen in dit veld.</span><span class="sxs-lookup"><span data-stu-id="3f604-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="3f604-122">Als het argument `delimiter` scheidingsteken leeg is, wordt een nieuwe lijst geretourneerd die bestaat uit één record met een veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="3f604-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="3f604-123">Dit veld bevat de ingevoerde tekst.</span><span class="sxs-lookup"><span data-stu-id="3f604-123">This field contains the input text.</span></span>

<span data-ttu-id="3f604-124">Als het argument `input` leeg is, wordt een nieuwe lege lijst geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="3f604-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="3f604-125">Als het argument `input` of `delimiter` niet is opgegeven (null), treedt een toepassingsuitzondering op.</span><span class="sxs-lookup"><span data-stu-id="3f604-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="3f604-126">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="3f604-126">Example 1</span></span>

<span data-ttu-id="3f604-127">`SPLIT ("abcd", 3)` retourneert een nieuwe lijst die bestaat uit twee records met een veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="3f604-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="3f604-128">Het veld **Waarde** in de eerste record bevat de tekst **abc** en het veld **Waarde** in de tweede record bevat de tekst **d**.</span><span class="sxs-lookup"><span data-stu-id="3f604-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3f604-129">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="3f604-129">Example 2</span></span>

<span data-ttu-id="3f604-130">`SPLIT ("XAb aBy", "aB")` retourneert een nieuwe lijst die bestaat uit drie records met een veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="3f604-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="3f604-131">Het veld **Waarde** in de eerste record bevat de tekst **X**, het veld **Waarde** in de tweede record bevat de tekst **&nbsp;** en het veld **Waarde** in de derde record bevat de tekst **y**.</span><span class="sxs-lookup"><span data-stu-id="3f604-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="3f604-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3f604-132">Additional resources</span></span>

[<span data-ttu-id="3f604-133">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="3f604-133">List functions</span></span>](er-functions-category-list.md)
