---
title: "Dimensiehiërarchie"
description: "Dit onderwerp bevat informatie over dimensiehiërarchieën. U gebruikt een dimensiehiërarchie om de rapportagestructuur, het kostenbeleid en de beveiligingsinstelling in Kostprijsboekhouding te definiëren."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dcbab70d2057a2eb252538a51343fa8bae16873d
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="dimension-hierarchy"></a>Dimensiehiërarchie

[!include[banner](../includes/banner.md)]

Dit onderwerp bevat informatie over dimensiehiërarchieën. U gebruikt een dimensiehiërarchie om de rapportagestructuur, het kostenbeleid en de beveiligingsinstelling in Kostprijsboekhouding te definiëren.  

## <a name="overview"></a>Overzicht

Dimensiehiërarchieën worden op verschillende plaatsen in Kostprijsboekhouding gebruikt. Met een dimensiehiërarchie kunt u de volgende informatie definiëren:

-  De rapportagestructuur die past bij de behoeften van de organisatie
-  Kostenbeleid
-  De beveiligingsinstelling

Hier volgt een voorbeeld van een dimensiehiërarchie.

![Voorbeeld van een dimensiehiërarchie](./media/dimension-hierarchy.png)

Een dimensiehiërarchie kan worden gemaakt voor de volgende typen dimensies:

-  Dimensies van kostenelement
-  Dimensies van kostenobject
-  Statistische dimensies

> [!NOTE]
> - U kunt meerdere dimensiehiërarchieën voor dezelfde dimensie maken als verschillende perspectieven vereist zijn.
> - Een dimensiehiërarchie kan aan slechts één dimensie worden gekoppeld.
> - Een dimensiehiërarchie kan een onbeperkt aantal niveaus in de structuur hebben. Alle niveaus zijn beschikbaar in het werkgebied **Kostenbeheer**. Wanneer u Microsoft Excel of Microsoft Power BI voor rapportagedoeleinden gebruikt, worden alleen de eerste 15 niveaus van de dimensiehiërarchie geëxporteerd. Deze beperking geldt omdat zowel Excel als Power BI een vast schema vereisen.
> - Een dimensiehiërarchie is niet datumeffectief. Daarom wordt een wijziging in een dimensiehiërarchie onmiddellijk in de record opgeslagen en kunt u de datum vóór en de datum na niet vergelijken.

## <a name="dimension-hierarchy-type"></a>Type dimensiehiërarchie

Wanneer u een nieuwe dimensiehiërarchie maakt, moet u een hiërarchietype selecteren. Ga naar **Kostprijsboekhouding** > **Dimensies** > **Dimensiehiërarchieën**. Klik op **Nieuw** en selecteer een type dimensiehiërarchie. U kunt **Hiërarchie dimensiecategorisatie** of **Hiërarchie dimensieclassificatie** selecteren.

### <a name="dimension-categorization-hierarchy"></a>Hiërarchie dimensiecategorisatie

Het type **Hiërarchie dimensiecategorisatie** wordt gebruikt voor rapportagedoeleinden. Dit type ondersteunt alleen de kostenelementdimensies. Wanneer u dit type gebruikt, gelden de volgende regels:

-  Een dimensielid kan meerdere keren worden gekoppeld in de hiërarchiestructuur.
-  U kunt een kostenelementdimensielid in verschillende knooppunten plaatsen door een kostengedrag aan het bladknooppunt toe te wijzen.

### <a name="dimension-classification-hierarchy"></a>Hiërarchie dimensieclassificatie

Het type **Hiërarchie dimensieclassificatie** wordt gebruikt om regels voor rapportagedoeleinden te definiëren. Het biedt ondersteuning voor alle dimensies, zoals kostenobjecten, kostenelementen en statistische dimensies. Als u dit type selecteert, kan een dimensielid slechts één keer in de hiërarchiestructuur worden gekoppeld.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Een dimensiehiërarchie maken en onderhouden

Een dimensiehiërarchie wordt gemaakt als een boomstructuur die knooppunt- en bladknooppuntrelaties heeft.

-  Een knooppunt kan 1:_n_ subknooppunten hebben.
-  Aan een knooppunt kunnen niet zowel subknooppunten als bladknooppunten worden toegewezen.
-  Een bladknooppunt kan alleen op het laagste niveau in de hiërarchie worden toegewezen.

