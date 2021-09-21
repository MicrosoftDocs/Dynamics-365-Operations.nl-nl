---
title: Gemengde voorraadtypen bij gebruik van profiel dockbeheer
description: Er moet eerst een werkkoptekstopsplitsing worden ingesteld om het mengen van voorraad op een effectieve manier te beheren via een dockbeheerprofiel. Op deze pagina wordt uitgelegd hoe u dit doet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475996"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Voorraadtypen worden gemengd bij gebruik van een profiel dockbeheer

## <a name="symptoms"></a>Symptomen

U maakt gebruik van *beleidsregels voor samenvoegen van zendingen*. U hebt een *Profiel dockbeheer* ingesteld voor een *locatieprofiel*, maar wanneer er werk wordt aangemaakt, worden de voorraadtypen gemengd op de laatste locatie.

## <a name="resolution"></a>Oplossing

Voor dockbeheerprofielen moet werk vooraf worden opgesplitst. Met andere woorden, het dockbeheerprofiel verwacht dat een werkkoptekst niet meerdere wegzetlocaties bevat.

Er moet een werkkoptekstopsplitsing worden ingesteld om het mengen van voorraad op een effectieve manier te beheren via het dockbeheerprofiel.

In dit voorbeeld is ons profiel dockbeheer zo geconfigureerd dat **Voorraadtypen die niet mogen worden gemengd** wordt ingesteld op *Zending-ID*. Hiervoor stellen we een werkkoptekstopsplitsing in:

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Selecteer het **Werkordertype** dat u wilt bewerken (bijvoorbeeld *Inkooporders*).
1. Selecteer de werksjabloon die u wilt bewerken.
1. Selecteer **Query bewerken** in het actievenster.
1. Open het tabblad **Sorteren** en voeg een rij toe met de volgende instellingen:
    - **Tabel** - *Tijdelijke werktransacties*
    - **Afgeleide tabel** - *Tijdelijke werktransacties*
    - **Veld** - *Zending-id*
1. Selecteer **OK**.
1. U keert terug naar de pagina **Werksjablonen**. Selecteer **Opsplitsingen voor werkkoptekst** in het actievenster.
1. Selecteer **Bewerken** in het actievenster.
1. Schakel het selectievakje in dat is gekoppeld aan de **veldnaam** *Zending-id*.
1. Selecteer **Opslaan** in het actievenster.
