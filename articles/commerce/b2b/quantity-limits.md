---
title: De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites
description: In dit onderwerp wordt beschreven hoe u limieten voor producthoeveelheid instelt voor B2B-e-commercesites (business-to-business).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 18dc138693dc9fb0e8cf8727de77b5f8584cde79
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690190"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u limieten voor producthoeveelheid instelt voor B2B-e-commercesites (business-to-business).

De meeste producten hebben een maateenheid die hun groepering bepaalt. De groepering heeft invloed op de manier waarop de producten kunnen worden verkocht. Sommige producten hebben mogelijk een extra groepering voor hoeveelheden. Deze groepering bepaalt of de producten kunnen worden verkocht als afzonderlijke eenheden of veelvouden en of er een minimale of maximale orderhoeveelheidlimiet is die moet worden gevolgd.

De functionaliteit voor het beperken van hoeveelheden zorgt ervoor dat de minimale, maximale, meervoudige en standaardhoeveelheden die in Microsoft Dynamics 365 Commerce zijn geconfigureerd (in de standaardorderinstellingen of de site-instellingen van Commerce Site Builder), worden toegepast op klantorders die op een e-commercesite worden geplaatst. Producthoeveelheidslimieten worden momenteel niet ondersteund voor het POS (Point of Sale) en callcenters.

Veel detailhandelaren bieden de optie van klantorders, oftewel speciale orders, om aan verschillende product- en afhandelingsvereisten te voldoen. Hierna vindt u enkele typische scenario's:

- Een klant wil dat bepaalde varianten van producten in veelvouden van een paar worden verkocht.
- Een klant wil producten bij een andere winkel of locatie ophalen dan de winkel of locatie waar de klant deze producten heeft gekocht. De verpakkingsstandaarden voor de winkels verschillen echter van de verpakkingsstandaarden voor online verkoopdistributie.
- Een klant wil een limited-edition product kopen met een maximale hoeveelheidslimiet voor artikelen die kunnen worden gekocht.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>De functie voor standaardorderinstellingen in Commerce Headquarters inschakelen

Voordat u limieten voor producthoeveelheden kunt instellen, moet de standaardfunctie voor orderinstellingen zijn ingeschakeld in Commerce Headquarters.

Voer de volgende stappen uit om de functie voor standaardorderinstellingen in te schakelen.

1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
1. Zoek en selecteer de functie **De site- en standaardorderinstellingen in de klantorder ondersteunen**.
1. Selecteer **Nu inschakelen** onder in het rechterdeelvenster. 

## <a name="define-quantity-settings"></a>Kwaliteitsinstellingen definiëren 

U definieert de kwaliteitsinstellingen op de pagina **Standaard orderinstellingen**.

Voer de volgende stappen uit om de kwaliteitsinstellingen op te geven. 

1. Ga naar Product **Retail en Commerce \> Producten en categorieën \> Vrijgegeven producten per categorie**.
1. Selecteer een vrijgegeven product.
1. Selecteer in het actievenster op het tabblad **Voorraadbeheer** in de groep **Orderinstellingen** de optie **Standaardorderinstellingen**. 
1. Stel op de pagina **Standaardorderinstellingen** op het sneltabblad **Verkooporder** in de sectie **Verkoophoeveelheid** de hoeveelheden voor productverkoop in:

    - **Veelvoud**: de hoeveelheid waarvoor het product in veelvouden kan worden gekocht.
    - **Minimumorderhoeveelheid**: het minimum aantal producten dat moet worden gekocht.
    - **Maximumorderhoeveelheid**: het maximum aantal producten dat kan worden gekocht.
    - **Standaardorderhoeveelheid**: de standaardhoeveelheid die automatisch wordt ingevoerd wanneer het product wordt geselecteerd.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>De functionaliteit voor hoeveelheidslimieten voor B2B-orders inschakelen in Commerce Site Builder

Voer deze stappen uit om de functionaliteit voor hoeveelheidslimieten voor B2B-orders in te schakelen in Commerce Site Builder.

1. Ga naar **Site-instellingen \> Extensies**
1. Selecteer onder **Limieten voor orderhoeveelheid inschakelen** de optie **Ingeschakeld voor B2B-klanten** in het vervolgkeuzemenu. 

> [!NOTE] 
> Bijgewerkte Site Builder-instellingen worden pas van kracht nadat het bestand app.settings.json is bijgewerkt. Zie [Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2B-e-commercesite instellen](set-up-b2b-site.md)

[B2B-zakenpartners beheren met behulp van klanthiërarchieën](partners-customer-hierarchies.md)

[Gebruikers van zakelijke partners beheren op e-commercesites voor B2B](manage-b2b-users.md)

[De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
