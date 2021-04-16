---
title: Enkel boekstuk met meerdere klant- of leveranciersrecords
description: Dit onderwerp geeft een overzicht van wat er gebeurt wanneer u één enkel boekstuk boekt met meerdere klant- of leverancierrecords. Deze functionaliteit gaat verdwijnen in toekomstige versies van Microsoft Dynamics 365 Finance. Het wordt daarom afgeraden om deze boekingsmethode te gebruiken, vanwege het boekhoudingseffect op de verwerking van vereffeningen.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4e12eb3162d00c76254582c0621c9dd567df562
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837292"
---
# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Enkel boekstuk met meerdere klant- of leveranciersrecords

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft een overzicht van wat er gebeurt wanneer u één enkel boekstuk boekt met meerdere klant- of leverancierrecords. Deze functionaliteit gaat verdwijnen in toekomstige versies. Het wordt daarom afgeraden om deze boekingsmethode te gebruiken, vanwege het boekhoudingseffect op de verwerking van vereffeningen. 

Enkele veelvoorkomende gevallen waarin een enkel boekstuk wordt gebruikt voor meerdere klanten of leveranciers zijn saldo-overboekingen tussen klanten en verrekening van saldi tussen klanten en leveranciers binnen dezelfde organisatie. 

Een boekstuk met meer dan één klant of leverancier kan worden ingevoerd met een van de volgende methoden:

-   Met een journaal waarvoor de optie **Maximaal één boekstuknummer** is geselecteerd, zodat elke regel die aan het journaal wordt toegevoegd op hetzelfde boekstuk wordt opgenomen.
-   Met een meerregelig boekstuk, waarbij geen tegenrekening in het grootboek bestaat, met meer dan één klant of leverancier.
-   Door een boekstuk in te voeren waarvan de rekening en de tegenrekening leverancier/leverancier, klant/klant, leverancier/klant, leverancier/klant zijn.

In dit onderwerp wordt getoond hoe de vereffening wordt verwerkt wanneer een boekstuk met meerdere klant- of leverancierrecords wordt geboekt. Daarnaast reikt dit onderwerp workarounds aan die u helpen te begrijpen hoe u het gebruik van één boekstuk met meerdere klanten of leveranciers kunt vermijden. In het bijzonder zijn er voorbeelden die twee veel voorkomende vereffeningscenario's illustreren, die last hebben van het gebruik van een boekstuk met meerdere klanten of leveranciers:

-   Boekhouding met contantkortingen
-   Boekhouden met herwaarderingen

## <a name="how-does-settlement-impact-single-voucher-usage"></a>De invloed van vereffening op gebruik van enkele boekstukken
Wanneer u een boekstuk boekt dat meerdere klant- of leverancierrecords bevat, wordt één boekhoudingsboekstuk gemaakt dat meerdere saldi van klanten en/of leveranciers bevat. Tijdens het vereffeningsproces worden de oorspronkelijke boekhoudvermeldingen gebruikt om boekhoudvermeldingen te maken voor de contantkorting, niet-gerealiseerde winsten en verliezen, gerealiseerde winsten en verliezen, en de ontlasting van de overzichtrekening van het oorspronkelijke document. Stel dat een contantkorting wordt gebruikt wanneer een betaling wordt verrekend met een factuur. De contantkortingsboekhouding moet dan naar de leveranciersgrootboekrekening van de oorspronkelijke factuur boeken. Als de oorspronkelijke factuur werd geboekt in een boekstuk met meerdere leverancierrecords, wordt de oorspronkelijke boekhouding samengevat. Omdat er in dit geval geen manier is om de gedetailleerde boekhoudvermelding voor elke leverancierstransactie in het enkele boekstuk te lezen, kan niet worden bepaald op welke manier de gebruiker de contantkorting wilde verklaren.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Eén boekstuk met meerdere leveranciers en het effect op de contantkortingsboekhouding

In het volgende voorbeeld zijn meerdere leveranciersfacturen geregistreerd in het grootboek op één boekstuk op de pagina **Algemeen journaal**. Deze facturen zijn verdeeld over meerdere rekeningdimensies.

| Boekstuk | Rekeningtype | Rekening  | Beschrijving | Debet | Krediet |
|-------------|------------------|--------------|-----------------|-----------|------------|
| GNJL001     | Leverancier           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Leverancier           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Leverancier           | 1001         | INV3            |           | 300,00     |
| GNJL001     | Grootboek           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Grootboek           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Grootboek           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Grootboek           | 606300-004-- | INV3            | 300,00    |            |

