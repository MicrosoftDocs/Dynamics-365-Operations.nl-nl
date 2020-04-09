---
title: Validatie van factuurvereffening instellen voor leveranciers
description: Dit onderwerp biedt informatie over het instellen van validatie van factuurvereffening voor leveranciers.
author: abruer
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a101edd9e25fba1aa2325cb2193c6ea56282c9d1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143783"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Validatie van factuurvereffening instellen voor leveranciers

[!include [banner](../../includes/banner.md)]

Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd. Als uw rechtspersoon uitgaven bijhoudt, zoals verzendkosten, door kosten te berekenen, moet u er voor zorgen dat de configuratiesleutel Toeslagen is geselecteerd.  Factuurmatching in Klanten is het proces van het vergelijken van de leverancierfactuur-, inkooporder- en productontvangstgegevens. Verschillen in deze documenten worden matchingverschillen genoemd. Matchingverschillen worden vergeleken met de gespecificeerde toleranties. Als een vereffeningsverschil groter is dan het tolerantiepercentage of -bedrag, worden de pictogrammen voor vereffeningsafwijkingen weergegeven op de pagina **Leveranciersfactuur** en op de pagina **Factuurvereffeningsgegevens**.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Bepalen welke validatie voor factuurvereffening moet worden gebruikt
Er zijn vier verschillende typen vereffeningsvalidatie beschikbaar. 

- **Vereffening op regelniveau**: het meestgebruikte type is regelvereffening. Regelvereffening kan in twee of in drie richtingen worden uitgevoerd. Op de pagina **Parameters van module Leveranciers** kan het standaardniveau voor regelvereffening worden opgegeven voor een rechtspersoon. Bij tweeweg-afstemming wordt de eenheidsprijs van de factuur vergeleken met de eenheidsprijs van de inkooporder. Bij drieweg-afstemming wordt de factuurhoeveelheid bovendien ook nog vergeleken met het vereffende aantal productontvangstbonnen.
- **Vereffening van factuurtotalen**: vereffen de totaalbedragen op de factuur met de totaalbedragen op de inkooporder. Dit type factuurvergelijking bevat de minste gegevens, dus kunt u deze optie gebruiken voor het instellen van besturingselementen die de werktijd minimaliseren die vereist is voor het controleren van factuurvergelijkingsinformatie. Er worden zes totalen vergeleken, zoals het subtotaal, de totale korting, toeslagen, btw, afronding en factuurbedrag. Er wordt gecontroleerd of deze waarden op de factuur afwijken van de verwachte bedragen met meer dan een acceptabel verschil.
- **Vereffening van toeslagen**: vereffen de informatie over toeslagen (bedragen) op de factuur met de informatie over toeslagen (bedragen) op de inkooporder.
- **Prijstotalen voor regelartikelvereffening**: dit type vereffening is nuttig voor bedrijven die normaal gesproken meerdere facturen voor één inkooporderregel ontvangen. Als u doorgaans slechts één factuur per inkooporderregel ontvangt, is dit type vereffening niet nodig. Dit type vereffening vereist dat twee- of drieweg-afstemming is ingeschakeld en dient als validatie van een niet te overschrijden nettobedrag, op basis van tolerantiepercentages en -bedragen.  Bij dit type vereffening worden prijsgegevens vergeleken voor het nettobedrag van elke regel van de factuur en alle in behandeling zijnde en eerder geboekte factuurregels, met het nettobedrag van de overeenkomstige inkooporderregel. Het nettobedrag wordt bepaald met behulp van de volgende formule: (prijs per eenheid * regelkwaliteit) + regelkosten - regelkortingen. Bij het vergelijken van prijstotalen op basis van percentage, worden waarden met behulp van de transactievaluta vergeleken. Bij het vergelijken van prijstotalen op basis van bedrag, worden de waarden met behulp van de valuta voor boekhouding vergeleken.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Parameters voor factuurvereffeningsvalidatie instellen
1. Ga naar **Leveranciers > Instellingen > Parameters van module Leveranciers**.
2. Selecteer het tabblad **Factuurvalidatie**.
3. Schakel het selectievakje **Factuurvereffeningsvalidatie inschakelen** in of uit.
    * Selecteer of goedkeuring vereist is voordat een factuur die verschillen vertoont voor factuurvereffening kan worden geboekt. Als dit is ingesteld op **Toestaan met waarschuwing**, geeft de grafische indicatie weer wanneer een verschil voor factuurvereffening groter is dan de tolerantie. U kunt de factuur echter wel boeken. Als u workflows gebruikt samen met factuurvereffeningsvalidatie, moet u controleren of het veld **Factuur met verschillen boeken** is ingesteld op **Toestaan met waarschuwing** om meerdere keren goedkeuren te voorkomen.  
    * Selecteer in het veld **Status factuurkoptekst automatisch bijwerken** of de vereffening automatisch door het systeem wordt uitgevoerd tijdens de invoer van factuurgegevens. De aanbevolen instelling is **Ja**, tenzij u problemen ondervindt met de prestaties voor gegevensinvoer. Als automatische updates worden uitgeschakeld, worden de systeemprestaties mogelijk sneller omdat de factuurvereffeningsvalidatie worden genegeerd tijdens de gegevensinvoer. De medewerker die de gegevensinvoer doet moet handmatig de vereffeningsstatus bijwerken om de resultaten van de factuurvereffeningsvalidatie te bekijken wanneer dit is ingesteld op **Nee**.  
