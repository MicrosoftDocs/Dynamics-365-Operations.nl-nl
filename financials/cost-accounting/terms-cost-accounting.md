---
title: Terminologie voor kostprijsboekhouding
description: In dit onderwerp worden de belangrijkste termen gedefinieerd die in Kostprijsboekhouding worden gebruikt.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 76c5d4b3a118747246eeb7ca0db69532af04bf9c
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="cost-accounting-terminology"></a>Terminologie voor kostprijsboekhouding

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de belangrijkste termen gedefinieerd die in Kostprijsboekhouding worden gebruikt.

**Kostprijsboekhouding**

Door middel van Kostprijsboekhouding kunt u gegevens uit verschillende bronnen verzamelen, zoals het grootboek, subadministraties, budgetten en statistische gegevens. U kunt dan kostengegevens analyseren, samenvatten en evalueren, zodat het management de best mogelijke beslissingen kan nemen voor prijsaanpassingen, budgetten, kostenbeheer en dergelijke. De brongegevens voor kostenanalyse worden onafhankelijk behandeld in Kostprijsboekhouding. Daarom hebben updates in Kostprijsboekhouding geen invloed op de brongegevens. Wanneer u echter kostengegevens van verschillende bronnen verzamelt, en vooral als u de hoofdrekeningen importeert vanuit Grootboek in Microsoft Dynamics 365 for Operations als kostenelementen, zijn er redundante gegevens omdat dezelfde gegevens in zowel Grootboek als kostprijsboekhouding voorkomen. Deze redundantie is vereist, omdat u financieel beheer gebruikt voor externe rapportage en Kostprijsboekhouding voor interne rapportage.

**Grootboek van kostprijsboekhouding**

Het grootboek voor kostprijsboekhouding is een gespecialiseerd framework, dat bepaalt hoe processen, waarden en hoeveelheden worden ingevoerd en gepresenteerd voor een specifiek gebied in Kostprijsboekhouding. Het grootboek voor kostprijsboekhouding bepaalt processen en regels voor het meten van kosten voor kostenobjecten. Het verwerkt kostentransacties en beheert documenten die de wijzigingen registreren in waarden en hoeveelheden die voortkomen uit kostentransacties.

**Kosteninvoer**

Kosteninvoeren ontstaan door de overdracht via gegevensconnectoren van grootboekposten, kostentoewijzingen en geboekte kosteninvoeren in kostenjournalen.

**Kostenobject**

Een kostenobject is een object van een willekeurig type, waaraan kosten zijn toegewezen. Hieronder staan enkele veelvoorkomende kostenobjecten:

-   Producten
-   Projecten
-   Bronnen
-   Afdelingen
-   Kostenplaatsen
-   Geografische regio's

Met kostenobjecten kan het management kosten kwantificeren en ook winstgevendheidsanalyses uitvoeren.

**Kostenelement**

Kostenelementen worden gebruikt als functie om te volgen en te categoriseren waarheen de kosten stromen. Er zijn twee typen kostenelementen: primaire kosten en secundaire kosten. **Primaire kosten** De primaire kostenelementen vertegenwoordigen de stroom van kosten van financiële boekhouding naar kostprijsboekhouding. De kostenelementenstructuur correspondeert met de winst- verliesrekeningstructuur in het grootboek, waar een kostenelement kan corresponderen met een hoofdrekening. Niet alle hoofdrekeningen hoeven als kostenelementen te worden vertegenwoordigd, afhankelijk van de behoeften van het bedrijf. Hieronder volgen enkele voorbeelden van primaire kostenelementen:

-   Kosten van verkochte goederen
-   Indirecte materiaalkosten
-   Personeelskosten
-   Energiekosten

**Secundair kostenelement** 

De secundaire kostenelementen vertegenwoordigen de interne stroom van kosten, omdat deze kosten alleen in Kostenprijsboekhouding worden gemaakt en gebruikt. Secundaire kostenelementen helpen te borgen dat de oorsprong van kosten getraceerd kan worden. Deze kostenelementen worden gebruikt in kostentoewijzingen en overheadberekeningen. Hieronder volgen enkele voorbeelden van secundaire kostenelementen:

-   Productiekosten
-   Overheadkosten voor productie, materiaal, en marketing

**Kostenbeheereenheid**

Een kostenbeheereenheid vertegenwoordigt de kostprijsstructuur. De eenheid moet zijn gekoppeld aan kostenobjectdimensies in een kostprijsboekhoudinggrootboek.

**Versie**

Versies worden gebruikt om verschillende resultaten te simuleren, weer te geven en te vergelijken. Standaard worden alle werkelijke kosten weergegeven in een basisversie die wordt aangeduid als *werkelijk*. Voor budgetten en berekeningen kunt u werken met zoveel versies als nodig is. U kunt bijvoorbeeld budgetgegevens importeren in een oorspronkelijke versie en het budget vervolgens bewerken in een herziene versie. Voor berekeningen kunt u meerdere versies maken. In deze verschillende versies kunt u vervolgens berekeningen maken door middel van verschillende berekeningsregels die voor kostentoewijzing worden toegepast.

**Overzicht**

Overzichten zijn weergaven voor managers die verantwoordelijk zijn voor kostenbeheersing. Overzichten worden gedefinieerd door een kostencontroller Ze geven snel inzicht in werkelijke en gebudgetteerde kosten, en zelfs afwijkings- en berekeningsversies. Om ervoor te zorgen dat managers alleen de gegevens zien waarvoor zij verantwoordelijk zijn, gelden toegangsregels voor de gegevens in de overzichten.

