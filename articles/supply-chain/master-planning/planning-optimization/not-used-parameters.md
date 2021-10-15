---
title: Parameters die niet worden gebruikt door Planningsoptimalisatie
description: In dit onderwerp worden de parameters vermeld waarmee tijdens de bewerking van Planningsoptimalisatie momenteel geen rekening wordt houden.
author: ChristianRytt
ms.date: 09/02/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 61cdbe3d966d06193b1dc5c145233e53be3946ff
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571060"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Parameters die niet worden gebruikt door Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

In dit onderwerp worden de parameters vermeld waarmee tijdens de bewerking van Planningsoptimalisatie momenteel geen rekening wordt houden. Een parameter kan worden overgeslagen, bijvoorbeeld omdat gerelateerde functionaliteit nog niet wordt ondersteund. De parameter kan ook verouderd zijn geraakt als gevolg van functionele wijzigingen.

In de volgende secties vindt u een overzicht van de parameters die tijdens Planningsoptimalisatie niet worden gebruikt op specifieke pagina's. Er wordt ook uitgelegd waarom elke parameter niet wordt gebruikt.

## <a name="master-planning-parameters-page"></a>Pagina Parameters hoofdplanning

Bij Planningsoptimalisatie worden de volgende parameters of opties op de pagina **Parameters hoofdplanning** niet gebruikt:

- Tabblad **Algemeen**:

  - **Huidig prognoseplan**: in afwachting van ondersteuning voor *Prognoses*.
  - **Huidige statisch hoofdplan**: in afwachting van ondersteuning voor *Statisch plan kopiëren naar dynamisch plan*.
  - **Huidige dynamisch hoofdplan**: in afwachting van ondersteuning voor *Statisch plan kopiëren naar dynamisch plan*.
  - **Het volledige en bijgewerkte statische hoofdplan kopiëren naar het dynamische hoofdplan**: in afwachting van ondersteuning voor *Statisch plan kopiëren naar dynamisch plan*.
  - **Begintijd voor berekende vertragingen**: in afwachting van ondersteuning voor *Berekende vertragingen*.
  - **Dynamische negatieve dagen gebruiken**: bij Planningsoptimalisatie wordt altijd de benadering *Dynamische negatieve dagen* gebruikt.
  - **Kalender van vandaag**: in afwachting van ondersteuning voor *Planning*.
  - **Gebruik van cache**: de configuratie van het Microsoft Azure-abonnement handelt prestatiepunten af.
  - **Aantal taken in de taakbundel van de helper**: de configuratie van het Azure-abonnement handelt prestatiepunten af.
  - **Voorverwerking: automatisch filteren op artikelen met directe vraag:** de configuratie van het Azure-abonnement handelt prestatiepunten af.
  - **Naverwerking: automatisch filteren op artikelen met directe vraag:** de configuratie van het Azure-abonnement handelt prestatiepunten af.
  - **Aantal orders fiatteringsbundel**: de configuratie van het Azure-abonnement handelt prestatiepunten af.
  - **Aantal threads**: de configuratie van het Azure-abonnement handelt prestatiepunten af.
  - **Time-out planningsproces in minuten**: de configuratie van het Azure-abonnement handelt prestatiepunten af.
  - **Begintijd planning**: in afwachting van ondersteuning voor *Planning*.

- Tabblad **Geplande orders**:

  - **Ontvangsttijd**: in afwachting van ondersteuning voor *Planning*.
  - **Productie**: in afwachting van ondersteuning voor *Planning*.
  - Velden in de sectie **Project**: in afwachting van ondersteuning voor *Planning*.

