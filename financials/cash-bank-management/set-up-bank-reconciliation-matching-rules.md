---
title: Afstemmingsregels voor bankafstemming instellen
description: In dit artikel wordt beschreven hoe afstemmingsregels en sets afstemmingsregels kunnen worden ingesteld om het bankafstemmingsproces te vereenvoudigen. Afstemmingsregels zijn een reeks criteria die worden gebruikt om regels van bankafschriften en bankdocumentregels te filteren tijdens het afstemmingsproces.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: e4c07a6afb90535c57f372d5b850919b5b34aaa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Afstemmingsregels voor bankafstemming instellen

In dit artikel wordt beschreven hoe afstemmingsregels en sets afstemmingsregels kunnen worden ingesteld om het bankafstemmingsproces te vereenvoudigen. Afstemmingsregels zijn een reeks criteria die worden gebruikt om regels van bankafschriften en bankdocumentregels te filteren tijdens het afstemmingsproces.

U kunt afstemmingsregels en sets afstemmingsregels instellen om het bankafstemmingsproces te vereenvoudigen. Afstemmingsregel voor bankafstemming is een reeks criteria die worden gebruikt voor het filteren van regels van bankafschriften en Microsoft Dynamics 365 op transactieregels van de bank bewerkingen tijdens het afstemmingsproces. Gebruik de pagina **Afstemmingsregels** om de afstemmingsregels in te stellen. U kunt meerdere afstemmingsregels instellen en vervolgens een afstemmingsregelset maken op de pagina **Afstemmingsregelsets**. 

> [!NOTE] 
> Afstemmingsregels bank worden gebruikt als u een elektronisch bankafschrift afstemmen met behulp van geavanceerde bankafstemming. 

Op de pagina **Afstemmingsregels** kunt u selecteren welke acties en selectiecriteria worden gebruikt wanneer de afstemmingsregel wordt uitgevoerd. In de **acties** veldgroep, selecteert u de actie die moet worden uitgevoerd wanneer de afstemmingsregel wordt uitgevoerd tijdens het afstemmingsproces.  

> [!NOTE] 
> De optie die u selecteert, bepaalt de velden die worden weergegeven.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Actie**                         |                                                                                                                                                                                                                                                                                                               | **Beschikbare selectiecriteria wanneer de actie wordt geselecteerd**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Afstemmen met bankdocument **       | Maak criteria om op te geven hoe de bankdocumenten en bankafschriftregels worden afgestemd wanneer de afstemmingsregel wordt uitgevoerd vanuit de pagina **Werkblad voor bankafstemming**. De transactieregels worden geselecteerd in overeenstemming met de aanvullende criteria die zijn ingesteld op de sneltabbladen.                                | **Stap 1: Definieer de overeenkomende regel** : selecteren van criteria die zijn om op te geven welke bankafschriften moeten worden vereffend met Dynamics 365 voor bewerkingen banktransacties. **Stap 2 (optioneel): selecteer de overzichtregels ten opzichte waarvan afstemmingsregels moeten worden uitgevoerd:** Pas een filter toe op de afschriftregel ten opzichte waarvan de regels moeten worden uitgevoerd.                                                                                                                                                                                                                                                                                                               |
| **Terugboekingsregels op een afschrift wissen** | Maak criteria om op te geven hoe terugboekingsregels moeten worden verwijderd van de pagina **Werkblad voor bankafstemming** wanneer de afstemmingsregel wordt uitgevoerd. Deze optie wordt gebruikt wanneer de bank een fout maakt en er twee bankafschriftregels moeten worden weergegeven in het geïmporteerde bankafschrift en de regels moeten worden afgestemd. | **Stap 1**:** terugboekingsregels op afschrift zoeken**: voeg selectiecriteria toe om terugboekingsregels van het bankafschrift te selecteren. Als u bijvoorbeeld alleen cheques wilt selecteren, selecteert u de **Banktransactiecode**, selecteert u het plusteken (+) in het veld **Operator** en voert u vervolgens **Cheques** in het veld Waarde in. **Stap 2: oorspronkelijke afschriftregels zoeken**: u kunt selectiecriteria toevoegen om bankdocumentregels af te stemmen op bankafschriftregels. ** Stap 3: Zoeken Dynamics 365 voor bewerkingen banktransacties **: U kunt selectiecriteria toevoegen om te voldoen aan Dynamics 365 voor bewerkingen banktransacties op bankafschriftregels. |
| **Mark new transactions**          | Maak criteria om op te geven hoe nieuwe transacties moeten worden gemarkeerd op de pagina **Werkblad voor bankafstemming** wanneer de afstemmingsregel wordt uitgevoerd.                                                                                                                                                                 | **Stap 1: afschriftregels zoeken**: voeg selectievelden toe om op te geven welke bankafschriftregels moeten worden geselecteerd op de pagina ** Bankafstemmingswerkblad**. ** Stap 2: Zoeken Dynamics 365 voor bewerkingen banktransacties **: U kunt selectiecriteria toevoegen om te zoeken naar bankdocumentregels. Als er geen bankdocument wordt gevonden, wordt een afschriftregel als een nieuwe transactie gemarkeerd.                                                                                                                                                                                                                                             |

 





