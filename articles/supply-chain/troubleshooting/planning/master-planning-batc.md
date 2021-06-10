---
title: U kunt hoofdplanningsartikelen niet filteren op de gerelateerde waarden van de behoefteplanningsgroep
description: U kunt hoofdplanningsartikelen niet filteren op de gerelateerde waarden van de behoefteplanningsgroep.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049461"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="a05fd-103">U kunt hoofdplanningsartikelen niet filteren op de gerelateerde waarden van de behoefteplanningsgroep</span><span class="sxs-lookup"><span data-stu-id="a05fd-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="a05fd-104">KB-nummer: 4612572</span><span class="sxs-lookup"><span data-stu-id="a05fd-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="a05fd-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="a05fd-105">Symptoms</span></span>

<span data-ttu-id="a05fd-106">U wilt de artikelen filteren die worden opgenomen in een batchtaak voor de hoofdplanning op basis van de waarden van gerelateerde records uit de tabel voor artikelbehoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="a05fd-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="a05fd-107">(U wilt artikelen bijvoorbeeld filteren op de waarde die ervoor is ingesteld bij **Leverancier** en/of **Behoefteplanningsgroep**).</span><span class="sxs-lookup"><span data-stu-id="a05fd-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="a05fd-108">Met de filterinstellingen voor de batchtaak kunt u een join maken vanuit de tabel **Artikelen** naar de tabel **Artikelbehoefteplanning** en vervolgens veldwaarden opgeven vanuit de tabel voor artikelbehoefteplanning in uw query.</span><span class="sxs-lookup"><span data-stu-id="a05fd-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="a05fd-109">Nadat u deze instelling hebt voltooid, worden echter nog steeds geplande orders gemaakt voor de volledige artikelbehoefteplanning, niet alleen voor de artikelen die overeenkomen met de opgegeven veldwaarden uit de tabel voor artikelbehoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="a05fd-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="a05fd-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="a05fd-110">Resolution</span></span>

<span data-ttu-id="a05fd-111">Het batchtaakfilter kan alleen op artikelen filteren.</span><span class="sxs-lookup"><span data-stu-id="a05fd-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="a05fd-112">Hoewel u een join kunt toevoegen aan de tabel **Artikelbehoefteplanning**, zijn filterinstellingen die u voor die tabel maakt, niet van invloed op de query-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="a05fd-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="a05fd-113">Tijdens de uitvoering wordt de planning uitgevoerd voor alle behoefteplanningsgroepen en alle variaties die de gefilterde artikelen hebben.</span><span class="sxs-lookup"><span data-stu-id="a05fd-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="a05fd-114">Nadat een artikel al is opgenomen in de uitvoering, zijn behoefteplanningsgroepen die zijn opgenomen in het artikelfilter, niet van invloed op de planningsuitvoer.</span><span class="sxs-lookup"><span data-stu-id="a05fd-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
