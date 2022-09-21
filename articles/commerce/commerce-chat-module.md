---
title: Commerce Chat met module Omnichannel voor Customer Service
description: Dit artikel beschrijft de module Commerce Chat met Omnichannel voor Customer Service in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: b8eaed3eb015e96b1db6fa2297c341ea9d3ff8ad
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473804"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Commerce Chat met module Omnichannel voor Customer Service

[!include [banner](includes/banner.md)]

Dit artikel beschrijft de module *Commerce Chat met Omnichannel voor Customer Service* in Microsoft Dynamics 365 Commerce.

In de release van Commerce versie 10.0.29 is een nieuwe module Commerce Chat met Omnichannel voor Customer Service toegevoegd aan de modulebibliotheek van Commerce. De Commerce-chatfunctie voorziet e-commerceklanten van de chatfuncties van Dynamics 365 Omnichannel voor Customer Service. Deze functie omvat live agent-ondersteuning om vragen van klanten te beantwoorden, klantenservice te leveren en verkoop voor klanten van Commerce te vergemakkelijken.

Detailhandelaren kunnen de Commerce-chatfunctie gebruiken voor de volgende doelen:

- Gepersonaliseerde interactie met klanten verbeteren voor extra klantenbinding.
- De klantenservice verbeteren door de integratie van menselijke agenten en selfservice chatbots.
- Medewerkers ervaring laten krijgen met behulp van real-time gegevens over klantprofiel, orders en inkoop die de operationele verbeteringen en interacties stimuleren.
- De algehele klanttevredenheid verbeteren om de verkoop te verhogen.

De volgende voorzieningen zijn beschikbaar als onderdeel van de Commerce-chatfunctie:

- Commerce Chat met Omnichannel voor Customer Service
- De toevoeging van **Commerce-callcenter** als een tabblad in de agentfunctie van Dynamics 365 Omnichannel voor Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Vereisten voor Omnichannel voor Customer Service

U moet vooraf chat configureren in de beheerwidget voor Omnichannel voor Customer Service en een aantal parameters configureren voor de Commerce-chatfunctie. Zie [Een chatkanaal configureren](/dynamics365/customer-service/set-up-chat-widget) voor instructies.

Nadat u de chatfunctie hebt geconfigureerd in de beheerwidget Omnichannel voor Customer Service, krijgt u een script dat op het volgende voorbeeld lijkt.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopieer dit script, omdat u de waarden nodig hebt om de chatmodule te configureren.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Verplichte velden voor Commerce Chat met Omnichannel voor Customer Service

In de volgende tabel ziet u de scriptwaarden van de beheerwidget Omnichannel voor Customer Service die nodig zijn om de module Commerce Chat met Omnichannel voor Customer Service te configureren.

| Widgeteigenschap | Beschrijving |
| ------------- |--------------|
| Scriptbron | De waarde van **src** in het chatwidgetscript. |
| Gegevenstoepassings-id | De waarde van **data-app-id** in het chatwidgetscript. |
| Gegevensorganisatie-id | De waarde van **data-org-id** in het chatwidgetscript. |
| Gegevensorganisatie-URL | De waarde van **data-org-url** in het chatwidgetscript. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>De Commerce-chatervaring configureren voor uw e-commercesite

Een van de aanbevolen manier om de chatervaring voor uw e-commercesite te implementeren, is het toevoegen van de module Commerce Chat met Omnichannel voor Customer Service aan het gedeelde koptekstfragment dat op uw e-commercesitepagina's wordt gebruikt.

Voer de volgende stappen uit om de chatmodule toe te voegen aan het koptekstfragment van uw site in Commerce Site Builder.

1. Ga op uw site in Site Builder naar **Fragmenten**.
1. Selecteer **Nieuw**.
1. Selecteer in het dialoogvenster **Fragment selecteren** de module **Commerce Chat met Omnichannel voor Customer Service**, voer een naam voor het fragment in en selecteer **OK**.
1. Selecteer in de overzichtsweergave het vak **Msdyn365 cs chat connector**.
1. Volg deze stappen in het deelvenster **Chateigenschappen** aan de rechterkant:

    1. Voer in het veld **Scriptbron** de waarde **src** in die u hebt verkregen uit het script Omnichannel voor Customer Service.
    1. Voer in het veld **Gegevenstoepassings-id** de waarde **data-app-id** in die u hebt verkregen uit het script Omnichannel voor Customer Service.
    1. Voer in het veld **Gegevensorganisatie-id** de waarde **data-org-id** in die u hebt verkregen uit het script Omnichannel voor Customer Service.
    1. Voer in het veld **Gegevensorganisatie-URL** de waarde **data-org-url** in die u hebt verkregen uit het script Omnichannel voor Customer Service.

    ![Een fragment maken in de module Commerce Chat in Commerce Site Builder.](media/Commerce-chat-creating-new-fragment.png)

