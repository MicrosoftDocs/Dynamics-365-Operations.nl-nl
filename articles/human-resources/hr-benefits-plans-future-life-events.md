---
title: Toekomstige levensgebeurtenissen configureren
description: U kunt toekomstige levensgebeurtenissen plannen in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f10d7b6c9b45f6cedc16972fb157e43b7e0c40b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112117"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="61fc2-103">Toekomstige levensgebeurtenissen configureren</span><span class="sxs-lookup"><span data-stu-id="61fc2-103">Configure future life events</span></span>

<span data-ttu-id="61fc2-104">U kunt toekomstige levensgebeurtenissen plannen in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="61fc2-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="61fc2-105">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Toekomstige levensgebeurtenissen**.</span><span class="sxs-lookup"><span data-stu-id="61fc2-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="61fc2-106">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="61fc2-106">Select **New**.</span></span>

3. <span data-ttu-id="61fc2-107">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="61fc2-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="61fc2-108">Veld</span><span class="sxs-lookup"><span data-stu-id="61fc2-108">Field</span></span> | <span data-ttu-id="61fc2-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="61fc2-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="61fc2-110">Datum van levensgebeurtenis</span><span class="sxs-lookup"><span data-stu-id="61fc2-110">Life event date</span></span> | <span data-ttu-id="61fc2-111">Het systeem verwerkt alle gebeurtenissen tijdens de inschrijvingsperiode die plaatsvinden tot en met deze datum.</span><span class="sxs-lookup"><span data-stu-id="61fc2-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="61fc2-112">Levensgebeurtenis vastgelegd</span><span class="sxs-lookup"><span data-stu-id="61fc2-112">Life event logged</span></span> | <span data-ttu-id="61fc2-113">De datum en het tijdstip waarop de levensgebeurtenis in het logboek is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="61fc2-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="61fc2-114">Logboektype</span><span class="sxs-lookup"><span data-stu-id="61fc2-114">Log type</span></span> | <span data-ttu-id="61fc2-115">Hier ziet u of de actie een van de volgende acties is:</span><span class="sxs-lookup"><span data-stu-id="61fc2-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="61fc2-116">- **Bijwerken** – een wijziging aanbrengen in een bestaande record die levensgebeurtenissen bijhoudt</span><span class="sxs-lookup"><span data-stu-id="61fc2-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="61fc2-117">- **Invoegen** – een nieuwe levensgebeurtenisrecord maken</span><span class="sxs-lookup"><span data-stu-id="61fc2-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="61fc2-118">Type-id van levensgebeurtenis</span><span class="sxs-lookup"><span data-stu-id="61fc2-118">Life event type ID</span></span> | <span data-ttu-id="61fc2-119">De unieke id voor het type levensgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="61fc2-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="61fc2-120">Type levensgebeurtenis</span><span class="sxs-lookup"><span data-stu-id="61fc2-120">Life event type</span></span> | <span data-ttu-id="61fc2-121">Een katalysator om de inschrijving van een werknemer voor vergoedingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="61fc2-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="61fc2-122">Zie de sectie Triggers voor levensgebeurtenissen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="61fc2-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="61fc2-123">Status</span><span class="sxs-lookup"><span data-stu-id="61fc2-123">Status</span></span> | <span data-ttu-id="61fc2-124">Of de levensgebeurtenis wel of niet is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="61fc2-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="61fc2-125">Regel</span><span class="sxs-lookup"><span data-stu-id="61fc2-125">Line</span></span> | <span data-ttu-id="61fc2-126">Het regelnummer van de toekomstige levensgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="61fc2-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="61fc2-127">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="61fc2-127">Select **Save**.</span></span> 
