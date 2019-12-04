---
title: Gebruiker heeft toegang tot Core HR, maar niet tot Onboard of Attract
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een gebruiker toegang tot Microsoft Dynamics 365 Talent - Core HR krijgt, maar geen toegang heeft tot Attract of Onboard.
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
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772914"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="2c9a4-103">Gebruiker heeft toegang tot Core HR, maar niet tot Onboard of Attract</span><span class="sxs-lookup"><span data-stu-id="2c9a4-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c9a4-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-104">**Environment details**</span></span>

- <span data-ttu-id="2c9a4-105">De implementatie van Microsoft Dynamics Lifecycle Services (LCS) is uitgevoerd door gebruiker A.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="2c9a4-106">Gebruiker A heeft gebruiker B als gebruiker toegevoegd aan Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="2c9a4-107">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-107">**Issue**</span></span>

<span data-ttu-id="2c9a4-108">Gebruiker B heeft toegang tot Core HR, maar kan de app Talent: Attract of Talent: Onboard niet openen.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="2c9a4-109">Wanneer de gebruiker naar **Apps ervaren** probeert te gaan, komt hij of zij in plaats daarvan terecht in een proefomgeving.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="2c9a4-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-110">**Solution**</span></span>

<span data-ttu-id="2c9a4-111">Aan gebruiker B moeten de rechten worden toegewezen die nodig zijn om de Microsoft Power Apps-omgeving weer te geven die gebruiker A heeft gemaakt tijdens het inrichtingsproces.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="2c9a4-112">Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="2c9a4-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="2c9a4-113">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-113">**Long-term solution**</span></span>

<span data-ttu-id="2c9a4-114">Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Core HR.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
