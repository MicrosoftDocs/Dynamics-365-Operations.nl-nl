---
title: Module Commerce-chat met Power Virtual Agents
description: In dit artikel wordt de module Commerce-chat met Power Virtual Agents beschreven die Microsoft Power Virtual Agents integreert met Dynamics 365 Commerce-websites .
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691061"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Module Commerce-chat met Power Virtual Agents

[!include [banner](includes/banner.md)]

In dit artikel wordt de module Commerce-chat met Power Virtual Agents beschreven die Microsoft Power Virtual Agents integreert met Dynamics 365 Commerce-websites .

Met de functie Commerce-chat met Power Virtual Agents kunnen e-commerceklanten van Dynamics 365 gebruikmaken van Power Virtual Agents-chatbots om query's af te handelen. Vanaf release 10.0.30 van Dynamics 365 Commerce kan deze functie worden opgenomen in e-commercewebsites met de module Commerce-chat met Power Virtual Agents die deel uitmaakt van de Commerce-modulebibliotheek.

Met de functie Commerce-chat met Power Virtual Agents kunnen bedrijven de volgende doelen behalen:

- Gepersonaliseerde interactie met hun klanten en de klantenbinding verbeteren.
- De klantenservice verbeteren door de integratie van selfservice chatbots.
- De algehele klanttevredenheid verbeteren en zo de verkoop verhogen.

> [!NOTE]
> Zie [Overzicht van Commerce-chatmodules](/commerce-chat-modules-overview.md) voor meer informatie over de verschillen tussen Dynamics 365 Omnichannel voor Customer Service en Power Virtual Agents.

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Vereisten voor het gebruik van Power Virtual Agents

Als u de functie Commerce-chat met Power Virtual Agents wilt gebruiken, moet u eerst een Power Virtual Agents-chatbot maken voor uw e-commercewebsite. Zie [Een Power Virtual Agents-bot maken](/power-virtual-agents/authoring-first-bot) voor instructies.

Nadat u de chatbot hebt geconfigureerd, moet u de waarden van de chatbotparameters **Bot-id** en **Tenant-id** kopiëren om de Commerce-chatervaring te configureren. Zie [Uw Power Virtual Agents-botparameters ophalen](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters) voor informatie over het kopiëren van deze waarden.

## <a name="configure-your-e-commerce-site"></a>Uw e-commercesite configureren 

Een van de aanbevolen manieren om de chatervaring voor uw e-commercesite te implementeren, is door de module Commerce-chat met Power Virtual Agents toe te voegen aan het gedeelde koptekstfragment dat op uw sitepagina's wordt gebruikt.

Voer de volgende stappen uit om de chatmodule toe te voegen aan het koptekstfragment van uw site in Commerce Site Builder.

1. Ga op uw site in Commerce site builder naar **Fragmenten**.
1. Selecteer **Nieuw**.
1. Selecteer in het dialoogvenster **Fragment selecteren** de module **Commerce-chat met Power Virtual Agents**, voer een naam voor het fragment in en selecteer **OK**.
1. Selecteer in de overzichtsweergave het vak **Msdyn365 pva chat connector**.
1. Volg deze stappen in het deelvenster aan de rechterkant:

    1. Laat onder **Botparameters** in het veld **CDN URL voor Bot Framework Webchat-chats** de standaardwaarde (bijvoorbeeld `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`) ongewijzigd.
    1. Laat in het veld **Verificatie-URL voor Bot Framework Direct Line** de standaardwaarde (bijvoorbeeld `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`) ongewijzigd.
    1. Voer in het veld **Bot-id** de Power Virtual Agents-waarde voor **Bot-id** in die u hebt gekopieerd in de sectie [Vereisten voor het gebruik van Power Virtual Agents](#prereq).
    1. Geef in het veld **Tenant-id** de waarde voor **tenant-id** op die u hebt gekopieerd.

1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.
1. Ga naar **Fragmenten** en open het koptekstfragment voor uw site.
1. Selecteer in het vak **Standaardcontainer** het beletselteken (**...**) en selecteer vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** het chatfragment dat u eerder hebt gemaakt, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.

## <a name="proactive-chat-parameters"></a>Proactieve chatparameters

Zie [Proactieve chatparameters voor Commerce-chatmodule](chat-proactive-chat-parameters.md) voor een volledige lijst met configuratieparameters voor proactieve chats.

> [!NOTE]
> Momenteel biedt Power Virtual Agents geen ondersteuning voor Azure Active Directory B2C-verifiatie (Azure AD B2C). Alleen anonieme RCSU-aanroepen (Retail Cloud Scale Unit) voor de productbeschikbaarheid of interactie met andere anonieme API's worden ondersteund. Voor aanroepen naar geverifieerde API's via Power Virtual Agents-chatbots is een expliciete klantaanmelding vereist.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van chatfuncties voor Commerce](commerce-chat-overview.md)

[Commerce Chat met module Omnichannel voor Customer Service](commerce-chat-module.md)

[Proactieve chatparameters voor Commerce-chatmodule](chat-proactive-chat-parameters.md)
