---
title: Voorraadlabeltelling
description: Dit onderwerp bevat informatie over labeltelling, dat u gebruikt om de werkelijke inhoud van een magazijn te vergelijken met de voorhanden voorraad.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd10c24045fae5db00e88f3b84d4dea7b2c82c37
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571088"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="034e4-103">Voorraadlabeltelling</span><span class="sxs-lookup"><span data-stu-id="034e4-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="034e4-104">Dit onderwerp bevat informatie over labeltelling, dat u gebruikt om de werkelijke inhoud van een magazijn te vergelijken met de voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="034e4-104">This topic provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="034e4-105">Met behulp van regels op de pagina **Telling labels** plaatst u een labelnummer op elk voorraadartikel, zoals een getal tussen 1 en 500.</span><span class="sxs-lookup"><span data-stu-id="034e4-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="034e4-106">Tijdens de telling voert u het artikelnummer en de hoeveelheid op een bijbehorend label in.</span><span class="sxs-lookup"><span data-stu-id="034e4-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="034e4-107">Dit label kan vervolgens als basis voor invoer in de labeltellijst worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="034e4-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="034e4-108">Nadat u de labeltellijst hebt geboekt, wordt een nieuwe tellijst gemaakt op de pagina **Tellen**.</span><span class="sxs-lookup"><span data-stu-id="034e4-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="034e4-109">De nieuwe lijst wordt gebaseerd op de regels van de labeltellijst die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="034e4-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="034e4-110">Als u een labeltelling op artikelen uitvoert op basis van een specifieke voorraaddimensie, selecteert u de dimensie op de pagina **Dimensie weergeven** die wordt weergegeven wanneer u de labeltellijst maakt.</span><span class="sxs-lookup"><span data-stu-id="034e4-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="034e4-111">Als u bijvoorbeeld artikelen in een specifiek magazijn wilt tellen, schakelt u het selectievakje **Magazijn** in.</span><span class="sxs-lookup"><span data-stu-id="034e4-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="034e4-112">Als de schuifregelaar **Artikelen vergrendelen tijdens telling** op de pagina **Parameters voor voorraad- en magazijnbeheer** wordt geselecteerd, kunnen artikelen niet fysiek tijdens het tellen worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="034e4-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="034e4-113">Artikelen in labeltellijsten worden echter niet vergrendeld tijdens het tellen.</span><span class="sxs-lookup"><span data-stu-id="034e4-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="034e4-114">Voorraadtransacties worden pas gemaakt als labeltelregels worden geboekt en overgeboekt naar een tellijst.</span><span class="sxs-lookup"><span data-stu-id="034e4-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="034e4-115">Als labels willekeurig worden ingevoerd en u wilt bepalen of er labels ontbreken, klikt u op de kolomkoptekst **Label** om de regels op label te sorteren.</span><span class="sxs-lookup"><span data-stu-id="034e4-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="034e4-116">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="034e4-116">Additional resources</span></span>

[<span data-ttu-id="034e4-117">Cyclustelling</span><span class="sxs-lookup"><span data-stu-id="034e4-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
