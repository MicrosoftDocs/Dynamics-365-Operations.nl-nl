---
title: Productaanbevelingen inschakelen
description: In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b201e5481cfaf5bb6cd64a89cdb6b5a91f31447f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411260"
---
# <a name="enable-product-recommendations"></a>Productaanbevelingen inschakelen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce. Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Aanbevelingen voor controle vooraf

Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-klanten die hun opslag hebben gemigreerd met behulp van Azure Data Lake Storage. 

De volgende configuraties moeten zijn ingeschakeld in de backoffice voordat u aanbevelingen kunt inschakelen:

1. Zorg ervoor dat Azure Data Lake Storage is aangeschaft en in de omgeving is geverifieerd. Zie [Zorg ervoor dat Azure Data Lake Storage is aangeschaft en in de omgeving is geverifieerd](enable-ADLS-environment.md) voor meer informatie.
2. Zorg ervoor dat het vernieuwen van de entiteitsopslag is geautomatiseerd. Zie [Zorg ervoor dat het vernieuwen van de entiteitsopslag is geautomatiseerd](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) voor meer informatie.
3. Bevestig dat Azure AD-identiteitsconfiguratie een vermelding voor aanbevelingen bevat. Hieronder vindt u meer informatie over het uitvoeren van deze actie.

Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld. Zie [Werken met maateenheden](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) voor meer informatie over dit instelproces.

## <a name="azure-ad-identity-configuration"></a>Azure AD-identiteitsconfiguratie

Deze stap is vereist voor alle klanten die een service IaaS-configuratie uitvoeren (Infrastructure as a Service). Voor klanten die met een Service Fabric (SF) werken, moet deze stap automatisch worden uitgevoerd. Het wordt aangeraden om de instelling te controleren.

### <a name="setup"></a>Instelling

1. Zoek vanuit de backoffice naar de pagina **Azure Active Directory-toepassingen**.
2. Controleer of er een vermelding bestaat voor "RecommendationSystemApplication-1".

Als de vermelding nog niet bestaat, voegt u een nieuwe vermelding toe met de volgende informatie:

- **Client-id** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Naam** - RecommendationSystemApplication-1
- **Gebruikers-id** - RetailServiceAccount

De pagina opslaan en sluiten 

## <a name="turn-on-recommendations"></a>Aanbevelingen inschakelen

Volg deze stappen om productaanbevelingen in te schakelen.

1. Zoek in Commerce-hoofdkantoren naar **Functiebeheer**.
1. Selecteer **Alles** om een lijst met beschikbare functies weer te geven. 
1. Typ **Aanbevelingen** in het zoekvak.
1. Selecteer de functie **Productaanbevelingen**.
1. Selecteer in het eigenschappenvenster **Productaanbevelingen** de optie **Nu inschakelen**.

![Aanbevelingen inschakelen](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Met deze procedure start u het genereren van lijsten voor productaanbevelingen. Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Parameters voor aanbevelingslijsten configureren

Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden. U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf. Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Aanbevelingen weergeven op POS-apparaten

Nadat u aanbevelingen in de Commerce-backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie. Zie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md) voor meer informatie over dit proces. 

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

