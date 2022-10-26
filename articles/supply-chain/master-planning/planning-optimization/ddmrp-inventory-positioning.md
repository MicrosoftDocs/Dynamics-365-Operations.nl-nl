---
title: Voorraadpositionering
description: Dit artikel biedt informatie over strategische voorraadpositionering waarbij het gaat om het identificeren van ontkoppelingspunten in uw toeleveringsketen waar u de beschikbare voorraad kunt opbouwen om de doorlooptijden te verkorten en schokken op te vangen voor uw toeleveringsketen.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 847108575cbf7207282db00d731363c8cfad883a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689533"
---
# <a name="inventory-positioning"></a>Voorraadpositionering

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Bij strategische voorraadpositionering gaat het om het identificeren van ontkoppelingspunten in uw toeleveringsketen waar u beschikbare voorraad kunt opbouwen. Deze aanpak wordt met name gebruikt om de doorlooptijden te verkorten en schokken voor uw toeleveringsketen op te vangen. U kunt hiermee het 'zweepslageffect' beperken, omdat de vraagvariabiliteit niet door de hele toeleveringsketen heen geldt. (Het *zweepslageffect* verwijst naar hoe kleine schommelingen in de vraag op detailhandelniveau kunnen zorgen voor progressief grotere schommelingen in de vraag op het niveau van groothandel, distributeur, fabrikant en leverancier van grondstoffen.)

Voorraadpositionering is de eerste stap van DDMRP (Demand Driven Materials Resource Planning).

## <a name="inventory-positioning-for-manufacturing"></a>Voorraadpositionering voor productie

In dit gedeelte wordt een voorbeeld gegeven dat laat zien hoe u beslissingen moet nemen over de voorraadpositionering als u een normaal product zoals een kussen produceert. Het kussen heeft een stuklijst met meerdere niveaus, zoals in de onderstaande afbeelding is weergegeven.

![Voorbeeld van een stuklijst met meerdere niveaus voor het product kussen.](media/ddmrp-bom-example.png "Voorbeeld van een stuklijst met meerdere niveaus voor het product kussen")

### <a name="choose-your-decoupling-points"></a>Uw ontkoppelingspunten kiezen

Wanneer u kiest waar u uw ontkoppelingspunten wilt plaatsen, moet u alle volgende aspecten van elk artikel in de stuklijst als criteria overwegen:

- Externe variabiliteit
- Hefboomwerking en flexibiliteit van voorraad
- Bescherming van kritieke bewerkingen
- Tolerantietijd van klant
- Zichtbaarheidsperiode verkooporder
- Potentiële doorlooptijd markt

In het voorbeeld van het kussen kunt u om de volgende redenen het eerste ontkoppelingspunt plaatsen op *schuimrubber*:

- Het is moeilijk om de materialen te vinden die worden gebruikt om schuimrubber te maken en de beschikbaarheid is wisselvallig. Daarom wordt voldaan aan het criterium van *externe variabiliteit*.
- Schuimrubber kan in veel verschillende vormen en maten worden gesneden om schuimvulling naast het kussen voor andere producten die u produceert te maken. Daarom wordt voldaan aan het criterium voor *hefboomwerking en flexibiliteit van de voorraad*.

U kunt vervolgens uw volgende ontkoppelingspunt op *stofpakket* plaatsen, wat voorgesneden stof voor kussens is. U kunt dit punt kiezen, omdat u slechts één snijmachine voor stof hebt. Daarom wordt voldaan aan het criterium voor *bescherming van kritieke bewerkingen*.

Tot slot kunt u uw laatste ontkoppelingspunt plaatsen op het eindproduct kussen. U kunt dit punt kiezen omdat u een zeer korte *tolerantietijd van klant* bij verkoop hebt en omdat de *zichtbaarheidsperiode van verkooporders* vrij kort is. Daarom wilt u er zeker van zijn dat u over de beschikbare voorraad beschikt om aan binnenkomende orders te kunnen voldoen. U kunt ook een hogere prijs instellen door de doorlooptijd zo kort te houden, waarnaar het criterium *potentiële doorlooptijd van de markt* verwijst.

