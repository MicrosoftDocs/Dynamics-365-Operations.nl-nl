---
title: Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS
description: In dit onderwerp wordt beschreven hoe u taakbeheer synchroniseert tussen Microsoft Teams en Dynamics 365 Commerce POS (verkooppunt).
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
ms.openlocfilehash: f9abebbf8d6c5dd6695b9697361e1a9a9e6005dc3ded16c4211c9c5c9e34a0b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730870"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u taakbeheer synchroniseert tussen Microsoft Teams en Dynamics 365 Commerce POS (verkooppunt).

Een van de belangrijkste doelen van Teams-integratie is het inschakelen van de synchronisatie van taakbeheer tussen de POS-toepassing en Teams. Op deze manier kunnen winkelmedewerkers de POS-toepassing of Teams gebruiken om taken te beheren en hoeven ze niet over te schakelen.

Omdat Planner wordt gebruikt als opslagplaats voor taken in Teams, moet er een koppeling zijn tussen Teams en Dynamics 365 Commerce. Deze koppeling wordt tot stand gebracht met een specifieke plan-id voor een bepaald winkelteam.

In de volgende procedures wordt aangegeven hoe u synchronisatie van taakbeheer kunt instellen tussen de POS- en Teams-toepassingen.

## <a name="publish-a-test-task-list-in-teams"></a>Een testtakenlijst publiceren in Teams

In de volgende procedure wordt ervan uitgegaan dat uw winkelteams voor het eerst gebruikmaken van Microsoft Teams-taakbeheerintegratie met Commerce.

Volg deze stappen om een testtakenlijst te publiceren in Teams.

1. Meld u als communicatiemanager aan bij Teams. Meestal zijn communicatiemanagers gebruikers met de rol **Regiomanager** in Commerce.
1. Selecteer **Taken per planner** in het linkernavigatievenster.
1. Selecteer op het tabblad **Gepubliceerde lijsten** de optie **Nieuwe lijst** linksonder en geef de nieuwe lijst **Testtakenlijst** een naam.
1. Selecteer **Maken**. De nieuwe lijst wordt weergegeven onder **Concepten**.
1. Geef onder **Taaktitel** de eerste taak de titel **Teams-Integratie testen**. Selecteer vervolgens **Enter**.
1. Selecteer de takenlijst in de lijst **Concepten**. Selecteer vervolgens **Publiceren** in de rechterbovenhoek.
1. Selecteer in het dialoogvenster **Selecteren wie moet worden gepubliceerd** de teams die de testtakenlijst moeten ontvangen.
1. Selecteer **Volgende** om uw publicatieplan te bekijken. Als u wijzigingen moet aanbrengen, selecteert u **Terug**. 
1. Selecteer **Bevestigen om door te gaan**  en selecteer vervolgens **Publiceren**.
1. Nadat de publicatie is voltooid, wordt er een bericht boven aan het tabblad **Gepubliceerde lijsten** weergegeven waarin wordt aangegeven of uw takenlijst is geleverd.

Zie [Takenlijsten publiceren om werk in uw organisatie te maken en te volgen](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df) voor meer informatie.

## <a name="link-pos-and-teams-for-task-management"></a>POS en Teams koppelen voor taakbeheer

Volg deze stappen om de toepassingen POS en Microsoft Teams te koppelen voor taakbeheer in Commerce Headquarters.

1. Ga naar **Retail en commerce \> Taakbeheer \> Takenintegratie met Microsoft Teams**.
1. Selecteer **Bewerken** in het actievenster.
1. Stel de optie **Integratie van taakbeheer inschakelen** in op **Ja**.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer **Taakbeheer instellen** in het actievenster. U moet een melding ontvangen dat een batchtaak met de naam **Teams inrichten** wordt gemaakt.
1. Ga naar **Systeembeheer \> Query's \> Batchtaken** en zoek de meest recente taak met de beschrijving **Teams inrichten**. Wacht tot deze taak is voltooid.
1. Voer **CDX-taak 1070** uit om de plan-id en winkelverwijzingen te publiceren naar Retail Server.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams](commerce-teams-integration.md)

[Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen](enable-teams-integration.md)

[Microsoft Teams inrichten vanuit Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Gebruikersrollen beheren in Microsoft Teams](manage-user-roles-teams.md)

[Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn](map-stores-existing-teams.md)

[Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams](teams-integration-faq.md)
