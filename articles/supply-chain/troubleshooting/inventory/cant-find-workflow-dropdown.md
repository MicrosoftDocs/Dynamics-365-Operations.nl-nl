---
title: U kunt het dialoogvenster met vervolgkeuzelijst 'Werkstroom' niet vinden voor voorraadjournalen
description: U kunt het dialoogvenster met vervolgkeuzelijst 'Werkstroom' niet vinden op de journaalpagina of er zijn geen gerelateerde werkstroombewerkingen beschikbaar
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475994"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>U kunt het dialoogvenster met vervolgkeuzelijst 'Werkstroom' niet vinden voor voorraadjournalen

## <a name="symptoms"></a>Symptomen

U kunt het vervolgkeuzedialoogvenster **Werkstroom** niet vinden op de journaalpagina of er zijn geen gerelateerde werkstroombewerkingen beschikbaar.

Dit probleem kan om drie redenen optreden, zoals wordt beschreven in de volgende gedeelten.

## <a name="resolution-1"></a>Oplossing 1

Als het probleem voor alle gebruikers geldt, kan het komen doordat de goedkeuringswerkstroom niet aan de journaalnaam is toegewezen. Volg deze stappen om het probleem op te lossen.

1. Ga naar **Voorraadbeheer &gt; Instellingen &gt; Journaalnamen &gt; Voorraad**.
1. Selecteer een journaalnaam in het lijstdeelvenster om de bijbehorende instellingen te openen.
1. Stel op het sneltabblad **Algemeen** de optie **Goedkeuringswerkstroom** in op *Ja*. Selecteer **Ja** als u wordt gevraagd de wijziging te bevestigen.
1. Selecteer in het veld **Werkstroom** de werkstroom die u voor de geselecteerde journaalnaam wilt gebruiken.

## <a name="resolution-2"></a>Oplossing 2

Als in uw werkstroom aangepaste code wordt gebruikt, kunnen problemen optreden nadat u een upgrade op het systeem hebt uitgevoerd. In de journaalwerkstroom is het bijvoorbeeld mogelijk dat de knop **Indienen** grijs wordt weergegeven, zodat u deze niet kunt selecteren om een indiening goed te keuren.

Als de knop **Indienen** grijs wordt weergegeven, is uw werkstroom mogelijk aangepast. Dit houdt in dat de methode van de werkstroom, `canSubmitToWorkflow()` in `FormDataUtil` is uitgebreid. Om dit probleem op te lossen, wijzigt u de manier waarop u de methode van `canSubmitToWorkflow()` uitbreidt om de structuur in het volgende voorbeeld te gebruiken.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Oplossing 3

Als het probleem alleen voor een paar specifieke gebruikers geldt, beschikken deze gebruikers mogelijk niet over de beveiligingsbevoegdheden die zijn vereist om werkstroombewerkingen uit te voeren op voorraadjournalen. Controleer of elke betrokken gebruiker beschikt over de beveiligingsbevoegdheid *Werkstroom voorraadjournaal onderhouden*. Standaard wordt deze bevoegdheid toegewezen aan een taak met dezelfde naam en die taak wordt toegepast op de rollen *Magazijnmedewerker* en *Magazijnbeheerder*.
