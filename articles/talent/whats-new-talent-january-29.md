---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (31 januari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4504cebb7702c7163c94badeeb06d9af0e5467e
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "857633"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="23939-103">Wat is nieuw of gewijzigd in Dynamics 365 for Talent (31 januari 2019)</span><span class="sxs-lookup"><span data-stu-id="23939-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23939-104">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="23939-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="23939-105">**Build 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="23939-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="23939-106">Core HR-wijzigingen</span><span class="sxs-lookup"><span data-stu-id="23939-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="23939-107">Bij verlof dat wordt opgenomen op de verlofkaart wordt geen rekening gehouden met verlofplandatums</span><span class="sxs-lookup"><span data-stu-id="23939-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="23939-108">Voor personen die verlofplannen hebben die niet in een kalenderjaar vallen, wordt op de kaart **Gebruikt** nu verlof weergegeven dat is opgenomen in het in het plan gedefinieerde verlofjaar.</span><span class="sxs-lookup"><span data-stu-id="23939-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="23939-109">Als het verlofjaar van een organisatie bijvoorbeeld van1 juni tot en met 30 mei loopt en een werknemer 3 dagen verlof heeft opgenomen in december, wordt op de kaart **Gebruikt** op 15 januari 3 dagen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="23939-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="23939-110">Toerekeningsbedragen die niet overeenkomen met de laagdatumbasis</span><span class="sxs-lookup"><span data-stu-id="23939-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="23939-111">Nieuwe opties zijn toegevoegd aan verlof en afwezigheid (**Human resources**-parameters) waarmee klanten kunnen bepalen wanneer de dienstmaanden van werknemers geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="23939-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="23939-112">Voor sommige organisaties is de datum het einde van de maand, maar voor andere organisaties kan de datum het begin van de volgende maand zijn.</span><span class="sxs-lookup"><span data-stu-id="23939-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="23939-113">Een bepaalde organisatie kan bijvoorbeeld verlof geven op 31 december, terwijl een andere organsatie verlof op 1 januari geeft.</span><span class="sxs-lookup"><span data-stu-id="23939-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="23939-114">Met deze optie kunt u bepalen wanneer de toekenning moet plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="23939-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="23939-115">Aanstellingsacties van werknemers kunnen vastzitten in de status Workflows voltooid.</span><span class="sxs-lookup"><span data-stu-id="23939-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="23939-116">Er zijn wijzigingen aangebracht om een probleem op te lossen waarbij een klein aantal workflows vastzat in de status Workflows voltooid.</span><span class="sxs-lookup"><span data-stu-id="23939-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="23939-117">Nieuwe workflows krijgen nu de status 'Voltooid' als de workflow is voltooid.</span><span class="sxs-lookup"><span data-stu-id="23939-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="23939-118">Alle workflows met de status Workflow voltooid krijgen de status Fout zodat zo nodig wijziging of verwijdering mogelijk is.</span><span class="sxs-lookup"><span data-stu-id="23939-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
