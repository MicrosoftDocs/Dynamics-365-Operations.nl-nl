---
title: Resultaten van productaanbevelingen op basis van AI-ML beheren
description: In dit onderwerp wordt uitgelegd hoe u resultaten van productaanbevelingen kunt aanpassen op basis van kunstmatige intelligentie-machine learning (AI-ML) voor uw bedrijf.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5da77f71fb2569adc011bb9ee9c8c795d85545f8
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024997"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a>Resultaten van productaanbevelingen op basis van AI-ML beheren


[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u resultaten van productaanbevelingen kunt aanpassen op basis van kunstmatige intelligentie-machine learning (AI-ML) voor uw bedrijf. 

Nadat de productaanbevelingen zijn ingeschakeld, worden de standaardinstellingen van kracht. Deze parameters werken mogelijk voor meerdere behoeften. Het is aan te raden om enige tijd te besteden aan het evalueren van de resultaten van de verkoopbewegingen van producten. Voordat u de parameters wijzigt, wordt u aangeraden de resultaten te evalueren voordat u ze opnieuw gaat testen. 

## <a name="understanding-recommendation-list-parameters"></a>Parameters voor aanbevelingslijsten begrijpen

Voordat u de parameters wijzigt, moet u weten hoe deze de resultaten hieronder beïnvloeden.

### <a name="trending-product-list"></a>Productlijst 'Trending'

De productlijst 'Trending' bevat twee parameters die kunnen worden gewijzigd:

![Voorbeeld standaardparameter van lijst 'Trending'](./media/exampletrendingparameters.png)

1. **Nieuwe producten van laatste X dagen opnemen**: producten die zijn toegevoegd binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om productkandidaten te selecteren. De standaardwaarde in de afbeelding geeft aan dat producten met een ouderdom van 180 dagen in de lijst met trendproducten kunnen worden gebruikt.
1. **Verkoop van laatste X dagen opnemen**: verkooptransacties die hebben plaatsgevonden binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om producten te bestellen. De standaardwaarde hierboven geeft aan dat alle aankopen van een product in de laatste 30 dagen worden gebruikt om de plaatsing van het product in de lijst met trendproducten te bepalen. 

### <a name="best-selling-product-list"></a>Productlijst 'Meest verkocht'

Afhankelijk van uw bedrijf kunnen de resultaten in de lijst 'Meest verkocht' afwijken van de trend, hoewel ze beide transactiegegevens gebruiken voor het bestellen van producten. Omdat voor Meest verkocht geen einddatum op basis van de assortimentsdatum wordt gebruikt, worden hiermee ook populaire, oudere producten die mogelijk uit de trendlijst zijn verwijderd, worden gemarkeerd. 

De productlijst 'Meest verkocht' bevat één parameter die kan worden gewijzigd:

![Voorbeeld standaardparameter Meest verkochte lijst](./media/examplebestsellingparameters.PNG)

1. **Verkoop van laatste X dagen opnemen**: verkooptransacties die hebben plaatsgevonden binnen het opgegeven aantal dagen voor de huidige datum, kunnen worden gebruikt om producten te bestellen. De standaardwaarde hierboven geeft aan dat alle aankopen van een product in de laatste 30 dagen worden gebruikt om de plaatsing van het product in de lijst met meest verkochte producten te bepalen. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Handmatig producten toevoegen aan of verwijderen uit aanbevelingslijsten

### <a name="for-new-trending-or-best-selling-lists"></a>Voor lijsten 'Nieuw', 'Trending' of 'Meest verkocht'

1.  Ga naar **Retail en Commerce** > **Productaanbevelingen** > **Aanbevelingsparameters**.
1.  Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters.
1.  Selecteer de lijst voor het toevoegen of verwijderen van producten.
1.  Selecteer **Regel toevoegen** om producten aan de tabel toe te voegen. 
1.  Zoek onder de kolom Product naar een product op **naam** of **productnummer**.

    ![Voorbeeld van het zoeken naar een product op de productlijst 'Nieuw'](./media/examplenewlistconfiguration1.png)

1.  Selecteer een van de volgende opties onder de kolom Regeltype:
    -   **Opnemen**: een product aan het begin de lijst plaatsen
    -   **Uitsluiten**: een product uit de lijst verwijderen
    
    ![Voorbeeld van het opnemen of uitsluiten van een product uit de productlijst 'Nieuw'](./media/examplenewlistconfiguration2.png)

1.  Als u de **Weergavevolgorde** wijzigt, wordt de volgorde gewijzigd waarin producten die zijn gemarkeerd als **Opnemen** in de lijst worden weergegeven.
    - Als twee producten dezelfde waarde voor **weergavevolgorde** hebben, kan de uiteindelijke volgorde van de twee resultaten afwijken van de backoffice.
1.  Producten verwijderen uit de tabel: selecteer de regel die u wilt verwijderen en selecteer **Verwijderen**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Voor de lijsten 'Anderen vinden dit ook leuk' of 'Vaak samen gekocht'

In de context van de lijsten 'Vaak samen gekocht' of 'Anderen vinden dit ook leuk', wordt machine learning gebruikt om inkooppatronen voor consumenten te analyseren om verwante producten aan te raden die vaak bij elkaar zijn gekocht voor een uniek seedproduct. 
 
Een *seedproduct* is het product waarvoor u resultaten wilt genereren. In de context van het handmatig aanpassen van aanbevelingslijsten, kunt u resultaten voor dit product toevoegen of verwijderen. 

Voer de volgende stappen uit om handmatig resultaten voor een seed product toe te voegen of te verwijderen:
1.  Selecteer het **Seedproduct**. 
1.  Zoek onder de kolom **Product** naar een product op **Naam** of **Productnummer**
![.Voorbeeld van zoeken naar een product in de lijst Vaak samen gekocht](./media/exampleFBTlistconfiguration1.png)
1. Selecteer een van de volgende opties onder de kolom **Regeltype**:
    - **Opnemen**: een product aan het begin de lijst plaatsen
    - **Uitsluiten**: een product uit de lijst verwijderen     
![Voorbeeld van het opnemen of uitsluiten van een product voor de lijst met vaak samen gekochte producten](./media/exampleFBTlistconfiguration2.png)
1.  Producten verwijderen uit de tabel: selecteer de regel die u wilt verwijderen en selecteer Verwijderen.


## <a name="additional-resources"></a>Aanvullende resources

[Overzicht productaanbevelingen](product-recommendations.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md)

[Lijsten met productaanbevelingen toevoegen aan pagina's](add-reco-list-to-page.md)

[Overzicht productverzamelingsmodule](product-collection-module-overview.md)