Na het boeken wordt één boekstuk gemaakt.

| Boekstuk | Rekening  | Boekingstype | Bedrag in transactievaluta |
|-------------|--------------|------------------|------------------------------------|
| GNJL001     | 606300-001-- | Grootboekjournaal   | 50,00                              |
| GNJL001     | 606300-002-- | Grootboekjournaal   | 50,00                              |
| GNJL001     | 606300-003-- | Grootboekjournaal   | 200,00                             |
| GNJL001     | 606300-004-- | Grootboekjournaal   | 300,00                             |
| GNJL001     | 200110-001-  | Leveranciersaldo   | -100,00                            |
| GNJL001     | 200110-001-  | Leveranciersaldo   | -200,00                            |
| GNJL001     | 200110-001-  | Leveranciersaldo   | -300,00                            |

Merk op dat hier drie vermeldingen voorkomen voor het boekingstype Leverancierssaldo in één boekstuk. Er is geen manier om aan te geven dat het debetbedrag van 50,00 voor 606300-001 en debetbedrag 50,00 voor 606300-002 bedoeld zijn om de vermelding van het leverancierssaldo van 200110-001 te verrekenen. Dit komt doordat de gebruiker meerdere leverancierrecords in één boekstuk heeft ingevoerd.

Met dit voorbeeld kunnen we het effect analyseren dat een enkel boekstuk heeft op de vereffeningboekhouding later in het proces. Stel dat u van de factuur van 200,00 een bedrag van 197,00 betaalt en een contantkorting van 3,00 neemt. Merk op dat de waarde van de contantkortingsrekening over alle dimensies van kostenrekeningen van het factuurboekstuk is toegewezen. Dit komt doordat één boekstuk werd gebruikt om de bovenstaande factuur te boeken, zonder aan te geven hoe de gebruiker de kostenverdelingen wilde laten correleren met het leverancierssaldo in het enkele boekstuk.

| Boekstuk | Rekening  | Boekingstype     | Debet | Krediet |
|-------------|--------------|----------------------|-----------|------------|
| APPAYM001   | 200110-001-  | Leveranciersaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bank                 |           | 197.00     |
| 14000056    | 520200-001-- | Contantkorting van leverancier |           | 0.25       |
| 14000056    | 520200-002-- | Contantkorting van leverancier |           | 0.25       |
| 14000056    | 520200-003-- | Contantkorting van leverancier |           | 1,00       |
| 14000056    | 520200-004-- | Contantkorting van leverancier |           | 1.50       |
| 14000056    | 200110-001-  | Leveranciersaldo       | 3,00      |            |

Als de gebruiker niet wil dat de contantkorting wordt toegewezen over de volledige uitgavenverdeling van de oorspronkelijke factuur, in plaats van één boekstuk, moeten meerdere boekstukken worden gebruikt om de facturen te registreren. In het volgende voorbeeld ziet u hoe meerdere boekstukken kunnen worden ingevoerd in het grootboek, in plaats een enkel boekstuk te gebruiken zoals aan het begin van dit voorbeeld wordt getoond.

| Boekstuk | Rekeningtype | Rekening  | Beschrijving | Debet | Krediet | Type tegenrekening | Tegenrekening |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| GNJL001     | Leverancier           | 1001         | INV1            |           | 100,00     | Grootboek          | &lt;leeg&gt;      |
| GNJL001     | Grootboek           | 606300-001-- | INV1            |   50,00   |            | Grootboek          | &lt;leeg&gt;      |
| GNJL001     | Grootboek           | 606300-002-- | INV1            |   50,00   |            | Grootboek          | &lt;leeg&gt;      |
| GNJL002     | Leverancier           | 1001         | INV2            |           | 200,00     | Grootboek          | 606300-003--       |
| GNJL003     | Leverancier           | 1001         | INV3            |           | 300,00     | Grootboek          | 606300-004--       |

Wanneer nu INV2 wordt betaald, wordt de volgende vermelding aangemaakt. Merk op dat de financiële dimensies van de contantkorting de financiële dimensies van de bijbehorende uitgaven volgen.

| Boekstuk | Rekening  | Boekingstype     | Debet | Krediet |
|-------------|--------------|----------------------|-----------|------------|
| APPAYM001   | 200110-001-  | Leveranciersaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bank                 |           | 197.00     |
| 14000056    | 520200-003-- | Contantkorting van leverancier |           | 3,00       |
| 14000056    | 200110-001-  | Leveranciersaldo       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Eén boekstuk met meerdere leveranciers en het effect op de boekhouding voor gerealiseerde winsten/verliezen

