---
title: Prestaties van hoofdplanning verbeteren
description: In dit onderwerp worden de verschillende opties beschreven waarmee u de prestaties van de hoofdplanning kunt verbeteren of problemen kunt oplossen.
author: t-benebo
manager: tfehr
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 54f39793b6e8b24a13a4b80b59ba35f10e8f3da5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237468"
---
# <a name="improve-master-planning-performance"></a>Prestaties van hoofdplanning verbeteren

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de verschillende opties beschreven waarmee u de prestaties van de hoofdplanning kunt verbeteren of problemen kunt oplossen. Het bevat informatie over parameters en instellingen en over aanbevolen configuraties en acties. Daarnaast bevat het een overzicht van alle belangrijke parameters waarmee u rekening moet houden wanneer u langlopende hoofdplanningstaken uitvoert.

Dit onderwerp is bedoeld voor systeembeheerders of IT-gebruikers die de mogelijkheid hebben om problemen op te lossen. Het is ook bedoeld voor productie- of aanbodplanners, omdat hierin informatie wordt opgenomen over parameters die zijn gerelateerd aan bedrijfsplanningsvereisten. 

## <a name="parameters-related-to-master-planning-performance"></a>Parameters die zijn gerelateerd aan hoofdplanningsprestaties

Verschillende parameters beïnvloeden de uitvoeringstijd van de hoofdplanning en moeten worden overwogen.

### <a name="number-of-threads"></a>Aantal threads

Met de parameter **Aantal threads** kunt u het hoofdplanningsproces aanpassen, voor betere prestaties voor de specifieke gegevensset. Met deze parameter wordt het totale aantal threads opgegeven dat wordt gebruikt om de hoofdplanning uit te voeren. Dit veroorzaakt parallellisatie van de uitvoering van de hoofdplanning en hierdoor wordt de uitvoeringstijd verlaagd. 

U kunt de parameter **Aantal threads** in het dialoogvenster **Hoofdplanningsuitvoering** instellen. Als u dit dialoogvenster wilt openen, gaat u naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Hoofdplanning** of selecteert u **Uitvoeren** in het werkgebied **Hoofdplanning**. Om de beste waarde voor deze parameter te bepalen, moet u gebruikmaken van een proefondervindelijk proces. U kunt echter de volgende formules gebruiken om een beginwaarde te berekenen:

- **Als productie uw bedrijfstak is:** (aantal threads) = (aantal geplande orders ÷ 1000)
- **Anders:** (aantal threads) = (aantal artikelen ÷ 1000)

Het aantal helpers dat tijdens de hoofdplanning wordt gebruikt, moet kleiner dan of gelijk zijn aan het maximum aantal threads dat op de batchserver is toegestaan. Als het aantal helpers groter is dan het aantal threads op de batchserver, werken de extra threads niet.

> [!NOTE]
> Een instelling van **0** (nul) voor de parameter **Aantal threads** verhoogt de uitvoeringstijd van de hoofdplanning. Daarom is het raadzaam altijd een waarde in te stellen die hoger is dan 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Aantal taken in de taakbundel van de helper

Als u de instelling **Aantal taken in de taakbundel** (de bundelgrootte) wijzigt, kunt u mogelijk de uitvoeringstijd verkorten. Deze instelling bepaalt het aantal artikelen dat met één helper gezamenlijk wordt gepland.

U kunt de parameter **Aantal taken in de taakbundel** in de sectie **Prestaties** op het tabblad **Algemeen** van de pagina **Parameters hoofdplanning** instellen (**Hoofdplanning \> Instellen \> Parameters hoofdplanning**). De beste waarde voor deze parameter is afhankelijk van uw gegevens. Daarom is het raadzaam om te beginnen met de waarde **1** en vervolgens een proefondervindelijk proces te gebruiken om de beste waarde voor uw instellingen te bepalen.

Over het algemeen is het raadzaam om het aantal taken te verhogen wanneer het aantal artikelen erg groot is (in de honderdduizenden). Anders moet u het aantal taken verminderen. Houd rekening met de volgende aanbevelingen voor de volgende specifieke industrieën:

- In de detailhandel- en distributiesector, met een groot aantal onafhankelijke artikelen, gebruikt u een groot aantal helpers, omdat er geen afhankelijkheid bestaat tussen artikelen. 
- In de productie-industrie, waar veel met stuklijsten en gedeelde subonderdelen wordt gewerkt, kunt u minder helpers gebruiken omdat afhankelijkheden tussen artikelen wachttijden kunnen veroorzaken.

