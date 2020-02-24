---
title: ADLS inschakelen in een Dynamics 365 Commerce-omgeving
description: In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage (ADLS) voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025236"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>ADLS inschakelen in een Dynamics 365 Commerce-omgeving

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u Azure Data Lake Storage (ADLS) voor een Dynamics 365 Commerce-omgeving kunt inschakelen en testen. Dit is een vereiste voor het inschakelen van productaanbevelingen.

## <a name="overview"></a>Overzicht

In de Dynamics 365 Commerce-oplossing worden alle product- en transactiegegevens bijgehouden in het entiteitsarchief van de omgeving. Als u deze gegevens toegankelijk wilt maken voor andere Dynamics 365-services, zoals gegevensanalyse, Business Intelligence en persoonlijke aanbevelingen, is het noodzakelijk de omgeving te verbinden met een Azure Data Lake Storage Gen 2-oplossing (ADLS) van de klant.

Aangezien ADLS in een omgeving is geconfigureerd, worden alle benodigde gegevens gespiegeld vanuit de entiteitsopslag en zijn deze nog steeds beveiligd en onder controle van de klant.

Als er ook productaanbevelingen of persoonlijke aanbevelingen in de omgeving zijn ingeschakeld, wordt toegang verleend aan de productaanbevelingsstack tot de speciale map in ADLS om de gegevens van de klant op basis hiervan op te halen en aanbevelingen te berekenen.

## <a name="prerequisites"></a>Vereisten

Klanten moeten ADLS geconfigureerd hebben in een Azure-abonnement. Dit onderwerp geldt niet voor de aankoop van een Azure-abonnement of het instellen van een ADLS-opslagaccount.

Zie [Officiële ADLS-documentatie](https://azure.microsoft.com/pricing/details/storage/data-lake) voor meer informatie over ADLS.
  
## <a name="configuration-steps"></a>Configuratiestappen

In deze sectie worden de configuratiestappen beschreven die nodig zijn om ADLS in een omgeving in te schakelen.

### <a name="enable-adls-in-the-environment"></a>ADLS in de omgeving inschakelen

1. Meld u aan bij de backoffice-portal van de omgeving.
1. Zoek **Systeemparameters** en navigeer naar het tabblad **Gegevensverbindingen**. 
1. Stel **Data Lake-integratie inschakelen** in op **Ja**.
1. Stel **Data Lake in kleine delen bijwerken** in op **Ja**.
1. Voer dan de volgende vereiste informatie in:
    1. **Toepassings-id** // **Toepassingsgeheim** // **DNS-naam**: vereist om verbinding te maken met KeyVault, waar het ADLS-geheim is opgeslagen.
    1. **Geheime naam**: de geheime naam die in KeyVault is opgeslagen en die wordt gebruikt voor verificatie met ADLS.
1. Sla uw wijzigingen op in de linkerbovenhoek van de pagina.

In de volgende afbeelding ziet u een voorbeeld van een ADLS-configuratie.

![Voorbeeld van ADLS-configuratie](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>De ADLS-verbinding testen

1. Test de verbinding met KeyVault via de koppeling **Azure KeyVault testen**.
1. Test de verbinding met ADLS via de koppeling **Azure-opslag testen**.

> [!NOTE]
> Als de tests mislukken, controleert u of alle bovenstaande informatie over KeyVault juist is en probeer het opnieuw.

Nadat de verbindingstest is voltooid, moet u automatisch vernieuwen inschakelen voor de entiteitsopslag.

Voer de volgende stappen uit om het automatisch vernieuwen van de entiteitsopslag in te schakelen.

1. Zoek **Entiteitsopslag**.
1. Ga in lijst aan de linkerkant naar het item **RetailSales** en selecteer **Bewerken**.
1. Controleer of **Automatisch vernieuwen ingeschakeld** is ingesteld op **Ja**, selecteer **Vernieuwen** en selecteer **Opslaan**.

De volgende afbeelding toont een voorbeeld van een entiteitsopslag waarvoor automatisch vernieuwen is ingeschakeld.

![Voorbeeld van entiteitsopslag met automatisch vernieuwen ingeschakeld](./media/exampleADLSConfig2.png)

ADLS wordt nu geconfigureerd voor de omgeving. 

Als u nog niet klaar bent, voert u de stappen voor [productaanbevelingen en -aanpassingen inschakelen](enable-product-recommendations.md) voor de omgeving uit.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht productaanbevelingen](product-recommendations.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Lijsten met productaanbevelingen toevoegen aan pagina's](add-reco-list-to-page.md)

[Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