| Boekstuk | Rekeningtype | Rekening | Beschrijving | Debet | Krediet | Rekeningtype | Rekening  |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| GNJL001     | Leverancier           | 1001        | INV1            |           | 100,00     | Grootboek           | 606300-001-- |
| GNJL001     | Leverancier           | 1001        | INV2            |           | 200,00     | Grootboek           | 606300-002-- |

In het volgende voorbeeld zijn er meerdere leveranciersfacturen geregistreerd in het grootboek op één boekstuk op de pagina **Algemeen journaal**. Deze facturen zijn verdeeld over meerdere rekeningdimensies. Na het boeken wordt één boekstuk gemaakt.

| Boekstuk | Rekening  | Boekingstype | Bedrag in transactievaluta (EUR) | Bedrag in boekhoudingsvaluta (USD) |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| GNJL001     | 606300-001-- | Grootboekjournaal   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Grootboekjournaal   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Leveranciersaldo   | -100,00                                  | -114.00                                 |
| GNJL001     | 200110-001-  | Leveranciersaldo   | -200,00                                  | -228.00                                 |

Merk op dat hier twee vermeldingen voorkomen voor het boekingstype Leverancierssaldo in één boekstuk. Er is geen manier om aan te geven dat het debetbedrag voor 606300-001 bedoeld is om de vermelding van het leverancierssaldo van 100,00 met 200110-001 te verrekenen. Dit komt doordat de gebruiker meerdere leverancierrecords in één boekstuk heeft ingevoerd. 

Met dit voorbeeld kunnen we het effect analyseren dat een enkel boekstuk heeft op de vereffeningboekhouding later in het proces. Stel dat uw valuta voor boekhouding USD is en de bovenstaande transacties werden geboekt in de transactievaluta EUR. Stel dat u de factuur van EUR 200,00 volledig betaalt maar u een gerealiseerd verlies tegenkomt vanweg een verschil in de wisselkoersen op het tijdstip waarop de factuur werd geboekt en het moment waarop de betaling werd geboekt. Merk op dat de waarde van de rekening voor gerealiseerde verliezen over alle dimensies van kostenrekeningen van het factuurboekstuk is toegewezen. In dit geval werden de twee dimensie 001 en 002 beide toegewezen, zelfs als de gebruiker van mening kan zijn dat alleen 002 behoort tot de onkostenrekening van de factuur die wordt vereffend. Dit komt doordat één boekstuk werd gebruikt om de bovenstaande factuur te boeken, waardoor er geen manier is om aan te geven hoe de gebruiker de kostenverdelingen wilde laten correleren met het leverancierssaldo in het enkele boekstuk.

| Boekstuk | Rekening | Boekingstype   | Bedrag in transactievaluta (EUR) | Bedrag in boekhoudingsvaluta (USD) |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| APPAYM001   | 200110-001- | Leveranciersaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bank               | -200,00                                  | -230.00                                 |
| 14000056    | 801300-001- | Wisselkoersverlies | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Wisselkoersverlies | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Leveranciersaldo     |                                          | -2.00                                   |

Als de gebruiker niet wil dat het wisselkoersverlies wordt toegewezen over de volledige uitgavenverdeling van de oorspronkelijke factuur in plaats van één boekstuk, moeten meerdere boekstukken worden gebruikt om de facturen te registreren. In het volgende voorbeeld ziet u hoe meerdere boekstukken kunnen worden ingevoerd in het grootboek, in plaats een enkel boekstuk te gebruiken zoals aan het begin van dit voorbeeld wordt getoond.

| Boekstuk | Rekeningtype | Rekening | Beschrijving | Debet | Krediet | Type tegenrekening | Tegenrekening |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| GNJL002     | Leverancier           | 1001        | INV1            |           | 100,00     | Grootboek          | 606300-001--       |
| GNJL003     | Leverancier           | 1001        | INV2            |           | 200,00     | Grootboek          | 606300-002--       |

Wanneer nu INV2 wordt betaald, wordt de volgende vermelding aangemaakt. Merk op dat de financiële dimensies van het wisselkoersverlies de financiële dimensies van de bijbehorende uitgaven volgen.

