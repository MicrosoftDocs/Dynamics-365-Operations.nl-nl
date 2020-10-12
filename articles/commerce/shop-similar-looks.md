---
title: Aanbevelingen voor vergelijkbare artikelen inschakelen
description: In dit onderwerp wordt beschreven hoe u productaanbevelingen voor vergelijkbare artikelen kunt inschakelen in in Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818369"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Aanbevelingen voor vergelijkbare artikelen inschakelen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u productaanbevelingen voor vergelijkbare artikelen kunt inschakelen in in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De aanbevelingen van de optie voor voor vergelijkbare artikelen in Dynamics 365 Commerce maakt gebruik van de kracht van kunstmatige intelligentie en machine learning (AI-ML) om aanbevelingen te geven voor vergelijkbare producten aan klanten. Door de aanbevelingen voor vergelijkbare artikelen beschikbaar te maken voor alle detailhandelkanalen in Commerce, kunnen detailhandelaren de klanttevredenheid verbeteren doordat klanten gemakkelijk vinden wat ze zoeken.

De functie voor aanbevelingen voor vergelijkbare artikelen maakt gebruik van afbeeldingen van seedproductvarianten om visueel vergelijkbare producten te zoeken en aan te raden in de productcatalogus van een detailhandelaar. 

De aanbevelingen voor vergelijkbare artikelen zijn beschikbaar in zowel POS als e-Commerce.

### <a name="example-scenarios"></a>Voorbeeldscenario's

- Een klant bekijkt een zwart gestreepte trui en ontvangt een aanbeveling voor een vergelijkbare rode trui. De klant selecteert het aanbevolen product in plaats van het oorspronkelijk weergegeven product en ontvangt vervolgens aanbevelingen voor soortgelijke producten in het rood. 
- Een klant gebruikt aanbevelingen voor vergelijkbare artikelen om bijpassende oorbellen te ontdekken voor een ring die de klant wil kopen.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Aanbevelingen voor vergelijkbare artikelen inschakelen in Commerce Headquarters

Productaanbevelingen worden alleen ondersteund voor Commerce-gebruikers die hun opslag hebben gemigreerd naar Azure Data Lake Gen2.

### <a name="prerequisites"></a>Vereisten

Voordat detailhandelaren kunnen beginnen met het weergeven aanbevelingen voor vergelijkbare artikelen, zijn er twee vereiste stappen:

- [Schakel productaanbevelingen](enable-product-recommendations.md) in Commerce Headquarters in.
- Controleer of de mediaserver HTTPS-oproepen ondersteunt.

Voordat de aanbevelingsengine toegang krijgt tot de productafbeeldingen, moeten detailhandelaren de product-URL's genereren. Voer deze stappen uit om product-URL's te genereren in Commerce Headquarters.

1. Ga naar **Productafbeeldingen**.
1. Selecteer in het actievenster de optie **Mediasjabloon definiëren**.
1. Selecteer in het eigenschappenvenster **Mediasjabloon definiëren** onder **Media-URL's** de optie **URL's genereren**.

> [!NOTE]
> Wanneer u de aanbevelingsfunctie voor vergelijkbare producten inschakelt, wordt het proces voor het genereren van de productaanbevelingen gestart. Mogelijk is maximaal een dag vereist voordat deze lijsten online en op de POS-terminals beschikbaar en zichtbaar zijn.

Voer de volgende stappen uit om de aanbevelingen voor vergelijkbare producten in te schakelen in Commerce Headquarters.

1. Ga naar **Functiebeheer**.
1. Zoek in de lijst met beschikbare functies naar **Vergelijkbare artikelen** en selecteer deze optie.
1. Selecteer in het rechterdeelvenster de optie **Inschakelen** om de service in te schakelen.

In de volgende afbeelding ziet u de functie **Vergelijkbare artikelen** op de pagina **Functiebeheer** in Commerce Headquarters.

![De functie Vergelijkbare artikelen op de pagina Functiebeheer in Commerce Headquarters](./media/enableshopsimilarlooks.png)

Nadat de voorgaande taken zijn voltooid, worden POS-terminals automatisch uitgebreid met een contextvenster met **Vergelijkbare artikelen**. Als u **Meer weergeven** kiest, kunnen gebruikers van POS-terminals een specifieke pagina met Vergelijkbare artikelen openen voor verdere filtering.

> [!NOTE]
> Als u de aanbevelingen voor vergelijkbare artikelen uitschakelt, heeft dit geen invloed op andere typen productaanbevelingen. Zie [Overzicht van productaanbevelingen](product-recommendations.md) voor meer informatie over productaanbevelingen.

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Een knop voor Vergelijkbare artikelen toevoegen aan de pagina's met productdetails met Commerce site builder

Nadat u de aanbevelingen in Commerce Headquarters hebt ingeschakeld, kunnen detailhandelaren via een optie in Commerce site builder een knop **Vergelijkbare artikelen** toevoegen aan het koopvak op een pagina met productgegevens (PDP). Een klant die deze knop selecteert, wordt naar een speciale pagina met vergelijkbare artikelen geleid die visueel vergelijkbare producten retourneert. Vervolgens kan de klant selectors gebruiken om de producten verder te filteren.

Voer deze stappen uit om een knop voor **Vergelijkbare artikelen** toe te voegen aan de pagina's met productdetails met Commerce site builder

1. Open een bestaande pagina voor Site Builder die een koopvakmodule bevat.
1. Selecteer de koopvakmodule in het navigatievenster aan de linkerkant.
1. Schakel in het rechternavigatievenster het selectievakje **Koppeling voor vergelijkbare artikelen inschakelen** in.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren. Nadat de pagina is gepubliceerd, zal de PDP een knop **Vergelijkbare artikelen** bevatten.

In de volgende afbeelding ziet u het selectievakje **Koppeling voor vergelijkbare artikelen inschakelen** en de knop **Vergelijkbare artikelen** op een PDP-voorbeeldpagina in site builder.

![Selectievakje Koppeling voor vergelijkbare artikelen inschakelen en de knop Vergelijkbare artikelen op een PDP in site builder](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Productaanbevelingen toevoegen op POS](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)
