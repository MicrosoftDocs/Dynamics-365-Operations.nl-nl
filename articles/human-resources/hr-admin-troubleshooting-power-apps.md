---
title: Kan geen omgeving maken in het Power Apps-beheercentrum
description: In dit artikel wordt beschreven wat er moet gebeuren als de beheerder geen omgeving kan maken in het Microsoft Power Apps-beheercentrum.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112077"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="cde2f-103">Kan geen omgeving maken in het Power Apps-beheercentrum</span><span class="sxs-lookup"><span data-stu-id="cde2f-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="cde2f-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="cde2f-104">**Issue**</span></span>

- <span data-ttu-id="cde2f-105">De tenant-/omgevingsbeheerder kan geen omgeving maken in het Microsoft Power Apps-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="cde2f-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="cde2f-106">De gebruiker heeft geen licentie die het recht geeft om omgevingen te maken.</span><span class="sxs-lookup"><span data-stu-id="cde2f-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="cde2f-107">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="cde2f-107">**Solution**</span></span>

<span data-ttu-id="cde2f-108">Zorg ervoor dat de tenantbeheerder een geldige Power Apps P2-licentie heeft toegewezen aan de gebruiker die de omgeving maakt.</span><span class="sxs-lookup"><span data-stu-id="cde2f-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="cde2f-109">De volgende Microsoft Dynamics-serviceabonnementen bieden machtigingen voor het maken van omgevingen:</span><span class="sxs-lookup"><span data-stu-id="cde2f-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="cde2f-110">Algemene product-SKU</span><span class="sxs-lookup"><span data-stu-id="cde2f-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="cde2f-111">Power Apps P2-serviceplan</span><span class="sxs-lookup"><span data-stu-id="cde2f-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="cde2f-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="cde2f-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="cde2f-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cde2f-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="cde2f-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="cde2f-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="cde2f-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cde2f-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="cde2f-116">Houd er rekening mee dat verschillende Microsoft Office-SKU's ook dit recht verlenen, samen met zelfstandige Power Apps Plan 2-SKU's.</span><span class="sxs-lookup"><span data-stu-id="cde2f-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="cde2f-117">Het belangrijkste is dat een van deze SKU's aanwezig moet zijn.</span><span class="sxs-lookup"><span data-stu-id="cde2f-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="cde2f-118">Ga naar [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="cde2f-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="cde2f-119">Maak de omgeving door de instructies in [Human Resources inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) te volgen.</span><span class="sxs-lookup"><span data-stu-id="cde2f-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