4. Stel **Vereffening van factuurtotalen** in.
5. Schakel het selectievakje **Factuurtotalen vereffenen** in of uit om de feitelijke factuurtotalen te vereffenen met de verwachte totalen.
    * Selecteer of een pictogram wordt weergegeven als een verschil voor factuurvereffening groter is dan de tolerantie. U kunt kiezen om het pictogram weer te geven als een positieve discrepantie groter is dan de tolerantie, of wanneer een positieve of een negatieve discrepantie de tolerantie overschrijdt.  
    * Bijvoorbeeld: de tolerantie is 5 procent en het totale factuurbedrag op de inkooporder is 100,00. Daarom wordt een pictogram voor prijsvereffening weergegeven als het totale factuurbedrag op de factuur hoger is dan 105,00. Als u **Indien groter of kleiner dan tolerantie** selecteert, wordt het pictogram ook weergegeven als het factuurbedrag minder dan 95,00 bedraagt.  
6. Voer in het veld **Tolerantiepercentage voor factuurtotalen** het acceptabele tolerantiepercentage in. Deze waarde is de standaardwaarde voor het bedrijf. Deze waarde kan voor specifieke leveranciers worden overschreven via de pagina **Toleranties voor factuurtotalen**. Zie de sectie Vereffeningstolerantie voor factuurtotalen voor leveranciers instellen verderop in dit onderwerp voor meer informatie over het overschrijven van het tolerantiepercentage voor factuurtotalen voor een specifieke leverancier.
7. Stel **Prijs- en hoeveelheidsvereffening** in.
8. Selecteer in het veld **Regelovereenstemmingsbeleid** een waarde om te gebruiken als standaardbeleid voor de rechtspersoon waarmee u werkt. **Niet vereist** betekent dat er geen controle van afzonderlijke prijzen op factuurregels ten opzichte van inkooporderprijzen of factuurhoeveelheden ten opzichte van pakbonhoeveelheden vereist is. **Tweewegs overeenstemming** betekent dat de verificatie van factuurregels vereist is, maar dat alleen de inkooporder en de factuurdocumenten van de leverancier worden gebruikt voor de verificatie. Er wordt geen rekening gehouden met de productontvangst bij de overeenstemmingsvalidaties. **Driewegs overeenstemming** betekent dat de netto-eenheidprijs van de factuur wordt vergeleken met de netto-eenheidsprijs van de inkooporder en dat de overeenkomstige productontvangsthoeveelheid wordt vergeleken met de factuurhoeveelheid.
9. Selecteer een waarde in het veld **Overschrijven van overeenstemmingsbeleid toestaan** om toe te staan dat een ander vereffeningsniveau voor een artikel, leverancier, combinatie van leverancier en artikel of inkooporderregel wordt toegepast. Het regelovereenstemmingsbeleid van de rechtspersoon kan worden genegeerd voor een specifieke leverancier, een specifiek artikel of een specifieke combinatie van leverancier op de pagina **Overeenstemmingbeleid**.
    * Als u een overeenstemmingsbeleid voor regels van Tweewegs overeenstemming of Driewegs overeenstemming gebruikt, kunt u prijstolerantiepercentages instellen voor uw rechtspersoon, artikelen en leveranciers op de pagina **Artikelprijstolerantie**. De prijstolerantie voor de standaardrechtspersoon wordt ingesteld op nul procent voor vereffening in twee en drie richtingen. Als de leveranciersfacturen vergeleken worden met de informatie op inkooporders, wordt gezocht naar het van toepassing zijnde percentage voor prijstolerantie.   
