---
title: Instellingen maateenheid toepassen
description: In dit onderwerp worden instellingen van de maateenheid beschreven en hoe u deze toepast in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fe5cf6b57a8897a0bd541146cb1ad17b496d5633c0a1df9d58b2a4fbc868139
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761509"
---
# <a name="apply-unit-of-measure-settings"></a>Instellingen maateenheid toepassen

[!include [banner](includes/banner.md)]

In dit onderwerp worden instellingen van de maateenheid beschreven en hoe u deze toepast in Microsoft Dynamics 365 Commerce.

Een product kan worden verkocht in verschillende eenheden, zoals 'stuk', 'paar' en 'dozijn'. In Commerce Headquarters kan de maateenheid voor een product worden gedefinieerd en weergegeven op een e-commerce-site. Als een detailhandelaar bijvoorbeeld een product per stuk of per dozijn verkoopt, kunnen de beschikbare maateenheden tegelijk met de andere productgegevens worden weergegeven.

In het onderstaande voorbeeld is een maateenheid per **st** (stuk) geconfigureerd voor een product in Commerce Headquarters.

![Voorbeeld van een product dat is geconfigureerd met een maateenheid in Commerce Headquarters.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Ondersteuning voor het toepassen en weergeven van de maateenheid is beschikbaar vanaf Commerce versie 10.0.19.

## <a name="unit-of-measure-settings"></a>Instellingen maateenheid

U kunt weergave-instellingen voor maateenheden definiëren in Commerce Site Builder, in **Site-instellingen \> Extensies \> Maateenheid voor producten weergeven**. Er zijn drie ondersteunde instellingen:

- **Niet weergeven**: wanneer deze instelling is geselecteerd, wordt de maateenheid voor het product niet weergegeven op de e-commercesite. Dit is het standaardgedrag.
- **Weergeven bij het kopen van producten**: wanneer deze instelling is geselecteerd, wordt de maateenheid weergegeven bij productgegevens, winkelwagen, kassa, orderhistorie en orderdetailpagina's.
- **Weergeven bij het zoeken en kopen van producten**: wanneer deze instelling is geselecteerd, wordt de maateenheid weergegeven op de pagina's waar u producten kunt kopen en tijdens het zoeken naar producten. Als onderdeel van dit gedrag worden maateenheden weergegeven in zoekresultaten en productverzamelingsmodules.

> [!IMPORTANT]
> Weergave-instellingen voor maateenheden zijn beschikbaar vanaf Commerce versie 10.0.19. Als u een oudere versie van Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer instructies.

## <a name="modules-that-use-unit-of-measure-settings"></a>Modules die maateenheidsinstellingen gebruiken

Modules die de maateenheidsinstellingen gebruiken, omvatten de modules koopvak, verlanglijst, winkelwagen, pictogram van winkelwagen, containerzoekresultaten, productverzameling en orderdetails.

In het voorbeeld in de volgende afbeelding ziet u op een pagina met productdetails (PDP) de maateenheid (**st**) voor een product.

![Voorbeeld van een PDP met de maateenheid.](./media/Productunit-PDP.png)

In het voorbeeld in de volgende afbeelding ziet u op een productverzamelingsmodule de maateenheid (**st**) voor een product.

![Voorbeeld van een productverzamelingsmodule met de maateenheid.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Winkelwagenmodule](add-cart-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Accountbeheerpagina's en -modules](account-management.md)

[Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
