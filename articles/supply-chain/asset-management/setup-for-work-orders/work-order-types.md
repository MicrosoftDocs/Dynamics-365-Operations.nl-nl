---
title: Werkordertypen
description: In dit onderwerp wordt uitgelegd hoe u werkordertypen instelt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425547"
---
# <a name="work-order-types"></a><span data-ttu-id="c4749-103">Werkordertypen</span><span class="sxs-lookup"><span data-stu-id="c4749-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c4749-104">Werkordertypen worden gebruikt om werkorders te categoriseren.</span><span class="sxs-lookup"><span data-stu-id="c4749-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="c4749-105">Zo kunnen er typen werkorders zijn die betrekking hebben op preventief onderhoud of op correctief onderhoud.</span><span class="sxs-lookup"><span data-stu-id="c4749-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="c4749-106">Een werkordertype definieert een aansluiting met een levenscyclusmodel van een werkorder.</span><span class="sxs-lookup"><span data-stu-id="c4749-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="c4749-107">Met een levenscyclusmodel voor werkorders worden de statuswaarden voor levenscyclusmodellen voor werkorders gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c4749-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="c4749-108">(Voorbeelden van statuswaarden voor werkorders zijn **Gemaakt**, **Onderhanden** en **Voltooid**.)</span><span class="sxs-lookup"><span data-stu-id="c4749-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="c4749-109">Zie [Levenscyclusstatussen van werkorder](work-order-lifecycle-states.md)voor meer informatie over levenscyclusstatussen van werkorders en projectfasen.</span><span class="sxs-lookup"><span data-stu-id="c4749-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="c4749-110">Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Werkordertypen**.</span><span class="sxs-lookup"><span data-stu-id="c4749-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="c4749-111">Selecteer **Nieuw** om een levenscyclustype te maken.</span><span class="sxs-lookup"><span data-stu-id="c4749-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="c4749-112">Voer in het veld **Werkordertype** een id in voor het werkordertype.</span><span class="sxs-lookup"><span data-stu-id="c4749-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="c4749-113">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="c4749-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="c4749-114">Selecteer in het veld **Levenscyclusmodel van werkorder** een model voor de levenscyclus.</span><span class="sxs-lookup"><span data-stu-id="c4749-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="c4749-115">Stel de optie **Eén onderhoudsmedewerker** in op **Ja** als alle werkordertaken die zijn gerelateerd aan een werkorder van dit type, moeten worden gepland voor dezelfde onderhoudsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="c4749-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="c4749-116">Selecteer in het veld **Kostentype** uit **Corrigerend**, **Preventief** of **Investering**.</span><span class="sxs-lookup"><span data-stu-id="c4749-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="c4749-117">Alle werkordertaken op een werkorder moeten hetzelfde kostentype hebben.</span><span class="sxs-lookup"><span data-stu-id="c4749-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="c4749-118">Stel in de sectie **Verplicht** de relevante opties in op **Ja** om aan te geven welke fout- of uitvaltijd-gerelateerde informatie wordt toegevoegd aan een werkorder van dit type.</span><span class="sxs-lookup"><span data-stu-id="c4749-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4749-119">De opties in de sectie **Verplicht** zijn gerelateerd aan de opties op het sneltabblad **Valideren** van de pagina **Levenscyclusstatus van werkorder** (**Activabeheer** \> **Instellen** \> **Werkorders** \> **Levenscyclusstatussen**).</span><span class="sxs-lookup"><span data-stu-id="c4749-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="c4749-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c4749-120">Select **Save**.</span></span>

![Werkordertypen](media/16-setup-for-work-orders.png)