### <a name="example"></a>Voorbeeld

Een klein bedrijf heeft de volgende organisatiestructuur, waarin Financiën en Personeelszaken afdelingen zijn die onder Administatie vallen, en Assemblage en Verpakking onder Productie.

![Voorbeeld van een organisatiestructuur](./media/dimension-hierarchy-org.png)

Een kostenobjectdimensie vertegenwoordigt alle kostenplaatsen in de organisatie.

- Dimensie van kostenobject
    - Kostenplaatsen

De kostenobjectdimensie die alle kostenplaatsen vertegenwoordigt, kan worden ingesteld zoals hier wordt weergegeven.

| Kostenplaatsen | Omschrijving |
|--------------|-------------|
| CC001        | HR          |
| CC002        | Financiën     |
| CC003        | Btw         |
| CC007        | Leveranciers/Klanten       |
| CC005        | Assembleren    |
| CC006        | Verpakking   |

Een kostenelementdimensie vertegenwoordigt alle kostenelementen in de organisatie.

- Dimensie van kostenelement
    - Kostenelementen

De kostenelementdimensie die alle kostenelementen vertegenwoordigt, kan worden ingesteld zoals hier wordt weergegeven.

| Kostenelementen | Omschrijving |
|---------------|-------------|
| 10001         | Elektriciteit |
| 10010         | Schoonmaken    |
| 10011         | Verwarming     |
| 40001         | COGS        |

Een dimensiehiërarchie die voldoet aan de rapportagevereisten van de organisatie kan worden ingesteld zoals hier wordt weergegeven.

**Gegevens van dimensiehiërarchie**

| Naam van dimensiehiërarchie | Dimensie    | Naam van type dimensiehiërarchie      | Hiërarchie van toegangslijsten |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatie             | Kostenplaatsen | Hiërarchie dimensieclassificatie | Nee                    |

De dimensiehiërarchie voor rapportage kan worden ingesteld zoals hier wordt weergegeven.

|                   | Bereiken van dimensieleden   |                         |
|-------------------|---------------------------|-------------------------|
| **Knooppunten**         | **Van dimensielid** | **Tot dimensielid** |
| Organisatie      |                           |                         |
| &nbsp;&nbsp;Beheer         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Financiën   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | CC001                     | CC001                   |
| &nbsp;&nbsp;Productie    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Verpakking | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembleren  | CC006                     | CC006                   |

Een dimensiehiërarchie die voldoet aan de beleidsvereiste kan worden ingesteld zoals hier wordt weergegeven.

**Gegevens van dimensiehiërarchie**

| Naam van dimensiehiërarchie | Dimensie     | Naam van type dimensiehiërarchie      |
|--------------------------|---------------|------------------------------------|
| Kostengedrag            | Kostenelementen | Hiërarchie dimensieclassificatie |

De dimensiehiërarchie voor het beleid kan worden ingesteld zoals hier wordt weergegeven.

|                   | Bereiken van dimensieleden   |                         |
|-------------------|---------------------------|-------------------------|
| **Knooppunten**         | **Van dimensielid** | **Tot dimensielid** |
| Kostengedrag     |                           |                         |
| &nbsp;&nbsp;Vaste kosten    | 10001                     | 10011                   |
|&nbsp;&nbsp;Variabele kosten | 40001                     | 40010                   |

> [!NOTE]
> Onder **Bereiken van dimensieleden** kan een knooppunt 1: _n_ bereiken van dimensieleden bevatten. U kunt de dimensielid-id´s invoegen die nog niet bestaan als dimensieleden. Deze benadering maakt de hiërarchie flexibel voor de toekomst.  

### <a name="copy-a-hierarchy"></a>Een hiërarchie kopiëren

U kunt een huidige dimensiehiërarchie kopiëren als uitgangspunt voor een nieuwe dimensiehiërarchie. Deze benadering kan nuttig zijn als u de vorige dimensiehiërarchie wilt vergelijken met de nieuwe dimensiehiërarchie.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Knooppunten in een hiërarchie opnieuw rangschikken

