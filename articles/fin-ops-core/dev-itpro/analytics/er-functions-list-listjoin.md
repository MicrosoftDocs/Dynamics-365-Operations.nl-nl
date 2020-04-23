---
title: De ER-functie LISTJOIN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249030"
---
# <a name=""></a><span data-ttu-id="89e24-103"><a name="LISTJOIN">De ER-functie LISTJOIN</a></span><span class="sxs-lookup"><span data-stu-id="89e24-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89e24-104">De functie `LISTJOIN` retourneert een waarde van het type *Recordlijst* die een nieuwe gekoppelde lijst met records aanduidt die wordt gemaakt op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="89e24-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e24-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="89e24-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="89e24-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="89e24-106">Arguments</span></span>

<span data-ttu-id="89e24-107">`list 1`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="89e24-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="89e24-108">Een verwijzing naar een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="89e24-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="89e24-109">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="89e24-109">This argument is mandatory.</span></span>

<span data-ttu-id="89e24-110">`list N`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="89e24-110">`list N`: *Record list*</span></span>

<span data-ttu-id="89e24-111">Een verwijzing naar een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="89e24-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="89e24-112">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="89e24-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="89e24-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="89e24-113">Return values</span></span>

<span data-ttu-id="89e24-114">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="89e24-114">*Record list*</span></span>

<span data-ttu-id="89e24-115">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="89e24-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="89e24-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="89e24-116">Usage notes</span></span>

<span data-ttu-id="89e24-117">De structuur van de lijst die wordt gemaakt, bevat alleen de velden die aanwezig zijn in de structuur van elke recordlijst waarnaar wordt verwezen in de argumenten.</span><span class="sxs-lookup"><span data-stu-id="89e24-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="89e24-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="89e24-118">Example</span></span>

<span data-ttu-id="89e24-119">U voert gegevensbron **Record 1** van het type `Container` in.</span><span class="sxs-lookup"><span data-stu-id="89e24-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="89e24-120">Deze gegevensbron bevat de volgende geneste velden van het type `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="89e24-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="89e24-121">**Code**: dit veld bevat een expressie die een waarde van het type `String` retourneert.</span><span class="sxs-lookup"><span data-stu-id="89e24-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="89e24-122">**Bedrag**: dit veld bevat een expressie die een waarde van het type `Real` retourneert.</span><span class="sxs-lookup"><span data-stu-id="89e24-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="89e24-123">U voert vervolgens gegevensbron **Record 2** van het type `Container` in.</span><span class="sxs-lookup"><span data-stu-id="89e24-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="89e24-124">Deze gegevensbron bevat de volgende geneste velden van het type `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="89e24-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="89e24-125">**Bedrag**: dit veld bevat een expressie die een waarde van het type `Real` retourneert.</span><span class="sxs-lookup"><span data-stu-id="89e24-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="89e24-126">**IsValid**: dit veld bevat een expressie die een waarde van het type `Boolean` retourneert.</span><span class="sxs-lookup"><span data-stu-id="89e24-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="89e24-127">In dit geval retourneert de expressie `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` een nieuwe lijst die twee records bevat.</span><span class="sxs-lookup"><span data-stu-id="89e24-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="89e24-128">De structuur van deze lijst bestaat uit één veld **Bedrag** van het type `Real`, omdat dit veld het enige veld is dat in elk argument van de aangeroepen functie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="89e24-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89e24-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="89e24-129">Additional resources</span></span>

[<span data-ttu-id="89e24-130">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="89e24-130">List functions</span></span>](er-functions-category-list.md)
