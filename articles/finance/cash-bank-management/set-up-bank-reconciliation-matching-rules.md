---
title: Afstemmingsregels voor bankafstemming instellen
description: In dit artikel wordt beschreven hoe afstemmingsregels en sets afstemmingsregels kunnen worden ingesteld om het bankafstemmingsproces te vereenvoudigen. Afstemmingsregels zijn een reeks criteria die worden gebruikt om regels van bankafschriften en bankdocumentregels te filteren tijdens het afstemmingsproces.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803932"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Afstemmingsregels voor bankafstemming instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe afstemmingsregels en sets afstemmingsregels kunnen worden ingesteld om het bankafstemmingsproces te vereenvoudigen. Afstemmingsregels zijn een reeks criteria die worden gebruikt om regels van bankafschriften en bankdocumentregels te filteren tijdens het afstemmingsproces.

U kunt afstemmingsregels en sets afstemmingsregels instellen om het bankafstemmingsproces te vereenvoudigen. Een afstemmingsregels is een reeks criteria die worden gebruikt om regels van bankafschriften en Dynamics 365 Finance-banktransactieregels te filteren tijdens het afstemmingsproces. Gebruik de pagina **Afstemmingsregels** om de afstemmingsregels in te stellen. U kunt meerdere afstemmingsregels instellen en vervolgens een afstemmingsregelset maken op de pagina **Afstemmingsregelsets**. 

> [!NOTE] 
> Bankafstemmingsregels worden gebruikt als u een elektronisch bankafschrift afstemt met behulp van geavanceerde bankafstemming. 

Op de pagina **Afstemmingsregels** kunt u selecteren welke acties en selectiecriteria worden gebruikt wanneer de afstemmingsregel wordt uitgevoerd. Selecteer in de veldgroep **Acties** welke actie wordt uitgevoerd wanneer de afstemmingsregel wordt uitgevoerd tijdens het afstemmingsproces.  

De afstemmingsregels zoeken standaard naar het eerste bankdocument dat voldoet aan de criteria van de afstemmingsregels. Als er meerdere bankdocumenten zijn die aan de regelcriteria voldoen, kan de parameter voor het verplicht stellen van handmatige afstemming worden ingeschakeld. Daarvoor gaat u naar **Contanten en bankbeheer > Instellen > Parameters voor Contanten en bankbeheer > Bankafstemming > Handmatige afstemming vereisen wanneer met geavanceerde afstemmingsregels voor bankafstemming meerdere documenten worden gevonden met dat bedrag**.

> [!NOTE] 
> De geselecteerde optie bepaalt welke velden worden weergegeven.

| Actie | Beschrijving   | Beschikbare selectiecriteria wanneer de actie wordt geselecteerd     |
|--------|---------------|----------------------------------------------------------|
| **Afstemmen met bankdocument**       | Maak criteria om op te geven hoe de bankdocumenten en bankafschriftregels worden afgestemd wanneer de afstemmingsregel wordt uitgevoerd vanuit de pagina **Werkblad voor bankafstemming**. De transactieregels worden geselecteerd in overeenstemming met de aanvullende criteria die zijn ingesteld op de sneltabbladen. | <ul><li>**Stap 1: De afstemmingsregel definiëren** – selecteer criteria om op te geven welke bankafschriften met Finance-banktransacties moeten worden afgestemd.</li><li> **Stap 2 (optioneel): selecteer de overzichtregels ten opzichte waarvan afstemmingsregels moeten worden uitgevoerd:** Pas een filter toe op de afschriftregel ten opzichte waarvan de regels moeten worden uitgevoerd.</li></ul>                                       |
| **Terugboekingsregels op een afschrift wissen** | Maak criteria om op te geven hoe terugboekingsregels moeten worden verwijderd van de pagina **Werkblad voor bankafstemming** wanneer de afstemmingsregel wordt uitgevoerd. Deze optie wordt gebruikt wanneer de bank een fout maakt en er twee bankafschriftregels moeten worden weergegeven in het geïmporteerde bankafschrift en de regels moeten worden afgestemd. |<ul><li> **Stap 1**: **terugboekingsregels op afschrift zoeken**: voeg selectiecriteria toe om terugboekingsregels van het bankafschrift te selecteren. Als u bijvoorbeeld alleen cheques wilt selecteren, selecteert u de **Banktransactiecode** in het veld **Veld**, selecteert u het plusteken (+) in het veld **Operator** en voert u vervolgens **Cheques** in het veld **Waarde** in. </li><li>**Stap 2: oorspronkelijke afschriftregels zoeken**: u kunt selectiecriteria toevoegen om bankdocumentregels af te stemmen op bankafschriftregels. </li><li>**Stap 3: Finance-banktransacties zoeken** – u kunt selectiecriteria toevoegen om Finance-banktransacties af te stemmen op bankafschriftregels.</li></ul>  |
| **Nieuwe transacties markeren**          | Maak criteria om op te geven hoe nieuwe transacties moeten worden gemarkeerd op de pagina **Werkblad voor bankafstemming** wanneer de afstemmingsregel wordt uitgevoerd.                                                                                                                                                                 | <ul><li>**Stap 1: afschriftregels zoeken**: voeg selectievelden toe om op te geven welke bankafschriftregels moeten worden geselecteerd op de pagina **Bankafstemmingswerkblad**.</li><li> **Stap 2: Apps voor financiën en bedrijfsactiviteiten zoeken** – u kunt selectiecriteria toevoegen om bankdocumentregels te zoeken. Als er geen bankdocument wordt gevonden, wordt een afschriftregel als een nieuwe transactie gemarkeerd. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

