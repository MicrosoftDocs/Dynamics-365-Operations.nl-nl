---
title: De ER-functie SPLITLIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SPLITLIST.
author: NickSelin
ms.date: 03/15/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745564"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="904b4-103">De ER-functie SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="904b4-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="904b4-104">De functie `SPLITLIST` splitst de opgegeven lijst in sublijsten (of batches) waarvan elk het opgegeven aantal records bevat.</span><span class="sxs-lookup"><span data-stu-id="904b4-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="904b4-105">De functie retourneert vervolgens het resultaat als een nieuwe waarde van het type *Recordlijst* die uit de batches bestaat.</span><span class="sxs-lookup"><span data-stu-id="904b4-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="904b4-106">Syntaxis 1</span><span class="sxs-lookup"><span data-stu-id="904b4-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="904b4-107">Syntaxis 2</span><span class="sxs-lookup"><span data-stu-id="904b4-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="904b4-108">Argumenten</span><span class="sxs-lookup"><span data-stu-id="904b4-108">Arguments</span></span>

<span data-ttu-id="904b4-109">`list`: *Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="904b4-109">`list`: *Record list*</span></span>

<span data-ttu-id="904b4-110">Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.</span><span class="sxs-lookup"><span data-stu-id="904b4-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="904b4-111">`number`: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="904b4-111">`number`: *Integer*</span></span>

<span data-ttu-id="904b4-112">Het maximum aantal records per batch.</span><span class="sxs-lookup"><span data-stu-id="904b4-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="904b4-113">`on-demand reading flag`: *Booleaans*</span><span class="sxs-lookup"><span data-stu-id="904b4-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="904b4-114">Een *Booleaanse* waarde die aangeeft of elementen van sublijsten op aanvraag moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="904b4-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="904b4-115">Retourwaarden</span><span class="sxs-lookup"><span data-stu-id="904b4-115">Return values</span></span>

<span data-ttu-id="904b4-116">*Recordlijst*</span><span class="sxs-lookup"><span data-stu-id="904b4-116">*Record list*</span></span>

<span data-ttu-id="904b4-117">De resulterende lijst met records.</span><span class="sxs-lookup"><span data-stu-id="904b4-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="904b4-118">Gebruiksaanwijzingen</span><span class="sxs-lookup"><span data-stu-id="904b4-118">Usage notes</span></span>

<span data-ttu-id="904b4-119">De geretourneerde lijst batches bevat de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="904b4-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="904b4-120">**Waarde**: *Lijst*</span><span class="sxs-lookup"><span data-stu-id="904b4-120">**Value:** *List*</span></span>

    <span data-ttu-id="904b4-121">De lijst met records die deel uitmaken van de huidige batch.</span><span class="sxs-lookup"><span data-stu-id="904b4-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="904b4-122">**BatchNumber**: *Geheel getal*</span><span class="sxs-lookup"><span data-stu-id="904b4-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="904b4-123">Het nummer van de huidige batch in de geretourneerde lijst.</span><span class="sxs-lookup"><span data-stu-id="904b4-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="904b4-124">Wanneer de on-demand leesmarkering is ingesteld op **Waar**, worden sublijsten op aanvraag gegenereerd, waardoor het geheugenverbruik kan worden beperkt, maar prestaties kunnen verslechteren als elementen niet opeenvolgend worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="904b4-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="904b4-125">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="904b4-125">Example</span></span>

<span data-ttu-id="904b4-126">In het volgende voorbeeld wordt een gegevensbron **Regels** gemaakt als een recordlijst met drie records.</span><span class="sxs-lookup"><span data-stu-id="904b4-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="904b4-127">Deze lijst is onderverdeeld in batches, die elk maximaal twee records bevatten.</span><span class="sxs-lookup"><span data-stu-id="904b4-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="904b4-128">In de volgende afbeelding ziet u de ontworpen indelingslay-out.</span><span class="sxs-lookup"><span data-stu-id="904b4-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="904b4-129">In deze indelingslay-out worden bindingen met de gegevensbron **Regels** gemaakt voor het genereren van uitvoer in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="904b4-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="904b4-130">Deze uitvoer presenteert afzonderlijke knooppunten voor elke batch en de records daarin.</span><span class="sxs-lookup"><span data-stu-id="904b4-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="904b4-131">In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="904b4-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="904b4-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="904b4-132">Additional resources</span></span>

[<span data-ttu-id="904b4-133">Lijstfuncties</span><span class="sxs-lookup"><span data-stu-id="904b4-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
