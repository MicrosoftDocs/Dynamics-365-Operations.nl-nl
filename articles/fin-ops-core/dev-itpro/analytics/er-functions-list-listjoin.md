---
title: De ER-functie LISTJOIN
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTJOIN.
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efee93df7d1cf40d016b36042bb5e7f33c47ae44
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743794"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="99d0e-103">De ER-functie LISTJOIN</span><span class="sxs-lookup"><span data-stu-id="99d0e-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99d0e-104">De functie `LISTJOIN` retourneert een waarde van het type *Recordlijst* die een nieuwe gekoppelde lijst met records aanduidt die wordt gemaakt op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="99d0e-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="99d0e-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="99d0e-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="99d0e-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="99d0e-106">Arguments</span></span>

<span data-ttu-id="99d0e-107">`list 1`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="99d0e-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="99d0e-108">Een verwijzing naar een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="99d0e-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="99d0e-109">Dit is een verplicht argument.</span><span class="sxs-lookup"><span data-stu-id="99d0e-109">This argument is mandatory.</span></span>

<span data-ttu-id="99d0e-110">`list N`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="99d0e-110">`list N`: *Record list*</span></span>

<span data-ttu-id="99d0e-111">Een verwijzing naar een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="99d0e-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="99d0e-112">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="99d0e-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="99d0e-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="99d0e-113">Return values</span></span>

<span data-ttu-id="99d0e-114">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="99d0e-114">*Record list*</span></span>

<span data-ttu-id="99d0e-115">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="99d0e-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="99d0e-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="99d0e-116">Usage notes</span></span>

<span data-ttu-id="99d0e-117">De structuur van de lijst die wordt gemaakt, bevat alleen de velden die aanwezig zijn in de structuur van elke recordlijst waarnaar wordt verwezen in de argumenten.</span><span class="sxs-lookup"><span data-stu-id="99d0e-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="99d0e-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="99d0e-118">Example</span></span>

<span data-ttu-id="99d0e-119">U voert gegevensbron **Record 1** van het type `Container` in.</span><span class="sxs-lookup"><span data-stu-id="99d0e-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="99d0e-120">Deze gegevensbron bevat de volgende geneste velden van het type `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="99d0e-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="99d0e-121">**Code**: dit veld bevat een expressie die een waarde van het type `String` retourneert.</span><span class="sxs-lookup"><span data-stu-id="99d0e-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="99d0e-122">**Bedrag**: dit veld bevat een expressie die een waarde van het type `Real` retourneert.</span><span class="sxs-lookup"><span data-stu-id="99d0e-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="99d0e-123">U voert vervolgens gegevensbron **Record 2** van het type `Container` in.</span><span class="sxs-lookup"><span data-stu-id="99d0e-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="99d0e-124">Deze gegevensbron bevat de volgende geneste velden van het type `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="99d0e-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="99d0e-125">**Bedrag**: dit veld bevat een expressie die een waarde van het type `Real` retourneert.</span><span class="sxs-lookup"><span data-stu-id="99d0e-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="99d0e-126">**IsValid**: dit veld bevat een expressie die een waarde van het type `Boolean` retourneert.</span><span class="sxs-lookup"><span data-stu-id="99d0e-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![Pagina voor ontwerper van ER-modeltoewijzingen](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="99d0e-128">In dit geval retourneert de expressie `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` een nieuwe lijst die twee records bevat.</span><span class="sxs-lookup"><span data-stu-id="99d0e-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![Pagina voor ontwerper van ER-modeltoewijzingen met twee records](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="99d0e-130">De structuur van deze lijst bestaat uit één veld **Bedrag** van het type `Real`, omdat dit veld het enige veld is dat in elk argument van de aangeroepen functie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="99d0e-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![Veld voor bedrag op pagina voor ontwerper van ER-modeltoewijzingen](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="99d0e-132">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="99d0e-132">Additional resources</span></span>

[<span data-ttu-id="99d0e-133">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="99d0e-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="99d0e-134">Fouten opsporen in gegevensbronnen van een uitgevoerde ER-indeling om gegevensstromen en transformatie te analyseren</span><span class="sxs-lookup"><span data-stu-id="99d0e-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]