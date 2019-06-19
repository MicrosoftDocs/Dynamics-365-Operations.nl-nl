---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (8 oktober 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
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
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 34216e2181915cf615e6e77fa2a10d06a4e9db85
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617267"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="a9da8-103">Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (8 oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="a9da8-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a9da8-104">**Build 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="a9da8-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="a9da8-105">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.</span><span class="sxs-lookup"><span data-stu-id="a9da8-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="a9da8-106">Toestaan dat andere datums worden gebruikt op basis van verlofniveau (verlofbeheer)</span><span class="sxs-lookup"><span data-stu-id="a9da8-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="a9da8-107">Wanneer verlof wordt toegekend aan werknemers, bepaalt de toekenningsniveaubasis hoeveel verloftijd een werknemer opbouwt.</span><span class="sxs-lookup"><span data-stu-id="a9da8-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="a9da8-108">Op dit moment zijn deze niveaus gebaseerd op begin- en anciënniteitsdatum van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="a9da8-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="a9da8-109">Organisaties moeten in sommige gevallen deze niveaus baseren op andere datums, zoals een jubileumdatum of de oorspronkelijke aanstellingsdatum.</span><span class="sxs-lookup"><span data-stu-id="a9da8-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="a9da8-110">Deze datums worden al gebruikt in het verlofplan om te bepalen wanneer toerekeningen plaatsvinden. De mogelijkheid dat dezelfde datums worden gebruikt wanneer een werknemer wordt ingeschreven bij een plan, is toegevoegd om het toerekeningsbedrag te bepalen.</span><span class="sxs-lookup"><span data-stu-id="a9da8-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="a9da8-111">Andere wijzigingen</span><span class="sxs-lookup"><span data-stu-id="a9da8-111">Other changes</span></span>
<span data-ttu-id="a9da8-112">Overige correcties zijn opgenomen in deze release.</span><span class="sxs-lookup"><span data-stu-id="a9da8-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="a9da8-113">Bekend probleem</span><span class="sxs-lookup"><span data-stu-id="a9da8-113">Known issue</span></span>

<span data-ttu-id="a9da8-114">**Probleem:** als een nieuwe bijlage wordt toegevoegd aan een werknemer, zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar. **Oplossing:** voordat u de pagina van de bijlage opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="a9da8-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="a9da8-115">Als de feitenvakken worden gesloten wanneer de pagina **Werknemer** wordt geladen, worden de bijlageknoppen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="a9da8-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="a9da8-116">(Dit probleem wordt opgelost in de volgende platformupdate.)</span><span class="sxs-lookup"><span data-stu-id="a9da8-116">(This issue will be fixed in the next platform update.)</span></span>
