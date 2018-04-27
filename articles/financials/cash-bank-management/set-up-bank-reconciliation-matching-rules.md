---
title: Afstemmingsregels voor bankafstemming instellen
description: In dit onderwerp wordt beschreven hoe afstemmingsregels en sets afstemmingsregels kunnen worden ingesteld om het bankafstemmingsproces te vereenvoudigen. Afstemmingsregels zijn een reeks criteria die worden gebruikt om regels van bankafschriften en bankdocumentregels te filteren tijdens het afstemmingsproces.
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b48accdc7aaaa65b4c620777546b20056038905b
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Afstemmingsregels voor bankafstemming instellen

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe afstemmingsregels en sets afstemmingsregels kunnen worden ingesteld om het bankafstemmingsproces te vereenvoudigen. Afstemmingsregels zijn een reeks criteria die worden gebruikt om regels van bankafschriften en bankdocumentregels te filteren tijdens het afstemmingsproces.

U kunt afstemmingsregels en sets afstemmingsregels instellen om het bankafstemmingsproces te vereenvoudigen. Een afstemmingsregel is een reeks criteria die worden gebruikt om regels van bankafschriften en banktransactieregels van Microsoft Dynamics 365 for Finance and Operations te filteren tijdens het afstemmingsproces. Gebruik de pagina **Afstemmingsregels** om de afstemmingsregels in te stellen. U kunt meerdere afstemmingsregels instellen en vervolgens een afstemmingsregelset maken op de pagina **Afstemmingsregelsets**. 

> [!NOTE] 
> Bankafstemmingsregels worden gebruikt als u een elektronisch bankafschrift afstemt met behulp van geavanceerde bankafstemming. 

Op de pagina **Afstemmingsregels** kunt u selecteren welke acties en selectiecriteria worden gebruikt wanneer de afstemmingsregel wordt uitgevoerd. Selecteer in de veldgroep **Acties** welke actie wordt uitgevoerd wanneer de afstemmingsregel wordt uitgevoerd tijdens het afstemmingsproces.  

> [!NOTE] 
> De geselecteerde optie bepaalt welke velden worden weergegeven.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Actie**                         |                                                                                                                                                                                                                                                                                                               | **Beschikbare selectiecriteria wanneer de actie wordt geselecteerd**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Afstemmen met bankdocument**       | Maak criteria om op te geven hoe de bankdocumenten en bankafschriftregels worden afgestemd wanneer de afstemmingsregel wordt uitgevoerd vanuit de pagina **Werkblad voor bankafstemming**. De transactieregels worden geselecteerd in overeenstemming met de aanvullende criteria die zijn ingesteld op de sneltabbladen.                                | **Stap 1: de afstemmingsregel definiëren**: selecteer criteria om op te geven welke bankafschriften met Finance and Operations-banktransacties moeten worden afgestemd. **Stap 2 (optioneel): selecteer de overzichtregels ten opzichte waarvan afstemmingsregels moeten worden uitgevoerd:** Pas een filter toe op de afschriftregel ten opzichte waarvan de regels moeten worden uitgevoerd.                                                                                                                                                                                                                                                                                                               |
| **Terugboekingsregels op een afschrift wissen** | Maak criteria om op te geven hoe terugboekingsregels moeten worden verwijderd van de pagina **Werkblad voor bankafstemming** wanneer de afstemmingsregel wordt uitgevoerd. Deze optie wordt gebruikt wanneer de bank een fout maakt en er twee bankafschriftregels moeten worden weergegeven in het geïmporteerde bankafschrift en de regels moeten worden afgestemd. | **Stap 1**:**terugboekingsregels op afschrift zoeken**: voeg selectiecriteria toe om terugboekingsregels van het bankafschrift te selecteren. Als u bijvoorbeeld alleen cheques wilt selecteren, selecteert u de **Banktransactiecode**, selecteert u het plusteken (+) in het veld **Operator** en voert u vervolgens **Cheques** in het veld Waarde in. **Stap 2: oorspronkelijke afschriftregels zoeken**: u kunt selectiecriteria toevoegen om bankdocumentregels af te stemmen op bankafschriftregels. **Stap 3: Finance and Operations-banktransacties zoeken**: u kunt selectiecriteria toevoegen om banktransacties van Finance and Operations af te stemmen met bankafschriftregels. |
| **Nieuwe transacties markeren**          | Maak criteria om op te geven hoe nieuwe transacties moeten worden gemarkeerd op de pagina **Werkblad voor bankafstemming** wanneer de afstemmingsregel wordt uitgevoerd.                                                                                                                                                                 | **Stap 1: afschriftregels zoeken**: voeg selectievelden toe om op te geven welke bankafschriftregels moeten worden geselecteerd op de pagina **Bankafstemmingswerkblad**. **Stap 2: Finance and Operations-banktransacties zoeken**: u kunt selectiecriteria toevoegen om bankdocumentregels te zoeken. Als er geen bankdocument wordt gevonden, wordt een afschriftregel als een nieuwe transactie gemarkeerd.                                                                                                                                                                                                                                             |









