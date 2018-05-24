---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Operations, versie 1611 (november 2016 )
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Operations, versie 1611.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 53c51ec1be145c72ff5090666399ac4ea113e5df
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Operations, versie 1611 (november 2016 )

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Operations, versie 1611.

<a name="cost-accounting"></a>Kostprijsboekhouding
---------------

<table>




<thead>
<tr class="header">
<th>Wat u kunt doen</th>
<th>Waarom dit belangrijk is</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dimensies van kostenelementen definiëren en dimensieleden van kostenelementen importeren.</td>
<td>Door middel van kostenelementen worden in kostprijsboekhouding kosten gecategoriseerd en de stroom van kosten gedocumenteerd. De primaire kostenelementen worden op een van twee wijzen geïmporteerd: door middel van een gegevensconnector in Microsoft Dynamics 365 for Operations worden hoofdrekeningen rechtstreeks opgehaald bij Operations; of door middel van een algemene gegevensconnector worden via Microsoft Excel hoofdrekeningen opgehaald bij een ander type bronsysteem. Nadat hoofdrekeningen in Kostprijsboekhouding zijn geïmporteerd, worden ze gebruikt als dimensieleden voor kostenelementen. De secundaire kostenelementen worden door de gebruiker gedefinieerd in en gebruikt in toewijzingen om de stroom van kosten te documenteren.</td>
</tr>
<tr class="even">
<td>Dimensies van kostenelementen toewijzen.</td>
<td>Als de hoofdrekeningen in uw verschillende rechtspersonen vanwege wettelijk voorgeschreven boekhoudvereisten niet kunnen worden gedeeld, kunt u deze toewijzen nadat u deze hebt geïmporteerd in Kostprijsboekhouding voor een holistisch beeld van de gehele organisatie.</td>
</tr>
<tr class="odd">
<td>Kostenobjectdimensies definiëren en leden van kostenobjectdimensie importeren.</td>
<td>Een kostenobject is een object van een willekeurig type, waarin kosten zijn toegewezen. Veelgebruikte kostenobjecten zijn bijvoorbeeld producten, projecten, bronnen, afdelingen, kostenplaatsen en geografische regio's. U kunt financiële dimensies en waarden op een van twee manieren verkrijgen: door middel van een gegevensconnector in Microsoft Dynamics 365 for Operations worden deze opgehaald bij Operations; of door middel van een algemene gegevensconnector worden via Microsoft Excel hoofdrekeningen opgehaald bij een ander type bronsysteem. Als u bijvoorbeeld de financiële dimensie Kostenplaats gebruikt als de objectdimensie, worden alle geïmporteerde kostenplaatsen de dimensieleden voor het kostenobject.</td>
</tr>
<tr class="even">
<td>Statistische dimensies definiëren of importeren</td>
<td>Statistische dimensieleden worden worden gemeten in niet-monetaire eenheden, zoals machine-uren, aantal werknemers, en vierkanten. Ze worden gebruikt in overzichten of als basis voor toewijzingen en distributies.</td>
</tr>
<tr class="odd">
<td>Sjablonen van providers van statistische maateenheden maken.</td>
<td>Door middel van een sjabloon van een statistische maateenheid worden gegevens uit Dynamics 365 for Operations omgezet in statistische maateenheden. De sjabloon wordt vervolgens gekoppeld aan een bepaald statistisch dimensielid. De sjablonen zijn vooraf gefilterd, zodat ze alleen tabellen weergeven die aan financiële dimensies zijn gekoppeld.</td>
</tr>
<tr class="even">
<td>Grootboeken van kostprijsboekhouding maken.</td>
<td>Een kostprijsboekhoudinggrootboek is een agnostisch grootboek dat zijn eigen kalender en valuta gebruikt. Het speelt een belangrijke rol in de verwerking van alle kostentransacties. Een kostprijsboekhoudinggrootboek classificeert bijvoorbeeld kosten op basis van de eigen kostenelementen en voegt kosten samen op basis van de eigen objectdimensies. U kunt zoveel kostprijsboekhoudinggrootboeken maken als u nodig hebt om rapportages vanuit verschillende gezichtspunten aan te maken.</td>
</tr>
<tr class="odd">
<td>Kostenbeheereenheden maken.</td>
<td>Kostenbeheereenheden vormen de kostenstructuur en definiëren de stroom van kosten in een kostprijsboekhoudinggrootboek. Ze moeten aan kostenobjectdimensies worden gekoppeld om de kostenobjectdimensies in het grootboek te vertegenwoordigen.</td>
</tr>
<tr class="even">
<td>Grootboekvermeldingen verwerken.</td>
<td>Om werkelijke prestaties te kunnen meten, moet u gegevens hebben. De gegevens worden geïmporteerd door middel van de connectors die u voor het kostprijsboekhoudinggrootboek definieert. Wanneer u de grootboekposten verwerkt, worden de gegevens incrementeel geïmporteerd.</td>
</tr>
<tr class="odd">
<td>Budgetregels verwerken.</td>
<td>Om begrote prestaties te kunnen meten, moet u gegevens hebben. De gegevens worden geïmporteerd door middel van de connectors die u voor het kostprijsboekhoudinggrootboek definieert. Wanneer u de budgetregels verwerkt, worden de gegevens incrementeel geïmporteerd.</td>
</tr>
<tr class="even">
<td>Beleid voor kostengedrag maken en toepassen.</td>
<td>Door middel van een beleid voor kostengedrag classificeert u kosten als vast, variabel of semi-variabel. Een beleid is gebaseerd op regels en de ingangsdatum. Standaard worden alle kosten gemarkeerd als ongeclassificeerd, tot u een beleid voor kostengedrag toepast en de gevolgen van de regel berekent. Na de berekening zijn de kosten geclassificeerd.</td>
</tr>
<tr class="odd">
<td>Kosten in de gaten houden.</td>
<td>Om u te helpen het effect van kostenbeleid begrijpen, kunt u met Kostprijsboekhouding kosten terugvolgen naar de bronwaarden en de toegepaste regels waaruit zij ontstaan. Deze functie geeft volledig inzicht in waar de kosten zijn opgetreden, welke typen kosten optreden en welke regels voor kostengedrag zijn toegepast.</td>
</tr>
<tr class="even">
<td>Dimensiehiërarchieën definiëren.</td>
<td>U kunt dimensiehiërarchieën maken ten behoeve van categoriseren of classificeren. U kunt bijvoorbeeld een categorisatiehiërarchie definiëren, die is gebaseerd op een kostenelementdimensie en de leden daarvan. Ook kunt u een classificatiehiërarchie definiëren, die is gebaseerd op een kostenobjectdimensie en de leden daarvan. De rapportagestructuren worden gebruikt in de volgende situaties:
<ul>
<li>U kunt toewijzingen, kostentarieven, en regels voor kostentotalisering.</li>
<li>U geeft overzichten weer door de werkruimte te gebruiken.</li>
<li>U definieert toegang voor weergave van geaggregeerde gegevens.</li>
<li>U geeft gegevens weer in Excel.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Overzichten maken die in het werkgebied kunnen worden weergegeven.</td>
<td>Met het werkgebied kunt u snel een overzicht krijgen van de werkelijke en gebudgetteerde kosten en de afwijkingen. U kunt de gegevens per periode of kostenniveau filteren. Het werkgebied is ontworpen voor managers die voor kostenbeheer verantwoordelijk zijn. Het houdt de regels voor toegang aan, die zijn gedefinieerd voor de dimensiehiërarchieën.</td>
</tr>
<tr class="even">
<td>Rapporten maken met Excel. <strong>Opmerking:</strong> u moet Microsoft Excel 2016 gebruiken.</td>
<td>U kunt kostprijsboekhoudinggegevens rechtstreeks naar Excel exporteren via gegevensentiteiten met Microsoft PivotTable rapporten maken.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Onkostenbeheer

| Wat u kunt doen                                                            | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Creditcardtransacties van vertrokken werknemers opnieuw toewijzen.                     | Soms is de Active Directory Domain Services-account van een vertrokken werknemer al uitgeschakeld, maar worden er nog actieve creditcardtransacties geïmporteerd die moeten worden opgevoerd. Voorheen kon u geen gemachtigde voor onkosteninvoer toewijzen of de creditcardtransacties koppelen aan een onkostennota. Met de pagina **Creditcardtransacties** kunt u nu de werknemer voor een creditcardtransactie opnieuw toewijzen, als de oorspronkelijke werknemer niet meer bij het bedrijf werkt. Nadat u de creditcardtransactie opnieuw hebt toegewezen, kan de transactie voor een onkostennota worden geselecteerd en betaald via het normale proces voor terugbetaling van onkosten. |
| De gegevens voor de onkostencreditcard wijzigen voor aankomende werknemers en oud-medewerkers. | U kunt de creditcardgegevens in Onkostenbeheer wijzigen voor aankomende werknemers en oud-werknemers. Voorheen kon u de informatie van de onkostencreditcard alleen wijzigen als de werknemer een actieve werknemer was.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Een onkostennota kopiëren.                                                    | U kunt een bestaande onkostenpost nu kopiëren, wanneer u een nieuwe onkostenpost aanmaakt op dezelfde onkostennota. U kunt een onkostennota en alle gekoppelde onkosten die niet gerelateerd zijn aan een creditcard kopiëren naar een nieuwe onkostennota. U moet nog wel alle vereiste specificaties uitvoeren en vereiste betalingsbewijzen koppelen, op basis van gedefinieerd beleid en categorieën voor onkosten. U kunt creditcardtransacties toevoegen aan de onkostennota door aan te geven dat u niet-afgestemde onkosten toevoegt.                                                                                                                                                                                                                        |
| Onkosten bulksgewijs bewerken.                                                        | Sommige creditcardtransacties worden mogelijk niet aan een onkostencategorie toegewezen, of ze worden incorrect toegewezen wanneer ze worden geïmporteerd. In dit geval moeten werknemers de gekoppelde onkostencategorie handmatig wijzigen. Als beheerder van niet-afgestemde onkosten kunt u nu onkostencategorie voor de geselecteerde onkosten in bulk bewerken. Als u geselecteerde onkosten voor een specifieke onkostennota beheert, kunt u daarnaast het project en de aanvullende informatie bulksgewijs bewerken.                                                                                                                                                                                    |
| De wisselkoers wijzigen voor creditcardtransacties.                     | De werkelijke wisselkoers die voor een creditcardtransactie is gebruikt, wijkt misschien af van de wisselkoers die in het systeem is ingesteld. Voorheen konden werknemers niet de wisselkoers wijzigen voor een creditcardtransactie die in Onkostenbeheer was geïmporteerd. U kunt nu op de pagina **Parameters onkostenbeheer** een parameter instellen, waardoor de wisselkoers voor creditcardtransacties kan worden gewijzigd.                                                                                                                                                                                                                                            |
| Anti-corruptieattesten instellen voor onkosten.                            | Sommige werknemers van een organisatie onderhouden contacten met overheidsambtenaren. Sommige onkosten bij die contacten ontstaan, zouden kunnen worden beschouwd als omkoping. In Onkostenbeheer kunt u nu een anti-corruptieattest instellen die wordt weergegeven voor geselecteerde onkostencategorieën, zoals maaltijden en geschenken. Werknemers moeten aangeven of onkosten die voor anti-corruptieattesten zijn ingesteld, voldoen aan de criteria die in het beleid van uw organisatie zijn gedefinieerd.                                                                                                                                                                                     |
| Handmatige invoer van onkosten voorkomen voor specifieke onkostencategorieën.          | Een onkostencategorie kan worden ingesteld om een creditcardtransactie te vertegenwoordigen waarvoor de categorie niet kan worden gewijzigd. Een voorbeeld zijn de kosten voor late afbetaling van de creditcard. U kunt nu een onkostencategorie configureren, waarin onkosten alleen door import kunnen worden ingevoerd. Met deze functie kunt u voorkomen dat werknemers een onkostenpost voor de categorie maken. Het voorkomt ook dat de categorie wordt gewijzigd voor transacties die zijn geïmporteerd en die deze categorie gebruiken.                                                                                                                                                                                   |
| Een betalingsbewijs toevoegen aan meerdere onkostenposten.                                     | Een betalingsbewijs dat in Onkostenbeheer is geüpload, kan gerelateerd zijn aan meerdere onkostenposten. Voorheen moest een betalingsbewijs dat aan meerdere onkosten was gerelateerd, voor elke onkostenpost apart worden geüpload. U kunt nu een betalingsbewijs, dat al is geüpload en aan een onkostenpost op dezelfde onkostennota is gekoppeld, aan een andere onkostenpost koppelen. Als u een betalingsbewijs naar de koptekst van de onkostennota hebt geüpload, kunt u daarnaast één of meerdere regels selecteren om aan het betalingsbewijs te koppelen.                                                                                                                                                                                        |
| Onkosten met een datum in de toekomst aanmaken.                                              | Wanneer u bijvoorbeeld een onkostennota kopieert, kan de transactiedatum voor een post een datum in de toekomst hebben. In vroegere versies kunnen onkosten geen datum in de toekomst hebben. U kunt nu onkostenposten maken en opslaan die een datum in de toekomst hebben. U kunt echter geen onkostenpost met een datum in de toekomst indienen.                                                                                                                                                                                                                                                                                                                                                                                 |
| Onkostenbelastingen configureren voor een staat/provincie.                              | In sommige landen/regio's kunnen voor onkosten die in verschillende staten/provincies worden gemaakt, verschillende btw-tarieven gelden. U kunt nu de configuraties van de btw-tarieven voor onkosten instellen op het niveau van staat/provincie, in plaats van alleen op het niveau van land/regio. Als u op de pagina **Belastingconfiguratie** het veld **Staat/provincie** leeg laat, geldt de btw-groep voor alle staten/provincies in het opgegeven land/regio.                                                                                                                                                                                                                                       |
| Typen creditcards voor onkosten instellen.                                          | Voorheen was er geen pagina waar u nieuwe creditcardtypen kon maken, zoals Visa, MasterCard of AMEX, die u in Onkostenbeheer kon gebruiken. U kunt nu creditcardtypen maken die u in Onkostenbeheer wilt gebruiken. U vindt de pagina in het gebied **Instellingen** in de sectie **Berekeningen en codes**.                                                                                                                                                                                                                                                                                                                                                 |
| Een goedkeuringsworkflow voor onkostennota's met meerdere niveaus definiëren.                 | Een nieuwe workflow voor onkostennota's ondersteunt een goedkeuringsproces op meerdere niveaus. Werknemers voeren tussentijdse fiatteurs en definitieve fiatteurs in, wanneer ze een onkostennota maken. De workflow stuurt de onkostennota eerst door naar de interim fiatteurs. Nadat de onkostennota op dat niveau is goedgekeurd, leidt de workflow de nota door naar de definitieve fiatteurs voor definitieve goedkeuring.                                                                                                                                                                                                                                                                                          |
| Onkosten maken en beheren die niet aan een onkostennota zijn gekoppeld.    | Gebruikers kunnen nu onkosten maken en beheren (door bijvoorbeeld betalingsbewijzen te koppelen of te specificeren, of gasten toe te wijzen) zonder dat ze eerst een onkostennota moeten maken. De gebruiker kan een of meer onkostenposten selecteren en aan een nieuwe onkostennota toevoegen, zodat ze kunnen worden ingediend ter goedkeuring. Een nieuwe pagina voor het beheren van onkosten is beschikbaar op **Onkostenbeheer** &gt; **Mijn uitgaven** &gt; **Onkosten**.                                                                                                                                                                                                                                                       |

