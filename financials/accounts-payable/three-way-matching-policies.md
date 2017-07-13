---
title: Drieweg-overeenstemmingsbeleid
description: Dit artikel geeft voorbeelden van drieweg-overeenstemming.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 8ae07088fec05ad416ce1891dd0d0ecd489364ca
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="three-way-matching-policies"></a>Drieweg-overeenstemmingsbeleid

[!include[banner](../includes/banner.md)]


Dit artikel geeft voorbeelden van drieweg-overeenstemming.

<a name="example-three-way-matching-for-items"></a>Voorbeeld: drieweg-overeenstemming voor artikelen
-------------------------------------

**Samenvatting:** Ken is de controller van het hoofdkantoor van een rechtspersoon met de naam Fabrikam. Ken besluit dat alle facturen van leveranciers die zijn gebaseerd op een inkooporder, moeten worden vereffend met inkooporderregels (tweeweg-overeenstemming). Voor aankopen van items die worden gebruikt als vaste activa, moeten facturen worden vereffend met zowel de inkooporderregels en de productontvangstregels (drieweg-overeenstemming).

Fabrikam werkt met meerdere rechtspersonen en werknemers in alle delen van de wereld. Als het volume van de transacties toeneemt, nemen de verschillen tussen de ontvangsten en facturen ook toe. Dit resulteert in de activa die worden afgeschreven. Facturen van leveranciers worden betaald, maar in het proces worden geen verschillen geïdentificeerd wanneer er minder items dan besteld worden ontvangen of wanneer artikelen helemaal niet zijn ontvangen. Uitgaven vergroten ook omdat werknemers nog steeds middelen en andere materialen nodig hebben voor hun werk. Ken wil ervoor zorgen dat leveranciers de producten leveren die besteld zijn en dat de artikelen worden ontvangen door werknemers van Fabrikam. Daarom vereist Ken tweeweg- en drieweg-overeenstemming voor alle rechtspersonen in de organisatie. Door factuurvereffening kunnen problemen met artikelen die niet zijn ontvangen of die zijn verdwenen, worden bijgehouden en opgelost. 

Het factuurvereffeningsbeleid in dit voorbeeld helpen mensen in de volgende functies deze doelstellingen te bereiken:

-   Ken is de controller voor de onderneming Fabrikam. Hij kan de mensen binnen de organisatie helpen problemen te identificeren en oplossen met bestellen, ontvangen en betalen van artikelen (goederen en diensten) van leveranciers.
-   Phyllis en April zijn boekhoudmanagers in de leveranciersafdeling voor de VS-afdeling van Fabrikam. Ze kunnen bedrijfsbeleid opleggen en ervoor zorgen dat facturen pas worden betaald nadat de facturen worden vergeleken met de inkooporder en de ontvangsten van goederen en diensten, indien van toepassing.
-   Tony is de productiemanager van de voor de Verenigde Staten-afdeling van Fabrikam. Hij en ander productiepersoneel kunnen ervoor dat de artikelen worden ontvangen van leveranciers zoals ze zijn besteld en dat ze worden geregistreerd zodat het personeel het nodige heeft om hun taak uit te voeren.

### <a name="prerequisites"></a>Vereisten

-   Ken stelt het overeenstemmingsbeleid op rechtspersoonsniveau in op Drieweg-afstemming.
-   Ken stelt de vereffeningsstatus Koptekst automatisch bijwerken voor de rechtspersoon in op Ja.
-   Ken stelt het veld Totaalprijzen vereffenen voor de rechtspersoon in op Percentage en vult 15% in als het tolerantiepercentage.
-   Ken stelt het overeenstemmingsbeleid op het artikelniveau voor artikel 1500 – CNC Milicron Machine in op Drieweg-afstemming. Dit artikel is een activumartikel dat wordt gebruikt voor de productie bij Fabrikam. Facturen voor dit artikel worden vereffend met inkooporderregels voor prijzen en met productontvangstbonnen voor de hoeveelheden.
-   Tony voert een bestelopdracht voor vijf CNC-Milicron Machines in. Alicia, een medewerker inkooporders van Fabrikam, maakt een inkooporder op aan een rechtspersoon met de naam Contoso om de artikelen te leveren.

    | Artikelnummer                 | Hoeveelheid | Eenheidsprijs | Nettobedrag | Toeslagcode        | Waarde van toeslagen |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – CNC Milicron Machine | 5        | 8000,00   | 40.000,00  | Verzending & verwerking | 3000,00      |

-   Arnie, een medewerker klanten bij Contoso, bekijkt de verzendingen voor de week. Arnie selecteert de verzendtransacties om de levering van de CNC Milicron Machines aan Fabrikam te factureren. Arnie voegt een toeslag voor verzenden en behandelen toe. Fabrikam beschouwt de toeslag als een deel van de kosten van het activum.

### <a name="scenario"></a>Scenario

