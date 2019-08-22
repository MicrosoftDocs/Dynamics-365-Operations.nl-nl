---
title: Terminologie voor kostprijsboekhouding
description: In dit onderwerp worden de belangrijkste termen gedefinieerd die in Kostprijsboekhouding worden gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c04a1b79006ed3fdc7311830d5f08f9962976787
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841100"
---
# <a name="cost-accounting-terminology"></a>Terminologie voor kostprijsboekhouding

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de belangrijkste termen gedefinieerd die in Kostprijsboekhouding worden gebruikt.

**Toewijzingsgrondslag**

Met de toewijzingsgrondslag kunnen activiteiten, zoals gebruikte machine-uren, verbruikte kilowattuur of vierkante meters die in beslag worden genomen, worden gemeten en gekwantificeerd. Dit is de basis voor het toewijzen van kosten aan een of meer kostenobjecten

**Kostprijsboekhouding**

Door middel van Kostprijsboekhouding kunt u gegevens uit verschillende bronnen verzamelen, zoals het grootboek, subadministraties, budgetten en statistische gegevens. U kunt dan kostengegevens analyseren, samenvatten en evalueren, zodat het management de best mogelijke beslissingen kan nemen voor prijsaanpassingen, budgetten, kostenbeheer en dergelijke. De brongegevens voor kostenanalyse worden onafhankelijk behandeld in Kostprijsboekhouding. Daarom hebben updates in Kostprijsboekhouding geen invloed op de brongegevens. Wanneer u echter kostengegevens van verschillende bronnen verzamelt, en vooral als u de hoofdrekeningen importeert vanuit Grootboek in Microsoft Dynamics 365 for Finance and Operations als kostenelementen, zijn er redundante gegevens omdat dezelfde gegevens in zowel Grootboek als kostprijsboekhouding voorkomen. Deze redundantie is vereist, omdat u financieel beheer gebruikt voor externe rapportage en Kostprijsboekhouding voor interne rapportage.

**Grootboek van kostprijsboekhouding**

Gedefinieerd op basis van kalender, valuta en kostenelementdimensie, beheert u hiermee processen en het beleid voor het meten van kosten. 

**Kosteninvoer**

Kosteninvoeren ontstaan door de overdracht via gegevensconnectoren van grootboekposten, kostentoewijzingen en geboekte kosteninvoeren in kostenjournalen.

**Kostenobject**

Elk type object dat is geselecteerd voor kostenbeheer. Kosten of opbrengsten worden rechtstreeks geboekt voor of toegewezen aan kostenobjecten. Enkele veelvoorkomende kostenobjecten:

-  Producten
-  Projecten
-  Afdelingen
-  Kostenplaatsen

Met kostenobjecten kan het management kosten kwantificeren en ook winstgevendheidsanalyses uitvoeren.

**Kostenelement**

Wordt gebruikt als een functie om kosten te volgen en te categoriseren. Er zijn twee typen kostenelementen: primair en secundair.

Primaire kostenelementen vertegenwoordigen de stroom van kosten van financiële boekhouding naar kostprijsboekhouding. De structuur correspondeert doorgaans met de winst- en verliesrekeningstructuur in het grootboek, waar een kostenelement kan corresponderen met een hoofdrekening. Niet alle hoofdrekeningen hoeven als kostenelementen te worden vertegenwoordigd, afhankelijk van de behoeften van het bedrijf. 

Secundaire kostenelementen vertegenwoordigen de interne stroom van kosten, omdat deze kosten alleen in Kostprijsboekhouding worden gebruikt. Ze worden gebruikt in regels voor kostentotalisatie om kosten samen te voegen in betekenisvolle verzamelingen die worden gebruikt voor overheadberekeningen. 

**Kostenclassificatie**

Met kostenclassificatie worden kosten gegroepeerd op basis van gedeelde karakteristieken. Kosten kunnen bijvoorbeeld worden gegroepeerd op elementen, traceerbaarheid en gedrag.

-   **Op elementen**: materialen, arbeid, en kosten.
-   **Op traceerbaarheid**: Directe kosten en indirecte kosten. Directe kosten worden rechtstreeks toegewezen aan kostenobjecten. Indirecte kosten kunnen niet rechtstreeks naar kostenobjecten worden getraceerd. Indirecte kosten worden toegewezen aan kostenobjecten.
-   **Op gedrag**: vast, variabel en semi-variabel.

**Kostengedrag**

Met kostengedrag worden kosten geclassificeerd op basis van hun gedrag ten opzichte van wijzigingen in belangrijke zakelijke activiteiten. Om kosten effectief te kunnen beheersen, moet het management het kostenbedrag begrijpen. Er zijn drie typen kostengedragspatronen: vast, variabel en semi-variabel.