Op basis van deze analyse wordt in de volgende afbeelding aangegeven hoe de stuklijst voor een kussen eruitziet. Met gele voorraadsymbolen worden de ontkoppelingspunten gemarkeerd.

![Voorbeeld van stuklijst met ontkoppelingspunten gemarkeerd.](media/ddmrp-bom-decoupling-example.png "Voorbeeld van stuklijst met ontkoppelingspunten gemarkeerd")

### <a name="calculate-your-decoupled-lead-time"></a>Uw ontkoppelde doorlooptijd berekenen

In dit gedeelte wordt aangegeven hoe u uw nieuwe doorlooptijden berekent nadat u ontkoppelingspunten hebt geïntroduceerd.

In de volgende afbeelding van het kussenvoorbeeld in het vorige gedeelte worden de doorlooptijden weergegeven in grijze vakken linksboven in elk stuklijstonderdeel. Vakken met een rode contour geven artikelen aan die de cumulatieve doorlooptijd bepalen (de som van de langste doorlooptijden op elk niveau van de stuklijst). Deze doorlooptijd is 21 dagen wanneer u opnieuw begint.

![Voorbeeld van stuklijst met doorlooptijden.](media/ddmrp-bom-lead-times-example.png "Voorbeeld van stuklijst met doorlooptijden")

Als u echter de ontkoppelingspunten toepast die u eerder hebt gekozen, zijn de ontkoppelde artikelen altijd op voorraad. Deze hebben dus een doorlooptijd van 0 (nul). De nieuwe doorlooptijd voor het kussen is nu slechts vijf dagen: twee dagen voor aankoop van het garen en drie dagen om het kussen te produceren. Deze doorlooptijd wordt de *ontkoppelde doorlooptijd* genoemd.

![Voorbeeld van ontkoppelde doorlooptijd.](media/ddmrp-bom-decoupled-lead-time-example.png "Voorbeeld van ontkoppelde doorlooptijd")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Strategische voorraadpositionering in een detailhandelmodel

Aangezien detailhandelaren alleen eindproducten in voorraad hebben, zijn de stuklijsten geen probleem. Detailhandelaren kunnen echter wel gebruik maken van DDMRP door strategische voorraadpositionering en bufferniveaus in te stellen op basis van opslaglocaties in het distributienetwerk.

In de volgende afbeelding ziet u een voorbeeld van een bedrijf dat een distributiecentrum in Seattle heeft en winkels in Boston, Atlanta en Portland.

![Ontkoppelingspunten op basis van locatie in een detailhandelmodel.](media/ddmrp-retail-decoupl-points-example.png "Ontkoppelingspunten op basis van locatie in een detailhandelmodel")

Mogelijk besluit u dat de transporttijd om het product deken tussen het distributiecentrum en de winkels in strijd is met de *tolerantietijd van uw klant*, omdat uw klanten verwachten dat het deken op voorraad is als ze op bezoek komen. In dit geval stelt u een ontkoppelingspunt in voor het artikel deken in elk van de drie winkels. Elke winkel heeft verschillende bufferniveaus, gebaseerd op de doorlooptijden, vraagpatronen en dergelijke.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Voorraadpositionering implementeren in Dynamics 365 Supply Chain Management

In dit gedeelte wordt beschreven hoe u de strategie voor voorraadpositionering in Microsoft Dynamics 365 Supply Chain Management kunt implementeren.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Artikelbehoefteplanningsgroepen instellen waarmee ontkoppelingspunten worden gemaakt

