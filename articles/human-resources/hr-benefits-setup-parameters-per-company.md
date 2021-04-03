---
title: Parameters voor Vergoedingenbeheer per bedrijf configureren
description: Parameters voor Vergoedingenbeheer per bedrijf configureren in Microsoft Dynamics 365 Human Resources.
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
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 31f30c3d268132327074e931b714b5b2ee3ec5ac
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466635"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="2a42c-103">Parameters voor Vergoedingenbeheer per bedrijf configureren</span><span class="sxs-lookup"><span data-stu-id="2a42c-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2a42c-104">Voor elke organisatie die vergoedingen biedt, moet u instellingen configureren voor bevestigingse-mails over vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="2a42c-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="2a42c-105">Bevestigingse-mailinstellingen configureren</span><span class="sxs-lookup"><span data-stu-id="2a42c-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="2a42c-106">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="2a42c-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="2a42c-107">Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="2a42c-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="2a42c-108">Veld</span><span class="sxs-lookup"><span data-stu-id="2a42c-108">Field</span></span> | <span data-ttu-id="2a42c-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2a42c-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2a42c-110">**Bevestigingse-mail verzenden**</span><span class="sxs-lookup"><span data-stu-id="2a42c-110">**Send confirmation email**</span></span> | <span data-ttu-id="2a42c-111">Als deze functie is ingeschakeld, wordt er een bevestigingsbericht verzonden naar werknemers wanneer ze in Werknemerselfservice niet meer zijn geregistreerd voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="2a42c-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="2a42c-112">**Sjabloon bevestigingse-mail**</span><span class="sxs-lookup"><span data-stu-id="2a42c-112">**Confirmation email template**</span></span> | <span data-ttu-id="2a42c-113">Selecteer het e-mailsjabloon van de organisatie voor het verzenden van de inschrijvingsbevestiging.</span><span class="sxs-lookup"><span data-stu-id="2a42c-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="2a42c-114">Als u geen sjabloon selecteert, wordt de volgende e-mail verzonden:</span><span class="sxs-lookup"><span data-stu-id="2a42c-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="2a42c-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="2a42c-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="2a42c-116">Gefeliciteerd!</span><span class="sxs-lookup"><span data-stu-id="2a42c-116">Congratulations!</span></span> <span data-ttu-id="2a42c-117">U bent ingeschreven voor de vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="2a42c-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="2a42c-118">Hartelijk dank,</span><span class="sxs-lookup"><span data-stu-id="2a42c-118">Thank you,</span></span><br><span data-ttu-id="2a42c-119"><Naam bedrijf/organisatie> Vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="2a42c-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="2a42c-120">**Standaard e-mailadres van afzender**</span><span class="sxs-lookup"><span data-stu-id="2a42c-120">**Default email sender address**</span></span> | <span data-ttu-id="2a42c-121">Het e-mailadres dat moet worden gebruikt voor het verzenden van het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="2a42c-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="2a42c-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="2a42c-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]