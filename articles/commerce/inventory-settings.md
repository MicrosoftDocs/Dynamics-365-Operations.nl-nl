---
title: Voorraadinstellingen toepassen
description: In dit artikel worden voorraadinstellingen beschreven en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: df1d1283a7692336906550169bc77104a9118779
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909552"
---
# <a name="apply-inventory-settings"></a>Voorraadinstellingen toepassen

[!include [banner](includes/banner.md)]

In dit artikel worden voorraadinstellingen beschreven en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.

Met voorraadinstellingen wordt opgegeven of voorraad moet worden gecontroleerd voordat producten aan de winkelwagen worden toegevoegd. Ze definiëren ook voorraadgerelateerde merchandisingberichten, zoals In voorraad en Slechts een paar over. Deze instellingen zorgen ervoor dat een product niet kan worden aangeschaft als het niet op voorraad is.

Dynamics 365 Commerce biedt schattingen van voorhanden voorraad voor producten. Zie [Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md) voor informatie over de berekening van geschatte voorhanden voorraad .

In Commerce Site Builder kunt u voorraaddrempels en -bereiken definiëren voor een product of een categorie. Ze bepalen of voorraad kan worden geclassificeerd als in voorraad, weinig voorraad of niet op vorraad. Zie [Voorraadbuffers en voorraadniveaus configureren](inventory-buffers-levels.md) voor meer informatie

> [!NOTE]
> Ondersteuning voor voorraaddrempels en -bereiken is beschikbaar in de release van Dynamics 365 Commerce 10.0.12.

## <a name="inventory-settings"></a>Voorraadinstellingen

In Commerce worden voorraadinstellingen gedefinieerd via **Site-instellingen \> Extensies \> Voorraadbeheer** in Site Builder. Er zijn zes voorraadinstellingen, waarvan er een is verouderd (afgeschaft):

- **Voorraadcontrole in app inschakelen**: met deze instelling wordt de voorraadcontrole van een product ingeschakeld. De modules voor koopvak, winkelwagen en ophalen in winkel comntroleren vervolgens de productvoorraad en zorgen ervoor dat een product alleen aan de winkelwagen kan worden toegevoegd als er voorraad beschikbaar is.
- **Voorraadniveau gebaseerd op**: deze instelling bepaalt hoe voorraadniveaus worden berekend. De beschikbare waarden zijn **Totaal beschikbaar**, **Fysiek beschikbaar** en **Drempelwaarde voor niet op voorraad**. In Commerce kunt u drempelwaarden en bereiken definiëren voor elk product en elke categorie. De voorraad-API's geven productvoorraadinformatie als resultaat voor de eigenschappen **Totaal beschikbaar** en **Fysiek beschikbaar**. De detailhandelaar beslist of de waarde **Totaal beschikbaar** of **Fysiek beschikbaar** moet worden gebruikt om de voorraadtelling en de bijbehorende bereiken voor op voorraad en niet op voorraad te bepalen.

    De waarde **Drempelwaarde voor niet op voorraad** van de instelling **Voorraadniveau gebaseerd op** is een oude (verouderde) waarde. Wanneer deze wordt geselecteerd, wordt de voorraadtelling bepaald op basis van de resultaten van de waarde **Totaal beschikbaar**, de drempel wordt gedefinieerd door de numerieke instelling **Drempelwaarde voor niet op voorraad** die later wordt beschreven. Deze drempelwaarde-instelling is van toepassing op alle producten voor een e-commerce-site. Als voorraad lager is dan de drempelwaarde, wordt een product als niet op voorraad beschouwd. Anders wordt het beschouwd als op voorraad. De mogelijkheden van de waarde **Drempel waarde voor niet op voorraad** zijn beperkt en wij raden u aan om deze niet meer te gebruiken in versie 10.0.12 en hoger.

