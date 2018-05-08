--- 
title: Procesactiviteiten maken voor lean manufacturing
description: Maak een procesactiviteit voor lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dd77c20b622fd8a14e1cdf77883043699f9a6317
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-process-activities-for-lean-manufacturing"></a>Procesactiviteiten maken voor lean manufacturing

[!include [task guide banner](../../includes/task-guide-banner.md)]

Maak een procesactiviteit voor lean manufacturing. 

Vereisten: 

1. Een productiestroom en versie die niet actief zijn, moeten worden gemaakt.

2. Een werkcel moet worden gemaakt.


## <a name="find-the-production-flow-version"></a>De productiestroomversie vinden
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="create-a-new-activity"></a>Een nieuwe activiteit maken
1. Klik op Activiteiten.
    * Zorg ervoor dat de geselecteerde productiestroom een versie in concept heeft en selecteer deze versie.  
2. Klik op Nieuwe planactiviteit maken.
3. Klik op Volgende.
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Naam.
    * De naam moet uniek zijn voor een bepaalde productiestroom voor alle versies.  
6. Voer in het veld Verwerkingshoeveelheid een getal in.
    * Ongeacht de taakhoeveelheid die wordt verwerkt, dit is de minimumhoeveelheid per taak om de loonkosten te berekenen. Als de taakhoeveelheden van deze hoeveelheid afwijken, wordt de arbeidskostenafwijking gemaakt.  
7. Klik op Volgende.

## <a name="select-the-work-cell"></a>De werkcel selecteren
1. Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.
2. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="define-the-inventory-updates"></a>De updates van de voorraad definiëren
1. Schakel het selectievakje Voorhanden ontvangst bijwerken in of uit.
    * Als Voorhanden voorraad bijwerken = Nee, kunt u de activiteit definiëren om een halffabricaatproduct (de activiteit bereikt niet het stuklijstniveau) te ontvangen.    U kunt ook kiezen om halffabricaten te verbruiken.  

## <a name="define-the-picking-activities"></a>De orderverzamelactiviteiten definiëren
1. Klik op Volgende.
2. Markeer in de lijst de geselecteerde rij.
    * Een standaard orderverzamelactiviteit wordt gemaakt voor de invoerlocatie van de geselecteerde werkcel.  
3. Klik op Toevoegen.
    * U kunt extra orderverzamelactiviteiten maken voor specifieke producten die niet worden gefaseerd aan de invoeractiviteit van de werkcel.  
4. Zoek en selecteer de gewenste record in de lijst.
5. Typ een waarde in het veld Artikelnummer.
6. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Met deze definitie worden alle materialen die in de activiteit worden verbruikt verzameld uit het standaardinvoermagazijn en -locatie, behalve het artikel dat in de tweede orderverzamelactiviteit wordt gedefinieerd. Dit artikel wordt uit een ander(e) magazijn en locatie verzameld.  
7. Zoek en selecteer de gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Schakel het selectievakje Uitval registreren in of uit.
10. Klik op Volgende.

## <a name="define-the-activity-times"></a>De activiteitstijden dfiniëren
1. Zoek en selecteer de gewenste record in de lijst.
    * De definitie van Runtime is vereist. De Runtime wordt gebruikt om kosten en de doorvoertijden van de kanbantaken te berekenen. Runtimes worden niet gebruikt om capaciteitsbelasting en verbruik te berekenen. Deze wordt berekend door cyclusduur, afgeleid uit de taak van de productiestroomversie.  
2. Voer in het veld Tijd een nummer in.
3. Typ een waarde in het veld Eenheid.
4. Selecteer de tijdseenheid.
5. Voer in het veld Per hoeveelheid een getal in.
6. Zoek en selecteer de gewenste record in de lijst.
    * Wachttijden zijn optioneel.  
7. Voer in het veld Tijd een nummer in.
8. Typ een waarde in het veld Eenheid.
9. Selecteer de tijdseenheid.
10. Voer in het veld Per hoeveelheid een getal in.
11. Klik op Volgende.
12. Klik op Voltooien.
13. Sluit de pagina.


