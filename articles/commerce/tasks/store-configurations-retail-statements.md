---
title: Winkelconfiguraties voor detailhandeloverzichten
description: Deze procedure doorloopt winkelconfiguraties die van invloed zijn op hoe Commerce-overzichten worden gemaakt en geboekt.
author: jashanno
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da862af25df241ad42b7e1ade3fdca19f6280278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804108"
---
# <a name="store-configurations-for-retail-statements"></a>Winkelconfiguraties voor detailhandeloverzichten

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt winkelconfiguraties die van invloed zijn op hoe Commerce-overzichten worden gemaakt en geboekt. Financiële dimensies voor winkels worden in een andere procedure behandeld. Deze procedure gebruikt het demobedrijf USRT.

1. Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Kanalen > Winkels > Alle detailhandelwinkels**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op **Bewerken**.
5. De instellingen op het sneltabblad **Overzicht/afsluiting** zijn van invloed op het maken, valideren en boeken van overzichten voor de winkel. Vouw het sneltabblad **Overzicht/afsluiting** uit.  
6. Selecteer de gewenste methode waarmee u de overzichtsregels wilt groeperen in het veld **Overzichtsmethode**.  
7. Selecteer Ja bij **Eén overzicht per dag** als er slechts één overzicht per dag moet worden gemaakt wanneer overzichten worden gemaakt vanuit de batchtaak voor het maken van overzichten.  
8. Het veld **Berekening kascontrole** definieert of kascontroles moeten worden opgeteld of dat de laatste moet worden gebruikt.  
9. Selecteer in het veld **Afronding** de grootboekrekening om afrondingsverschillen naar te boeken.  
10. In het veld **Maximaal afrondingsbedrag** kunt u het maximaal toegestane afrondingsverschil invoeren.
11. In het veld **Boeking** kunt u het maximale boekingsverschil invoeren dat toegestaan is voor een overzicht.
12. In het veld **Ploeg** kunt u het maximaal toegestane totale verschil binnen een ploeg in een overzicht invoeren.  
13. In het veld **Transactie** kunt u het maximaal toegestane totale verschil op een overzichtsregel invoeren.  
14. In het veld **Afsluitingsmethode** kunt u definiëren of transacties die in een overzicht worden opgenomen, deel moeten uitmaken van een gesloten ploeg of dat het transacties kunnen zijn binnen het gedefinieerde datum/tijd-bereik.  
15. In het veld **Einde van werkdag** voert u een tijd in als transacties die na middernacht plaatsvinden op de vorige dag moeten worden geboekt.  
16. Selecteer Ja bij **Als werkdag boeken** als transacties die na middernacht plaatsvinden, als onderdeel van de vorige dag moeten worden geboekt.  
17. Selecteer Ja bij **Splitsing per overzichtsmethode** om overzichten te laten maken voor elke gedefinieerde overzichtsmethode. Deze actie kan nuttig zijn als de prestaties van de boeking moeten worden verbeterd voor winkels met grote transactievolumes, aangezien er veel kleinere overzichten worden gemaakt die parallel kunnen worden verwerkt.  
18. In het veld **Standaardklant** op het sneltabblad **Algemeen** kunt u de klantrekening selecteren die u wilt gebruiken voor verkoop aan inloopklanten.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]