---
title: Workflowacties
description: In dit artikel worden de acties beschreven die elke deelnemer in een goedkeuringsproces kan uitvoeren.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a4717accfa7e5879ee757820c39f000fa7d3e95
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-actions"></a>Workflowacties

[!include [banner](../includes/banner.md)]

In dit artikel worden de acties beschreven die elke deelnemer in een goedkeuringsproces kan uitvoeren.

Bij een workflow kunnen meerdere groepen gebruikers zijn betrokken: de starter, degenen aan wie taken zijn toegewezen, degenen die beslissingen nemen en fiatteurs. Hieronder ziet u een workflow voor een onkostennota. In dit voorbeeld is Sam de starter, zijn de leden van de wachtrij toegewezenen, is Jan een besluitvormer en zijn Frank, Suzan en Anne de fiatteurs.   

[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif) 

In de volgende secties worden de workflowacties beschreven die door elk van deze groepen kan worden uitgevoerd.

## <a name="actions-that-an-originator-can-perform"></a>Acties die kunnen worden uitgevoerd door een starter
De opdrachtgever start een workflowexemplaar door een document ter verwerking aan te bieden. Als Sam bijvoorbeeld zijn onkostennota wilt verzenden, moet hij klikken op de knop **Aanbieden** op de pagina **Onkostennota**.

## <a name="actions-that-a-task-assignee-can-perform"></a>Acties die kunnen worden uitgevoerd door een toegewezene
Een taak kan worden toegewezen aan meerdere personen of aan een wachtrij voor werkitems die door meerdere mensen wordt gecontroleerd. Slechts één persoon kan echter een taak uitvoeren. Stel dat Sam in de bovenstaande workflow een onkostennota heeft ingediend en de ontvangstbewijzen ter controle naar de afdeling voor onkostennota's van zijn organisatie heeft gestuurd. 

De leden van de afdeling Onkostennota's van Adventure Works controleren de wachtrij. Julie, een lid van die afdeling, heeft de taak geaccepteerd om de onkostennota en ontvangstbewijzen van Sam te controleren. Ze kan nu een van de volgende acties uitvoeren: voltooien, afwijzen, delegeren, een wijziging aanvragen, opnieuw toewijzen of vrijgeven. 

**Opmerking:** Welke acties beschikbaar zijn, is afhankelijk van de manier waarop de taak door de softwareontwikkelaar is ontworpen.

### <a name="complete"></a>Voltooien

Als een gebruiker een taak voltooit, wordt het document dat is ingediend voor verwerking zo nodig toegewezen aan de volgende gebruiker in de workflow (als deze een volgende gebruiker bevat). Als er geen verdere verwerking vereist is, eindigt het workflowproces. 

Stel dat Julie een lid is van de afdeling voor onkostennota's van Adventure Works en ze de taak heeft geaccepteerd om de onkostennota en ontvangstbewijzen van Sam te controleren. Nadat Julie de controle heeft voltooid, wordt het document aan Jan toegewezen.

### <a name="reject"></a>Weigeren

Als een gebruiker een document afwijst, eindigt het workflowproces. 

Stel dat Julie een lid is van de afdeling voor onkostennota's van Adventure Works en ze de taak heeft geaccepteerd om de onkostennota en ontvangstbewijzen van Sam te controleren. Als Julie de onkostennota afwijst, eindigt het workflowproces. 

Sam kan de onkostennota vervolgens opnieuw indienen. Hij kan eerst wijzigingen aanbrengen of de oorspronkelijke versie opnieuw indienen. Als Sam de onkostennota opnieuw indient, start het workflowproces vanaf de handmatige controletaak.

### <a name="delegate"></a>gemachtigde

Wanneer een gebruiker een taak delegeert, wordt deze taak aan een andere gebruiker toegewezen. 

Stel dat Julie een lid is van de afdeling voor onkostennota's van Adventure Works en ze de taak heeft geaccepteerd om de onkostennota en ontvangstbewijzen van Sam te controleren. Julie delegeert deze taak aan haar assistent Tim. 

Tim handelt dan namens Julie. Wanneer Tim zijn controle voltooit, wordt de onkostennota daarom aan Jan toegewezen, net als wanneer Julie de taak had voltooid.

### <a name="request-change"></a>Wijziging aanvraag

Wanneer een gebruiker een wijziging aanvraagt in een aangeboden document, wordt dit document teruggestuurd naar de opdrachtgever. 

Stel dat Julie een lid is van de afdeling voor onkostennota's van Adventure Works en ze de taak heeft geaccepteerd om de onkostennota en ontvangstbewijzen van Sam te controleren. Julie merkt enkele fouten in de onkostennota op en vraagt wijzigingen aan. De onkostennota wordt weer naar Sam verzonden. 

Sam kan de onkostennota opnieuw indienen. Hij kan eerst de gevraagde wijzigingen aanbrengen of de oorspronkelijke versie opnieuw indienen. Als Sam de onkostennota opnieuw indient, moet een lid van de wachtrij voor werkitems de onkostennota en de ontvangstbewijzen opnieuw controleren.

### <a name="reassign"></a>Opnieuw toewijzen

De leden van een wachtrij voor werkitems kunnen documenten in die wachtrij opnieuw toewijzen aan een andere wachtrij. 

Stel dat Julie een lid is van de afdeling Onkostennota's van Adventure Works en de wachtrij controleert. Om de werklast te balanceren, kan ze de onkostennota en de bijbehorende ontvangstbewijzen opnieuw toewijzen aan een andere wachtrij.

### <a name="release"></a>Vrijgave

