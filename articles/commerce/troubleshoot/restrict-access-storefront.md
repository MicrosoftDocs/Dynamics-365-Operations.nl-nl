---
title: Toegang tot een winkel beperken tijdens het testen of ontwikkelen
description: In dit artikel wordt uitgelegd hoe u de toegang tot een Microsoft Dynamics 365 Commerce-winkel kunt beperken terwijl interne testen of ontwikkeling plaatsvinden.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 77b652aafa6aea807ab11fe02209bc7de43fa446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898879"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Toegang tot een winkel beperken tijdens het testen of ontwikkelen

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de toegang tot een Microsoft Dynamics 365 Commerce-winkel kunt beperken terwijl interne testen of ontwikkeling plaatsvinden.

## <a name="description"></a>Beschrijving

Tijdens het interne testen of tijdens de actieve ontwikkeling wilt u mogelijk de toegang tot uw site beperken om te voorkomen dat externe gebruikers de gepubliceerde pagina's van winkels openen.

## <a name="resolution"></a>Oplossing

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Azure AD B2C instellen met behulp van standaardgebruikersstromen

Zie [Een B2C-tenant instellen in Commerce](../set-up-b2c-tenant.md) voor informatie over het configureren van Azure Active Directory B2C (Azure AD B2C) voor uw e-commercesite.

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Toegang van gebruikers tot winkelpagina's beperken en het maken van nieuwe gebruikers blokkeren

Volg deze stappen om gebruikerstoegang tot winkelpagina's in Commerce Site Builder te beperken.

1. Ga naar uw site.
1. Selecteer **Pagina's** en selecteer vervolgens de pagina waarvoor u de gebruikerstoegang wilt beperken.
1. Selecteer het module- of fragmentvak en selecteer **Bewerken**.
1. Selecteer In het eigenschappendeelvenster de optie **Aanmelden vereist?** en selecteer **Bewerken voltooien**.
1. Selecteer **Publiceren**.

Volg deze stappen om het maken van nieuwe Azure AD-gebruikers te blokkeren.

1. Ga naar de [Azure-portal](https://portal.azure.com/).
1. Selecteer de Azure AD B2C-toepassing die u voor toegang tot uw site hebt gemaakt.
1. Selecteer **Gebruikersstromen** in het navigatievenster aan de linkerkant.
1. Selecteer boven aan de pagina **Gebruikersstromen** de optie **Nieuwe gebruikersstroom**.
1. Selecteer op de pagina **Een gebruikersstroomtype selecteren** de optie **Voorbeeld**.
1. Selecteer **Aanmelden v2** op het midden van de pagina. Volg daarna de stappen in [Een B2C-tenant instellen in Commerce](../set-up-b2c-tenant.md) om de stroom te configureren als de standaardgebruikersstroom van uw site voor Azure AD B2C tijdens het testen of ontwikkelen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](../set-up-b2c-tenant.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](../custom-pages-user-logins.md)
