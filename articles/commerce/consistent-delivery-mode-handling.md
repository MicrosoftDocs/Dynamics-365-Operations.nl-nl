---
title: Consistente afhandeling van afleveringsmodus in e-commercekanalen inschakelen
description: In dit artikel wordt beschreven hoe u consistente afhandeling van de leveringsmodus kunt inschakelen om mogelijke problemen op te lossen die te maken hebben met toeslagenstromen in Microsoft Dynamics 365 Commerce e-commercekanalen.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: f32f1915f8f7de1d5536b69b05bc74c6149dfda6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885580"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Consistente afhandeling van afleveringsmodus in e-commercekanalen inschakelen 

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u consistente afhandeling van de leveringsmodus kunt inschakelen om mogelijke problemen op te lossen die te maken hebben met toeslagenstromen in Microsoft Dynamics 365 Commerce e-commercekanalen.

In Dynamics 365 Commerce worden niet-pro rata toeslagen op koptekstniveau niet standaard toegepast in e-commercekanalen. Dit gedrag kan voor een of meer van de volgende problemen in e-commercekanalen zorgen:

- Niet-pro rata toeslagen op koptekstniveau worden niet weergegeven.
- De toeslagen voor leveringsmethoden zijn niet consistent tussen de selectie van de leveringsmodus en het overzicht van de uitcheckorder.

Als u deze problemen wilt oplossen, moet u de functie **Consistente afhandeling van afleveringsmodus in kanaal inschakelen** inschakelen. Met deze functie worden niet-pro rata toeslagen op koptekstniveau weergegeven in e-commercekanalen en worden de leveringsgegevens van verkooporders consistent verwerkt via dezelfde aanvraagwerkstroom.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Functie Consistente afhandeling van afleveringsmodus in kanaal inschakelen

Volg deze stappen om de functie **Consistente afhandeling van afleveringsmodus in kanaal inschakelen** in te schakelen in Commerce Headquarters.

1. Open de werkruimte **Functiebeheer** (**Systeembeheer \> Werkruimten \> Functiebeheer**).
1. Zoek in de lijst met beschikbare functies naar **Consistente afhandeling van afleveringsmodus in kanaal inschakelen**.
1. Selecteer **Nu inschakelen** in het rechterdeelvenster.
