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
ms.openlocfilehash: 5e241475c9652ab2dafe6886479e9c0a93711aca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466755"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="51438-103">Parameters voor Vergoedingenbeheer en Werknemerselfservice instellen voor alle bedrijven</span><span class="sxs-lookup"><span data-stu-id="51438-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="51438-104">Voordat u vergoedingsplannen kunt instellen in Microsoft Dynamics 365 Human Resources, moet u parameters voor Vergoedingenbeheer configureren.</span><span class="sxs-lookup"><span data-stu-id="51438-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="51438-105">Met deze parameters worden standaardwaarden, redencodes en andere opties ingesteld.</span><span class="sxs-lookup"><span data-stu-id="51438-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="51438-106">Algemene parameters configureren</span><span class="sxs-lookup"><span data-stu-id="51438-106">Configure general parameters</span></span>

1. <span data-ttu-id="51438-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Gedeelde parameters voor Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="51438-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="51438-108">Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="51438-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="51438-109">Veld</span><span class="sxs-lookup"><span data-stu-id="51438-109">Field</span></span> | <span data-ttu-id="51438-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51438-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="51438-111">**Land/regio**</span><span class="sxs-lookup"><span data-stu-id="51438-111">**Country/region**</span></span> | <span data-ttu-id="51438-112">Het veld **Land/regio** bepaalt de weergavevolgorde van postcodes/staten.</span><span class="sxs-lookup"><span data-stu-id="51438-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="51438-113">Het geselecteerde land wordt als eerste weergegeven in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="51438-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="51438-114">**Redencode van inschrijving**</span><span class="sxs-lookup"><span data-stu-id="51438-114">**Enrollment reason code**</span></span> | <span data-ttu-id="51438-115">Selecteer een standaard redencode die moet worden gebruikt wanneer er plannen voor werknemers worden gemaakt tijdens de verwerking van open inschrijving.</span><span class="sxs-lookup"><span data-stu-id="51438-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="51438-116">**Redencode voor annulering**</span><span class="sxs-lookup"><span data-stu-id="51438-116">**Cancellation reason code**</span></span> | <span data-ttu-id="51438-117">De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="51438-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="51438-118">Tijdens het annuleringsproces wordt een dialoogvenster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="51438-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="51438-119">Gebruikers kunnen dit desgewenst wijzigen in de **redencodes voor annulering**.</span><span class="sxs-lookup"><span data-stu-id="51438-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="51438-120">**Redencode voor opnieuw openen**</span><span class="sxs-lookup"><span data-stu-id="51438-120">**Reopen reason code**</span></span> | <span data-ttu-id="51438-121">De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt opnieuw geopend.</span><span class="sxs-lookup"><span data-stu-id="51438-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="51438-122">Tijdens het annuleringsproces wordt een dialoogvenster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="51438-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="51438-123">Gebruikers kunnen de optie **Redencode opnieuw openen** desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="51438-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="51438-124">**Redencode van levensgebeurtenis**</span><span class="sxs-lookup"><span data-stu-id="51438-124">**Life event reason code**</span></span> | <span data-ttu-id="51438-125">De redencode die wordt gebruikt wanneer een levensgebeurtenis plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="51438-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="51438-126">**Redencode tariefwijziging**</span><span class="sxs-lookup"><span data-stu-id="51438-126">**Rate change reason code**</span></span> | <span data-ttu-id="51438-127">De redencode die moet worden gebruikt bij het annuleren en opnieuw openen van een vergoedingsplan voor werknemers tijdens het bijwerkproces van de tariefwijziging.</span><span class="sxs-lookup"><span data-stu-id="51438-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="51438-128">Het geeft aan welke records zijn gewijzigd door het wijzigingsproces voor de tariefwijziging.</span><span class="sxs-lookup"><span data-stu-id="51438-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="51438-129">**Vergoedingen jaarsalaris**</span><span class="sxs-lookup"><span data-stu-id="51438-129">**Benefits annual salary**</span></span> | <span data-ttu-id="51438-130">Hiermee kunt u een **Jaarlijks salarisbedrag voor vergoedingen** voor een werknemer instellen.</span><span class="sxs-lookup"><span data-stu-id="51438-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="51438-131">Human Resources gebruikt **het jaarlijkse salarisbedrag voor vergoedingen** om de dekkingsbedragen vast te stellen in plaats van het vaste jaarlijkse compensatiebedrag.</span><span class="sxs-lookup"><span data-stu-id="51438-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="51438-132">**Nieuwe in aanmerking komende medewerker**</span><span class="sxs-lookup"><span data-stu-id="51438-132">**New hire eligible**</span></span> | <span data-ttu-id="51438-133">Hiermee wordt opgegeven of nieuw aangestelde medewerkers in aanmerking komen.</span><span class="sxs-lookup"><span data-stu-id="51438-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="51438-134">**Nieuwe inschrijvingsperiode van aanstelling**</span><span class="sxs-lookup"><span data-stu-id="51438-134">**New hire enrollment period**</span></span> | <span data-ttu-id="51438-135">De tijdsperiode waarin inschrijving van nieuw aangestelde medewerkers is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="51438-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="51438-136">**Opmerking**: deze instelling heeft voorrang op elke nieuwe inschrijvingsperiode die u instelt voor de geschiktheidsregel voor het plan.</span><span class="sxs-lookup"><span data-stu-id="51438-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="51438-137">**Standaard betalingsfrequentie**</span><span class="sxs-lookup"><span data-stu-id="51438-137">**Default pay frequency**</span></span> | <span data-ttu-id="51438-138">De standaardbetalingsfrequentie die wordt gebruikt wanneer nieuwe werknemers worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="51438-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="51438-139">**Levensgebeurtenissen ingeschakeld**</span><span class="sxs-lookup"><span data-stu-id="51438-139">**Life events enabled**</span></span> | <span data-ttu-id="51438-140">Hiermee worden levensgebeurtenissen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="51438-140">Enables life events.</span></span> |
   | <span data-ttu-id="51438-141">**Verouderde vergoedingsformulieren verbergen**</span><span class="sxs-lookup"><span data-stu-id="51438-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="51438-142">Hiermee kunt u verouderde vergoedingsformulieren verbergen.</span><span class="sxs-lookup"><span data-stu-id="51438-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="51438-143">**Vergoedingsverificatie**</span><span class="sxs-lookup"><span data-stu-id="51438-143">**Benefit verification**</span></span> | <span data-ttu-id="51438-144">De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="51438-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="51438-145">**Begunstigden automatisch selecteren**</span><span class="sxs-lookup"><span data-stu-id="51438-145">**Auto select designees**</span></span> | <span data-ttu-id="51438-146">Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd, op basis van hun geschiktheid voor planopties.</span><span class="sxs-lookup"><span data-stu-id="51438-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="51438-147">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="51438-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="51438-148">Parameters voor Werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="51438-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="51438-149">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="51438-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="51438-150">Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="51438-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="51438-151">Veld</span><span class="sxs-lookup"><span data-stu-id="51438-151">Field</span></span> | <span data-ttu-id="51438-152">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51438-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="51438-153">**Vergoedingsverificatie**</span><span class="sxs-lookup"><span data-stu-id="51438-153">**Benefit verification**</span></span> | <span data-ttu-id="51438-154">De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="51438-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="51438-155">**Begunstigden automatisch selecteren**</span><span class="sxs-lookup"><span data-stu-id="51438-155">**Auto select designees**</span></span> | <span data-ttu-id="51438-156">Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd op basis van hun geschiktheid voor planopties.</span><span class="sxs-lookup"><span data-stu-id="51438-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="51438-157">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="51438-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]