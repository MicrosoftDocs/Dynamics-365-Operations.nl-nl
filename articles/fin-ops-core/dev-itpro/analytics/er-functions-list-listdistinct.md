---
title: Functie LISTDISTINCT ER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) LISTDISTINCT.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: f20565d73cea8d0cc1361bd03cda86a79a97955e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563819"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="e460b-103">Functie LISTDISTINCT ER</span><span class="sxs-lookup"><span data-stu-id="e460b-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e460b-104">De `LISTDISTINCT`-functie berekent de opgegeven expressie als een selector voor elke record van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="e460b-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="e460b-105">Er wordt een nieuwe waarde *Recordlijst* geretourneerd die één record bevat voor elke unieke selectorwaarde.</span><span class="sxs-lookup"><span data-stu-id="e460b-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e460b-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="e460b-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="e460b-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="e460b-107">Arguments</span></span>

<span data-ttu-id="e460b-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="e460b-108">`list`: *Record list*</span></span>

<span data-ttu-id="e460b-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="e460b-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e460b-110">`selector`: *Primitieve gegevenstype*</span><span class="sxs-lookup"><span data-stu-id="e460b-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="e460b-111">Een geldige expressie die wordt gebruikt om een selectiewaarde te berekenen voor elke record in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="e460b-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="e460b-112">De volgende gegevenstypen worden voor deze parameter ondersteund:</span><span class="sxs-lookup"><span data-stu-id="e460b-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="e460b-113">Booleaans</span><span class="sxs-lookup"><span data-stu-id="e460b-113">Boolean</span></span>
- <span data-ttu-id="e460b-114">Datum</span><span class="sxs-lookup"><span data-stu-id="e460b-114">Date</span></span>
- <span data-ttu-id="e460b-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="e460b-115">DateTime</span></span>
- <span data-ttu-id="e460b-116">Guid</span><span class="sxs-lookup"><span data-stu-id="e460b-116">GUID</span></span>
- <span data-ttu-id="e460b-117">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="e460b-117">Integer</span></span>
- <span data-ttu-id="e460b-118">Int64</span><span class="sxs-lookup"><span data-stu-id="e460b-118">Int64</span></span>
- <span data-ttu-id="e460b-119">Real-modus</span><span class="sxs-lookup"><span data-stu-id="e460b-119">Real</span></span>
- <span data-ttu-id="e460b-120">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="e460b-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="e460b-121">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="e460b-121">Return values</span></span>

<span data-ttu-id="e460b-122">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="e460b-122">*Record list*</span></span>

<span data-ttu-id="e460b-123">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="e460b-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e460b-124">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="e460b-124">Usage notes</span></span>

<span data-ttu-id="e460b-125">De structuur van de lijst die wordt gemaakt, komt overeen met de structuur van de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="e460b-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="e460b-126">Dezelfde selectorwaarde kan worden berekend voor meerdere records in de opgegeven lijst.</span><span class="sxs-lookup"><span data-stu-id="e460b-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="e460b-127">In dit geval zijn de veld waarden van de bijbehorende record in de gemaakte lijst gelijk aan de waarden van de eerste record uit de opgegeven lijst waarvoor de selectorwaarde wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="e460b-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="e460b-128">De uitvoering van deze functie vindt plaats op elke [ER](general-electronic-reporting.md)-gegevensbron van het type *recordlijst* die aanwezig is in het geheugen.</span><span class="sxs-lookup"><span data-stu-id="e460b-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="e460b-129">De gegevensbron **GROUPBY** kan ook worden gebruikt om de lijst met records te genereren waarvoor de selector met afzonderlijke waarden wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="e460b-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="e460b-130">Vanuit het oogpunt van prestatie en geheugenverbruik is het echter beter om de functie `LISTDISTINCT` te gebruiken dan de gegevensbron **GROUPBY**, omdat de uitvoering van de functie in het geheugen plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="e460b-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="e460b-131">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="e460b-131">Example</span></span>

<span data-ttu-id="e460b-132">In het volgende voorbeeld ziet u hoe u de lijst met unieke klantrekeningnummers kunt ophalen die gedurende een bepaalde periode voor ten minste één verkoopfactuur of projectfactuur zijn uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="e460b-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="e460b-133">Voer de gegevensbron **SalesInvoice** in van het type `Record list` die verwijst naar de toepassingstabel **CustInvoiceJour** en de verkoopfacturen filtert voor specifieke perioden.</span><span class="sxs-lookup"><span data-stu-id="e460b-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="e460b-134">Het veld `InvoiceAccount` van deze gegevensbron retourneert het rekeningnummer van een gefactureerde klant.</span><span class="sxs-lookup"><span data-stu-id="e460b-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="e460b-135">Voer de gegevensbron **ProjectInvoice** in van het type `Record list` die verwijst naar de toepassingstabel **ProjInvoiceJour** en de projectfacturen filtert voor specifieke perioden.</span><span class="sxs-lookup"><span data-stu-id="e460b-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="e460b-136">Het veld `InvoiceAccount` van deze gegevensbron retourneert het rekeningnummer van een gefactureerde klant.</span><span class="sxs-lookup"><span data-stu-id="e460b-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="e460b-137">Configureer de gegevensbron **AllInvoices** van het veld `Calculated field` dat de expressie `LISTJOIN(SalesInvoice, ProjectInvoice)` bevat.</span><span class="sxs-lookup"><span data-stu-id="e460b-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="e460b-138">Deze gegevensbron retourneert de gekoppelde lijst met verkoopfacturen en projectfacturen.</span><span class="sxs-lookup"><span data-stu-id="e460b-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="e460b-139">Configureer de gegevensbron **InvoicedCustomer** van het veld `Record list` dat de expressie `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` bevat.</span><span class="sxs-lookup"><span data-stu-id="e460b-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="e460b-140">Met deze gegevensbron wordt een nieuwe lijst geretourneerd die één record bevat voor elke unieke klant die gedurende de gedefinieerde periode is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="e460b-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="e460b-141">Het veld `InvoiceAccount` van deze lijst bevat een rekeningnummer van een klant.</span><span class="sxs-lookup"><span data-stu-id="e460b-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e460b-142">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e460b-142">Additional resources</span></span>

[<span data-ttu-id="e460b-143">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="e460b-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]