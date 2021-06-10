---
title: Parameters voor Vergoedingenbeheer per bedrijf configureren
description: Parameters voor Vergoedingenbeheer per bedrijf configureren in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057617"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="a7b53-103">Parameters voor Vergoedingenbeheer per bedrijf configureren</span><span class="sxs-lookup"><span data-stu-id="a7b53-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a7b53-104">Voor elke organisatie die vergoedingen biedt, moet u instellingen configureren voor bevestigingse-mails over vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a7b53-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="a7b53-105">Bevestigingse-mailinstellingen configureren</span><span class="sxs-lookup"><span data-stu-id="a7b53-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="a7b53-106">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="a7b53-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="a7b53-107">Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="a7b53-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="a7b53-108">Veld</span><span class="sxs-lookup"><span data-stu-id="a7b53-108">Field</span></span> | <span data-ttu-id="a7b53-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a7b53-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a7b53-110">**Bevestigingse-mail verzenden**</span><span class="sxs-lookup"><span data-stu-id="a7b53-110">**Send confirmation email**</span></span> | <span data-ttu-id="a7b53-111">Als deze functie is ingeschakeld, wordt er een bevestigingsbericht verzonden naar werknemers wanneer ze in Werknemerselfservice niet meer zijn geregistreerd voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a7b53-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="a7b53-112">**Sjabloon bevestigingse-mail**</span><span class="sxs-lookup"><span data-stu-id="a7b53-112">**Confirmation email template**</span></span> | <span data-ttu-id="a7b53-113">Selecteer het e-mailsjabloon van de organisatie voor het verzenden van de inschrijvingsbevestiging.</span><span class="sxs-lookup"><span data-stu-id="a7b53-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="a7b53-114">Als u geen sjabloon selecteert, wordt de volgende e-mail verzonden:</span><span class="sxs-lookup"><span data-stu-id="a7b53-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="a7b53-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="a7b53-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="a7b53-116">Gefeliciteerd!</span><span class="sxs-lookup"><span data-stu-id="a7b53-116">Congratulations!</span></span> <span data-ttu-id="a7b53-117">U bent ingeschreven voor de vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a7b53-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="a7b53-118">Hartelijk dank,</span><span class="sxs-lookup"><span data-stu-id="a7b53-118">Thank you,</span></span><br><span data-ttu-id="a7b53-119"><Naam bedrijf/organisatie> Vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a7b53-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="a7b53-120">**Standaard e-mailadres van afzender**</span><span class="sxs-lookup"><span data-stu-id="a7b53-120">**Default email sender address**</span></span> | <span data-ttu-id="a7b53-121">Het e-mailadres dat moet worden gebruikt voor het verzenden van het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="a7b53-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="a7b53-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="a7b53-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]