| Boekstuk | Rekening | Boekingstype   | Bedrag in transactievaluta (EUR) | Bedrag in boekhoudingsvaluta (USD) |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| APPAYM001   | 200110-001- | Leveranciersaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bank               | -200,00                                  | -230.00                                 |
| 14000056    | 801300-002- | Wisselkoersverlies | 0,00                                     | 2.00                                    |
| 14000056    | 200110-001- | Leveranciersaldo     |                                          | -2.00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Eén boekstuk voor scenario's met saldo-overboekingen en verrekeningen
Twee veel voorkomende scenario's waarin één boekstuk wordt gebruikt met meerdere klanten of leveranciers, zijn saldo-overboekingen van een klant of leverancier naar een andere klant of leverancier, en een verrekening tussen een klant en een leverancier binnen dezelfde organisatie. In de volgende twee voorbeelden wordt de voorkeursmethode getoond voor het invoeren van deze scenario's, als alternatief voor het invoeren in één boekstuk. 

Een *saldo-overboeking* is een boekstuk met meerdere klanten, dat wordt ingevoerd om het saldo van de en klant naar een andere over te zetten. Bij leveranciers functioneert dit op dezelfde wijze. Dit scenario kan voorkomen wanneer de verantwoordelijkheid voor het betalen van de factuur overgaat naar een andere partij, zoals wanneer een dochteronderneming de verantwoordelijkheid doorgeeft aan een moederbedrijf. 

In dit voorbeeld wordt uitgegaan van een verkoop waarbij de klant in aanmerking komt voor een contantkorting als binnen 10 dagen wordt betaald. De klant in dit voorbeeld gebruikt een verzekeringsmaatschappij die verantwoordelijk is voor het betalen van factuur. De verzekeringsmaatschappij is ingesteld als tweede klant in het systeem. Het oorspronkelijke saldo van de klant wordt overgebracht naar de verzekeringsmaatschappij, die de rekening betaalt en een contantkorting van 2% neemt voor betaling binnen de kortingsperiode. 

Laten we aannemen dat de onderstaande verkoop wordt uitgevoerd aan klant ACME. De volgende boekhoudboekingen vertegenwoordigen de verkoop.

| Grootboekrekening | Boekingstype | Debet | Krediet |
|--------------------|------------------|-----------|------------|
| 401100-002-023-    | Opbrengst          |           | 100        |
| 130100-002-        | Klantsaldo | 100       |            |

Vervolgens boekt de gebruiker het te betalen saldo van ACME naar de verzekeringsmaatschappij, in een enkel boekstuk in het journaal voor klantbetalingen. De verzekeringsmaatschappij is ingesteld als klantverzekering.

| Boekstuk | Rekeningtype | Rekening | Beschrijving | Debet | Krediet | Type tegenrekening | Tegenrekening |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| ARPAYM001   | Klant         | ACME        | Overboeking        |           | 100,00     | Klant        | Verzekering          |

Merk op dat de bovenstaande vermelding is opgenomen in een enkel boekstuk. Dit boekstuk bevat twee klantenrecords. Het volgende boekstuk wordt gemaakt wanneer de bovenstaande grootboekvermelding wordt geboekt.

| Boekstuk | Rekening | Boekingstype | Bedrag in transactievaluta |
|-------------|-------------|------------------|------------------------------------|
| ARPAYM001   | 130100-002- | Klantsaldo | 100,00                             |
| ARPAYM001   | 130100-002- | Klantsaldo | -100,00                            |

Stel vervolgens dat u een betaling van 98,00 ontvangt van de klant Verzekering en u ervoor kiest de betaling te vereffenen met de factuur die door de saldo-overboeking is aangemaakt. Het resultaat is het onderstaande boekstuk. U verwacht mogelijk dat vereffening de financiële dimensies uit de oorspronkelijke factuur gebruikt, maar dat is niet mogelijk omdat er geen factuurdocument is voor de klant Verzekering. Merk op dat standaard de distributiedimensies op de contantkorting komen van de klanttransactie die voor de overboeking is gemaakt en niet van de opbrengstrekening van de oorspronkelijke factuur. De standaard is een resultaat van het gebruik van een enkel boekstuk om de saldi over te boeken.

| Boekstuk | Rekening | Boekingstype | Debet | Krediet |
|-------------|-------------|------------------|-----------|------------|
| ARPAYM002   | 110110-002- | Bank             | 98.00     |            |
| ARPAYM002   | 130100-002- | Klantsaldo |           | 98.00      |

Op het gerelateerde boekstuk voor contantkorting komt de standaardwaarde voor de financiële dimensie van de klanttransactie die op basis van de overboeking is gemaakt, omdat de overboeking meer dan één klant heeft.

