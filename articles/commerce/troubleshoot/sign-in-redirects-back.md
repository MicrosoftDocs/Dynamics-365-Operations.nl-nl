---
title: Aanmeldingskoppeling leidt terug naar een e-commercesite
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een aanmeldingskoppeling terugleidt naar de e-commercesite in plaats van naar de aanmeldingspagina.
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
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585259"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Aanmeldingskoppeling leidt terug naar een e-commercesite

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een aanmeldingskoppeling terugleidt naar de e-commercesite in plaats van naar de aanmeldingspagina.

## <a name="description"></a>Beschrijving

Nadat u een nieuwe Microsoft Azure Active Directory B2C-tenant (Azure AD B2C) hebt geconfigureerd in Commerce Site Builder, worden gebruikers die de koppeling **Aanmelden** selecteren teruggeleid naar de hoofdpagina van de e-commercesite zonder naar de aanmeldingspagina te gaan.

## <a name="resolution"></a>Oplossing

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Bevestigen dat de antwoord-URL correct is geconfigureerd in de Azure AD B2C-toepassing

Voer deze stappen uit om te bevestigen dat de antwoord-URL correct is geconfigureerd in de Azure AD B2C-toepassing.

1. Ga naar de [Azure-portal](https://portal.azure.com/).
1. Selecteer de Azure AD B2C-toepassing die u voor toegang tot uw site hebt gemaakt.
1. Selecteer de toepassing die u hebt gemaakt tijdens het instellen van Azure AD B2C.
1. Zorg er onder **Antwoord-URL** voor dat de lijst vermeldingen bevat voor zowel de URL van het sitedomein als de door e-commerce gegenereerde URL, zoals in het voorbeeld in de volgende afbeelding is weergegeven.

    ![Vermeldingen van antwoord-URL in Azure AD B2C](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Zowel de URL van het sitedomein als de URL die door e-commerce is gegenereerd, moeten een geldige URL-indeling hebben die geen voorloop- of volgslashes bevat.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een webtoepassing registreren in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Een B2C-tenant instellen in Commerce](../set-up-b2c-tenant.md)
