---
title: Factuurvereffening voor leveranciers
description: Factuurmatching in Klanten is het proces van het vergelijken van de leverancierfactuur-, inkooporder- en productontvangstgegevens.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 6d1348ad43f8170f29bfc2f3df8a2ec60f9f8912
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="accounts-payable-invoice-matching"></a>Factuurvereffening voor leveranciers

[!include[banner](../includes/banner.md)]


Factuurmatching in Klanten is het proces van het vergelijken van de leverancierfactuur-, inkooporder- en productontvangstgegevens.

Bij het afstemmen van documenten worden verschillen in deze documenten aangeduid als matchingverschillen. Matchingverschillen worden vergeleken met de gespecificeerde toleranties. Als een matchingverschil het tolerantiepercentage of -bedrag overschrijdt, worden er pictogrammen voor het vereffeningsverschil weergegeven in het formulier Leveranciersfactuur en op de pagina Factuurhistorie en vereffeningsgegevens. 

U voert bijvoorbeeld een inkooporder in met één regelartikel voor 1000 batterijen tegen een prijs van 1,00 per stuk. De inkooporder wordt goedgekeurd en naar de leverancier verzonden. De leverancier verzendt 1000 batterijen en u voert een productontvangstbon in voor 1000 batterijen tegen een prijs van 1,00 per stuk. De voorraadkosten voor de batterijen worden bijgewerkt met deze prijs. 

Er komt een factuur binnen voor 1000 batterijen tegen een prijs van 1,10 per stuk. Volgens het rechtspersoonbeleid is een prijstolerantie per netto eenheid van 5 procent toegestaan voor deze artikelcategorie. Een prijs van 1,05 is dus acceptabel, maar een prijs van 1,10 niet. Wanneer u de factuurgegevens invoert, wordt er een prijsverschil geconstateerd en kunt u de factuur opslaan totdat het verschil is opgelost.

U kunt de volgende typen Factuurvergelijking voor leveranciers gebruiken:

-   Vergelijking factuurtotalen – Vergelijk de totaalbedragen op de factuur met de totaalbedragen op de inkooporder. Dit type factuurvergelijking bevat de minste gegevens, dus kunt u deze optie gebruiken voor het instellen van besturingselementen die de werktijd minimaliseren die vereist is voor het controleren van factuurvergelijkingsinformatie.
-   Vergelijking op twee manieren – Vergelijk de prijsgegevens op de factuur met de prijsgegevens op de inkooporder.
-   Vergelijking op drie manieren – Vergelijk de prijsgegevens op de factuur met de prijsgegevens op de inkooporder. Vergelijk ook de informatie over de hoeveelheid op de factuur met de informatie over de hoeveelheid op de productontvangstbonnen die voor de factuur zijn geselecteerd.
-   Toeslagen vergelijken – Vergelijk de informatie over toeslagen (bedragen) op de factuur met de informatie over toeslagen (bedragen) op de inkooporder.

> [!NOTE]
> Andere vormen van factuurvalidatie kunnen worden uitgevoerd door beleidsregels voor leveranciersfacturen te gebruiken. 

Vergelijkingen op twee en drie manieren vergelijken altijd prijsgegevens met de prijs per eenheid. U kunt dit overeenstemmingsbeleid tevens dusdanig configureren dat prijsgegevens met de totaalprijs worden vergeleken.
-   Netto prijs per eenheid vergelijken – Vergelijk prijsgegevens voor vergelijken op drie manieren door de netto prijs per eenheid voor iedere regel op de factuur te vergelijken met de betreffende netto prijs per eenheid op de inkooporder. De netto prijs per eenheid wordt bepaald met behulp van de volgende formule: netto bedrag van de regel / hoeveelheid van de regel.
-   Prijstotalen vergelijken – Vergelijk prijsgegevens voor vergelijken op drie manieren door het netto bedrag (totaalprijs) voor iedere regel op de factuur te vergelijken met het betreffende netto bedrag op de inkooporder. Het netto bedrag wordt bepaald met behulp van de volgende formule: (prijs per eenheid \* regelkwaliteit) + regelkosten - regelkortingen

