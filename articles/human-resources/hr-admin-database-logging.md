---
title: Databaselogboeken configureren en beheren
description: U kunt wijzigingen in tabellen en velden in Dynamics 365 Human Resources bijhouden met databaselogboeken.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801330"
---
# <a name="configure-and-manage-database-logging"></a>Databaselogboeken configureren en beheren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt wijzigingen in tabellen en velden in Dynamics 365 Human Resources bijhouden met databaselogboeken. In dit onderwerp komt het volgende aan de orde:

- Beveiliging en prestaties voor databaselogboeken beheren
- Databaselogboek instellen
- Databaselogboeken opschonen

## <a name="overview-of-database-logging"></a>Overzicht van databaselogboeken

U kunt specifieke wijzigingen in Microsoft Dynamics 365 Human Resources bijhouden met databaselogboeken. Deze wijzigingen betreffen onder andere invoegen, bijwerken of verwijderen. Met databaselogboeken wordt een record met wijzigingen in tabellen of velden in de databaselogboektabel opgeslagen.

Zakelijke toepassingen van databaselogboeken zijn onder andere:

- Een controlerecord maken van wijzigingen in specifieke tabellen die gevoelige informatie bevatten.
- Het bijhouden van afzonderlijke transacties. Databaselogboeken zijn niet bedoeld voor het bijhouden van geautomatiseerde transacties die in batchtaken worden uitgevoerd.

## <a name="security-for-database-logging"></a>Beveiliging voor databaselogboeken

Databaselogboeken kunnen vertrouwelijke gegevens bevatten. Beperk de toegang tot beveiligingsrollen die toegang moeten hebben tot de logboekgegevens.

## <a name="database-logging-and-performance"></a>Databaselogboeken en prestaties

Het bijhouden van databaselogboeken kan waardevol zijn vanuit een zakelijk perspectief, maar ook kostbaar in termen van resourcegebruik en beheer. De implicaties van de prestaties van databaselogboeken zijn onder andere:

- De databaselogboektabel kan snel groter worden en veroorzaakt een toename van de omvang van de database. De groei is afhankelijk van de hoeveelheid vastgelegde gegevens die u wilt behouden. Standaard worden in de databaselogboektabel slechts 30 dagen aan logboekgegevens bijgehouden. 

- Databaselogboeken kunnen een negatieve invloed hebben op langdurige geautomatiseerde processen, zoals langlopende gegevensimportprocessen.

### <a name="best-practices"></a>Best practices

Selecteer specifieke velden die u in het logboek wilt opnemen in plaats van gehele tabellen, zodat de prestaties worden verbeterd. Om de prestaties op peil te houden zijn de databaselogboeken beperkt tot 20 tabellen.

> [!NOTE]
> Voor afzonderlijke velden kunnen alleen updates worden vastgelegd.

## <a name="set-up-database-logging"></a>Databaselogboek instellen

Met de wizard **Logboek van wijzigingen in database maken** kunt u databaselogboeken instellen. De wizard biedt een flexibele manier om logboeken voor tabellen of velden in te stellen.

1. Ga naar **Systeembeheer > Koppelingen > Database > Databaselogboek instellen**. Selecteer **Nieuw** om de wizard **Logboek van wijzigingen in database maken** te starten.
2. Selecteer **Volgende**. 
3. Selecteer op de pagina **Tabellen en velden** van de wizard de tabellen en velden waarvoor u databaseregistratie wilt inschakelen en selecteer **Volgende**.

   > [!Note]
   > Databaseregistratie is niet beschikbaar voor alle tabellen in de Human Resources-database. Als u **Alle tabellen weergeven** selecteert onder de lijst, wordt de lijst met tabellen en velden uitgebreid om alle databasetabellen weer te geven waarvoor databaseregistratie beschikbaar is, maar dit is een subset van de volledige lijst met databasetabellen.

4. Selecteer op de pagina **Typen wijzigingen** van de wizard de gegevensbewerkingen waarvoor u wijzigingen voor elk van de tabellen en velden wilt bijhouden en selecteer **Volgende**. Zie de onderstaande tabel voor een beschrijving van de gegevensbewerkingen die beschikbaar zijn voor logboekregistratie.
5. Bekijk op de pagina **Voltooien** de wijzigingen die worden aangebracht en selecteer **Voltooien**.

| Bewerking | Beschrijving |
| -- | -- |
| Nieuwe transacties traceren | Maak een logboek voor nieuwe records die in de tabel worden gemaakt. |
| Update | Maak een logboek voor updates van tabelrecords of updates voor afzonderlijk geselecteerde velden in de tabel. Als u ervoor kiest om updates voor de tabel te registreren, wordt er elke keer een logboekrecord gemaakt als een update wordt uitgevoerd voor een veld van een record in de tabel. Als u ervoor kiest om updates voor specifieke velden te registreren, wordt alleen een logboekrecord gemaakt bij updates van die velden van tabelrecords. |
| Delete | Maak een logboek voor records die uit de tabel worden verwijderd. |
| Sleutel hernoemen | Maak een logboekrecord wanneer de naam van een tabelsleutel wordt gewijzigd. |


## <a name="clean-up-database-logs"></a>Databaselogboeken opschonen

U kunt de databaselogboeken geheel of gedeeltelijk verwijderen met behulp van de volgende opties:

- Alle logboeken voor een bepaalde tabel selecteren.
- Specifieke typen databaselogboeken selecteren.
- Een datum en tijd selecteren waarop een logboek is gemaakt.

Volg deze stappen om databaselogboeken op te schonen: 

1. Ga naar **Systeembeheer > Koppelingen > Database > Databaselogboek**. Selecteer **Logboek opschonen**.

2. Kies een van de volgende opties voor het selecteren van logboeken die u wilt verwijderen:

   - Tabel-ID
   - Type logboek
   - Aanmaakdatum en -tijd

3. Gebruik het tabblad **Databaselogboek opschonen** om te bepalen wanneer u de taak voor het opschonen van het logboek wilt uitvoeren. Databaselogboeken zijn standaard 30 dagen beschikbaar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
