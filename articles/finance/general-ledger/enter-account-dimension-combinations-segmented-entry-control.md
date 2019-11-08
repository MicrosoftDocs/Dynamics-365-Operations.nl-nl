---
title: Account- en dimensiecombinaties invoeren (gesegmenteerd invoerbesturingselement)
description: In dit artikel wordt beschreven hoe u combinaties van rekeningen en dimensies of grootboekrekeningen invoert. Deze invoerervaring wordt ook wel gesegmenteerd invoerbestuur genoemd.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 872ee7812d98e6102798c3a10773176541c02c90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186642"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="f2f4b-104">Account- en dimensiecombinaties invoeren (gesegmenteerd invoerbesturingselement)</span><span class="sxs-lookup"><span data-stu-id="f2f4b-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2f4b-105">In dit artikel wordt beschreven hoe u combinaties van rekeningen en dimensies of grootboekrekeningen invoert.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="f2f4b-106">Deze invoerervaring wordt ook wel gesegmenteerd invoerbestuur genoemd.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="f2f4b-107">Gebruikers voeren account- en dimensiecombinaties in op verschillende pagina's, zoals pagina's voor algemene journalen, budgettering en boekdefinities.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="f2f4b-108">De geldige account- en dimensiecombinaties zijn afhankelijk van de rekeningstructuren die aan het grootboek worden toegewezen en de geavanceerde regels die aan de rekeningstructuren worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="f2f4b-109">Wanneer gebruikers een combinatie invoeren, kunnen ze de waarden handmatig typen of gebruikmaken van een uitgebreide zoekfunctie.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="f2f4b-110">Wanneer u het veld invoert, kunt u beginnen met typen en er wordt dan gezocht naar de waarde en de omschrijving.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="f2f4b-111">Bijvoorbeeld: als u 180 typt, wordt gezocht naar alle waarden die met deze nummercombinatie beginnen.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="f2f4b-112">U kunt ook Contant typen. Er wordt dan gezocht naar elke waarde met een beschrijving die met Contant begint.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="f2f4b-113">U kunt ook een jokerteken gebruiken, zoals \*Contant of \*180 om te zoeken naar een waarde of omschrijving die de zoekcriteria bevat.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="f2f4b-114">In de volgende tabel worden de sneltoetsen op het toetsenbord beschreven die kunnen worden gebruikt wanneer de zoekopdracht gesloten is.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f4b-115">Sneltoets</span><span class="sxs-lookup"><span data-stu-id="f2f4b-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="f2f4b-116">Actie</span><span class="sxs-lookup"><span data-stu-id="f2f4b-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2f4b-117">Alt+pijl omlaag</span><span class="sxs-lookup"><span data-stu-id="f2f4b-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="f2f4b-118">De zoekopdracht openen.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-118">Open the lookup.</span></span> <span data-ttu-id="f2f4b-119">Als u een tweede keer op Alt+pijl omlaag drukt, wordt de focus verplaatst naar de segmenten in de flyout.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="f2f4b-120">Enter en Shift+Enter</span><span class="sxs-lookup"><span data-stu-id="f2f4b-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="f2f4b-121">Scheidingsteken voor rekeningschema</span><span class="sxs-lookup"><span data-stu-id="f2f4b-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="f2f4b-122">Pijl naar rechts en pijl naar links</span><span class="sxs-lookup"><span data-stu-id="f2f4b-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="f2f4b-123">Verplaatsen naar het volgende of vorige segment.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2f4b-124">Tabblad</span><span class="sxs-lookup"><span data-stu-id="f2f4b-124">Tab</span></span></td>
<td><span data-ttu-id="f2f4b-125">Naar het volgende veld in het raster verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f2f4b-126">In de volgende tabel worden de sneltoetsen op het toetsenbord beschreven die kunnen worden gebruikt wanneer de zoekopdracht open is.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f4b-127">Sneltoets</span><span class="sxs-lookup"><span data-stu-id="f2f4b-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="f2f4b-128">Actie</span><span class="sxs-lookup"><span data-stu-id="f2f4b-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2f4b-129">Esc</span><span class="sxs-lookup"><span data-stu-id="f2f4b-129">Esc</span></span></td>
<td><span data-ttu-id="f2f4b-130">Sluit de zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="f2f4b-131">Pijl omhoog en pijl omlaag</span><span class="sxs-lookup"><span data-stu-id="f2f4b-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="f2f4b-132">PgUp en PgDn</span><span class="sxs-lookup"><span data-stu-id="f2f4b-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="f2f4b-133">Home en End</span><span class="sxs-lookup"><span data-stu-id="f2f4b-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="f2f4b-134">Verplaatsen naar de volgende of vorige waarde in de lijsten, naar de vorige of volgende groep waarden of naar het eerste of laatste element in de zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f2f4b-135">Scheidingsteken voor rekeningschema</span><span class="sxs-lookup"><span data-stu-id="f2f4b-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="f2f4b-136">Pijl naar rechts en pijl naar links</span><span class="sxs-lookup"><span data-stu-id="f2f4b-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="f2f4b-137">Verplaatsen naar het volgende of vorige segment.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2f4b-138">Tabblad</span><span class="sxs-lookup"><span data-stu-id="f2f4b-138">Tab</span></span></td>
<td><span data-ttu-id="f2f4b-139">Naar het volgende veld in het raster verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2f4b-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="f2f4b-140">Alt+W</span></span></td>
<td><span data-ttu-id="f2f4b-141">Schakelen tussen <strong>Alles weergeven</strong> en <strong>Alleen geldige weergeven</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2f4b-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>




