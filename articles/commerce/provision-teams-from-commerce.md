---
title: Microsoft Teams inrichten vanuit Dynamics 365 Commerce
description: In dit onderwerp wordt beschreven hoe u Microsoft Teams inricht met behulp van organisatiegegevens vanuit Dynamics 365 Commerce.
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
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842645"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Microsoft Teams inrichten vanuit Dynamics 365 Commerce

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u Microsoft Teams inricht met behulp van organisatiegegevens vanuit Dynamics 365 Commerce.

Dynamics 365 Commerce biedt een eenvoudige manier om Teams in te richten als u nog geen teams hebt ingesteld voor uw winkels daar. Door gebruik te maken van goed gedefinieerde informatie uit Commerce die u wilt gebruiken in Teams, kunt u uw winkelmedewerkers helpen aan de slag te gaan in Teams. Deze informatie omvat de organisatiehiërarchie, winkelnamen, werknemergegevens en Azure Active Directory (Azure AD) rekeningen. 

Het inrichtingsproces voor Teams telt twee hoofdstappen:

1. Maak in Teams een team voor elke winkel en voeg winkelmedewerkers toe als leden van het relevante team. Als een werknemer aan meerdere winkels is gekoppeld, blijkt dit uit het teamlidmaatschap. Er wordt een communicatieteam met regionale managers als leden gemaakt om te helpen bij het publiceren van taken vanuit Teams.
1. Upload de organisatiehiërarchie van Commerce naar Teams.

## <a name="provision-teams-in-commerce-headquarters"></a>Teams inrichten in Commerce Headquarters

Voltooi deze taken voordat u Microsoft Teams gaat inrichten:

- Bevestig dat alle regionale managers tot communicatiemanagers zijn gemaakt.
- Bevestig dat de Azure-rekening van elke winkelmanager en -medewerker is gekoppeld aan de werknemersrecord van die manager of medewerker in Commerce Headquarters.

Voer de volgende stappen uit om Teams in te richten in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Microsoft Teams-integratieconfiguratie**.
1. Selecteer **Teams inrichten** in het actievenster. Er wordt een batchtaak met de naam **Teams inrichten** gemaakt.
1. Ga naar **Systeembeheer \> Query's \> Batchtaken** en zoek de meest recente taak met de beschrijving **Teams inrichten**. Wacht tot deze taak is voltooid.

> [!TIP]
> Als geen van uw regiomanagers, winkelmanagers en winkelmedewerkers aan een Teams-licentie is gekoppeld, ontvangt u mogelijk het volgende foutbericht: 'Het ophalen van toepasselijke Sku-categorieën voor de gebruiker is mislukt'. U kunt dit probleem oplossen door **Teams en leden synchroniseren** te selecteren in het actievenster.

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Inrichting van Teams valideren in het Teams-beheercentrum

Volg deze stappen om de inrichting van Microsoft Teams in het Microsoft Teams-beheercentrum te valideren.
    
1. Ga naar het [Teams-beheercentrum](https://admin.teams.microsoft.com/)en meld u aan als beheerder van uw e-commerce-tenant.
1. Selecteer in het linkernavigatievenster de optie **Teams** om deze uit te vouwen en selecteer vervolgens **Teams beheren**.
1. Bevestig dat er één team is gemaakt voor elke winkel van Commerce.
1. Selecteer een team en bevestig dat winkelmedewerkers als leden zijn toegevoegd aan het team.
1. Selecteer **Gebruikers** in het linkernavigatievenster en bevestig dat alle winkelwerknemers in alle winkels als gebruikers zijn toegevoegd.

In de volgende afbeelding ziet u een voorbeeld van de pagina **Teams beheren** in het Teams-beheercentrum.

![Voorbeeld van de pagina Teams beheren in het Teams-beheercentrum](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Een Commerce-organisatiehiërarchie uploaden naar Teams
    
De Commerce-organisatiehiërarchie kan worden gebruikt in Microsoft Teams om taken te publiceren naar alle of geselecteerde winkels met dezelfde hiërarchiestructuur.

Volg deze stappen om een Commerce-organisatiehiërarchie te uploaden naar Teams.
    
1. Ga in Commerce Headquarters naar **Retail en commerce \> Afzetkanaalinstellingen \> Configuratie van Microsoft Teams-integratie**.
1. Selecteer **Doelgroephiërarchie downloaden** en selecteer vervolgens **Detailhandelwinkels per regio** om een CSV-bestand (Comma Separated Values) van de organisatiehiërarchie te downloaden.
1. Installeer de Microsoft Teams PowerShell-module door de stappen in [Microsoft Teams PowerShell installeren](https://docs.microsoft.com/microsoftteams/teams-powershell-install) te volgen.
1. Wanneer u wordt gevraagd in het Teams PowerShell-venster, meldt u zich aan met het beheerdersaccount voor uw Azure AD-tenant.
1. Volg de stappen in [De doelgroephiërarchie voor uw team instellen](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) om het CSV-bestand voor de doelgroephiërarchie te uploaden.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Controleren of de organisatiehiërarchie naar Teams is geüpload

Volg deze stappen om te controleren of de organisatiehiërarchie is geüpload naar Microsoft Teams.

1. Meld u als communicatiemanager aan bij Teams.
1. Selecteer **Taken per planner** in het linkernavigatievenster.
1. Maak op het tabblad **Gepubliceerde lijsten** een nieuwe lijst met een dummy taak.
1. Selecteer **Publiceren**. De organisatiehiërarchie moet worden weergegeven in het dialoogvenster **Selecteren wie moet worden gepubliceerd**, zoals in het voorbeeld in de volgende afbeelding is weergegeven.

![Voorbeeld van een organisatiehiërarchie in het dialoogvenster Selecteren wie moet worden gepubliceerd](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams](commerce-teams-integration.md)

[Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen](enable-teams-integration.md)

[Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Gebruikersrollen beheren in Microsoft Teams](manage-user-roles-teams.md)

[Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn](map-stores-existing-teams.md)

[Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams](teams-integration-faq.md)
