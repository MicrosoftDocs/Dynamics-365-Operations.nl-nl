---
title: Voorraadinstellingen toepassen
description: In dit onderwerp worden voorraadinstellingen beschreven en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 77a3bde12fd047e15d7730903416cdb5263a8cd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972804"
---
# <a name="apply-inventory-settings"></a>Voorraadinstellingen toepassen

[!include [banner](includes/banner.md)]

In dit onderwerp worden voorraadinstellingen beschreven en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Met voorraadinstellingen wordt opgegeven of voorraad moet worden gecontroleerd voordat producten aan de winkelwagen worden toegevoegd. Ze definiëren ook voorraadgerelateerde merchandisingberichten, zoals In voorraad en Slechts een paar over. Deze instellingen zorgen ervoor dat een product niet kan worden aangeschaft als het niet op voorraad is.

Dynamics 365 Commerce biedt schattingen van voorhanden voorraad voor producten. Zie [Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md) voor informatie over de berekening van geschatte voorhanden voorraad .

In Commerce Site Builder kunt u voorraaddrempels en -bereiken definiëren voor een product of een categorie. Ze bepalen of voorraad kan worden geclassificeerd als in voorraad, weinig voorraad of niet op vorraad. Zie [Voorraadbuffers en voorraadniveaus configureren](inventory-buffers-levels.md) voor meer informatie

> [!NOTE]
> Ondersteuning voor voorraaddrempels en -bereiken is beschikbaar in de release van Dynamics 365 Commerce 10.0.12.

## <a name="inventory-settings"></a>Voorraadinstellingen

In Commerce worden voorraadinstellingen gedefinieerd via **Site-instellingen \> Extensies \> Voorraadbeheer** in Site Builder. Er zijn vier voorraadinstellingen, waarvan er een is verouderd (afgeschaft):

- **Voorraadcontrole in app inschakelen**: met deze instelling wordt de voorraadcontrole van een product ingeschakeld. De modules voor koopvak, winkelwagen en ophalen in winkel comntroleren vervolgens de productvoorraad en zorgen ervoor dat een product alleen aan de winkelwagen kan worden toegevoegd als er voorraad beschikbaar is.
- **Voorraadniveau gebaseerd op**: deze instelling bepaalt hoe voorraadniveaus worden berekend. De beschikbare waarden zijn **Totaal beschikbaar**, **Fysiek beschikbaar** en **Drempelwaarde voor niet op voorraad**. In Commerce kunt u drempelwaarden en bereiken definiëren voor elk product en elke categorie. De voorraad-API's geven productvoorraadinformatie als resultaat voor de eigenschappen **Totaal beschikbaar** en **Fysiek beschikbaar**. De detailhandelaar beslist of de waarde **Totaal beschikbaar** of **Fysiek beschikbaar** moet worden gebruikt om de voorraadtelling en de bijbehorende bereiken voor op voorraad en niet op voorraad te bepalen.

    De waarde **Drempelwaarde voor niet op voorraad** van de instelling **Voorraadniveau gebaseerd op** is een oude (verouderde) waarde. Wanneer deze wordt geselecteerd, wordt de voorraadtelling bepaald op basis van de resultaten van de waarde **Totaal beschikbaar**, de drempel wordt gedefinieerd door de numerieke instelling **Drempelwaarde voor niet op voorraad** die later wordt beschreven. Deze drempelwaarde-instelling is van toepassing op alle producten voor een e-commerce-site. Als voorraad lager is dan de drempelwaarde, wordt een product als niet op voorraad beschouwd. Anders wordt het beschouwd als op voorraad. De mogelijkheden van de waarde **Drempel waarde voor niet op voorraad** zijn beperkt en wij raden u aan om deze niet meer te gebruiken in versie 10.0.12 en hoger.

- **Voorraadbereiken**: met deze instelling definieert u de voorraadbereiken waarvoor berichten worden weergegeven in sitemodules. Deze is alleen van toepassing als de waarde **Totaal beschikbaar** of **Fysiek beschikbaar** is geselecteerd voor de instelling **Voorraadniveau gebaseerd op**. De beschikbare waarden zijn **Alle**, **Weinig en niet op voorraad** en **Niet op voorraad**.

    - Wanneer **Alle** is geselecteerd, worden berichten voor alle voorraadbereiken, van op voorraad (Beschikbaar) tot niet op voorraad (Niet op voorraad), weergegeven.
    - Wanneer **Weinig en niet op voorraad** is geselecteerd, worden berichten voor alle voorraadbereiken, behalve op voorraad (Beschikbaar), weergegeven.
    - Wanneer **Niet op voorraad** is geselecteerd, wordt alleen het bericht Niet op vooraad weergegeven.

- **Drempelwaarde voor niet op voorraad**: deze oude numerieke instelling wordt alleen van kracht als de waarde **Drempelwaarde voor niet op voorraad** is geselecteerd voor de instelling **Voorraadniveau gebaseerd op**.

> [!IMPORTANT] 
> Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.12. Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json.

## <a name="modules-that-use-inventory-settings"></a>Modules die voorraadinstellingen gebruiken

De modules voor koopvak, wensenlijst, winkelselectie en winkelwagen gebruiken voorraadinstellingen om de voorraadbereiken en berichten weer te geven.

De volgende afbeelding toont een voorbeeld van een pagina met productgegevens (PDP) met een bericht over voorhanden voorraad (Beschikbaar).

![Voorbeeld van een PDP-module met een bericht over voorhanden voorraad](./media/pdp-InStock.png)

De volgende afbeelding toont een voorbeeld van een PDP met het bericht Niet op voorraad.

![Voorbeeld van een PDP-module met het bericht dat er geen voorraad beschikbaar is](./media/pdp-outofstock.png)

De volgende afbeelding toont een voorbeeld van een winkelwagen met het bericht Beschikbaar.

![Voorbeeld van een winkelwagenmodule met een bericht over voorhanden voorraad](./media/cart-instock.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Voorraadbuffers en voorraadniveaus configureren](inventory-buffers-levels.md)

[Winkelwagenmodule](add-cart-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Accountbeheerpagina's en -modules](account-management.md)

[Winkelselectiemodule](store-selector.md)

[Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md)
