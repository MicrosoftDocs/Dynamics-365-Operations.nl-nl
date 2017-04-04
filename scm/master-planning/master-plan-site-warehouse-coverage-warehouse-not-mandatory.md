---
title: Hoofdplanning voor locatie en magazijn niet verplicht magazijn
description: Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is niet verplicht.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3671024dc097c94638b1579d7cacc8447c49e97b
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Hoofdplanning voor locatie en magazijn niet verplicht magazijn

Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is niet verplicht.

Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie. Deze instelling kan niet worden gewijzigd.
-   De magazijndimensie is niet ingesteld als verplicht. Het magazijn kan bekend zijn, maar wordt niet bij de berekening van de hoofdplanning gebruikt.
-   De site- en magazijndimensie zijn ingesteld voor de behoefteplanning. Er kunnen ook andere dimensies worden ingesteld voor de behoefteplanning. De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.

In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat. In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:
-   Het magazijn is ingesteld op handmatig. Klik op **voorraadbeheer &gt;Setup &gt;opsplitsing van voorraad &gt;magazijnen**. Ga op het sneltabblad **Hoofdplanning** naar het veld **Handmatig**.
-   De artikelbehoefteplanning wordt gedefinieerd voor het artikel. Klik op **productgegevensbeheer &gt;producten&gt; vrijgegeven producten**. Selecteer het artikel en klik in het actievenster op het **plannen** en klik op **artikelbehoefteplanning**.
-   Aanvullingsrelaties zijn gedefinieerd voor het magazijn. Klik op **voorraadbeheer &gt;Setup &gt;opsplitsing van voorraad &gt;magazijnen**. Zie op het sneltabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.
-   Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban. Klik op **productgegevensbeheer &gt;producten&gt; vrijgegeven producten**. Selecteer het artikel en klik in het actievenster op het **plannen** en klik op **standaard orderinstellingen**. Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.

![Vraag naar locatie en magazijn, magazijn niet](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>Zie ook
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Hoofdplanning - locatie en magazijnbehoefte, magazijn verplicht](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatiebehoefte, magazijn verplicht](master-plan-site-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatiebehoefte, magazijn niet verplicht](master-plan-site-coverage-warehouse-not-mandatory.md)

[Hoofdplanning - hoe de stuklijstversie wordt bepaald](master-plan-bom-version-determined.md)


