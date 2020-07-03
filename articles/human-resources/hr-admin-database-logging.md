---
title: Databaselogboeken configureren en beheren
description: U kunt wijzigingen in tabellen en velden in Dynamics 365 Human Resources bijhouden met databaselogboeken.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443569"
---
# <a name="configure-and-manage-database-logging"></a>Databaselogboeken configureren en beheren

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
2. Voer de wizard uit.

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
