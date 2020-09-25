---
title: De ER-functie LIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LIST.
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
ms.openlocfilehash: a31288885abda69873ae23b28a36e2a54852f593
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745148"
---
# <a name="list-er-function"></a><span data-ttu-id="a8921-103">De ER-functie LIST</span><span class="sxs-lookup"><span data-stu-id="a8921-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8921-104">De functie `LIST` retourneert een waarde van het type *Recordlijst* die bestaat uit een nieuwe lijst records die wordt gemaakt op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="a8921-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8921-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a8921-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="a8921-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a8921-106">Arguments</span></span>

<span data-ttu-id="a8921-107">`record 1`: *Container (record)*</span><span class="sxs-lookup"><span data-stu-id="a8921-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="a8921-108">Een verwijzing naar een gegevensbron van het gegevenstype *Record*.</span><span class="sxs-lookup"><span data-stu-id="a8921-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="a8921-109">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="a8921-109">This argument is required.</span></span>

<span data-ttu-id="a8921-110">`record N`: *Container (record)*</span><span class="sxs-lookup"><span data-stu-id="a8921-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="a8921-111">Een verwijzing naar een gegevensbron van het gegevenstype *Record*.</span><span class="sxs-lookup"><span data-stu-id="a8921-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="a8921-112">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="a8921-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a8921-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a8921-113">Return values</span></span>

<span data-ttu-id="a8921-114">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="a8921-114">*Record list*</span></span>

<span data-ttu-id="a8921-115">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="a8921-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a8921-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="a8921-116">Usage notes</span></span>

<span data-ttu-id="a8921-117">De structuur van de lijst die wordt gemaakt, bevat alleen de velden die worden weergegeven in de structuur van elke record die wordt vermeld in de argumenten.</span><span class="sxs-lookup"><span data-stu-id="a8921-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="a8921-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a8921-118">Example</span></span>

<span data-ttu-id="a8921-119">U voert gegevensbron **Record 1** van het type *Container* in.</span><span class="sxs-lookup"><span data-stu-id="a8921-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="a8921-120">Deze gegevensbron bevat de volgende geneste velden van het type *Berekend veld*:</span><span class="sxs-lookup"><span data-stu-id="a8921-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="a8921-121">**Code:** dit veld bevat een expressie die een waarde van het type *Tekenreeks* retourneert.</span><span class="sxs-lookup"><span data-stu-id="a8921-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="a8921-122">**Bedrag:** dit veld bevat een expressie die een waarde van het type *Werkelijk* retourneert.</span><span class="sxs-lookup"><span data-stu-id="a8921-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="a8921-123">U voert gegevensbron **Record 2** van het type *Container* in.</span><span class="sxs-lookup"><span data-stu-id="a8921-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="a8921-124">Deze gegevensbron bevat de volgende geneste velden van het type *Berekend veld*:</span><span class="sxs-lookup"><span data-stu-id="a8921-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="a8921-125">**Bedrag:** dit veld bevat een expressie die een waarde van het type *Werkelijk* retourneert.</span><span class="sxs-lookup"><span data-stu-id="a8921-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="a8921-126">**IsValid:** dit veld bevat een expressie die een waarde van het type *Booleaans* retourneert.</span><span class="sxs-lookup"><span data-stu-id="a8921-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="a8921-127">In dit geval retourneert de expressie `LIST('Record 1', 'Record 2')` een nieuwe lijst die twee records bevat.</span><span class="sxs-lookup"><span data-stu-id="a8921-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="a8921-128">De structuur van deze lijst bestaat uit één veld **Bedrag** van het type *Werkelijk*, omdat dit veld het enige veld is dat in elk argument van de aangeroepen functie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a8921-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8921-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a8921-129">Additional resources</span></span>

[<span data-ttu-id="a8921-130">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="a8921-130">List functions</span></span>](er-functions-category-list.md)