## <a name="financial-management"></a>Financieel beheer
<table>




<thead>
<tr class="header">
<th>Wat u kunt doen</th>
<th>Waarom dit belangrijk is</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vaste-activawaarderingen traceren met het concept van één 'boek'.</td>
<td>Voorheen werden twee afzonderlijke typen waardering gebruikt om vaste activawaarden bij te houden: waardemodellen en afschrijvingsboeken. In de huidige versie worden deze twee concepten samengevoegd in één waardevaststellingsconcept dat wordt aangeduid als een 'boek'. Boeken bieden alle functionaliteit van de waardemodellen en de afschrijvingsboeken. U kunt bijvoorbeeld het boeken naar het grootboek uitschakelen. Boeken die naar het grootboek boeken, worden doorgaans gebruikt voor financiële rapportage van de onderneming. Boeken die niet naar het grootboek boeken, kunnen worden gebruikt voor belastingaangiftes.</td>
</tr>
<tr class="even">
<td>De jaarafsluiting van het grootboek uitvoeren voor meerdere rechtspersonen.</td>
<td>Om het jaarafsluitingsproces te versnellen, kunt u de jaarafsluiting nu uitvoeren voor meerdere rechtspersonen vanaf een gedeelde pagina voor jaarafsluitingen. U kunt groepen van rechtspersonen definiëren, samen met instellingen die voor alle jaren moeten worden behouden. De bruikbaarheid van het jaarafsluitingsproces is ook op andere punten verbeterd.</td>
</tr>
<tr class="odd">
<td>Profiteren van verbeteringen aan herwaardering van vreemde valuta in het grootboek.</td>
<td>In het grootboekproces zijn de volgende verbeteringen doorgevoerd voor herwaardering van vreemde valuta:
<ul>
<li>Een wisselkoerstype is toegevoegd aan de hoofdrekening. Dit type wisselkoers wordt nu gebruikt om de wisselkoers te bepalen tijdens herwaardering van valuta. Als geen wisselkoerstype is gedefinieerd, blijft het proces het wisselkoerstype gebruiken dat voor het grootboek is gedefinieerd.</li>
<li>Het is nu eenvoudiger om een bereik van hoofdrekeningen en valuta te selecteren waarop u het herwaarderingsproces wilt laten uitvoeren.</li>
<li>De herwaardering kan voor meerdere rechtspersonen worden uitgevoerd.</li>
<li>Het systeem houdt nu een historie bij van alle herwaarderingsprocessen die zijn uitgevoerd, zoals het ook doet voor de herwaarderingsprocessen voor Klanten en Leveranciers.</li>
<li>Wanneer u het proces uitvoert, kunt u nu een voorbeeldweergave oproepen van de resultaten van de herwaardering. In het voorbeeld worden de resultaten voor alle rechtspersonen getoond waarvoor het proces werd uitgevoerd. U kunt dan alle rechtspersonen (of een subset daarvan) boeken vanuit de voorbeeldweergave. U kunt de resultaten in het voorbeeld ook naar Excel exporteren.</li>
</ul></td>
</tr>
<tr class="even">
<td>Transacties weergeven voor aanvullende boekingslagen.</td>
<td>Op de lijstpagina <strong>Proefbalans</strong> en in het rapport <strong>Dimensieoverzicht</strong> kunt u nu de aanvullende boekingslagen selecteren die aan het grootboek zijn toegevoegd. Als u de extra boekingslagen selecteert, worden correcties voor die boekingslagen opgenomen in de saldi op de lijstpagina of in het rapport.</td>
</tr>
<tr class="odd">
<td>Documentatie met instructies koppelen aan de sjabloon voor het afsluiten van financiële periodes.</td>
<td>Voorheen kon u documentatie koppelen nadat een taak was voltooid. U kon bijvoorbeeld een rapport koppelen dat was gegenereerd. U kunt nu ook een document met instructies aan de sjabloon koppelen. Dit document wordt vervolgens gekopieerd naar elke taak in de planning van de financiële periode, zodat de taakeigenaar instructies kan bekijken voor het uitvoeren van de taak.</td>
</tr>
<tr class="even">
<td>De instellingen van de intercompany-boekhouding definiëren vanaf een gedeelde pagina.</td>
<td>De <strong>pagina met de instellingen voor de intercompany-boekhouding</strong> wordt nu gedeeld, zodat een organisatie alle paren van rechtspersonen kan definiëren die transacties met elkaar kunnen uitvoeren. Daarnaast kunt u nu een transactie in de bronrechtspersoon invoeren, maar niet vanuit de doelrechtspersoon. Als beide rechtspersoon een intercompany-transactie in gang kunnen zetten, moet het wederkerige paar worden gedefinieerd. Daarom is de doelrechtspersoon ook geconfigureerd als een bronrechtspersoon.</td>
</tr>
<tr class="odd">
<td>Verantwoordingsdocumenten voor budgetplannen indienen.</td>
<td>U kunt een verantwoordingssjabloon maken ten behoeve van aanvullende documentatie voor de aangevraagde budgetbedragen. Gebruikers kunnen de details van de sjabloon vullen en de sjabloon koppelen aan de budgetplan, zodat het tijdens het goedkeuringsproces kan worden gebruikt.</td>
</tr>
<tr class="even">
<td>Geavanceerde regels voor budgetregisterregels inschakelen.</td>
<td>Als geavanceerde regels zijn geconfigureerd in het grootboek, kunnen die regels worden gebruikt voor nieuwe posten en overboekingen in het budgetregister.</td>
</tr>
<tr class="odd">
<td>Profiteer van verbeterde zichtbaarheid van activiteiten voor vooruitbetalingsfacturering.</td>
<td>De nieuwe lijstpagina <strong>Openstaande vooruitbetalingen</strong> bevat een momentopname van de status van activiteiten voor vooruitbetalingsfacturering. De pagina biedt de boekhoudafdeling informatie over inkooporders met openstaande vooruitbetalingswaarden die moeten worden gefactureerd, gefactureerde waarden die moeten worden betaald, en betaalde factuurwaarden die op standaardfacturen moeten worden toegepast. Daarnaast kunnen boekhoudmedewerkers gegevens efficiënter invoeren, doordat betaalde vooruitbetalingsfacturen nu beter automatisch worden toegepast op standaardfacturen.</td>
</tr>
<tr class="even">
<td>Het werkgebied voor <strong>Leverancierssamenwerkingsfacturen</strong> gebruiken.</td>
<td>Een nieuwe werkruimte <strong>Facturering</strong> in het gebied <strong>Leverancierssamenwerking</strong> geeft externe leveranciers beveiligde toegang tot hun eigen factuurgegevens. Zo kunnen ze bijvoorbeeld zien of een factuur is betaald en hun eigen facturen verzenden. Deze wijziging niveau maakt efficiëntere en snellere communicatie met externe leveranciers mogelijk. Dit stelt de facturerende boekhoudmedewerkers in staat om met minder onderbrekingen door te werken.</td>
</tr>
<tr class="odd">
<td>Wisselen van rechtspersoon tijdens invoeren van facturen.</td>
<td>Facturerende medewerkers die facturen voor verschillende rechtspersonen invoeren, kunnen nu snel op de factureringspagina's overschakelen naar andere rechtspersonen. Deze functie helpt de medewerkers tijd te besparen, omdat ze zich niet meer bij de huidige rechtspersoon hoeven af te melden en daarna bij een andere rechtspersoon aan te melden. Op de pagina's <strong>Algemeen factuurjournaal</strong> en <strong>Leveranciersfacturen</strong> kunnen gebruikers overschakelen naar een andere rechtspersoon terwijl zij gegevens invoeren.</td>
</tr>
<tr class="even">
<td>Ondersteuning voor elektronische bestanden voor het programma voor gecombineerde aangifte voor staat en federale overheid 1099 van de Amerikaanse Internal Revenue Service (IRS)</td>
<td>Wanneer de configuratiesleutel <strong>VS</strong> is ingeschakeld, biedt het elektronische aangifteproces 1099 extra functionaliteit die voldoet aan de IRS-regels voor het gezamenlijke aangifteprogramma. De IRS heeft dit programma opgezet, zodat het ingediende informatie elektronisch kan doorsturen naar de deelnemende staten.</td>
</tr>
<tr class="odd">
<td>Verbeteringen in vereffeningen</td>
<td>Medewerkers die betalingen uitvoeren, kunnen nu bedragen efficiënter vereffenen, omdat ze meerdere niet-geboekte betalingen kunnen vereffenen met dezelfde factuur.</td>
</tr>
<tr class="even">
<td>Overzicht over meerdere bedrijven</td>
<td>Betalingsmedewerkers in een gecentraliseerde organisatie kunnen nu achterstallige facturen bekijken voor meerdere bedrijven. De werkruimten <strong>Leveranciersbetalingen</strong> en <strong>Betalingen van klant</strong> geven nu meer zicht op en controle over achterstallige facturen, doordat gegevens kunnen worden gefilterd en weergegeven voor meerdere bedrijven die deel uitmaken van een gecentraliseerde organisatiehiërarchie voor betalingen.</td>
</tr>
<tr class="odd">
<td>De werkruimte <strong>Bankbeheer</strong> gebruiken.</td>
<td>Met de nieuwe werkruimte <strong>Bankbeheer</strong> kunt u de bankrekeningen en saldi voor uw rechtspersonen volgen. Actuele en uitstaande saldi zijn onmiddellijk beschikbaar voor alle accounts, en u kunt inzoomen vanuit de saldi in de gedetailleerde transactieboekstukken boren. U kunt de historische saldogegevens voor elke bankrekening weergeven, of een samenvatting voor alle bankrekeningen in het bedrijf, in weergaven voor zowel de korte als de lange termijn. U kunt beter inzicht in bankrekeningafstemming krijgen omdat de datum van de laatste afstemming voor elke bankrekening wordt gerapporteerd, en er ook een indicator is voor afstemmingen die nog worden uitgevoerd.</td>
</tr>
<tr class="even">
<td>Elektronische afschriften importeren voor alle rechtspersonen in één stap.</td>
<td>U kunt nu elektronische afschriften importeren voor alle rechtspersonen in één stap. Bankafschriftbestanden kunnen overzichten van veel bankrekeningen en rechtspersonen bevatten, en gezipte bestanden kunnen meerdere bankafschriftbestanden bevatten. Door één importproces te gebruiken, kunt u de afstemming voor alle gerapporteerde bankrekeningen in alle rechtspersonen starten. Deze functie bespaart u tijd, doordat u niet hoeft over te schakelen tussen bedrijven en meerdere afschriftimporten. U kunt vervolgens ook automatisch afstemmingsregels uit laten voeren voor alle geïmporteerde overzichten in elk bedrijf.</td>
</tr>
<tr class="odd">
<td>Waardevaststellingen volgen</td>
<td>Een vast activum kan meerdere waardevaststellingen hebben voor verschillende boekhoudingsnormen en kan optioneel de bijbehorende transacties naar het grootboek boeken. Voorheen werden deze waardevaststellingen gevolgd door middel van waardemodellen of afschrijvingsboeken. U kunt deze waardevaststellingen (die nu worden aangeduid als 'boeken') door middel van een gemeenschappelijke set van journalen, query's en rapporten. Deze samenvoeging van functies vereenvoudigt implementatie en vermindert het aantal interfaces dat de periodieke processen vereisen.</td>
</tr>
<tr class="even">
<td>Profiteren van verbeteringen voor afschrijvingsruns voor meerdere bedrijven.</td>
<td>U kunt nu een afschrijvingsrun starten voor activa in alle rechtspersonen vanaf een enkele pagina. U kunt de journalen ook automatisch boeken nadat ze zijn gemaakt. U kunt het maken en boeken van de journalen naar een batchgewijze verwerking zenden, zodat de afschrijvingsrun in de achtergrond wordt uitgevoerd. Deze verbeteringen reduceren inefficiënties, omdat u niet afzonderlijke afschrijvingsruns voor elk bedrijf apart hoeft te starten. De verbeteringen maken ook beter gecentraliseerd beheer van uw vaste activa mogelijk.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Human Capital-beheer