- **Vaste kosten** Vaste kosten zijn kosten die niet op de korte termijn variëren, ongeacht of het activiteitenniveau toe- of afneemt. Vaste kosten kunnen bijvoorbeeld basale bedrijfskosten van een onderneming zijn zoals de huur, die niet worden beïnvloed door schommelingen in het activiteitenniveau.

- **Variabele kosten** Variabele kosten veranderen mee met wijzigingen in het activiteitenniveau. Specifieke directe materiaalkosten kunnen bijvoorbeeld zijn gekoppeld aan elk product dat wordt verkocht. Hoe meer producten worden verkocht, des te hoger de directe materialenkosten uitvallen.

- **Semi-variable kosten** Semi-variable kosten zijn kosten die deels vastliggen en deels variëren. Een internetabonnement kan bijvoorbeeld een maandelijks abonnementsbedrag omvatten plus een tarief voor breedbandgebruik. Het standaard abonnementsgedrag wordt geboekt bij de vaste kosten, maar het tarief voor breedbandgebruik bij variabele kosten.

**Kostenbeheereenheid**

De kostenbeheereenheid vertegenwoordigt de kostprijsstructuur. De structuur bepaalt hoe kosten in een hiërarchische volgorde tussen kostobjectdimensies en hun respectieve kostenobjecten stromen. 

**Kostenverdeling**

Wordt gebruikt om de kosten van een kostenobject te verdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen. Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten en er geen wederkerige verwerking plaatsvindt.

**Kostentoewijzing**

Wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen. Finance and Operations ondersteunt de wederzijdse toewijzingsmethode. Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend. Het systeem bepaalt automatisch de volgorde voor het uitvoeren van de toewijzingen en herhalingen. Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag. Toewijzingen tussen dimensies voor kostenobjecten en hun respectievelijke leden worden ondersteund. De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.

**Beleid voor kostprijstoewijzing**

Door een beleid voor kostprijstoewijzing worden de bedragen en de hoeveelheden gedefinieerd, die moeten worden toegewezen. Toewijzingsregels bevatten regels voor toewijzingsbronnen, die de kosten definiëren die worden toegewezen, en regels voor toewijzingsdoelen, die bepalen waaraan de kosten worden toegewezen. Alle kosten voor faciliteitservices zijn bijvoorbeeld een toewijzingsbron die aan verschillende afdelingen in een organisatie (d.w.z. aan toewijzingsdoelen) kan worden toegewezen.

**Kostentotalisatie**

Het doel van regels voor kostentotalisatie is om kosten samen te voegen in betekenisvolle verzamelingen. Het aggregatieniveau wordt door de gebruiker gedefinieerd en omvat de toewijzing van een secundair kostenelement. Als u geen gebruikmaakt van kostentotalisatie, worden alle kostenelementen toegewezen van het ene kostenobject aan het andere.

**Kostentariefbeleid**

Het kostentarief dient om de prijs per kostenobject te berekenen. Om de elementen van de prijs te begrijpen, definieert u beleid voor kostentarieven. Er zijn twee typen kostentarieven: historische kostentarieven en geplande kostentarieven. Een historische kostentarief een berekend tarief, dat wordt gebruikt als factor voor de toewijzingsgrondslag van een kostenobject. Het tarief wordt berekend op basis van de kostentoewijzingen in de vorige periode. Een gepland tarief is een door de gebruiker gedefinieerd tarief.

**Dimensiehiërarchie**

Er zijn twee dimensiehiërarchieën: de categorisatiehiërarchie en de classificatiehiërarchie. Het type dimensiecategorisatiehiërarchie wordt gebruikt voor rapportagedoeleinden. Dit type ondersteunt alleen de kostenelementdimensies. Het type dimensieclassificatiehiërarchie wordt gebruikt om beleidsregels voor rapportagedoeleinden te definiëren. Het biedt ondersteuning voor alle dimensies, zoals kostenobjecten, kostenelementen en statistische dimensies. 

**Gegevensconnector**

Kostprijsboekhouding ondersteunt de integratie van gegevens uit bronsystemen via een reeks gegevensconnectors. De volgende gegevensconnectors zijn beschikbaar:

-  Geïmporteerde transacties (vooraf geconfigureerd)
-  Dynamics 365 for Finance and Operations (vooraf geconfigureerd)
-  Dynamics AX (configuratie vereist)

**Opmerking:** de gegevensconnector Geïmporteerde transacties is gebaseerd op gegevensentiteiten.

**Gegevensprovider**

De meeste bronsystemen kunnen gegevens leveren die overeenkomen met een of meer gegevensbronnen in Kostprijsboekhouding. Als u gegevens uit de bronsystemen met de gegevensbron in Kostprijsboekhouding wilt uitlijnen, moet er een gegevensprovider worden geconfigureerd. In de volgende tabel wordt de beschikbaarheid van gegevensproviders per gegevensconnector en gegevensbron weergegeven.