Soms komt het voor dat een lid van de wachtrij voor werkitems een taak accepteert, maar besluit daarna dat hij of zij de taak niet kan voltooien. In dit geval kan de persoon die de taak heeft geaccepteerd het document weer vrijgeven aan de wachtrij voor werkitems. 

Stel dat Julie een lid is van de afdeling voor onkostennota's van Adventure Works en ze de taak heeft geaccepteerd om de onkostennota en ontvangstbewijzen van Sam te controleren. Als Julie beslist dat ze de taak niet kan voltooien, kan ze het document vrijgeven. De onkostennota komt weer in de wachtrij terecht zodat andere leden van de afdeling Onkostennota's van Adventure Works de taak kunnen voltooien.

## <a name="actions-that-a-decision-maker-can-perform"></a>Acties die een besluitvormer kan uitvoeren
Wanneer een document aan een besluitvormer is toewezen, is dit doorgaans omdat de besluitvormer een vraag moet beantwoorden. Het antwoord op de vraag is doorgaans **Ja** of **Nee** of **Waar** of **Onwaar**. Als de besluitvormer geen van deze opties selecteert, kan hij of zij de beslissing delegeren.

### <a name="choice-1-or-choice-2"></a>\[Keuze 1\] of \[Keuze 2\]

Een besluitvormer moet een vraag beantwoorden voor het document. Het antwoord op de vraag is doorgaans **Ja** of **Nee** of **Waar** of **Onwaar**. Het antwoord van de besluitvormer bepaalt welke tak van de workflow wordt gebruikt om het document te verwerken. 

Stel dat de onkostennota van Sam aan Jan is toegewezen. Jan moet beslissen of voor de informatie op de onkostennota een telefoontje naar de manager van Sam is vereist. Als Jan beslist dat een telefoontje is vereist, wordt de onkostennota aan Aretha toegewezen, die vervolgens de manager van Sam moet bellen. Als Jan beslist dat geen telefoontje is vereist, wordt de onkostennota aan Frank toegewezen ter goedkeuring.

### <a name="delegate"></a>Delegeren

Wanneer een besluitvormer een beslissing delegeert, wordt het document aan een andere gebruiker toegewezen die de beslissing moet nemen. 

Stel dat de onkostennota van Sam aan Jan is toegewezen. Jan delegeert de beslissing naar zijn assistente Marie. 

Marie handelt dan namens Jan. Als Marie beslist dat de manager van Sam moet worden gebeld, wordt de onkostennota aan Aretha toegewezen, die vervolgens de manager van Sam moet bellen. Als Marie beslist dat geen telefoontje is vereist, wordt de onkostennota aan Frank toegewezen ter goedkeuring.

## <a name="actions-that-an-approver-can-perform"></a>Acties die kunnen worden uitgevoerd door een fiatteur
Wanneer een document aan een fiatteur wordt toegewezen, kan de fiatteur een van de volgende acties uitvoeren: goedkeuren, afwijzen, delegeren of een wijziging aanvragen.

### <a name="approve"></a>Goedkeuren

Een document dat door een fiatteur wordt goedgekeurd, wordt toegewezen aan de volgende gebruiker in de workflow (als deze een volgende gebruiker bevat). Als er geen verdere verwerking vereist is, eindigt het workflowproces. 

Stel dat Sam een onkostennota van EUR 6.000 heeft ingediend, die is toegewezen aan Frank. Nadat Frank het document heeft goedgekeurd, wordt het ter goedkeuring aan Suzan toegewezen. Wanneer Suzan de onkostennota heeft goedgekeurd, eindigt het workflowproces.

### <a name="reject"></a>Weigeren

Wanneer een fiatteur een document afwijst, wordt het workflowproces beëindigd. 

Stel dat Sam een onkostennota van EUR 12.000 heeft ingediend, die is toegewezen aan Suzan. Als Suzan de onkostennota afwijst, eindigt het workflowproces. 

Sam kan de onkostennota opnieuw indienen. Hij kan eerst de gevraagde wijzigingen aanbrengen of de oorspronkelijke versie van de onkostennota opnieuw indienen. Als Sam de onkostennota opnieuw indient, start het workflowproces bij het goedkeuringsproces.

### <a name="delegate"></a>Delegeren

Wanneer een fiatteur een document delegeert, wordt het document ter goedkeuring toegewezen aan een andere gebruiker. 

Stel dat Sam een onkostennota van EUR 12.000 heeft ingediend, die is toegewezen aan Frank. Frank delegeert de onkostennota aan Anne. 

Anne treedt op namens Frank. Wanneer Anne het document goedkeurt, wordt het daarom ter goedkeuring aan Suzan toegewezen, net als wanneer Frank het document zelf had goedgekeurd. Als Suzan het document goedkeurt, wordt het ter goedkeuring naar Anne verzonden.

### <a name="request-change"></a>Wijziging aanvraag

Wanneer een fiatteur een wijziging in een document aanvraagt, wordt het document teruggestuurd naar de opdrachtgever. 

Stel dat Sam een onkostennota van EUR 12.000 heeft ingediend, die is toegewezen aan Suzan. Als Suzan een wijziging aanvraagt, wordt de onkostennota teruggestuurd naar Sam. 

Sam kan de onkostennota opnieuw indienen. Hij kan eerst de gevraagde wijzigingen aanbrengen of de oorspronkelijke versie van de onkostennota opnieuw indienen. Als Sam de onkostennota opnieuw indient, wordt het ter goedkeuring naar Frank verzonden omdat hij de eerste fiatteur in het goedkeuringsproces is.




