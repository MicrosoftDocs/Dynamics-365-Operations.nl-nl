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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683082"
---
# <a name="list-er-function"></a><span data-ttu-id="44fa0-103">De ER-functie LIST</span><span class="sxs-lookup"><span data-stu-id="44fa0-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44fa0-104">De functie `LIST` retourneert een waarde van het type *Recordlijst* die bestaat uit een nieuwe lijst records die wordt gemaakt op basis van de opgegeven argumenten.</span><span class="sxs-lookup"><span data-stu-id="44fa0-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fa0-105">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="44fa0-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="44fa0-106">Argumenten</span><span class="sxs-lookup"><span data-stu-id="44fa0-106">Arguments</span></span>

<span data-ttu-id="44fa0-107">`record 1`: *Container (record)*</span><span class="sxs-lookup"><span data-stu-id="44fa0-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="44fa0-108">Een verwijzing naar een gegevensbron van het gegevenstype *Record*.</span><span class="sxs-lookup"><span data-stu-id="44fa0-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="44fa0-109">Dit argument is verplicht.</span><span class="sxs-lookup"><span data-stu-id="44fa0-109">This argument is required.</span></span>

<span data-ttu-id="44fa0-110">`record N`: *Container (record)*</span><span class="sxs-lookup"><span data-stu-id="44fa0-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="44fa0-111">Een verwijzing naar een gegevensbron van het gegevenstype *Record*.</span><span class="sxs-lookup"><span data-stu-id="44fa0-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="44fa0-112">Deze aanvullende argumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="44fa0-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="44fa0-113">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="44fa0-113">Return values</span></span>

<span data-ttu-id="44fa0-114">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="44fa0-114">*Record list*</span></span>

<span data-ttu-id="44fa0-115">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="44fa0-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="44fa0-116">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="44fa0-116">Usage notes</span></span>

<span data-ttu-id="44fa0-117">De structuur van de lijst die wordt gemaakt, bevat alleen de velden die worden weergegeven in de structuur van elke record die wordt vermeld in de argumenten.</span><span class="sxs-lookup"><span data-stu-id="44fa0-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="44fa0-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="44fa0-118">Example</span></span>

<span data-ttu-id="44fa0-119">U voert gegevensbron **Record 1** van het type *Container* in.</span><span class="sxs-lookup"><span data-stu-id="44fa0-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="44fa0-120">Deze gegevensbron bevat de volgende geneste velden van het type *Berekend veld*:</span><span class="sxs-lookup"><span data-stu-id="44fa0-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="44fa0-121">**Code:** dit veld bevat een expressie die een waarde van het type *Tekenreeks* retourneert.</span><span class="sxs-lookup"><span data-stu-id="44fa0-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="44fa0-122">**Bedrag:** dit veld bevat een expressie die een waarde van het type *Werkelijk* retourneert.</span><span class="sxs-lookup"><span data-stu-id="44fa0-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="44fa0-123">U voert gegevensbron **Record 2** van het type *Container* in.</span><span class="sxs-lookup"><span data-stu-id="44fa0-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="44fa0-124">Deze gegevensbron bevat de volgende geneste velden van het type *Berekend veld*:</span><span class="sxs-lookup"><span data-stu-id="44fa0-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="44fa0-125">**Bedrag:** dit veld bevat een expressie die een waarde van het type *Werkelijk* retourneert.</span><span class="sxs-lookup"><span data-stu-id="44fa0-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="44fa0-126">**IsValid:** dit veld bevat een expressie die een waarde van het type *Booleaans* retourneert.</span><span class="sxs-lookup"><span data-stu-id="44fa0-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="44fa0-127">In dit geval retourneert de expressie `LIST('Record 1', 'Record 2')` een nieuwe lijst die twee records bevat.</span><span class="sxs-lookup"><span data-stu-id="44fa0-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="44fa0-128">De structuur van deze lijst bestaat uit één veld **Bedrag** van het type *Werkelijk*, omdat dit veld het enige veld is dat in elk argument van de aangeroepen functie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="44fa0-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44fa0-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="44fa0-129">Additional resources</span></span>

[<span data-ttu-id="44fa0-130">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="44fa0-130">List functions</span></span>](er-functions-category-list.md)
