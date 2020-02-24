---
title: Beoordelingen en recensies beheren
description: In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies beheert met behulp van het moderatorhulpprogramma Microsoft Dynamics 365 Commerce Beoordelingen en recensies.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027237"
---
# <a name="manage-ratings-and-reviews"></a>Beoordelingen en recensies beheren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u beoordelingen en recensies beheert met behulp van het moderatorhulpprogramma Microsoft Dynamics 365 Commerce Beoordelingen en recensies.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce gebruikt Microsoft Azure Cognitieve service om de recensietekst automatisch te controleren op ongepaste woorden. Bovendien kunnen moderators de functie voor het toezicht op beoordelingen en recensies gebruiken voor de volgende handmatige taken:

- Recensies beheren door ze te beantwoorden of te verwijderen.
- De beoordelingen van een klant verwijderen op verzoek van de klant.
- Gegevens van beoordelingen en recensies voor alle producten importeren in een Microsoft Power BI-sjabloon, zodat trends kunnen worden geanalyseerd.

## <a name="access-ratings-and-reviews-moderation-features"></a>Toegang verkrijgen tot moderatorfuncties voor beoordelingen en recensies

Ga als volgt te werk om moderatorfuncties voor beoordelingen en recensies te bekijken in het beheerhulpprogramma voor e-Commerce-sites.

1. Meld u aan bij [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).
1. Open het project dat de omgeving bevat waarin u e-commerce wilt initialiseren.
1. Selecteer de omgeving in de sectie **Omgevingen**.
1. Selecteer **Retail beheren** onder **Omgevingsfuncties**.
1. Selecteer op het tabblad **e-Commerce** onder **Koppelingen** de optie **Beheerhulpprogramma voor e-Commerce-sites**.

## <a name="read-a-review"></a>Een recensie lezen 

1. Ga naar **Start \> Recensies \> Moderator**.
1. Gebruik het zoekveld in de rechterbovenhoek van de pagina om de recensies te filteren die worden weergegeven op product-id, productnaam of recensietekst.

Met extra filters kunt u de recensies beperken op basis van de periode, beoordeling, kanaal of status (verwijderd, gereageerd of gerapporteerd).

