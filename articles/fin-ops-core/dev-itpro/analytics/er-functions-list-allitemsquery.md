---
title: De ER-functie ALLITEMSQUERY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ALLITEMSQUERY.
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
ms.openlocfilehash: ed21252fbbe3d4adad106625062e10e3de712bb0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687739"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="cab10-103">De ER-functie ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="cab10-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cab10-104">De functie `ALLITEMSQUERY` wordt uitgevoerd als een gekoppelde SQL-query.</span><span class="sxs-lookup"><span data-stu-id="cab10-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="cab10-105">Het resultaat is een nieuwe afgevlakte waarde van het type *Recordlijst* die bestaat uit een lijst met records en alle items vertegenwoordigt die overeenkomen met het opgegeven pad.</span><span class="sxs-lookup"><span data-stu-id="cab10-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="cab10-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="cab10-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="cab10-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="cab10-107">Arguments</span></span>

<span data-ttu-id="cab10-108">`path`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="cab10-108">`path`: *Record list*</span></span>

<span data-ttu-id="cab10-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="cab10-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="cab10-110">Het moet ten minste één relatie bevatten.</span><span class="sxs-lookup"><span data-stu-id="cab10-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="cab10-111">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="cab10-111">Return values</span></span>

<span data-ttu-id="cab10-112">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="cab10-112">*Record list*</span></span>

<span data-ttu-id="cab10-113">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="cab10-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cab10-114">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="cab10-114">Usage notes</span></span>

<span data-ttu-id="cab10-115">Het opgegeven pad moet worden gedefinieerd als een geldig gegevensbronpad van een gegevensbronelement van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="cab10-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="cab10-116">Het moet ook ten minste één relatie bevatten.</span><span class="sxs-lookup"><span data-stu-id="cab10-116">It must also contain at least one relation.</span></span> <span data-ttu-id="cab10-117">Gegevenselementen zoals de *padreeks* en *datum* moeten tijdens het ontwerp tot een fout leiden in ER Expression Builder.</span><span class="sxs-lookup"><span data-stu-id="cab10-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="cab10-118">Wanneer deze functie wordt toegepast op gegevensbronnen van het gegevenstype *Recordlijst* die verwijzen naar een toepassingsobject dat rechtstreeks kan worden aangeroepen met behulp van SQL (bijvoorbeeld een tabel, entiteit of query), wordt deze uitgevoerd als een samengevoegde SQL-query.</span><span class="sxs-lookup"><span data-stu-id="cab10-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="cab10-119">Anders wordt deze in het geheugen uitgevoerd als de functie [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="cab10-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="cab10-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="cab10-120">Example</span></span>

<span data-ttu-id="cab10-121">U definieert de volgende gegevensbronnen in uw modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="cab10-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="cab10-122">Een gegevensbron **CustInv** van het type *Tabelrecords* die verwijst naar de tabel CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="cab10-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="cab10-123">Een gegevensbron **Filteredinv** van het type *Berekend veld* die de expressie `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` bevat</span><span class="sxs-lookup"><span data-stu-id="cab10-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="cab10-124">Een gegevensbron **JourLines** van het type *Berekend veld* die de expressie `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` bevat</span><span class="sxs-lookup"><span data-stu-id="cab10-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="cab10-125">Bij het uitvoeren van de modeltoewijzing om de gegevensbron **JourLines** aan te roepen, wordt de volgende SQL-instructie uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="cab10-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="cab10-126">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="cab10-126">Additional resources</span></span>

[<span data-ttu-id="cab10-127">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="cab10-127">List functions</span></span>](er-functions-category-list.md)