Berekeningen van de factuurvergelijking worden automatisch uitgevoerd wanneer u leveranciersfacturen bewerkt op de pagina Leveranciersfactuur. Factuurvergelijking kan eventueel ook worden uitgevoerd op aanvraag, wanneer vereist. Factuurvereffening op aanvraag wordt voor de rechtspersoon geregeld door Status factuurkoptekst automatisch bijwerken ´Aan´ op de pagina Parameters van Leveranciers op het tabblad Factuurvalidatie. Factuurvereffening kan tevens worden uitgevoerd als onderdeel van een beoordelingsproces van een factuur. U kunt de resultaten van factuurvergelijking op de pagina Leverancierfactuur en gerelateerde factuurvergelijkingsformulieren bekijken.

## <a name="invoice-totals-matching"></a>Vereffening van factuurtotalen
U kunt factuurtotaalvergelijking gebruiken om ervoor te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil. Er worden zes totalen vergeleken op de pagina Vergelijkingsgegevens factuurtotalen, zoals getoond in de volgende tabel. Als de toegestane tolerantie voor factuurtotaalvergelijking 20% is, wordt het afwijkingspercentage van 100% voor het totale kortingsbedrag als matchingverschil beschouwd.

| Totaal veld    | Werkelijk factuurtotaal | Verwacht factuurtotaal | Afwijkingspercentage | Vereffeningsstatus |
|----------------|----------------------|------------------------|---------------------|--------------|
| Saldo        | 495,00               | 495,00                 | 0%                  | Geslaagd       |
| Totale korting | 0,00                 | 9,90                   | 100%                | Mislukt       |
| Kosten        | 64,90                | 64,90                  | 0%                  | Geslaagd       |
| Btw      | 139,98               | 137,50                 | 2%                  | Geslaagd       |
| Afronden      | 0,00                 | 0,00                   | 0%                  | Geslaagd       |
| Factuurbedrag | 699,88               | 687,50                 | 2%                  | Geslaagd       |

Factuurtotalen vergelijken wordt geregeld voor de rechtspersoon door de wisselknop voor Factuurtotalen vereffenen op de pagina Parameters van module Leveranciers. Verwachte factuurtotalen en de werkelijke factuurtotalen worden vergeleken. De verwachte factuurtotalen worden berekend op basis van de prijzen, toeslagen en btw-gegevens uit de inkooporder en de hoeveelheden uit de factuur.

## <a name="two-way-price-totals-matching"></a>Prijstotalen vergelijken op twee manieren
Gebruik vergelijken op twee manieren om ervoor te zorgen dat het verschil tussen de prijsgegevens op de inkooporder en de factuur acceptabel is. U kunt prijsgegevens vergelijken voor het netto bedrag op iedere regel van de factuur, en alle in behandeling zijnde en eerder geboekte factuurregels, met het netto bedrag van de betreffende inkooporderregel. Dit noemen we prijstotalen vergelijken. 

Prijstotalen vergelijken kan gebaseerd zijn op een percentage, een bedrag, of een percentage en bedrag. 

Als een tolerantiepercentage van een inkoopprijstotaal is gespecificeerd, worden er vijf velden vergeleken, zoals in de volgende tabel wordt weergegeven. Omdat het tolerantiepercentage van het inkoopprijstotaal 10% is, vertegenwoordigt het afwijkingspercentage van het prijstotaal van 50% een matchingverschil.

| Vereffeningsstatus | Nettobedrag van factuur | Verwacht nettobedrag | Afwijkingspercentage totaalinkoopsprijs (afwijkingsbedrag) | Afwijkingspercentage totaalinkoopsprijs (afwijkingspercentage) | Tolerantiepercentage totale inkoopprijs |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Geslaagd       | 105,00             | 100,00              | 5,00                                             | 5%                                                              | 10%                                    |
| Mislukt       | 150,00             | 100,00              | 50,00                                            | 50%                                                             | 10%                                    |

Als er een tolerantiebedrag van een inkoopprijstotaal is gespecificeerd, worden er vijf velden vergeleken, zoals in de volgende tabel wordt weergegeven. Omdat het tolerantiebedrag van het inkoopprijstotaal 100 is, vertegenwoordigt het afwijkingsbedrag van het prijstotaal van 105 een matchingverschil.