**Gegevensconnector**

Gegevens kunnen in Kostprijsboekhouding worden geïmporteerd vanuit externe systemen via gegevensconnectors. U kunt bijvoorbeeld rekeningstructuren, dimensies, grootboekvermeldingen en budgetregels importeren. U kunt gegevens importeren en dataverbindingen maken door middel van vooraf geconfigureerde gegevensconnectors of aangepaste connectors.

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

**Overheadkosten**

Overheadkosten verwijzen naar de doorlopende uitgaven die gerelateerd zijn aan het runnen van een bedrijf. Dit zijn kosten die niet rechtstreeks aan bepaalde zakelijke activiteiten kunnen worden gekoppeld. Hieronder staan enkele voorbeelden van overheadkosten:

-   Boekhoudingskosten
-   Afschrijvingen
-   Verzekering
-   Interesse
-   Juridische kosten
-   Belastingen
-   Gas, water, stroom

**Kostentoewijzing**

Kostentoewijzing is het proces voor het toewijzen van kosten op basis van de hoofdoorzaken van de gemeenschappelijke kosten. U wijst de kostenbedragen en -hoeveelheden toe van één kostenobject aan een of meer andere kostenobjecten. Alle kosten voor faciliteitservices worden toegewezen aan de verschillende afdelingen die het gezamenlijke bureaugebouw gebruiken.

**Beleid voor kostprijstoewijzing**

Door een beleid voor kostprijstoewijzing worden de bedragen en de hoeveelheden gedefinieerd, die moeten worden toegewezen. Toewijzingsregels bevatten regels voor toewijzingsbronnen, die de kosten definiëren die worden toegewezen, en regels voor toewijzingsdoelen, die bepalen waaraan de kosten worden toegewezen. Alle kosten voor faciliteitservices zijn bijvoorbeeld een toewijzingsbron die aan verschillende afdelingen in een organisatie (d.w.z. aan toewijzingsdoelen) kan worden toegewezen.

**Toewijzingsgrondslag**

De toewijzingsgrondslag is de basis waarmee activiteiten kunnen worden gemeten en gekwantificeerd, zoals gebruikte machine-uren, verbruikte kilowatt-uren, uren die zijn besteed aan directe arbeid of vierkante meters op die worden bezet. Hiermee worden kosten toegewezen aan een of meer kostenobjecten.

**Toewijzingsmethode**

Een van de toewijzingsmethodes houdt in dat kosten worden toegewezen op kostentarief. U kunt ervoor kiezen om kosten toe te wijzen door middel van het tarief van de actuele periode of een historisch tarief. Toewijzing waarbij de wederkerige methode wordt gebruikt, zorgt ervoor dat de toewijzingsbasis wordt bepaald door een reeks gelijktijdige vergelijkingen voordat toewijzing wordt uitgevoerd door middel van het tarief van de actuele periode.

**Kostentotalisatie**

Het doel van kostentotalisatie is om alle kosten voor een bepaald kostenobject op te nemen. Het aggregatieniveau wordt door de gebruiker gedefinieerd. Met kostentotalisatie kunt u elementen van kosten aggregeren, die van het ene kostenobject naar een ander moeten worden toegewezen. Als u geen gebruik maakt van kostentotalisatie, worden alle kostenelementen toegewezen van het ene kostenobject naar het andere.

**Kostentariefbeleid**

Het kostentarief dient om de prijs per kostenobject te berekenen. Om de elementen van de prijs te begrijpen, definieert u beleid voor kostentarieven. Er zijn twee typen kostentarieven: historische kostentarieven en geplande kostentarieven. Een historische kostentarief een berekend tarief, dat wordt gebruikt als factor voor de toewijzingsgrondslag van een kostenobject. Het tarief wordt berekend op basis van de kostentoewijzingen in de vorige periode. Een gepland tarief is een door de gebruiker gedefinieerd tarief.

**Dimensiehiërarchie**

Dimensiehiërarchieën worden gebruikt als rapportagestructuren wanneer u regels voor toewijzing, kostentarief en kostentotalisatie definieert of overzichten of gegevens weergeeft in Microsoft Excel en toegang tot de geaggregeerde gegevens definieert. Er zijn twee dimensiehiërarchieën: de categorisatiehiërarchie en de classificatiehiërarchie. Een categorisatiehiërarchie wordt gedefinieerd op basis van kostenelementen. Een classificatiehiërarchie wordt gedefinieerd op basis van kostenobjecten.

**Statistische dimensie**

Een statistische dimensie is de expressie van een aantal of som van een object, die kan worden gebruikt als basis voor toewijzingen of kostentariefberekeningen. De dimensie wordt handmatig gemaakt of geïmporteerd vanuit bronsystemen. Voorbeelden van statistische dimensies zijn het aantal werknemers, het aantal softwareprogramma's met een licentie op elk apparaat, het stroomverbruik van elke machine of het aantal vierkante meters voor een kostenplaats.

**Statistische boeking**

Statistische boekingen bevatten de geregistreerde waarde van de som of telling voor een bepaalde statistische dimensie. De geregistreerde som- of tellingswaarde wordt ook wel aangeduid als magnitude.




