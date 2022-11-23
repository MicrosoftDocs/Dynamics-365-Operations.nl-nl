---
title: Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal
description: In dit artikel wordt beschreven hoe u een Azure Active Directory (Azure AD) B2C-tenant (business-to-consumer) in de Microsoft Azure-portal maakt of koppelt met een bestaande.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785252"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een Azure Active Directory (Azure AD) B2C-tenant (business-to-consumer) in de Microsoft Azure-portal maakt of koppelt. Zie [Zelfstudie: Een Azure Active Directory B2C-tenant maken](/azure/active-directory-b2c/tutorial-create-tenant) voor meer informatie.

Volg deze stappen om een bestaande Azure AD B2C-tenant te maken of te koppelen in de Azure-portal.

1. Meld u aan bij de [Azure-portal](https://portal.azure.com/).
1. Selecteer **Een resource maken** in het menu van Azure Portal. Gebruik het abonnement en de map die met uw Commerce-omgeving worden verbonden.

    ![Een resource maken in Azure Portal.](./media/B2CImage_1.png)

1. Ga naar **Identiteit \> Azure Active Directory B2C**.
1. Op de pagina **Nieuwe B2C-tenant maken of koppelen aan bestaande tenant maken** gebruikt u een van de volgende opties die het beste aansluit bij de behoeften van uw bedrijf:

    - **Een nieuwe Azure AD B2C-tenant maken**: gebruik deze optie om een nieuwe Azure AD B2C-tenant te maken.
        1. Selecteer **Een nieuwe Azure AD B2C-tenant maken**.
        1. Voer onder **Naam van organisatie** de naam van de organisatie in.
        1. Voer bij **Oorspronkelijke domeinnaam** de oorspronkelijke domeinnaam in.
        1. Selecteer het land of de regio bij **Land of regio**.
        1. Selecteer **Maken** om de tenant te maken.

     ![Een nieuwe Azure AD-tenant maken.](./media/B2CImage_2.png)

     - **Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**: gebruik deze optie als u al een Azure AD B2C-tenant hebt waarmee u een koppeling tot stand wilt brengen.
        1. Selecteer **Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**.
        1. Selecteer bij **Azure AD B2C-tenant** de geschikte B2C-tenant. Als het bericht Geen B2C-tenants gevonden die in aanmerking komen wordt weergegeven in het selectievak, beschikt u niet over een bestaande B2C-tenant die in aanmerking komt en moet u een nieuwe maken.
        1. Selecteer **Nieuwe maken** voor **Resourcegroep**. Voer een **naam** in voor de resourcegroep die de tenant moet bevatten, selecteer **de locatie de resourcegroep** en selecteer vervolgens **Maken**.

    ![Een bestaande Azure AD B2C-tenant koppelen aan een Azure-abonnement.](./media/B2CImage_3.png)

1. Zodra de nieuwe Azure AD B2C-map is gemaakt (dit kan even duren), wordt een koppeling naar de nieuwe map weergegeven op het dashboard. Met deze koppeling wordt u naar de pagina Welkom bij Azure Active Directory B2C geleid.

    ![Koppeling naar nieuwe Azure AD-directory](./media/B2CImage_4.png)

> [!NOTE]
> Als u meerdere abonnementen hebt in uw Azure-account of als u de B2C-tenant hebt ingesteld zonder deze aan een actief abonnement te koppelen, kunt u via een banner **Problemen oplossen** de tenant aan een abonnement koppelen. Selecteer het probleemoplossingsbericht en volg de instructies om het probleem met het abonnement op te lossen.

In de volgende afbeelding ziet u een voorbeeld van een Azure AD B2C-banner **Problemen oplossen**.

![Waarschuwing met de melding dat voor de map geen actief abonnement bestaat.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Volgende stappen

Als u wilt doorgaan met het instellen van een B2C-tenant in Commerce, gaat u verder met [De B2C-toepassing maken](create-b2c-app.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[De B2C-toepassing maken](create-b2c-app.md)

[Beleid voor gebruikersstromen maken](create-user-flow-policies.md)

[Providers van sociale identiteiten toevoegen (optioneel)](add-social-identity-providers.md)

[Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md)

[Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Aanvullende B2C-gegevens](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
