---
title: Journaalboeking mislukt door onevenwichtigheid
description: In dit onderwerp wordt uitgelegd waarom debet- en credittransacties mogelijk niet in evenwicht zijn in boekstuktransacties, waardoor de transacties niet kunnen worden geboekt. Het onderwerp bevat ook stappen voor het oplossen van het probleem.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fc413f8230849653aef8c2951f1749823edded6e
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605424"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Journaalboeking mislukt door onevenwichtigheid

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd waarom debet- en credittransacties mogelijk niet in evenwicht zijn in boekstuktransacties, waardoor de transacties niet kunnen worden geboekt. Het onderwerp bevat ook stappen voor het oplossen van het probleem.

## <a name="symptom"></a>Symptoom

In sommige gevallen kan een journaal niet worden geboekt en wordt het volgende bericht weergegeven: 'De transacties op een specifieke bon zijn niet in evenwicht vanaf een bepaalde datum (valuta voor boekhouding: 0,01 - aangiftevaluta: 0,06)'. Waarom kan het journaal niet worden geboekt?

## <a name="resolution"></a>Oplossing

Tijdens het boeken naar het grootboek moet elk boekstuk in evenwicht zijn in de transactievaluta, de valuta voor de boekhouding en de aangiftevaluta als deze valuta's zijn gedefinieerd op de pagina **Grootboek instellen**. (Boekstukken zijn in evenwicht wanneer het totaal aan debet gelijk is aan het totaal aan credit.)

Onderaan de pagina met journaalregels worden totalen getoond in de valuta voor boekhouding en de aangiftevaluta. Deze worden **niet** getoond in de transactievaluta voor transacties in vreemde valuta. In het foutbericht dat gebruikers tijdens de simulatie of boeking ontvangen, worden bovendien alleen de verschillen in de valuta voor boekhouding en de aangiftevaluta getoond. Deze worden niet in de transactievaluta getoond, omdat een enkel boekstuk meer dan één transactievaluta kan hebben, en het journaal boekstukken in verschillende transactievaluta's kan bevatten. Het is daarom belangrijk dat u handmatig controleert of de transactievalutabedragen voor elk boekstuk met slechts één transactievaluta in evenwicht zijn.

### <a name="transaction-currency"></a>Transactievaluta

Tijdens de simulatie en de boeking controleert het systeem of elk boekstuk met slechts één transactievaluta in evenwicht is in de transactievaluta. Voor elk boekstuk dat wordt ingevoerd, kan er een of meer valuta's voor de transactievaluta zijn. Een boekstuk dat in het algemene journaal wordt ingevoerd, kan bijvoorbeeld twee transactievaluta's hebben wanneer contant geld wordt overgeboekt van een bankrekening waarin euro's (EUR) worden gebruikt naar een bankrekening waarin Canadese dollars (CAD) worden gebruikt.

Als een boekstuk slechts één transactievaluta heeft, moeten de totale debets gelijk zijn aan de totale credit in de transactievaluta voor dat boekstuk. Klanten hebben de volgende scenario's meegemaakt waarbij de boeking op de juiste manier is mislukt, omdat de bedragen in transactievaluta niet in evenwicht waren:

- De totale debet en totale credit zijn **niet** in evenwicht in de transactievaluta, maar ze waren wel in evenwicht voor de valuta voor boekhouding en aangiftevaluta. Een klant was ervan uitgegaan dat het boekstuk nog wel zou worden geboekt. Deze veronderstelling was echter onjuist. **De bedragen in transactievaluta op een boekstuk moeten altijd in evenwicht zijn wanneer alle regels van het boekstuk dezelfde transactievaluta hebben.**
- Het boekstuk is geïmporteerd met een gegevensentiteit via Data Management Framework (DMF) en de gebruiker heeft gedacht dat de bedragen in de transactievaluta in evenwicht waren. In het importbestand hebben sommige bedragen meer dan twee decimalen en zijn er meer dan twee decimalen opgenomen bij het importeren van de bedragen. Dat betekent dat de debets niet gelijk zijn aan de crediteringen, omdat deze een fractie van een cent afweken. Dit verschil wordt niet weergegeven in de regels van het boekstuk, omdat de weergegeven bedragen slechts twee decimalen hebben.
- Het boekstuk is geïmporteerd met een gegevensentiteit via DMF en de gebruiker heeft gedacht dat de bedragen in de transactievaluta in evenwicht waren. Hoewel het **boekstuk** in evenwicht was, hebben sommige regels van het boekstuk verschillende transactiedatums. Als u de totale debet en de totale credit in de transactievaluta per **boekstuk en transactiedatum** hebt toegevoegd, waren deze niet in evenwicht. Deze vereiste wordt afgedwongen wanneer u een boekstuk via het algemene journaal in het systeem invoert. Het wordt echter niet afgedwongen wanneer een boekstuk met een gegevensentiteit wordt geïmporteerd via DMF.

