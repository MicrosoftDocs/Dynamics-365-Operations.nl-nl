---
title: Kostengroepen
description: Kostengroepen vormen de basis voor het segmenteren en analyseren van kostenbijdragen in de berekende kosten van een gefabriceerd artikel, zoals de kostenbijdragen voor materiaal, arbeid en overhead. Voor segmentatie van kostengroepen worden in de productieomgeving verschillende synoniemen gehanteerd, zoals kostenanalyse, kostenontleding of kostenclassificatie.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef656e24aadfbf6edb7c15851ea4142edd9520e6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967767"
---
# <a name="cost-groups"></a>Kostengroepen

[!include [banner](../includes/banner.md)]

Kostengroepen vormen de basis voor het segmenteren en analyseren van kostenbijdragen in de berekende kosten van een gefabriceerd artikel, zoals de kostenbijdragen voor materiaal, arbeid en overhead. Voor segmentatie van kostengroepen worden in de productieomgeving verschillende synoniemen gehanteerd, zoals kostenanalyse, kostenontleding of kostenclassificatie. 

Voor segmentatie van kostengroepen worden in de productieomgeving verschillende synoniemen gehanteerd, zoals kostenanalyse, kostenontleding of kostenclassificatie. Segmentatie van kostengroepen kan voor verschillende doeleinden worden gebruikt. Hieronder vindt u enkele voorbeelden:

-   Het kan kosten voor verschillende materiaaltypen, zoals ingrediënten en verpakkingsmateriaal voor levensmiddelen in blik, segmenteren op basis van de kostengroepen die aan artikelen zijn toegewezen.
-   Het kan kosten voor verschillende typen bronnen voor bedrijfsactiviteiten, zoals verschillende typen arbeid of machines, segmenteren op basis van de kostengroepen die zijn toegewezen aan kostencategorieën die zijn gerelateerd aan bronnen voor bedrijfsactiviteiten en routebewerkingen.
-   Het kan kosten voor de instel- en uitvoeringstijd in routebewerkingen segmenteren, op basis van de kostengroepen die zijn toegewezen aan kostencategorieën die zijn gerelateerd aan de routebewerkingen.
-   Het kan kosten voor verschillende typen overhead, zoals arbeids- en machineoverheads, segmenteren op basis van de kostengroepen die zijn toegewezen aan indirecte kosten in de instellingen van de kostprijsberekening.
-   Het kan dienen als basis voor het berekenen van diverse typen productieoverhead bij het definiëren van de kostprijsberekening. Deze overhead kan bestaan uit verschillende typen overhead die gerelateerd zijn aan routeringsgegevens voor bronnen voor bedrijfsactiviteiten of gegevens over de instel- en uitvoeringstijd. Productieoverhead kan ook gerelateerd zijn aan kostenbijdragen van onderdeelmateriaal, wat een lean-manufacturingbenadering weerspiegelt waarbij routeringsgegevens overbodig zijn.

Segmentatie van kostengroepen is van toepassing op de berekende kosten van een gefabriceerd artikel, ongeacht of deze kosten zijn gebaseerd op standaardkosten of geplande kosten. De pagina **Overzicht** geeft deze segmentatie weer op kostengroep, op niveau, of op zowel kostengroep als niveau. 

De term *splitsen* verwijst naar de mogelijkheid om kostengroepsegmentatie op meerdere niveaus in een productstructuur te behouden. Splitsen geldt alleen voor gefabriceerde artikelen die een standaardkostenvoorraadmodel gebruiken. Zonder splitsing worden de kosten van een gefabriceerd onderdeel beschouwd als een materiaalkostenbijdrage. De voorraadparameter voor kostenanalyse per grootboek geeft aan dat kostengroepsegmentatie op meerdere niveaus in standaardkostenberekeningen behouden blijft. Terwijl bij een beleid zonder niveaus kostengroepsegmentatie alleen van toepassing is op een berekening met één niveau. De pagina **Kostenvergaring per kostengroep** geeft bijvoorbeeld de kostengroepsegmentatie weer over meerdere niveaus voor standaardkostenartikelen. 

Kostengroepsegmentatie kan ook van toepassing zijn op afwijkingen voor een standaardkostenartikel. Een tweede voorraadparameter definieert of afwijkingen worden aangegeven per kostengroep, of alleen worden samengevat. 

Aan een kostengroep kunnen een kostengroeptype en gedrag voor extra segmentatie worden toegewezen.

-   **Kostengroeptype** − aan elke kostengroep moet een kostengroeptype worden toegewezen, waarmee wordt aangegeven dat de kostengroep van toepassing is op directe materialen, directe productie of directe outsourcing of om aan te geven dat deze indirect of ongedefinieerd is. Een kostengroep waarvoor is aangegeven dat directe materialen aan artikelen kunnen worden toegewezen. Een kostengroep voor directe productie kan aan kostencategorieën worden toegewezen. Een kostengroep directe outsourcing kan aan een producttype service worden toegewezen, zodat u kosten kunt classificeren die aan de inkoop van services voor uitbestedingsactiviteiten zijn gekoppeld. Een indirecte-kostengroep kan worden toegewezen aan indirecte kosten voor toeslagen of tarieven. Een kostengroep die is ingesteld als ongedefinieerd, kan worden toegewezen aan artikelen, kostencategorieën of indirecte kosten. Een kostengroeptype wordt toegewezen voor verschillende doeleinden. Allereerst kunnen er minder kostengroepen worden toegewezen en wordt een lijst met toepasselijke kostengroepen weergegeven. Ten tweede biedt de toewijzing extra segmentatie voor rapportagedoeleinden. Tot slot kan toewijzing worden gebruikt om grootboekrekeningen voor afwijkingen toe te wijzen.
-   **Gedrag** − aan elke kostengroep kan desgewenst een gedrag worden toegewezen om aan te geven dat de kostengroep geldt voor vaste of variabele kosten. Kostengroepen met een null-waarde voor gedrag worden beschouwd als variabele kosten. Een gedrag wordt alleen toegewezen voor rapportagedoeleinden. Kosten kunnen bijvoorbeeld worden weergegeven met segmentatie van vaste en variabele kosten in de kostprijsberekening en op de pagina **Kostenvergaring per kostengroep**. Als u een winstinstellingspercentage aan elke kostengroep toewijst, bevat de stuklijstberekening een voorgestelde verkoopprijs op basis van de kostprijs plus een opslagpercentage.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]