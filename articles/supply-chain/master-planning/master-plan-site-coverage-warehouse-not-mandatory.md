---
title: Hoofdplanning voor locatiebehoefte, magazijn niet verplicht
description: In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatiedimensie is ingesteld voor de behoefteplanning.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9475a7fbe40d7feb60c23e0d7164222469dffa75
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552317"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Hoofdplanning voor locatiebehoefte, magazijn niet verplicht

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatiedimensie is ingesteld voor de behoefteplanning.

Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.
-   De magazijndimensie is niet ingesteld als verplicht. Het magazijn kan bekend zijn, maar wordt niet bij de berekening van de hoofdplanning gebruikt.
-   De locatiedimensie is ingesteld voor de behoefteplanning.
-   De magazijndimensie is niet ingesteld voor de behoefteplanning. Vraag en aanbod worden daarom samengevoegd per site en mogelijk ook andere dimensies voor de behoefteplanning.

In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat. In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:
-   De artikelbehoefteplanning wordt gedefinieerd voor het artikel. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en klik vervolgens op **Plannen &gt; Artikelbehoefteplanning**.
-   Aanvullingsrelaties zijn gedefinieerd voor het magazijn. Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**. Zie op het tabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.
-   Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en klik vervolgens op **Plannen &gt; Standaard orderinstellingen**. Raadpleeg in het formulier **Standaard orderinstellingen** het veld **Standaardordertype**.

![Vraag naar locatie en magazijndekking niet verplicht](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>Aanvullende resources
--------

[Hoofdplanning en de functionaliteit voor meerdere locaties](master-plan-multisite-functionality.md)

[Hoofdplanning - locatiebehoefte, magazijn verplicht](master-plan-site-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatie- en magazijnbehoefte, magazijn niet verplicht](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hoofdplanning - locatie en magazijnbehoefte, magazijn verplicht](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hoofdplanning - hoe de stuklijstversie wordt bepaald](master-plan-bom-version-determined.md)



