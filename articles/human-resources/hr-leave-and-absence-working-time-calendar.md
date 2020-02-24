---
title: Een werktijdkalender maken
description: Definieer een werktijdkalender, feestdagen en vrije tijd in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 641f66c75875cfba51af3753223a070d7cb7dc50
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008657"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="74b46-103">Een werktijdkalender maken</span><span class="sxs-lookup"><span data-stu-id="74b46-103">Create a working time calendar</span></span>

<span data-ttu-id="74b46-104">Een werktijdkalender in Dynamics 365 Human Resources toont de dagen en uren die werknemers in uw organisatie werken.</span><span class="sxs-lookup"><span data-stu-id="74b46-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="74b46-105">Wanneer een werknemer een verlofaanvraag indient, hoeft hij of zij zich geen zorgen te maken over feestdagen en sluitingen.</span><span class="sxs-lookup"><span data-stu-id="74b46-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="74b46-106">Voor het stroomlijnen van verlofaanvragen configureert u deze items voor uw organisatie:</span><span class="sxs-lookup"><span data-stu-id="74b46-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="74b46-107">Werktijdkalender</span><span class="sxs-lookup"><span data-stu-id="74b46-107">Working time calendar</span></span>
- <span data-ttu-id="74b46-108">Feestdagen en sluitingen</span><span class="sxs-lookup"><span data-stu-id="74b46-108">Holidays and closures</span></span>
- <span data-ttu-id="74b46-109">Vrije tijd</span><span class="sxs-lookup"><span data-stu-id="74b46-109">Non-work time</span></span>

<span data-ttu-id="74b46-110">U kunt de laatste twee items toevoegen terwijl u een werktijdkalender instelt.</span><span class="sxs-lookup"><span data-stu-id="74b46-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="74b46-111">U kunt deze ook afzonderlijk configureren of bijwerken.</span><span class="sxs-lookup"><span data-stu-id="74b46-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="74b46-112">Een werktijdkalender instellen</span><span class="sxs-lookup"><span data-stu-id="74b46-112">Set up a working time calendar</span></span>

<span data-ttu-id="74b46-113">Stel minimaal één werktijdkalender in waarin uw dagen en werktijden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="74b46-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="74b46-114">Als u locaties hebt in meerdere landen en regio's, kunt u een werktijdkalender instellen voor elk gebied.</span><span class="sxs-lookup"><span data-stu-id="74b46-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="74b46-115">Selecteer op de pagina **Organisatiebeheer** de optie **Kalenders**.</span><span class="sxs-lookup"><span data-stu-id="74b46-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="74b46-116">Selecteer **Nieuw** en geef een naam en beschrijving op voor uw kalender.</span><span class="sxs-lookup"><span data-stu-id="74b46-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="74b46-117">Selecteer onder **Opties voor genereren** de werkdagen voor uw organisatie en geef werktijden op.</span><span class="sxs-lookup"><span data-stu-id="74b46-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="74b46-118">Als u een feestdag of sluiting wilt toevoegen, selecteert u de knop **Toevoegen** naast **Feestdagen en sluitingen**.</span><span class="sxs-lookup"><span data-stu-id="74b46-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="74b46-119">Als u vrije tijd wilt toevoegen, zoals lunchen of pauzes, selecteert u **Toevoegen** onder **VRIJE TIJD** en voert u de naam en het tijdsbereik in.</span><span class="sxs-lookup"><span data-stu-id="74b46-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="74b46-120">Selecteer onder **Dagen** de optie **Genereren** om de dagen in uw kalender te genereren.</span><span class="sxs-lookup"><span data-stu-id="74b46-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="74b46-121">Voer het datumbereik voor uw kalender in en selecteer vervolgens **Dagen genereren**.</span><span class="sxs-lookup"><span data-stu-id="74b46-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="74b46-122">Als u werkschema's wilt toevoegen, selecteert u onder **Werkschema** de optie **Toevoegen** en voert u vervolgens de tijden voor elke werkplanning in.</span><span class="sxs-lookup"><span data-stu-id="74b46-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="74b46-123">Feestdagen en sluitingen configureren</span><span class="sxs-lookup"><span data-stu-id="74b46-123">Configure holidays and closures</span></span>

<span data-ttu-id="74b46-124">U kunt vrije dagen en sluitingen apart van een werktijdkalender toevoegen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="74b46-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="74b46-125">Selecteer op de pagina **Organisatiebeheer** de optie **Feestdagen en sluitingen**.</span><span class="sxs-lookup"><span data-stu-id="74b46-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="74b46-126">Selecteer **Nieuw** en geef een naam en datum op voor de feestdag of sluiting.</span><span class="sxs-lookup"><span data-stu-id="74b46-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="74b46-127">Vrije tijd configureren</span><span class="sxs-lookup"><span data-stu-id="74b46-127">Configure non-work time</span></span>

<span data-ttu-id="74b46-128">U kunt vrije tijd apart van een werktijdkalender toevoegen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="74b46-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="74b46-129">Selecteer op de pagina **Organisatiebeheer** de optie **Vrije tijd**.</span><span class="sxs-lookup"><span data-stu-id="74b46-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="74b46-130">Selecteer **Nieuw** en voer een naam en tijdbereik in voor de vrije tijd.</span><span class="sxs-lookup"><span data-stu-id="74b46-130">Select **New** and enter a name and time range for the non-work time.</span></span>

## <a name="leave-and-absence-preview-feature"></a><span data-ttu-id="74b46-131">Preview-functie voor verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="74b46-131">Leave and absence preview feature</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="74b46-132">Als u de preview-functie van Verlof en verzuim voor correcties voor feestdagen hebt ingeschakeld, gebruikt Human Resources feedsdagen en sluitingsdatums om het aantal dagen te bepalen dat moet worden aangepast voor werknemers die zijn ingeschreven in de kalender.</span><span class="sxs-lookup"><span data-stu-id="74b46-132">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="74b46-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="74b46-133">See also</span></span>

- [<span data-ttu-id="74b46-134">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="74b46-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="74b46-135">Verlof- en verzuimtypen configureren</span><span class="sxs-lookup"><span data-stu-id="74b46-135">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
