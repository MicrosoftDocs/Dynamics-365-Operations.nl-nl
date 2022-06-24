---
title: Aanbevelingen voor vergelijkbare omschrijvingen inschakelen
description: In dit artikel wordt beschreven hoe u productaanbevelingen voor vergelijkbare omschrijvingen kunt inschakelen in Microsoft Dynamics 365 Commerce.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b935731b24f96753c814e3b496ffeeb7a92d9cc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852003"
---
# <a name="enable-shop-similar-description-recommendations"></a>Aanbevelingen voor vergelijkbare omschrijvingen inschakelen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u productaanbevelingen voor vergelijkbare omschrijvingen kunt inschakelen in Microsoft Dynamics 365 Commerce.

De aanbevelingen van de optie voor voor vergelijkbare omschrijvingen in Dynamics 365 Commerce maakt gebruik van kunstmatige intelligentie en machine learning (AI-ML) om aanbevelingen te geven voor producten met vergelijkbare omschrijvingen als waar de klant naar op zoek is. Door de aanbevelingen voor vergelijkbare omschrijvingen beschikbaar te maken voor alle detailhandelkanalen in Commerce, kunnen detailhandelaren klanten helpen te vinden wat ze zoeken.

De functie voor aanbevelingen voor vergelijkbare artikelen maakt gebruik van de productnaam en omschrijving van seedproductvarianten om vergelijkbare producten te zoeken en aan te raden in de productcatalogus van een detailhandelaar.

De aanbevelingen voor vergelijkbare omschrijvingen zijn beschikbaar in POS en e-Commerce.

## <a name="example-scenarios"></a>Voorbeeldscenario's

In de volgende voorbeeldscenario's worden de typen aanbevelingen beschreven die de functionaliteit voor aanbevelingen voor vergelijkbare omschrijvingen kan bieden:

- Een klant bekijkt een retrobril met hoornen montuur en ontvangt een reeks aanbevelingen voor andere brillen met een vergelijkbaar ontwerp binnen de context van de sector van de detailhandelaar.
- Een klant gebruikt aanbevelingen voor vergelijkbare omschrijvingen om koffiesmaken te ontdekken die lijken op een eerder gekochte smaak bij die detailhandelaar.

## <a name="set-up-shop-similar-description-recommendations"></a>Aanbevelingen voor vergelijkbare omschrijving instellen

Productaanbevelingen worden alleen ondersteund voor Commerce-gebruikers die hun opslag hebben gemigreerd naar Azure Data Lake Storage Gen2.

### <a name="prerequisites"></a>Vereisten

Voordat aanbevelingen voor vergelijkbare omschrijvingen kunnen worden getoond aan klanten, moet u aan de volgende vereisten voldoen:

- [Schakel productaanbevelingen](enable-product-recommendations.md) in Commerce Headquarters in.
- Controleer of de mediaserver HTTPS-oproepen ondersteunt.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>De functie voor aanbevelingen voor vergelijkbare omschrijvingen inschakelen

Voer de volgende stappen uit om de aanbevelingen voor vergelijkbare omschrijvingen in te schakelen in Commerce Headquarters.

1. Selecteer in het werkgebied **Functiebeheer** in de lijst met beschikbare functies de optie **Winkelen voor vergelijkbare omschrijvingen**.
1. Selecteer **Inschakelen** in het rechterdeelvenster.

> [!NOTE]
> Wanneer u de functie inschakelt, genereert het systeem productaanbevelingslijsten. Het kan een dag duren voordat deze lijsten online en op POS-terminals beschikbaar en zichtbaar zijn.
>
> Als u de functie uitschakelt, heeft dit geen invloed op andere typen productaanbevelingen. Zie [Overzicht van productaanbevelingen](product-recommendations.md) voor meer informatie over productaanbevelingen.

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Een knop Winkelen voor vergelijkbare omschrijvingen toevoegen aan pagina's met productgegevens

Nadat u de functie voor aanbevelingen voor vergelijkbare omschrijvingen in Commerce Headquarters hebt ingeschakeld, kunt u de knop **Winkelen voor vergelijkbare omschrijvingen** toevoegen aan het koopvak op een pagina met productgegevens. Een klant die deze knop selecteert, wordt naar een speciale pagina **Winkelen voor vergelijkbare omschrijvingen** geleid waarop visueel vergelijkbare producten worden weergegeven. De klant kan vervolgens selectors gebruiken om de producten verder te filteren.

Voer deze stappen uit om een knop **Winkelen voor vergelijkbare omschrijvingen** toe te voegen aan de pagina's met productgegevens met Commerce Site Builder.

1. Open een bestaande pagina voor Site Builder die een koopvakmodule bevat.
1. Selecteer de koopvakmodule in het navigatievenster aan de linkerkant.
1. Schakel in het rechtervenster het selectievakje **Koppeling voor vergelijkbare omschrijvingen inschakelen** in.
1. Selecteer **Opslaan**.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren. Nadat de pagina is gepubliceerd, zal de PDP een knop **Vergelijkbare omschrijving** bevatten.

In de volgende afbeelding ziet u het selectievakje **Koppeling voor vergelijkbare omschrijvingen inschakelen** en de knop **Winkelen voor vergelijkbare omschrijvingen** op een voorbeeldpagina met productgegevens in Site Builder.

![Selectievakje Koppeling voor vergelijkbare omschrijvingen inschakelen en de knop Winkelen voor vergelijkbare omschrijvingen op een pagina met productgegevens in Site Builder.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]