1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.
1. Ga naar **Fragmenten** en open het koptekstfragment voor uw site.
1. Selecteer in het vak **Standaardcontainer** het beletselteken (**...**) en selecteer vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** het chatfragment dat u eerder hebt gemaakt, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Commerce headquarters toevoegen als toepassingstabblad voor Omnichannel voor Customer Service

U kunt een toepassingstabblad toevoegen voor Commerce headquarters in Omnichannel voor Customer Service. Live agenten kunnen vervolgens met de gebruikersinterface voor Omnichannel voor Customer Service eenvoudig toegang krijgen tot de klantenservicemodule van Dynamics 365 Commerce die contextuele informatie voor de klant bevat samen met de verkoopordergegevens. Daarnaast kunnen medewerkers van de klantenservice nieuwe orders plaatsen, retouren starten en informatie over de orderstatus controleren.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Een nieuw toepassingstabblad maken waarmee Commerce Headquarters in een iFrame-module wordt geladen 

Volg deze stappen om een nieuw toepassingstabblad te maken waarmee Commerce Headquarters in een iFrame-module wordt geladen.

1. Open de [Power Apps Maker Portal](https://make.powerapps.com).
1. Selecteer **Apps** in het navigatievenster aan de linkerkant.
1. Selecteer **Customer Service-beheercentrum**.
1. Ga naar **Agentvoorziening**.
1. Selecteer **Beheren** voor **Sjablonen voor toepassingstabbladen**.
1. Maak een nieuw toepassingstabblad van het type **Website van derden**. Zie [Sjablonen voor toepassingstabbladen beheren](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter) voor instructies.
1. Voer onder **Parameters** in het veld **Waarde** van **de url-parameter** de volgende URL in, waarbij `<YourOrganizationHeadquartersURL>` en `<LegalEntityname>` worden vervangen door de juiste waarden. Omnichannel Customer Service leest **{AccountNumber}** uit de chatcontext. Laat **{AccountNumber}** dus ongewijzigd.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Laat het veld **Waarde** van de parameter **data** leeg.

![Een toepassingstabblad maken in Dynamics 365 Omnichannel voor Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Een nieuw toepassingstabblad inschakelen voor klantagenten in Dynamics 365 Omnichannel voor Customer Service

Volg deze stappen om een nieuw toepassingstabblad in te schakelen voor klantagenten in Dynamics 365 Omnichannel voor Customer Service.
    
1. Open de [Power Apps Maker Portal](https://make.powerapps.com).
1. Selecteer **Apps** in het navigatievenster aan de linkerkant.
1. Selecteer **Customer Service-beheercentrum**.
1. Ga naar **Klantondersteuning \> Werkstromen**.
1. Open de werkstroom die u voor uw agenten hebt gemaakt en selecteer vervolgens onder **Geavanceerde instellingen** de optie **Sessiestandaard**.
1. Selecteer onder **Toepassingstabbladen** de optie **Bestaand toepassingstabblad toevoegen** en voeg het nieuwe toepassingstabblad toe dat u eerder hebt gemaakt. Met deze stap zorgt u ervoor dat een toepassingstabblad waarmee Commerce Headquarters wordt geladen in een iFrame-module, wordt weergegeven wanneer een medewerker een inkomend chatverzoek ontvangt van uw e-commercewebsite.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Contextvariabelen toevoegen in Dynamics 365 Omnichannel voor Customer Service

Volg deze stappen om contextvariabelen toe te voegen in Dynamics 365 Omnichannel voor Customer Service.

1. Open de [Power Apps Maker Portal](https://make.powerapps.com).
1. Selecteer **Apps** in het navigatievenster aan de linkerkant.
1. Selecteer **Customer Service-beheercentrum**.
1. Ga naar **Klantondersteuning \> Werkstromen**.
1. Open de werkstroom die u voor uw agenten hebt gemaakt en ga vervolgens onder **Geavanceerde instellingen** naar de sectie **Contextvariabele**.
1. Selecteer **Bewerken** en voeg vervolgens **AccountNumber** toe als een contextvariabele van het **teksttype**. Met deze variabele kan Commerce headquarters klantgegevens laden met overeenkomende rekeningnummers.

> [!NOTE]
> Als u de e-mailadressen en namen van aangemelde gebruikers uit een e-commercekanaal wilt lezen, kunt u **E-mail** en **Naam** toevoegen als contextvariabelen van het **teksttype** naast de contextvariabele **AccountNumber**.
