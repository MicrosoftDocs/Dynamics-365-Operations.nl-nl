--- 
title: Een vrije-tekstfactuur invoeren
description: Deze taakbegeleiding toont het maken van een vrije-tekstfactuur.
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a9f9a780868926009f30cee6aa634c53ca870b3f
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-free-text-invoice"></a>Een vrije-tekstfactuur invoeren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding toont het maken van een vrije-tekstfactuur. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Klanten > Facturen > Alle vrije-tekstfacturen.
2. Klik op Nieuw.
3. Selecteer in het veld Klantrekening een waarde.
    * De factuurrekening wordt standaard ingesteld op dezelfde rekening als wordt gebruikt voor de klantrekening.   
    * De boekhoudstatus begint met Onderhanden als de factuur niet is geboekt.   
    * Het factuurnummer wordt toegewezen wanneer de factuur wordt geboekt.  
    * Als u SEPA-mandaten gebruikt, wordt het mandaat voor automatische afschrijving automatisch ingevuld met een mandaat wanneer u de klantrekening selecteert.  
4. Typ een waarde in het veld Omschrijving.
5. Geef in het veld Hoofdrekening een rekeningnummer zonder dimensies op.
    * U kunt ook één of meerdere tekens voor de hoofdrekening invoeren en de zoekopdracht gebruiken om uw rekening te zoeken. Verderop in deze handleiding voert u dimensies in.  
6. Vouw het sneltabblad Regeldetails uit zodat u dimensies kunt toevoegen aan uw hoofdrekening.
7. Klik op het tabblad Financiële dimensieregel.
    * De dimensies gelden uitsluitend voor de geselecteerde regel.    
    * De btw-groep wordt ingevuld van de klant. Als de klant geen btw-groep heeft, wordt de btw-groep van de hoofdrekening gebruikt.  
    * De btw-groep van het artikel wordt ingevuld vanuit de hoofdrekening. Als de hoofdrekening geen btw-groep voor het artikel heeft, wordt de btw-groep voor het artikel in de grootboekparameters voor btw gebruikt.    
8. Voer in het veld Hoeveelheid een getal in.
    * De hoeveelheid is optioneel.  
9. Voer in het veld Eenheidsprijs een getal in.
    * De eenheidsprijs is optioneel.  
    * Het bedrag wordt berekend als de hoeveelheid keer de eenheidsprijs. U kunt die berekening echter negeren en een bedrag invoeren.  
10. Klik op Btw om de berekende btw voor uw factuur te bekijken.
    * Bekijk de btw-bedragen op deze pagina of u kunt de bedragen op het tabblad Correctie negeren.  
11. Klik op OK.
12. Klik op Toeslagen om een toeslag aan de factuur toe te voegen. 
13. Typ een waarde in het veld Toeslagcode.
14. Voer een nummer in het veld Waarde van toeslagen in.
15. Sluit de pagina.
16. Klik op Totalen om de overzichtsfactuurdetails en totalen weer te geven.
17. Klik op Sluiten.
18. Klik op Boeken om de factuur te boeken. U kunt annuleren voordat u boekt.
    * Als u de timing voor het afdrukken van de facturen wilt wijzigen: Selecteer Huidig om elke factuur af te drukken wanneer deze wordt bijgewerkt of Na om alle facturen af te drukken die zijn bijgewerkt.  
    * Als u wilt wijzigen hoe de kredietlimiet van de klant wordt gecontroleerd voordat er wordt geboekt, wijzigt u het type kredietlimiet.  
    * Als u de factuur wilt afdrukken, selecteert u Ja.  
    * Als u de factuur wilt boeken, selecteert u Ja. U kunt de factuur afdrukken zonder te boeken.  
19. Klik op OK.


