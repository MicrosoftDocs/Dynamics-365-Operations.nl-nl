---
title: Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving
description: In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.
author: bebeale
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61f96dae0643e3383afd91864e4c145f3b5c04c8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792602"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.

In de Dynamics 365 Commerce-oplossing worden alle product- en transactiegegevens bijgehouden in het entiteitsarchief van de omgeving. Als u deze gegevens toegankelijk wilt maken voor andere Dynamics 365-services, zoals gegevensanalyse, Business Intelligence en persoonlijke aanbevelingen, is het noodzakelijk de omgeving te verbinden met een Azure Data Lake Storage Gen 2-oplossing van de klant.

Aangezien Azure Data Lake Storage in een omgeving is geconfigureerd, worden alle benodigde gegevens gespiegeld vanuit de entiteitsopslag en zijn deze nog steeds beveiligd en onder controle van de klant.

Als er ook productaanbevelingen of persoonlijke aanbevelingen in de omgeving zijn ingeschakeld, wordt toegang verleend aan de productaanbevelingsstack tot de speciale map in Azure Data Lake Storage om de gegevens van de klant op basis hiervan op te halen en aanbevelingen te berekenen.

## <a name="prerequisites"></a>Vereisten

Klanten moeten Azure Data Lake Storage geconfigureerd hebben in een Azure-abonnement. Dit onderwerp geldt niet voor de aankoop van een Azure-abonnement of het instellen van een Azure Data Lake Storage-opslagaccount.

Zie [Officiële Azure Data Lake Storage Gen2-documentatie](https://azure.microsoft.com/pricing/details/storage/data-lake) voor meer informatie over Azure Data Lake Storage.
  
## <a name="configuration-steps"></a>Configuratiestappen

In deze sectie worden de configuratiestappen beschreven die nodig zijn om Azure Data Lake Storage in een omgeving in te schakelen vanwege de samenhang met productaanbevelingen.
Zie [Entiteitopslag beschikbaar maken als een Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) voor een uitgebreidere beschrijving van de stappen die nodig zijn om Azure Data Lake Storage in te schakelen.

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Azure Data Lake Storage in de omgeving inschakelen

1. Meld u aan bij de backoffice-portal van de omgeving.
1. Zoek **Systeemparameters** en navigeer naar het tabblad **Gegevensverbindingen**. 
1. Stel **Data Lake-integratie inschakelen** in op **Ja**.
1. Stel **Data Lake in kleine delen bijwerken** in op **Ja**.
1. Voer dan de volgende vereiste informatie in:
    1. **Toepassings-id** // **Toepassingsgeheim** // **DNS-naam**: vereist om verbinding te maken met KeyVault, waar het Azure Data Lake Storage-geheim is opgeslagen.
    1. **Geheime naam**: de geheime naam die in KeyVault is opgeslagen en die wordt gebruikt voor verificatie met Azure Data Lake Storage.
1. Sla uw wijzigingen op in de linkerbovenhoek van de pagina.

In de volgende afbeelding ziet u een voorbeeld van een Azure Data Lake Storage-configuratie.

![Voorbeeld van Azure Data Lake Storage-configuratie](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>De Azure Data Lake Storage-verbinding testen

1. Test de verbinding met KeyVault via de koppeling **Azure KeyVault testen**.
1. Test de verbinding met Azure Data Lake Storage via de koppeling **Azure-opslag testen**.

> [!NOTE]
> Als de tests mislukken, controleert u of alle bovenstaande informatie over KeyVault juist is en probeer het opnieuw.

Nadat de verbindingstest is voltooid, moet u automatisch vernieuwen inschakelen voor de entiteitsopslag.

Voer de volgende stappen uit om het automatisch vernieuwen van de entiteitsopslag in te schakelen.

1. Zoek **Entiteitsopslag**.
1. Ga in lijst aan de linkerkant naar het item **RetailSales** en selecteer **Bewerken**.
1. Controleer of **Automatisch vernieuwen ingeschakeld** is ingesteld op **Ja**, selecteer **Vernieuwen** en selecteer **Opslaan**.

De volgende afbeelding toont een voorbeeld van een entiteitsopslag waarvoor automatisch vernieuwen is ingeschakeld.

![Voorbeeld van entiteitsopslag met automatisch vernieuwen ingeschakeld](./media/exampleADLSConfig2.png)

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
