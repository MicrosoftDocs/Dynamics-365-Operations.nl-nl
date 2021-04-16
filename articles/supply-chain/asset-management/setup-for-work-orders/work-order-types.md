---
title: Werkordertypen
description: In dit onderwerp wordt uitgelegd hoe u werkordertypen instelt in Activabeheer.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6bdc9d226d8e1aa6960cac38b95b0245e46ee1ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825585"
---
# <a name="work-order-types"></a><span data-ttu-id="95c97-103">Werkordertypen</span><span class="sxs-lookup"><span data-stu-id="95c97-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="95c97-104">Werkordertypen worden gebruikt om werkorders te categoriseren.</span><span class="sxs-lookup"><span data-stu-id="95c97-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="95c97-105">Zo kunnen er typen werkorders zijn die betrekking hebben op preventief onderhoud of op correctief onderhoud.</span><span class="sxs-lookup"><span data-stu-id="95c97-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="95c97-106">Een werkordertype definieert een aansluiting met een levenscyclusmodel van een werkorder.</span><span class="sxs-lookup"><span data-stu-id="95c97-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="95c97-107">Met een levenscyclusmodel voor werkorders worden de statuswaarden voor levenscyclusmodellen voor werkorders gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="95c97-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="95c97-108">(Voorbeelden van statuswaarden voor werkorders zijn **Gemaakt**, **Onderhanden** en **Voltooid**.)</span><span class="sxs-lookup"><span data-stu-id="95c97-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="95c97-109">Zie [Levenscyclusstatussen van werkorder](work-order-lifecycle-states.md)voor meer informatie over levenscyclusstatussen van werkorders en projectfasen.</span><span class="sxs-lookup"><span data-stu-id="95c97-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="95c97-110">Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Werkordertypen**.</span><span class="sxs-lookup"><span data-stu-id="95c97-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="95c97-111">Selecteer **Nieuw** om een levenscyclustype te maken.</span><span class="sxs-lookup"><span data-stu-id="95c97-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="95c97-112">Voer in het veld **Werkordertype** een id in voor het werkordertype.</span><span class="sxs-lookup"><span data-stu-id="95c97-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="95c97-113">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="95c97-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="95c97-114">Selecteer in het veld **Levenscyclusmodel van werkorder** een model voor de levenscyclus.</span><span class="sxs-lookup"><span data-stu-id="95c97-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="95c97-115">Stel de optie **Eén onderhoudsmedewerker** in op **Ja** als alle werkordertaken die zijn gerelateerd aan een werkorder van dit type, moeten worden gepland voor dezelfde onderhoudsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="95c97-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="95c97-116">Selecteer in het veld **Kostentype** uit **Corrigerend**, **Preventief** of **Investering**.</span><span class="sxs-lookup"><span data-stu-id="95c97-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="95c97-117">Alle werkordertaken op een werkorder moeten hetzelfde kostentype hebben.</span><span class="sxs-lookup"><span data-stu-id="95c97-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="95c97-118">Stel in de sectie **Verplicht** de relevante opties in op **Ja** om aan te geven welke fout- of uitvaltijd-gerelateerde informatie wordt toegevoegd aan een werkorder van dit type.</span><span class="sxs-lookup"><span data-stu-id="95c97-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="95c97-119">De opties in de sectie **Verplicht** zijn gerelateerd aan de opties op het sneltabblad **Valideren** van de pagina **Levenscyclusstatus van werkorder** (**Activabeheer** \> **Instellen** \> **Werkorders** \> **Levenscyclusstatussen**).</span><span class="sxs-lookup"><span data-stu-id="95c97-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="95c97-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="95c97-120">Select **Save**.</span></span>

![Werkordertypen](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]