- Tabblad **Standaardupdate**:

  - **Markering bijwerken**: in afwachting van ondersteuning voor *Fiattering*.
  - **Fiatteren beëindigen bij fout**: in afwachting van ondersteuning voor *Fiattering*.
  - **Groeperen op leverancier**: in afwachting van ondersteuning voor *Fiattering*.
  - **Groeperen op inkopersgroep**: in afwachting van ondersteuning voor *Fiattering*.
  - **Groeperen op inkoopovereenkomst**: in afwachting van ondersteuning voor *Fiattering*.
  - **Groeperen op periode**: in afwachting van ondersteuning voor *Fiattering*.
  - **Inkoopovereenkomst zoeken**: in afwachting van ondersteuning voor *Fiattering*.
  - **Groeperen op planningsprioriteit**: in afwachting van ondersteuning voor *Fiattering*.
  - **Groeperen op periode**: in afwachting van ondersteuning voor *Fiattering*.

## <a name="coverage-groups-page"></a>Pagina Behoefteplanningsgroepen

Bij Planningsoptimalisatie worden de volgende parameters of opties op de pagina **Behoefteplanningsgroepen** niet gebruikt:

- Sneltabblad **Algemeen**:

  - **Positieve dagen**: in afwachting van ondersteuning voor *Positieve dagen*.
  - **Voorhanden voorraad verbruiken**: in afwachting van ondersteuning voor *Verbruik van voorhanden voorraad*.
  - **De opgegeven stuklijst- of formuleversie gebruiken**: in afwachting van ondersteuning voor *Formuleversies met co-/bijproducten*.
  - **De opgegeven routeversie gebruiken**: in afwachting van ondersteuning voor *Vraag waarvoor specifieke stuklijst- of routevereisten zijn gedefinieerd*.

- Sneltabblad **Actie**:

  - **Actiebericht**: in afwachting van ondersteuning voor *Acties*.
  - **Time fence van actie**: in afwachting van ondersteuning voor *Acties*.
  - **Marge voor uitstellen**: in afwachting van ondersteuning voor *Acties*.
  - **Marge voor vervroegen**: in afwachting van ondersteuning voor *Acties*.
  - **Basisdatum**: in afwachting van ondersteuning voor *Acties*.
  - **Vervroegen**: in afwachting van ondersteuning voor *Acties*.
  - **Uitstellen**: in afwachting van ondersteuning voor *Acties*.
  - **Verlagen**: in afwachting van ondersteuning voor *Acties*.
  - **Verhogen**: in afwachting van ondersteuning voor *Acties*.
  - **Afgeleide acties**: in afwachting van ondersteuning voor *Acties*.

- Sneltabblad **Overig**:

  - **Time fence (dagen) blokkeren**: ondersteuning voor *Time fence voor blokkering* is niet gepland in Planningsoptimalisatie.
  - **Time fence van stuklijstexplosie (dagen)**: in afwachting van ondersteuning voor *Planning*.
  - **Time fence capaciteitsplanning (dagen)**: in afwachting van ondersteuning voor *Planning*.
  - **Time fence goedgekeurde bestelaanvragen (dagen)**: in afwachting van ondersteuning voor *Aanvraag*.
  - **Prognoseplan (timefence)**: in afwachting van ondersteuning voor *Prognoses*.

- Sneltabab **Vertragingen**:

  - **Berekende vertragingen**: in afwachting van ondersteuning voor *Berekende vertragingen*.
  - **Time fence vertragingen berekenen (dagen)**: in afwachting van ondersteuning voor *Berekende vertragingen*.

## <a name="item-coverage-page"></a>Pagina Artikelbehoefteplanning

Bij Planningsoptimalisatie worden de volgende parameters of opties op de pagina **Artikelbehoefteplanning** niet gebruikt:

