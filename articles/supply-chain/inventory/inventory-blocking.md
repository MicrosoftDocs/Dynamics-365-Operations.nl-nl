---
title: Voorraadblokkering
description: Dit onderwerp geeft een overzicht van voorraadblokkering, dat deel van het kwaliteitsinspectieproces in Supply Chain Management is. U kunt voorraadblokkering gebruiken om te voorkomen dat artikelen worden verwerkt of verbruikt.
author: perlynne
manager: tfehr
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1d4b006f37904c0ae20691aaa98c75f1d5833b7
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487892"
---
# <a name="inventory-blocking"></a>Voorraadblokkering

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft een overzicht van voorraadblokkering, dat deel van het kwaliteitsinspectieproces in Supply Chain Management is. U kunt voorraadblokkering gebruiken om te voorkomen dat artikelen worden verwerkt of verbruikt.

U kunt op de volgende manieren voorraadartikelen blokkeren:

- Handmatig
- Door een kwaliteitsorder te maken
- Door een proces te gebruiken waarmee een kwaliteitsorder wordt gegenereerd
- Door blokkering van voorraadstatus te gebruiken

## <a name="blocking-items-manually"></a>Door artikelen handmatig te blokkeren

U kunt een hoeveelheid van een artikel blokkeren door een transactie te maken op de pagina **Voorraadblokkering**. Alleen artikelen die beschikbaar zijn als voorhanden voorraad kunnen handmatig worden geblokkeerd. Voor handmatig geblokkeerde hoeveelheden moet u bepalen of verwachte ontvangsten moeten worden opgenomen in planningsactiviteiten als verwachte voorhanden hoeveelheid. Verwachte ontvangsten zijn geblokkeerde artikelen waarvan u verwacht dat ze na inspectie als voorhanden voorraad beschikbaar zijn. U kunt de verwachte datum onderhouden. Standaard is de optie **Verwachte ontvangsten** ingeschakeld voor artikelen die zijn geblokkeerd door een kwaliteitsorder. U kunt een handmatige blokkering van een hoeveelheid annuleren door de transactie te verwijderen op de pagina **Voorraadblokkering**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Artikelen blokkeren door een kwaliteitsorder te maken

U kunt artikelen opgeven die moeten worden geïnspecteerd door een kwaliteitsorder te maken op de pagina **Kwaliteitsorders**. Wanneer u een kwaliteitsorder maakt, wordt de hoeveelheid die u opgeeft voor een artikel geblokkeerd. Het bemonsteringsplan dat is gekoppeld aan een kwaliteitsorder bepaalt alleen de hoeveelheid artikelen die moet worden geïnspecteerd, niet de hoeveelheid die wordt geblokkeerd. De hoeveelheid die wordt ingevoerd in de kwaliteitsorder is de geblokkeerde hoeveelheid, ongeacht de hoeveelheid die volgens het bemonsteringsplan moet worden verzonden voor inspectie.

> [!NOTE]
> Het gebruik van de batchvervaldatum en blokkering van voorraadstatusfuncties worden niet ondersteund door de hoofdplanning. Dit kan leiden tot dubbele uitsluiting van voorhanden voorraad, wat kan optreden tijdens hoofdplanning. Het is raadzaam om in plaats van de voorraad status te vertrouwen op batchbeschikkingscodes voor het blokkeren van vervallen batches.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Artikelen blokkeren via een proces waarmee een kwaliteitsorder wordt gegenereerd

Als in een kwaliteitsinspectieproces wordt opgegeven dat een artikel moet worden geïnspecteerd, wordt een hoeveelheid van het artikel automatisch geblokkeerd. Dus als een kwaliteitsorder automatisch wordt gegenereerd, bepaalt het artikelbemonsteringsplan dat is gekoppeld aan de kwaliteitsorder, zowel de hoeveelheid artikelen die wordt geblokkeerd als de hoeveelheid artikelen die moet worden geïnspecteerd. Als het selectievakje **Volledig blokkeren** op de pagina **Artikelbemonstering** is ingeschakeld, wordt de volledige hoeveelheid van, bijvoorbeeld een inkooporder, geblokkeerd tijdens de inspectie, ongeacht de hoeveelheid voor artikelbemonstering.

