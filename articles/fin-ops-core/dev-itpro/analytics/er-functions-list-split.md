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
ms.openlocfilehash: 31caf7c728a92d31428f47320c074fa9fc35bda6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916103"
---
# <span data-ttu-id="0c46a-103"><a name="SPLIT">De ER-functie SPLIT</a></span><span class="sxs-lookup"><span data-stu-id="0c46a-103"><a name="SPLIT">SPLIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c46a-104">De functie `SPLIT` splitst de opgegeven invoertekenreeks in subtekenreeksen en retourneert het resultaat als een nieuwe waarde van het type *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="0c46a-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0c46a-105">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="0c46a-105">Syntax 1</span></span>

```
SPLIT (input, length)
```

<span data-ttu-id="0c46a-106">Deze syntaxis wordt gebuikt om de opgegeven invoertekenreeks te splitsen in subreeksen, waarvan elk de opgegeven lengte heeft.</span><span class="sxs-lookup"><span data-stu-id="0c46a-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="0c46a-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="0c46a-107">Syntax 2</span></span>

```
SPLIT (input, delimiter)
```

<span data-ttu-id="0c46a-108">Deze syntaxis wordt gebruikt om de opgegeven invoertekenreeks te splitsen in subreeksen, op basis van het opgegeven scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="0c46a-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="0c46a-109">Argumenten</span><span class="sxs-lookup"><span data-stu-id="0c46a-109">Arguments</span></span>

<span data-ttu-id="0c46a-110">`input`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="0c46a-110">`input`: *String*</span></span>

<span data-ttu-id="0c46a-111">De tekst die moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="0c46a-111">The text to split.</span></span>

<span data-ttu-id="0c46a-112">`length`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="0c46a-112">`length`: *Integer*</span></span>

<span data-ttu-id="0c46a-113">De maximale lengte van één subtekenreeks.</span><span class="sxs-lookup"><span data-stu-id="0c46a-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="0c46a-114">`delimiter`: *Tekenreeks*</span><span class="sxs-lookup"><span data-stu-id="0c46a-114">`delimiter`: *String*</span></span>

<span data-ttu-id="0c46a-115">Een scheidingsteken dat wordt gebruikt om subtekenreeksen te scheiden.</span><span class="sxs-lookup"><span data-stu-id="0c46a-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c46a-116">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="0c46a-116">Return values</span></span>

<span data-ttu-id="0c46a-117">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="0c46a-117">*Record list*</span></span>

<span data-ttu-id="0c46a-118">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="0c46a-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c46a-119">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="0c46a-119">Usage notes</span></span>

<span data-ttu-id="0c46a-120">De recordstructuur van de lijst die wordt geretourneerd, bestaat uit het veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="0c46a-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c46a-121">Elke record van de lijst die wordt geretourneerd, bevat gegenereerde subtekenreeksen in dit veld.</span><span class="sxs-lookup"><span data-stu-id="0c46a-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="0c46a-122">Als het argument `delimiter` scheidingsteken leeg is, wordt een nieuwe lijst geretourneerd die bestaat uit één record met een veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="0c46a-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c46a-123">Dit veld bevat de ingevoerde tekst.</span><span class="sxs-lookup"><span data-stu-id="0c46a-123">This field contains the input text.</span></span>

<span data-ttu-id="0c46a-124">Als het argument `input` leeg is, wordt een nieuwe lege lijst geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0c46a-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="0c46a-125">Als het argument `input` of `delimiter` niet is opgegeven (null), treedt een toepassingsuitzondering op.</span><span class="sxs-lookup"><span data-stu-id="0c46a-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c46a-126">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="0c46a-126">Example 1</span></span>

<span data-ttu-id="0c46a-127">`SPLIT ("abcd", 3)` retourneert een nieuwe lijst die bestaat uit twee records met een veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="0c46a-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c46a-128">Het veld **Waarde** in de eerste record bevat de tekst **abc** en het veld **Waarde** in de tweede record bevat de tekst **d**.</span><span class="sxs-lookup"><span data-stu-id="0c46a-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c46a-129">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="0c46a-129">Example 2</span></span>

<span data-ttu-id="0c46a-130">`SPLIT ("XAb aBy", "aB")` retourneert een nieuwe lijst die bestaat uit drie records met een veld **Waarde** van het type *Tekenreeks*.</span><span class="sxs-lookup"><span data-stu-id="0c46a-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="0c46a-131">Het veld **Waarde** in de eerste record bevat de tekst **X**, het veld **Waarde** in de tweede record bevat de tekst **&nbsp;** en het veld **Waarde** in de derde record bevat de tekst **y**.</span><span class="sxs-lookup"><span data-stu-id="0c46a-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0c46a-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0c46a-132">Additional resources</span></span>

[<span data-ttu-id="0c46a-133">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="0c46a-133">List functions</span></span>](er-functions-category-list.md)
