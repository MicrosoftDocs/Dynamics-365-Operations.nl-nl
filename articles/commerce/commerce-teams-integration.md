---
title: Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams
description: Dit onderwerp geeft een overzicht van integratie tussen Microsoft Dynamics 365 Commerce en Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021984"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="de2f5-103">Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="de2f5-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de2f5-104">Dit onderwerp geeft een overzicht van integratie tussen Microsoft Dynamics 365 Commerce en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="de2f5-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="de2f5-105">Dynamics 365 Commerce integreert met Teams om klanten en hun medewerkers te helpen de productiviteit te verbeteren door taakbeheer tussen de twee toepassingen te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="de2f5-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="de2f5-106">Met het naadloze taakbeheer dat integratie van Commerce met Teams biedt, kunnen winkelmanagers en werknemers takenlijsten maken, taken toewijzen aan meerdere winkels en de status van taken in verschillende winkels bijhouden vanuit beide toepassingen.</span><span class="sxs-lookup"><span data-stu-id="de2f5-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="de2f5-107">Integratie tussen Commerce en Teams is beschikbaar vanaf Commerce-versie 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="de2f5-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="de2f5-108">Belangrijke functies</span><span class="sxs-lookup"><span data-stu-id="de2f5-108">Key features</span></span>

<span data-ttu-id="de2f5-109">Hier zijn enkele van de belangrijkste functies die de integratie van Commerce en Microsoft Teams biedt:</span><span class="sxs-lookup"><span data-stu-id="de2f5-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="de2f5-110">Teams inrichten door gebruik te maken van goed gedefinieerde informatie uit Commerce, zoals de organisatiestructuur en informatie over winkels, werknemers, machtigingen en bedrijfscontext.</span><span class="sxs-lookup"><span data-stu-id="de2f5-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="de2f5-111">Eenvoudig lopende wijzigingen (bijvoorbeeld de toevoeging van nieuwe winkels of het aannemen van nieuwe werknemers) tussen Commerce en Teams synchroniseren, waarbij Commerce wordt behouden als hoofdbron van organisatiestructuurgegevens.</span><span class="sxs-lookup"><span data-stu-id="de2f5-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="de2f5-112">Taakbeheer integreren tussen Commerce en Teams om winkelmedewerkers, winkelmanagers, regiomanagers en communicatiemanagers te helpen taakbeheer vanuit beide toepassingen af te handelen.</span><span class="sxs-lookup"><span data-stu-id="de2f5-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="de2f5-113">Vereisten voor het gebruik van integratiefuncties</span><span class="sxs-lookup"><span data-stu-id="de2f5-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="de2f5-114">Aan de volgende vereisten moet worden voldaan voordat u integratiefuncties van Microsoft Teams kunt gaan gebruiken:</span><span class="sxs-lookup"><span data-stu-id="de2f5-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="de2f5-115">Microsoft 365 Business Standard-licentie (deze licentie bevat Teams.)</span><span class="sxs-lookup"><span data-stu-id="de2f5-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="de2f5-116">Azure Active Directory (Azure AD) is verantwoordelijk voor alle winkelmanagers en werknemers</span><span class="sxs-lookup"><span data-stu-id="de2f5-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="de2f5-117">POS-systemen (verkooppunt) die zijn geconfigureerd met Azure AD-verificatie</span><span class="sxs-lookup"><span data-stu-id="de2f5-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="de2f5-118">Conceptuele architectuur</span><span class="sxs-lookup"><span data-stu-id="de2f5-118">Conceptual architecture</span></span>

<span data-ttu-id="de2f5-119">In de volgende afbeelding ziet u de conceptuele architectuur van integratie van Dynamics 365 Commerce en Microsoft Teams, met een winkel in San Francisco als voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="de2f5-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="de2f5-120">Zowel Teams als de Commerce POS-toepassing gebruiken Microsoft Planner als opslagplaats, zodat taken die vanuit Teams worden gepubliceerd, in de POS-toepassing worden weergegeven en ad-hoctaken die door winkelmanagers in de POS-toepassing zijn gemaakt in Teams worden weergegeven, wat resulteert in een naadloze taakbeheerervaring tussen de toepassingen.</span><span class="sxs-lookup"><span data-stu-id="de2f5-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Architectuur van integratie van Commerce met Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="de2f5-122">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="de2f5-122">Additional resources</span></span>

[<span data-ttu-id="de2f5-123">Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen</span><span class="sxs-lookup"><span data-stu-id="de2f5-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="de2f5-124">Microsoft Teams inrichten vanuit Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de2f5-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="de2f5-125">Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="de2f5-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="de2f5-126">Gebruikersrollen beheren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="de2f5-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="de2f5-127">Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn</span><span class="sxs-lookup"><span data-stu-id="de2f5-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="de2f5-128">Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="de2f5-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