> [!TIP]
> Als u prestatieproblemen ondervindt, is het raadzaam de instelling **Aantal helpers in taakbundel** te beperken tot **1**. U kunt vervolgens de het proefondervindelijke proces starten om de beste waarde voor uw instellingen te vinden. Over het algemeen doen zich prestatieproblemen voor wanneer de verwerking van een bepaald artikel langer duurt dan voor de overige artikelen. In dit geval ziet u dat twee volgende taken met de status **Behoefteplanning** in de uitvoering van de hoofdplanning veel tijd in beslag nemen om te worden uitgevoerd. In extreme gevallen kan dit verschil tot 30 minuten oplopen. U kunt afleiden hoeveel tijd de uitvoering van taken kost door de duur van elke taak te bekijken.

### <a name="use-of-cache"></a>Gebruik van cache

Met de parameter **Gebruik van cache** kunt u het hoofdplanningsproces aanpassen, zodat het beter presteert voor de specifieke gegevensset. U kunt dit bijvoorbeeld aanpassen om de volgende resultaten te bereiken:

- Als er meer cachebewerkingen worden uitgevoerd, worden er meer gegevens verzameld in het gegevensgeheugen. De verwachting is dat de gegevens later opnieuw worden gebruikt. Als de gegevens zich in het geheugen bevinden, kunt u bepaalde databaseaanvragen opslaan. Als er meer cachebewerkingen worden uitgevoerd, neemt de geheugenvereisten echter toe.
- Als er minder cachebewerkingen wordt uitgevoerd, moeten dezelfde gegevens mogelijk vaker uit de database worden opgehaald. Bovendien worden in AOS (Application Object Server) weinig gegevens in het geheugen opgeslagen tijdens het proces.

Het is moeilijk te voorspellen welke optie beter is, omdat elk geval niet alleen afhankelijk is van de gegevens, maar ook van de hardware. Omdat bij minder cachebewerkingen de databaseserver minder extra wordt belast, is het waarschijnlijk niet verstandig om deze optie te gebruiken als de database server al overbelast is.

U kunt de parameter **Gebruik van cache** in de sectie **Prestaties** op het tabblad **Algemeen** van de pagina **Parameters hoofdplanning** instellen (**Hoofdplanning \> Instellen \> Parameters hoofdplanning**). De effectiviteit van cachebewerkingen hangt sterk af van de klantgegevens. Als cachegegevens bijvoorbeeld nooit nodig zijn, verspilt u alleen geheugen als u gegevens opslaat tot aan het einde van het planningsproces. Als u in dit geval minder cachebewerkingen configureert, kunnen de prestaties toenemen, omdat er minder geheugen nodig is voor AOS en er serverbronnen worden vrijgemaakt voor andere taken.

