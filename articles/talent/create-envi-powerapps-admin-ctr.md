---
title: Kan geen omgeving maken in het PowerApps-beheercentrum
description: In dit onderwerp wordt beschreven wat er moet gebeuren als de beheerder geen omgeving kan maken in het Microsoft PowerApps-beheercentrum.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303949"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="99d71-103">Kan geen omgeving maken in het PowerApps-beheercentrum</span><span class="sxs-lookup"><span data-stu-id="99d71-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99d71-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="99d71-104">**Issue**</span></span>

- <span data-ttu-id="99d71-105">De tenant-/omgevingsbeheerder kan geen omgeving maken in het Microsoft PowerApps-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="99d71-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="99d71-106">Een licentie die gebruikers het recht geeft de stap voor het maken van de omgeving uit te voeren, is niet direct toegewezen aan de gebruiker die deze stap uitvoert.</span><span class="sxs-lookup"><span data-stu-id="99d71-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="99d71-107">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="99d71-107">**Solution**</span></span>

<span data-ttu-id="99d71-108">Zorg ervoor dat de tenantbeheerder een geldige PowerApps P2-licentie heeft toegewezen aan de gebruiker die de stap voor het maken van de omgeving uitvoert.</span><span class="sxs-lookup"><span data-stu-id="99d71-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="99d71-109">Hier vindt u de Microsoft Dynamics-serviceplannen die dit recht bieden.</span><span class="sxs-lookup"><span data-stu-id="99d71-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="99d71-110">Algemene product-SKU</span><span class="sxs-lookup"><span data-stu-id="99d71-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="99d71-111">PowerApps P2-serviceplan</span><span class="sxs-lookup"><span data-stu-id="99d71-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="99d71-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="99d71-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="99d71-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="99d71-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="99d71-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="99d71-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="99d71-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="99d71-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="99d71-116">Houd er rekening mee dat verschillende Microsoft Office-SKU's ook dit recht verlenen, samen met zelfstandige PowerApps Plan 2-SKU's.</span><span class="sxs-lookup"><span data-stu-id="99d71-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="99d71-117">Het belangrijkste is dat een van deze SKU's aanwezig moet zijn.</span><span class="sxs-lookup"><span data-stu-id="99d71-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="99d71-118">Ga naar [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="99d71-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="99d71-119">Maak de omgeving door de instructies in [Talent inrichten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) te volgen.</span><span class="sxs-lookup"><span data-stu-id="99d71-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
