---
title: Consistente afhandeling van afleveringsmodus in e-commercekanalen inschakelen
description: In dit onderwerp wordt beschreven hoe u consistente afhandeling van de leveringsmodus kunt inschakelen om mogelijke problemen op te lossen die te maken hebben met toeslagenstromen in Microsoft Dynamics 365 Commerce e-commercekanalen.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349943"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Consistente afhandeling van afleveringsmodus in e-commercekanalen inschakelen 

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u consistente afhandeling van de leveringsmodus kunt inschakelen om mogelijke problemen op te lossen die te maken hebben met toeslagenstromen in Microsoft Dynamics 365 Commerce e-commercekanalen.

In Dynamics 365 Commerce worden niet-pro rata toeslagen op koptekstniveau niet standaard toegepast in e-commercekanalen. Dit gedrag kan voor een of meer van de volgende problemen in e-commercekanalen zorgen:

- Niet-pro rata toeslagen op koptekstniveau worden niet weergegeven.
- De toeslagen voor leveringsmethoden zijn niet consistent tussen de selectie van de leveringsmodus en het overzicht van de uitcheckorder.

Als u deze problemen wilt oplossen, moet u de functie **Consistente afhandeling van afleveringsmodus in kanaal inschakelen** inschakelen. Met deze functie worden niet-pro rata toeslagen op koptekstniveau weergegeven in e-commercekanalen en worden de leveringsgegevens van verkooporders consistent verwerkt via dezelfde aanvraagwerkstroom.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Functie Consistente afhandeling van afleveringsmodus in kanaal inschakelen

Volg deze stappen om de functie **Consistente afhandeling van afleveringsmodus in kanaal inschakelen** in te schakelen in Commerce Headquarters.

1. Open de werkruimte **Functiebeheer** (**Systeembeheer \> Werkruimten \> Functiebeheer**).
1. Zoek in de lijst met beschikbare functies naar **Consistente afhandeling van afleveringsmodus in kanaal inschakelen**.
1. Selecteer **Nu inschakelen** in het rechterdeelvenster.
