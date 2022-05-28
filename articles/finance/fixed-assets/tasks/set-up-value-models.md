---
title: Waardemodellen instellen
description: In deze procedure ziet u hoe u een nieuw vaste-activaboek maakt en deze koppelt aan een vaste-activagroep.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71d256b600956a4e525cde626c958713f6258f5a
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727056"
---
# <a name="set-up-value-models"></a>Waardemodellen instellen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

In deze procedure ziet u hoe u een nieuw vaste-activaboek maakt en deze koppelt aan een vaste-activagroep.

## <a name="create-a-book"></a>Een boek maken
1. Ga naar **Vaste activa \> Instellen \> Boeken**.
2. Selecteer **Nieuw**.
3. Voer een waarde in het veld **Boeken** in.
4. Voer een waarde in het veld **Beschrijving** in.
5. Stel de optie **Afschrijving berekenen** in op **Ja**.

    Als de optie **Afschrijving berekenen** is ingesteld op **Ja**, dus wordt het gekoppelde activumboek in afschrijvingsvoorstellen opgenomen. Als dit is ingesteld op **Nee**, wordt het activumboek niet automatisch afgeschreven.

6. Typ of selecteer een waarde in het veld **Afschrijvingsprofiel**.

    * Een alternatief afschrijvingsprofiel is ook bekend als overschakelingsmethode voor afschrijving. Het afschrijvingsvoorstel schakelt over op dit profiel wanneer het alternatieve profiel een afschrijvingsbedrag berekent dat groter of gelijk is als het standaardafschrijvingsprofiel.
    * Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden. U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.
    * Wanneer u **Afschrijvingscorrecties met basiscorrecties maken** selecteert, worden afschrijvingscorrecties automatisch gemaakt wanneer de waarde van het activum wordt bijgewerkt. Anders heeft de bijgewerkte activawaarde alleen invloed op toekomstige afschrijvingsberekeningen.

7. Stel de optie **Afschrijvingscorrecties met basiscorrecties maken** in op **Ja**.

    * Standaard worden transacties in het vaste-activaboek naar het grootboek geboekt. U kunt het boeken naar het algemene grootboek voor het boek echter ook uitschakelen door de optie **Boeken naar grootboek** in te stellen op **Nee**. Boeken die niet naar het grootboek worden geboekt, worden gewoonlijk gebruikt voor belastingaangiftes. Deze optie geeft u meer flexibiliteit om historische transacties voor het activumboek te verwijderen, omdat de transacties niet in het grootboek zijn bevestigd.
    * Standaard is het veld **Boekingslaag** ingesteld op de **huidige laag** als het boek wordt geboekt naar het grootboek en op de waarde **Geen** als het boek niet naar het grootboek wordt geboekt. Werk de waarde van het veld **Boekingslaag** bij als transacties voor dit boek naar een andere laag moeten worden geboekt.

8. Positieve afschrijving berekenen.

    * De optie **Positieve afschrijving berekenen** is standaard ingesteld op **Nee**. Deze instelling geeft aan dat de afschrijving naar het geselecteerde activaboek wordt gecrediteerd. Bovendien zijn de opties **Nettoboekwaarde hoger dan aanschafprijs toestaan** en **Negatieve nettoboekwaarde toestaan** beide ingesteld op **Nee** en kunnen de instellingen onafhankelijk worden gewijzigd. 
    * Stel **Positieve afschrijving berekenen** in op **Ja** om de positieve afwijking te berekenen. Deze instelling geeft aan dat de afschrijving van het vaste-activaboek wordt afgeschreven. Als de optie **Positieve afschrijving berekenen** is ingesteld op **Ja**, worden de opties **Nettoboekwaarde hoger dan aanschafprijs toestaan** en **Negatieve nettoboekwaarde toestaan** automatisch ingesteld op **Ja** en worden deze vergrendeld. Deze vergrendeling zorgt ervoor dat positieve afschrijving alleen wordt toegepast op vaste activa die zijn verworven met een negatieve boekwaarde (credit). 

10. Typ of selecteer een waarde in het veld **Kalender**.

    Aafgeleide boeken boeken transacties naar verschillende boeken tegelijk. U maakt de transacties met het primaire boek. Tijdens het boeken wordt een exacte kopie van de transactie geboekt naar het afgeleide boek. Omdat er geen herberekening met afgeleide boektransacties is, moet deze niet voor afschrijvingstransacties moeten gebruikt.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Het boek aan een vaste-activagroep koppelen

1. Selecteer **Groepen vaste activa**.
2. Typ of selecteer een waarde in het veld **Groep vaste activa**.
3. Voer een getal in het veld **Levensduur** in.

    * Afschrijvingsperioden worden berekend, nadat de levensduur van het activum is ingevoerd.
    * De afschrijvingsconventie kan al naar gelang de belastingvereisten ingesteld worden.
    * Voor vaste activa die aan leases zijn gekoppeld, wordt de waarde van het veld **Levensduur** overschreven door een lagere leasetermijn dan de leasetermijn in het activaboek en de levensduur van het activum. Als de optie **Eigendomsoverdracht** is ingesteld op **Ja** voor het leaseboek, is de waarde van het veld **Levensduur** altijd de economische levensduur van het activum.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
