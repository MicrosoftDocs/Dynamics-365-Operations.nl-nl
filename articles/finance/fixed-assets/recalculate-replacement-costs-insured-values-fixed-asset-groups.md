---
title: Vervangingskosten en verzekerde waarden voor vaste-activagroepen herberekenen
description: In dit artikel wordt het proces toegelicht voor het bijwerken van de vervangingskosten en verzekerde waarden van vaste activa.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9dd04072b4845fe5df2a918b64ba1835ea584dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442021"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Vervangingskosten en verzekerde waarden voor vaste-activagroepen herberekenen

[!include [banner](../includes/banner.md)]

In dit artikel wordt het proces toegelicht voor het bijwerken van de vervangingskosten en verzekerde waarden van vaste activa.

Mogelijk wordt u er periodiek van op de hoogte gesteld dat de kosten om bepaalde vaste activa te vervangen of te verzekeren zijn gewijzigd. Uw manager vertelt u bijvoorbeeld dat de inflatie vorig jaar 3 procent bedroeg, zodat u de vervangingskosten voor alle vaste activa moet verhogen met 3 procent. 

Hoewel u de vervangingskosten en de verzekerde waarde voor afzonderlijke vaste activa kunt bewerken op de pagina **Vaste activa**, kunt u de pagina **Vervangingskosten en verzekerde waarden bijwerken** gebruiken om deze waarden bij te werken voor een hele groep activa tegelijk. Met deze informatie wordt beschreven hoe u waarden voor vaste-activagroepen of voor specifieke activa in de groepen bijwerkt.

## <a name="how-values-are-updated"></a>Waarden bijwerken
Als u de vervangingskosten en de verzekerde waarden voor vaste-activagroepen opnieuw wilt berekenen, moet u eerst het percentage opgeven waarmee de bestaande vervangingskosten en verzekerde waarden moeten worden gewijzigd, en moet u vervolgens de periodieke update uitvoeren om de waarden daadwerkelijk opnieuw te berekenen. U geeft het percentage op in de velden **Factor vervangingskosten** en **Factor verzekerde waarde** op de pagina **Vaste-activagroepen**. Hoewel u deze factoren opgeeft voor de vaste-activagroep, kunt u, wanneer u de pagina **Vervangingskosten en verzekerde waarden bijwerken** gebruikt, selecteren dat u de vervangingskosten en de verzekerde waarde alleen opnieuw wilt berekenen voor bepaalde vaste activa in een groep. 

Wanneer u de pagina **Vervangingskosten en verzekerde waarden bijwerken** gebruikt om de vervangingskosten en de verzekerde waarde voor de activa opnieuw te berekenen, worden de volgende formules gebruikt:

-   \[(Factor vervangingskosten van activagroep / 100) + 1\] \* Bestaande vervangingskosten van activum
-   \[(Factor verzekerde waarde van activagroep / 100) + 1\] \* Bestaande verzekerde waarde van activum

> [!NOTE] 
> Wanneer u de pagina **Vervangingskosten en verzekerde waarden bijwerken** gebruikt, worden zowel de vervangingskosten als de verzekerde waarde voor de geselecteerde activa bijgewerkt. U kunt niet opgeven dat slechts één waarde moet worden bijgewerkt. Als u één waarde wilt handhaven en de andere waarde wilt bijwerken, voert u 0 (nul) als factor op de pagina **Vaste-activagroepen** in. Als u nul invoert, wordt de berekening tijdens de update overgeslagen. De boekwaarde en de nettoboekwaarde van vaste activa worden niet beïnvloed door de periodieke update. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a>Een datum gebruiken om bij te werken artikelen te selecteren
De geselecteerde activa die op de desbetreffende dag nog niet zijn bijgewerkt maar mogelijk wel zijn bijgewerkt op voorgaande dagen, worden standaard bijgewerkt. Bijvoorbeeld: &lt; vandaag betekent 'vóór vandaag'. U kunt de datum op de pagina **Vervangingskosten en verzekerde waarden bijwerken** wijzigen door te klikken op de knop **Selecteren**. De datumcriteria die u opgeeft, worden vergeleken met de datum van de laatste periodieke update voor het activum (het veld **Laatste periodieke update waarde/kosten** op de pagina **Vaste activa)**. Elke keer dat u de vervangingskosten of de verzekerde waarde van een vast activum bijwerkt, wordt het veld **Laatste periodieke update waarde/kosten** automatisch bijgewerkt met de huidige datum. 

