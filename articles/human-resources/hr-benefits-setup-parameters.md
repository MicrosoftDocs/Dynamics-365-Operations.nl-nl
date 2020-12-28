---
title: Parameters voor Vergoedingenbeheer en Werknemerselfservice instellen voor alle bedrijven
description: Parameters voor Vergoedingenbeheer en Werknemerselfservice configureren in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692692"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="efdaa-103">Parameters voor Vergoedingenbeheer en Werknemerselfservice instellen voor alle bedrijven</span><span class="sxs-lookup"><span data-stu-id="efdaa-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="efdaa-104">Voordat u vergoedingsplannen kunt instellen in Microsoft Dynamics 365 Human Resources, moet u parameters voor Vergoedingenbeheer configureren.</span><span class="sxs-lookup"><span data-stu-id="efdaa-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="efdaa-105">Met deze parameters worden standaardwaarden, redencodes en andere opties ingesteld.</span><span class="sxs-lookup"><span data-stu-id="efdaa-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="efdaa-106">Algemene parameters configureren</span><span class="sxs-lookup"><span data-stu-id="efdaa-106">Configure general parameters</span></span>

1. <span data-ttu-id="efdaa-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Gedeelde parameters voor Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="efdaa-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="efdaa-108">Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="efdaa-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="efdaa-109">Veld</span><span class="sxs-lookup"><span data-stu-id="efdaa-109">Field</span></span> | <span data-ttu-id="efdaa-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="efdaa-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="efdaa-111">**Land/regio**</span><span class="sxs-lookup"><span data-stu-id="efdaa-111">**Country/region**</span></span> | <span data-ttu-id="efdaa-112">Het veld **Land/regio** bepaalt de weergavevolgorde van postcodes/staten.</span><span class="sxs-lookup"><span data-stu-id="efdaa-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="efdaa-113">Het geselecteerde land wordt als eerste weergegeven in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="efdaa-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="efdaa-114">**Redencode van inschrijving**</span><span class="sxs-lookup"><span data-stu-id="efdaa-114">**Enrollment reason code**</span></span> | <span data-ttu-id="efdaa-115">Selecteer een standaard redencode die moet worden gebruikt wanneer er plannen voor werknemers worden gemaakt tijdens de verwerking van open inschrijving.</span><span class="sxs-lookup"><span data-stu-id="efdaa-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="efdaa-116">**Redencode voor annulering**</span><span class="sxs-lookup"><span data-stu-id="efdaa-116">**Cancellation reason code**</span></span> | <span data-ttu-id="efdaa-117">De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="efdaa-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="efdaa-118">Tijdens het annuleringsproces wordt een dialoogvenster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="efdaa-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="efdaa-119">Gebruikers kunnen dit desgewenst wijzigen in de **redencodes voor annulering**.</span><span class="sxs-lookup"><span data-stu-id="efdaa-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="efdaa-120">**Redencode voor opnieuw openen**</span><span class="sxs-lookup"><span data-stu-id="efdaa-120">**Reopen reason code**</span></span> | <span data-ttu-id="efdaa-121">De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt opnieuw geopend.</span><span class="sxs-lookup"><span data-stu-id="efdaa-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="efdaa-122">Tijdens het annuleringsproces wordt een dialoogvenster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="efdaa-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="efdaa-123">Gebruikers kunnen de optie **Redencode opnieuw openen** desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="efdaa-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="efdaa-124">**Redencode van levensgebeurtenis**</span><span class="sxs-lookup"><span data-stu-id="efdaa-124">**Life event reason code**</span></span> | <span data-ttu-id="efdaa-125">De redencode die wordt gebruikt wanneer een levensgebeurtenis plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="efdaa-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="efdaa-126">**Redencode tariefwijziging**</span><span class="sxs-lookup"><span data-stu-id="efdaa-126">**Rate change reason code**</span></span> | <span data-ttu-id="efdaa-127">De redencode die moet worden gebruikt bij het annuleren en opnieuw openen van een vergoedingsplan voor werknemers tijdens het bijwerkproces van de tariefwijziging.</span><span class="sxs-lookup"><span data-stu-id="efdaa-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="efdaa-128">Het geeft aan welke records zijn gewijzigd door het wijzigingsproces voor de tariefwijziging.</span><span class="sxs-lookup"><span data-stu-id="efdaa-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="efdaa-129">**Vergoedingen jaarsalaris**</span><span class="sxs-lookup"><span data-stu-id="efdaa-129">**Benefits annual salary**</span></span> | <span data-ttu-id="efdaa-130">Hiermee kunt u een **Jaarlijks salarisbedrag voor vergoedingen** voor een werknemer instellen.</span><span class="sxs-lookup"><span data-stu-id="efdaa-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="efdaa-131">Human Resources gebruikt **het jaarlijkse salarisbedrag voor vergoedingen** om de dekkingsbedragen vast te stellen in plaats van het vaste jaarlijkse compensatiebedrag.</span><span class="sxs-lookup"><span data-stu-id="efdaa-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="efdaa-132">**Nieuwe in aanmerking komende medewerker**</span><span class="sxs-lookup"><span data-stu-id="efdaa-132">**New hire eligible**</span></span> | <span data-ttu-id="efdaa-133">Hiermee wordt opgegeven of nieuw aangestelde medewerkers in aanmerking komen.</span><span class="sxs-lookup"><span data-stu-id="efdaa-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="efdaa-134">**Nieuwe inschrijvingsperiode van aanstelling**</span><span class="sxs-lookup"><span data-stu-id="efdaa-134">**New hire enrollment period**</span></span> | <span data-ttu-id="efdaa-135">De tijdsperiode waarin inschrijving van nieuw aangestelde medewerkers is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="efdaa-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="efdaa-136">**Opmerking**: deze instelling heeft voorrang op elke nieuwe inschrijvingsperiode die u instelt voor de geschiktheidsregel voor het plan.</span><span class="sxs-lookup"><span data-stu-id="efdaa-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="efdaa-137">**Standaard betalingsfrequentie**</span><span class="sxs-lookup"><span data-stu-id="efdaa-137">**Default pay frequency**</span></span> | <span data-ttu-id="efdaa-138">De standaardbetalingsfrequentie die wordt gebruikt wanneer nieuwe werknemers worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="efdaa-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="efdaa-139">**Levensgebeurtenissen ingeschakeld**</span><span class="sxs-lookup"><span data-stu-id="efdaa-139">**Life events enabled**</span></span> | <span data-ttu-id="efdaa-140">Hiermee worden levensgebeurtenissen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="efdaa-140">Enables life events.</span></span> |
   | <span data-ttu-id="efdaa-141">**Verouderde vergoedingsformulieren verbergen**</span><span class="sxs-lookup"><span data-stu-id="efdaa-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="efdaa-142">Hiermee kunt u verouderde vergoedingsformulieren verbergen.</span><span class="sxs-lookup"><span data-stu-id="efdaa-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="efdaa-143">**Vergoedingsverificatie**</span><span class="sxs-lookup"><span data-stu-id="efdaa-143">**Benefit verification**</span></span> | <span data-ttu-id="efdaa-144">De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="efdaa-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="efdaa-145">**Begunstigden automatisch selecteren**</span><span class="sxs-lookup"><span data-stu-id="efdaa-145">**Auto select designees**</span></span> | <span data-ttu-id="efdaa-146">Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd, op basis van hun geschiktheid voor planopties.</span><span class="sxs-lookup"><span data-stu-id="efdaa-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="efdaa-147">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="efdaa-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="efdaa-148">Parameters voor Werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="efdaa-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="efdaa-149">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="efdaa-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="efdaa-150">Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="efdaa-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="efdaa-151">Veld</span><span class="sxs-lookup"><span data-stu-id="efdaa-151">Field</span></span> | <span data-ttu-id="efdaa-152">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="efdaa-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="efdaa-153">**Vergoedingsverificatie**</span><span class="sxs-lookup"><span data-stu-id="efdaa-153">**Benefit verification**</span></span> | <span data-ttu-id="efdaa-154">De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="efdaa-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="efdaa-155">**Begunstigden automatisch selecteren**</span><span class="sxs-lookup"><span data-stu-id="efdaa-155">**Auto select designees**</span></span> | <span data-ttu-id="efdaa-156">Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd op basis van hun geschiktheid voor planopties.</span><span class="sxs-lookup"><span data-stu-id="efdaa-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="efdaa-157">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="efdaa-157">Select **Save**.</span></span>


