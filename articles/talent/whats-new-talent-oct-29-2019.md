---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (29 oktober 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773872"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="45d3f-103">Wat is nieuw of gewijzigd in Dynamics 365 Talent (29 oktober 2019)</span><span class="sxs-lookup"><span data-stu-id="45d3f-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="45d3f-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="45d3f-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="45d3f-105">Wijzigingen in Attract</span><span class="sxs-lookup"><span data-stu-id="45d3f-105">Changes in Attract</span></span>

<span data-ttu-id="45d3f-106">Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="45d3f-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="45d3f-107">Wijzigingen in Onboard</span><span class="sxs-lookup"><span data-stu-id="45d3f-107">Changes in Onboard</span></span>

<span data-ttu-id="45d3f-108">Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="45d3f-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="45d3f-109">Wijzigingen in Core HR</span><span class="sxs-lookup"><span data-stu-id="45d3f-109">Changes in Core HR</span></span>

<span data-ttu-id="45d3f-110">Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="45d3f-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="45d3f-111">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="45d3f-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="45d3f-112">Partijen zonder rollen verwijderen moet standaard zijn ingeschakeld (371233)</span><span class="sxs-lookup"><span data-stu-id="45d3f-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="45d3f-113">Wanneer u een nieuwe omgeving inricht in Talent, is **Partijen zonder rollen verwijderen** standaard ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="45d3f-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="45d3f-114">Wanneer u een werknemer verwijdert, wordt de partij die aan de werknemer is gekoppeld alleen verwijderd als deze instelling is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="45d3f-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="45d3f-115">Door deze wijziging worden dubbele records in het algemene adresboek beperkt wanneer u werknemers importeert, wijzigt of opnieuw importeert.</span><span class="sxs-lookup"><span data-stu-id="45d3f-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="45d3f-116">Concept- en geannuleerde verlofaanvragen moeten kunnen worden verwijderd in Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="45d3f-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="45d3f-117">Met deze wijziging kunt u nu verlofaanvragen met de status **Concept** of **Geannuleerd** in Common Data Service verwijderen.</span><span class="sxs-lookup"><span data-stu-id="45d3f-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="45d3f-118">Aanvullende lijstwaarden in aangepaste velden worden niet weergegeven in Common Data Service nadat u op Toepassen hebt geklikt in het formulier Aangepaste velden (379599)</span><span class="sxs-lookup"><span data-stu-id="45d3f-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="45d3f-119">Wanneer u nieuwe lijstwaarden toevoegt aan een bestaand aangepast veld dat al is gesynchroniseerd met Common Data Service, zijn deze nu beschikbaar in Common Data Service nadat u de wijzigingen hebt toegepast in het formulier **Aangepaste velden**.</span><span class="sxs-lookup"><span data-stu-id="45d3f-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="45d3f-120">Controlelijsten voor onboarden toepassen op rechtspersonen wanneer meer dan één dienstverband bestaat (371270)</span><span class="sxs-lookup"><span data-stu-id="45d3f-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="45d3f-121">In de release van deze week kunt u controlelijsten toepassen op werknemers met meer dan één werknemer in **Formulier Medewerker > Controlelijsten**.</span><span class="sxs-lookup"><span data-stu-id="45d3f-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="45d3f-122">De preview-functie Open inschrijving voor voordelen is verwijderd</span><span class="sxs-lookup"><span data-stu-id="45d3f-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="45d3f-123">In combinatie met onze mededeling in het blogbericht [Strategische investeringen Core HR dragen bij tot uitmuntendheid](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) heeft Microsoft de functie Open inschrijving voor voordelen uit de openbare preview-versie verwijderd.</span><span class="sxs-lookup"><span data-stu-id="45d3f-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="45d3f-124">In de toekomst wordt nieuwe functionaliteit uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="45d3f-124">New functionality will be released in the future.</span></span> <span data-ttu-id="45d3f-125">Het productiegebruik van de functie voor open inschrijving voor voordelen wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="45d3f-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="45d3f-126">Binnenkort beschikbaar</span><span class="sxs-lookup"><span data-stu-id="45d3f-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="45d3f-127">Prestatiebeoordelingen afdrukken</span><span class="sxs-lookup"><span data-stu-id="45d3f-127">Print performance reviews</span></span>

<span data-ttu-id="45d3f-128">Zie [Beoordelingen van afdrukprestaties](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in het Dynamics 365: releasewave 2-plan van 2019.</span><span class="sxs-lookup"><span data-stu-id="45d3f-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="45d3f-129">Werkgebied Functiebeheer</span><span class="sxs-lookup"><span data-stu-id="45d3f-129">Feature management workspace</span></span>

<span data-ttu-id="45d3f-130">Functies worden toegevoegd en bijgewerkt in elke release.</span><span class="sxs-lookup"><span data-stu-id="45d3f-130">Features are added and updated in every release.</span></span> <span data-ttu-id="45d3f-131">De Functiebeheerervaring biedt een werkgebied waarin u een lijst met functies kunt weergeven die in elke release zijn geleverd.</span><span class="sxs-lookup"><span data-stu-id="45d3f-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="45d3f-132">Nieuwe functies zijn standaard uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="45d3f-132">By default, new features are turned off.</span></span> <span data-ttu-id="45d3f-133">U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="45d3f-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="45d3f-134">Voor meer informatie over de wijzigingen in functiebeheer raadpleegt u [Overzicht van Functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="45d3f-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