Artikelen worden ontkoppelingspunten wanneer ze horen bij een behoefteplanningsgroep die wordt geconfigureerd met een waarde voor **Behoefteplanningscode** van *Ontkoppelingspunt*. Daarom is de eerste stap in het proces voor het instellen van DDMRP te bepalen welke behoefteplanningsgroepen u moet implementeren voor uw DDMRP-strategie en deze vervolgens te maken door deze stappen uit te voeren.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Behoefteplanningsgroepen**.
1. Selecteer in het actievenster **Nieuw** om een behoefteplanningsgroep te maken.
1. Voer de informatie in die de behoefteplanningsgroep identificeert en selecteer de kalender die moet worden gebruikt.
1. Stel op het tabblad **Algemeen** het veld **Behoefteplanningscode** in op *Ontkoppelingspunt*. Door deze instelling worden alle artikelen die tot deze behoefteplanningsgroepen behoren, behandeld als ontkoppelingspunten voor DDMRP. Ook worden met deze instelling alle DDMRP-instellingen voor deze groep ingeschakeld, zoals later in deze procedure wordt beschreven.
1. Stel op het tabblad **Overige** in de sectie **DDMRP-parameters** de volgende velden in:

    - **Factor doorlooptijd**: geef een factor op (als een decimale waarde tussen 0 en 1) om het effect te bepalen dat de doorlooptijd moet hebben wanneer de minimale en maximale voorraadniveaus worden berekend voor artikelen in deze behoefteplanningsgroep. In het algemeen geldt dat des te langer de doorlooptijd van een artikel is, des te lager de doorlooptijdfactor moet zijn. Een lagere doorlooptijdfactor zorgt voor lagere minimale en maximale voorraadniveaus en daardoor voor kleinere en frequentere orders. Volgens de DDMRP-methodologie is een waarde tussen 0,20 en 0,40 aan te bevelen voor artikelen met lange doorlooptijden, tussen 0,41 en 0,60 voor artikelen met een gemiddelde doorlooptijd en tussen 0,61 en 1,00 voor artikelen met korte doorlooptijden. Zie [Bufferprofiel en -niveaus](ddmrp-buffer-profile-and-levels.md) voor meer informatie.
    - **Variabiliteitsfactor**: geef een factor op (als een decimale waarde tussen 0 en 1) om het effect te bepalen dat wisselende vraag moet hebben wanneer het minimale voorraadniveau wordt berekend voor artikelen in deze behoefteplanningsgroep. In het algemeen geldt dat des te variabeler de vraag van een artikel is, des te hoger de variabiliteitsfactor ervan moet zijn. Een hogere variabiliteitsfactor zorgt voor een hoger minimumvoorraadniveau. Volgens de DDMRP-methodologie is een waarde tussen 0,00 en 0,40 aan te bevelen voor artikelen met een lage variabiliteit, tussen 0,41 en 0,60 voor artikelen met een gemiddelde variabiliteit en tussen 0,61 en 1,00 voor artikelen met een hoge variabiliteit. Zie [Bufferprofiel en -niveaus](ddmrp-buffer-profile-and-levels.md) voor meer informatie.
    - **Periode min, max. en bestelpunt**: geef op hoe vaak bufferwaarden moeten worden berekend (*Dagelijks* of *Wekelijks*).

