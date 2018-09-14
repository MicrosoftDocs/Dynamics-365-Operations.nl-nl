--- 
title: " Winkelconfiguraties voor detailhandeloverzichten"
description: Deze procedure doorloopt configuraties voor de detailhandelwinkel die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cac676c9c6ebb6769fe7e30ac08a2c8334befc24
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="store-configurations-for-retail-statements"></a> Winkelconfiguraties voor detailhandeloverzichten

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure doorloopt configuraties voor de detailhandelwinkel die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt. Financiële dimensies voor detailhandelwinkels worden in een andere procedure behandeld. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * De instellingen in de sectie Overzicht/afsluiting zijn van invloed op het maken, valideren en boeken van overzichten voor de winkel.  Open de sectie Overzicht/afsluiting.  
    * Selecteer de gewenste methode om de overzichtsregels op te groeperen.  
    * Selecteer 'Ja' als er slechts één overzicht per dag moet worden gemaakt wanneer overzichten worden gemaakt vanuit de batchtaak voor het maken van overzichten.  
    * Het veld Berekening kascontrole definieert of kascontroles moeten worden opgeteld of dat de laatste moet worden gebruikt.  
    * Selecteer de grootboekrekening om afrondingsverschillen naar te boeken.  
    * In het veld Maximaal afrondingsbedrag kunt u het maximaal toegestane afrondingsverschil invoeren.  
    * In het veld Boeking kunt u het maximale boekingsverschil invoeren dat toegestaan is voor een overzicht.  
    * In het veld Ploeg kunt u het maximaal toegestane totale verschil binnen een ploeg in een overzicht invoeren.  
    * In het veld Transactie kunt u het maximaal toegestane totale verschil op een overzichtsregel invoeren.  
    * In het veld Afsluitingsmethode kunt u definiëren of transacties die in een overzicht worden opgenomen, deel moeten uitmaken van een gesloten ploeg of dat het transacties kunnen zijn binnen het gedefinieerde datum/tijd-bereik.  
    * In het veld Einde van werkdag kunt u een tijd invoeren als transacties die na middernacht plaatsvinden, op de vorige dag moeten worden geboekt.  
    * Selecteer 'Ja' als transacties die na middernacht plaatsvinden, als onderdeel van de vorige dag moeten worden geboekt.  
    * Selecteer 'Ja' om overzichten te laten maken voor elke gedefinieerde overzichtsmethode. Dat kan nuttig zijn als de prestaties van de boeking moeten worden verbeterd voor winkels met grote transactievolumes, aangezien er veel kleinere overzichten worden gemaakt die parallel kunnen worden verwerkt.  
    * In het veld Standaardklant kunt u de klantrekening selecteren om te gebruiken voor verkoop aan inloopklanten.  