### <a name="example"></a>Voorbeeld

In het volgende voorbeeld wordt een kwaliteitsorder gegenereerd wanneer de pakbon van een inkooporder wordt geboekt. Op de pagina **Kwaliteitskoppelingen** hebt u opgegeven dat het boeken van een pakbon voor een inkooporder het proces is waarmee een kwaliteitsorder wordt geactiveerd.

|Instellingen |Gebruikersactie |Resultaat |
|----|---|---|
| Met een kwaliteitskoppeling wordt opgegeven dat bij het boeken van een pakbon voor een inkooporder een kwaliteitsorder moet worden gegenereerd. Met het artikelbemonsteringsplan van de kwaliteitsorder wordt bepaald dat 10 procent van de hoeveelheid op de inkooporderregel moet worden geïnspecteerd. Verder moet, omdat het selectievakje **Volledige blokkering** is ingeschakeld in de instellingen voor de artikelbemonstering, de volledige hoeveelheid van de inkooporderregel worden geblokkeerd tijdens de inspectie, ongeacht de hoeveelheid die wordt verzonden voor inspectie. | De pakbon wordt geboekt. | Een kwaliteitsorder wordt gegenereerd. Tien procent van de inkooporderhoeveelheid voor het artikel wordt naar inspectie verzonden. De volledige hoeveelheid van de inkooporderregel wordt geblokkeerd. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Artikelen blokkeren via blokkering van voorraadstatus

U kunt opgeven welke voorraadstatussen blokkeringsstatussen zijn door de parameter **Voorraadblokkering** op de pagina **Voorraadstatussen** te gebruiken . U kunt geen voorraadstatussen als blokkeringsstatus gebruiken voor productieorders, verkooporders, transferorders, uitgaande transacties of projectintegraties. Gebruik voor uitgaand werk artikelen met een beschikbare voorraadstatus. Als artikelen de status **Verbroken** hebben en de hoofdplanning op deze artikelen wordt uitgevoerd, worden de artikelen als ontbrekend beschouwd en wordt de voorraad automatisch aangevuld.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Let op wanneer u artikelen blokkeert waarvoor zowel blokkering van voorraadstatus als blokkering van kwaliteitsorder wordt gebruikt

U kunt een kwaliteitsorder maken die is gekoppeld aan voorraad met een voorraadstatus waarvoor de bijbehorende parameter **Voorraadblokkering** is ingeschakeld. In dit geval wordt door de kwaliteitsorder een extra record voor voorraadblokkering gegenereerd naast de record die is gemaakt door de voorraadstatus. Omdat de parameter **Verwachte ontvangsten** zijn ingeschakeld voor de voorraadblokkering van de kwaliteitsorder, wordt er een extra transactie *Bestelde voorraad* gegenereerd die ook wordt geblokkeerd door de bijbehorende voorraadstatus. Deze combinatie kan ertoe leiden dat er steeds minder inzicht is in de betekenis van gegenereerde voorraadtransacties, omdat het erop lijkt dat de totale geblokkeerde hoeveelheid meer is dan de totale hoeveelheid in voorraad. Laten we de transacties eens bekijken van een voorbeeld van een ontvangst van 10 stuks van artikel A0001 met een kwaliteitsorder die is gegenereerd om van één stuk een monsteren te nemen. Het gedrag is ook afhankelijk van de vraag of de optie **Bestelde artikelen reserveren** is ingeschakeld op de pagina **Parameters voor voorraad- en magazijnbeheer**.

>[!NOTE]
>Als u blokkering van voorraadstatus en kwaliteitsorders samen gebruikt, raden we u sterk aan de optie **Bestelde artikelen reserveren** in te stellen.