1. Stel op het tabblad **Overige** in de sectie **Gemiddeld dagelijks gebruik** de volgende velden in:

    - **Gemiddeld dagelijks gebruik gebaseerd op**: selecteer op welke perioden de berekening van het gemiddelde dagelijks gebruik moet worden gebaseerd. Selecteer een van de volgende waarden:

        - *Verleden*: kijk alleen naar eerder gebruik voor het aantal dagen dat is opgegeven in het veld **Periode in verleden (dagen)**. Het gemiddelde dagelijkse gebruik wordt berekend als de totale vraag naar een artikel tijdens de berekeningsperiode (in voorraadeenheden) gedeeld door het aantal dagen in de berekeningsperiode.
        - *Toekomst*: kijk alleen naar verwacht toekomstig gebruik (inclusief prognoses) voor het aantal dagen dat is opgegeven in het veld **Toekomstige periode (dagen)**. Het gemiddelde dagelijkse gebruik wordt berekend als de totale vraag naar een artikel tijdens de berekeningsperiode (in voorraadeenheden) gedeeld door het aantal dagen in de berekeningsperiode. 
        - *Gemengd*: kijk zowel naar gebruik in het verleden als naar toekomstig gebruik. De instellingen voor het veld **Periode in verleden (dagen)**, het veld **Toekomstige periode (dagen)** en gecombineerde opties zijn allemaal van toepassing. 

            *Gemengd gemiddeld dagelijks gebruik* = (\[*Gewicht in het verleden* × *Gemiddeld dagelijks gebruik in het verleden*\] + \[*Toekomstig gewicht* × *Toekomstig gemiddeld dagelijks gebruik*\]) ÷ (*Gewicht in het verleden* + *Toekomstig gewicht*)

    - **Periode in verleden (dagen)**: voer het aantal dagen in verleden (tot en met vandaag) in waarmee het systeem rekening moet houden bij het berekenen van het gemiddelde dagelijkse gebruik van artikelen in deze behoefteplanningsgroep. Deze instelling is alleen van toepassing als het veld **Gemiddeld dagelijks gebruik gebaseerd op** is ingesteld op *Verleden* of *Gemengd*.
    - **Toekomstige periode (dagen)**: voer het aantal toekomstige dagen in (vanaf vandaag tot en met de opgegeven dag) waarmee het systeem rekening moet houden bij het berekenen van het gemiddelde dagelijkse gebruik van artikelen in deze behoefteplanningsgroep. Deze instelling is alleen van toepassing als het veld **Gemiddeld dagelijks gebruik gebaseerd op** is ingesteld op *Toekomst* of *Gemengd*.
    - **Relatief gewicht van verstreken periode voor gemengd gemiddeld dagelijks gebruik**: voer het gewicht in (als percentage) dat u wilt toepassen op de afgelopen periode wanneer het gemengde gemiddelde dagelijkse gebruik wordt berekend. Deze instelling is alleen van toepassing als het veld **Gemiddeld dagelijks gebruik gebaseerd op** is ingesteld op *Gemengd*.
    - **Relatief gewicht van toekomstige periode voor gemengd gemiddeld dagelijks gebruik**: voer het gewicht in (als percentage) dat u wilt toepassen op de toekomstige periode wanneer het gemengd gemiddeld dagelijks gebruik wordt berekend. Deze instelling is alleen van toepassing als het veld **Gemiddeld dagelijks gebruik gebaseerd op** is ingesteld op *Gemengd*.

1. Voer voor alle andere tabbladen en velden de gedetailleerde instellingen in die worden gebruikt om behoeften voor de artikelen te berekenen die aan deze behoefteplanningsgroep zijn gekoppeld.

### <a name="set-an-item-as-a-decoupling-point"></a>Een artikel als een ontkoppelingspunt instellen

Voer de volgende stappen uit om een artikel in te stellen als een ontkoppelingspunt.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer een vrijgegeven artikel dat u wilt instellen voor DDMRP.
1. Selecteer in het actievenster op het tabblad **Plan** **Artikelbehoefteplanning**.
1. Op de pagina **Artikelbehoefteplanning** staan mogelijk al verschillende records voor artikelbehoefteplanning vermeld, waarvan elk van toepassing is op een andere combinatie van opslag- en productdimensies. U kunt een bestaande record van artikelbehoefteplanning selecteren die van toepassing is op de dimensies waar u een ontkoppelingspunt wilt maken. U kunt ook **Nieuw** selecteren in het actievenster om een nieuwe artikelbehoefteplanningsrecord te maken.
1. Stel de artikelbehoefteplanningsrecord zoals gebruikelijk in. U moet minimaal de locatie en het magazijn opgeven waarop het ontkoppelingspunt van toepassing is.
1. Terwijl de desbetreffende record nog steeds is geselecteerd, selecteert u het tabblad **Algemeen**.
1. Schakel het selectievakje **Specifieke instellingen gebruiken** in.
1. Stel het veld **Behoefteplanningsgroep** in op een behoefteplanningsgroep die is ingesteld om ontkoppelingspunten te maken (zoals is beschreven in het vorige gedeelte).
1. Het artikel wordt nu geconfigureerd als een ontkoppelingspunt. Wanneer u DDMRP gebruikt, worden hier meestal ook instellingen geconfigureerd die van invloed zijn op buffergrootten en de bestelhoeveelheid. U kunt deze configuratie echter later voltooien. Zie [Buffers instellen voor een ontkoppelingspuntartikel](ddmrp-buffer-profile-and-levels.md#set-up-buffers) voor meer informatie over de instellingen.

> [!NOTE]
> Als u artikelen wilt plannen die geen ontkoppelingspunten zijn, moet u dezelfde stappen uitvoeren als wanneer standaard-MRP (Material Requirements Planning) wordt gebruikt.
