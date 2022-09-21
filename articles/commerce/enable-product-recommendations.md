---
title: Productaanbevelingen inschakelen
description: In dit artikel wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 09/08/2022
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
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460016"
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
1. Controleer of in uw omgeving de serving- en cooking-regio's zijn gedefinieerd in de momenteel ondersteunde regio's, zoals hieronder getoond:

    - **Ondersteunde cooking-regio's:** EU/US/CA/AU.
    - **Ondersteunde serving-regio's:** US/CA/AU. Als de serving-regio niet overeenkomst met een van de bestaande ondersteunde regio's, selecteert de aanbevelingenservice de dichtstbijzijnde ondersteunde serving-regio.

Nadat de bovenstaande stappen zijn voltooid, bent u gereed om aanbevelingen in te schakelen.

> [!NOTE]
> Er is een bekend probleem waarbij aanbevelingen pas worden weergegeven nadat de volgende stappen zijn voltooid. Dit probleem wordt veroorzaakt door gegevensstroomproblemen in de omgeving. Als in uw omgeving geen aanbevelingsresultaten worden gegeven, configureert u de alternatieve gegevens voor de aanbevelingenservice door de stappen te volgen in [Een alternatieve gegevensstroom voor aanbevelingen instellen](set-up-alternate-data-flow.md). U moet beheerdersmachtigingen voor Azure hebben om deze stappen uit te kunnen voeren. Neem contact op met uw FastTrack-vertegenwoordiger als u ondersteuning nodig hebt.

## <a name="azure-ad-identity-configuration"></a>Azure AD-identiteitsconfiguratie

Deze stap is alleen vereist voor alle klanten die een IaaS-configuratie uitvoeren (Infrastructure as a Service). Azure AD-identiteitsconfiguratie is automatisch voor klanten die draaien op Azure Service Fabric, maar het wordt aanbevolen om te controleren of de instelling volgens verwachting is geconfigureerd.

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

[Een alternatieve gegevensstroom voor aanbevelingen instellen](set-up-alternate-data-flow.md)

[Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Productaanbevelingen toevoegen op POS](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
