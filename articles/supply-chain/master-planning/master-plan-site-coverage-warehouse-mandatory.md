---
title: Hoofdplanning voor locatiebehoefte, magazijn verplicht
description: In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatie is ingesteld als behoeftedimensie. De magazijndimensie is verplicht.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ca01913a0338004fabcda5136108ec3c5be8ff7
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Hoofdplanning voor locatiebehoefte, magazijn verplicht

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatie is ingesteld als behoeftedimensie. De magazijndimensie is verplicht.

Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie. Deze instelling kan niet worden gewijzigd.
-   De magazijndimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.
-   De locatiedimensie is ingesteld voor de behoefteplanning. U kunt ook andere dimensies instellen voor de behoefteplanning. De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.
-   De magazijndimensie is niet ingesteld voor de behoefteplanning. Vraag en aanbod worden daarom samengevoegd per site en mogelijk ook andere dimensies voor de behoefteplanning.

In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat. In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:
-   De artikelbehoefteplanning wordt gedefinieerd voor het artikel. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en klik vervolgens op **Plannen &gt; Artikelbehoefteplanning**.
-   Aanvullingsrelaties zijn gedefinieerd voor het magazijn. Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**. Zie op het tabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.
-   Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en klik vervolgens op **Plannen &gt; Standaard orderinstellingen**. Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.

![Vraag naar locatie en magazijndekking verplicht](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Zie ook
--------

[Hoofdplanning en de functionaliteit voor meerdere locaties](master-plan-multisite-functionality.md)

[Hoofdplanning - locatie en magazijnbehoefte, magazijn verplicht](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatiebehoefte, magazijn verplicht](master-plan-site-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatie- en magazijnbehoefte, magazijn niet verplicht](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hoofdplanning - hoe de stuklijstversie wordt bepaald](master-plan-bom-version-determined.md)




