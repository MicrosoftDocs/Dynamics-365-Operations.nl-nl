---
title: 'Gemengde planmodus: combineer discrete sourcing, processourcing en lean sourcing'
description: Dit onderwerp biedt informatie over de gemengde planmodus.
author: cvocph
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4c9c7d244e7709491cfa97283a9ea0a33914817e3f6d69923d4910796f276d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759450"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Gemengde planmodus: combineer discrete sourcing, processourcing en lean sourcing

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over de gemengde planmodus. Bij de gemengde planmodus kunt u uw leveringsketen modelleren op basis van de materiaalstroom. Dynamics 365 Supply Chain Management zorgt ervoor dat de materiaalstroom uw modellen volgt, ongeacht het leveringsbeleid dat is geselecteerd (kanbans, productieorders, inkooporders, batchorders of overboekingsorders). 

U kunt uw algemene strategie voor productlevering selecteren, ongeacht de productstructuur.  

U kunt bijvoorbeeld kanbancontrole hebben in de assembly, waaruit materialen voor het assemblygebied worden gehaald door productieorders, kanbans, overboekingen, batchorders of een combinatie die past bij de kenmerken van uw leveringsketen, maar toch volledige zichtbaarheid van leveringen hebben. Deze capaciteit leidt tot geoptimaliseerde processen in de keten van toeleveranciers en uitgebreide zichtbaarheid in uw leveringsketen.  

Gedetailleerdheid van het leveringsbeleid dat in de hoofdplanning gebruikt wordt, is afhankelijk van de opslagdimensies die als dekkingsdimensies zijn ingeschakeld. Om de hoofdplanning in te schakelen voor het controleren van de aanvulling en levering van verschillende typen locaties (bijvoorbeeld door de productievloer voor verschillende productie-eenheden te scheiden of door verschillende magazijnen te gebruiken voor verschillende typen materialen en eindproducten), is het raadzaam locatie en magazijn in te schakelen als behoefteplanningsdimensies. Als alternatief kan Magazijn worden weggelaten als behoefteplanningsdimensie. In dat geval, als u geavanceerd magazijnbeheer gebruikt, worden alle verplaatsing binnen een magazijn bepaald door magazijnwerk, terwijl alle verplaatsing tussen magazijnen kunnen worden bepaald door terugtrekkingskanbans.

## <a name="supply-policies"></a>Leveringsbeleid
Met de gemengde planmodus bepaalt hoe een product wordt geleverd en, op basis van de voorraad, hoe de afgeleide behoeften (verbruik van artikelen van een stuklijst of \[BOM\]) worden uitgegeven. Op basis van het ordertype vindt het systeem automatisch materialen om aan de vereisten te voldoen.  

Het leveringsbeleid kan worden gedefinieerd op het productniveau of op elk niveau van gedetailleerdheid dat voldoet aan uw behoeften. U definieert de gedetailleerdheid van leveringsbeleid op de pagina **Standaard orderinstellingen**.  

Het leveringsbeleid kan worden gecontroleerd per product, artikeldimensie (configuratie, kleur en grootte), site en magazijn. Deze instellingen worden uitgevoerd op de pagina **Artikelbehoefteplanning**.  

Het standaardordertype bepaalt welke order de hoofdplanning genereert.  

Ongeacht hoe de leveringsketen wordt gemodelleerd, ondersteunt Supply Chain Management uw specifieke leveringsbeleid. U kunt productieorders hebben die kanbans als bron hebben. Als alternatief kunt u een batchorder hebben die vereist dat een product wordt geleverd door overboekingen of kanbans.  

Supply Chain Management zorgt ervoor dat de materiaalstroom het model volgt.  

Het magazijn voor het verzamelen van materiaal wordt dynamisch toegewezen tijdens uitvoeringstijd, nadat het leveringsbeleid is gedefinieerd.  

Doorgaans worden kanbans niet gemaakt voor toekomstige datums, omdat een kanban een korte levenscyclus heeft. Voor volledige zichtbaarheid in de leveringsketen, hebben we het nieuwe planningsconcept "geplande kanban" geïntroduceerd, wat wordt gebruikt om afgeleide behoeften te berekenen en helpt ervoor te zorgen dat de behoeften worden gebaseerd op dezelfde logica die wordt gebruikt wanneer de werkelijke kanban wordt gemaakt.  

Dezelfde logica is aanwezig voor alle andere typen leveringsbeleid. Daarom is materiaalplanning op de lange termijn gebaseerd op dezelfde logica als u kunt verwachten bij de werkelijke orders nadat de productie en de levering zijn goedgekeurd.

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>Het kruislingse-leveringsbeleid voor de materialentoewijzing - resourceverbruik op stuklijsten
Resourceverbruik is een belangrijke functionaliteit. Resourceverbruik stelt een magazijn in staat verzamelmaterialen dynamisch te selecteren, op basis van het leveringsbeleid (ordertype) en maakt ook het bijhouden van de basisgegevens eenvoudiger.  

Resourceverbruik vereist dat het magazijn waarin de materialen worden verzameld, wordt toegewezen aan de hand van de manier waarop het product wordt geleverd. Met andere woorden, tijdens uitvoeringstijd vindt het systeem de bronnen die voor productie moeten worden gebruikt. Op basis van die bronnen vindt het systeem vervolgens het verzamelmagazijn.  

Voor werk dat onafhankelijk is van een leveringsbeleid hoeft u geen informatie te wijzigen op de stuklijst als de levering verandert. Bij ad-hoc wijzigingen zorgt Supply Chain Management ervoor dat de materialen van het juiste magazijn afkomstig zijn.

## <a name="process-manufacturing--the-production-type"></a>Procesfabricage - het productietype
Voor volledige flexibiliteit in de gemengde modus wordt u aangeraden het productietype stuklijsten te gebruiken voor alle producten. Vervolgens kunt u productieorders, kanbans, overboekingsorders of inkooporders voor het leveren van een product gebruiken. Voor procesfabricage moet u het productietype **Formule**, **Coproduct**, **Bijproduct** of **Planningsartikel** gebruiken. Kanbans en productieorders kunnen niet voor deze productietypen worden gebruikt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]