| Vereffeningsstatus | Nettobedrag van factuur | Verwacht nettobedrag | Afwijkingspercentage totaalinkoopsprijs (afwijkingsbedrag) | Afwijking van totaalinkoopsprijs, uitgedrukt in valuta voor boekhouding (afwijkingsbedrag) | Tolerantie totale inkoopprijs |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Geslaagd       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Mislukt       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Als prijstotalen vergelijken is ingesteld met een percentagetolerantie en een tolerantiebedrag, ook wel 'een bedrag dat niet mag worden overschreden' genoemd, wordt er met beide rekening gehouden bij het bepalen of een regel een matchingverschil heeft. Als het percentage of het bedrag de tolerantie overschrijdt, zoals in de regels 150 en 205 in de volgende tabel wordt weergegeven, heeft de regel een matchingverschil.

| Vereffeningsstatus | Nettobedrag van factuur | Verwacht nettobedrag | Afwijkingspercentage totaalinkoopsprijs (afwijkingspercentage) | Tolerantiepercentage totale inkoopprijs | Afwijking van totaalinkoopsprijs, uitgedrukt in valuta voor boekhouding (afwijkingsbedrag) | Tolerantie totale inkoopprijs |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Geslaagd       | 105,00             | 100,00              | 5%                                                              | 10%                                    | 5,00                                                                    | 100,00                         |
| Mislukt       | 150,00             | 100,00              | 50%                                                             | 10%                                    | 50,00                                                                   | 100,00                         |
| Mislukt       | 205,00             | 100,00              | 105%                                                            | 10%                                    | 105,00                                                                  | 100,00                         |

Op twee manieren vergelijken wordt geregeld voor de rechtspersoon in het veld Regelovereenstemmingsbeleid op de pagina Parameters van module Leveranciers. Afhankelijk van de selectie in het veld Overschrijven van overeenstemmingsbeleid toestaan kunt u vergelijken op twee manieren selecteren voor een bepaald leveranciersartikel, of een combinatie van artikel en leverancier op de pagina Overeenstemmingbeleid en voor een bepaalde inkooporder op de pagina Inkooporder.

Prijstotalen vergelijken wordt geregeld voor de rechtspersoon in het veld Totaalprijzen vereffenen op de pagina Parameters van module Leveranciers. Het tolerantiepercentage en tolerantiebedrag van het inkoopprijstotaal (bedrag dat niet mag worden overschreden) worden ook op die pagina gespecificeerd.

## <a name="two-way-net-unit-price-matching"></a>Prijsmatching van netto eenheid op twee manieren
Gebruik vergelijken op twee manieren om ervoor te zorgen dat het verschil tussen de prijsgegevens op de inkooporder en de factuur acceptabel is. U kunt prijsgegevens vergelijken voor de netto prijs per eenheid van ieder artikel op de factuur. Dit noemen we de netto prijs per eenheid vergelijken. 

Er worden negen regelbedragen vergeleken op de pagina Vergelijkingsgegevens factuurtotalen, zoals getoond in de volgende tabel. Als de toegestane prijstolerantie voor prijsmatching van de netto eenheid 10% is, wordt de afwijking van 22,61% voor de prijs per eenheid beschouwd als een matchingverschil.

| Regelveld                    | Factuurwaarde | Waarde inkooporder | Afwijkingspercentage | Vereffeningsstatus |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Eenheidsprijs                    | 55,40         | 55,38                | 0%                  | Geslaagd       |
| Prijseenheid                    | 1,00          | 1,00                 | 0%                  | Geslaagd       |
| Toeslagen op inkopen          | 50,00         | 0,00                 | 100%                | Mislukt       |
| Korting                      | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Kortingspercentage              | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Meerregelkorting            | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Meerregelkortingspercentage | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Nettobedrag                    | 271,60        | 221,52               | 22,61%              | Mislukt       |
| Netto eenheidsprijs                | 67,9000       | 55,3800              | 22,61%              | Mislukt       |

Op twee manieren vergelijken wordt geregeld voor de rechtspersoon in het veld Regelovereenstemmingsbeleid op de pagina Parameters van module Leveranciers. Afhankelijk van de selectie in het veld Overschrijven van overeenstemmingsbeleid toestaan kunt u vergelijken op twee manieren selecteren voor een bepaald leveranciersartikel, of een combinatie van artikel en leverancier op de pagina Overeenstemmingbeleid en voor een bepaalde inkooporder op de pagina Inkooporder. 