- **Voorraadniveau voor meerdere magazijnen**: Met deze instelling kan het voorraadniveau worden berekend op basis van het standaardmagazijn of meerdere magazijnen. Met de optie **Op basis van afzonderlijk magazijn** worden voorraadniveaus berekend op basis van het standaardmagazijn. Een webwinkel kan ook naar meerdere magazijnen wijzen om de levering te vergemakkelijken. In dat geval wordt de optie **Gebaseerd op samenvoeging voor verzend- en afhaalmagazijnen** gebruikt om de beschikbaarheid van de voorraad aan te geven. Als een klant bijvoorbeeld een artikel inkoopt en 'verzending' selecteert als de leveringsmodus, kan het artikel worden verzonden vanuit elk magazijn in de vervullingsgroep dat over beschikbare voorraad beschikt. Op de pagina met productdetails wordt een bericht 'In voorraad' weergegeven voor zending als een beschikbaar magazijn in de vervullingsgroep voorraad heeft. 

    > [!IMPORTANT] 
    > De instelling **Voorraadniveau voor meerdere magazijnen** is beschikbaar vanaf Commerce-versie 10.0.19. Als u een oudere versie van Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer instructies.

- **Voorraadinstellingen voor productlijstpagina's** met deze instelling wordt bepaald hoe producten die niet op voorraad zijn, worden weergegeven in productlijsten die worden weergegeven door modules voor productverzameling en zoekresultaten. De beschikbare waarden zijn **In bestelling weergeven met andere producten**, **Uit voorraadproducten verbergen uit de lijst** en **Uit voorraadproducten weergeven aan het einde van de lijst**. Als u deze instelling wilt gebruiken, moet u eerst een aantal vereiste instellingen configureren in Commerce Headquarters. Zie [De voorraadbeschikbaarheid voor de module voor zoekresultaten inschakelen](search-result-module.md#enable-inventory-awareness-for-the-search-results-module) voor meer informatie.

    > [!IMPORTANT] 
    > De instelling **Voorraadinstellingen voor productlijstpagina's** is beschikbaar vanaf Commerce-versie 10.0.20. Als u een oudere versie van Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer instructies.

- **Voorraadbereiken**: met deze instelling definieert u de voorraadbereiken waarvoor berichten worden weergegeven in sitemodules. Deze is alleen van toepassing als de waarde **Totaal beschikbaar** of **Fysiek beschikbaar** is geselecteerd voor de instelling **Voorraadniveau gebaseerd op**. De beschikbare waarden zijn **Alle**, **Weinig en niet op voorraad** en **Niet op voorraad**.

    - Wanneer **Alle** is geselecteerd, worden berichten voor alle voorraadbereiken, van op voorraad (Beschikbaar) tot niet op voorraad (Niet op voorraad), weergegeven.
    - Wanneer **Weinig en niet op voorraad** is geselecteerd, worden berichten voor alle voorraadbereiken, behalve op voorraad (Beschikbaar), weergegeven.
    - Wanneer **Niet op voorraad** is geselecteerd, wordt alleen het bericht Niet op vooraad weergegeven.

- **Drempelwaarde voor niet op voorraad**: deze oude numerieke instelling wordt alleen van kracht als de waarde **Drempelwaarde voor niet op voorraad** is geselecteerd voor de instelling **Voorraadniveau gebaseerd op**.

> [!IMPORTANT] 
> Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.12. Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json.

## <a name="modules-that-use-inventory-settings"></a>Modules die voorraadinstellingen gebruiken

De modules voor koopvak, wensenlijst, winkelselectie en winkelwagen gebruiken voorraadinstellingen om de voorraadbereiken en berichten weer te geven.

In het voorbeeld in de volgende afbeelding toont een productpagina een bericht In voorraad ('Beschikbaar').

![Voorbeeld van een PDP-module met een bericht over voorhanden voorraad.](./media/pdp-InStock.png)

In het voorbeeld in de volgende afbeelding toont een productpagina een bericht Niet op voorraad.

![Voorbeeld van een PDP-module met het bericht dat er geen voorraad beschikbaar is.](./media/pdp-outofstock.png)

In het voorbeeld in de volgende afbeelding toont een winkelwagen een bericht In voorraad ('Beschikbaar').

![Voorbeeld van een winkelwagenmodule met een bericht over voorhanden voorraad.](./media/cart-instock.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Voorraadbuffers en voorraadniveaus configureren](inventory-buffers-levels.md)

[Winkelwagenmodule](add-cart-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Accountbeheerpagina's en -modules](account-management.md)

[Winkelselectiemodule](store-selector.md)

[Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