1.  Sammy, een werknemer in de ontvangende afdeling bij Fabrikam, ontvangt de totale hoeveelheid machines die werden verzonden door Contoso. Hij voert een aantal van 5 in op de productontvangstbon. Aangezien de inkooporder volledig is ontvangen, wordt de status van de inkooporder gewijzigd naar Ontvangen.
2.  April, de coördinator leveranciers bij Fabrikam, controleert de factuur die Contoso heeft ingediend en voert deze in. Zij controleert de volgende informatie:
    -   Voor artikelen waar drieweg-overeenstemming is vereist, controleert ze of de hoeveelheid op de factuurregel overeenstemt met de ontvangen hoeveelheid. De ontvangen hoeveelheid is aangegeven op de productontvangstbon die met de factuur wordt vereffend.
    -   Voor artikelen waarvoor een tweeweg-overeenstemming of drieweg-overeenstemming is vereist, vallen de prijzen op de factuurregel binnen de toleranties die zijn gedefinieerd in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Dit omvat de volgende soorten prijsovereenstemming:
        -   Overeenstemming netto-eenheidsprijs: De afwijking tussen de netto-eenheidsprijs op de factuurregel en de netto-eenheidsprijs op de inkooporderregel moet binnen toegestane toleranties liggen. In dit voorbeeld is de tolerantie van de netto-eenheidsprijs +8%.
        -   Vereffening van prijstotalen: de afwijking tussen de het nettobedrag op de factuurregel en het nettobedrag op de inkooporderregel moet binnen het toegestane tolerantiepercentage, -bedrag of -percentage en -bedrag liggen. In dit voorbeeld is de tolerantie van prijstotalen +15%.

De papieren factuur van Contoso bevat de volgende gegevens.

| Artikel                        | De hoeveelheid | Eenheidsprijs | Nettobedrag |
|-----------------------------|----------|------------|------------|
| 1500 – CNC Milicron Machine | 5        | 8100,00   | 40.500,00  |
| Verzending en verwerking       |          |            | 4000,00   |
| Btw                         |          |            | 0,00       |
| Totaal                       |          |            | 44.500,00  |

In Finance and Operations bevat de factuurregel de volgende informatie.

| artikelnummer                 | Hoeveelheid | Eenheidsprijs | Nettobedrag per regel | Overeenstemmingbeleid    | Overeenkomst van hoeveelheid van productontvangstbon | Prijsovereenkomst | Totaalprijsvereffening |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – CNC Milicron Machine | 5        | 8100,00   | 40.500,00       | Drieweg-afstemming | Geslaagd                         | Geslaagd      | Geslaagd            |

Omdat deze regel het factuurvereffeningsproces passeert, kan de factuur worden geboekt.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a>Voorbeeld: drieweg-overeenstemming voor combinaties van artikel en leverancier
Samenvatting: Ken is de controller van het hoofdkantoor van een rechtspersoon met de naam Fabrikam. Ken besluit dat alle facturen die zijn gebaseerd op een inkooporder, moeten worden vereffend met inkooporderregels (tweeweg-overeenstemming). Cassie is de boekhouder bij de Maleisië-afdeling van Fabrikam. Zij geeft aan dat geselecteerde artikelen die worden besteld bij bepaalde leveranciers in Maleisië, moeten worden vereffend met zowel de inkooporderregels als de productontvangstbonregels (drieweg-overeenstemming). Ze kan ook het overeenstemmingsbeleid negeren en aanpassen naar een hoger niveau voor specifieke inkooporders. 

Het volume en de bedragen zijn klein en er zijn problemen met de levering van bepaalde leveranciers in Maleisië. Om deze redenen stelt Cassie het niveau van controle voor bepaalde combinaties van artikel en leverancier in Maleisië in op drieweg-overeenstemming. 

Het factuurvereffeningsbeleid in dit voorbeeld helpen mensen in de volgende functies deze doelstellingen te bereiken:
-   Ken is de controller voor de onderneming Fabrikam. Hij kan de mensen binnen de organisatie helpen problemen te identificeren en oplossen met bestellen, ontvangen en betalen van artikelen (goederen en diensten) van leveranciers.
-   Cassie is de boekhouder voor de Maleisië-afdeling van Fabrikam. Zij kan bedrijfsbeleid opleggen en ervoor zorgen dat facturen pas worden betaald nadat deze worden vergeleken met de inkooporderregels en de productontvangstbonnen van de ontvangsten van goederen en diensten. Zij kan ook het niveau van de controle verhogen naar drieweg-overeenstemming voor bepaalde artikelen om de operationele kosten te beheren.

### <a name="prerequisites"></a>Vereisten

