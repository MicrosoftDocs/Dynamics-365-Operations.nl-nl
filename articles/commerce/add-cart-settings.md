---
title: Instellingen toepassen voor toevoegen van product aan winkelwagen
description: In dit onderwerp worden instellingen voor het toevoegen van producten aan de winkelwagen beschreven en hoe deze worden toegevoegd in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 55b81e7c644f884b052853206f312ac796031600
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479433"
---
# <a name="apply-add-product-to-cart-settings"></a>Instellingen toepassen voor toevoegen van product aan winkelwagen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp worden instellingen voor **Product toevoegen aan winkelwagen beschreven** en hoe deze worden toegevoegd in Microsoft Dynamics 365 Commerce.

Verschillende werkstromen worden ondersteund wanneer een product wordt toegevoegd aan de winkelwagen op een e-commercesite in Dynamics 365 Commerce. De sitegebruiker kan bijvoorbeeld naar de winkelwagenpagina worden overgebracht. Het is ook mogelijk dat de gebruiker op de huidige pagina blijft, maar een melding ontvangt om te bevestigen dat het product aan de winkelwagen is toegevoegd.

Ter ondersteuning van de verschillende werkstromen is een veld **Product toevoegen aan winkelwagen** beschikbaar in **Instellingen \> Extensies** in Commerce Site Builder. Selecteer een van de volgende instellingsopties om de bijbehorende werkstroom te implementeren:

- **Navigeren naar winkelwagen**: wanneer gebruikers een item toevoegen aan de winkelwagen, worden zij naar de winkelwagenpagina overgebracht.
- **Melding weergeven**: wanneer gebruikers een item aan de winkelwagen toevoegen, ontvangen zij een bevestigingsbericht en kunnen zij doorgaan met zoeken op de pagina met productdetails (PDP).
- **Minikar weergeven**: wanneer gebruikers een artikel aan de winkelwagen toevoegen, wordt de inhoud van de minikar weergegeven. Gebruikers kunnen alle items in de winkelwagen controleren en doorgaan met uitchecken als ze gereed zijn.
- **Melding via de module Meldingen tonen**: wanneer gebruikers een item aan de winkelwagen toevoegen, wordt de meldingsmodule gebruikt om een bevestigingsmelding weer te geven. Als u deze instellingsoptie wilt gebruiken, moet de meldingsmodule worden toegevoegd aan de paginakoptekst.
- **Niet navigeren naar winkelwagen**: wanneer gebruikers een item toevoegen aan de winkelwagen, blijven zij op de huidige pagina.

In de volgende afbeelding ziet u een voorbeeld van de instellingsopties voor **Product toevoegen aan winkelwagen** in Site Builder.

![Voorbeeld van de instellingsopties voor Product toevoegen aan winkelwagen in Site Builder](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - De site-instellingen voor **Product toevoegen aan winkelwagen** zijn beschikbaar vanaf Dynamics 365 Commerce versie 10.0.11. Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor informtie over het bijwerken van het bestand appsettings.json.
> - De instellingsoptie **Minikar tonen** is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.20. Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor informtie over het bijwerken van het bestand appsettings.json.

De volgende illustratie toont een voorbeeld van de bevestiging 'toegevoegd aan winkelwagen' op de Fabrikam-site.

![Voorbeeld van een bevestiging 'toegevoegd aan winkelwagen' op de Fabrikam-site](./media/ecommerce-addtocart-notifications.PNG)

De volgende illustratie toont een voorbeeld van de bevestiging 'toegevoegd aan winkelwagen' op de Adventure Works-site.

![Voorbeeld van een bevestiging 'toegevoegd aan winkelwagen' op de Adventure Works-site](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelselectiemodule](store-selector.md)