Netto-eenheidsprijzen vergelijken wordt geregeld voor de rechtspersoon in het veld Factuurvereffeningsvalidatie inschakelen op de pagina Parameters van module Leveranciers. De tolerantiepercentages voor de netto prijs per eenheid kan worden geconfigureerd voor artikelen, artikelgroepen, leveranciersgroepen, combinaties van artikel en leverancier, of rechtspersoon door de pagina Prijstoleranties te gebruiken.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a>Vergelijken van prijstotalen op twee manieren en prijsmatching van netto eenheid
U kunt vergelijken van prijstotalen en prijsmatching van netto eenheid samen gebruiken. Dit voorbeeld gaat uit van de volgende configuratie:

-   De prijstolerantie per netto eenheid voor het USB-drive-artikel is 10%.
-   De matchingtolerantie voor prijstotalen voor de rechtspersoon bedraagt 15% of 500.

De inkooporder bevat de volgende regel:

| Artikelnummer | Hoeveelheid | Eenheidsprijs | Nettobedrag |
|-------------|----------|------------|------------|
| USB-drive   | 1.000    | 10,00      | 10.000,00  |

Er worden drie facturen ingevoerd, zoals in onderstaande tabel wordt weergegeven. Er is een factuurverschil voor factuur 3 omdat het verschil van 1.880 het tolerantiebedrag van het inkoopprijstotaal van 500 overschrijdt. Voor het vergelijken van prijstotalen, bevat het netto bedrag van de factuur alle eerder geboekte facturen, naast de factuur waar u momenteel mee werkt.

| Artikelnummer          | Hoeveelheid | Eenheidsprijs | Nettobedrag | Prijsovereenkomst | Totaalprijsvereffening |
|----------------------|----------|------------|------------|-------------|-------------------|
| Factuur 1: USD-drive | 800      | 10,80      | 8.640,00   | Geslaagd      | Geslaagd            |
| Factuur 2: USB-drive | 100      | 10,80      | 1.080,00   | Geslaagd      | Geslaagd            |
| Factuur 3: USD-drive | 200      | 10,80      | 2.160,00   | Geslaagd      | Mislukt            |
| Totaal                |          |            | 11.880,00  |             |                   |

## <a name="three-way-matching"></a>Drieweg-afstemming

Gebruik vergelijken op drie manieren om ervoor te zorgen dat het verschil tussen de prijsgegevens op de inkooporder en de factuur acceptabel is, en om ervoor te zorgen dat de hoeveelheid op de factuur overeenkomst met de hoeveelheid op de betreffende productontvangstbonnen.

Dezelfde regelbedragen worden vergeleken op de pagina Factuurvergelijkingsgegevens, net als bij het vergelijken op twee manieren. Verder wordt het aantal facturen vergeleken met het aantal ontvangen productontvangstbonnen. Als het aantal facturen verschilt van het vergeleken aantal productontvangstbonnen, is er een fout op het gebied van aantallen.

| Regelveld                    | Factuurwaarde | Waarde inkooporder | Afwijkingspercentage | Vereffeningsstatus |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Eenheidsprijs                    | 55,40         | 55,38                | 0%                  | Geslaagd       |
| Prijseenheid                    | 1,00          | 1,00                 | 0%                  | Geslaagd       |
| Toeslagen op inkopen          | 50,00         | 0,00                 | 100%                | Mislukt       |
| Korting                      | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Kortingspercentage              | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Meerregelkorting            | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Meerregelkortingspercentage | 0,00          | 0,00                 | 0%                  | Geslaagd       |
| Nettobedrag                    | 271,60        | 221,52               | 22,61%              | Mislukt       |
| Netto eenheidsprijs                | 67,9000       | 55,3800              | 22,61%              | Mislukt       |

| Regelveld                     | Factuurwaarde | Vereffeningsstatus |
|--------------------------------|---------------|--------------|
| Gefactureerde hoeveelheid               | 4,00          |              |
| Totaal gematchte productontvangstbonnen | 0,00          | Mislukt       |

Op drie manieren vergelijken wordt geregeld voor de rechtspersoon in het veld Regelovereenstemmingsbeleid op de pagina Parameters van module Leveranciers. Afhankelijk van de selectie in het veld Overschrijven van overeenstemmingsbeleid toestaan kunt u vergelijken op drie manieren selecteren voor een bepaald leveranciersartikel, of een combinatie van artikel en leverancier op de pagina Overeenstemmingbeleid en voor een bepaalde inkooporder op de pagina Inkooporder.

