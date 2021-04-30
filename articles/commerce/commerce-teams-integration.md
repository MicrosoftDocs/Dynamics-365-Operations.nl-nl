---
title: Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams
description: Dit onderwerp geeft een overzicht van integratie tussen Microsoft Dynamics 365 Commerce en Microsoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9289aca4f53eb2ae8f1fa06d5f80b7ee0bbab8e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908462"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams

[!include [banner](includes/banner.md)]

Dit onderwerp geeft een overzicht van integratie tussen Microsoft Dynamics 365 Commerce en Microsoft Teams.

Dynamics 365 Commerce integreert met Teams om klanten en hun medewerkers te helpen de productiviteit te verbeteren door taakbeheer tussen de twee toepassingen te synchroniseren. Met het naadloze taakbeheer dat integratie van Commerce met Teams biedt, kunnen winkelmanagers en werknemers takenlijsten maken, taken toewijzen aan meerdere winkels en de status van taken in verschillende winkels bijhouden vanuit beide toepassingen.

Integratie tussen Commerce en Teams is beschikbaar vanaf Commerce-versie 10.0.18.

## <a name="key-features"></a>Belangrijke functies

Hier zijn enkele van de belangrijkste functies die de integratie van Commerce en Microsoft Teams biedt:

- Teams inrichten door gebruik te maken van goed gedefinieerde informatie uit Commerce, zoals de organisatiestructuur en informatie over winkels, werknemers, machtigingen en bedrijfscontext.
- Eenvoudig lopende wijzigingen (bijvoorbeeld de toevoeging van nieuwe winkels of het aannemen van nieuwe werknemers) tussen Commerce en Teams synchroniseren, waarbij Commerce wordt behouden als hoofdbron van organisatiestructuurgegevens.
- Taakbeheer integreren tussen Commerce en Teams om winkelmedewerkers, winkelmanagers, regiomanagers en communicatiemanagers te helpen taakbeheer vanuit beide toepassingen af te handelen.

## <a name="prerequisites-for-using-integration-features"></a>Vereisten voor het gebruik van integratiefuncties

Aan de volgende vereisten moet worden voldaan voordat u integratiefuncties van Microsoft Teams kunt gaan gebruiken:

- Microsoft 365 Business Standard-licentie (deze licentie bevat Teams.)
- Azure Active Directory (Azure AD) is verantwoordelijk voor alle winkelmanagers en werknemers
- POS-systemen (verkooppunt) die zijn geconfigureerd met Azure AD-verificatie

## <a name="conceptual-architecture"></a>Conceptuele architectuur

In de volgende afbeelding ziet u de conceptuele architectuur van integratie van Dynamics 365 Commerce en Microsoft Teams, met een winkel in San Francisco als voorbeeld. Zowel Teams als de Commerce POS-toepassing gebruiken Microsoft Planner als opslagplaats, zodat taken die vanuit Teams worden gepubliceerd, in de POS-toepassing worden weergegeven en ad-hoctaken die door winkelmanagers in de POS-toepassing zijn gemaakt in Teams worden weergegeven, wat resulteert in een naadloze taakbeheerervaring tussen de toepassingen.    

![Architectuur van integratie van Commerce met Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen](enable-teams-integration.md)

[Microsoft Teams inrichten vanuit Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Gebruikersrollen beheren in Microsoft Teams](manage-user-roles-teams.md)

[Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn](map-stores-existing-teams.md)

[Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams](teams-integration-faq.md)