- Tabblad **Algemeen**:

  - **Gepland ordertype**: Planningsoptimalisatie biedt geen ondersteuning voor de optie *Kanban*, in afwachting van ondersteuning voor *Kanban*.
  - **Time fence (dagen) blokkeren**: ondersteuning voor *Time fence voor blokkering* is niet gepland in Planningsoptimalisatie.
  - **Time fence van stuklijstexplosie (dagen)**: in afwachting van ondersteuning voor *Planning*.
  - **Time fence capaciteitsplanning (dagen)**: in afwachting van ondersteuning voor *Planning*.
  - **Time fence goedgekeurde bestelaanvragen (dagen)**: in afwachting van ondersteuning voor *Aanvraag*.
  - **Minimum behalen**: Planningsoptimalisatie biedt geen ondersteuning voor de opties *Datum van vandaag*, *Eerste uitgifte* en *Time fence voor behoefteplanning*. Er wordt altijd gebruikgemaakt van de optie *Datum van vandaag + levertijd*.
  - **Minimumperioden**: in afwachting van ondersteuning voor *Minimumvoorraadniveau*.
  - **Planningsformule**: in afwachting van ondersteuning voor *Formuleversies met co-/bijproducten*.
  - **Standaardprioriteit**: in afwachting van ondersteuning voor *Formuleversies met co-/bijproducten*.
  - **Huidige prioriteit**: in afwachting van ondersteuning voor *Formuleversies met co-/bijproducten*.
  - **Datum gewijzigd**: in afwachting van ondersteuning voor *Formuleversies met co-/bijproducten*.
  - **Voorhanden voorraad verbruiken**: in afwachting van ondersteuning voor *Verbruik van voorhanden voorraad*.

- Tabblad **Levertijd**:

  - **Inkooptijd**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.
  - **Productietijd**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.
  - **Verplaatsingstijd**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.
  - **Werkdagen**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.

## <a name="master-plans-page"></a>Pagina Hoofdplannen

Bij Planningsoptimalisatie worden de volgende parameters of opties op de pagina **Hoofdplannen** niet gebruikt:

- Sneltabblad **Algemeen**:

  - **Voorhanden voorraad opnemen**: in afwachting van ondersteuning voor *Verbruik van voorhanden voorraad*.
  - **Voorhanden voorraad overschrijven**: in afwachting van ondersteuning voor *Verbruik van voorhanden voorraad*.
  - **Voorhanden voorraad verbruiken**: in afwachting van ondersteuning voor *Verbruik van voorhanden voorraad*.
  - **Voorraadtransacties opnemen**: in afwachting van ondersteuning voor *Verbruik van voorhanden voorraad*.
  - **Verkoopoffertes opnemen**: in afwachting van ondersteuning voor *Verkoopoffertes*.
  - **Offerteaanvragen opnemen**: in afwachting van ondersteuning voor *Offerteaanvragen*.
  - **Houdbaarheidsdatums gebruiken**: in afwachting van ondersteuning voor *Houdbaarheid*.
  - **Continuïteitsplan opnemen**: in afwachting van ondersteuning voor *Continuïteitsplanning*.
  - **Planningsmethode**: in afwachting van ondersteuning voor *Planning*.
  - **Beperking**: in afwachting van ondersteuning voor *Planning*.
  - **Time fence capaciteit achterwaartse planning**: in afwachting van ondersteuning voor *Planning*.
  - **Eindige capaciteit**: in afwachting van ondersteuning voor *Planning*.
  - **Tijdlimiet beperkte capaciteit**: in afwachting van ondersteuning voor *Planning*.
  - **Eindige capaciteit voor bottleneck resources**: in afwachting van ondersteuning voor *Planning*.
  - **Time fence capaciteit voor bottleneck resources**: in afwachting van ondersteuning voor *Planning*.
  - **Geplande orders**: bij Planningsoptimalisatie worden vaste nummerreeksen gebruikt.
  - **Sessie**: bij Planningsoptimalisatie worden vaste nummerreeksen gebruikt.
  - **Continuïteitsplan**: bij Planningsoptimalisatie worden vaste nummerreeksen gebruikt.

- Sneltabblad **Time fences in dagen**:

  - **Blokkeren**: ondersteuning voor *Time fence voor blokkering* is niet gepland in Planningsoptimalisatie.
  - **Explosie**: in afwachting van ondersteuning voor *Planning*.
  - **Prognoseplan**: in afwachting van extra ondersteuning voor *Prognoses*.
  - **Capaciteit**: in afwachting van ondersteuning voor *Planning*.
  - **Continuïteitsplan**: in afwachting van ondersteuning voor *Continuïteitsplanning*.
  - **Actiebericht**: in afwachting van ondersteuning voor *Acties*.
  - **Berekende vertragingen**: in afwachting van extra ondersteuning voor *Berekende vertragingen*.
  - **Sequentiëren**: in afwachting van ondersteuning voor *Productie*.

