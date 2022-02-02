---
title: Beoordelingen en recensies importeren en exporteren
description: In dit onderwerp wordt beschreven hoe u productbeoordelingen en -recensies importeert en exporteert in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 3ae85f21f7a78d56621aed60527207badcee9c75
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968515"
---
# <a name="import-and-export-ratings-and-reviews"></a>Beoordelingen en recensies importeren en exporteren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u productbeoordelingen en -recensies importeert en exporteert in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce biedt [Beoordelingen en recensies](ratings-reviews-overview.md) als een oplossing voor meerdere kanalen. Wanneer u overschakelt naar de oplossing voor beoordelingen en recensies van Dynamics 365 Commerce, wilt u mogelijk uw bestaande beoordelingen en recensies naar het Commerce-platform verplaatsen. Het kan zijn dat u ook beoordelingen en recensies wilt exporteren vanuit Commerce op basis van uw bedrijfsbehoeften. Met een Power Automate-connector kunt u beoordelingen en recensies in Commerce importeren en exporteren vanuit Commerce.

> [!NOTE]
> Zie [Een cloudstroom maken in Power Automate](/power-automate/get-started-logic-flow) voor informatie over het werken met logische stromen in Power Automate.

## <a name="prerequisites"></a>Vereisten

Voordat u beoordelingen en recensies kunt importeren en exporteren, moet u aan de volgende vereisten voldoen:

- De oplossing voor beoordelingen en recensies moet voor uw e-commercesite op het Commerce-platform zijn ingeschakeld. Zie [Aanmelden om beoordelingen en recensies te gebruiken](opt-in-ratings-reviews.md) voor meer informatie.
- De Dynamics 365 Ratings and Reviews Power App Connector moet zijn geconfigureerd voor het indienen of exporteren van beoordelingen in Power Automate. Zie [Dynamics 365 Commerce - beoordelingen en recensies (Preview)](/connectors/dynamics365ratingsre/) voor meer informatie.
- Service-to-service-verificatie (S2S) moet worden geconfigureerd om de API (Application Programming Interface) voor beoordelingen en recensies veilig aan te roepen van buiten Commerce. Zie [Service-to-Service verificatie configureren](service-to-service-auth.md) voor meer informatie.

## <a name="import-ratings-and-reviews"></a>Beoordelingen en recensies importeren

Als u beoordelingen en recensies uit uw bestaande systeem wilt importeren in Commerce, moet u de Dynamics 365 Power Automate-connector voor beoordelingen en recensies toevoegen aan een bestaande of een nieuwe Power Automate-stroom. Zie [Dynamics 365 Commerce - beoordelingen en recensies (Preview)](/connectors/dynamics365ratingsre/) voor meer informatie.

> [!IMPORTANT]
> Voordat u deze procedure kunt uitvoeren, moet u [S2S-verificatie configureren](service-to-service-auth.md).

Volg deze stappen om beoordelingen en recensies te importeren in Commerce met de Dynamics 365 Power Automate-connector voor beoordelingen en recensies.

1. Selecteer de actie **Gebruikersbeoordeling indienen**.
1. Breng een verbinding tot stand met behulp van de gegevens voor de app Azure Active Directory (Azure AD) die is gemaakt toen u S2S-verificatie hebt geconfigureerd. Zie [Service-to-Service verificatie configureren](service-to-service-auth.md) voor meer informatie.
1. Geef voor de actie **Gebruikersbeoordeling indienen** één beoordeling tegelijk op. Herhaal daarom de actie. Gebruik de bronbeoordelingen als een lijst om bulkbeoordelingen in te dienen.
    
## <a name="export-ratings-and-reviews"></a>Beoordelingen en recensies exporteren

Als u beoordelingen en recensies wilt exporteren uit Commerce, moet u de Dynamics 365 Power Automate-connector voor beoordelingen en recensies toevoegen aan een bestaande of een nieuwe Power Automate-stroom. Zie [Dynamics 365 Commerce - beoordelingen en recensies (Preview)](/connectors/dynamics365ratingsre/) voor meer informatie.

Volg deze stappen om beoordelingen en recensies te exporteren uit Commerce met de Dynamics 365 Power Automate-connector voor beoordelingen en recensies.

1. Selecteer de actie **Alle beoordelingen exporteren**.
1. Voltooi de actie. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Aanmelden om beoordelingen en recensies te gebruiken](opt-in-ratings-reviews.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Beoordelingen en recensies configureren](configure-ratings-reviews.md)

[Productbeoordelingen synchroniseren](sync-product-ratings.md)

[Handmatig publiceren van beoordelingen en recensies inschakelen door een moderator](manual-publish-rating-reviews.md)

[Service-to-Service verificatie configureren](service-to-service-auth.md)

[Veelgestelde vragen over beoordelingen en recensies](ratings-reviews-faq.md)
