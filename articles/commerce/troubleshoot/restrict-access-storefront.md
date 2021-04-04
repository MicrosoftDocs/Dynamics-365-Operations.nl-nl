---
title: Toegang tot een winkel beperken tijdens het testen of ontwikkelen
description: In dit onderwerp wordt uitgelegd hoe u de toegang tot een Microsoft Dynamics 365 Commerce-winkel kunt beperken terwijl interne testen of ontwikkeling plaatsvinden.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585271"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Toegang tot een winkel beperken tijdens het testen of ontwikkelen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de toegang tot een Microsoft Dynamics 365 Commerce-winkel kunt beperken terwijl interne testen of ontwikkeling plaatsvinden.

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
