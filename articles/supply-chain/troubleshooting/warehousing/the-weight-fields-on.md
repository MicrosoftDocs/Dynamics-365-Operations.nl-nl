---
title: De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading
description: De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924346"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading

Foutcodes: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading %1. Voer de Consistentiecontrole capaciteit magazijn uit om de gewichtsvelden opnieuw te berekenen.

## <a name="cause"></a>Oorzaak

De velden **Nettogewicht** en **Tarragewicht** worden op de ladingregel ingesteld op *0* (nul). De gewichtsvelden zijn echter niet ingesteld op *0* voor de gewichtsmaten op het product. Wanneer er geen gewichtsvelden op de ladingregel zijn ingesteld, kunnen correcties van de hoeveelheid op de ladingregel leiden tot een onjuiste gewichtsberekening van de lading. Dit probleem kan optreden als het gewicht van het product is gewijzigd nadat de ladingregel werd gemaakt.

## <a name="resolution"></a>Oplossing

Wanneer u een ladingregel maakt, worden de gewichtsvelden van het product standaard ingevuld. Als het gewicht nul is, kunt u deze opnieuw berekenen met behulp van de functionaliteit *Consistentiecontrole capaciteit magazijn*.

1. Ga naar **Systeembeheer \> Periodieke taken \> Database \> Consistentiecontrole**.
1. In het dialoogvenser **Consistentiecontrole**, stelt u het veld **Module** in op *Magazijnbeheer*.
1. Stel het veld **Controleren/corrigeren** in op *Fout oplossen*.
1. Schakel in de lijst met selectievakjes het selectievakje **Consistentiecontrole capaciteit magazijn** in en zorg ervoor dat alleen de rij voor dit selectievakje is gemarkeerd.
1. Selecteer de knop met het weglatingsteken (**...**) boven aan de lijst met selectievakjes en selecteer vervolgens **Dialoog** in het menu.
1. In het dialoogvenster **Consistentiecontrole capaciteit magazijn** stelt u de volgende velden in om de criteria van de consistentiecontrole op te geven:

    - **Lading-id:** Geef een lading-id op. Laat dit leeg als u alle lading-id's wilt controleren.
    - **Artikelnummer:** Geef een artikelnummer op. Laat dit leeg als u alle artikelen wilt controleren.
    - **Altijd opnieuw berekenen van gewicht voor ladingen:** Zet deze optie op *Ja*.
    - **Overschrijven van gewicht op ladingregels toestaan:** Zet deze optie op *Ja*.

1. Selecteer **OK** om het dialoogvenster **Consistentiecontrole capaciteit magazijn** te sluiten.
1. Selecteer de knop met het weglatingsteken en selecteer vervolgens **Uitvoeren** in het menu.

Het gewicht wordt opnieuw berekend op basis van de criteria die u hebt opgegeven. Selecteer de koppeling **Berichtdetails** als u het resultaat van de consistentiecontrole wilt bekijken.