### <a name="example-with-reserve-ordered-items-enabled"></a>Voorbeeld met Bestelde artikelen reserveren ingeschakeld

Wanneer **Bestelde artikelen reserveren** is ingeschakeld, hebben alle transacties voor voorraadblokkering de status *Fysiek gereserveerd* of *Besteld en gereserveerd*.

| Verwijzing naar voorraadtransactie | Ontvangst | Uitgeven | Hoeveelheid | Locatie | Magazijn | Voorraadstatus | Locatie | Nummerplaat | Opmerking |
|---|---|---|---|---|---|---|---|---|---|
| Inkooporder | Ingekocht | | 10 st. | 2 | 24 | Blokkering | RECV | receiptLp1 | | 
| Voorraadblokkering | | Fysiek gereserveerd | -9 st. | 2 | 24 | Blokkering | | | Transactie die is gegenereerd door de blokkering van de voorraadstatus |
| Voorraadblokkering | | Fysiek gereserveerd | -1 st. | 2 | 24 | Blokkering | RECV | receiptLp1 | Transactie die is gegenereerd door de bemonsteringsblokkering voor kwaliteitsorders |
| Voorraadblokkering | Besteld | | 1 st. | 2 | 24 | Blokkering | RECV | receiptLp1 | Verwachte ontvangsten van de bemonsteringsblokkering voor de kwaliteitsorder |
| Voorraadblokkering | | Besteld en gereserveerd | 1 st. | 2 | 24 | Blokkering | | | Transactie die is gegenereerd door de blokkering van de voorraadstatus

### <a name="example-with-reserve-ordered-items-disabled"></a>Voorbeeld met Bestelde artikelen reserveren uitgeschakeld

Wanneer **Bestelde artikelen reserveren** is uitgeschakeld, kunnen de verwachte ontvangsten niet worden gereserveerd omdat ze de status *Besteld* hebben, zodat bepaalde blokkeringen de status *In bestelling* blijven behouden.

| Verwijzing naar voorraadtransactie | Ontvangst | Uitgeven | Hoeveelheid | Locatie | Magazijn | Voorraadstatus | Locatie | Nummerplaat | Opmerking |
|---|---|---|---|---|---|---|---|---|---|
| Inkooporder | Ingekocht | | 10 st. | 2 | 24 | Blokkering | RECV | receiptLp1 | |
| Voorraadblokkering | | Fysiek gereserveerd | -9 st. | 2 | 24 | Blokkering | | | Transactie die is gegenereerd door de blokkering van de voorraadstatus |
| Voorraadblokkering | | Fysiek gereserveerd | -1 st. | 2 | 24 | Blokkering | RECV | receiptLp1 | Transactie die is gegenereerd door de bemonsteringsblokkering voor kwaliteitsorders |
| Voorraadblokkering | Besteld | | 1 st. | 2 | 24 | Blokkering | RECV | receiptLp1 | Verwachte ontvangsten van de bemonsteringsblokkering voor de kwaliteitsorder |
| Voorraadblokkering | | In bestelling | 1 st. | 2 | 24 | Blokkering | RECV | receiptLp1 | Transactie die is gegenereerd door de blokkering van de voorraadstatus

Let op het verschil in transactiestatus en dimensies tussen de twee cases. We raden u daarom aan de optie **Bestelde artikelen reserveren** in te schakelen.

<!-- KFM: (Enable this section when the feature leaves private preview)

### Disable expected receipts from quality orders that sample blocked inventory feature

To simplify the inventory transactions in the case of quality orders that sample inventory blocked as a consequence of inventory status, the system provides a feature that disables expected receipts from such quality orders. As the expected receipt is in any case immediately blocked by inventory status blocking, there is no reduction of on-hand inventory because of this change.

-->

## <a name="additional-resources"></a>Aanvullende bronnen

[Voorraadblokkering maken en beheren](tasks/create-maintain-inventory-blocking.md)

[Processen voor kwaliteitsbeheer](quality-management-processes.md)

[Inspecteer de kwaliteit van goederen](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]