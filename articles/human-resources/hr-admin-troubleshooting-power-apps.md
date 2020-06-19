---
title: Kan geen omgeving maken in het Power Apps-beheercentrum
description: In dit artikel wordt beschreven wat er moet gebeuren als de beheerder geen omgeving kan maken in het Microsoft Power Apps-beheercentrum.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431056"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="da083-103">Kan geen omgeving maken in het Power Apps-beheercentrum</span><span class="sxs-lookup"><span data-stu-id="da083-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="da083-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="da083-104">**Issue**</span></span>

- <span data-ttu-id="da083-105">De tenant-/omgevingsbeheerder kan geen omgeving maken in het Microsoft Power Apps-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="da083-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="da083-106">Een licentie die gebruikers het recht geeft de stap voor het maken van de omgeving uit te voeren, is niet direct toegewezen aan de gebruiker die deze stap uitvoert.</span><span class="sxs-lookup"><span data-stu-id="da083-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="da083-107">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="da083-107">**Solution**</span></span>

<span data-ttu-id="da083-108">Zorg ervoor dat de tenantbeheerder een geldige Power Apps P2-licentie heeft toegewezen aan de gebruiker die de stap voor het maken van de omgeving uitvoert.</span><span class="sxs-lookup"><span data-stu-id="da083-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="da083-109">Hier vindt u de Microsoft Dynamics-serviceplannen die dit recht bieden.</span><span class="sxs-lookup"><span data-stu-id="da083-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="da083-110">Algemene product-SKU</span><span class="sxs-lookup"><span data-stu-id="da083-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="da083-111">Power Apps P2-serviceplan</span><span class="sxs-lookup"><span data-stu-id="da083-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="da083-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="da083-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="da083-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="da083-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="da083-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="da083-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="da083-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="da083-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="da083-116">Houd er rekening mee dat verschillende Microsoft Office-SKU's ook dit recht verlenen, samen met zelfstandige Power Apps Plan 2-SKU's.</span><span class="sxs-lookup"><span data-stu-id="da083-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="da083-117">Het belangrijkste is dat een van deze SKU's aanwezig moet zijn.</span><span class="sxs-lookup"><span data-stu-id="da083-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="da083-118">Ga naar [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="da083-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="da083-119">Maak de omgeving door de instructies in [Human Resources inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) te volgen.</span><span class="sxs-lookup"><span data-stu-id="da083-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
