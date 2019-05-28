---
title: Groepen boekingen in grootboek instellen voor btw
description: De btw wordt berekend en naar hoofdrekeningen geboekt die in de grootboekboekingsgroepen worden opgegeven.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 15421da6f325dfee22a303e9fe83a0e72895fa08
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562806"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Groepen boekingen in grootboek instellen voor btw

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

