---
title: Het Adventure Works-thema installeren
description: In dit onderwerp wordt beschreven hoe u het Adventure Works-thema installeert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ad704c6c3b95abcfd52e449a0ffbb4b82b236498ae8d2775c4e65811de3ef503
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763831"
---
# <a name="install-the-adventure-works-theme"></a>Het Adventure Works-thema installeren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u het Adventure Works-thema installeert in Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Het Adventure Works-thema en modules zijn beschikbaar vanaf Dynamics 365 Commerce versie 10.0.20. Zij zijn beschikbaar vanuit Microsoft AppSource.

## <a name="prerequisites"></a>Vereisten

Voordat u het Adventure Works-thema installeert, moet u een Dynamics 365 Commerce-omgeving (Commerce versie 10.0.20 of hoger) hebben waarin Retail Cloud Scale Unit (RCSU), de Commerce online Software Development Kit (SDK) en de Commerce-modulebibliotheek zijn. Zie [SDK en modulesbibliotheekupdates](e-commerce-extensibility/sdk-updates.md) voor informatie over het installeren van de Commerce SDK en de modulebibliotheek. 

## <a name="installation-steps"></a>Installatiestappen

### <a name="install-the-adventure-works-theme-in-your-application"></a>Het Adventure Works-thema in uw toepassing installeren

Het pakket van het Adventure Works-thema is beschikbaar in de feed **dynamics365-commerce** als **@msdyn365-commerce-thema/adventuredynamic-thema-kit**. Hoewel het pakket van het Adventure Works-thema deel uitmaakt van die feed, valt het onder een andere naamruimte. Daarom moet u deze stappen volgen om registervermeldingen voor de naamruimte toe te voegen.

1. Werk het **.npmrc**-bestand bij zodat het de volgende registervermelding bevat (als de vermelding nog niet is opgenomen):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Werk het **.yarnrc**-bestand bij zodat het de volgende registervermelding bevat (als de vermelding nog niet is opgenomen):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Als u het pakket in de lokale omgeving wilt installeren, moet u de volgende opdracht uitvoeren via de opdrachtprompt. Met deze opdracht wordt het bestand package.json automatisch bijgewerkt zodat het de afhankelijkheid bevat.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

In het bestand **package.json** moet u de themaversie bijwerken naar een specifieke versie.

> [!IMPORTANT]
> - De themaversie moet overeenkomen met de versie van de modulebibliotheek om ervoor te zorgen dat alle functies werken zoals verwacht. 
> - De minimumversie voor de Commerce-modulebibliotheek en SDK moet beschikbaar zijn 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>De lettertypetekenbestanden voor het Adventure Works-thema toevoegen

Nadat het Adventure Works-thema in uw app is geïnstalleerd, moet u de vereiste lettertypebestanden voor de app toevoegen. Om deze stap te voltooien, kopieert u alle lettertypebestanden van **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** naar het pad van de openbare directory van de partnertoepassing **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>De resources voor het Adventure Works-thema instellen

De volgende stap is het bijwerken van de vereiste standaardresource voor het thema. Om deze stap te voltooien, kopieert u de inhoud van het bestand global.json onder **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** naar het bestand global.json van de partnertoepassing onder **\src\resources\modules**. Als de doeldirectory **\src\resources** niet bestaat, kan deze in zijn geheel worden gekopieerd van de brondirectory **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** naar de doeldirectory **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>Updates ophalen en het thema valideren

Zie de sectie 'Updates ophalen' van [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#pull-updates) voor informatie over het ontvangen van de nieuwste updates van SDK, modulebibliotheek en andere afhankelijkheden.

Nadat de laatste afhankelijkheden zijn gedefinieerd, kunt u de opdracht **yarn start** uitvoeren om de knooppuntserver te starten in uw ontwikkelomgeving en het nieuwe Adventure Works-thema te testen. Blader lokaal door de toepassing met behulp van de queryreeksparameter `?theme=adventureworks` (bijvoorbeeld `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Aanvullende bronnen

[Adventure Works-thema](adventure-works-theme.md)

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
