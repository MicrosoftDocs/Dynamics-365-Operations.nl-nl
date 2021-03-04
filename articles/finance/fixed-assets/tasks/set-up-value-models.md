---
title: Waardemodellen instellen
description: In deze procedure ziet u hoe u een nieuw vaste-activaboek maakt en deze koppelt aan een vaste-activagroep.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a59bafe3099b50d34bdd9e125cfb7f43d219dcc6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442024"
---
# <a name="set-up-value-models"></a>Waardemodellen instellen

[!include [banner](../../includes/banner.md)]

In deze procedure ziet u hoe u een nieuw vaste-activaboek maakt en deze koppelt aan een vaste-activagroep. Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.


## <a name="create-a-book"></a>Een boek maken
1. Ga naar Vaste activa > Instellen > Boeken.
2. Klik op Nieuw.
3. Typ een waarde in het veld Boek.
4. Typ een waarde in het veld Omschrijving.
    * Als Afschrijving berekenen is geselecteerd, wordt het gekoppelde activumboek in afschrijvingsvoorstellen opgenomen. Als dit niet is geselecteerd, wordt het activumboek niet automatisch afgeschreven.  
5. Selecteer Ja in het veld Afschrijving berekenen.
6. Typ of selecteer een waarde in het veld Afschrijvingsprofiel.
    * Een alternatief afschrijvingsprofiel is ook bekend als overschakelingsmethode voor afschrijving. Het afschrijvingsvoorstel schakelt over op dit profiel wanneer het alternatieve profiel een afschrijvingsbedrag berekent dat groter of gelijk is als het standaardafschrijvingsprofiel.  
    * Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden. U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.  
    * Wanneer Afschrijvingscorrecties met basiscorrecties maken is geselecteerd, worden afschrijvingscorrecties automatisch gemaakt wanneer de waarde van het activum wordt bijgewerkt. Als het niet is geselecteerd, beïnvloedt de bijgewerkte activumwaarde alleen nieuwe afschrijvingsberekeningen.  
7. Selecteer in het veld Afschrijvingscorrecties met basiscorrecties maken de waarde Ja.
    * Standaard worden transacties in het vaste-activaboek naar het grootboek geboekt. U kunt het boeken naar het algemene grootboek voor het boek uitschakelen door het veld Boeken naar grootboek in te stellen op nee. De boeken die niet naar het grootboek boeken, worden doorgaans gebruikt voor belastingaangiftes. Dit geeft u meer flexibiliteit om historische transacties voor het activumboek te verwijderen, omdat ze niet in het grootboek zijn bevestigd.  
    * De Boekingslaag heeft standaard de waarde Huidige laag, als het boek in het algemene grootboek boekt, en de waarde Geen als het boek niet naar het grootboek boekt. Werk de Boekingslaag bij als u transacties voor dit boek naar een andere laag wilt boeken.  
8. Typ of selecteer een waarde in het veld Kalender.
    * Aafgeleide boeken boeken transacties naar verschillende boeken tegelijk. U maakt de transacties met het primaire boek. Tijdens het boeken wordt een exacte kopie van de transactie geboekt naar het afgeleide boek. Omdat er geen herberekening met afgeleide boektransacties is, moet deze niet voor afschrijvingstransacties moeten gebruikt.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Het boek aan een vaste-activagroep koppelen
1. Klik op Vaste-activagroepen.
2. Typ of selecteer een waarde in het veld Groep vaste activa.
3. Voer een getal in het veld Levensduur in.
    * Merk op dat de waarde in Afschrijvingsperioden wordt berekend nadat de levensduur is ingesteld.  
    * U kunt de afschrijvingsconventie instellen al naar gelang de belastingvereisten.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]