## <a name="charges-matching"></a>Vereffening van toeslagen
U kunt het vergelijken van toeslagen gebruiken om ervoor te zorgen dat bedragen van toeslagen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil. De totale bedragen voor iedere toeslagcode met betrekking tot de factuur en inkooporder worden vergeleken op de pagina Toeslagwaarden vergelijken - factuur: pagina, zoals in de volgende tabel wordt weergegeven. Als de toegestane tolerantie voor de toeslagcode 25% is, wordt het afwijkingspercentage van 99,999,999,999.99% voor de Licentie toeslagcode als matchingverschil beschouwd.

> [!NOTE] 
> Een afwijkingspercentage van 99,999,999,999.99% betekent dat het verwachte bedrag op de inkooporder nul is en het werkelijke bedrag op de factuur een positieve waarde is. 

| Vereffeningsstatus toeslagen | Factuurcode voor toeslagen | Berekende waarde van werkelijk totaal | Berekende waarde van verwacht totaal | Variantiebedrag | Afwijkingspercentage | Tolerantiepercentage |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Mislukt               | Rijbewijs              | 25                            | 0                               | 25              | 99.999.999.999,99%  | 25%                  |
| Geslaagd               | Vracht              | 200                           | 200                             | 0               | 0%                  | 25%                  |
| Mislukt               | Spoed             | 4                             | 2                               | 2               | 100%                | 25%                  |

Toeslagen vergelijken wordt geregeld voor de rechtspersoon door de wisselknop Toeslagen vereffenen op de pagina Parameters van module Leveranciers. U kunt tolerantiepercentages van het verschil instellen voor toeslagen op de pagina Toleranties voor toeslagen.

> [!NOTE]
> Vergelijken van toeslagen wordt uitsluitend uitgevoerd op toeslagcodes waarvoor de wisselknop Inkooporder en factuurwaarden vergelijken op de pagina Toeslagencode is geselecteerd.

## <a name="related-functionality"></a>Gerelateerde functionaliteit
Leverancierfacturen zijn vaak gebaseerd op productontvangstbonnen die staan voor werkelijke zendingen, in plaats van op inkooporders. Soms komen de gefactureerde bedragen niet overeen met de inkooporderbedragen, en soms komen de verzonden hoeveelheden niet overeen met de gefactureerde hoeveelheden. U kunt deze gegevens op de volgende manieren helpen beheren:
-   Maak een leveranciersfactuur op basis van productontvangstbonnen. Productontvangstbonnen worden automatisch voorgesteld voor facturen, en u kunt selecteren welke productontvangstbonnen er moeten worden gebruikt. U kunt indien nodig ook specifieke regelartikelen voor productontvangstbonnen selecteren uit meerdere inkooporders.
-   Geef hoeveelheidsverschillen weer tussen de gefactureerde hoeveelheid op de factuur en de ontvangen hoeveelheid op de productontvangstbon en keur deze goed. Als er een verschil is, kunt u de factuur opslaan en deze later matchen met een andere productontvangstbon of de gefactureerde hoeveelheid wijzigen zodat deze overeenkomt met de ontvangen hoeveelheid.
-   Geef factuurbedragen op die niet zijn opgenomen in de oorspronkelijke inkooporder, zodat de factuurgegevens overeenkomen met de factuur die u hebt ontvangen van de leverancier. U kunt de toeslagen voor inkooporders vergelijken met de toeslagen voor facturen. U kunt indien nodig toeslagen toevoegen aan facturen en deze toewijzen aan factuurregels.
-   Geef prijsverschillen tussen de netto-eenheidsprijs van de factuur en de netto-eenheidsprijs van de inkooporder op en keur deze goed. U kunt prijstolerantiepercentages instellen voor uw rechtspersonen, leveranciers, en artikelen. Als de leverancierfactuurregelprijs niet binnen de prijstolerantie valt, kunt u de factuur opslaan totdat deze is goedgekeurd voor boeking of totdat u een correctie ontvangt van de leverancier.

Zie [Drieweg-overeenstemmingsbeleid](three-way-matching-policies.md) voor meer informatie.





