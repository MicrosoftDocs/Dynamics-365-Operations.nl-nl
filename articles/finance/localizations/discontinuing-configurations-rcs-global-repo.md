---
title: Configuraties stopzetten in de globale opslagplaats van RCS
description: In dit onderwerp wordt beschreven hoe u stopt met de configuraties in de globale opslagplaats van RFS.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 25ad0744e7c3320505c13c465d440b6a364da47c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840287"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="91c3a-103">Configuraties stopzetten in de globale opslagplaats van RCS</span><span class="sxs-lookup"><span data-stu-id="91c3a-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91c3a-104">In dit onderwerp wordt beschreven hoe u stopt met een configuratie in de globale opslagplaats van RFS.</span><span class="sxs-lookup"><span data-stu-id="91c3a-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="91c3a-105">Voorheen was het alleen mogelijk om configuraties te verwijderen die niet meer nodig waren.</span><span class="sxs-lookup"><span data-stu-id="91c3a-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="91c3a-106">Nu kunt u echter een vrijgegeven configuratie als **Beëindigd** markeren in de globale opslagplaats van RCS.</span><span class="sxs-lookup"><span data-stu-id="91c3a-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="91c3a-107">Met deze functionaliteit kunt u ook het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="91c3a-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="91c3a-108">Vooraf meldingen opgeven wanneer een configuratie volgens de planning moet worden beëindigd.</span><span class="sxs-lookup"><span data-stu-id="91c3a-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="91c3a-109">Toepasselijke gegevens over de vervangingsconfiguratie opnemen.</span><span class="sxs-lookup"><span data-stu-id="91c3a-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="91c3a-110">Een datum **Ondersteund tot** instellen voor de specifieke configuratie om de gebruiker te informeren wanneer deze wordt beëindigd.</span><span class="sxs-lookup"><span data-stu-id="91c3a-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="91c3a-111">Wanneer u een configuratieversie beëindigt, kunt u de volgende optionele informatie opgeven:</span><span class="sxs-lookup"><span data-stu-id="91c3a-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="91c3a-112">**Vervangingsconfiguratie**</span><span class="sxs-lookup"><span data-stu-id="91c3a-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="91c3a-113">**Versie van vervangingsconfiguratie**</span><span class="sxs-lookup"><span data-stu-id="91c3a-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="91c3a-114">**Vrije-tekstnotitie**: gebruik dit veld als u documentatiekoppelingen of verwijzingen wilt leveren</span><span class="sxs-lookup"><span data-stu-id="91c3a-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="91c3a-115">**Ondersteund tot**: dit veld bevat de voorgestelde datum tot wanneer de huidige configuratie/versie wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="91c3a-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="91c3a-116">Deze datum moet handmatig worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="91c3a-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="91c3a-117">Als u de configuratie wilt beëindigen, voltooit u de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="91c3a-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="91c3a-118">Selecteer of u wilt één versie of alle versies met dezelfde instellingen in één bewerking wilt beëindigen door **Alle versies** in te stellen op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="91c3a-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="91c3a-119">Stel de parameter **Beëindigen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="91c3a-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="91c3a-120">Selecteer **OK** om de configuraties te beëindigen.</span><span class="sxs-lookup"><span data-stu-id="91c3a-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="91c3a-121">Het veld **Einddatum** wordt ingevuld wanneer u de wijzigingen opslaat.</span><span class="sxs-lookup"><span data-stu-id="91c3a-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Configuratiegegevens stopzetten](media/Discontinue-details-2.png)
  
<span data-ttu-id="91c3a-123">U kunt de configuratie op elk moment terugdraaien naar **Gedeeld** of beëindigingsgegevens aanpassen.</span><span class="sxs-lookup"><span data-stu-id="91c3a-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="91c3a-124">Als u een configuratie deelt, geeft u de datum **Ondersteund tot** en alle andere informatie met betrekking tot de beëindiging op om aan te geven dat u toekomstige beëindiging plant.</span><span class="sxs-lookup"><span data-stu-id="91c3a-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="91c3a-125">Als u informatie wilt delen over een geplande beëindiging voordat de configuratie daadwerkelijk wordt beëindigd, kan de gebruiker alle velden die zijn gerelateerd aan de vervanging vooraf invullen, maar de parameter **Beëindigen** op **Nee** laten staan.</span><span class="sxs-lookup"><span data-stu-id="91c3a-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="91c3a-126">Bij beëindiging worden bewerkingen met configuraties niet beperkt.</span><span class="sxs-lookup"><span data-stu-id="91c3a-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="91c3a-127">U kunt de configuraties blijven importeren, uitvoeren of afleiden. Deze velden dienen ter informatie.</span><span class="sxs-lookup"><span data-stu-id="91c3a-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="91c3a-128">Finance ondersteunt het weergeven van deze informatie vanaf versie 10.0.14</span><span class="sxs-lookup"><span data-stu-id="91c3a-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="91c3a-129">Vanaf versie 10.0.14 ondersteunt Dynamics 365 Finance het weergeven van beëindigingsinformatie.</span><span class="sxs-lookup"><span data-stu-id="91c3a-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="91c3a-130">Op de pagina **Globale opslagplaats** kunt u actuele informatie weergeven met betrekking tot beëindiging.</span><span class="sxs-lookup"><span data-stu-id="91c3a-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="91c3a-131">Configuraties die zijn beëindigd worden standaard uitgefilterd.</span><span class="sxs-lookup"><span data-stu-id="91c3a-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="91c3a-132">Op de pagina **Geïmporteerde configuraties** (ERSolutionTable) worden configuraties weergegeven die al waren beëindigd toen zij werden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="91c3a-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="91c3a-133">Voor configuraties die zijn beëindigd na het importeren, kan de beëindigingsinformatie worden gesynchroniseerd door de taak **Updates van configuraties importeren** uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="91c3a-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


