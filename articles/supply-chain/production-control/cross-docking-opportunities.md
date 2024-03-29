---
title: Cross-docken van productieorders naar outbound docks
description: In dit artikel wordt beschreven hoe u het proces van cross-docken van gereedgemeld materiaal van een productieregel naar een outbound transportdock kunt beheren.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockOpportunityPolicy, WHSReservationHierarchy, WHSInventTableReservationHierarchy, WHSItemGroupLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea3ae6cb83d6577ba76d7e2aff9a05973b314cfe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849324"
---
# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Cross-docken van productieorders naar outbound docks

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u het proces van cross-docken van gereedgemeld materiaal van een productieregel naar een outbound transportdock kunt beheren.

## <a name="introduction"></a>Introductie

Cross-docken van productie naar een uitgaande locatie is relevant voor fabrikanten die grote hoeveelheden produceren en in het ideale geval de eindproducten willen verzenden zodra ze gereedgemeld zijn op de productieregels. Het doel is de producten te verzenden naar distributiecentra die zich fysiek dicht bij de vraag van klanten bevinden in plaats van voorraad op de productielocatie aan te leggen.

Als er geen directe vraag naar een product is, moeten de producten worden opgeslagen op magazijnlocaties op de productielocatie. Dit proces wordt ook wel *opportunistisch cross-docken* genoemd. Hiermee wordt aangegeven dat als er een directe vraag voor verzending van het product is, deze gelegenheid moet worden gebruikt in plaats van het product voor interne opslag op te slaan.

Het volgende voorbeeld toont drie variaties van een stroom die begint aan het einde van de productieregel (2).

Een product wordt gereedgemeld bij de productie-uitvoerlocatie (3) en een heftruckchauffeur haalt de pallet op deze locatie (3) op.

-   Als er een geplande activiteit (6) is voor het overbrengen van het product van de productie (1) naar een distributiecentrum (7), wordt de chauffeur door het systeem verteld dat de pallet moet worden geplaatst bij een laaddeurlocatie (4).
-   Als er al een trailer aan de laaddeur is toegewezen, wordt de vrachtwagenchauffeur doorgestuurd om het product rechtstreeks op de trailer te laden.
-   Als er geen geplande activiteit is voor het overbrengen van het product, wordt de heftruckchauffeur doorgestuurd om het product op een locatie in het interne magazijn te plaatsen (5).

