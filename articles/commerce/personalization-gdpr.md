---
title: Zich afmelden voor persoonlijke aanbevelingen
description: In dit onderwerp wordt uitgelegd hoe u klanten in staat kunt stellen af te zien van het ontvangen van persoonlijke aanbevelingen in Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e88980ef6ad585826762c8be35304aecbcc02ab
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154290"
---
# <a name="opt-out-of-personalized-recommendations"></a>Zich afmelden voor persoonlijke aanbevelingen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u klanten in staat kunt stellen af te zien van het ontvangen van persoonlijke aanbevelingen in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Tijdens het maken van de rekening worden nieuwe klanten automatisch ingesteld voor het ontvangen van persoonlijke aanbevelingen. Dynamics 365 Commerce biedt echter verschillende manieren om gebruikers in staat te stellen zich af te melden voor het ontvangen van deze aanbevelingen en de verwerking van hun persoonlijke gegevens te beperken. Geverifieerde gebruikers die zich afmelden voor het ontvangen van persoonlijke aanbevelingen zien direct geen persoonlijke lijsten meer. Bovendien worden alle persoonlijke gegevens die worden verzameld voor personalisatie, verwijderd uit persoonlijke aanbevelingen.

Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over persoonlijke productaanbevelingen.

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Manieren voor detailhandelaren om een afmeldingsmethode te implementeren

Detailhandelaren hebben drie manieren om een afmeldingsmethode te implementeren.

### <a name="opting-out-on-behalf-of-users"></a>Afmelden namens gebruikers

In Accountbeheer in Commerce Back Office kunnen detailhandelaren de afmelding uitvoeren namens gebruikers.

1. Zoek op de startpagina van Back Office naar **alle klanten**.
1. Zoek en selecteer een klant en selecteer vervolgens het sneltabblad **Detailhandel**.

    ![Sneltabblad Detailhandel](./media/Disablepersonalizationpart1.png)

1. Stel onder **Privacy** de optie **Persoonlijke instellingen uitschakelen** in op **Ja**.

    ![Privacy-instellingen](./media/Disablepersonalizationpart2.png)

1. Selecteer **Opslaan** en sluit de pagina.

### <a name="module-based-opt-out-experience"></a>Modulegebaseerde afmelding

Detailhandelaren kunnen geverifieerde gebruikers in staat stellen zichzelf af te melden voor persoonlijke aanbevelingen. Voeg de afmeldingsmodule voor gebruikers toe aan klantrekeningprofielpagina's om deze methode van afmelding te kunnen bieden.

### <a name="custom-extensions"></a>Aangepaste extensies

Detailhandelaren kunnen hun eigen extensies maken om de afmelding voor gebruikers te beheren. Zie [Retail Server-API's aanroepen](e-commerce-extensibility/call-retail-server-apis.md) en [Uitbreidbaarheid van online afzetkanaal](e-commerce-extensibility/overview.md). voor meer informatie.

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Een digitale kopie van persoonlijke aanbevelingen ophalen namens een geverifieerde gebruiker

Klanten willen mogelijk een digitale kopie van hun persoonlijke gegevens verkrijgen en tevens een geëxporteerde weergave van hun aanbevelingen bekijken. Als een klant deze informatie aanvraagt, moet de detailhandelaar een aangepaste extensie maken die de API (Application Programming Interface) van de Retail Server aanroept en vraagt om de volledige resultaten van de lijst **Selectie voor u**, op basis van de klant-id van de klant. De resultaten kunnen vervolgens in CSV-indeling (Comma-Separated Values) worden geëxporteerd en met de klant worden gedeeld.

In het volgende voorbeeld ziet u hoe een detailhandelaar deze taak kan uitvoeren.

1. De detailhandelaar maakt een aangepaste extensie om persoonlijke aanbevelingen te verzamelen namens de gebruiker. Zie [Uitbreidbaarheid van online afzetkanaal](e-commerce-extensibility/overview.md) voor informatie over het maken van modules, het klonen van bestaande modules, het aanroepen van Retail Server API's en het oproepen van gegevens.
2. Met de aangepaste extensie wordt een oproep gedaan aan de kerngegevensactie **get-recommendations** en wordt de vereiste informatie doorgegeven op basis van de vereisten van de lijst. In het geval van de lijst **Selectie voor u** moet de extensie de juiste lijstnaam en klant-id doorgeven voor de gegevensactie.

    Eén manier om de aangepaste extensie te maken is door de bestaande module voor productverzamelingen te klonen die wordt gebruikt om aanbevelingen te retourneren. Door deze bestaande module te klonen, kan een detailhandelaar de bestaande code wijzigen en een nieuwe knop toevoegen waarmee de resultaten van de aanbevelingen worden geëxporteerd naar een CSV-bestand. Zie [Een starterskit voor een module klonen](e-commerce-extensibility/clone-starter-module.md) en [Productverzamelingsmodules](product-collection-module-overview.md) voor meer informatie.

    Zie [Klanten- en consumenten-API's voor Retail Server](dev-itpro/retail-server-customer-consumer-api.md) voor een volledige weergave van de API-bibliotheek van Retail Server.

3. Nadat de aangepaste extensie is gemaakt, kan de detailhandelaar een CSV-bestand van alle aanbevelingen exporteren op basis van de unieke klant-id van de geverifieerde gebruiker.
4. De detailhandelaar kan het geëxporteerde CSV-bestand dat de volledig aangepaste lijst met aanbevolen producten bevat delen met de geverifieerde gebruiker.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[ADLS inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Productaanbevelingen op POS toevoegen](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)
