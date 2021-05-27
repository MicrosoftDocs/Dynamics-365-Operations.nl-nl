---
title: Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen
description: In dit onderwerp wordt beschreven hoe u integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams inschakelt.
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
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019830"
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
1. Kopieer de waarde van **Id van toepassing (client)** vanaf de pagina **Overzicht** voor de geregistreerde app. U gebruikt deze waarde om Teams-integratie mogelijk te maken in Commerce Headquarters.
1. Kopieer de certificaatwaarde die werd ingevoerd bij het [toevoegen van een certificaat](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in stap 1. Het certificaat wordt ook wel de openbare sleutel of toepassingssleutel genoemd. U gebruikt deze waarde om Teams-integratie mogelijk te maken in Commerce Headquarters.

Voer de volgende stappen uit om Teams-integratie in te schakelen in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Microsoft Teams-integratieconfiguratie**.
1. Selecteer **Bewerken** in het actievenster.
1. Stel de optie **Microsoft Teams-integratie inschakelen** in op **Ja**.
1. Voer in de velden **Toepassings-id** en **Toepassingssleutel** de waarden in die u hebt verkregen toen u de Teams-toepassing registreerde in de Azure-portal.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van de configuratie van Teams-integratie in Commerce Headquarters.

![Configuratie van Teams-integratie in Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

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