U kunt een knooppunt omhoog en omlaag verplaatsen binnen het huidige niveau in de structuur. Op deze manier u kunt de volgorde van knooppunten opnieuw rangschikken in het werkgebied **Kostenbeheer**.

U verplaatst een knooppunt naar een nieuwe locatie in de hiërarchie door het doelknooppunt te selecteren. U kunt een knooppunt op twee manieren verplaatsen:

- **Verplaatsen onder**: verplaats het geselecteerde knooppunt van de huidige positie in de hiërarchie en voeg het **onder** het geselecteerde doelknooppunt in.
- **Verplaatsen na**: verplaats het geselecteerde knooppunt van de huidige positie in de hiërarchie en voeg het **na** het geselecteerde doelknooppunt in op het niveau ervan in de hiërarchie.

> [!NOTE] 
> De volgorde van de knooppunten wordt niet behouden wanneer u gegevens naar Excel of Power BI exporteert, omdat deze programma's standaard een alfanumerieke sorteervolgorde gebruiken. U moet de volgorde handmatig opnieuw rangschikken.

## <a name="define-dimension-hierarchies-for-reporting"></a>Dimensiehiërarchieën definiëren rapportage

Dimensiehiërarchieën zijn belangrijk voor rapportage. U kunt er de specifieke structuur mee definiëren die past in de afzonderlijke organisatie. Met de samenvoegingen die zijn uitgevoerd op het knooppuntniveau van de dimensiehiërarchie, kunnen belanghebbenden op elk niveau van de organisatie gegevens op elk niveau bekijken.

Dimensiehiërarchieën zijn beschikbaar in de volgende rapportageprogramma's. Deze benadering garandeert consistentie in de rapportagestructuur.

- Werkgebied **Kostenbeheer** (client):

    - Beheerd door configuratie.

- Werkgebied **Kostenbeheer** (mobiele toepassing):

    - Beheerd door configuratie.

- Excel

    - Biedt de optie om specifieke dimensiehiërarchieën per exportdefinitie te selecteren:

        - Eén kostenelementdimensiehiërarchie (verplicht)
        - Eén kostenobjectdimensiehiërarchie (optioneel)
        - Eén statistische dimensiehiërarchie (optioneel)

- Power BI:

    - Alle dimensiehiërarchieën zijn beschikbaar.
    
Als u rapporten maakt met behulp van Excel of Power BI, worden alleen de eerste 15 niveaus van de dimensiehiërarchieën geëxporteerd. Deze beperking geldt omdat er een vast schema is vereist in Excel en Power BI. Als een hiërarchie meer dan 15 niveaus heeft, worden de extra niveaus niet geëxporteerd. De gestandaardiseerde tabel bevat een record voor elk dimensielid in de hiërarchie. Daarom vindt automatische samenvoeging plaats. Dit gedrag helpt ervoor te zorgen dat de saldi op elk van de 15 beschikbare niveaus in de hiërarchie nog steeds correct zijn.

Het volgende voorbeeld laat zien hoe een dimensiehiërarchie eruit kan zien in de rapportagestructuur.

| Dimensiehiërarchie van een kostenobject - niveau 1 | Dimensiehiërarchie van een kostenobject - niveau 2 | Dimensiehiërarchie van een kostenobject - niveau 3 | Dimensiehiërarchie van een kostenobject - niveau 4 | Dimensiehiërarchie van een kostenobject - niveau 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organisatie                              | Beheer                                     | Financiën                                   | CC002                                     |                                            |
| Organisatie                              | Beheer                                     | Financiën                                   | CC003                                     |                                            |
| Organisatie                              | Beheer                                     | Financiën                                   | CC007                                     |                                            |
| Organisatie                              | Beheer                                     | HR                                        | CC001                                     |                                            |
| Organisatie                              | Productie                                | Verpakking                                 | CC005                                     |                                            |
| Organisatie                              | Productie                                | Assembleren                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Dimensiehiërarchieën bijwerken die worden gebruikt voor rapportage 

In de loop van de tijd worden de dimensiehiërarchieën die worden gebruikt in de eerder genoemde rapportagefuncties bijgewerkt. U kunt dimensiehiërarchieën bijwerken door de client te vernieuwen.

