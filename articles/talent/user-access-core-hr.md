---
title: Gebruiker heeft toegang tot Human Resources, maar niet tot de app Onboard of Attract
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een gebruiker toegang tot Microsoft Dynamics 365 Talent - Human Resources krijgt, maar geen toegang heeft tot Attract of Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006305"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="cd9c4-103">Gebruiker heeft toegang tot Human Resources, maar niet tot de app Onboard of Attract</span><span class="sxs-lookup"><span data-stu-id="cd9c4-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd9c4-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="cd9c4-104">**Environment details**</span></span>

- <span data-ttu-id="cd9c4-105">De implementatie van Microsoft Dynamics Lifecycle Services (LCS) is uitgevoerd door gebruiker A.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="cd9c4-106">Gebruiker A heeft gebruiker B als gebruiker toegevoegd aan Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cd9c4-107">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="cd9c4-107">**Issue**</span></span>

<span data-ttu-id="cd9c4-108">Gebruiker B heeft toegang tot Human Resources, maar kan de app Talent: Attract of Talent: Onboard niet openen.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="cd9c4-109">Wanneer de gebruiker naar **Apps ervaren** probeert te gaan, komt hij of zij in plaats daarvan terecht in een proefomgeving.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="cd9c4-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="cd9c4-110">**Solution**</span></span>

<span data-ttu-id="cd9c4-111">Aan gebruiker B moeten de rechten worden toegewezen die nodig zijn om de Microsoft Power Apps-omgeving weer te geven die gebruiker A heeft gemaakt tijdens het inrichtingsproces.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="cd9c4-112">Zie voor meer informatie de sectie Toegang verlenen tot de omgeving in [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="cd9c4-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="cd9c4-113">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="cd9c4-113">**Long-term solution**</span></span>

<span data-ttu-id="cd9c4-114">Microsoft overweegt automatisch de juiste rechten voor Onboard en Attract toe te wijzen wanneer een gebruiker wordt toegevoegd aan Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
