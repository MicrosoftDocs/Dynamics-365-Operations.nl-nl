---
title: Typen onderhoudsverzoeken
description: In dit onderwerp wordt uitgelegd hoe u typen onderhoudsverzoeken instelt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56a83457097b64d195eec53000b29b2f16251772
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019324"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="70874-103">Typen onderhoudsverzoeken</span><span class="sxs-lookup"><span data-stu-id="70874-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="70874-104">Typen onderhoudsverzoeken worden gebruikt voor het categoriseren van onderhoudsverzoeken.</span><span class="sxs-lookup"><span data-stu-id="70874-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="70874-105">Zo kunnen er typen onderhoudsverzoeken zijn die betrekking hebben op preventief onderhoud en correctief onderhoud.</span><span class="sxs-lookup"><span data-stu-id="70874-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="70874-106">Of u hebt een speciaal type onderhoudsverzoek dat wordt gebruikt voor het beheren van reparatie van activa (depotreparatie).</span><span class="sxs-lookup"><span data-stu-id="70874-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="70874-107">Een type onderhoudsverzoek definieert de aansluiting met een levenscyclusstatusgroep met onderhoudsverzoeken (onderhoudslevenscyclusmodel).</span><span class="sxs-lookup"><span data-stu-id="70874-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="70874-108">Levenscyclusmodellen voor onderhoudsverzoeken bepalen welke levenscyclusstatussen voor een onderhoudsverzoek kunnen worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="70874-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="70874-109">(Voorbeelden van levenscyclusstatussen voor onderhoudsverzoeken **Gemaakt**, **Actief** en **Beëindigd**.)</span><span class="sxs-lookup"><span data-stu-id="70874-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="70874-110">Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudsverzoeken** \> **Typen onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="70874-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="70874-111">Selecteer **Nieuw** als u een type onderhoudsverzoek wilt maken.</span><span class="sxs-lookup"><span data-stu-id="70874-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="70874-112">Voer in het veld **Type onderhoudsverzoek** een id in voor het type onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="70874-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="70874-113">Voer in het veld **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="70874-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="70874-114">Ga naar het sneltabblad **Algemeen** en selecteer in het veld **Levenscyclusmodel voor onderhoudsverzoek** een levenscyclusmodel voor het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="70874-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="70874-115">Selecteer een type werkorder in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="70874-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="70874-116">Wanneer een onderhoudsverzoek wordt geconverteerd naar een werkorder, haalt de werkorder automatisch het werkordertype op dat is gerelateerd aan het type onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="70874-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="70874-117">In de volgende afbeelding ziet u een voorbeeld van de pagina **Typen onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="70874-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Pagina Typen onderhoudsverzoeken](media/07-setup-for-requests.png)
