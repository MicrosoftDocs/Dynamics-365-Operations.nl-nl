--- 
title: Een vrije-tekstfactuur invoeren
description: In dit artikel wordt beschreven hoe u een vrije-tekstfactuur maakt.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: nl-nl
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Een vrije-tekstfactuur invoeren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een vrije-tekstfactuur maakt. Gebruik voor deze procedure het demobedrijf USMF.

## <a name="create-a-free-text-invoice"></a>Een vrije-tekstfactuur invoeren

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
    * De btw-groep van het artikel wordt ingevuld vanuit de hoofdrekening. Als de hoofdrekening geen btw-groep voor een artikel heeft, wordt de btw-groep voor het artikel in de grootboekparameters voor btw gebruikt.    
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

## <a name="copy-lines"></a>Regels kopiëren
Als u regels in de vrije-tekstfactuur wilt kopiëren, selecteert u een of meer regels en klikt u op Geselecteerde regels kopiëren. U kunt opgeven hoeveel kopieën u wilt maken en u kunt ook notities en bijlagen kopiëren. U kunt de verdelingen kopiëren of opnieuw laten maken wanneer u boekt. Wanneer u de regels hebt gekopieerd, kunt u de gegevens vervolgens zo nodig bewerken. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Een vrije-tekstfactuur maken op basis van een sjabloon
U kunt een vrije-tekstfactuur maken op basis van een sjabloon. Wanneer u Nieuw van sjabloon op het tabblad Factuur selecteert, kunt u een sjabloonnaam en de klantrekening voor de nieuwe vrije-tekstfactuur selecteren. U kunt ook kiezen voor de standaardwaarden, zoals de betalingsvoorwaarden en betalingsmethode van de klant, of de waarden gebruiken die zijn opgeslagen met de sjabloon. Er wordt een nieuwe vrije-tekstfactuur gemaakt en u kunt de waarden in deze factuur bewerken. 