- Werkgebied **Kostenbeheer** (client)
- Werkgebied **Kostenbeheer** (mobiele toepassing)

Updates van dimensiehiërarchieën worden elke 24 uur verzameld door een vooraf in cache opgeslagen taak. Nadat de geëxporteerde gegevens zijn bijgewerkt, zijn de bijgewerkte dimensiehiërarchieën beschikbaar in de volgende programma's:

- Excel
- Power BI

> [!NOTE] 
> Als u handmatig een update van de dimensiehiërarchiecache wilt activeren, kunt u een nieuwe export naar Excel maken voor de dimensiehiërarchie of -hiërarchieën die moet(en) worden bijgewerkt.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Dimensiehiërarchieën definiëren voor kostenbeleid

Kostprijsboekhouding bestaat uit meerdere beleidsregels waarin gedetailleerde regels worden gedefinieerd. U moet een of meer dimensiehiërarchieën voor de volgende beleidsregels definiëren:

- Kostengedrag
- Kostenverdeling
- Kostentoewijzing
- Kosten totaliseren

Dimensiehiërarchieën maken het eenvoudig om regels te maken. Om te voorkomen dat u regels voor elk dimensielid moet maken, kunt u profiteren van de samenvoegingen van dimensieleden die worden verschaft door dimensiehiërarchieniveaus. Als er overlappende regels zijn, moet u specifieke regels definiëren die door het systeem worden meegenomen wanneer de berekening van overhead wordt uitgevoerd.

### <a name="example-define-a-cost-behavior-policy"></a>Voorbeeld: een beleid voor kostengedrag definiëren

Een nieuw kostengedragbeleid wordt gemaakt en de juiste dimensiehiërarchieën worden toegewezen aan het beleid, zoals hier wordt weergegeven.

**Kostengedragbeleid**

| Beleidsnaam   | Dimensiehiërarchie van een kostenelement | Dimensiehiërarchie van een kostenobject | Valuta voor boekhouding |
|---------------|----------------------------------|---------------------------------|---------------------|
| Kostengedrag | Kostengedrag                    | Organisatie                    | EUR                 |

**Regels**

| Dimensiehiërarchieknooppunt van een kostenelement | Dimensiehiërarchieknooppunt van een kostenobject | Vast percentage | Vast bedrag | Geldig vanaf | Geldig tot |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Vaste kosten                            | Organisatie                         | 100,00           | 0,00         | 1/1/2017   | Nooit    |
| 10001                                 | Organisatie                         | 0,00             | 150,00       | 1/1/2017   | Nooit    |
| 10001 (\*)                             | Financiën                              |                  | 50,00        | 1/1/2017   | Nooit    |
| Kostengedrag of variabele kosten (\*\*)   | Organisatie                         | 0,00             | 0,00         | 1/1/2017   | Nooit    |

\* Het knooppunt van de variabele kosten is niet vereist. Als kosten niet worden geclassificeerd als vaste kosten, moeten dit variabele kosten zijn.

\*\* Een gedetailleerde regel wordt gemaakt voor de combinatie van kostenelementlid 10001 en alle kostenobjectleden die onder het hiërarchieniveau Financiën (CC002, CC003, CC007) worden samengevoegd.

De voorgaande regels tonen de flexibiliteit die dimensiehiërarchieën verschaffen. Door regels op hoog niveau te definiëren, kunt u onderhoud minimaliseren. Vervolgens kunt u gedetailleerde regels definiëren die passen in een specifieke zakelijke doelstelling.

Als de dimensiehiërarchieën die worden gebruikt in regels worden bijgewerkt, worden de updates automatisch aangereikt.

Als een niveau van gedetailleerdheid in de regels niet meer nodig is, kan de regel vervallen.

Zo is een specifieke kostengedragregel voor het knooppunt van de kostenobjectdimensiehiërarchie Financiën niet langer vereist. In dit geval klikt u op **Regel vervallen** om de regel te laten vervallen.

| Dimensiehiërarchieknooppunt van een kostenelement | Dimensiehiërarchieknooppunt van een kostenobject | Vast percentage | Vast bedrag | Geldig vanaf | Geldig tot  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Vaste kosten                            | Organisatie                         | 100,00           | 0.00         | 1/1/2017   | Nooit     |
| 10001                                 | Organisatie                         | 0.00             | 150,00       | 1/1/2017   | Nooit     |
| 10001                                 | Financiën                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Kostengedrag of variabele kosten        | Organisatie                         | 0.00             | 0.00         | 1/1/2017   | Nooit     |

