--- 
title: Groepen boekingen in grootboek instellen voor btw
description: De btw wordt berekend en naar hoofdrekeningen geboekt die in de grootboekboekingsgroepen worden opgegeven.
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0682afed4664e1491ed46e4e40f467015701711
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Groepen boekingen in grootboek instellen voor btw

[!include[task guide banner](../../includes/task-guide-banner.md)]

De btw wordt berekend en naar hoofdrekeningen geboekt die in de grootboekboekingsgroepen worden opgegeven. Grootboekboekingsgroepen worden gekoppeld aan elke btw-code. U kunt afzonderlijke grootboekboekingsgroepen instellen voor elke btw-code, één grootboekboekingsgroep gebruiken voor alle btw-codes of meerdere grootboekboekingsgroepen aan de btw-codes toewijzen. Bij deze registratie wordt het demobedrijf DEMF gebruikt. 

1. Ga naar Belasting > Instellingen > Btw > Grootboekboekingsgroepen.
2. Klik op Nieuw.
3. Typ in het veld Groep boekingen in grootboek een waarde.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer in het veld Te betalen btw de hoofdrekening voor uitgaande btw, die aan de belastingdienst moet worden betaald.
    * De btw wordt geïnd namens de belastingdienst wanneer u goederen en diensten verkoopt.  
6. Selecteer in het veld Te ontvangen btw de hoofdrekening voor inkomende btw, die van de belastingdienst moet worden ontvangen.
    * Leveranciers innen btw namens de belastingdienst wanneer u goederen en diensten koopt. Dit veld is niet beschikbaar als de optie Belastingregels btw toepassen is geselecteerd in de pagina Grootboekparameters. In plaats hiervan wordt de btw die is betaald aan leveranciers, op dezelfde rekening gedebiteerd als de inkopen.   
7. Selecteer in het veld Gebruiksbelastinguitgave de hoofdrekening voor het boeken van aftrekbare gebruiksbelasting die niet wordt gevorderd of aan de belastingdienst via leveranciers als onderdeel van EU GST/HST-terugboeking wordt gerapporteerd.
    * De optie Gebruiksbelasting moet voor de btw-code in de btw-groep zijn geselecteerd die voor de transactie wordt gebruikt.  Dit veld is niet beschikbaar als de optie Belastingregels btw toepassen is geselecteerd in de pagina Grootboekparameters.   
8. Selecteer in het veld Te betalen gebruiksbelasting de hoofdrekening voor het boeken van inkomende gebruiksbelasting, die aan de belastingdienst moet worden betaald.
    * De optie Gebruiksbelasting moet in de btw-code in de btw-groep zijn geselecteerd om gebruiksbelasting te boeken. Als de optie Belastingregels btw toepassen is geselecteerd in Grootboekparameters, wordt tegengeboekt op de kostenrekening van de transactie.   
9. Selecteer in het veld Vereffeningsrekening de hoofdrekening waarnaar het netto saldo van de grootboekrekeningen die in de velden Te betalen gebruiksbelasting en Te ontvangen btw worden opgegeven, wordt geboekt.
    * Het saldo wordt gemaakt wanneer de taak Btw vereffenen en boeken wordt uitgevoerd.  Als de belastingdienst voor de vereffeningsperiode aan een leveranciersrekening is gekoppeld, wordt het saldo in plaats daarvan geboekt naar de leverancierrekening.   
10. Selecteer in het veld Contantkorting van leverancier de hoofdrekening om contantkorting voor btw-codes die zijn gekoppeld aan deze grootboekboekingsgroep te boeken.
    * Dit is optioneel en als er geen rekening is ingevoerd, wordt de hoofdrekening op Contantkortingscodes gebruikt. Het kan handig zijn om verschillende rekeningen per grootboekboekingsgroep te gebruiken als de optie Btw op contantkorting omkeren op Btw-groepen wordt gebruikt.  
11. Selecteer in het veld Contantkorting van klant de hoofdrekening om contantkorting voor btw-codes die zijn gekoppeld aan deze grootboekboekingsgroep te boeken.
    * Dit is optioneel en als er geen rekening is ingevoerd, wordt de hoofdrekening op Contantkortingscodes gebruikt. Het kan handig zijn om verschillende rekeningen per grootboekboekingsgroep te gebruiken als de optie Btw op contantkorting omkeren op Btw-groepen wordt gebruikt.  
12. Klik op Opslaan.