- Sneltab **Berekende vertragingen**:

  - **Zorg ervoor dat de geplande orders niet zijn gemaakt vóór de uitvoeringsdatum van de hoofdplanning**: in afwachting van ondersteuning voor *Berekende vertragingen*.
  - **De berekende vertraging optellen bij de behoeftedatum** (in de sectie **Geplande inkooporders**): in afwachting van ondersteuning voor *Berekende vertragingen*.
  - **De berekende vertraging optellen bij de behoeftedatum** (in de sectie **Geplande productieorders**): in afwachting van ondersteuning voor *Berekende vertragingen*.
  - **De berekende vertraging optellen bij de behoeftedatum** (in de sectie **Geplande overboekingsorders**): in afwachting van ondersteuning voor *Berekende vertragingen*.
  - **De berekende vertraging optellen bij de behoeftedatum** (in de sectie **Geplande kanban**): in afwachting van ondersteuning voor *Berekende vertragingen*.

- Sneltabab **Sequentiëren**:

  - **Volgorde van geplande orders na hoofdplanning**: in afwachting van ondersteuning voor *Sequentiëren*.
  - **Buckettype**: in afwachting van ondersteuning voor *Sequentiëren*.
  - **Periodetype**: in afwachting van ondersteuning voor *Sequentiëren*.
  - **Aantal buckets in de campagnecyclus**: in afwachting van ondersteuning voor *Sequentiëren*.

## <a name="released-product-details-page"></a>Pagina Vrijgegeven productdetails

Bij Planningsoptimalisatie worden de volgende parameters of opties op de pagina **Vrijgegeven productdetails** niet gebruikt:

- Sneltabwerk **Technicus**:

  - **Productietype**: bij Planningsoptimalisatie wordt de optie *Planningsartikelen* niet ondersteund, in afwachting van ondersteuning voor *Planningsartikelen*.

## <a name="default-order-settings-page"></a>Pagina Standaard orderinstellingen

Bij Planningsoptimalisatie worden de volgende parameters of opties op de pagina **Standaard orderinstellingen** niet gebruikt:

- Sneltabblad **Inkooporder**:

  - **Inkoopdoorlooptijd**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.
  - **Werkdagen**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.

- Sneltablijst **Voorraad**:

  - **Controle van leveringsdatum**: Planningsoptimalisatie biedt geen ondersteuning voor de optie *CTP*, in afwachting van ondersteuning voor *CTP*.
  - **Voorraaddoorlooptijd**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.
  - **Werkdagen**: in versies van de service Planningsoptimalisatie die ouder zijn dan de versie van 6 augustus 2021, gebruikt Planningsoptimalisatie deze parameter om de juiste order- en leveringsdatums te berekenen, maar slaat niet de berekende levertijd zelf naar de geplande order op. In latere versies gebruikt de service ook de berekende doorlooptijd om het veld **Levertijd** en de optie **Werkdagen** in te stellen zoals is vereist voor de relevante geplande order.

## <a name="working-time-calendars-page"></a>Pagina Werktijdkalenders

Bij Planningsoptimalisatie wordt de volgende parameter op de pagina **Werktijdkalenders** niet gebruikt:

- **Basiskalender**: in afwachting van ondersteuning voor *Basiskalenders*.

## <a name="batch-disposition-master-page"></a>Pagina Hoofdbatchbeschikking

Bij Planningsoptimalisatie wordt de volgende parameter op de pagina **Hoofdbatchbeschikking** niet gebruikt:

- Sneltabblad **Instellingen**:

  - **Nettobehoeften**: in afwachting van ondersteuning voor *Batchbeschikkingscodes*.
