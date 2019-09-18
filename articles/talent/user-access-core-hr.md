---
title: Gebruiker heeft toegang tot Core HR, maar niet tot de app Onboard of Attract
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een gebruiker toegang tot Microsoft Dynamics 365 for Talent Core HR krijgt, maar geen toegang heeft tot de app Attract of Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741707"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="6d78a-103">Gebruiker heeft toegang tot Core HR, maar niet tot de app Onboard of Attract</span><span class="sxs-lookup"><span data-stu-id="6d78a-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6d78a-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="6d78a-104">**Environment details**</span></span>

- <span data-ttu-id="6d78a-105">De implementatie van Microsoft Dynamics Lifecycle Services (LCS) is uitgevoerd door gebruiker A.</span><span class="sxs-lookup"><span data-stu-id="6d78a-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="6d78a-106">Gebruiker A heeft gebruiker B als gebruiker toegevoegd aan Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="6d78a-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="6d78a-107">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="6d78a-107">**Issue**</span></span>

<span data-ttu-id="6d78a-108">Gebruiker B heeft toegang tot Core HR, maar kan de app Talent: Attract of Talent: Onboard niet openen.</span><span class="sxs-lookup"><span data-stu-id="6d78a-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="6d78a-109">Wanneer de gebruiker naar **Apps ervaren** probeert te gaan, komt hij of zij in plaats daarvan terecht in een proefomgeving.</span><span class="sxs-lookup"><span data-stu-id="6d78a-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="6d78a-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="6d78a-110">**Solution**</span></span>

<span data-ttu-id="6d78a-111">Aan gebruiker B moeten de rechten worden toegewezen die nodig zijn om de Microsoft PowerApps-omgeving weer te geven die gebruiker A heeft gemaakt tijdens het inrichtingsproces.</span><span class="sxs-lookup"><span data-stu-id="6d78a-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="6d78a-112">Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="6d78a-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="6d78a-113">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="6d78a-113">**Long-term solution**</span></span>

<span data-ttu-id="6d78a-114">Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Core HR.</span><span class="sxs-lookup"><span data-stu-id="6d78a-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