|  **Gegevensbronnen** |  **Gegevensconnector Geïmporteerde transacties** | **Dynamics 365 for Finance and Operations-gegevensconnector**  | **Dynamics AX-gegevensconnector**  |
|---|---|---|---|
| Dimensieleden van kostenelement  |  Ja | Ja  | Ja  |
|  Dimensieleden van kostenobject |  Ja | Ja  | Ja  |
|  Statistische dimensieleden | Ja  | Nee  | Nee  |
|  Grootboek | Ja  | Ja  | Ja  |
|  Budgetregels  | Ja  | Ja  | Ja  |
|  Statistische maateenheden | Ja  | Ja  | Ja  |

**Formule**

Met formuletoewijzingsgrondslagen kunt u geavanceerde formules definiëren voor het bereiken van de juiste toewijzingsgrondslag. U kunt formuletoewijzingsgrondslagen handmatig maken. U kunt de volgende operatoren gebruiken voor het definiëren van uw formule.

|  **Symbolen** | **Tekst**  |
|---|---|
|  ( ) | Haakjes  |
|  < |  Kleiner dan |
|  > |  Groter dan |
|  + |  Optelling |
|  – |  Aftrekken |
| *  | Vermenigvuldigen  |

Traditionele IF-instructies worden niet ondersteund. U kunt echter instructies maken en nagaan of deze waar zijn.

|  **Instructievalidatie** | **Resultaat**  |
|---|---|
|  a > b| Waar  |
|  a > b |  Onwaar |

**Overheadkosten**

Overheadkosten verwijzen naar de doorlopende uitgaven die gerelateerd zijn aan het runnen van een bedrijf. Dit zijn kosten die niet rechtstreeks aan bepaalde zakelijke activiteiten kunnen worden gekoppeld. Hieronder staan enkele voorbeelden van overheadkosten:

-   Boekhoudingskosten
-   Afschrijvingen
-   Verzekering
-   Interesse
-   Juridische kosten
-   Belastingen
-   Gas, water, stroom

**Overheadtarieven**

Tarieven worden gedefinieerd per kostenobject en kostenelement. Er zijn twee typen tarieven: boekperiode en door de gebruiker opgegeven. Boekperiodetarieven worden berekend met de overheadberekening. Een gebruikersspecifiek tarief is door de gebruiker gedefinieerd en kan worden gebruikt om kosten tussen kostenobjecten toe te wijzen volgens een vooraf vastgesteld tarief in de overheadberekening.

**Gepubliceerd**

Als u dit veld instelt op Ja, kan een gebruiker die is toegewezen aan een van de volgende rollen, het rapport in het werkgebied Kostenbeheer zien:

-  Manager van kostprijsboekhouding
-  Kostenaccountant
-  Assistent kostenaccountant
-  Controller voor kostenobjecten

Als u dit veld instelt op Nee, kunnen alleen gebruikers die zijn toegewezen aan een van de volgende rollen, het rapport in het werkgebied Kostenbeheer zien:

-  Manager van kostprijsboekhouding
-  Kostenaccountant
-  Assistent kostenaccountant

**Statistische dimensie**

Een statistische dimensie en de leden ervan worden gebruikt om niet-monetaire posten in Kostprijsboekhouding te registreren en beheren. Statistische dimensieleden kunnen worden gebruikt voor twee doelen:

-  Als een toewijzingsgrondslag in beleid zoals kostenverdeling of kostentoewijzing.
-  Voor rapportage van niet-monetair verbruik.

Een statistische dimensie is de expressie van een aantal of som van een activiteit, die kan worden gebruikt als basis voor toewijzingen of tariefberekeningen. De dimensie wordt handmatig gemaakt of geïmporteerd vanuit bronsystemen. Voorbeelden van statistische dimensies zijn het aantal werknemers, het aantal softwareprogramma's met een licentie op elk apparaat, het stroomverbruik van elke machine of het aantal vierkante meters voor een kostenplaats.

**Instructie**

Overzichten zijn weergaven voor managers die verantwoordelijk zijn voor kostenbeheersing. Overzichten worden gedefinieerd door een kostencontroller en bieden snel inzicht in werkelijke en gebudgetteerde kosten, en afwijkingen. Een manager kan zo nodig meer details bekijken. Om ervoor te zorgen dat managers alleen de gegevens zien waarvoor zij verantwoordelijk zijn, gelden toegangsregels voor de gegevens in de overzichten.

**Versie**

Versies worden gebruikt om verschillende resultaten te simuleren, weer te geven en te vergelijken. Standaard worden alle werkelijke kosten weergegeven in een basisversie die wordt aangeduid als *werkelijk*. Voor budgetten en berekeningen kunt u werken met zoveel versies als nodig is. U kunt bijvoorbeeld budgetgegevens importeren in een oorspronkelijke versie en het budget vervolgens bewerken in een herziene versie. Voor berekeningen kunt u meerdere versies maken. In deze verschillende versies kunt u vervolgens berekeningen maken door middel van verschillende berekeningsregels die voor kostentoewijzing worden toegepast.