-   Ken stelt het overeenstemmingsbeleid op rechtspersoonsniveau in op Tweeweg-afstemming.
-   Ken stelt het veld Totaalprijzen vereffenen voor de rechtspersoon in op Percentage en vult 10% in als het tolerantiepercentage.
-   Ken stelt de eenheidsprijstolerantie voor alle artikelen in op 2%.
-   Cassie stelt het overeenstemmingsbeleid op het niveau van de combinatie artikel en leverancier voor artikel PH2500 – Computer en leverancier Contoso in op Drieweg-afstemming.
-   Alicia, een inkooporder medewerker van de afdeling Maleisië van Fabrikam, maakt inkooporders naar Contoso op om drie artikelen te leveren, zoals getoond in de volgende tabel. Wanneer ze de inkooporder maakt, overschrijft zij het overeenstemmingsbeleid voor de draadloze muis met drieweg-overeenstemming in plaats van tweeweg-overeenstemming.

    | Artikelnummer           | Hoeveelheid | Eenheidsprijs | Nettobedrag | Overeenstemmingsbeleid (standaardwaarde) | Overeenstemmingsbeleid (op de inkooporderregel) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – Computer     | 2        | 2.500,00   | 5.000,00   | Drieweg-afstemming              | Drieweg-afstemming                           |
    | MM01 – Draadloze muis | 2        | 40,00      | 80,00      | tweeweg-afstemming                | Drieweg-afstemming                           |
    | USB-drive             | 200      | 10,00      | 2.000,00   | tweeweg-afstemming                | tweeweg-afstemming                             |

### <a name="scenario"></a>Scenario

1.  De artikelen worden geleverd. Sammy, een werknemer van de ontvangstafdeling van de Maleisië-afdeling van Fabrikam, wordt onderbroken en de boekt de productontvangstbon niet onmiddellijk.
2.  April, de coördinator leveranciers bij Fabrikam, controleert de factuur die Contoso heeft ingediend en voert deze in. Zij controleert de volgende informatie:
    -   Voor artikelen waar drieweg-overeenstemming is vereist, controleert ze of de hoeveelheid op de factuurregel overeenstemt met de ontvangen hoeveelheid. De ontvangen hoeveelheid is aangegeven op de productontvangstbon die met de factuur wordt vereffend.
    -   Voor artikelen waarvoor een tweeweg-overeenstemming of drieweg-overeenstemming is vereist, vallen de prijzen op de factuurregel binnen de toleranties die zijn gedefinieerd in Finance and Operations. Dit omvat de volgende soorten prijsovereenstemming:
        -   Overeenstemming netto-eenheidsprijs: De afwijking tussen de netto-eenheidsprijs op de factuurregel en de netto-eenheidsprijs op de inkooporderregel moet binnen toegestane toleranties liggen. In dit voorbeeld is de tolerantie van de netto-eenheidsprijs +2%.
        -   Vereffening van prijstotalen: de afwijking tussen de het nettobedrag op de factuurregel en het nettobedrag op de inkooporderregel moet binnen het toegestane tolerantiepercentage, -bedrag of -percentage en -bedrag liggen. In dit voorbeeld is de tolerantie van prijstotalen +10%.

De papieren factuur van Contoso bevat de volgende gegevens.

| Artikel                  | De hoeveelheid | Eenheidsprijs | Nettobedrag |
|-----------------------|----------|------------|------------|
| PH2500 – Computer     | 2        | 2.500,00   | 5.000,00   |
| MM01 – Draadloze muis | 2        | 41,00      | 82,00      |
| USB-drive             | 200      | 10,05      | 2010,00   |
| Totaal factuur         |          |            | 7092,00   |

In Finance and Operations bevat de factuurregel de volgende informatie.

| artikelnummer           | Hoeveelheid | Eenheidsprijs | Nettobedrag per regel | Overeenstemmingbeleid    | Overeenkomst van hoeveelheid van productontvangstbon | Prijsovereenkomst | Totaalprijsvereffening |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – Computer     | 2        | 2.500,00   | 5.000,00        | Drieweg-afstemming | Mislukt                         | Geslaagd      | Geslaagd            |
| MM01 – Draadloze muis | 2        | 41,00      | 82,00           | Drieweg-afstemming | Mislukt                         | Mislukt      | Geslaagd            |
| USB-drive             | 200      | 10,05      | 2010,00         | tweeweg-afstemming   |                                | Geslaagd      | Geslaagd            |

Merk het volgende op:
-   Voor de regel PH2500 – Computer wordt er in de kolom Overeenkomst van hoeveelheid van productontvangstbon een waarschuwingspictogram weergegeven omdat de factuurregel niet is vereffend met een productontvangstbon.
-   Voor de regel MM01 – Draadloze muis wordt er in de kolom Overeenkomst van hoeveelheid van productontvangstbon een waarschuwingspictogram weergegeven omdat de factuurregel niet is vereffend met een productontvangstbon. De kolom Eenheidsprijs vereffenen bevat een waarschuwingspictogram omdat de tolerantie van 2% op de netto-eenheidsprijs is overschreden.
-   Voor de regel USB-station, is de kolom Overeenkomst van hoeveelheid van productontvangstbon leeg omdat tweeweg-overeenstemming niet overeenkomt met de hoeveelheden van de factuurregel en de productontvangstregel.

Als goedkeuring vereist is voor facturen die moeten worden geboekt met verschillen in factuurvereffening, moet het selectievakje Boeking met vereffeningsverschillen goedkeuren op de pagina Factuurvereffeningsgegevens worden geselecteerd voordat de factuur kan worden geboekt met de fouten bij prijsvereffening en hoeveelheidvereffening. Als er geen goedkeuring is vereist, kan factuurverwerking verdergaan als er geen andere boekingsfouten zijn.


Zie [Factuurvereffening voor crediteuren](accounts-payable-invoice-matching.md) voor meer informatie.




