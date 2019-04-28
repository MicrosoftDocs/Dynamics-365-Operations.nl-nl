---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (14 februari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "859385"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="5da0e-103">Wat is nieuw of gewijzigd in Dynamics 365 for Talent (14 februari 2019)</span><span class="sxs-lookup"><span data-stu-id="5da0e-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5da0e-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Talent.</span><span class="sxs-lookup"><span data-stu-id="5da0e-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="5da0e-105">Wijzigingen in Attract</span><span class="sxs-lookup"><span data-stu-id="5da0e-105">Changes in Attract</span></span>
<span data-ttu-id="5da0e-106">Er zijn andere kleine correcties opgenomen in deze release.</span><span class="sxs-lookup"><span data-stu-id="5da0e-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="5da0e-107">Wijzigingen in Onboarding</span><span class="sxs-lookup"><span data-stu-id="5da0e-107">Changes in Onboarding</span></span>
<span data-ttu-id="5da0e-108">Er zijn andere kleine correcties opgenomen in deze release.</span><span class="sxs-lookup"><span data-stu-id="5da0e-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="5da0e-109">Wijzigingen in Core HR</span><span class="sxs-lookup"><span data-stu-id="5da0e-109">Changes in Core HR</span></span> 
<span data-ttu-id="5da0e-110">**Build 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="5da0e-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="5da0e-111">Met de entiteit Vaste compensatie voor werknemer worden niet alle records geëxporteerd</span><span class="sxs-lookup"><span data-stu-id="5da0e-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="5da0e-112">Met deze wijziging worden nu alle records geëxporteerd met de entiteit **Vaste compensatie voor werknemer**.</span><span class="sxs-lookup"><span data-stu-id="5da0e-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="5da0e-113">De entiteit kan worden gebruikt om bestaande records voor vaste compensatie voor werknemers te maken en bij te werken.</span><span class="sxs-lookup"><span data-stu-id="5da0e-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="5da0e-114">Bij Einddatum dienstverband wordt geen rekening gehouden met de voorkeursinstellingen voor tijdzones van werknemers</span><span class="sxs-lookup"><span data-stu-id="5da0e-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="5da0e-115">Bij Einddatum dienstverband wordt nu wel rekening gehouden met voorkeurstijdzone van gebruikers bij het maken of beëindigen van een dienstverband bij een bedrijf.</span><span class="sxs-lookup"><span data-stu-id="5da0e-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="5da0e-116">Adressen in het Verenigd Koninkrijk worden in Analyses weergegeven als adressen in Oost-Zwitserland</span><span class="sxs-lookup"><span data-stu-id="5da0e-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="5da0e-117">In deze release is een wijziging aangebracht om onjuiste uitlijning te corrigeren in adressen in het rapport 'Personeelsbezetting per locatie' in **Personeelsbeheer**.</span><span class="sxs-lookup"><span data-stu-id="5da0e-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="5da0e-118">Ontslagcode wordt niet ingevuld in de record voor werknemerspositietoewijzing wanneer de positie wordt beëindigd</span><span class="sxs-lookup"><span data-stu-id="5da0e-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="5da0e-119">Er is een wijziging aangebracht zodat de code voor 'Ontslagreden' standaard wordt ingesteld wanneer de werknemerspositietoewijzing wordt beëindigd.</span><span class="sxs-lookup"><span data-stu-id="5da0e-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="5da0e-120">Er is een nieuwe entiteit gemaakt voor taakcompensatieniveaus</span><span class="sxs-lookup"><span data-stu-id="5da0e-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="5da0e-121">Er is een nieuwe DMF-entiteit (Data Management Framework) gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5da0e-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="5da0e-122">Met de entiteit kunnen compensatieniveaus, marktwaarden en onderzoeksinformatie worden gemaakt en bijgewerkt voor elke taak die in het systeem is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="5da0e-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
