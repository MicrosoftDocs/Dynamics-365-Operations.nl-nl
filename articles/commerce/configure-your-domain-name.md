---
title: Uw domeinnaam configureren
description: In dit onderwerp wordt uitgelegd hoe u een domeinnaam configureert voor Microsoft Dynamics 365 e-commerce-site.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796046"
---
# <a name="configure-your-domain-name"></a>Uw domeinnaam configureren


[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een domeinnaam configureert voor Microsoft Dynamics 365 e-commerce-site. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domeinen toevoegen tijdens e-commerce-initialisatie

Als u domeinen wilt koppelen aan uw Dynamics 365 Commerce e-commerce-omgeving, initialiseert u e-Commerce zoals beschreven in [Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md). Tijdens de initialisatie wordt u gevraagd informatie op te geven die wordt gebruikt om uw e-commerce-omgeving in te richten. Voeg in het veld **Ondersteunde hostnamen** alle domeinen toe die u met deze omgeving wilt gebruiken. Meerdere domeinen moeten worden gescheiden door een puntkomma. Op deze manier worden de domeinen geconfigureerd in alle vereiste e-commerce-onderdelen en kunnen ze worden gebruikt wanneer u verkeer van uw CDN (Content Delivery Network) of webserver overbrengt naar de e-commerce front-ends.

## <a name="add-domains-after-e-commerce-initialization"></a>Domeinen toevoegen na e-commerce-initialisatie

Als u na de e-commerce-initialisatie nieuwe domeinen wilt koppelen aan uw e-commerce-omgeving, moet u een serviceaanvraag indienen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[robots.txt-bestanden beheren](manage-robots-txt-files.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

[Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-B2C-tenants.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]