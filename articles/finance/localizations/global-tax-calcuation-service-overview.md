---
title: Belastingberekening (Preview)
description: In dit onderwerp worden het algehele bereik en de functies voor belastingberekening uitgelegd.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e01247cddad4201760fd56e00e05a8373a1ca6ef7c26ae5e1f5cca63bd8a456
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775089"
---
# <a name="tax-calculation-preview"></a>Belastingberekening (Preview)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen. De belastingengine kan volledig worden geconfigureerd. De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting. De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.

Belastingberekening wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management. Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.

> [!IMPORTANT]
> Wanneer u de service voor belastingberekening inschakelt, kunnen bepaalde bewerkingen op gerelateerde gegevens worden uitgevoerd in een ander datacentrum dan het datacentrum dat uw servicegegevens onderhoudt. Controleer de [Algemene voorwaarden](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) voor u de service voor belastingberekening inschakelt. Uw privacy is belangrijk voor ons. Lees onze [Privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) voor meer informatie.

Belastingberekening is een op microservices gebaseerde belastingengine die exponentiële schaalbaarheid biedt. Hiermee kunt u de volgende taken uitvoeren:

- Configureer Belastingberekening via Regulatory Configuration Service (RCS). RCS is een verbeterde versie van de ER-ontwerper (Electronic Reporting) en is beschikbaar als zelfstandig service.
- Configureer de belastingmatrix om automatisch belastingcodes en -tarieven te bepalen.
- Configureer de belastingmatrix om automatisch het belastingregistratienummer te bepalen.
- Configureer de ontwerper voor belastingberekening om formules en voorwaarden te definiëren.
- Deel de oplossing voor belastingbepaling en -berekening voor rechtspersonen.

Als u de service voor belastingberekening wilt gebruiken, installeert u de invoegtoepassing voor de service vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS). Voltooi vervolgens de instellingen in RCS en schakel de service voor belastingberekeningsservice in Finance en Supply Chain Management in. Zie [Aan de slag met belastingservice](./global-get-started-with-tax-calculation-service.md) voor meer informatie.

## <a name="availability"></a>Beschikbaarheid

Belastingberekening is alleen beschikbaar in sandbox-omgevingen en voor bepaalde klanten, via een openbaar preview-programma. Uiteindelijk wordt deze algemeen beschikbaar voor alle klanten en in productieomgevingen.

Er wordt steeds nieuwe functies geleverd. Controleer daarom regelmatig de meest actuele documentatie voor meer informatie over de dekking en het bereik van ondersteunde functies.

Belastingberekening wordt geïmplementeerd in de volgende geografische regio's van Azure. Deze wordt daarnaast geïmplementeerd in andere Azure-regio's op basis van klantbehoeften:

- Verenigde Staten
- Europa

> [!NOTE]
> Belastingberekening ondersteunt geen on-premises implementaties van Dynamics 365. Ook eerdere versies, zoals Dynamics AX 2012, worden niet ondersteund.

## <a name="feature-highlights"></a>Belangrijkste functies

- Een configureerbare belastingmatrix om automatisch belasting te bepalen en te berekenen
- Ondersteuning voor meerdere belastingregistratienummers
- Ondersteuning van transferorders voor het bepalen en berekenen van btw
- Ondersteuning van transferorder voor het bepalen van meerdere belastingregistratienummers

## <a name="supported-transactions"></a>Ondersteunde transacties

Belastingberekening kan worden ingeschakeld per rechtspersoon en transactie. De volgende transacties worden ondersteund:

- Verkoopproces

    - Verkoopofferte
    - Verkooporder
    - Bevestiging
    - Orderverzamellijst
    - Pakbon
    - Verkoopfactuur
    - Creditnota
    - Retourorder
    - Diverse toeslagen voor koptekst
    - Diverse toeslagen voor regels

- Aankoopproces

    - Inkooporder
    - Bevestiging
    - Ontvangstlijst
    - Ontvangst van producten
    - Inkoopfactuur
    - Diverse toeslagen voor koptekst
    - Diverse toeslagen voor regels
    - Creditnota
    - Retourorder
    - Opdracht tot inkoop
    - Diverse toeslagen voor regel van opdracht tot inkoop
    - Offerteaanvraag
    - Diverse toeslagen voor koptekst van offerteaanvraag
    - Diverse toeslagen voor regel van offerteaanvraag

- Voorraadproces

    - Transferorder – verzenden
    - Transferorder – ontvangen

## <a name="related-resources"></a>Gerelateerde bronnen

[Aan de slag met belastingservice](./global-get-started-with-tax-calculation-service.md)

[Meerdere btw-registratienummers](./emea-multiple-vat-registration-numbers.md)

[Ondersteuning voor belastingfunctie voor transferorder](./tasks/tax-feature-support-for-transfer-order.md)

[Uitbreiding in belastingservice maken](./tax-service-add-data-fields-tax-integration-by-extension.md)
