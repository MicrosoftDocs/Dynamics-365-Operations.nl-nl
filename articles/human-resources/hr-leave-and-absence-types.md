---
title: Verlof- en verzuimtypen configureren
description: Typen verlof instellen die werknemers kunnen aanvragen in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008658"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="afca1-103">Verlof- en verzuimtypen configureren</span><span class="sxs-lookup"><span data-stu-id="afca1-103">Configure leave and absence types</span></span>

<span data-ttu-id="afca1-104">Verloftypen in Dynamics 365 Human Resources geven de typen verlof aan die werknemers kunnen rapporteren.</span><span class="sxs-lookup"><span data-stu-id="afca1-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="afca1-105">U kunt de typen verlof aanpassen op basis van de behoeften van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="afca1-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="afca1-106">Voorbeelden van verloftypen zijn:</span><span class="sxs-lookup"><span data-stu-id="afca1-106">Examples of leave types include:</span></span>

- <span data-ttu-id="afca1-107">Betaald verlof</span><span class="sxs-lookup"><span data-stu-id="afca1-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="afca1-108">Onbetaald verlof</span><span class="sxs-lookup"><span data-stu-id="afca1-108">Unpaid leave</span></span>
- <span data-ttu-id="afca1-109">Betaalde vakantie</span><span class="sxs-lookup"><span data-stu-id="afca1-109">Paid vacation</span></span>
- <span data-ttu-id="afca1-110">Ziekteverlof</span><span class="sxs-lookup"><span data-stu-id="afca1-110">Sick leave</span></span>
- <span data-ttu-id="afca1-111">Medisch verlof</span><span class="sxs-lookup"><span data-stu-id="afca1-111">Medical leave</span></span>
- <span data-ttu-id="afca1-112">Familieverlof</span><span class="sxs-lookup"><span data-stu-id="afca1-112">Family leave</span></span>
- <span data-ttu-id="afca1-113">Kortdurende arbeidsongeschiktheid</span><span class="sxs-lookup"><span data-stu-id="afca1-113">Short-term disability</span></span>
- <span data-ttu-id="afca1-114">Verlof bij sterfgeval</span><span class="sxs-lookup"><span data-stu-id="afca1-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="afca1-115">Een verloftype toevoegen</span><span class="sxs-lookup"><span data-stu-id="afca1-115">Add a leave type</span></span>

1. <span data-ttu-id="afca1-116">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="afca1-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="afca1-117">Selecteer onder **Instellingen** de optie **Verlof- en verzuimtypen**.</span><span class="sxs-lookup"><span data-stu-id="afca1-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="afca1-118">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="afca1-118">Select **New**.</span></span>

4. <span data-ttu-id="afca1-119">Voer een naam in voor het verloftype onder **Type**, selecteer een werkstroom bij **Werkstroom-id** en voer een beschrijving in onder **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="afca1-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="afca1-120">Selecteer bij **Algemeen** de optie **Geen**, **Gepland** of **Ongepland** in de vervolgkeuzelijst **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="afca1-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="afca1-121">Selecteer een inkomstencode in de vervolgkeuzelijst **Inkomstencode**.</span><span class="sxs-lookup"><span data-stu-id="afca1-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="afca1-122">Geef onder **Redencode vereist** aan of u een redencode wilt vereisen.</span><span class="sxs-lookup"><span data-stu-id="afca1-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="afca1-123">Als u redencodes wilt vereisen, moet u deze mogelijk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="afca1-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="afca1-124">Selecteer onder **Redencodes** de optie **Toevoegen**, selecteer een redencode en schakel vervolgens het selectievakje **Ingeschakeld** hiernaast in.</span><span class="sxs-lookup"><span data-stu-id="afca1-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="afca1-125">Kies onder **Toegang tot geselecteerde rollen beperken** of u de toegang wilt beperken.</span><span class="sxs-lookup"><span data-stu-id="afca1-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="afca1-126">Selecteer vervolgens de beveiligingsrollen onder **Beveiligingsrollen voor dit verloftype**.</span><span class="sxs-lookup"><span data-stu-id="afca1-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="afca1-127">De beveiligingsrollen worden gedefinieerd in de werkstroom die u onder **Werkstroom-id** eerder in deze procedure hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="afca1-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="afca1-128">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="afca1-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="afca1-129">Voorbeeldfuncties configureren</span><span class="sxs-lookup"><span data-stu-id="afca1-129">Configure preview features</span></span>

<span data-ttu-id="afca1-130">Als u de voorbeeldfuncties voor verlof en verzuim hebt ingeschakeld, moet u ook de instellingen hiervoor configureren.</span><span class="sxs-lookup"><span data-stu-id="afca1-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="afca1-131">Stel afrondingsopties in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="afca1-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="afca1-132">De beschikbare opties zijn **Geen**, **Naar boven**, **Naar beneden** en **Dichtstbijzijnde**.</span><span class="sxs-lookup"><span data-stu-id="afca1-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="afca1-133">U kunt ook een afrondingsprecisie instellen voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="afca1-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="afca1-134">Stel **Feestdagcorrectie** in voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="afca1-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="afca1-135">Wanneer u deze optie selecteert, gebruikt Human Resources het aantal feestdagen dat op een werkdag valt om te bepalen hoe het verlof moet worden opgebouwd voor het verloftype.</span><span class="sxs-lookup"><span data-stu-id="afca1-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="afca1-136">Als kerstdag bijvoorbeeld op een maandag valt, trekt Human Resources een dag af van het verloftype bij het verwerken van toerekeningen.</span><span class="sxs-lookup"><span data-stu-id="afca1-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="afca1-137">U kunt feestdage instellen in de werktijdkalender.</span><span class="sxs-lookup"><span data-stu-id="afca1-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="afca1-138">Zie [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md) voor meer informatie</span><span class="sxs-lookup"><span data-stu-id="afca1-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="afca1-139">Zie ook</span><span class="sxs-lookup"><span data-stu-id="afca1-139">See also</span></span>

- [<span data-ttu-id="afca1-140">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="afca1-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="afca1-141">Een verlof- en verzuimplan maken</span><span class="sxs-lookup"><span data-stu-id="afca1-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="afca1-142">Een werktijdkalender maken</span><span class="sxs-lookup"><span data-stu-id="afca1-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)