[![opportunistisch cross-docken.](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Cross-docken configureren
U configureert het proces van cross-docken in **Werkbeleid**. Een werkbeleid bevat een werkordertype, locatie en product. In het volgende voorbeeld wordt cross-docken geconfigureerd voor product X en locatie Y.

#### <a name="work-order-types"></a>Werkordertypen

-   Werkordertype: eindproducten opslaan
-   Werkaanmaakmethode: cross-docken
-   Naam van beleid voor cross-docken: overboekingsorders

#### <a name="inventory-locations"></a>Voorraadlocaties

-   Magazijn: 51
-   Locatie: Y

#### <a name="products"></a>Producten

-   Artikelnummer: X

Op dit moment kan cross-docken worden geconfigureerd voor slechts twee werkordertypen:

-   Eindproducten wegzetten
-   Coproducten en bijproducten wegzetten

In het **Beleid voor cross-docken** definieert u welke documenttypen van toepassing zijn voor cross-docken. Het enige documenttype dat momenteel wordt ondersteund, is **overboekingsorders**. In het volgende voorbeeld ziet u de configuratie van een beleid voor cross-docken.

### <a name="cross-docking-policy-name-transfer-order"></a>Naam van beleid voor cross-docken: overboekingsorder

- Volgnummer: 10
  -   Werkordertype: transferuitgifte
- Voor verzoek om cross-docken is locatie vereist: Onwaar
- Strategie voor cross-docken: datum en tijd

### <a name="sequence-number"></a>Volgnummer

Met **volgnummer** wordt de prioriteit van het documenttype aangegeven. Momenteel is **Transferuitgifte** het enige documenttype dat wordt ondersteund. Het volgnummer wordt daarom alleen relevant wanneer er meer werkordertypen worden ondersteund.

### <a name="cross-docking-policy"></a>Beleid voor cross-docken

Met het beleid voor cross-docken wordt ook het beleid voor de prioriteitstelling van overboekingsordervraag ingesteld. Als er bijvoorbeeld meerdere overboekingsorders bestaan voor hetzelfde product, wordt de prioriteitstelling tussen de orders bepaald aan de hand van de geplande datum en tijd die zijn ingesteld voor de lading en die zijn gekoppeld aan de overboekingsorder. De geplande datum en tijd kunnen rechtstreeks worden ingesteld voor de lading. Ze kunnen ook worden ingesteld op basis van een **afspraakplanning** die is gekoppeld aan de lading. De prioriteitstelling wordt bepaald door de strategie voor cross-docken. Er is momenteel slechts één strategie: **Datum en tijd**.

### <a name="cross-docking-demand-requires-location"></a>Voor verzoek om cross-docken is locatie vereist

In het beleid voor cross-docken kunt u een criterium instellen om te vereisen dat overboekingsorders een toegewezen locatie hebben om in aanmerking te komen voor cross-docken. Dit criterium wordt ingesteld in het veld **Voor verzoek om cross-docken is locatie vereist**. De locatie in de afspraakplanning die is gekoppeld aan de lading, wordt gebruikt als de uiteindelijke locatie voor de goederen waarop cross-docken wordt toegepast. De uiteindelijke locatie voor de goederen waarop cross-docken wordt toegepast, wordt bepaald door de locatierichtlijn voor **Transferuitgifte** voor het werkordertype **Wegzetten**. Het kan nuttig zijn om het veld **Voor verzoek om cross-docken is locatie vereist** in te stellen in een scenario waarin op de eindproducten cross-docken alleen moet worden toegepast als een trailer is toegewezen aan een laaddeur. In dit scenario worden de goederen rechtstreeks vanuit de productieregel naar de trailer verplaatst. Wanneer een trailer wordt toegewezen aan de laaddeur, wijst een gebruiker de locatie aan de afspraakplanning toe waardoor de locatie van toepassing is voor cross-docken. In de volgende gedeelten worden twee voorbeelden uitgelegd.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Scenario 1: cross-docken van productie naar overboekingsorders

Nadat een product is gereedgemeld voor de productielijn, wordt het overgebracht naar een laaddeurlocatie waar het wordt geladen in een vrachtwagen en overgeplaatst naar een distributiecentrum. Gebruik USMF van bedrijf.

1.  Schakel een nieuwe nummerreeks voor cross-docken in. Ga naar de pagina **Nummerreeksen** en selecteer de knop **Genereren**. Een wizard begeleidt u in het proces.
2.  Maak een beleid voor cross-docken. Ga naar de pagina **Beleid voor cross-docken** en maak een nieuw beleid met de naam **Cross-docken voor overboekingsorder**. Houd er rekening mee dat u alleen het werkordertype **Transferuitgifte** kunt selecteren en dat de enige beschikbare strategie **Datum en tijd** is.
3.  Maak een werkbeleid. Ga naar de pagina **Werkbeleidsregels** en maak een nieuw werkbeleid met de naam **Cross-docken L0101**.
4.  Stel ladingen zo in dat ze automatisch worden gemaakt voor overboekingsorders. Stel in de magazijnparameters ladingen zo in dat ze automatisch worden gemaakt wanneer er overboekingsorders worden gemaakt. Een belasting is een vereiste om de overboekingsorder in aanmerking te laten komen voor cross-docken.
5.  Stel de artikelladingtoewijzing in. Ga naar de pagina **Ladingtoewijzing artikel** en stel een standaardsjabloon voor lading in voor de artikelgroep **CarAudio**. Met deze toewijzing wordt de ladingsjabloon automatisch ingevoegd in de lading wanneer de overboekingsorder wordt gemaakt.
6.  Een overboekingsorder maken. Maak de overboekingsorder voor artikelnummer L0101. Hoeveelheid = 20.
7.  Geef de overboekingsorder vrij via de workbench van de ladingplanning. Selecteer op het tabblad **Verzenden** de menuopdracht voor de ladingplanningworkbench en selecteer in het menu **Vrijgeven** van de ladingregel **Vrijgave naar magazijn**. Er is nu een open waveregel van het type **Transferuitgifte** aanwezig voor de overboekingsorder.
8.  Maak een productieorder. Ga naar de lijstpagina **Productieorder** en maak een productieorder voor product L0101. Hoeveelheid = 20. Maak een raming en start de productieorder. Houd er rekening mee dat het veld **Orderverzamellijst nu boeken** blijft ingesteld op **Nee**.
9.  Meld gereed via het mobiele apparaat. Ga naar de portal van het mobiele apparaat en selecteer menuopdracht **Rapporteren als voltooid en wegzetten**. Meld nu L0101 gereed via het handheldapparaat. Hoeveelheid = 10. De locatie voor plaatsing is **LAADDEUR**. Deze locatie vindt u in de locatierichtlijn **Transferuitgifte** voor het werkordertype **Plaatsen**. U ziet ook dat werk van het type **Transferuitgifte** is gemaakt en is voltooid. Ga naar de werkdetails van de overboekingsorder om het werk te controleren.
10. Rapporteer nu 10 stuks extra vanaf het mobiele apparaat. De locatie voor plaatsing is opnieuw **LAADDEUR**. U ziet ook dat nieuw werk van het type **Transferuitgifte** is gemaakt voor de 10 stuks.
11. Probeer nu 20 stuks meer op de productieorder te starten en probeer vervolgens 20 stuks gereed te melden met behulp van het handheldapparaat. Deze keer wordt de locatie **LP-001** voorgesteld als de locatie voor plaatsing. Deze locatie vindt u via de locatierichtlijn voor **Eindproducten wegzetten**. Deze locatierichtlijn wordt gebruikt, omdat er geen gelegenheid voor cross-docken bestaat. De overboekingsorder voor LP-001 is volledig afgehandeld door de twee activiteiten voor cross-docken in stap 9 en 10. Werk van het type **Eindproducten wegzetten** is gemaakt en verwerkt.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Scenario 2: cross-docken van productie naar overboekingsorders met een afspraakplanning

Nadat een product voor de productieregel gereed is gemeld, wordt het overgebracht naar een laaddeurlocatie die wordt geïdentificeerd door een afspraakplanning voor de laaddeurlocaties. Gebruik USMF van bedrijf.

1.  Wijzig het beleid voor cross-docken. Wijzig het beleid voor cross-docken dat u hebt gemaakt in scenario 1 door het selectievakje **Voor verzoek om cross-docken is locatie vereist** in te schakelen.
2.  Maak een nieuwe overboekingsorder.
3.  Open de **Workbench ladingplanning**.
4.  Ga van de ladingplanningworkbench naar de sectie **Ladingen** en selecteer **Afspraakplanning** in het menu **Transport** om een nieuwe afspraakplanning te maken. Houd er rekening mee dat de afspraakplanning een verwijzing bevat naar de overboekingsorder in het veld **Ordernummer**. In het veld **Geplande begindatum en -tijd op locatie** kunt u de datum en tijd instellen voor de afspraak. Deze datum en tijd worden gebruikt wanneer bij het cross-docken van vraag prioriteit wordt verleend tijdens het cross-docken. Met de datum en tijd die u in dit veld instelt, wordt het veld **Geplande datum en tijd voor verzending lading** voor de bijbehorende lading bijgewerkt. De locatie op het sneltabblad **Verzendgegevens** bepaalt de locatie waar de overboekingsorder wordt verzonden.
5.  Geef de order vrij aan het magazijn in de **Workbench ladingplanning**.
6.  Maak een productieorder voor artikelnummer **L0101** en stel de status in op **Gestart** met een hoeveelheid van 20.
7.  Meld gereed via het mobiele apparaat.
8.  Ga naar de portal van het mobiele apparaat en selecteer de menuopdracht **Rapporteren als voltooid en wegzetten**.
9.  Meld artikelnummer **L0101** gereed via het handheldapparaat. De locatie voor plaatsing is nu **LAADDEUR 2**. Deze locatie vindt u in de planning van de afspraakplanning in plaats van de locatierichtlijn **Ontvangst van overboekingsorder**.

### <a name="additional-information"></a>Aanvullende gegevens

-   Het scenario van cross-docken wordt ondersteund voor batch- en serie gecontroleerde artikelen, waarbij zowel de batch- als serienummerdimensies boven en onder de locatie in de reserveringshiërarchie zijn gedefinieerd. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]