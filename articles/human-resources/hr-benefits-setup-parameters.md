---
title: Parameters voor Vergoedingenbeheer instellen
description: Configureer parameters voor Vergoedingenbeheer in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229758"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="84e1e-103">Parameters voor Vergoedingenbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="84e1e-103">Set Benefits management parameters</span></span>

<span data-ttu-id="84e1e-104">Voordat u verlofplannen kunt instellen in Microsoft Dynamics 365 Human Resources, moet u parameters voor Vergoedingenbeheer configureren.</span><span class="sxs-lookup"><span data-stu-id="84e1e-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="84e1e-105">Met deze parameters worden standaardwaarden, redencodes en andere opties ingesteld.</span><span class="sxs-lookup"><span data-stu-id="84e1e-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="84e1e-106">Algemene parameters configureren</span><span class="sxs-lookup"><span data-stu-id="84e1e-106">Configure general parameters</span></span>

1. <span data-ttu-id="84e1e-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="84e1e-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="84e1e-108">Geef op het tabblad **Algemeen** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="84e1e-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="84e1e-109">Veld</span><span class="sxs-lookup"><span data-stu-id="84e1e-109">Field</span></span> | <span data-ttu-id="84e1e-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="84e1e-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="84e1e-111">**Land/regio**</span><span class="sxs-lookup"><span data-stu-id="84e1e-111">**Country/region**</span></span> | <span data-ttu-id="84e1e-112">Het veld **Land/regio** bepaalt de weergavevolgorde van postcodes/staten.</span><span class="sxs-lookup"><span data-stu-id="84e1e-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="84e1e-113">Het geselecteerde land wordt als eerste weergegeven in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="84e1e-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="84e1e-114">**Redencode van inschrijving**</span><span class="sxs-lookup"><span data-stu-id="84e1e-114">**Enrollment reason code**</span></span> | <span data-ttu-id="84e1e-115">Selecteer een standaard redencode die moet worden gebruikt wanneer er plannen voor werknemers worden gemaakt tijdens de verwerking van open inschrijving.</span><span class="sxs-lookup"><span data-stu-id="84e1e-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="84e1e-116">**Redencode voor annulering**</span><span class="sxs-lookup"><span data-stu-id="84e1e-116">**Cancellation reason code**</span></span> | <span data-ttu-id="84e1e-117">De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="84e1e-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="84e1e-118">Tijdens het annuleringsproces wordt een dialoogvenster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="84e1e-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="84e1e-119">Gebruikers kunnen dit desgewenst wijzigen in de **redencodes voor annulering**.</span><span class="sxs-lookup"><span data-stu-id="84e1e-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="84e1e-120">**Redencode voor opnieuw openen**</span><span class="sxs-lookup"><span data-stu-id="84e1e-120">**Reopen reason code**</span></span> | <span data-ttu-id="84e1e-121">De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt opnieuw geopend.</span><span class="sxs-lookup"><span data-stu-id="84e1e-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="84e1e-122">Tijdens het annuleringsproces wordt een dialoogvenster weergegeven.</span><span class="sxs-lookup"><span data-stu-id="84e1e-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="84e1e-123">Gebruikers kunnen de optie **Redencode opnieuw openen** desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="84e1e-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="84e1e-124">**Redencode van levensgebeurtenis**</span><span class="sxs-lookup"><span data-stu-id="84e1e-124">**Life event reason code**</span></span> | <span data-ttu-id="84e1e-125">De redencode die wordt gebruikt wanneer een levensgebeurtenis plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="84e1e-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="84e1e-126">**Redencode tariefwijziging**</span><span class="sxs-lookup"><span data-stu-id="84e1e-126">**Rate change reason code**</span></span> | <span data-ttu-id="84e1e-127">De redencode die moet worden gebruikt bij het annuleren en opnieuw openen van een vergoedingsplan voor werknemers tijdens het bijwerkproces van de tariefwijziging.</span><span class="sxs-lookup"><span data-stu-id="84e1e-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="84e1e-128">Het geeft aan welke records zijn gewijzigd door het wijzigingsproces voor de tariefwijziging.</span><span class="sxs-lookup"><span data-stu-id="84e1e-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="84e1e-129">**Nieuwe in aanmerking komende medewerker**</span><span class="sxs-lookup"><span data-stu-id="84e1e-129">**New hire eligible**</span></span> | <span data-ttu-id="84e1e-130">Hiermee wordt opgegeven of nieuw aangestelde medewerkers in aanmerking komen.</span><span class="sxs-lookup"><span data-stu-id="84e1e-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="84e1e-131">**Nieuwe inschrijvingsperiode van aanstelling**</span><span class="sxs-lookup"><span data-stu-id="84e1e-131">**New hire enrollment period**</span></span> | <span data-ttu-id="84e1e-132">De tijdsperiode waarin inschrijving van nieuw aangestelde medewerkers is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="84e1e-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="84e1e-133">**Opmerking**: deze instelling heeft voorrang op elke nieuwe inschrijvingsperiode die u instelt voor de geschiktheidsregel voor het plan.</span><span class="sxs-lookup"><span data-stu-id="84e1e-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="84e1e-134">**Levensgebeurtenissen ingeschakeld**</span><span class="sxs-lookup"><span data-stu-id="84e1e-134">**Life events enabled**</span></span> | <span data-ttu-id="84e1e-135">Hiermee worden levensgebeurtenissen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="84e1e-135">Enables life events.</span></span> |
   | <span data-ttu-id="84e1e-136">**Verouderde vergoedingsformulieren verbergen**</span><span class="sxs-lookup"><span data-stu-id="84e1e-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="84e1e-137">Hiermee kunt u verouderde vergoedingsformulieren verbergen.</span><span class="sxs-lookup"><span data-stu-id="84e1e-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="84e1e-138">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="84e1e-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="84e1e-139">Parameters voor Selfservice werknemer configureren</span><span class="sxs-lookup"><span data-stu-id="84e1e-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="84e1e-140">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="84e1e-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="84e1e-141">Geef op het tabblad **Selfservice werknemer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="84e1e-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="84e1e-142">Veld</span><span class="sxs-lookup"><span data-stu-id="84e1e-142">Field</span></span> | <span data-ttu-id="84e1e-143">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="84e1e-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="84e1e-144">**Vergoedingsverificatie**</span><span class="sxs-lookup"><span data-stu-id="84e1e-144">**Benefit verification**</span></span> | <span data-ttu-id="84e1e-145">De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="84e1e-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="84e1e-146">**Begunstigden automatisch selecteren**</span><span class="sxs-lookup"><span data-stu-id="84e1e-146">**Auto select designees**</span></span> | <span data-ttu-id="84e1e-147">Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd op basis van hun geschiktheid voor planopties.</span><span class="sxs-lookup"><span data-stu-id="84e1e-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="84e1e-148">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="84e1e-148">Select **Save**.</span></span>
