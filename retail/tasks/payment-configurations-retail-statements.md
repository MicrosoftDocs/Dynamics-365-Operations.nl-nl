--- 
title: " Betalingsconfiguraties voor detailhandeloverzichten"
description: Deze procedure demonstreert configuraties voor betalingsmethoden voor detailhandelwinkels die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ccb17342ebbec67a9d6223354a4daa1e99b05262
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="payment-configurations-for-retail-statements"></a> Betalingsconfiguraties voor detailhandeloverzichten

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure demonstreert configuraties voor betalingsmethoden voor detailhandelwinkels die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.

Deze registratie gebruikt het demobedrijf USRT.

1. Ga naar Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het actievenster op Instellen.
5. Klik op Betalingsmethoden.
6. Vouw de sectie Boeking uit of samen.
7. Klik op Bewerken.
    * Selecteer of de ontvangen hoeveelheden voor deze betalingsmethode moeten worden geboekt naar een grootboekrekening of een bankrekening.  
    * Selecteer de rekening waarnaar ontvangen bedragen voor deze betalingsmethode moeten worden geboekt.  
    * Selecteer een rekening om mogelijke verschillen naar te boeken tussen het totale ontvangen transactiebedrag en het getelde bedrag voor deze betalingsmethode.  
    * In dit veld kunt u een bedrag invoeren om te bepalen wanneer het verschilbedrag moet worden geboekt naar een andere verschilrekening. U kunt dit gebruiken om grote verschillen bij te houden.  
    * Selecteer een rekening om mogelijke verschillen naar te boeken tussen het totale ontvangen transactiebedrag en het getelde bedrag, wanneer het de waarde overschrijdt die is gedefinieerd in het veld 'Maximumbedrag verschil'.  
    * Selecteer 'Ja' om bankstortingsbedragen naar een aparte rekening te boeken.  
    * In dit veld kunt u selecteren of bankstortingsbedragen moeten worden geboekt naar een grootboekrekening of een bankrekening.  
    * Selecteer de rekening om bankstortingsbedragen naar te boeken.  
    * Selecteer het type banktransactie dat moet worden gebruikt om bankstortingsbedragen te boeken naar de bankrekening.  
    * Selecteer 'Ja' om kluisstortingsbedragen naar een aparte rekening te boeken.  
    * Selecteer of kluisstortingsbedragen moeten worden geboekt naar de grootboekrekening of de bankrekening.  
    * Selecteer de rekening om kluisstortingsbedragen naar te boeken.  
8. Klik op Opslaan.


