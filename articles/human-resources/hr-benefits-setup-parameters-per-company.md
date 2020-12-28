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
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692740"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="ac6fc-103">Parameters voor Vergoedingenbeheer per bedrijf configureren</span><span class="sxs-lookup"><span data-stu-id="ac6fc-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="ac6fc-104">Voor elke organisatie die vergoedingen biedt, moet u instellingen configureren voor bevestigingse-mails over vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="ac6fc-105">Bevestigingse-mailinstellingen configureren</span><span class="sxs-lookup"><span data-stu-id="ac6fc-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="ac6fc-106">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="ac6fc-107">Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="ac6fc-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="ac6fc-108">Veld</span><span class="sxs-lookup"><span data-stu-id="ac6fc-108">Field</span></span> | <span data-ttu-id="ac6fc-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ac6fc-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ac6fc-110">**Bevestigingse-mail verzenden**</span><span class="sxs-lookup"><span data-stu-id="ac6fc-110">**Send confirmation email**</span></span> | <span data-ttu-id="ac6fc-111">Als deze functie is ingeschakeld, wordt er een bevestigingsbericht verzonden naar werknemers wanneer ze in Werknemerselfservice niet meer zijn geregistreerd voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="ac6fc-112">**Sjabloon bevestigingse-mail**</span><span class="sxs-lookup"><span data-stu-id="ac6fc-112">**Confirmation email template**</span></span> | <span data-ttu-id="ac6fc-113">Selecteer het e-mailsjabloon van de organisatie voor het verzenden van de inschrijvingsbevestiging.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="ac6fc-114">Als u geen sjabloon selecteert, wordt de volgende e-mail verzonden:</span><span class="sxs-lookup"><span data-stu-id="ac6fc-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="ac6fc-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="ac6fc-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="ac6fc-116">Gefeliciteerd!</span><span class="sxs-lookup"><span data-stu-id="ac6fc-116">Congratulations!</span></span> <span data-ttu-id="ac6fc-117">U bent ingeschreven voor de vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="ac6fc-118">Hartelijk dank,</span><span class="sxs-lookup"><span data-stu-id="ac6fc-118">Thank you,</span></span><br><span data-ttu-id="ac6fc-119"><Naam bedrijf/organisatie> Vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="ac6fc-120">**Standaard e-mailadres van afzender**</span><span class="sxs-lookup"><span data-stu-id="ac6fc-120">**Default email sender address**</span></span> | <span data-ttu-id="ac6fc-121">Het e-mailadres dat moet worden gebruikt voor het verzenden van het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="ac6fc-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ac6fc-122">Select **Save**.</span></span>