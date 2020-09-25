---
title: De ER-functie SPLITLIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLITLIST.
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
ms.openlocfilehash: 950fc711f0e28eaee7fabc437ee16a022e1b705e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744786"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="a6cdd-103">De ER-functie SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="a6cdd-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6cdd-104">De functie `SPLITLIST` splitst de opgegeven lijst in sublijsten (of batches) waarvan elk het opgegeven aantal records bevat.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="a6cdd-105">De functie retourneert vervolgens het resultaat als een nieuwe waarde van het type *Recordlijst* die uit de batches bestaat.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6cdd-106">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="a6cdd-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="a6cdd-107">Argumenten</span><span class="sxs-lookup"><span data-stu-id="a6cdd-107">Arguments</span></span>

<span data-ttu-id="a6cdd-108">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="a6cdd-108">`list`: *Record list*</span></span>

<span data-ttu-id="a6cdd-109">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a6cdd-110">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="a6cdd-110">`number`: *Integer*</span></span>

<span data-ttu-id="a6cdd-111">Het maximum aantal records per batch.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="a6cdd-112">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="a6cdd-112">Return values</span></span>

<span data-ttu-id="a6cdd-113">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="a6cdd-113">*Record list*</span></span>

<span data-ttu-id="a6cdd-114">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a6cdd-115">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="a6cdd-115">Usage notes</span></span>

<span data-ttu-id="a6cdd-116">De geretourneerde lijst batches bevat de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="a6cdd-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="a6cdd-117">**Waarde**: *Lijst*</span><span class="sxs-lookup"><span data-stu-id="a6cdd-117">**Value:** *List*</span></span>

    <span data-ttu-id="a6cdd-118">De lijst met records die deel uitmaken van de huidige batch.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="a6cdd-119">**BatchNumber**: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="a6cdd-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="a6cdd-120">Het nummer van de huidige batch in de geretourneerde lijst.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="a6cdd-121">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a6cdd-121">Example</span></span>

<span data-ttu-id="a6cdd-122">In het volgende voorbeeld wordt een gegevensbron **Regels** gemaakt als een recordlijst met drie records.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="a6cdd-123">Deze lijst is onderverdeeld in batches, die elk maximaal twee records bevatten.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="a6cdd-124">In de volgende afbeelding ziet u de ontworpen indelingslay-out.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="a6cdd-125">In deze indelingslay-out worden bindingen met de gegevensbron **Regels** gemaakt voor het genereren van uitvoer in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="a6cdd-126">Deze uitvoer presenteert afzonderlijke knooppunten voor elke batch en de records daarin.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="a6cdd-127">In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a6cdd-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="a6cdd-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a6cdd-128">Additional resources</span></span>

[<span data-ttu-id="a6cdd-129">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="a6cdd-129">List functions</span></span>](er-functions-category-list.md)