> [!TIP]
> Over het algemeen is het raadzaam om de parameter **Gebruik van cache** in te stellen op **Maximum**, omdat de parameter bedoeld is als functie voor het verbeteren van de prestaties. U wordt aangeraden de parameter in te stellen op **Minimum** als u lokaal werkt werkt en beperkt geheugen hebt (ongeveer 2 gigabyte \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Aantal orders fiatteringsbundel

Met de parameter **Aantal orders fiatteringsbundel** geeft u op hoeveel orders per keer worden verwerkt door elke thread/batch. Dit veroorzaakt parallellisatie van het proces voor automatisch fiattering.

U kunt de parameter **Aantal orders fiatteringsbundel** in de sectie **Prestaties** op het tabblad **Algemeen** van de pagina **Parameters hoofdplanning** instellen (**Hoofdplanning \> Instellen \> Parameters hoofdplanning**). Parallellisatie van het proces voor automatisch fiatteren is gebaseerd op de orders die samen moeten worden verwerkt. Als deze parameter bijvoorbeeld is ingesteld op **50**, worden door elke thread of batchtaak 50 orders tegelijk opgehaald en tegelijkertijd uitgevoerd. U wordt aangeraden proefondervindelijk de beste waarde proberen te vinden. U kunt echter de volgende formule gebruiken om een beginwaarde te berekenen:

(Aantal orders per bundel) = (aantal vraagartikelen ÷ aantal threads)

> [!NOTE]
> Als u de parameter **Aantal orders fiatteringsbundel** instelt op **0** (nul), wordt het proces voor automatisch fiatteren niet geparallelliseerd. Het gehele proces wordt uitgevoerd voor één batchtaak en heeft een cumulatieve uitvoeringstijd. Daarom neemt de uitvoeringstijd van de hoofdplanning toe. Daarom is het raadzaam om deze parameter in te stellen op een waarde die groter is dan **0** (nul).

### <a name="time-fences"></a>Time fences

Met time fences geeft u aan hoe ver in de toekomst de berekeningen en andere vereisten moeten worden berekend door de hoofdplanning. Hoe groter de time fence, hoe langer het duurt om de hoofdplanning uit te voeren. Stel de time fences daarom in op basis van uw zakelijke behoeften. Zie [Hoofdplanning instellen](master-planning-setup.md) voor meer informatie over time fences.

### <a name="actions"></a>Acties

Onder de time fences kunt u ook de parameter **Actiebericht** vinden. De berekening van actieberichten veroorzaakt een langere uitvoeringstijd voor de hoofdplanning. Als actieberichten niet regelmatig worden geanalyseerd en toegepast (dagelijks, wekelijks, enzovoort), kunt u overwegen de berekening uit te schakelen tijdens de uitvoering van de hoofdplanning. Als u de berekening wilt uitschakelen, stelt u op de pagina **Hoofdplannen** (**Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**) de time fence **Actiebericht** op **0** (nul) in. Controleer ook of de instelling **Actiebericht** is uitgeschakeld voor alle behoefteplanningsgroepen.

### <a name="futures"></a>Uitstel

De berekening van uitstel veroorzaakt een langere uitvoeringstijd voor de hoofdplanning. Als u geen stuklijsten hebt gepland of als vertragingen niet van voorraad aan vraag moeten worden doorgegeven tijdens de planning, kunt u berekeningen van uitstel uitschakelen tijdens de hoofdplanning. U kunt de berekeningen uitschakelen door de time fence **Uitstel** in te stellen op **0** (nul) voor het hoofdplan dat u uitvoert. Controleer ook of de instelling **Uitstel** is uitgeschakeld voor alle behoefteplanningsgroepen.

## <a name="one-heavy-routine-at-a-time"></a>Eén zware routine tegelijk

Wanneer u de hoofdplanning plant, moet u niet tegelijkertijd andere batchtaken plannen. Zorg er vooral voor dat u geen andere zware routines, zoals voorraadsluiting, tegelijkertijd plant.

## <a name="review-the-session-log"></a>Het sessielogboek controleren

Het systeem kan aanvullende informatie verzamelen over de taken die worden uitgevoerd tijdens de hoofdplanning. Als u deze gegevens door het systeem wilt laten verzamelen, schakelt u de instelling **Verwerkingstijd traceren** in het dialoogvenster **Hoofdplanningsuitvoering** in. De verzamelde informatie kan u helpen om knelpunten in de uitvoering te vinden. Wanneer de parameter **Aantal taken in de taakbundel van de helper** bijvoorbeeld is ingesteld op **1**, kunt u het item identificeren dat de langste uitvoeringstijd heeft. U kunt ook de uitvoeringstijden voor de verschillende threads met de status **Behoefteplanning** vergelijken en de duur van elke taak vergelijken.

Als u de hoofdplanningsuitvoering van uw systeem wilt controleren, volgt u een van deze stappen.

- Selecteer in het werkgebied **Hoofdplanning** een hoofdplan in het vervolgkeuzemenu en selecteer vervolgens **Historie** in de tegel **Hoofdplanning**. Selecteer een taak, selecteer **Query's** op het sneltabblad en selecteer vervolgens **Taakduur verwerken**.
- Selecteer op de pagina **Hoofdplannen** een plan in het linkerdeelvenster en selecteer vervolgens **Historie** op het sneltabblad. Selecteer een taak, selecteer **Query's** op het sneltabblad en selecteer vervolgens **Taakduur verwerken**.

Houd rekening met het volgende wanneer u het sessielogboek controleert:

- **Bijwerken** mag niet veel tijd kosten (over het algemeen niet meer dan 30 minuten). Dit is echter een proces met één thread.
- **Plan kopiëren** mag niet veel tijd kosten (dit moet ongeveer één minuut duren).
- **Automatische fiattering** duurt doorgaans ongeveer 30 minuten. Het kan echter meerdere uren in beslag nemen, afhankelijk van het aantal orders en de complexiteit van de artikelen.
- **Automatische fiattering** moet minder tijd in beslag nemen dan **Behoefteplanning**.
- **Behoefteplanning** moet in verhouding met de rest het langst duren.
- **Actie en** **toekomstige berichten** kan veel tijd in beslag nemen, afhankelijk van de gegevens en het aantal stuklijsten.

## <a name="filtering-of-items"></a>Filteren van artikelen

Filters die worden toegepast in het dialoogvenster **Hoofdplanningsuitvoering**, beïnvloeden de duur van de uitvoering van de hoofdplanning. Ga naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Hoofdplanning** of selecteer **Uitvoeren** in het werkgebied **Hoofdplanning**. Als u artikelen wilt uitsluiten van de uitvoering, is het raadzaam om te filteren op de levenscyclusstatus van het artikel (niet op artikelnummers). Wanneer u filtert op levenscyclusstatus, neemt het bijwerkproces minder tijd in beslag dan wanneer u filtert op artikelnummers.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Automatisch filteren op artikelen met directe vraag

Om de uitvoeringstijd van de hoofdplanning te verbeteren, kunt u ervoor kiezen alleen artikelen met directe vraag op te nemen. Dit filter kan alleen worden gebruikt voor een volledige hoofdplanningsuitvoering zonder dat er andere filters zijn toegepast in het veld **Op te nemen records**. Bij een hoofdplanningsuitvoering met filters wordt de instelling **Automatisch filteren op artikelen met directe vraag** genegeerd.

Het veld **Automatisch filteren op artikelen met directe vraag** is te vinden op de pagina **Parameters hoofdplanning** en kan worden gebruikt met voor- en naverwerkingsinstellingen.

### <a name="pre-processing"></a>Voorverwerking
De parameter **Voorverwerking: automatisch filteren op artikelen met directe vraag** zorgt ervoor dat de voorbewerkingsfase van de hoofdplanning alleen artikelen bevat die voldoen aan ten minste een van de volgende voorwaarden:
  - Het artikel heeft een verwachte ontvangst of uitgifte, zoals een inkooporder, verkooporder, offerte, transferorder of productieorder. 
  - Voor het artikel bestaat artikelbehoefteplanning met veiligheidsvoorraad (minimale voorhanden voorraad).
  - Er bestaat prognosevraag na vandaag voor het artikel.
  - Er bestaat prognoseaanbod na vandaag voor het artikel.
  - Het artikel bevat de continuïteitsregels van de callcentermodule die nog moeten worden gemaakt.

> [!NOTE]
> Een artikel met fysiek beschikbare voorhanden voorraad geeft geen behoeftetransactie weer omdat er geen vraag naar het artikel is.

### <a name="post-processing"></a>Naverwerking
De optie **Naverwerking: automatisch filteren op artikelen met directe vraag** is alleen relevant als u **Behoefte van stuklijstversie** in uw behoefteplanningsgroepen instelt. Anders hoeft u de parameter niet in te schakelen. 

Voordat de behoefteplanningsstap wordt gestart, is er een stap vóór de behoefteplanning waarbij artikelen opnieuw worden verwerkt als de behoefteplanningsinstelling **Behoefte van stuklijstversie** is ingeschakeld. Dit wordt gedaan om ervoor te zorgen dat artikelen uit de vereiste stuklijstversie worden gepland. Voor artikelen waarvoor ervan wordt uitgegaan dat er tijdens de voorverwerking vraag voor bestaat, is geen vraag meer en deze moeten daarom worden uitgesloten van de planningsuitvoering.

## <a name="performance-checklist-summary"></a>Overzicht van prestatiecontrolelijst

- **Aantal threads**: stel een waarde groter dan **0** (nul) in.
- **Aantal taken in de taakbundel van de helper**: stel een waarde groter dan **0** (nul) in. (gebruik de formules die eerder in dit onderwerp zijn beschreven.)
- **Gebruik van cache**: stel **Maximum** in, tenzij het systeem weinig geheugen heeft.
- **Aantal orders fiatteringsbundel**: stel een waarde groter dan **0** (nul) in. (gebruik de formule die eerder in dit onderwerp is beschreven.)
- **Time fences**: pas dit aan op basis van uw bedrijfsbehoeften.
- **Acties en uitstel**: schakel dit uit als u hiervan geen gebruikmaakt.
- **Eén zware routine tegelijk**: voer een hoofdplanning niet tegelijk met een andere zware routine uit.
- **Het sessielogboek controleren**.
- **Filteren van artikelen**: gebruik de levenscyclusstatus om artikelen uit de uitvoering van de hoofdplanning uit te sluiten. (Gebruik de artikelnummers niet.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]