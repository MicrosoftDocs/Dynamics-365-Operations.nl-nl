---
title: Productaanbevelingen inschakelen
description: In dit artikel wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/31/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3dceec9e8e994a81b43cd5d1bd13970f2d246f40
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892066"
---
# <a name="enable-product-recommendations"></a>Productaanbevelingen inschakelen

[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce. Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Aanbevelingen voor controle vooraf

1. Zorg ervoor dat u een geldige Dynamics 365 Commerce-licentie voor aanbevelingen hebt.
1. Controleer of de entiteitswinkel is gekoppeld aan een Azure Data Lake Storage Gen2-account van een klant. Zie [Zorg ervoor dat Azure Data Lake Storage is aangeschaft en in de omgeving is geverifieerd](enable-ADLS-environment.md) voor meer informatie.
1. Bevestig dat Azure AD-identiteitsconfiguratie een vermelding voor aanbevelingen bevat. Hieronder vindt u meer informatie over het uitvoeren van deze actie.
1. Controleer of de dagelijkse vernieuwing van de entiteitswinkel naar Azure Data Lake Storage Gen2 is gepland. Zie [Zorg ervoor dat het vernieuwen van de entiteitsopslag is geautomatiseerd](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) voor meer informatie.
1. RetailSale-afmetingen inschakelen voor entiteitswinkel. Raadpleeg [Werken met maateenheden](/dynamics365/ai/customer-insights/pm-measures) voor meer informatie over het instellen van dit proces.

Nadat de bovenstaande stappen zijn voltooid, bent u gereed om aanbevelingen in te schakelen.

## <a name="azure-ad-identity-configuration"></a>Azure AD-identiteitsconfiguratie

Deze stap is alleen vereist voor alle klanten die een IaaS-configuratie uitvoeren (Infrastructure as a Service). Azure AD De identiteitsconfiguratie wordt automatisch uitgevoerd voor klanten met Azure Service Fabric, maar het wordt aanbevolen om te controleren of de instelling volgens verwachting is geconfigureerd.

### <a name="setup"></a>Instelling

1. Zoek in Commerce Headquarters naar de pagina **Azure Active Directory**-programma's.
1. Controleer of er een vermelding bestaat voor **RecommendationSystemApplication-1**. Als er geen item bestaat, maakt er dan een aan met de volgende informatie:

    - **Client-id**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Naam**: RecommendationSystemApplication-1
    - **Gebruikers-ID**: RetailServiceAccount

1. De pagina opslaan en sluiten 

## <a name="turn-on-recommendations"></a>Aanbevelingen inschakelen

Volg deze stappen om productaanbevelingen in te schakelen.

1. Zoek in Commerce-hoofdkantoren naar **Functiebeheer**.
1. Selecteer **Alles** om een lijst met beschikbare functies weer te geven. 
1. Typ **Aanbevelingen** in het zoekvak.
1. Selecteer de functie **Productaanbevelingen**.
1. Selecteer in het eigenschappenvenster **Productaanbevelingen** de optie **Nu inschakelen**.

![Aanbevelingen inschakelen.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Met de bovenstaande procedure start u het genereren van lijsten voor productaanbevelingen. Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 Commerce.
> - Deze configuratie schakelt niet alle functies voor aanbevelingen in. Geavanceerde functies, zoals persoonlijke aanbevelingen, 'winkelen voor soortgelijke uitstraling'- en 'winkelen voor vergelijkbare beschrijving' worden beheerd door toegewezen invoer in functiebeheer. Raadpleeg ['Persoonlijke aanbevelingen' inschakelen](personalized-recommendations.md), [Aanbevelingen voor vergelijkbare uitstraling inschakelen](shop-similar-looks.md) en [Aanbevelingen voor winkelen voor vergelijkbare beschrijvingen inschakelen](shop-similar-description.md) voor informatie over het inschakelen van deze functies in Commerce Headquarters.

## <a name="configure-recommendation-list-parameters"></a>Parameters voor aanbevelingslijsten configureren

Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden. U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf. Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Aanbevelingen opnemen in de ervaring met e-commerce

Nadat aanbevelingen in Commerce Headquarters zijn ingeschakeld, kunnen de Commerce-modules die worden gebruikt om aanbevelingenresultaten voor e-commerce-ervaringen weer te geven, worden geconfigureerd. Raadpleeg [Modules voor productverzameling](product-collection-module-overview.md) voor meer informatie.

## <a name="show-recommendations-on-pos-devices"></a>Aanbevelingen weergeven op POS-apparaten

Nadat u aanbevelingen in Commerce Headquarters hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het configuratiescherm voor POS met behulp van de indelingsfunctie. Zie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md) voor meer informatie over dit proces. 

## <a name="enable-personalized-recommendations"></a>Gepersonaliseerde aanbevelingen inschakelen

In Dynamics 365 Commerce kunnen detailhandelaren persoonlijke productaanbevelingen maken (ook wel personalisatie genoemd). Op deze manier kunnen persoonlijke aanbevelingen in de online klantervaring en op het verkooppunt (POS) worden opgenomen. Wanneer de functionaliteit voor persoonlijke instellingen is ingeschakeld, kan het systeem de inkoop- en productgegevens van een gebruiker koppelen om individuele productaanbevelingen te genereren.

Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over persoonlijke productaanbevelingen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Productaanbevelingen toevoegen op POS](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
