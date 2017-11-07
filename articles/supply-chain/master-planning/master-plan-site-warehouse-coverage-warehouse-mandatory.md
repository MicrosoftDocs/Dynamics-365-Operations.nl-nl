---
title: Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht
description: Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is verplicht.
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e753edacb0e2e019d701745308e7d9190ef09fe8
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht

[!include[banner](../includes/banner.md)]


Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is verplicht.

Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.
-   De magazijndimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.
-   De site- en magazijndimensie zijn ingesteld voor de behoefteplanning. Er kunnen ook andere dimensies worden ingesteld voor de behoefteplanning. De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.

In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat. In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:
-   Het magazijn is ingesteld op **Handmatig**. Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**. Ga op het sneltabblad **Hoofdplanning** naar het veld **Handmatig**.
-   De artikelbehoefteplanning wordt gedefinieerd voor het artikel. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Artikelbehoefte**.
-   Aanvullingsrelaties zijn gedefinieerd voor het magazijn. Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**. Zie op het sneltabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.
-   Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Standaard orderinstellingen**. Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.

![Vraaglocatie en magazijndekking zonder verplicht magazijn](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Zie ook
--------

[Hoofdplanning en de functionaliteit voor meerdere locaties](master-plan-multisite-functionality.md)

[Hoofdplanning - locatiebehoefte, magazijn verplicht](master-plan-site-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatiebehoefte, magazijn niet verplicht](master-plan-site-coverage-warehouse-not-mandatory.md)

[Hoofdplanning - locatie- en magazijnbehoefte, magazijn niet verplicht](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hoofdplanning - hoe de stuklijstversie wordt bepaald](master-plan-bom-version-determined.md)




