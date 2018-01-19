--- 
title: " Winkelconfiguraties voor detailhandeloverzichten"
description: Deze procedure doorloopt configuraties voor de detailhandelwinkel die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 45aa0caf6fcef4cc49952557a251dd78f816125e
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

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