10. U kunt prijstotalen voor regelartikelen op facturen vereffenen door een waarde te selecteren in het veld **Totaalprijzen vereffenen**. Dit type aanpassing is handig wanneer de leverancier meerdere facturen voor dezelfde inkooporderregel verzendt. U kunt prijsgegevens vergelijken voor het nettobedrag van iedere regel van de factuur en alle in behandeling zijnde en eerder geboekte factuurregels, met het nettobedrag van de overeenkomstige inkooporderregel.  De beschikbare opties zijn **Geen**, **Percentage**, **Bedrag** en **Percentage en bedrag**.
11. Voer in het veld **Tolerantiepercentage totale inkoopprijs** een percentage van de afwijking in dat u wilt accepteren. Dit veld is beschikbaar als **Totaalprijzen vereffenen** is ingesteld op **Percentage** of **Percentage en bedrag**.
12. Voer in het veld **Tolerantie totale inkoopprijs** een bedrag in de valuta voor boekhouding in. Dit veld is beschikbaar als **Totaalprijzen vereffenen** is ingesteld op **Bedrag** of **Percentage en bedrag**.
13. Selecteer in het veld **Pictogram voor totaalprijsvereffening weergeven** of een pictogram wordt weergegeven als een verschil voor factuurvereffening groter is dan de tolerantie voor de nettoprijs per eenheid. U kunt kiezen om het pictogram weer te geven als een positieve discrepantie groter is dan de tolerantie, of wanneer een positieve of een negatieve discrepantie de tolerantie overschrijdt.
Bijvoorbeeld: de tolerantie is 5 procent en de totale artikelprijs op de inkooporder is 10,00. Daarom wordt een pictogram voor prijsvereffening weergegeven als de totale artikelprijs op de factuur hoger is dan 10,50. Als u **Indien groter of kleiner dan tolerantie** selecteert, wordt het pictogram ook weergegeven als de totale artikelprijs op de factuur minder dan 9,50 bedraagt.
13. Stel de vereffening van toeslagen in.
14. Als u feitelijke kosten wilt vereffenen met de verwachte kosten, gebaseerd op de informatie in de inkooporder, schakelt u het selectievakje **Vereffening van toeslagen** in.

## <a name="set-up-unit-price-tolerance-percentages"></a>Tolerantiepercentages voor eenheidsprijzen instellen
Ga naar **Leveranciers > Instellen > Instelling van factuurvereffening > Prijstoleranties** om toegestane prijstolerantiepercentages op te geven. Als u een overeenstemmingsbeleid voor regels van Tweewegs overeenstemming of Driewegs overeenstemming gebruikt, kunt u prijstolerantiepercentages instellen voor uw rechtspersoon, artikelen en leveranciers. Als de leveranciersfacturen vergeleken worden met de informatie op inkooporders, wordt gezocht naar het van toepassing zijnde percentage voor prijstolerantie. De standaardvolgorde voor zoeken is als volgt:
* Tabel/tabel
* Tabel/groep
* Tabel/alle
* Groep/tabel
* Groep/groep
* Groep/alle
* Alle/tabel
* Alle/groep
* Alle/alle

