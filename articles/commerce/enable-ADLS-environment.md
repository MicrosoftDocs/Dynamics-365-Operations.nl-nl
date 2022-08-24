---
title: Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving
description: Dit artikel geeft instructies voor het verbinden van een Azure Data Lake Storage Gen 2-oplossing met een Dynamics 365 Commerce-entiteitswinkel van een omgeving. Dit is een vereiste stap voordat productaanbevelingen worden ingeschakeld.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: d7995e826a838796f714ced2f30220201a157f93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284740"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving

[!include [banner](includes/banner.md)]

Dit artikel geeft instructies voor het verbinden van een Azure Data Lake Storage Gen 2-oplossing met een Dynamics 365 Commerce-entiteitswinkel van een omgeving. Dit is een vereiste stap voordat productaanbevelingen worden ingeschakeld.

In de Dynamics 365 Commerce-oplossing worden de gegevens die nodig zijn om aanbevelingen, producten en transacties te berekenen, samengevoegd in de entiteitswinkel van de omgeving. Om deze gegevens toegankelijk te maken voor andere Dynamics 365-services, zoals gegevensanalyse, Business Intelligence en persoonlijke aanbevelingen, is het noodzakelijk de omgeving te verbinden met een Azure Data Lake Storage Gen 2-oplossing van de klant.

Nadat de bovenstaande stappen zijn voltooid, worden alle klantgegevens in de entiteitswinkel van de omgeving automatisch weerspiegeld in de Azure Data Lake Storage Gen 2-oplossing van de klant. Wanneer aanbevelingenfuncties zijn ingeschakeld via het werkgebied voor functiebeheer in Commerce Headquarters, krijgt de aanbevelingenstapel toegang tot dezelfde Azure Data Lake Storage Gen 2-oplossing.

De gegevens van klanten blijven gedurende het gehele proces beveiligd en onder hun controle.

## <a name="prerequisites"></a>Vereisten

De entiteitswinkel van een Dynamics 365 Commerce-omgeving moet zijn verbonden met een Azure Data Lake Gen Storage Gen2-account en bijbehorende services.

Raadpleeg de [Officiële documentatie Azure Data Lake Storage Gen 2](https://azure.microsoft.com/pricing/details/storage/data-lake) voor meer informatie over Azure Data Lake Storage Gen 2 en het instellen ervan.
  
## <a name="configuration-steps"></a>Configuratiestappen

In dit gedeelte worden de configuratiestappen beschreven die nodig zijn om Azure Data Lake Storage Gen 2 in een omgeving in te schakelen vanwege de samenhang met productaanbevelingen.
Raadpleeg [Entiteitopslag beschikbaar maken als een Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) voor een uitgebreider beschrijving van de stappen die nodig zijn om Azure Data Lake Storage Gen 2 in te schakelen.

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Azure Data Lake Storage in de omgeving inschakelen

1. Meld u aan bij de backoffice-portal van de omgeving.
1. Zoek **Systeemparameters** en navigeer naar het tabblad **Gegevensverbindingen**. 
1. Stel **Data Lake-integratie inschakelen** in op **Ja**.
1. Voer dan de volgende vereiste informatie in:
    1. **Toepassings-id** // **Toepassingsgeheim** // **DNS-naam**: vereist om verbinding te maken met KeyVault, waar het Azure Data Lake Storage-geheim is opgeslagen.
    1. **Geheime naam**: de geheime naam die in KeyVault is opgeslagen en die wordt gebruikt voor verificatie met Azure Data Lake Storage.
1. Sla uw wijzigingen op in de linkerbovenhoek van de pagina.

In de volgende afbeelding ziet u een voorbeeld van een Azure Data Lake Storage-configuratie.

![Voorbeeld van Azure Data Lake Storage-configuratie.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>De Azure Data Lake Storage-verbinding testen

1. Test de verbinding met KeyVault via de koppeling **Azure KeyVault testen**.
1. Test de verbinding met Azure Data Lake Storage via de koppeling **Azure-opslag testen**.

> [!NOTE]
> Als een van de bovenstaande tests mislukt, bevestig dan dat alle bovenstaande informatie over KeyVault juist is en probeer het opnieuw.

Nadat de verbindingstest is voltooid, moet u automatisch vernieuwen inschakelen voor de entiteitsopslag.

Voer de volgende stappen uit om het automatisch vernieuwen van de entiteitsopslag in te schakelen.

1. Zoek **Entiteitsopslag**.
1. Ga in lijst aan de linkerkant naar het item **RetailSales** en selecteer **Bewerken**.
1. Controleer of **Automatisch vernieuwen ingeschakeld** is ingesteld op **Ja**, selecteer **Vernieuwen** en selecteer **Opslaan**.

De volgende afbeelding toont een voorbeeld van een entiteitsopslag waarvoor automatisch vernieuwen is ingeschakeld.

![Voorbeeld van entiteitsopslag met automatisch vernieuwen ingeschakeld.](./media/exampleADLSConfig2.png)

Azure Data Lake Storage wordt nu geconfigureerd voor de omgeving. 

Als u nog niet klaar bent, voert u de stappen voor [productaanbevelingen en -aanpassingen inschakelen](enable-product-recommendations.md) voor de omgeving uit.

## <a name="additional-resources"></a>Aanvullende bronnen

[Entiteitopslag beschikbaar maken als een Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Overzicht productaanbevelingen](product-recommendations.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Productaanbevelingen op POS toevoegen](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
