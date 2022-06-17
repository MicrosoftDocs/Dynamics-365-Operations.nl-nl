---
title: Scenario's voor het betalen van facturen instellen
description: In dit artikel wordt beschreven hoe u Dynamics 365 Commerce configureert om verschillende scenario's met betrekking tot factuurbetalingen te ondersteunen.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 78af54fec771e5012aca095d07fd772988a56029
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885369"
---
# <a name="set-up-pay-invoice-scenarios"></a>Scenario's voor het betalen van facturen instellen

[!include [banner](includes/banner.md)]

De functionaliteit Factuur betalen in Dynamics 365 Commerce is uitgebreid om het volgende te ondersteunen:

- De betaling van meerdere verkooporderfacturen in één POS-transactie.
- Betaling van verschillende typen klantfacturen, inclusief vrije-tekstfacturen, facturen op basis van projecten en creditnota's.

Om deze scenario's mogelijk te maken moet u het functionaliteitsprofiel voor winkels als volgt configureren.

1. Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen** en selecteer een profiel dat is gekoppeld aan de winkels waarvoor u de wijzigingen wilt doorvoeren.
2. Op het tabblad **Functies** kunt u de volgende parameters naar wens configureren.

    - **Verkooporderfactuur**: selecteer **Ja** om gebruikers in staat te stellen een of meer facturen op basis van verkooporders in één POS-transactie te betalen.
    - **Vrije-tekstfactuur**: selecteer **Ja** om gebruikers in staat te stellen een of meer vrije-tekstfacturen in één POS-transactie te betalen.
    - **Projectfactuur**: selecteer **Ja** om gebruikers in staat te stellen een of meer projectfacturen in één POS-transactie te betalen.
    - **Verkooporder - Creditnota**: selecteer **Ja** om gebruikers in staat te stellen meerdere creditnota's op basis van verkooporders te vereffenen op basis van openstaande facturen of om een restitutie aan de klant te verwerken voor een openstaande creditnota.

> [!NOTE]
> De betaling of vereffening van gedeeltelijke bedragen wordt nog niet ondersteund.


[!INCLUDE[footer-include](../includes/footer-banner.md)]