| Wat u kunt doen                                                                                | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Een prestatiejournaal maken.                                                                  | Voordat u uw beoordeling afrondt, verzamelt u vaak informatie over activiteiten of gebeurtenissen die hebben bijgedragen aan uw succes als werknemer tijdens de beoordelingsperiode. U kunt een regel aan uw prestatiejournaal toevoegen om die activiteiten en gebeurtenissen te documenteren. U kunt deze activiteiten en gebeurtenissen ook aan een doelstelling of een prestatiebeoordeling koppelen, zodat de beoordelaar meer informatie tot zijn beschikking heeft.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Meer gedetailleerde doelstellingen maken.                                                                    | U hebt nu meer controle over de inhoud van de doelstellingen die u formuleert. U kunt metinge aanmaken voor de doelstellingen, regels uit uw prestatiejournaal aan de metingen koppelen en documenten toevoegen en weergeven. U kunt doelstellingen opslaan als sjablonen en deze opnieuw gebruiken om snel nieuwe doelstellingen aan te maken.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Meer gedetailleerde prestatiebeoordelingen aanmaken.                                                      | Prestatiebeoordelingen, die formeel discussies worden genoemd, zijn nu flexibel genoeg om zowel doorlopende feedback als meer formele beoordelingen te ondersteunen. U kunt in actieve doelstellingen invoegen en opmerkingen over deze boeken, en secties toevoegen voor een beoordeling van uw competenties. Aanvullende secties zijn beschikbaar, waarin u metingen, prestatiejournaalitems, bijlagen, en signoffs kunt toevoegen of bekijken die gerelateerd zijn aan de beoordeling.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Extra positiehiërarchieën koppelen aan workflows.                                      | U kunt een workflow koppelen aan een positiehiërarchie. U kunt de workflowstappen ook wijzigen om het goedkeuringsproces te optimaliseren, zodat het voldoet aan de behoeften in uw bedrijf. Daarom kunt u een specifieke goedkeuringstructuur definiëren die aansluit op de verschillende relaties voor rapportage die uw organisatie gebruikt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Workflowondersteuning voor het invoeren van pincodes (PIN's) in werknemerselfservice. | De workflowmogelijkheden Human Resources (HR) zijn uitgebreid en bieden nu ondersteuning voor PIN's. Werknemers kunnen hun PIN toevoegen en bewerken om de efficiëntie te verbeteren. De HR-werknemers kunnen echter controleren of deze informatie nauwkeurig en volledig is, voordat ze deze toevoegen aan de record van de werknemer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Doelstellingsjablonen maken en gebruiken om nieuwe doelen toe te voegen.                                          | U kunt doelstellingsjablonen maken voor doelstellingen die door veel werknemers in het bedrijf worden gedeeld. Werknemers kunnen hun eigen doelstellingen toevoegen op basis van een sjabloon, managers kunnen doelstellingen voor hun team toevoegen op basis van een sjabloon en HR-teamleden kunnen doelstellingen toevoegen voor werknemers in het hele bedrijf.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Doelstellingsgroepen maken en gebruiken om nieuwe doelen toe te voegen.                                             | U kunt doelstellingsjablonen toevoegen aan een groep en door middel van de groep een of meer doelen maken voor een werknemer, een team, een functie, een afdeling of het bedrijf.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Meer controle uitoefenen op het beoordelingsproces.                                                     | U kunt door middel van een workflow het beoordelingsproces aansturen. U kunt beoordelingsjablonen maken en deze gebruiken om beoordelingen te maken. U kunt ook waarderingen toevoegen aan een beoordeling.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Door middel van beoordelingsperioden het tijdsbestek voor de beoordeling bepalen.                                    | U kunt een tijdsperiode voor een prestatiebeoordeling definiëren, waarbij de begin- en einddatums van de beoordeling automatisch worden ingevoerd. U kunt deze standaarddatums echter waar nodig aanpassen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Toegang tot vijf nieuwe Power BI-inhoudpakketten voor Human resources                                     | Met de nieuwe inhoudpakketten kunnen HR-organisaties en HR-managers de volgende zaken analyseren: Metrische personeelsgegevens • Demografische analyses op leeftijd, geslacht en huwelijkse status • Verloop jaar-op-jaar vergelijken en lijsten bekijken met redenen die werknemers hebben gegeven voor hun ontslag • Een lijst met vacatures zien, evenals een vergelijking van openstaande en vervulde vacatures Compensatie en vergoedingen • Werknemers met uurloon en vast salaris vergelijken • Het aantal werknemers weergeven dat is ingeschreven voor beschikbare vergoedingen • Werknemers weergeven op type dienstverband Werving • Sollicitanten analyseren op basis van het aantal sollicitanten, herkomst en op welke functies zij solliciteren Organisatietraining • Trainingsaanmeldingen op locatie • Trainingsdeelname op status • Lijst van werknemers die zijn aangemeld voor traningen Competenties en ontwikkeling van werknemer • Lijst met vaardigheden die werknemers bezitten • Analyse van vaardigheidstypen op teamlid |

## <a name="localizations"></a>Lokalisaties
<table>




<thead>
<tr class="header">
<th>Wat u kunt doen</th>
<th>Waarom dit belangrijk is</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lokalisaties zijn beschikbaar voor 18 extra landen:
<ul>
<li>Oostenrijk</li>
<li>België</li>
<li>Brazilië</li>
<li>China</li>
<li>Tsjechische Republiek</li>
<li>Estland</li>
<li>Finland</li>
<li>Hongarije</li>
<li>Italië</li>
<li>Letland</li>
<li>Litouwen</li>
<li>Noorwegen</li>
<li>Polen</li>
<li>Saudi-Arabië</li>
<li>Spanje</li>
<li>Zweden</li>
<li>Zwitserland</li>
<li>Thailand</li>
</ul>
De volgende landen vereisen ook de lokalisatie voor Retail. De Retail-lokalisatie voor deze landen is nog niet afgerond en staat gepland voor H1 CY2017:
<ul>
<li>Brazilië</li>
<li>Tsjechische Republiek</li>
<li>Estland</li>
<li>Hongarije</li>
<li>Letland</li>
<li>Litouwen</li>
<li>Maleisië</li>
<li>Polen</li>
<li>Zweden</li>
</ul></td>
<td>Dynamics 365 voor Operations is beschikbaar in 18 extra landen. In het kader van onze inzet om lokalisatie gemakkelijker en meer configureerbaar te maken, zijn de functies voor wettelijke elektronische rapportage geconverteerd naar ER-configuraties (Electronic Reporting). Ook zijn enkele wettelijk verplichte Microsoft SQL Server Reporting Services-rapporten (SSRS-rapporten) geconverteerd naar ER-configuraties op basis van Excel-sjablonen. Deze geconverteerde functies worden specifiek vermeld verderop in deze tabel.</td>
</tr>
<tr class="even">
<td>Japan: vaste activa groeperen wanneer u formulier 26 en de toegevoegde tabellen afdrukt.</td>
<td>Formulier 26 moet worden ingediend in elke plaats waarin het bedrijf actief is. Om het formulier 26 eenvoudiger te kunnen afdrukken, kunnen vaste activa automatisch worden gegroepeerd en gesorteerd op locatie.</td>
</tr>
<tr class="odd">
<td>Japan: de bedragen voor versnelde en aanvullende afschrijving op het profiel weergeven.</td>
<td>Het profiel kan een exacte raming geven van de bedragen voor versnelde en aanvullende afschrijving.</td>
</tr>
<tr class="even">
<td>Japan: bronbelasting progressief berekenen.</td>
<td>De Japanse overheid vereist dat u bronbelasting progressief berekent, op basis van de betalingsbedragen.</td>
</tr>
<tr class="odd">
<td>Japan: het postcodebestand importeren voor specifieke grote ondernemingsgebouwen.</td>
<td>Het postcodebestand dat de autoriteiten leveren voor specifieke grote ondernemingsgebouwen kan in het systeem worden geïmporteerd. Adressen kunnen vervolgens uit de postcodes worden afgeleid.</td>
</tr>
<tr class="even">
<td>Japan: een inactieve periode configureren voor vaste activa.</td>
<td>Door middel van inactieve perioden kan de gebruiker de afschrijving van een vast activum stilzetten gedurende een bepaalde periode. Deze functionaliteit wordt vereist door de autoriteiten.</td>
</tr>
<tr class="odd">
<td>Europa: een btw-registratienummer configureren voor het adres van een partij door middel van het Registratie-id-framework.</td>
<td>U kunt een btw-registratienummer voor het adres van een partij configureren door middel van het Registratie-id-framework en de nieuwe registratiecategorie te <strong>Btw-id</strong>.</td>
</tr>
<tr class="even">
<td>Finland: een klantnummer voor douanezaken configureren voor het adres van een partij door middel van het Registratie-id-framework.</td>
<td>U kunt een klantnummer voor douanezaken voor het adres van een partij configureren door middel van het Registratie-id-framework en de nieuwe registratiecategorie te <strong>Klant-id van de douane</strong>.</td>
</tr>
<tr class="odd">
<td>Frankrijk: klantfacturen afdrukken in een specifiek Franse indeling.</td>
<td>Het afdrukken van klantfacturen is aangepast om te voldoek aan vereisten die specifiek zijn voor Frankrijk.</td>
</tr>
<tr class="even">
<td>Frankrijk: chronologische nummering van documenten op boekperiode afdwingen.</td>
<td>Om te voldoen aan voor Frankrijk specifieke vereisten voor het nummeren van klantfacturen kunt u nummerreeksen instellen voor klantfacturen per boekperiode.</td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Oostenrijk: ER-configuraties</td>
<td><ul>
<li>XML-indeling voor de ICL-lijst voor Oostenrijk</li>
<li>Intrastat-indeling voor Oostenrijk</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Oostenrijk</li>
<li>Indeling voor automatische ISO20022-afschrijving voor Oostenrijk</li>
<li>Edifact-PAYMUL-indeling voor Oostenrijk</li>
<li>Btw-aangifte voor Oostenrijk</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor België: ER-configuraties</td>
<td><ul>
<li>BLWI-indeling voor België</li>
<li>XML-indeling voor de ICL-lijst voor België</li>
<li>Rapport vaste activa voor België</li>
<li>Intervat-indeling voor België</li>
<li>Intrastat-indeling voor België</li>
<li>Rapport factuuromzet voor België</li>
<li>Exportindeling voor grootboektransactie voor België</li>
<li>SWIFT-indeling voor leveranciersbetalingen voor België</li>
<li>CODA-importindeling voor bankafschriften voor België</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor België</li>
<li>Indeling voor automatische ISO20022-afschrijving voor België</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Brazilië: ER-configuraties</td>
<td><ul>
<li>GIA-SP voor Brazilië</li>
<li>GIA-ST voor Brazilië</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor Tsjechische Republiek: ER-configuraties</td>
<td><ul>
<li>XML-indeling voor ICL-lijst voor Tsjechische Republiek</li>
<li>Intrastat-indeling voor Tsjechische Republiek</li>
<li>Btw-aangifte voor Tsjechische Republiek</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lokalisatie voor China: ER-configuraties</td>
<td><ul>
<li>Indeling van naar ouderdom gerangschikt rapport voor klanten voor China</li>
<li>Indeling voor analyserapport voor uitstaande klantenbedragen voor China</li>
<li>Indeling van naar ouderdom gerangschikt rapport voor leveranciers voor China</li>
<li>Indeling voor analyserapport voor uitstaande leveranciersbedragen voor China</li>
<li>Indeling voor naar ouderdom gerangschikte analyse van te ontvangen betalingen voor China</li>
<li>Indeling van rapport voor klantsaldi voor China</li>
<li>Indeling van grootboeksaldorapport voor China</li>
<li>Indeling van rapport voor leverancierssaldi voor China</li>
<li>GBT-bestand voor China</li>
<li>Indeling voor Golden tax-exportbestand</li>
<li>Indeling voor rapport over verbruiksafwijkingen bij productie voor China</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor Estland: ER-configuraties</td>
<td><ul>
<li>XML-indeling voor de ICL-lijst voor Estland</li>
<li>Intrastat-indeling voor Estland</li>
<li>Overzicht van voorraadherclassificatie voor Estland</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Estland</li>
<li>Rapport saldomelding klant/verkoper voor Estland</li>
<li>Btw-aangifte voor Estland</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Finland: ER-configuraties</td>
<td><ul>
<li>TXT-indeling van EU-verkooplijst voor Finland</li>
<li>Intrastat-indeling voor Finland</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Finland</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor Hongarije: ER-configuraties</td>
<td><ul>
<li>XML-indeling voor de ICL-lijst voor Hongarije</li>
<li>Intrastat-indeling voor Hongarije</li>
<li>Vereenvoudigde Intrastat-indeling voor Hongarije</li>
<li>Exportindeling voor facturenlijst voor Hongarije</li>
<li>Btw-aangifte voor Hongarije</li>
<li>Gespecificeerde btw-aangifte voor Hongarije</li>
<li>Voorraadafschrift voor Hongarije</li>
<li>Indeling voor MultiCash-betalingen voor Hongarije</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Italië: ER-configuraties</td>
<td><ul>
<li>Intrastat-indeling voor Italië</li>
<li>Indeling voor projectfacturen voor Italië</li>
<li>Indeling voor verkoopfacturen voor Italië</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Italië</li>
<li>Indeling voor automatische ISO20022-afschrijving voor Italië</li>
<li>Indeling voor RIBA-incassoremise voor Italië</li>
<li>Rapport voor binnenlandse btw-transacties voor Italië</li>
<li>Zwarte-lijstrapport voor Italië</li>
<li>Modello770-rapport voor Italië</li>
<li>Rapport jaarlijkse belastingaangifte voor Italië</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor Letland: ER-configuraties</td>
<td><ul>
<li>Gebruiksrapport van kasontvangsten voor Letland</li>
<li>XML-indeling van EU-verkooplijst voor Letland</li>
<li>XML-indeling van correcties op EU-verkooplijst voor Letland</li>
<li>Intrastat (A)-indeling voor Estland</li>
<li>Intrastat (B)-indeling voor Estland</li>
<li>Voorraadtellinglijst voor Letland</li>
<li>Voorraadtellingoverzicht voor Letland</li>
<li>Voorraadmutatie voor Letland</li>
<li>Afleveringsbewijs van interne overboeking voor Letland</li>
<li>Document voor voorraadherclassificatie voor Letland</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Letland</li>
<li>Btw-aangifte voor Letland</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Litouwen: ER-configuraties</td>
<td><ul>
<li>XML-indeling voor de ICL-lijst voor Litouwen</li>
<li>Intrastat (B)-indeling voor Litouwen</li>
<li>Voorraadafschrift voor Litouwen</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Litouwen</li>
<li>Rapport inter-afstemming klant/leverancier voor Litouwen</li>
<li>Btw-aangifte voor Litouwen</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor Noorwegen: ER-configuraties</td>
<td><ul>
<li>Indeling voor aanmaningsbrieven voor Noorwegen</li>
<li>Indeling voor AutoGiro-betalingen voor Noorwegen</li>
<li>Indeling voor AvtaleGiro-klantbetalingen voor Noorwegen</li>
<li>Indeling voor eFaktura-klantbetalingen voor Noorwegen</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Noorwegen</li>
<li>Indeling voor NETS-betalingen voor Noorwegen</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Polen: ER-configuraties</td>
<td><ul>
<li>Intrastat-indeling voor Polen</li>
<li>Magazijndocumenten voor Polen</li>
<li>Document voor voorraadherclassificatie voor Polen</li>
<li>Indeling voor MultiCash-betalingen voor Polen</li>
<li>Indeling voor buitenlandse MultiCash-betalingen voor Polen</li>
<li>Rapport saldobevestiging klant/verkoper voor Polen</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor Saoedi-Arabië: ER-configuraties</td>
<td>Indeling voor toewijzing diverse toeslagen voor kredietbrief van bank voor Saoedi-Arabië</td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Spanje: ER-configuraties</td>
<td><ul>
<li>TXT-indeling van EU-verkooplijst voor Spanje</li>
<li>Intrastat-indeling voor Spanje</li>
<li>Indeling voor projectfacturen voor Spanje</li>
<li>Indeling voor verkoopfacturen voor Spanje</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Spanje</li>
<li>Indeling voor automatische ISO20022-afschrijving voor Spanje</li>
<li>Indeling voor btw-registerboek voor Spanje</li>
<li>Indeling voor btw-registerboekoverzicht voor Spanje</li>
<li>347-aangifte exporteren naar ASCII voor Spanje</li>
<li>Rapport van 347-aangifte voor Spanje</li>
</ul></td>
</tr>
<tr class="even">
<td>Lokalisatie voor Zweden: ER-configuraties</td>
<td><ul>
<li>Intrastat-indeling voor Zweden</li>
<li>Indeling voor Bankgirot Autogiro-klantbetalingen voor Zweden</li>
<li>Indeling van Bankgirot-leveranciersbetalingen voor Zweden</li>
<li>SWIFT-indeling voor leveranciersbetalingen voor Zweden</li>
<li>SIE-exportindeling voor Zweden</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Zweden</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lokalisatie voor Zwitserland: ER-configuraties</td>
<td><ul>
<li>Indeling voor DebitDirect-betalingen voor Zwitserland</li>
<li>Indeling voor automatische LSV-afschrijvingen voor Zwitserland</li>
<li>ISO20022-indeling voor kredietoverdrachtbetalingen voor Zwitserland</li>
<li>Indeling voor automatische ISO20022-afschrijving voor Zwitserland</li>
<li>ESR-importindeling voor bankafschriften voor Zwitserland</li>
</ul></td>
</tr>
<tr class="even">
<td>Duitsland: betalingen aan leveranciers in DTAZV-indeling exporteren</td>
<td>Duitsland vereist DTAZV met vreemde opmaakspecificatie, wat staat voor een overboekingsbericht (leveranciersbetaling) volgens de specificatie voor grensoverschrijdende betalingen vanuit Duitsland naar een rekening bij een buitenlandse bank of naar een binnenlandse bank in een vreemde valuta. 
</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektronische rapportage

| Wat u kunt doen                                                                                                                                                                                                                                                                                     | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ER-rapporten configureren om gegevens in verschillende indelingen vanuit de opslag van Documentbeheer in te voegen in elektronische berichten die worden gegenereerd.                                                                                                                                                              | ER-rapporten kunnen gegevens invoegen in elektronische berichten die worden gegenereerd vanuit de opslag van Documentbeheer. U kunt bijvoorbeeld een zakelijk document toevoegen als bijlage aan elektronische berichten die voor dat document worden gegenereerd, in overeenstemming met wettelijke vereisten. Momenteel kunnen deze bijlagen in MIME-indeling worden toegevoegd aan een XML-bericht dat wordt gegenereerd. Eventueel kunnen de bijlagen in Base64-indeling worden toegevoegd aan een binair bericht dat wordt gegenereerd.                                                                      |
| ER-rapporten configureren voor het genereren van elektronische documenten in Excel-, Microsoft Word- of PDF-indeling.                                                                                                                                                                                                      | Met één configuratie kunnen ER-rapporten elektronische documenten genereren in drie verschillende indelingen: OpenXML-werkblad (Excel), Word en XML Forms Data Format (XFDF, PDF). Gebruikers kunnen een indeling selecteren door een indelingssjabloon toe te voegen aan een ER-rapport als een Excel-, Word-, of PDF-document.                                                                                                                                                                                                                                                                       |
| ER-rapporten configureren voor het invoegen van gegevens in kop- en -voetteksten van elektronische documenten die in OpenXML-werkbladindeling worden gegenereerd en voor het controleren van pagina-einden.                                                                                                                               | ER-rapporten kunnen zakelijke gegevens invoegen in paginakopteksten en -voetteksten en ook bepalen waar pagina-einden worden geplaatst. Zo kunnen de rapporten de statische secties ondersteunen boven- en onderaan pagina's van elektronische documenten die worden gegenereerd. Ze kunnen ook specifieke paginering van documenten ondersteunen, zodat deze voldoen aan wettelijke vereisten.                                                                                                                                                                                                             |
| De bestemming van ER-rapporten configureren, zodat de uitvoer als e-mail wordt verzonden en zakelijke gegevens en ER-logica (expressies) kunnen worden gebruikt om tijdens uitvoeringstijd aan te geven welk e-mailadres wordt gebruikt.                                                                                                    | Voorheen kon u bij het configureren van een ER-bestemming het e-mailadres van de ontvanger definiëren tijdens het ontwerpen. U kunt nu een expressie in de ER-indeling configureren. Deze expressie kan vervolgens in een bestemming apart worden geselecteerd als de bron van het e-mailadres voor elke indelingsconfiguratie en elke uitvoercomponent (map of bestand). Zo kan bij het uitvoeren van een ER-rapport elk gegenereerde bestand naar een andere ontvanger worden verzonden, en het e-mailadres kan worden gedefinieerd op basis van ER-logica en zakelijke gegevens. |
| De bestemming van ER-rapporten configureren, zodat de uitvoer wordt verzonden naar de Microsoft SharePoint-map als een nieuw, benoemd bestand of een nieuwe versie van het bestaande bestand, en zodat de bedrijfsgegevens kunnen worden gebruikt in het Microsoft Power BI-framework als een gegevensset of als een rapport.                 | Wanneer u ER-rapporten configureert, kunt u nu eenvoudig (zonder code te gebruiken) de vereiste zakelijke gegevens voorbereiden, zodat deze door het Power BI-framework kunnen worden gebruikt. Wanneer u deze ER-rapporten uitvoert, kunt u de juiste, reeds beschikbare bedrijfsgegevens en/of Excel-rapporten leveren aan het Power BI-framework. Als u het rapport instelt voor periodieke uitvoering, kunt u de geplande push van bedrijfsgegevens vanuit Dynamics 365 for Operations laten aansluiten op de updateplanning van de op Power BI gebaseerde rapporten.                             |
| ER-rapporten configureren om een reeds gegenereerd deel van een elektronisch document te gebruiken als gegevensbron voor de rest van het document.                                                                                                                                             | U kunt de ER-rapporten configureren die de uitvoer in tekstindeling aanmaken om het aantal regels in het document te tellen. Deze informatie kan vervolgens in andere delen van het document worden gebruikt om regels te maken die samenvattingsdetails geven. De samenvattingsinformatie (totalen en getallen) kan worden berekend en uitgevoerd naar de elektronische documenten die worden gegenereerd zonder dat de gegevens nog een keer moeten worden omgezet. Deze functie helpt zo de prestaties van de rapportuitvoering te verbeteren en vereenvoudigt toekomstig onderhoud van de geconfigureerde ER-indeling.    |
| ER-rapporten configureren om de bestandsnaamextensie op te geven voor elektronische documenten die in tekstindeling worden gegenereerd.                                                                                                                                                                                 | U kunt ER-rapporten configureren om de uitvoer in tekstindeling te maken, zodat dit kan worden opgeslagen als een bestand met een specifieke extensie. Naast de standaardextensie .txt kunt u extensies zoals .csv en .prn configureren volgens de indelingsspecificaties.                                                                                                                                                                                                                                                                             |
| Nieuwe ER-rapporten maken die zijn gebaseerd op een specifieke versie van een ER-model.                                                                                                                                                                                                                          | Voorheen kon u bij het aanmaken van een nieuwe ER-indeling alleen de meest recente versie van het geselecteerde ER-model gebruiken als de gegevensbronlocatie van de indeling. U kunt nu elke beschikbare versie van het geselecteerde ER-model selecteren. Met deze functie kunt u ER-rapporten voor het huidige jaar aanhouden en daarnaast al een nieuwe versie van het ER-model voor het volgende jaar ontwerpen.                                                                                                                                                                                          |
| Gegevensbronnen en indelingen/modellen doorzoeken op tekst of een geselecteerd artefact met één klik. Proactief rebaseconflicten en conflicten tussen configuraties oplossen. ER-rapporten configureren om meerdere validatieberichten te maken voor fouten die worden vastgesteld, totdat de rapportuitvoering wordt beëindigd. | Dankzij diverse verbeteringen in de gebruikerservaring in het ER-framework kunnen gebruikers efficiënter en gemakkelijker met ER werken.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| De werkruimte **ER** weergeven in Power BI-rapporten.                                                                                                                                                                                                                                                      | Gebruikers kunnen de pagina **ER-werkruimte** configureren, zodat deze nieuwe menuopdrachten en live-tegels bevat die de op Power BI gebaseerde rapporten uitvoeren.                                                                                                                                                                                                                                                                                                                                                                                                                       |

## <a name="payroll"></a>Salaris
<table>




<thead>
<tr class="header">
<th>Wat u kunt doen</th>
<th>Waarom dit belangrijk is</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Salarisrecords configureren en salarissen verwerken met functionaliteit die gelijkwaardig is aan de functionaliteit van de module <strong>Salaris</strong> in Microsoft Dynamics AX 2012 R3.</td>
<td>U kunt nu salarissen voor de VS configureren en verwerken met een functie die gelijkwaardig is aan de functionaliteit in AX 2012 R3.
<ul>
<li>U kunt betalingscycli en salarisperioden weergeven, evenals werkcycli en werkperioden, inkomstencodes en inkomstencodegroepen, planningen, verloftypen en vergoedingstoerekeningsplannen.</li>
<li>U kunt ook verplichte inhoudingen instellen voor vergoedingen en belastingen en salarisinformatie vastleggen voor functies en medewerkers ten behoeve van rapportage en analyse.</li>
<li>U kunt ook inhoudingen instellen en beheren voor beslagleggingen en belastingheffingen en voor alle bijbehorenden administratiekosten.</li>
</ul></td>
</tr>
<tr class="even">
<td>Uw proces voor salarisperioden volgen en verwerken door middel van de nieuwe werkruimte <strong>Beheer van salarisadministratie</strong>.</td>
<td>U kunt nu uw salarisverwerking eenvoudig bewaken. In één oogopslag kunnen salarisadministrateurs inkomsten- en betalingsoverzichten zien die aandacht behoeven, zodat de betalingsrun volledig en juist wordt uitgevoerd. In de werkruimte <strong>Beheer van salarisadministratie</strong> kunnen gebruikers de processen van begin tot eind in één werkruimte volgen en uitvoeren.</td>
</tr>
<tr class="odd">
<td>Positieve betalingsbestanden genereren voor salarisbetalingscontroles.</td>
<td>Aan de functionaliteit voor positieve betalingen in de module Contanten en bankbeheer is een nieuwe functie voor salarisbetalingen toegevoegd. In het gehele kernproces zijn afzonderlijke menuopdrachten toegevoegd, zodat het mogelijk is om losstaande configuraties in te stellen die specifiek zijn voor salarisadministratie. De functionaliteit is identiek aan de kernfunctie voor positieve betalingen, die werd uitgebracht met versie 7.0.1 van Microsoft Dynamics AX (mei 2016). Dankzij deze toevoeging zijn de salarisgegevens volledig geïsoleerd van overige positieve-betalingstransacties. Deze isolatie borgt dat alleen gebruikers met salarisadministratietaken gegevens kunnen openen en zien die aan salarisadministratie zijn gerelateerd.</td>
</tr>
<tr class="even">
<td>Inkomstenoverzichtregels importeren uit een externe bron door middel van de nieuwe gegevensentiteit Inkomstenoverzichtregels.</td>
<td>Een belangrijke nieuwe gegevensentiteit maakt integratie met externe systemen voor berekening van tijd en inkomsten mogelijk. De gegevensentiteit importeert regels van inkomensoverzichten en voert dezelfde standaardlogica uit die de gebruiker rechtstreeks op het inkomstenoverzicht heeft ingevoerd. Na de import worden de regels automatisch gekoppeld aan het juiste inkomensoverzichtdocument. Als een bijbehorend inkomensoverzichtdocument niet bestaat, wordt automatisch een document gemaakt.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Plannen en planning

| Wat u kunt doen                                                                                                                                                                                                      | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| De standaardorderinstellingen voor in- en verkopen configureren, op basis van alle actieve productdimensies van het productmodel. U kunt standaardorderinstellingen definiéren voor de voorraadeenheid (SKU) of een gedeeltelijke SKU. | U kunt standaardorderinstellingen opgeven die gelden voor één productdimensie of voor een combinatie van productdimensies. **Voorbeeld** U verkoopt een product dat Polo-t-shirt wordt genoemd. Dit product is beschikbaar in twee kleuren: groen en blauw. Het is ook beschikbaar in twee maten: Small en Medium. Kleur en maat zijn actieve productdimensies voor Polo-t-shirt. U kunt de inkoop van alle groene polo-shirts blokkeren, ongeacht van welke maat. |

## <a name="product-master-data"></a>Producthoofdgegevens
<table>




<thead>
<tr class="header">
<th>Wat u kunt doen</th>
<th>Waarom dit belangrijk is</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alle standaardorderinstellingen en locatiespecifieke orderinstellingen tegelijk configureren, op één pagina.</td>
<td>Deze functie biedt een beter overzicht van artikelinstellingen.</td>
</tr>
<tr class="even">
<td>Een nomenclatuur maken voor productvariantnummers.</td>
<td>U kunt in uw productvariantnummer elementen opnemen zoals productdimensies, kenmerken en tekens. Wanneer u een verkooporder of een inkooporder maakt, kunt u de specifieke productvariant snel vinden.</td>
</tr>
<tr class="odd">
<td>Zoeken naar producten en productvarianten in verkoop- en inkoopscenario's.</td>
<td>Wanneer u een verkooporderregel of een inkoopregel maakt, kunt u producten zoeken door middel van productdimensies en alle productnummers, met uitzondering van Global Trade Item Numbers (GTIN's) en streepjescodes. Dit is een zoekopdracht in volledige tekst, die de bestaande zoekopdracht "Begint met" vervangt die in de zoeklijst voor verkopen en inkopen wordt gebruikt. Met deze functie kunt u productgroepen vinden die soortgelijke eigenschappen hebben, of één product dat unieke kenmerken heeft. Als u deze functie wilt inschakelen, selecteert u de parameter <strong>Zoekveld inschakelen om producten te zoeken</strong> op de pagina <strong>Zoekparameters</strong> in.</td>
</tr>
<tr class="even">
<td>De productvariant rechtstreeks opgeven wanneer u een verkoop- of inkooptransactie maakt. Ook kunt u een selectie maken in een lijst met geldige dimensiecombinaties.</td>
<td>Deze functie dient om de productiviteit te verbeteren. <strong>Voorbeeld</strong> Voorbeeld U verkoopt een product dat Polo-t-shirt wordt genoemd. Dit product is beschikbaar in twee kleuren: groen en blauw. Het is ook beschikbaar in twee maten: Small en Medium. Kleur en maat zijn actieve productdimensies voor Polo-t-shirt. Wanneer u een verkooporderregel invoert voor Polo-t-shirt met de kleur Groen en de maat Small, hoeft u geen gegevens in te voeren in de velden <strong>Artikelnummer</strong>, <strong>Kleur</strong> en <strong>Maat</strong>. U kunt de regel aanmaken via een van de volgende stappen:
<ul>
<li>Voer in het veld <strong>Artikelnummer</strong> het nummer van de productvariant, de naam van de kleur of de maat in. Zoek in de opzoeklijst de specifieke variant die u wilt verkopen en maak de verkooporderregel aan.</li>
<li>Voer het artikelnummer in in het veld <strong>Artikelnummer</strong>. Ga naar een van de productdimensievelden. In de opzoeklijst <strong>Productdimensie</strong> ziet u alle vrijgegeven dimensies die van toepassing zijn op Polo-t-shirt. In één stap kunt u de productvariant selecteren die u wilt verkopen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Opgeven of productnummers op transactiepagina's worden weergegeven.</td>
<td>De transactiepagina's, zoals die voor verkooporders en inkooporders, geven alleen de velden <strong>Artikelnummer</strong> en <strong>Productnaam</strong> weer. Als u het veld <strong>Productnummer</strong> wilt zien, selecteert u de parameter <strong>Productnummers weergeven op formulieren</strong> onder <strong>Parameters productgegevensbeheer</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Projectbeheer en boekhouding

| Wat u kunt doen                                                                                                           | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| De optie 'Later selecteren' wanneer u factuurvoorstellen batchgewijs boekt.                                                            | Projectaccountants kunnen een batchtaak instellen, waarmee automatisch factuurvoorstellen worden opgepakt om te boeken, als deze voldoen aan criteria die in de batchtaak zijn opgegeven. Deze functie verbetert het automatisch boeken van facturen, omdat de batchtaak doorlopend kan worden uitgevoerd en automatisch voorstellen oppakt om te boeken. |
| Analyses maken op het Power BI-bureaublad.                                                                                     | Op het Power BI-bureaublad kunt u eenvoudig Business Intelligence-inhoud (BI-inhoud) maken voor project- en resourcegerelateerde gegevens.                                                                                                                                                                                                       |
| Vooruitbetalingen voor inkooporders gebruiken en deze op de juiste wijze opnemen in het proces voor projectramingen.                               | Voor projectinkooporders moeten de vooruitbetalingen worden verwerkt voordat een deel van de betaling kan worden vrijgegeven aan leveranciers. Deze vooruitbetalingsfacturen worden nu weergegeven in het proces voor projectraming/herkenning voor projecten van het type **Vaste prijs**.                                                                                           |
| Kosten- en opbrengstramingen en artikelbehoeften oproepen en beheren, rechtstreeks vanuit een taak voor een structuur voor werkspecificatie (WBS). | U kunt kostenramingen, opbrengstramingen en artikelbehoeften voor een specifieke WBS-taak beheren in het detaildialoogvenster voor die taak in de WBS-planningsweergave.                                                                                                                                                                 |
| Een financieringsbron uitkiezen in bijzondere-kostenjournalen.                                                                                    | Als het contract voor een project meerdere financieringsbronnen bevat, kunt u een specifieke financieringsbron selecteren wanneer kosten worden geboekt. Als u geen specifieke financieringsbron selecteert, worden de kosten toegewezen op basis van de financieringsregels die in het contract zijn gespecificeerd.                                                                   |
| Projectoverzichten openen in Excel.                                                                                         | Nieuwe gegevensentiteiten voor grootboek- en budgetupdates stellen u in staat projectoverzichtgegevens in Excel te openen en analyses te maken met behulp van Excel-functionaliteit.                                                                                                                                                                           |
| Met slechts één configuratiesleutel functionaliteit voor Projectbeheer en boekhouding (PMA) inschakelen.                       | De projectgerelateerde configuratiesleutels zijn vervangen door een enkele projectconfiguratiesleutel die PMA-functionaliteit inschakelt.                                                                                                                                                                                                       |

## <a name="retail-and-commerce"></a>Detailhandel en commerce
### <a name="advanced-warehouse-management-in-a-retail-store"></a>Geavanceerd magazijnbeheer in een detailhandelwinkel

Detailhandelaren kunnen de oplossing Geavanceerd magazijnbeheer (WHS) in hun winkels gebruiken en de vereiste updates uitvoeren voor de huidige functies voor verkooppunten (POS) om deze te ondersteunen. De processen voor oplossingen met handhelds zouden in een winkel moeten werken zoals ze dat in ieder ander magazijn doen. Alle huidige processen voor winkelvoorraden in de detailhandel en alle POS-processen die voorraadtransacties maken of bijwerken, zijn bijgewerkt zodat ze de specifieke vereisten van voor WHS ingeschakelde magazijnen gebruiken.

| Wat u kunt doen                                                                       | Waarom dit belangrijk is                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Door middel van POS beschikbare voorraad opzoeken in voor WHS ingeschakelde winkels.                     | Wanneer u voorraad opzoekt, zou het proces precies hetzelfde moeten werken als in het verleden. De zoekopdracht moet de beschikbare voorraadhoeveelheden op magazijnniveau weergeven en mag niet de dimensies Locatie, Voorraadstatus of Nummerplaat hebben. |
| Met behulp van POS een productontvangstbon verwerken voor een transferorder in een voor WHS ingeschakelde winkel. | U kunt op POS transferorders ontvangen voor een voor WHS ingeschakelde winkel en artikelen. De gebruiker moet dan de locaties kunnen selecteren waarop de orders moeten worden ontvangen, en zou nummerplaat-id's moeten kunnen invoeren om de ontvangstregels automatisch te vullen.    |
| Met behulp van POS een productontvangstbon verwerken voor een verkooporder in een voor WHS ingeschakelde winkel. | U kunt op POS inkooporders ontvangen voor een voor WHS ingeschakelde winkel en artikelen. De gebruiker moet dan de locaties kunnen selecteren waarop de orders moeten worden ontvangen, en zou nummerplaat-id's moeten kunnen invoeren om de ontvangstregels automatisch te vullen.    |
| Door middel van POS een zending van producten van een voor WHS ingeschakelde winkel verwerken.               | U kunt vanaf POS transfers registreren voor een voor WHS ingeschakelde winkel en artikelen. De gebruiker moet de locaties kunnen selecteren van waaraf wordt verzonden, de voorraadstatus moet automatisch worden gegenereerd en de nummerplaten moeten worden genegeerd.         |

### <a name="enable-seamless-omni-channel-commerce"></a>Naadloze handel over meerdere kanalen mogelijk maken

Naadloze handel over meerdere kanalen verwijst naar beheer en orderverwerken in fysieke winkels, onlinewinkels, callcenters en verkopen via mobiele apparaten. Voor deze versie zijn de volgende investeringen gedaan in dit gebied:

-   Verbeteringen voor het publiceren van e-commercewinkels
-   Een nieuwe mobiele app voor consumenten die productdiscovery, accountbeheer en online winkelen mogelijk maakt.

| Wat u kunt doen                                                                                                                                                                                                                                                                   | Waarom dit belangrijk is                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consument: de huidige versie van de consumenten-app maakt de volgende functies mogelijk: producten zoeken, bladeren door categorieën, toevoegen aan winkelwagen en uitchecken als gast. Detailhandelaren kunnen de huisstijl van hun bedrijf ook toepassen op de app en deze vervolgens verpakken om aan te bieden in de app-stores voor Android en iOS. | Detailhandelaren kunnen eenvoudig een app voor consumenten maken, waarmee hun klanten kunnen bladeren, producten zoeken en als gast producten kunnen bestellen vanaf hun mobiele apparaten.                      |
| Wensenlijsten van klanten voor onlinewinkels met e-commerce.                                                                                                                                                                                                                             | Onafhankelijke softwareleveranciers (Independent software vendors - ISV's) kunnen het wenslijstbesturingselement gebruiken om gebruikers meerdere lijsten te laten aanmaken en beheren in de onlinewinkel, en die lijsten laten weergeven/gebruiken in de POS. |
| Asynchroon klanten aanmaken via e-commerce onlinewinkels.                                                                                                                                                                                                                  | ISV's kunnen nu klantaccounts maken, zelfs wanneer de real-time service van Commerce Data Exchange niet beschikbaar is.                                                                        |
| Kanaalproducten publiceren van Retail Server naar winkels van derden.                                                                                                                                                                                                           | Retail Server ondersteunt nu service-naar-service verificatie. ISV's kunnen profiteren uit het publiceren van kanaalproducten vanuit Retail Server naar winkels van derden.               |

### <a name="extensibility"></a>Uitbreidbaarheid

-   Commerce runtime-projecten zijn nu losgemaakt van de Retail SDK.
-   Eenvoudiger implementeren en onderhoud plegen via opgedeelde pakketten met Microsoft-onderdelen en ISV-pakketten voor de POS, Retail Server, Databases, Payment en Hardwarestations.

| Wat u kunt doen                                                                                                                 | Waarom dit belangrijk is                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CRT/Retail Server: Detailhandels of ISV's kunnen de CRT uitbreiden door uitbreidings-hooks. Inline codewijzigingen worden niet meer ondersteund. | Om continue integratie en implementatie mogelijk te maken, moeten inline codewijzigingen volledig worden vermeden. Dit is ook nodig om gemakkelijk hotfixes te kunnen uitrollen zonder samenvoeging van code en implementatie voor CRT-componenten. |

### <a name="personalized-product-recommendations"></a>Persoonlijke productaanbevelingen

| Wat u kunt doen                                                                                                                                                                                                                                                                        | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bekijk persoonlijke productaanbevelingen op meerdere contactpunten op POS om te bepalen waarin een klant geïnteresseerd kan zijn op basis van hun inkoophistorie, artikelen op hun wensenlijst en artikelen die andere klanten online en in fysieke winkels hebben gekocht. | Bij detailhandelaren met grote catalogi kunnen persoonlijke aanbevelingen de klant bijstaan in het ontdekken van producten en stellen winkelmedewerkers in staat beter te werken door intelligente clienteling. Door producten te belichten die zijn gericht op de interesses van een klant en diens koopgewoontes, kunnen productaanbevelingen detailhandelaren helpen met upsell en klantenbinding. Productaanbevelingen worden in Microsoft Dynamics 365 for Retail aangestuurd door cognitieve services en Microsoft Azure Machine Learning. |

### <a name="pos-task-recorder"></a>POS-taakregistratie

| Wat u kunt doen                                                                                                                                                                                                  | Waarom dit belangrijk is                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Detailhandels kunnen door middel van POS-taakregistratie trainingsmaterialen en bedrijfsprocesplannerdiagrammen samen te stellen en Help-inhoud te genereren voor grotere productiviteit en betere analyse en ontwerp van toepassingen. | Om continue integratie en implementatie mogelijk te maken, moeten inline codewijzigingen volledig worden vermeden. Dit is ook nodig om gemakkelijk hotfixes te kunnen uitrollen zonder samenvoeging van code en implementatie voor CRT-componenten. |
| Real-time help in POS.                                                                                                                                                                                           | De kassier/manager kan real-time help voor het bedrijfsproces krijgen in POS zonder over te schakelen naar een andere context.                                                                                                           |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Store system: een naadloze winkelervaring ter plaatse bieden

Store system is een implementatiekeuze voor detailhandels die helpt een set winkelbewerkingen aan te sturen, ongeacht of dat gebeurt in een plaatselijke winkel, de openbare cloud van Microsoft of de privécloud van de klant. Voor deze versie is het bereik uitsluitend scope in de winkel. Om omgevingen met langzame en onbetrouwbare netwerkverbinding beter te kunnen ondersteunen, moet detailhandelaren een optie worden geboden om de kanaaldatabase en Retail Server in de winkel te gebruiken. Ze kunnen dan de belangrijkste zakelijke scenario's blijven uitvoeren, zelfs wanneer er geen verbinding is met Headquarters (HQ). Op basis van de diverse gegevenspunten, zoals discussies binnen het technische team, de resultaten van klantenenquêtes en concurrentanalyse, hebben we het volgende oplossingsbereik gevonden als ideale fit voor onze doelgroep:

-   Een self-servicepakket is beschikbaar voor Store system.
-   De standaardinstallatie is een oplossing uit één stuk, maar aangepaste implementatie is mogelijk.
-   Eenvoudige implementatie/self-service inschakelen.
-   Retail Server en de winkeldatabase bevinden zich in de winkel, samen met de Async Client-service.
-   Retail Server in de winkel communiceert rechtstreeks met Application Object Server (AOS) in HQ voor Store system.
-   Ondersteuning voor scenario's met meerdere terminals, wanneer er geen verbinding met HQ is.
-   Retail Modern POS en Cloud POS communiceren altijd met Retail Server in de winkel.
-   Ondersteuning voor Retail Modern POS en Cloud POS wanneer er geen verbinding met HQ is.
-   Ondersteuning voor een specifiek voor Retail Modern POS opgezette offline database (geïsoleerd van alle Retail Modern POS-exemplaren) wanneer er geen verbinding met HQ is.
-   Verificatie is gebaseerd op uitsluitend service-naar-service voor Store system.
-   Aanroepen van Real-time Service worden niet ondersteund als er geen internetverbinding is.
-   Rechtstreekste databaseverbinding tussen Retail Modern POS naar de kanaaldabatase wordt niet ondersteund.
-   Telemetrie/bewaking mogelijk.

| Wat u kunt doen                                                                                                                                       | Waarom dit belangrijk is                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Een detailhandelaar downloadt het self-service-installatieprogramma voor Store system van de pagina van de kanaaldatabase in Dynamics AX HQ en downloadt het configuratiebestand.   | De detailhandelaar kan het self-servicepakket naadloos downloaden.                                          |
| Een detailhandelaar installeert Store system door middel van het self-service-installatieprogramma.                                                                                 | De detailhandelaar kan Store system installeren door middel van het self-service-pakket.                                |
| De IT-beheerder configureert Store system in Dynamics 365 for Operations (kanaaldatabase, kanaalprofiel, winkel, en implementeerbaar pakket).             | De IT-beheerder kan Store system gemakkelijk en efficiënt configureren.                                       |
| Een detailhandelaar voert Retail Modern POS uit in de fysieke winkel en kan in real time bewerkingen uitvoeren, zoals geschenkbonnen uitgeven, wanneer er verbinding is. | De detailhandelaar kan in real time acties uitvoeren vanuit Store system, als er verbinding is.                |
| Een detailhandelaar kan gegevens van het lokale Store-systeem met HQ synchroniseren, wanneer er verbinding is.                                                      | De detailhandelaar kan vanuit en naar Store system synchroniseren, als er verbinding is.                              |
| Een detailhandelaar kan beveiligde communicatie tussen het lokale Store system en HQ hebben.                                                                 | De detailhandelaar kan met beveiliging communiceren vanuit Store system, als er verbinding is.                     |
| De IT-beheerder en Microsoft Operations kunnen op het lokale Store system bewaken en erover rapporteren (diagnostiek en wijzigingen rapporteren).                   | De IT-beheerder Microsoft Operations kunnen Store system met beveiliging bewaken en efficiënt problemen oplossen. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>App voor Universeel Windows Platform voor Retail Modern POS

Momenteel is Retail Modern POS alleen beschikbaar als een Windows 8.1-toepassing voor desktop-pc's en tablets, en in de vorm van Cloud POS voor browsers op desktop-pc's en tablets. In deze versie is Retail Modern POS omgezet in een app voor het universeel Windows-platform (UWP). Dankzij deze wijziging kan Retail Modern POS worden uitgevoerd op elk Windows 10-apparaat (desktop, tablet of telefoon) en zelfs schakelen tussen weergaven voor apparaten die geschikt zijn voor Continuum.

| Wat u kunt doen                                                   | Waarom dit belangrijk is                                                                                     |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Belangrijke POS-functionaliteit inschakelen voor apparaten met een kleine vormfactor. | Retail POS-functionaliteit is beschikbaar voor telefoons en andere kleine apparaten met Windows 10. |

## <a name="supply-chain-management"></a>Supply Chain Management
### <a name="consignment-inventory"></a>Consignatievoorraad

| Wat u kunt doen                                                                                                                                                                | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Als leverancier kunt u onbewerkte materialen opslaan in het magazijn van een klant. Als klant kunt u de werkelijke aankoop uitstellen totdat de onbewerkte materialen nodig zijn voor productie. | Het aanhouden van een grondstoffenvoorraad kan grote kosten met zich meebrengen. Door middel van een consignatievoorraad kan een leverancier grondstoffen opslaan in het magazijn van de klant. De klant kan dan de werkelijke aankoop uitstellen totdat de onbewerkte materialen nodig zijn voor productie. Grondstoffen worden besteld en ontvangen door middel van een consignatieaanvullingsorder. Deze aanvullingsorder registreert fysieke transacties, maar heeft geen invloed op het grootboek. Om te kunnen zien welke voorraadartikelen eigendom van de klant zijn en welke eigendom van de leverancier, kunt u gebruik maken van de voorraaddimensie Eigenaar. De eigendomsoverdracht voor voorraad wordt afgehandeld door een journaalproces, dat de overdracht van eigendom voor grondstoffen afhandelt van voorraad die eigendom is van de leverancier naar de voorraad die eigendom is van de klant. Dit proces leidt ertoe dat een inkooporder en een productontvangstbon worden aangemaakt. **Opmerking:** Deze functie is beperkt tot inkomende consignatie van grondstoffen voor productie. Hij is niet geïntegreerd met Magazijnbeheer (WHS) en Transportbeheer (TMS). |
| Als leverancier: informatie ophalen over de hoeveelheid geconsigeerde voorraadartikelen die naar de klant wordt overgeboekt.                                                                      | Om een klant te kunnen factureren, moet de leverancier informatie hebben over de grondstoffen die van de consignatievoorraad zijn gekocht en de datum van inkoop. De leverancier kan ook de voorhanden voorraad op de klantlocatie bewaken via de interface voor leverancierssamenwerking.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Voorraad in eigendom van de leverancier verplaatsen door middel van een overboekingsjournaal.                                                                                                                       | Als u de fysieke positie van de voorraad in eigendom van de leverancier wilt bijhouden, moet u de positie in het systeem kunnen registreren. Als u gebruik maakt van een overboekingsjournaal, kunt u de fysieke verplaatsing van voorraad registreren, zoals een verplaatsing van de ene plek in een magazijn naar een andere locatie in dat magazijn.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Voorraad in eigendom van de leverancier aanpassen door middel van een tellijst.                                                                                                                     | Het is belangrijk om de in het systeem geregistreerde voorhanden voorraad synchroon te houden met de daadwerkelijke fysieke voorraad. De voorraad in eigendom van de leverancier kan voor in- en uitgaande mutaties worden gecorrigeerd door middel van telprocessen zoals hoeveelheidscorrecties en tellijstprocessen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Meer te weten komen over ondersteuning voor consignatie in Dynamics 365 for Operations.                                                                                                         | Voor meer informatie over de ondersteuning voor consignatieprocessen zie [Consignatie](../../supply-chain/inventory/consignment.md), [Consignatie instellen](../../supply-chain/inventory/set-up-consignment.md), [Een nieuwe consignatieaanvullingsorder maken (taakbegeleiding)](../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) en [Het eigendom van consignatievoorraad wijzigen op basis van de productievraag (taakbegeleiding)](../../supply-chain/inventory/tasks/change-ownership-consignment.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Leverancierssamenwerking (voorheen bekend als de Leveranciersportal)

| Wat u kunt doen                                                                      | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leveranciers in staat stellen om op elke inkooporderregel te reageren en wijzigingen voor te stellen.           | In sommige gevallen willen leveranciers sommige inkooporderregels accepteren maar andere afwijzen. Leveranciers kunnen nu individuele inkooporderregels beheren. Elke regel kan worden worden afgewezen, geaccepteerd of geaccepteerd met wijzigingen. Bijvoorbeeld kunnen leveranciers de leveringsdatum wijzigen, de levering en hoeveelheid splitsen, of een alternatief artikel voorstellen.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Leveranciers in staat stellen om gegevens van contactpersonen te beheren.                                 | Leveranciers kunnen gegevens voor contactpersonen voor hun bedrijf beheren. Deze informatie omvat namen, e-mailadressen en telefoonnummers. De toegang tot deze functie wordt verleend door middel van een specifieke beveiligingsrol.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Documenten die gerelateerd zijn aan inkooporders delen met leveranciers.                    | Wanneer u een document met een leverancier moet delen, zoals een document over vereisten, is het handig om het document aan de relevante inkooporder te koppelen. De leverancier kan dan opmerkingen en bijlagen delen met de klant, door het document te koppelen aan zijn of haar antwoord op de inkooporder. Documentbeheer het is het onderliggende ondersteunende raamwerk. Alleen opmerkingen en bijlagen die zijn geclassificeerd als 'extern' kunnen met leveranciers worden gedeeld.                                                                                                                                                                                                                                                                                                                              |
| Nieuwe gebruikers van leveranciers inrichten.                                                          | Als uw leveranciers de leverancierssamenwerkingsinterface gebruiken, hebben ze een naadloze manier om nieuwe gebruikersaccounts aan te vragen wanneer nieuwe contactpersonen toegang tot leverancierssamenwerking nodig hebben. Inkoopmedewerkers kunnen een aanvraag voor een gebruikersaccount voor een contactpersoon van de leveranciersorganisatie indienen. Een contactpersoon van een leverancier die al een gebruiker is in Leverancierssamenwerking, kan dit type aanvraag ook indienen. Deze aanvraag maakt uiteindelijk een nieuwe gebruiker aan in Dynamics 365 for Operations met leverancierspecifieke beveiligingsrollen. Het verstuurt ook een aanvraag aan de Microsoft Azure B2B-portal om voor de gebruiker een nieuwe gebruikersaccount in Azure Active Directory (AAD) in te richten. Leveranciers kunnen ook verzoeken om specifieke leveranciersgebruikersaccounts te deactiveren of de beveiligingsrollen aan te passen. |
| Meer te weten komen over ondersteuning voor leverancierssamenwerking in Dynamics 365 for Operations. | Meer informatie over leverancierssamenwerking vindt u in [Leverancierssamenwerking met externe leveranciers](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Leverancierssamenwerking met klanten](../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Leverancierssamenwerkingsgebruikers beheren](../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Leverancierssamenwerking instellen en onderhouden](../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) en [Het werkgebied Leverancierssamenwerkingsfacturen](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).                                                         |

### <a name="intercompany-order-processing"></a>Intercompany-orders verwerken

<table>




<thead>
<tr class="header">
<th>Wat u kunt doen</th>
<th>Waarom dit belangrijk is</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rechtstreeks op verkooporderregels definiëren van waaruit de producten voor de vraag moeten worden verzonden, en hoe de vraag moet worden vervuld. <strong>Voorbeeld</strong> Een verkooporderregel maken en rechtstreekse levering opgeven als leveringstype. De primaire leverancier wordt toegevoegd aan de verkooporderregel als sourcingpunt.</td>
<td>De flow voor het aannemen van orders is aanzienlijk verbeterd. U kunt nu rechtstreeks op verkooporderregels definiëren van waaruit de producten voor de vraag moeten worden verzonden, en hoe de vraag moet worden vervuld. U hoeft niet meer wachten totdat alle regels aan de verkooporder zijn toegevoegd. Met nieuwe opties voor verkooporderregels kunt u het leveringstype opgeven wanneer u een leverancier opgeeft. Wanneer u een leverancier koppelt aan verkooporderregels, worden de orderketens gemaakt voor levering vanaf de leverancier.
<ul>
<li>De leverancier kan een intercompany-leverancier zijn die een interne inkooporder en verkooporder gebruikt, of hij kan een externe leverancier zijn die een externe inkooporder gebruikt.</li>
<li>Het leveringstype kan <strong>Rechtstreekse levering</strong> zijn of <strong>Voorraad</strong>. Het leveringstype <strong>Voorraad</strong> geeft aan dat de leverancier aan de lokale voorraad moet leveren voordat dit naar de klant wordt verzonden.</li>
</ul></td>
</tr>
<tr class="even">
<td>Een orderbelofte rechtstreeks vanuit verkooporderregels maken. <strong>Voorbeeld</strong> Maak een verkooporderregel aan die waarbij levering plaatsvindt door een intercompany-leverancier. Verlaat de regel. De leveringsdatums worden berekend volgens de beschikbaarheid bij het leverende bedrijf.</td>
<td>Wanneer u verkooporderregels maakt die de nieuwe sourcinginformatie gebruiken, worden leveringsdatums berekend volgens het besturingselement <strong>Leveringsdatum</strong>. Als bijvoorbeeld een intercompany-leverancier wordt geselecteerd, wordt de beschikbaarheid bij het leverende bedrijf berekend. Op deze manier worden orderketens automatisch gemaakt samen met verkooporderregels. Deze functionaliteit zorgt ervoor dat de leveringsdatums zichtbaar worden in het leverende bedrijf, zodat de ATP-profielen (available to promise) de verwachte vraag meteen kunnen afhandelen wanneer verkooporders worden aangemaakt.</td>
</tr>
<tr class="odd">
<td>Productbeschikbaarheid controleren voor alle leverende locaties en de beste leveringsoptie selecteren.</td>
<td>De pagina <strong>Alternatieven voor levering</strong> is opnieuw ingericht en geeft nu waardevolle informatie over alle goedgekeurde interne en externe leveranciers. Deze informatie bevat sourcingopties voor inkoop bij leveranciers. Als u een leveringsmethode selecteert, berekent het systeem mogelijke leveringsdatums. U kunt naadloos de beste optie voor de klant selecteren en deze optie toepassen op elke verkooporderregel.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Magazijnverbeteringen voor distributiecentra met grote volumes

| Wat u kunt doen                                                              | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Werk maken nadat goederen zijn ingepakt op een inpakstation.               | Deze functie is nuttig wanneer er extra processen moeten worden uitgevoerd na het handmatige inpakwerk, zoals palletisering, kwaliteitscontrole, consolidatie van zendingen of wijzigingen in ladingsdokken. Met het nieuwe werktype **Orderverzameling voor ingepakte container** kunt u deze taken modelleren door middel van afzonderlijke werkregels. U kunt nu pakstations modelleren om werk na verpakking te genereren. Dit werk kan worden gebruikt om de verplaatsing van verpakte voorraad te organiseren.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Containers groeperen op het inpakstation.                                     | Met deze functie kunnen meerdere pakketten worden gegroepeerd in één container of nummerplaat bij het pakstation. Een e-commercewinkelier/groothandel kan bijvoorbeeld 100 afzonderlijk verpakte pakketten in één container groeperen (zoals een pallet of een kooi). Deze container kan vervolgens worden verplaatst, klaargezet of worden geladen met een enkele werkinstructie, die een werknemer genereert door één streepjescode (nummerplaat) voor de gegroepeerde container te scannen. Deze functie beperkt het aantal werktransacties voor het verplaatsen van vele kleinere verpakte containers. Meer informatie vindt u in [Een menuopdracht voor een mobiel apparaat maken ten behoeve van nummerplaatconsolidatie (taakbegeleider)](../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md).                                                                                                                                                                                                                                                                                                                                                                                            |
| Een vrijgavebeleid voor verpakte containers maken.                               | Werk dat wordt geactiveerd door het vrijgeven van containers kan automatisch of handmatig worden gemaakt. Wanneer het automatisch wordt gemaakt, wordt werk gegenereerd bij het sluiten van de container door middel van het framework voor locatie-instructies en werksjablonen. Wanneer de vrijgave handmatig gebeurt, kan de verpakker bepalen of het werk voor één container of een groep containers moet worden gegenereerd. Deze functie verkleint het risico dat afgesloten containers worden verzameld en verplaatst voordat ze klaar zijn om te worden weggehaald bij het pakstation. Dit maakt ook niet door het systeem aangestuurde gegroepeerde vrijgave mogelijk.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Hertoewijzing van kort orderverzamelen                                                   | Ondersteuning is toegevoegd voor processen voor kort orderverzamelen, om een partner te helpen die de goederen niet kan verzamelen en de order wil vervullen wanneer het vereiste artikel op een andere locatie beschikbaar is. U kunt een automatisch hertoewijzingsproces gebruiken, dat dezelfde locatie-instructies gebruikt voor het ophalen van de goederen als ze op een andere locatie beschikbaar zijn. Ook kan bij handmatige hertoewijzing het mobiele apparaat een lijst met locaties weergeven, samen met de beschikbare hoeveelheid. De magazijnwerknemer kan vervolgens de locatie selecteren waarvan de voorraad moet worden gebruikt. Deze twee methoden kunnen afzonderlijk worden ingesteld of als een enkele opdracht in het menu van de magazijnmedewerker. Bij handmatige hertoewijzing kan de magazijnwerknemer de artikelhoeveelheid voor kort orderverzamelen ophalen van verschillende locaties. Meer informatie vindt u in [Artikelhertoewijzing voor kort orderverzamelen instellen (taakbegeleiding)](../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md).                                                                                                                                                                                          |
| Voorraad verplaatsen waaraan werk is gekoppeld.                             | U kunt nu voorraad verplaatsen waaraan werk is gekoppeld. Deze functie kan nuttig zijn als bijvoorbeeld een werknemer ruimte in een dok voor inkomende artikelen wil vrijmaken en geregistreerde pallets verplaatst die wachten op opslag op een andere inbound locatie. Het dok wordt vrijgemaakt en kan een extra lading goederen ontvangen. De verplaatste voorraad wordt bijgewerkt met de nieuwe opslaggegevens. U kunt met deze functie ook ruimte vrijmaken op orderverzamellocaties, door voorraad te verplaatsen waaraan werk is gekoppeld en ruimte vrij te maken voor aanvulling. U kunt hiermee ook ladingen van de ene faseringslocatie naar een andere verplaatsen, zonder dat u het ladingswerk verliest dat is gegenereerd. Zo kan de functie helpen om de tijd te optimaliseren die nodig is om vrachtwagens te laden wanneer ze binnenkomen. U kunt voorraad verplaatsen die is gereserveerd voor verkooporders, transferorderuitgiftes, transferorderontvangsten, en inkooporders. Verplaatsing wordt geblokkeerd als hierdoor regels worden opgesplitst. Als u bijvoorbeeld een werkregel voor 100 stuks van een artikel hebt, kunt u niet slechts 30 stuks van dat artikel naar een andere locatie verplaatsen. |
| Nummerplaten samenvoegen waaraan werk is gekoppeld.                    | U kunt nummerplaten samenvoegen waaraan outbound werk is gekoppeld. Wanneer verzameling van een order bijvoorbeeld is opgesplitst in meerdere stuks werk, kan het handig zijn dat nummerplaten kunnen worden samengevoegd nadat ze op de faseringslocatie zijn afgeleverd. Nummerplaten kunnen alleen worden geconsolideerd als ze op dezelfde locatie zijn, deel uitmaken van dezelfde lading en dezelfde verzendingsgegevens hebben.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Op regelniveau orderverzameling blokkeren dat is gekoppeld aan aanvulling. | U kunt nu werk op regelniveau blokkeren in plaats van op koptekstniveau, zodat werknemers verzamelregels kunnen vervullen die niet door de vraagaanvulling zijn geblokkeerd. Zo kunnen groothandelaars of detailhandelaars met grote verkooporders of aanvullingstransferorders het werk voor orderverzameling laten beginnen voor alle regels waarvoor geen aanvullingswerk uitstaat. Het werk voor verzamelen en aanvullen kan dan tegelijkertijd worden voltooid. Deze functie kan zodanig worden geconfigureerd dat u kunt selecteren of u op koptekstniveau of regelniveau wilt blokkeren. U kunt ook beide methoden toepassen en voor elke methode een werksjabloon maken. De configuratie voor koptekst of regel wordt ingesteld in de werksjablonen, maar u kunt deze ook rechtstreeks op het gegenereerde werk wijzigen.                                                                                                                                                                                                                                                                                                                                                                      |
| Werk annuleren door middel van het mobiele apparaat.                                      | U kunt nu werk annuleren door middel van het mobiele apparaat, met of zonder vraagaanvulling. Voorheen moest u hiervoor de rich client gebruiken. Om deze functionaliteit te schakelen, maakt u een menuopdracht voor het mobiele apparaat waarin de modus is ingesteld op **Indirect** en de activiteitscode op **Werk annuleren**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

### <a name="warehouse-operation-enhancements"></a>Verbeteringen in magazijnbewerkingen

| Wat u kunt doen                    | Waarom dit belangrijk is                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verschillende containertypen modelleren.   | U gebruikt mogelijk verschillende containertypen in uw magazijn om opslag te optimaliseren en voor andere redenen. De nieuwe entiteit Containertype heeft de fysieke kenmerken van de containertypen. U kunt nu nummerplaten koppelen aan een bepaald containertype en de locatieopslaglimieten gebruiken. U kunt bijvoorbeeld met deze functie bepalen hoeveel pallets (of andere containertypen) op een specifieke locatie zijn toegestaan. Containertypen zijn ook toegevoegd aan de eenheidvolgordegroepen om standaardcontainertypen voor het ontvangende proces toe te voegen. Containertypen kunnen worden gebruikt met inkomende en uitgaande locatie-instructies. Ze kunnen ook in de weergave van de voorhanden voorraad worden gebruikt om u te helpen om te bepalen hoeveel containertypen momenteel op voorraad zijn opgeslagen. Meer informatie vindt u in het blogbericht [Gebruik van nummerplaten gekoppeld aan een containertype voor de uitvoering van processen voor magazijnbeheer](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/) Dit blogbericht beschrijft weliswaar een update voor Microsoft Dynamics AX 2012, maar dezelfde ondersteuning is nu toegevoegd aan Dynamics 365 for Operations.                                                                                                                                                                                                                                                                                                                         |
| Leveringen omkeren.                 | In een magazijn moet u wijzigingen op het laatste moment kunnen verwerken. Sommige goederen zijn bijvoorbeeld beschadigd, zodat u ze niet kunt verzenden. Of een klant kan op het laatste moment een aanvraag indienen om een order te annuleren of te wijzigen. Met Dynamics 365 for Operations kunt u nu een levering omkeren. U kunt dan een pakbon annuleren, zodat u deze later met de correcte hoeveelheden kunt bijwerken. Op dezelfde manier kunt u in de inbound flow productontvangstbonnen annuleren, zodat een bijgewerkte versie kan worden gemaakt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Pallets met gemengde artikelen gebruiken. | U kunt nu een 'gemengde' pallet ontvangen en registreren. Een gemengde pallet bestaat uit verschillende artikelen die voor een of meer inkooporders of -regels op één pallet zijn samengebracht. Alle registraties kunnen worden samengevat in een doelnummerplaat. Dit proces wordt ingeschakeld via het mobiele apparaat van het magazijn. Wanneer bijvoorbeeld de pallet met gemengde artikelen in het magazijn aankomt, identificeert de ontvangstmedewerker de artikelen en hoeveelheden op de pallet, voordat de pallet wordt verplaatst naar specifieke opslaglocaties. De opslaglocaties worden geïdentificeerd door werksjablonen en locatie-instructies. Als de opslaglocaties zijn verdeeld over verschillende artikelen met vaste locaties, maakt deze functie net zoveel regels voor neerzetwerk aan als er verschillende artikelen in de gemengde pallet zijn. Deze functie maakt het sneller en flexibeler om de ontvangen pallets met gemengde artikelen te registreren en weg te zetten. Meer informatie vindt u in het blogbericht [Ontvangen en registreren van een pallet met gemengde brondocumentregels met één nummerplaat](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) en de informatie voor ondersteuning voor gemengde pallets in de [aankondiging van de recente cumulatieve update](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Dit blogbericht beschrijft weliswaar een update voor AX 2012, maar dezelfde ondersteuning is nu toegevoegd aan Dynamics 365 for Operations. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Kleinere functieverbeteringen in Supply Chain Management

<table>




<thead>
<tr class="header">
<th>Wat u kunt doen</th>
<th>Waarom dit belangrijk is</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nieuwe gegevensentiteiten gebruiken om gegevens te importeren en te exporteren.</td>
<td>U kunt gegevens importeren en exporteren met behulp van deze gegevensentiteiten:
<ul>
<li>Vrachtfactuur</li>
<li>Samengestelde voorraad per magazijn en voorraadstatus</li>
<li>Voorraadtoeslagen</li>
<li>Offerte</li>
</ul></td>
</tr>
<tr class="even">
<td>Met het verbeterde Gantt-besturingselement interactieve planningsscenario's ontwikkelen.</td>
<td>Met het verbeterde Gantt-besturingselement kunt u nieuwe interactieve planningsscenario's ontwikkelen en betere API's leveren waarmee het uiterlijk van activiteiten kan worden aangepast. Dit zijn enkele van de nieuwe API's:
<ul>
<li>Activiteiten verticaal slepen en neerzetten</li>
<li>Activiteiten toevoegen/verwijderen</li>
<li>Voorbeeldweergave van geboekte perioden in overzichtsbalk</li>
<li>Kleur en stijl van activiteitsranden wijzigen</li>
<li>Kleur, stijl en achtergrond van tekst in het raster wijzigen</li>
</ul></td>
</tr>
<tr class="odd">
<td>Betere afhandeling van materiaal- en resourceplanning.</td>
<td>Enkele verbeteringen zijn doorgevoerd in materiaal- en resourceplanning:
<ul>
<li>De uitgiftemarge wordt nu verwerkt wanneer een artikel op voorraad is.</li>
<li>De leveringsdatum overschrijven wanneer u geplande orders vastlegt.</li>
<li>Voltooiing van orders hogere prioriteit geven dan veiligheidsvoorraad.</li>
<li>Inplannen van geplande orders in het verleden voorkomen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Het werkelijke verbruik voor productie rapporteren en de voorraadstatus weergeven.</td>
<td>U kunt het werkelijke verbruik voor productie weergeven. Daarnaast is het selectievakje <strong>Voorraadstatus weergeven</strong> toegevoegd aan <strong>Mutatie</strong> in de menuopdracht <strong>Werk aanmaken</strong>, dat de voorraadstatus zichtbaar maakt.</td>
</tr>
<tr class="odd">
<td>Volumetrisch gewicht berekenen, als de tarieven van uw vervoerder op volumetrisch gewicht zijn gebaseerd.</td>
<td>Een nieuwe TMS-tariefengine die op volumetrisch gewicht is gebaseerd, is toegevoegd zodat u volumetrisch gewicht kunt berekenen.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Aanvullende resources
--------

[Wat is nieuw of gewijzigd](whats-new-changed.md)




