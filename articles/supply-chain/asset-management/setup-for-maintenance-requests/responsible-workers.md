---
title: Verantwoordelijke onderhoudsmedewerkers
description: In dit onderwerp wordt uitgelegd hoe u verantwoordelijke onderhoudsmedewerkers instelt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 137ed393f28131262584d5a2ae414092b124ea0e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021950"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="926c3-103">Verantwoordelijke onderhoudsmedewerkers</span><span class="sxs-lookup"><span data-stu-id="926c3-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="926c3-104">Verantwoordelijke onderhoudsmedewerkers kunnen worden gerelateerd aan activumtypen, activa, functionele locaties, categorieën met typen onderhoudstaken, typen onderhoudstaken, varianten op typen onderhoudstaken en transacties.</span><span class="sxs-lookup"><span data-stu-id="926c3-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="926c3-105">Ze kunnen worden gebruikt met werkorders en onderhoudsverzoeken om een voorkeur aan te geven voor de onderhoudsmedewerkers die verantwoordelijk moeten zijn voor een werkorder.</span><span class="sxs-lookup"><span data-stu-id="926c3-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="926c3-106">(Deze onderhoudsmedewerkers zijn echter niet noodzakelijkerwijs dezelfde medewerkers die zijn gepland om de werkorder uit te voeren.) Het gebruik van deze functionaliteit is optioneel.</span><span class="sxs-lookup"><span data-stu-id="926c3-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="926c3-107">Deze kan bijvoorbeeld worden gebruikt om verantwoordelijke medewerkers of medewerkersgroepen voor specifieke werktypen of werkgebieden te selecteren.</span><span class="sxs-lookup"><span data-stu-id="926c3-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="926c3-108">Tijdens de levenscyclus van een werkorder of een onderhoudsverzoek kunnen verantwoordelijke onderhoudsmedewerkers worden gewijzigd of bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="926c3-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="926c3-109">Deze wijziging of update kan worden gerelateerd aan bijvoorbeeld een wijziging in de levenscyclusstatus van het onderhoudsverzoek of de levenscyclusstatus van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="926c3-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="926c3-110">De instellingen op de pagina **Verantwoordelijke onderhoudsmedewerkers** worden *niet* gebruikt tijdens de planning van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="926c3-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="926c3-111">In Activabeheer kunt u ook *voorkeuren* opgeven voor onderhoudsmedewerkers die mogelijk aan werkorders worden toegewezen tijdens de planning van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="926c3-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="926c3-112">Voordat u verantwoordelijke onderhoudsmedewerkers kunt instellen, moet u de medewerkers en onderhoudsmedewerkersgroepen instellen die beschikbaar moeten zijn voor selectie.</span><span class="sxs-lookup"><span data-stu-id="926c3-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="926c3-113">Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor informatie over het instellen van medewerkers en onderhoudswerknemersgroepen.</span><span class="sxs-lookup"><span data-stu-id="926c3-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="926c3-114">Verantwoordelijke onderhoudsmedewerkers instellen</span><span class="sxs-lookup"><span data-stu-id="926c3-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="926c3-115">Selecteer **Activabeheer** \> **Instellen** \> **Medewerkers** \> **Verantwoordelijke onderhoudsmedewerkers**</span><span class="sxs-lookup"><span data-stu-id="926c3-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="926c3-116">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="926c3-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="926c3-117">Maak eerst standaardinstellingen voor een verantwoordelijke onderhoudsmedewerker of verantwoordelijke medewerkersgroep, waarbij u alleen het veld **Verantwoordelijke onderhoudsmedewerkersgroep** en/of het veld **Verantwoordelijke medewerker** instelt.</span><span class="sxs-lookup"><span data-stu-id="926c3-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="926c3-118">Laat de overige velden leeg.</span><span class="sxs-lookup"><span data-stu-id="926c3-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="926c3-119">Deze standaardinstellingen worden gebruikt tijdens de planning van de werkorder als er geen andere, specifiekere combinatie overeenkomt met de inhoud van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="926c3-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="926c3-120">Wanneer er tijdens het maken van een onderhoudsverzoek een verantwoordelijke onderhoudsmedewerker of een verantwoordelijke onderhoudsmedewerkersgroep beschikbaar is gesteld voor selectie op de pagina **Alle onderhoudsverzoeken**, doorloopt Activabeheer alle verantwoordelijke onderhoudsmedewerkersrecords om te controleren op een mogelijke overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="926c3-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="926c3-121">De meest specifieke combinatie wordt altijd als eerste gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="926c3-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="926c3-122">Dat wil zeggen dat Activabeheer eerst controleert op een overeenkomst voor het veld **Handel**.</span><span class="sxs-lookup"><span data-stu-id="926c3-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="926c3-123">Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Variant op type onderhoudstaak**.</span><span class="sxs-lookup"><span data-stu-id="926c3-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="926c3-124">Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Type onderhoudstaak** enzovoort.</span><span class="sxs-lookup"><span data-stu-id="926c3-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="926c3-125">Zoals u aan de indeling van de pagina ziet, betekent dit gedrag dat Activabeheer, om de meest specifieke combinatie te vinden, elke record van rechts naar links controleert op een overeenkomst (eerst **Handel**, vervolgens **Variant op type onderhoudstaak**, **Type onderhoudstaak**, **Categorie van type onderhoudstaak**, **Functionele locatie**, **Activum** en tot slot **Activumtype**).</span><span class="sxs-lookup"><span data-stu-id="926c3-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="926c3-126">Als er geen overeenkomst wordt gevonden, wordt in deze zeven velden de standaardrecord zonder selecties gebruikt.</span><span class="sxs-lookup"><span data-stu-id="926c3-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="926c3-127">In de volgende afbeelding ziet u een voorbeeld van de pagina **Verantwoordelijke onderhoudsmedewerkers**.</span><span class="sxs-lookup"><span data-stu-id="926c3-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Pagina Verantwoordelijke onderhoudsmedewerkers](media/08-setup-for-requests.png)
