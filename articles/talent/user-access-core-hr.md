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
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "855651"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="1f0c8-103">Gebruiker heeft toegang tot Core HR, maar niet tot de app Onboard of Attract</span><span class="sxs-lookup"><span data-stu-id="1f0c8-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f0c8-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="1f0c8-104">**Environment details**</span></span>

- <span data-ttu-id="1f0c8-105">De implementatie van Microsoft Dynamics Lifecycle Services (LCS) is uitgevoerd door gebruiker A.</span><span class="sxs-lookup"><span data-stu-id="1f0c8-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="1f0c8-106">Gebruiker A heeft gebruiker B als gebruiker toegevoegd aan Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="1f0c8-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="1f0c8-107">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="1f0c8-107">**Issue**</span></span>

<span data-ttu-id="1f0c8-108">Gebruiker B heeft toegang tot Core HR, maar kan de app Talent: Attract of Talent: Onboard niet openen.</span><span class="sxs-lookup"><span data-stu-id="1f0c8-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="1f0c8-109">Wanneer de gebruiker naar **Apps ervaren** probeert te gaan, komt hij of zij in plaats daarvan terecht in een proefomgeving.</span><span class="sxs-lookup"><span data-stu-id="1f0c8-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="1f0c8-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="1f0c8-110">**Solution**</span></span>

<span data-ttu-id="1f0c8-111">Aan gebruiker B moeten de rechten worden toegewezen die nodig zijn om de Microsoft PowerApps-omgeving weer te geven die gebruiker A heeft gemaakt tijdens het inrichtingsproces.</span><span class="sxs-lookup"><span data-stu-id="1f0c8-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="1f0c8-112">Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="1f0c8-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="1f0c8-113">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="1f0c8-113">**Long-term solution**</span></span>

<span data-ttu-id="1f0c8-114">Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Core HR.</span><span class="sxs-lookup"><span data-stu-id="1f0c8-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
