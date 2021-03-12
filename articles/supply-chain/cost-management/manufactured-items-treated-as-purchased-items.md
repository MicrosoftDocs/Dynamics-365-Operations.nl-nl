---
title: Producten instellen die kunnen worden geproduceerd of kunnen worden aangeschaft
description: 'Producten kunnen verschillende bronnen hebben: ze kunnen worden geproduceerd of worden aangeschaft (ingekocht). Dit artikel beschrijft sommige algemene punten om na te gaan wanneer u producten configureert om multi-sourcing te ondersteunen.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7acf4952c1dbb33f4ec615d1ecb9d508a9e7b980
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967503"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="e7049-104">Producten instellen die kunnen worden geproduceerd of kunnen worden aangeschaft</span><span class="sxs-lookup"><span data-stu-id="e7049-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7049-105">Producten kunnen verschillende bronnen hebben: ze kunnen worden geproduceerd of worden aangeschaft (ingekocht).</span><span class="sxs-lookup"><span data-stu-id="e7049-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="e7049-106">Dit artikel beschrijft sommige algemene punten om na te gaan wanneer u producten configureert om multi-sourcing te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="e7049-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="e7049-107">Multi-sourcing wordt meestal gebruikt voor een ingekocht artikel dat soms wordt gefabriceerd, of wanneer een artikel dat hoofdzakelijk een gefabriceerd artikel was, is gewijzigd zodat het nu in eerste instantie een ingekocht artikel is.</span><span class="sxs-lookup"><span data-stu-id="e7049-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="e7049-108">Het artikel wordt eerst aangemerkt als een gefabriceerd artikel, zodat de stuklijsten en routegegevens kunnen worden gedefinieerd en om de productieorders voor het artikel te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="e7049-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="e7049-109">Het productietype moet worden ingesteld op **Stuklijst** (of voor procesproductie **Formule** of **Co-product**).</span><span class="sxs-lookup"><span data-stu-id="e7049-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="e7049-110">Wanneer u standaardkosten gebruikt, kan de kostprijsrecord voor het gefabriceerde artikel worden berekend.</span><span class="sxs-lookup"><span data-stu-id="e7049-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="e7049-111">De kostprijsrecord komt echter mogelijk niet overeen met de gewenste standaardkosten voor inkoopdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="e7049-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="e7049-112">In dat geval moeten de standaardkosten handmatig voor de artikelkostprijsrecord worden ingevoerd en geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="e7049-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="e7049-113">Overweeg voor de kostenberekening het gebruik van een speciale stuklijst en route die de leveringsmix van het product in de loop van een boekperiode vertegenwoordigen, om de afwijkingen in de loop der tijd te minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="e7049-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="e7049-114">Bovendien kan een artikel dat op de ene site wordt gefabriceerd, naar een andere worden overgebracht.</span><span class="sxs-lookup"><span data-stu-id="e7049-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="e7049-115">Dat betekent dat de kosten van het artikel handmatig moeten worden ingevoerd en geactiveerd voor de site waarnaar het artikel wordt overgebracht.</span><span class="sxs-lookup"><span data-stu-id="e7049-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="e7049-116">Als u een gefabriceerd artikel gebruikt als onderdeel van een product op hoger niveau, moeten de kosten van dat onderdeel worden behandeld als een ingekocht product.</span><span class="sxs-lookup"><span data-stu-id="e7049-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="e7049-117">Deze richtlijn geldt, ongeacht of de kosten van het onderdeel zijn berekend of handmatig ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="e7049-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="e7049-118">Dat wil zeggen dat bij een stuklijstberekening de artikelkosten moeten worden behandeld als een ingekocht onderdeel in plaats van de stuklijst- en routegegevens van het artikel te gebruiken om kosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="e7049-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="e7049-119">U kunt voorkomen dat deze berekening wordt uitgevoerd door de markering **Explosie stoppen** in te schakelen die is ingesloten in de stuklijstberekeningsgroep die aan het artikel is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e7049-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="e7049-120">U kunt explosievereisten buiten hoofdplanningsberekeningen via het artikel voorkomen door de time fence van explosie op 0 (nul) dagen in te stellen in artikelbehoefteplanning of in de dekkingsgroep.</span><span class="sxs-lookup"><span data-stu-id="e7049-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="e7049-121">Bij de hoofdplanningsberekening wordt het artikel dan behandeld als ingekocht artikel en worden er geen verdere berekeningen uitgevoerd voor de stuklijst- en routegegevens van het artikel.</span><span class="sxs-lookup"><span data-stu-id="e7049-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>





