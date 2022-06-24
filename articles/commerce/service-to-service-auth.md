---
title: Service-to-Service verificatie configureren
description: In dit artikel wordt beschreven hoe u Service-to-Service verificatie configureert in Microsoft Dynamics 365 Commerce om service-API's voor beoordelingen en recensies veilig aan te roepen.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: acb3a6220d146d32bbeb5bd8169033bc897ec3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871602"
---
# <a name="configure-service-to-service-authentication"></a>Service-to-Service verificatie configureren

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u Service-to-Service (S2S) verificatie configureert in Microsoft Dynamics 365 Commerce om service-API's voor beoordelingen en recensies veilig aan te roepen.

Dynamics 365 Commerce biedt [Beoordelingen en recensies](ratings-reviews-overview.md) als een oplossing voor meerdere kanalen. Met deze oplossing is toegang mogelijk tot service-API's buiten Commerce, zodat verschillende taken kunnen worden uitgevoerd. Deze taken omvatten het importeren van beoordelingen en recensies van uw externe systeem in Commerce, en het exporteren van beoordelingen en recensies vanuit Commerce. Als u in Commerce veilig API's voor beoordelingen en recensies wilt aanroepen, moet u S2S-verificatie eerst configureren door de procedures in dit artikel uit te voeren.

## <a name="add-a-new-app-registration"></a>Een nieuwe appregistratie toevoegen

Voordat u een nieuwe appregistratie toevoegt, moet u een toepassing maken met [Azure Portal](https://portal.azure.com). Als u een app wilt registreren in Azure Active Directory (Azure AD) en verificatie wilt inschakelen, volgt u de stappen in [Azure Active Directory gebruiken met een aangepaste connector in Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Verzamel de volgende id's uit Azure Portal. U hebt deze id's nodig in de volgende stappen.

- Clienttoepassings-id
- Clientdirectory-id (tenant)

Voer de volgende stappen uit om een nieuwe appregistratie toe te voegen in Commerce Site Builder.

1. Ga naar **Start \> Recensies \> Instellingen**.
1. Selecteer onder **Service-to-Service verificatie (S2S)** de optie **Beheren**.

    ![De knop Beheren in de sectie Service-to-Service verificatie (S2S) in Commerce Site Builder.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. Selecteer **Nieuwe S2S-appregistratie toevoegen** in het deelvenster **S2S-appvermeldingen** dat rechts verschijnt.
1. Voer in het dialoogvenster **S2S-appvermelding toevoegen** de volgende vereiste informatie in. Gebruik de waarden van uw toepassingsregistratie voor Azure.

    - **Naam**: voer de naam in van uw toepassing (bijvoorbeeld **Fabrikam App**).
    - **Clientapp-id**: voer de toepassings-id in (bijvoorbeeld **00000000-0000-0000-0000-000000000000**).
    - **Directory-id (Tenant)**: voer de directory-id in (bijvoorbeeld **00000000-0000-0000-0000-000000000000**).

    ![Het dialoogvenster S2S-appvermelding toevoegen in Commerce site builder.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Selecteer **Indienen**. De naam van de toepassing moet nu worden weergegeven in de lijst in het deelvenster **S2S-appvermeldingen**.
1. Sluit het deelvenster **S2S-appvermeldingen**.
1. Selecteer **Opslaan**.

## <a name="edit-an-existing-app-registration"></a>Een bestaande appregistratie bewerken

Voer de volgende stappen uit om een bestaande appregistratie te bewerken in Commerce Site Builder.

1. Ga naar **Start \> Recensies \> Instellingen**.
1. Selecteer onder **Service-to-Service verificatie (S2S)** de optie **Beheren**.
1. Selecteer in het deelvenster **S2S-appvermeldingen** het potloodsymbool naast het item dat u wilt bewerken.
1. Werk indien nodig de waarden in de velden **Naam**, **Clientapp-id** en **Directory-id (tenant)** bij.
1. Selecteer **Indienen**.
1. Sluit het deelvenster **S2S-appvermeldingen**.
1. Selecteer **Opslaan**.

## <a name="remove-an-existing-app-registration"></a>Een bestaande appregistratie verwijderen

Voer de volgende stappen uit om een bestaande appregistratie te verwijderen in Commerce Site Builder.

1. Ga naar **Start \> Recensies \> Instellingen**.
1. Selecteer onder **Service-to-Service verificatie (S2S)** de optie **Beheren**.
1. Selecteer in het deelvenster **S2S-appvermeldingen** het prullenbaksymbool naast het item dat u wilt verwijderen. De vermelding wordt uit de lijst verwijderd.
1. Sluit het deelvenster **S2S-appvermeldingen**.
1. Selecteer **Opslaan**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Aanmelden om beoordelingen en recensies te gebruiken](opt-in-ratings-reviews.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Beoordelingen en recensies configureren](configure-ratings-reviews.md)

[Productbeoordelingen synchroniseren](sync-product-ratings.md)

[Handmatig publiceren van beoordelingen en recensies inschakelen door een moderator](manual-publish-rating-reviews.md)

[Beoordelingen en recensies importeren en exporteren](import-export-reviews.md)

[Veelgestelde vragen over beoordelingen en recensies](ratings-reviews-faq.md) 
