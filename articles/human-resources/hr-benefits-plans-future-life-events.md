---
title: Toekomstige levensgebeurtenissen configureren
description: U kunt toekomstige levensgebeurtenissen plannen in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d52e91e7b050027485b3536f40f6ad80afd90de8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056727"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="5ba66-103">Toekomstige levensgebeurtenissen configureren</span><span class="sxs-lookup"><span data-stu-id="5ba66-103">Configure future life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5ba66-104">U kunt toekomstige levensgebeurtenissen plannen in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5ba66-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="5ba66-105">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Toekomstige levensgebeurtenissen**.</span><span class="sxs-lookup"><span data-stu-id="5ba66-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="5ba66-106">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5ba66-106">Select **New**.</span></span>

3. <span data-ttu-id="5ba66-107">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="5ba66-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5ba66-108">Veld</span><span class="sxs-lookup"><span data-stu-id="5ba66-108">Field</span></span> | <span data-ttu-id="5ba66-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5ba66-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5ba66-110">Datum van levensgebeurtenis</span><span class="sxs-lookup"><span data-stu-id="5ba66-110">Life event date</span></span> | <span data-ttu-id="5ba66-111">Het systeem verwerkt alle gebeurtenissen tijdens de inschrijvingsperiode die plaatsvinden tot en met deze datum.</span><span class="sxs-lookup"><span data-stu-id="5ba66-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="5ba66-112">Levensgebeurtenis vastgelegd</span><span class="sxs-lookup"><span data-stu-id="5ba66-112">Life event logged</span></span> | <span data-ttu-id="5ba66-113">De datum en het tijdstip waarop de levensgebeurtenis in het logboek is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="5ba66-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="5ba66-114">Logboektype</span><span class="sxs-lookup"><span data-stu-id="5ba66-114">Log type</span></span> | <span data-ttu-id="5ba66-115">Hier ziet u of de actie een van de volgende acties is:</span><span class="sxs-lookup"><span data-stu-id="5ba66-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="5ba66-116">- **Bijwerken** – een wijziging aanbrengen in een bestaande record die levensgebeurtenissen bijhoudt</span><span class="sxs-lookup"><span data-stu-id="5ba66-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="5ba66-117">- **Invoegen** – een nieuwe levensgebeurtenisrecord maken</span><span class="sxs-lookup"><span data-stu-id="5ba66-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="5ba66-118">Type-id van levensgebeurtenis</span><span class="sxs-lookup"><span data-stu-id="5ba66-118">Life event type ID</span></span> | <span data-ttu-id="5ba66-119">De unieke id voor het type levensgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="5ba66-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="5ba66-120">Type levensgebeurtenis</span><span class="sxs-lookup"><span data-stu-id="5ba66-120">Life event type</span></span> | <span data-ttu-id="5ba66-121">Een katalysator om de inschrijving van een werknemer voor vergoedingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="5ba66-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="5ba66-122">Zie de sectie Triggers voor levensgebeurtenissen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5ba66-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="5ba66-123">Status</span><span class="sxs-lookup"><span data-stu-id="5ba66-123">Status</span></span> | <span data-ttu-id="5ba66-124">Of de levensgebeurtenis wel of niet is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="5ba66-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="5ba66-125">Regel</span><span class="sxs-lookup"><span data-stu-id="5ba66-125">Line</span></span> | <span data-ttu-id="5ba66-126">Het regelnummer van de toekomstige levensgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="5ba66-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="5ba66-127">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5ba66-127">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]