| Boekstuk | Rekening | Boekingstype       | Debet | Krediet |
|-------------|-------------|------------------------|-----------|------------|
| ARP-00001   | 403300-002- | Contantkorting van klant | 2.00      |            |
| ARP-00001   | 130100-002- | Klantsaldo       |           | 2.00       |

Als de gebruiker niet de standaardinstellingen voor de financiële dimensies van de contantkorting accepteert, moeten in plaats van één boekstuk meerdere boekstukken worden gebruikt om de saldo-overdracht te registreren. Dit scenario moet worden gerealiseerd door een creditnota voor de klant te maken VANWAAR het saldo wordt verplaatst en een debetnota of factuur te maken voor de klant WAARNAAR het saldo wordt verplaatst. In het volgende voorbeeld ziet u hoe meerdere boekstukken in het journaal met klantbetalingen kunnen worden ingevoerd om het saldo over te boeken, in plaats van één boekstuk te gebruiken zoals eerder in dit voorbeeld werd getoond.

| Boekstuk | Rekeningtype | Rekening | Beschrijving | Debet | Krediet | Type tegenrekening | Tegenrekening |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| ARPAYM001   | Klant         | ACME        |                 |           | 100,00     | Grootboek          | 401100-002-023-    |
| ARPAYM002   | Klant         | Verzekering   |                 | 100,00    |            | Grootboek          | 401100-002-023-    |

Dit betekent dat wanneer de klant Verzekering 98,00 met boekstuk ARPAYM02 betaalt, de correcte financiële dimensies van de vermelding worden gebruikt in de grootboekrekening van boekstuk ARPAYM002.

| Boekstuk | Rekening | Boekingstype | Debet | Krediet |
|-------------|-------------|------------------|-----------|------------|
| ARPAYM003   | 110110-002- | Bank             | 98.00     |            |
| ARPAYM003   | 130100-002  | Klantsaldo |           | 98.00      |

Op het gerelateerde boekstuk voor contantkorting worden de financiële dimensies gebruikt van de opbrengstrekening die als tegenrekening dient en die op het boekstuk van ARPAYM002 wordt getoond.

| Boekstuk | Rekening     | Boekingstype       | Debet | Krediet |
|-------------|-----------------|------------------------|-----------|------------|
| ARP-00001   | 403300-002-023- | Contantkorting van klant | 2.00      |            |
| ARP-00001   | 130100-002-     | Klantsaldo       |           | 2.00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Eén boekstuk met een verrekening voor meerdere klanten en leveranciers
Verrekenen kan nuttig zijn wanneer een organisatie aan hetzelfde bedrijf verkoopt en ervan koopt. In plaats van leveranciersfacturen te betalen en wachten op ontvangst van betaling voor klantfacturen, worden de leveranciers- en klantfacturen verrekend. De verrekenende transactie wordt vereffend met de openstaande saldi. 

Dit lichten we als volgt toe: stel dat leverancier 1001 en klant US-008 dezelfde rechtspersoon zijn. Uw organisatie wil de te betalen en te ontvangen saldi vereffenen voordat het resterende saldo wordt betaald of ontvangen. Stel dat de klantrecord u EUR 75,00 verschuldigd is en u de leveranciersrecord EUR 100,00 schuldig bent. Dit betekent dat u de saldi wilt vereffenen en alleen EUR 25,00 betaalt aan de leverancier. Stel dat verder dat de valuta voor boekhouding USD is. In dit geval wordt een verrekeningstransactie ingevoerd in een boekstuk in het leveranciersbetalingsjournaal.

| Boekstuk | Rekeningtype | Rekening | Beschrijving | Debet | Krediet | Type tegenrekening | Tegenrekening |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| APPAYM001   | Leverancier           | 1001        | Verrekening         |  75,00    |            | Klant        | US-008             |

Om ongewenste problemen met toekomstige vereffeningen voor deze transactie te vermijden, zou u in plaats van één boekstuk meerdere boekstukken moeten invoeren in het journaal om de verrekeningstransactie te registreren. Merk op dat de klant- en leverancierssaldi met één speciale vereffeningsrekening worden vereffend, zodat u niet een enkel boekstuk hoeft te gebruiken dat meerdere klant- en leverancierssaldi bevat.

| Boekstuk | Rekeningtype | Rekening | Beschrijving | Debet | Krediet | Type tegenrekening | Tegenrekening |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| 001         | Klant         | US-008      |                 |           |  75,00     | Grootboek          | 999999---          |
| 002         | Leverancier           | 1001        |                 |  75,00    |            | Grootboek          | 999999---          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]