In een overheadkostenberekening die na 20 januari 2017 wordt uitgevoerd, wordt niet langer rekening gehouden met deze regel.

> [!NOTE] 
> De velden **Geldig vanaf** en **Geldig tot** zijn datumeffectief en tijdeffectief. U kunt de regel laten vervallen en op dezelfde dag een nieuwe berekening van de overheadkosten uitvoeren.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Dimensiehiërarchieën definiëren voor beveiligingsinstelling

Gegevens van Kostprijsboekhouding moeten beschikbaar worden gesteld aan alle beheerders die verantwoordelijk voor een rapportage-eenheid zijn. Volgens de terminologie van Kostprijsboekhouding wordt een rapportage-eenheid vertegenwoordigd als een kostenobject of een reeks kostenobjecten.

Alle managers kunnen mogelijk toegang krijgen tot zeer gevoelige bedrijfsgegevens, zoals opbrengsten en marges. Het is daarom belangrijk dat u beveiliging instelt, zodat managers alleen de gegevens zien die relevant zijn voor hen. Als hulpmiddel voor het beheer van gegevensbeveiliging definieert u dimensiehiërarchieën.

- Het gebruik van dimensiehiërarchieën geldt alleen als de dimensiewaarde die is geselecteerd in de dimensiehiërarchieverwijzing, een kostenobjectdimensie is.
- Er kan slechts één dimensiehiërarchie worden ingeschakeld per kostenobjectdimensie in de toegangslijsthiërarchie.

**Gegevens van dimensiehiërarchie**

| Naam van dimensiehiërarchie | Dimensie    | Naam van type dimensiehiërarchie      | Hiërarchie van toegangslijsten |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatie             | Kostenplaatsen | Hiërarchie dimensieclassificatie | **Ja**               |

Het nieuwe sneltabblad **Gebruikers** is beschikbaar in de hiërarchieontwerper. Hier kunt u een of meer gebruikers-id´s in elk knooppunt van de hiërarchie invoegen.

|                 | Gebruikers            | Bereiken van dimensieleden   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Knooppunten**       | **Gebruikers-id**      | **Van dimensielid** | **Tot dimensielid** |
| Organisatie    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Beheer         | april            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Financiën   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Productie    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Verpakking | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembleren  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Kostenaccountants moeten worden toegewezen op het hoogste niveau van de hiërarchie, zodat ze alle vermeldingen in Kostprijsboekhouding kunnen zien.

Als u de hiërarchie van toegangslijsten en de bijbehorende beveiligingsinstellingen wilt inschakelen, gaat u naar **Kostprijsboekhouding** > **Instellen** > **Parameters** > **Algemeen**. Selecteer de parameter **Weergavetoegang voor dimensieleden voor kostenobject inschakelen**.

De instellingen voor de hiërarchie van toegangslijsten worden gebruikt om de gegevens te beheren die in de volgende gebieden worden weergegeven:

- Werkgebied **Kostenbeheer** (client):

    - Gegevens in formulieren die worden gebruikt voor detailanalysescenario 's

- Werkgebied **Kostenbeheer** (mobiele toepassing):

    - Saldi in kaarten

- Power BI:

    - Gegevens die worden weergegeven in Power BI-visualisaties
    - Gegevens van Power BI-visualisaties die worden ingesloten in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, client

> [!NOTE] 
> - Voordat de hiërarchie van toegangslijsten van invloed kan zijn op gegevens in Power BI, moeten de hiërarchie van toegangslijsten en beveiliging op rijniveau in Power BI worden gekoppeld. Zie [Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding](/dynamics365/unified-operations/dev-itpro/analytics/setup-security-cost-accounting-content-pack) voor meer informatie.
> - De hiërarchie van toegangslijsten helpen de export van gegevens naar Excel niet beveiligen. Daarom moet die rapportagefunctie alleen worden gebruikt door kostenaccountants en managers die volledige toegang moeten hebben om de gegevens weer te geven.