Voorbeeld 

U hebt de vervangingskosten voor de groepen Voertuigen, Kantoormeubilair en Gebouwen gisteren bijgewerkt met 5 procent en u vindt nu dat deze activa correct zijn bijgewerkt. Als u deze activa wilt uitsluiten wanneer u alle overige vaste activa vandaag bijwerkt, geeft u een datum op in het veld **Laatste periodieke update waarde/kosten** die vóór gisteren valt (&lt; datum van gisteren) omdat de laatste periodieke update voor de groepen **Voertuigen**, **Kantoormeubilair** en **Gebouwen** buiten de opgegeven datumcriteria viel.

## <a name="cumulative-effect-of-each-update"></a>Cumulatief effect van elke update
Elke update heeft een cumulatief effect. Plan de updates daarom zorgvuldig. Als u alle activa op dinsdag bijvoorbeeld met 3 procent verhoogt en het kantoormeubilair vervolgens met 4 procent verhoogt op vrijdag, komt de verhoging voor het kantoormeubilair in totaal uit op 7,12 procent.

## <a name="scenario"></a>Scenario
Uw manager stelt u op de hoogte van de volgende wijzigingen voor vaste activa:
-   Verhoog de vervangingskosten van alle vaste activa, behalve voor computers, met 3,25 procent.
-   Verhoog de vervangingskosten van al het kantoormeubilair met nog eens 1 procent.
-   Verlaag de vervangingskosten en de verzekerde waarde van alle computers met 10 procent.

U brengt de volgende wijzigingen aan:
1.  Typ op de pagina **Vaste-activagroepen** voor alle vaste-activagroepen behalve voor de groepen **Kantoormeubilair** en **Computers** 3,25 in het veld **Factor vervangingskosten** en 0 in het veld **Factor verzekerde waarde**.
2.  Typ voor de groep **Kantoormeubilair** 4,25 in het veld **Factor vervangingskosten** en 0 in het veld **Factor verzekerde waarde**.
3.  Typ voor de groep **Computer** -10 in het veld **Factor vervangingskosten** en -10 in het veld **Factor verzekerde waarde**.
4.  Klik op de pagina **Vervangingskosten en verzekerde waarden bijwerken** op **OK** om de herberekening voor alle vaste activa uit te voeren.

De volgende dag vertelt uw manager u dat de computers zijn verlaagd met 8 procent in plaats van 10 procent. U moet de vervangingskosten en de verzekerde waarden dus corrigeren. U kunt op twee manieren te werk gaan om de fout te herstellen:
-   Wijzig de velden **Verzekerde waarde** en **Vervangingskosten** op de pagina **Vaste activa** handmatig voor elk vast activum in de vaste-activagroep **Computers**. Bereken de waarden alsof u het oorspronkelijke bedrag had verlaagd met 8 procent, en voer deze handmatig in. Bij deze methode gebruikt u de pagina **Vervangingskosten en verzekerde waarden bijwerken** niet.
-   Voer de factor vervangingskosten en de factor verzekerde waarde voor de groep **Computers** in de velden **Factor vervangingskosten** en **Factor verzekerde waarde** op de pagina **Vaste-activagroepen** in. Zo stelt u de activa weer in op hun oorspronkelijke waarde (voorafgaand aan de verlaging met 10 procent) en past u de verlaging met 8 procent toe op de oorspronkelijke waarde. Gebruik vervolgens de pagina **Vervangingskosten en verzekerde waarden bijwerken** om de waarden opnieuw te berekenen, afhankelijk van de factoren die u hebt ingevoerd.

> [!NOTE]  
> U kunt de factor -10 niet omkeren door de positieve factor 10 (of de factor 2, het verschil tussen -10 en -8) in te voeren, omdat de bedragen niet worden berekend zoals u bedoelt. 







[!INCLUDE[footer-include](../../includes/footer-banner.md)]