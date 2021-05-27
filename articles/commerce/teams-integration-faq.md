---
title: Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams
description: Dit onderwerp bevat antwoorden op veelgestelde vragen met betrekking tot integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams.
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
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019465"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams

[!include [banner](includes/banner.md)]

Dit onderwerp bevat antwoorden op veelgestelde vragen met betrekking tot integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Wie in de winkel wordt eigenaar van een team bij het inrichtgen van Teams vanuit Commerce? 

Alle winkelmanagers worden automatisch toegevoegd als eigenaren aan de bijbehorende teamgroep, zodat ze bewerkingen kunnen uitvoeren, zoals het toevoegen van een privékanaal en het toevoegen of verwijderen van leden. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Hoe wijs ik de rol "communicatiemanager" toe aan een werknemer in Commerce Headquarters? 

Communicatiemanagers in Microsoft Teams kunnen takenlijsten maken en publiceren. Aan organisatiewerknemers die communicatiemanager moeten worden, moet de rol "Taakbeheer detailhandel" worden toegewezen in Commerce Headquarters.

Volg deze stappen om de rol Taakbeheer detailhandel toe te wijzen aan een werknemer in Commerce Headquarters.

1. Ga naar **Detailhandel en commerce \> Werknemers \> Gebruikers**.
1. Selecteer een werknemer.
1. Selecteer op het sneltabblad **Rollen van gebruiker** op **Rollen toewijzen**.
1. Selecteer in het dialoogvenster **Rollen toewijzen aan gebruiker** de rol **Taakbeheer detailhandel** en selecteer vervolgens **OK**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Hoe maak ik een specifieke organisatiehiërarchie beschikbaar om te uploaden naar Microsoft Teams?

In Commerce Headquarters is de hiërarchie van elke organisatie aan een of meer doelen gekoppeld. Zorg ervoor dat aan de hiërarchie die u wilt inrichten in Microsoft Teams het doel **Detailhandelsrapportage** is gekoppeld, zoals in de volgende afbeelding van het voorbeeld wordt weergegeven. 

![Voorbeeld van een organisatiehiërarchiedoel in Commerce Headquarters](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Hoe schakel ik winkelmedewerkers in om zich aan te melden bij Commerce POS (verkooppunt) met Azure Active Directory (Azure AD)?

Zie [Verificatie voor Azure Active Directory inschakelen voor POS-aanmelding](aad-pos-logon.md) voor informatie over het configureren van de aanmeldingservaring van Commerce POS voor het gebruik van Azure AD.

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Hoe wijs ik winkels en overeenkomende teams toe in Commerce Headquarters als mijn organisatie al teams heeft gemaakt in Microsoft Teams?

Zie [Winkels en overeenkomende teams toewijzen indien uw organisatie al bestaande teams heeft in Microsoft Teams](map-stores-existing-teams.md) voor informatie over het toewijzen van winkels en teams.

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Hoe wis ik het Microsoft Graph API-token dat is opgeslagen in de sessieopslag?

Een gebruiker die is aangemeld bij het POS (verkooppunt) met een Azure Active Directory (Azure AD) rekening moet zich aanmelden via het POS of de toepassing sluiten om de sessieopslag te verwijderen. 

> [!TIP]
> Een aanbevolen procedure is om altijd winkelmedewerkers de POS-terminal te laten vergrendelen of zich af te melden voor een sessie wanneer de terminal niet wordt gebruikt. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Wat gebeurt er als een winkel geen winkelmanagers heeft?

Als een winkel geen managers heeft, wordt er geen teamgroep gemaakt voor de winkel of in Teams. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Wat gebeurt er als een winkelmanager het bedrijf verlaat?

Iedereen met de rol Eigenaar kan een nieuwe winkelmanager toevoegen in Commerce Headquarters en Teams opnieuw inrichten, zodat de nieuwe manager over de benodigde rechten in Teams beschikt voor de groep. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams](commerce-teams-integration.md)

[Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen](enable-teams-integration.md)

[Microsoft Teams inrichten vanuit Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Gebruikersrollen beheren in Microsoft Teams](manage-user-roles-teams.md)

[Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn](map-stores-existing-teams.md)
