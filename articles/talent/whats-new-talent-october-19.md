---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (16 oktober 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 13e89faa3f8470125010ccdb40a6f01c0a9c4fe7
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008772"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-19-2018"></a><span data-ttu-id="27d37-103">Wat is nieuw of gewijzigd in Dynamics 365 Talent: Core HR (19 oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="27d37-103">What's new or changed in Dynamics 365 Talent: Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="27d37-104">**Build 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="27d37-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="27d37-105">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.</span><span class="sxs-lookup"><span data-stu-id="27d37-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="27d37-106">Managers toestaan verlofaanvragen bij te werken</span><span class="sxs-lookup"><span data-stu-id="27d37-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="27d37-107">Verlofaanvragen van werknemers moeten mogelijk worden bijgewerkt nadat ze zijn goedgekeurd via de workflow.</span><span class="sxs-lookup"><span data-stu-id="27d37-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="27d37-108">In veel gevallen brengt de manager deze updates aan namens de werknemer.</span><span class="sxs-lookup"><span data-stu-id="27d37-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="27d37-109">Deze nieuwe functie biedt de mogelijkheid voor managers om verlof bij te werken of verlofaanvragen te annuleren namens hun werknemers.</span><span class="sxs-lookup"><span data-stu-id="27d37-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="27d37-110">Deze mogelijkheid wordt bepaald door de parameter **Werken namens** die kan worden ingesteld op de pagina **Parameters personeel**.</span><span class="sxs-lookup"><span data-stu-id="27d37-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="27d37-111">HR-managers toestaan verlofaanvragen bij te werken</span><span class="sxs-lookup"><span data-stu-id="27d37-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="27d37-112">Net als bij de bovenstaande functie moeten verlofaanvragen van werknemers mogelijk door HR worden bijgewerkt nadat ze eerder zijn goedgekeurd via de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="27d37-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="27d37-113">Deze functie biedt de mogelijkheid voor HR-gebruikers om verlofaanvragen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="27d37-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="27d37-114">De mogelijkheid wordt ingeschakeld in het werkgebied **Mensen** en op de pagina **Medewerker** met behulp van een nieuwe optie genaamd **Tijd vrijaf weergeven**.</span><span class="sxs-lookup"><span data-stu-id="27d37-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="27d37-115">Op deze pagina's kunnen HR-gebruikers aanvragen weergeven en verloftransacties bijwerken, net zoals managers deze acties kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="27d37-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="27d37-116">Dit is de beveiligingsfunctie die toegang tot deze functionaliteit bepaalt:</span><span class="sxs-lookup"><span data-stu-id="27d37-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="27d37-117">Functie: medewerkerspecifieke verlof- en verzuimprocessen onderhouden.</span><span class="sxs-lookup"><span data-stu-id="27d37-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="27d37-118">Bevoegdheid: verlof- en verzuimaanvragen onderhouden voor alle medewerkers.</span><span class="sxs-lookup"><span data-stu-id="27d37-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="27d37-119">Andere wijzigingen</span><span class="sxs-lookup"><span data-stu-id="27d37-119">Other changes</span></span>
<span data-ttu-id="27d37-120">De volgende updates zijn aangebracht in deze release:</span><span class="sxs-lookup"><span data-stu-id="27d37-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="27d37-121">Wijzigingen in acties voor het aanstellen van medewerkers, zodat ze niet meer "vastzitten" in de status **Workflow voltooid**.</span><span class="sxs-lookup"><span data-stu-id="27d37-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="27d37-122">Dienstverbandrecord kan nu worden gemaakt zonder een begindatum van het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="27d37-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="27d37-123">De registratiedatum van Dynamics 365 Talent voor een cursus die wordt weergegeven in de Werknemers-self-service past nu de tijdzoneverschuiving op de datum toe.</span><span class="sxs-lookup"><span data-stu-id="27d37-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="27d37-124">Excel-bestanden kunnen meerdere keren worden geïmporteerd zonder fouten met **Werknemersentiteit**.</span><span class="sxs-lookup"><span data-stu-id="27d37-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="27d37-125">Bekend probleem</span><span class="sxs-lookup"><span data-stu-id="27d37-125">Known issue</span></span>

- <span data-ttu-id="27d37-126">**Probleem**: bij het toevoegen van een nieuwe bijlage aan een werknemer zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="27d37-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="27d37-127">**Tijdelijke oplossing:** voordat u de bijlagepagina opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="27d37-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="27d37-128">Als de feitenvakken worden gesloten wanneer de pagina **Werknemer** wordt geladen, worden de bijlageknoppen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="27d37-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="27d37-129">(Dit probleem wordt opgelost in de volgende platformupdate.)</span><span class="sxs-lookup"><span data-stu-id="27d37-129">(This issue will be fixed in the next platform update.)</span></span>
