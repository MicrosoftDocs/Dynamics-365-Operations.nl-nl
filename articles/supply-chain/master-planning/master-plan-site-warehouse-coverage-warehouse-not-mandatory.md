---
title: Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht
description: Dit artikel beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is niet verplicht.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4989a05f4647ac836b78692da7f63396dbef788
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741007"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is niet verplicht.

Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie. Deze instelling kan niet worden gewijzigd.
-   De magazijndimensie is niet ingesteld als verplicht. Het magazijn kan bekend zijn, maar wordt niet bij de berekening van de hoofdplanning gebruikt.
-   De site- en magazijndimensie zijn ingesteld voor de behoefteplanning. Er kunnen ook andere dimensies worden ingesteld voor de behoefteplanning. De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.

In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat. In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:
-   Het magazijn is ingesteld op handmatig. Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**. Ga op het sneltabblad **Hoofdplanning** naar het veld **Handmatig**.
-   De artikelbehoefteplanning wordt gedefinieerd voor het artikel. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Artikelbehoefte**.
-   Aanvullingsrelaties zijn gedefinieerd voor het magazijn. Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**. Zie op het sneltabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.
-   Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Standaard orderinstellingen**. Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.

![Vraag naar locatie en magazijn, magazijn niet.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van de hoofdplanning en functionaliteit voor meerdere locaties](master-plan-multisite-functionality.md)
- [Hoofdplanning voor locatiebehoefte, magazijn verplicht](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht](master-plan-site-coverage-warehouse-mandatory.md)
- [Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht](master-plan-site-coverage-warehouse-not-mandatory.md)
- [De stuklijstversie bepalen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]