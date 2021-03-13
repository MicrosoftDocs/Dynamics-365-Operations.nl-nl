---
title: Overzicht van Levenscyclus van productieorder
description: Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel. De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum. Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28ef1da29b38354d7ccaad56fb036f21d8c9ff15
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011167"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="f7287-105">Overzicht van Levenscyclus van productieorder</span><span class="sxs-lookup"><span data-stu-id="f7287-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7287-106">Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="f7287-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="f7287-107">De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum.</span><span class="sxs-lookup"><span data-stu-id="f7287-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="f7287-108">Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren.</span><span class="sxs-lookup"><span data-stu-id="f7287-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="f7287-109">Een productieorder doorloopt fasen van de productielevenscyclus.</span><span class="sxs-lookup"><span data-stu-id="f7287-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="f7287-110">Bij het maken wordt aan een order de status **Gemaakt** toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f7287-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="f7287-111">Bij het voltooien wordt aan een order de status **Beëindigd** toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f7287-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="f7287-112">Met een parameterinstelling in elke fase kan een gebruiker elke stap configureren.</span><span class="sxs-lookup"><span data-stu-id="f7287-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="f7287-113">De instelling kan worden opgegeven voor één gebruiker of voor alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="f7287-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="f7287-114">De productiestuklijst en de productieroute zijn de belangrijkste entiteiten van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="f7287-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="f7287-115">Ze worden naar de productieorder gekopieerd op basis van het geselecteerde artikel en de hoeveelheid die gaan worden geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="f7287-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="f7287-116">Voordat de productieorder is gestart, kunnen de productiestuklijst en route worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="f7287-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="f7287-117">Een productieorder kan in de volgende scenario's worden gemaakt:</span><span class="sxs-lookup"><span data-stu-id="f7287-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="f7287-118">Gemaakt door hoofdplanningsuitvoering op basis van de vraag naar materiaal.</span><span class="sxs-lookup"><span data-stu-id="f7287-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="f7287-119">Rechtstreeks gemaakt van een verkooporderregel of wanneer een productieorder van een hoger niveau wordt gemaakt en geraamd (getraceerd aanbod).</span><span class="sxs-lookup"><span data-stu-id="f7287-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="f7287-120">Handmatig gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f7287-120">Created manually.</span></span>




