---
title: Adviesprijsrapporten
description: Dit artikel biedt een overzicht van de prijsrapportfunctie die kan worden gebruikt om de komende prijswijzigingen voor de verschillende producten weer te geven.
author: shajain
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 84025cf148e1b5a92b78593fc093c629a3af4764
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899036"
---
# <a name="retail-price-reports"></a>Adviesprijsrapporten

[!include [banner](includes/banner.md)]


Om concurrerende prijzen aan hun klanten te bieden wijzigen winkeliers vaak prijzen van hun producten. Winkelmanagers willen eenvoudig toegang tot recente of komende prijswijzigingen zodat ze de vereiste resources kunnen plannen om de prijsetiketten op de winkelschappen bij te werken. Met release 10.0 van Retail kan een winkelmanager het rapport **Prijs** openen door te navigeren naar **Alle winkels \> Winkel \> Prijsrapport** en de bijgewerkte prijzen weer te geven voor de producten die zijn gekoppeld aan de winkel. 

Om het prijsrapport in te schakelen moet de parameter **Prijsrapport inschakelen voor winkel** zijn ingeschakeld. Deze parameter bevindt zich op het tabblad **Commerce-parameters \> Kortingen \> Diversen**. Als de pagina **Prijsrapport** wordt geopend, wordt een dialoogvenster weergegeven met verschillende configuraties. Hieronder staan de beschikbare configuraties.

| Configuratie | Omschrijving |
|---|---|
| Vanaf datum / Tot datum| Het datumbereik waarvoor het prijsrapport moet worden gegenereerd. De duur is momenteel beperkt tot 7 dagen. |
| Kanaal| De winkel waarvoor het prijsrapport moet worden gegenereerd. |
| Producten met beschikbare voorraad weergeven| Als u dit op **Ja** instelt, worden de prijzen weergegeven voor alleen die producten die momenteel beschikbare voorraad in de winkel hebben. |
| Prijzen voor varianten weergeven | Als u dit op **Ja** instelt, worden de prijzen van varianten weergegeven met de productmodellen. Dit moet alleen op **Aan** worden gezet als u variantspecifieke prijzen hebt, omdat het aantal rijen zeer groot kan worden. In toekomstige versies schakelen we op dimensies gebaseerde prijzen in, zodat de winkelmanager de dimensies kan kiezen waarvoor de prijzen moeten worden weergegeven. |
| Producten met prijswijzigingen weergeven | Als u dit op **Ja** instelt, verschijnen de prijzen alleen voor datums waarop de prijs is gewijzigd. De prijs voor *één dag vóór* de geselecteerde **vanaf-datum** wordt altijd weergegeven, zodat de winkelmanager eenvoudig kan zien van welke producten de prijs de hele geselecteerde duur lang niet is gewijzigd en ook de huidige prijs kan weergeven. |

Nadat het rapport is gegenereerd, kunt u het Excel-bestand downloaden voor extra filtermogelijkheden. Het prijsrapport kan ook worden gebruikt om de historische prijzen te controleren van producten op datums in het verleden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]