De standaard prijstolerantie voor een rechtspersoon is 0 procent, en deze prijstolerantie wordt toepepast op alle artikelen en alle rekeningen (Alle, Alle). U kunt de record voor de prijstolerantie voor de standaardrechtspersoon niet verwijderen.

Standaard zijn negatieve prijsverschillen toegestaan. U kunt echter geen negatieve waarde invoeren als prijstolerantiepercentage. Als u negatieve prijstoleranties wilt traceren, selecteert u **Indien groter of kleiner dan tolerantie** in het veld **Pictogram voor eenheidsprijsovereenkomst weergeven** op de pagina **Parameters van Leveranciers**. Voer vervolgens prijstolerantiepercentages in op de pagina **Prijstoleranties**.

## <a name="set-up-matching-policy-override"></a>Overschrijven van overeenstemmingsbeleid instellen

Ga naar **Leveranciers > Instellen > Instelling van factuurvereffening > Overeenstemmingbeleid** om de standaardinvoer voor het veld Overeenstemmingbeleid voor regels in het formulier Inkooporder op te geven. Deze instelling is optioneel. Met dit formulier kunt u tweeweg- of drieweg-overeenstemming instellen voor artikelen, leveranciers of combinaties van artikelen en leveranciers. Hiermee kunt u een nauwkeuriger overeenstemmingsbeleid definiëren dan het overeenstemmingsbeleid voor rechtspersonen dat u hebt gedefinieerd op de pagina **Parameters van module Leveranciers**. Het standaard regelovereenstemmingsbeleid voor rechtspersonen is van toepassing op alle artikelen en leveranciers, met uitzondering van artikelen en leveranciers waarvoor een ander regelovereenstemmingsbeleid is opgegeven op deze pagina.

Selecteer op deze pagina **Niveau overeenstemmingsbeleid**. Selecteer het niveau in de hiërarchie voor het overeenstemmingsbeleid waarvoor u het regelovereenstemmingsbeleid wilt instellen.

- **Artikel en leverancier**: geef het overeenstemmingsbeleid op voor specifieke artikelen die zijn aangeschaft bij specifieke leveranciers.
- **Artikel**: geef het overeenstemmingsbeleid op voor specifieke artikelen die zijn aangeschaft bij alle leveranciers, met uitzondering van artikelen die zijn opgegeven op artikel- en leveranciersniveau.
- **Leverancier**: geef het overeenstemmingsbeleid op voor alle artikelen die zijn aangeschaft bij specifieke leveranciers, met uitzondering van artikelen die zijn opgegeven op leveranciers- en artikelniveau.
  
Op basis van de volgende hiërarchie wordt bepaald welk overeenstemmingsbeleid wordt gebruikt:
  *  Artikel en leverancier
  *  Item
  *  Leverancier
  *  Rechtspersoon
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Vereffeningstolerantie voor factuurtotalen voor leveranciers instellen

G naar **Leveranciers > Instellen > Instelling van factuurvereffening > Toleranties voor factuurtotalen** om leveranciersspecifieke toleranties voor de vereffening van factuurtotalen op te geven. De vereffeningberekening gebruikt het tolerantiepercentage voor de factuurtotalen van de leveranciersrekening die als orderrekening op de leveranciersfactuur is opgegeven. Als de leveranciersrekening geen opgegeven tolerantiepercentage voor factuurtotalen bevat, wordt het percentage gebruikt dat is opgegeven voor de rechtspersoon op de pagina **Parameters van module Leveranciers**.

1. Als u toleranties voor individuele leveranciers wilt instellen die de standaardtolerantie overschrijven, selecteer u **Leverancier**.
2. Voer het afwijkingspercentage in dat u voor deze leverancier accepteert.