![Startpagina Moderator](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Reageren op een recensie 

Soms geven klanten die een product hebben gekocht, uiting aan hun tevreden- of ontevredenheid of ze begrijpen niet hoe zij het product kunnen gebruiken. Als moderator kunt u een antwoord op een beoordeling plaatsen. Dit antwoord wordt samen met de recensie op de site weergegeven. 

Voer deze stappen uit om op een recensie te reageren.

1. Ga naar **Start \> Recensies \> Moderator**.
1. Zoek en selecteer de recensie waarvoor een antwoord nodig is.
1. Selecteer **Een antwoord toevoegen** in het eigenschappenvenster aan de rechterkant.
1. Voer de tekst van het antwoord en de naam in die voor de beantwoordende persoon moet worden weergegeven. De standaardnaam is **Moderator**.
1. Wanneer u klaar bent, selecteert u **Antwoord publiceren**.

![Reageren op een recensie](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Een beoordeling verwijderen 

Soms is er een zakelijke reden voor moderators om de klantbeoordelingen te verwijderen. 

Voer deze stappen uit om een recensie te verwijderen.

1. Ga naar **Start \> Recensies \> Moderator**.
1. Zoek en selecteer de beoordeling die moet worden verwijderd.
1. Selecteer in het venster Eigenschappen rechts een reden en selecteer vervolgens **Verwijderen**
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>De beoordelingen van een klant verwijderen op verzoek van de klant 

Soms willen klanten hun recensies en beoordelingen permanent van een e-commerce-website laten verwijderen. Een moderator die een aanvraag voor verwijdering van een klant ontvangt, kan de gegevens van de klant verwijderen met behulp van de functie voor het verwijderen van beoordelingen. Als de moderator de gegevens van een klant wil zoeken en verwijderen, is het e-mailadres nodig waarmee de klant zich aanmeldt en recensies aanlevert. 

Voer de volgende stappen uit om klantgegevens te zoeken en te verwijderen.

1. Ga naar **Start \> Recensies \> Verwijderen**.
1. Voer in het veld **Gebruikers zoeken op e-mailadres** het e-mailadres van de klant in en selecteer vervolgens **Zoeken**.
1. Als er voor de klant recensieactiviteiten bestaan (zoals ingediende recensies, stemmen over het nut van recensies van een andere klant of opmerkingen over de recensies van een andere klant), worden de resultaten weergegeven. Voor elk item wordt een knop **Verwijderen** getoond.
1. Selecteer **Verwijderen** voor elk item dat moet worden verwijderd. Selecteer **Ja** als u om een bevestiging wordt gevraagd. 
    
![Klantgegevens verwijderen](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Het kan maximaal zeven dagen duren voordat gegevens volledig uit het systeem zijn verwijderd. Moderators moeten klanten informeren over deze vertraging.
> - Als klanten hun naam hebben gewijzigd in hun accountinstellingen, kunnen er meerdere items worden weergegeven in de zoekresultaten. Als u in dit geval de gegevens van de klant volledig wilt verwijderen, moet de moderator voor elk artikel de optie **Verwijderen** selecteren. 

## <a name="download-ratings-and-reviews-data"></a>Gegevens over beoordelingen en recensies downloaden

Met het moderatorhulpprogramma voor beoordelingen en recensies kunnen moderators de gegevens van de beoordelingen en recensies in bulk importeren, zodat ze trends kunnen analyseren. Er is een Power BI-sjabloon beschikbaar die eenvoudige metrische gegevens bevat. Moderators kunnen deze sjabloon gebruiken om in bulk geïmporteerde gegevens te verbinden en een dashboard te bekijken. Ze hoeven geen aangepast dashboard te maken. Moderators kunnen de Power BI-sjabloon ook aan hun specifieke behoeften aanpassen. 

Ga als volgt te werk om gegevens over beoordelingen en recensies te downloaden.

1. Ga naar **Start \> Recensies \> Rapporteren**.
1. Selecteer **Gegevens van recensies downloaden** om gegevens van beoordelingen en recensies in bulk te downloaden in de CSV-indeling (door komma's gescheiden waarden).

## <a name="view-ratings-and-reviews-trends"></a>Trends voor beoordelingen en recensies weergeven

Moderators kunnen de Power BI-sjabloon downloaden zodat ze trends in een dashboard kunnen weergeven.

Volg deze stappen om trends voor beoordelingen en recensies te downloaden.

1. Ga naar **Start \> Recensies \> Rapporteren**.
1. Selecteer **PowerBI-sjabloon** om de sjabloon te downloaden.

    ![De Power BI-sjabloon downloaden](media/rnr-moderation-reports.png) 

1. Open de gedownloade sjabloon met de Power BI-app. Sluit het dialoogvenster **Toegang tot webinhoud** dat wordt weergegeven en sluit het foutbericht "Vernieuwen" dat wordt weergegeven.
1. Ga naar **Start**, selecteer **Query's bewerken** en selecteer vervolgens **Instellingen van gegevensbron**.
1. Selecteer **Bron wijzigen** in het dialoogvenster **Instellingen van gegevensbron**.
1. Voer in het veld **URL** het pad van de revisiegegevens in die u in de vorige procedure hebt gedownload (bijvoorbeeld **c:\\reviews\\ReviewsData.csv**).

    ![URL-veld in het dialoogvenster Door komma's gescheiden waarden](media/rnr-powerbi-datasource-settings.png) 

1. Selecteer **OK** en vervolgens **Wijzigingen toepassen**. Het kan één tot twee minuten duren voordat uw wijzigingen worden toegepast op de gegevensbron.
1. Selecteer **Blad met trends** om trends voor beoordelingen en recensies te bekijken.

    ![Trends voor beoordelingen en recensies](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Aanvullende resources

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Aanmelden om beoordelingen en recensies te gebruiken](opt-in-ratings-reviews.md)

[Beoordelingen en recensies configureren](configure-ratings-reviews.md)

[Productbeoordelingen synchroniseren in Dynamics 365 Retail](sync-product-ratings.md)