In een ondersteund scenario kan een boekstuk meerdere transactievaluta's hebben. In dit geval controleert het systeem **niet** of de debets gelijk zijn aan de credits in de transactievaluta, omdat de valuta niet overeenkomen. In plaats daarvan controleert het systeem of de bedragen in de valuta voor boekhouding en aangiftevaluta in evenwicht zijn.

### <a name="accounting-currency"></a>Valuta voor boekhouding

Als alle regels van een boekstuk dezelfde transactievaluta hebben en de bedragen voor transactievaluta in evenwicht zijn, controleert het systeem of de bedragen in de valuta voor boekhouding in evenwicht zijn. Als het boekstuk is ingevoerd in een vreemde valuta, wordt de wisselkoers op de boekstukregels gebruikt om de bedragen van de transactievaluta om te rekenen naar de valuta voor boekhouding. Eerst wordt elke regel van het boekstuk omgerekend en afgerond op twee decimalen. Vervolgens worden de regels opgeteld om de totale debet- en creditbedragen te bepalen. Aangezien elke regel wordt omgerekend, zijn de totale debet en totale credit mogelijk niet in evenwicht. Als de absolute waarde van het verschil echter binnen de waarde voor **Maximaal afrondingsverschil** valt die is gedefinieerd op de pagina **Grootboekparameters**, wordt het boekstuk geboekt en wordt het verschil automatisch geboekt naar de rekening voor afrondingsverschillen.

Als het boekstuk meerdere transactievaluta heeft, wordt elke regel van het boekstuk omgerekend naar de valuta voor boekhouding en afgerond op twee decimalen. Vervolgens worden de regels opgeteld om de totale debet- en totale creditbedragen te bepalen. Om als in evenwicht te worden beschouwd, moeten de debet- en creditrekeningen in evenwicht zijn, omgerekend of als het afrondingsverschil in de boekhoudingsvaluta wordt opgenomen.

### <a name="reporting-currency"></a>Aangiftevaluta

Als alle regels van een boekstuk dezelfde transactievaluta hebben en de bedragen voor transactievaluta in evenwicht zijn, controleert het systeem of de bedragen in de aangiftevaluta in evenwicht zijn. Als het boekstuk is ingevoerd in een vreemde valuta, wordt de wisselkoers op de boekstukregels gebruikt om de bedragen van de transactievaluta om te rekenen naar de aangiftevaluta. Eerst wordt elke regel van het boekstuk omgerekend en afgerond op twee decimalen. Vervolgens worden de regels opgeteld om de totale debet- en creditbedragen te bepalen. Aangezien elke regel wordt omgerekend, zijn de totale debet en totale credit mogelijk niet in evenwicht. Als het verschil niettemin binnen de waarde voor **Maximaal afrondingsverschil in aangiftevaluta** valt die is gedefinieerd op de pagina **Grootboekparameters**, wordt het boekstuk geboekt en wordt het verschil automatisch geboekt naar de rekening voor afrondingsverschillen.

Als het boekstuk meerdere transactievaluta heeft, wordt elke regel van het boekstuk omgerekend naar de aangiftevaluta en afgerond op twee decimalen. Vervolgens worden de regels opgeteld om de totale debet- en totale creditbedragen te bepalen. Om als in evenwicht te worden beschouwd, moeten de debet- en creditrekeningen in evenwicht zijn, omgerekend of als het afrondingsverschil in de aangiftevaluta wordt opgenomen.

### <a name="example-for-an-accounting-currency-imbalance"></a>Voorbeeld voor een onevenwicht in een boekhoudingsvaluta

> [!NOTE]
> Het bedrag van de aangiftevaluta wordt op dezelfde manier berekend als het bedrag in de transactievaluta.

Wisselkoers: 1,5

| Regel | Boekstuk | Rekening | Valuta | Debet (transactie) | Credit (transactie) | Debet (boekhouding) | Credit (boekhouding) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10.00 | | 15.00 |
| **Totaal** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

De boekhoudingsvaluta heeft een onevenwicht van 0,01. Als de maximale afronding in de valuta voor de boekhouding echter ten minste 0,01 is, wordt het verschil automatisch geboekt naar de rekening voor afrondingsverschillen en wordt het boekstuk geboekt.
