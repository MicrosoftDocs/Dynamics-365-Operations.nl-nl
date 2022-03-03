---
title: Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen
description: In dit onderwerp wordt beschreven hoe u integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams inschakelt.
author: gvrmohanreddy
ms.date: 02/17/2021
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
ms.openlocfilehash: 52b1a889a15cfe2e6e104e38b7d257f80762954f
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323425"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams inschakelt.

Als u Teams wilt voorzien van informatie uit Dynamics 365 Commerce en de functies voor taakbeheer tussen Teams en de POS-toepassing (verkooppunt) wilt synchroniseren, moet u de integratiefuncties in Commerce Headquarters inschakelen.

> [!NOTE]
> Wanneer u Teams-integratie inschakelt, stemt u ermee in uw gegevens met Teams te delen. Gegevens die met Teams worden gedeeld, bevinden zich mogelijk in een ander land dan uw Commerce-gegevens en zijn mogelijk onderworpen aan andere nalevingsnormen. Zie het [Microsoft Vertrouwenscentrum](https://www.microsoft.com/trust-center) voor meer informatie. Zie de [privacyverklaring van Microsoft](https://aka.ms/privacy) voor informatie over het privacybeleid van Microsoft.

## <a name="enable-teams-integration"></a>Teams-integratie inschakelen

Voordat u Microsoft Teams-integratie met Commerce inschakelt, moet u de Teams-toepassing registreren bij uw tenant in de Azure-portal.

Volg deze stappen om de Teams-toepassing te registreren bij uw tenant in de Azure-portal.

1. Volg de stappen in [Snelstart: Een app registreren op het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app) om de Teams-toepassing te registreren bij uw tenant in de Azure-portal.
1. Selecteer op het tabblad **Appregistratie** de app die in de vorige stap hebt gemaakt. Selecteer vervolgens **Een platform toevoegen** op het tabblad **Verificatie**.
1. Selecteer **Web** in het dialoogvenster. Voer vervolgens in het veld **Omleidings-URL's** een URL in de notatie **\<HQUrl\>/oauth** in. Vervang **\<HQUrl\>** door uw Commerce Headquarters-URL (bijvoorbeeld `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Kopieer op de pagina de waarde voor **Id van toepassing (client)** op de pagina **Overzicht** van de geregistreerde app. U moet deze waarde opgeven om in de volgende sectie Teams-integratie mogelijk te maken in Commerce Headquarters.
1. Volg de instructies in [Een clientgeheim toevoegen](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) om een clientgeheim toe te voegen. Kopieer vervolgens de waarde voor **Geheime waarde** voor de client. U moet deze waarde opgeven om in de volgende sectie Teams-integratie mogelijk te maken in Commerce Headquarters.
1. Selecteer **API-machtigingen** en selecteer vervolgens **Een machtiging toevoegen**.
1. Selecteer in het dialoogvenster **API-machtigingen aanvragen** de optie **Microsoft Graph**, selecteer **Gedelegeerde machtigingen**, vouw **Groep** uit, selecteer **Group.ReadWrite.All** en selecteer **Machtigingen toevoegen**.
1. Selecteer in het dialoogvenster **API-machtigingen aanvragen** de optie **Een machtiging toevoegen**, selecteer **Microsoft Graph** en **Toepassingsmachtigingen**, vouw **Groep** uit, selecteer **Group.ReadWrite.All** en selecteer **Machtigingen toevoegen**.
1. Selecteer **Een machtiging toevoegen** in het dialoogvenster **API-machtigingen aanvragen**. Zoek op het tabblad **API's die mijn organisatie gebruikt** naar **Microsoft Teams Retail Service** en selecteer dit.
1. Selecteer **Gedelegeerde machtigingen**, vouw **TaskPublishing** uit, selecteer **TaskPubllish.ReadWrite.All** en selecteer **Machtigingen toevoegen**. Zie [Een clienttoepassing configureren voor toegang tot een web-API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis) voor meer informatie.

Voer de volgende stappen uit om Teams-integratie in te schakelen in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Microsoft Teams-integratieconfiguratie**.
1. Selecteer **Bewerken** in het actievenster.
1. Stel de optie **Microsoft Teams-integratie inschakelen** in op **Ja**.
1. Voer in het veld **Toepassings-id** de waarde voor **Id van toepassing (client)** in die u hebt verkregen toen u de Teams-toepassing registreerde in de Azure-portal.
1. Voer in het veld **Toepassingssleutel** de waarde voor **Geheime waarde** in die u hebt verkregen toen u een clientgeheim toevoegde in de Azure-portal.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van de configuratie van Teams-integratie in Commerce Headquarters.

![Configuratie van Teams-integratie in Commerce Headquarters.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Teams-integratie uitschakelen

Voer de volgende stappen uit om Microsoft Teams-integratie uit te schakelen in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Microsoft Teams-integratieconfiguratie**.
1. Selecteer **Bewerken** in het actievenster.
3. Stel de optie **Microsoft Teams-integratie inschakelen** in op **Nee**.
4. Wis de waarden uit de velden **Toepassings-id** en **Toepassingssleutel**.
1. Selecteer **Opslaan** in het actievenster.

> [!NOTE]
> Nadat u Teams-integratie met Commerce hebt uitgeschakeld, worden in POS-terminals geen taken meer weergegeven die zijn gepubliceerd vanuit de Teams-toepassing.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams](commerce-teams-integration.md)

[Microsoft Teams inrichten vanuit Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Gebruikersrollen beheren in Microsoft Teams](manage-user-roles-teams.md)

[Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn](map-stores-existing-teams.md)

[Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams](teams-integration-faq.md)
