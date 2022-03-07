---
title: Service voor belastingberekening (Preview)
description: In dit onderwerp worden het algehele bereik en de functies van de service voor belastingberekening uitgelegd.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818219"
---
# <a name="tax-calculation-service-preview"></a>Service voor belastingberekening (Preview)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

De service voor belastingberekening is een hyperschaalbare multitenantservice waarmee de Global Tax Engine het proces voor belastingbepaling en -berekening kan automatiseren en vereenvoudigen. De belastingengine kan volledig worden geconfigureerd. De elementen die kunnen worden geconfigureerd zijn onder andere het belastbare gegevensmodel, de belastingcode, de matrix voor belastingtoepasbaarheid en de formule voor het berekenen van belasting. De belastingengine wordt uitgevoerd op het Microsoft Azure-platform voor kernservices en biedt geavanceerde technologie en exponentiële schaalbaarheid.

De service voor het berekenen van belastingen wordt geïntegreerd met Dynamics 365 Finance en Dynamics 365 Supply Chain Management. Uiteindelijk wordt deze ook geïntegreerd met Dynamics 365 Project Operations, Dynamics 365 Commerce en andere toepassingen van dezelfde leverancier en derden.

De service voor belastingberekening is een op Microsoft gebaseerde belastingengine die exponentiële schaalbaarheid biedt. Hiermee kunt u de volgende taken uitvoeren:

- Configureer de service voor belastingberekening via Regulatory Configuration Service (RCS). RCS is een verbeterde versie van de ER-ontwerper (Electronic Reporting) en is beschikbaar als zelfstandig service.
- Configureer de belastingmatrix om automatisch belastingcodes en -tarieven te bepalen.
- Configureer de belastingmatrix om automatisch het belastingregistratienummer te bepalen.
- Configureer de ontwerper voor belastingberekening om formules en voorwaarden te definiëren.
- Deel de oplossing voor belastingbepaling en -berekening voor rechtspersonen.

Als u de service voor belastingberekening wilt gebruiken, installeert u de invoegtoepassing voor de service vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS). Voltooi vervolgens de instellingen in RCS en schakel de service voor belastingberekeningsservice in Finance en Supply Chain Management in. Zie [Aan de slag met belastingservice](https://go.microsoft.com/fwlink/?linkid=2138482) voor meer informatie.

## <a name="availability"></a>Beschikbaarheid

De service voor belastingberekening is alleen beschikbaar in sandbox-omgevingen en voor bepaalde klanten, via een openbaar preview-programma. Uiteindelijk wordt deze algemeen beschikbaar voor alle klanten en in productieomgevingen.

Nieuwe functies blijven geleverd worden in de service voor belastingberekening. Controleer daarom regelmatig de meest actuele documentatie voor meer informatie over de dekking en het bereik van ondersteunde functies.

De service voor belastingberekening wordt geïmplementeerd in de volgende geografische regio's van Azure. Deze wordt daarnaast geïmplementeerd in andere Azure-regio's op basis van klantbehoeften:

- Verenigde Staten
- Europa
- Frankrijk
- Verenigd Koninkrijk

> [!NOTE]
> De service voor belastingberekening ondersteunt geen on-premises implementaties van Dynamics 365. Ook eerdere versies, zoals Dynamics AX 2012, worden niet ondersteund.

## <a name="feature-highlights"></a>Belangrijkste functies

- Een configureerbare belastingmatrix om automatisch belasting te bepalen en te berekenen
- Ondersteuning voor meerdere btw-registratienummers
- Ondersteuning van transferorders voor het bepalen en berekenen van btw
- Ondersteuning van transferorder voor het bepalen van meerdere btw-registratienummers

## <a name="supported-transactions"></a>Ondersteunde transacties

De service voor belastingberekening kan worden ingeschakeld per rechtspersoon en transactie. De volgende transacties worden ondersteund:

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

[Aan de slag met belastingservice](https://go.microsoft.com/fwlink/?linkid=2138482)

[Meerdere btw-registratienummers](https://go.microsoft.com/fwlink/?linkid=2153387)

[Ondersteuning voor belastingfunctie voor transferorder](https://go.microsoft.com/fwlink/?linkid=2153388)

[Uitbreiding in belastingservice maken](https://go.microsoft.com/fwlink/?linkid=2138483)
