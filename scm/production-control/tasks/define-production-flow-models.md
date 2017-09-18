--- 
title: "Modellen voor productiestroom definiëren"
description: De modellen voor productiestromen beschrijven hoe de capaciteit van werkcellen voor lean manufacturing wordt berekend en onderhouden.
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 3da0b5c4fc50136a98017e37b65afea9f8ec7b38
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="define-production-flow-models"></a>Modellen voor productiestroom definiëren

[!include[task guide banner](../../includes/task-guide-banner.md)]

De modellen voor productiestromen beschrijven hoe de capaciteit van werkcellen voor lean manufacturing wordt berekend en onderhouden. Daarom is de definitie van een model voor productiestroom een vereiste voor de definitie van werkcellen. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="define-a-production-flow-model"></a>Definieer een model voor productiestroom. 
1. Ga naar Productiebeheer > Instellen > De productiestroom > Modellen voor productiestroom.
2. Klik op Nieuw.
3. Voer in het veld Model voor productiestroom een id in voor het model voor productiestroom.
4. Selecteer een optie in het veld Modeltype.
    * Er zijn twee modeltypen: type Doorvoer en type Uren. Voor het type Doorvoer wordt de capaciteit van werkcellen die dit model voor productiestroom gebruiken, uitgedrukt en berekend in producthoeveelheden. Voor het type Uren wordt de capaciteit van werkcellen die dit model voor productiestroom gebruiken, uitgedrukt en berekend in uren. Deze eigenschap kan voor een bestaand model voor productiestroom niet worden gewijzigd. Nadat een werkcel capaciteitsreserveringen heeft, kunt u het model voor productiestroomtype niet wijzigen.  
5. Voer in de EPE-cyclus het aantal dagen in.
    * Het interval beschrijft de periode wanneer elk deel dat door een productiestroom of werkcel wordt geproduceerd ten minste eenmaal wordt geproduceerd. Hoe korter de EPE-cyclus, hoe flexibeler het productieproces is. Als EPE-cyclus = 0, kan alle vraag op dezelfde dag worden geproduceerd. De EPE-cyclus wordt gebruikt om lean procestaken te plannen. Bij het plannen van een taak op een werkcel met EPE-cyclus = 5, zoekt het planningsproces naar capaciteit op de werkcel op Vervaldatum - EPE-cyclus (5 dagen vóór de vervaldatum) om ervoor te zorgen dat het product in die cyclus kan worden geproduceerd. De voorraadlevertijd van een product is meestal gelijk aan of groter dan de EPE-cyclus van het gerelateerde productieproces.  
6. Selecteer een optie in het veld Type planningsperiode.
    * Nadat een werkcel capaciteitsreserveringen heeft, kunt u het type planningsperiode niet meer wijzigen. U kunt voor deze specifieke werkcel alleen modellen voor productiestromen selecteren met hetzelfde periodetype.  
7. Voer in het veld Time fence voor de planning een aantal dagen in.
    * De time fence voor de planning beschrijft het aantal dagen waarin de capaciteitsreserveringen voor de gerelateerde werkcellen kunnen worden gemaakt. Voer in Time fence voor de planning het aantal dagen in.   De taken van het kanbanproces die buiten deze periode vallen, worden niet gepland met automatische planning. De time fence voor planning is gewoonlijk tweemaal de gemiddelde voorraadlevertijd van de producten die in een productiestroom of werkcel worden geproduceerd. De EPE-cyclus mag niet meer dan de helft van de time fence voor planning zijn.     
8. Selecteer een optie in het veld Reactie bij capaciteitstekort.
    * De opties zijn: Uitstellen - Stel de volledige vraag van de planningsgebeurtenis uit naar de volgende beschikbare productiedag, met beschikbare doorvoer. Annuleren - Beëindig de automatische planning voor de planningsgebeurtenis en laat de verwante taken ongepland.   Toevoegen aan de aangevraagde dag - Plan de aangevraagde taken voor de opgegeven periode. Hierdoor wordt de cel voor deze dag overbelast en moet de planner dit controleren en een handmatige interactie ondernemen.   Verdelen naar beschikbare perioden - Verdeel de verschillende taken van de planningsgebeurtenis over alle beschikbare productiedagen en begin met de eerste beschikbare dag. De minimale distributiehoeveelheid is de kanbantaakhoeveelheid. De verdeling wijst de minimale planningshoeveelheid (kanbanhoeveelheid) toe aan elke dag met voldoende beschikbare doorvoer.  

