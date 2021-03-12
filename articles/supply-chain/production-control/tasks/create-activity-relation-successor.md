---
title: 'Activiteitsrelatie maken: opvolgende activiteit'
description: De stroom van activiteiten in lean productiestroom wordt gedocumenteerd door middel van activiteitsrelaties.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f23dc0cb4b2ea7a4a298368a56869db90dd044d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981276"
---
# <a name="create-activity-relation---successor"></a>Activiteitsrelatie maken: opvolgende activiteit

[!include [banner](../../includes/banner.md)]

De stroom van activiteiten in lean productiestroom wordt gedocumenteerd door middel van activiteitsrelaties. Deze registratie toont aan hoe een activiteitsrelatie wordt gemaakt.

Vereisten:

- Een productiestroom en versie in conceptmodus. 

- Twee activiteiten die elkaar opvolgen in de productiestroom worden gemaakt maar zijn niet gerelateerd.


## <a name="find-the-production-flow-version"></a>De productiestroomversie vinden 
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Markeer in de lijst de geselecteerde rij.
5. Selecteer een conceptversie in de lijst.
    * Activiteitsrelaties kunnen worden toegevoegd aan zowel conceptversies of actieve versies van een productiestroom.  

## <a name="open-the-activity-overview"></a>Het overzicht van activiteiten openen
1. Klik op Activiteiten.
    * Het formulier geeft alle activiteiten van de productiestroom weer die zijn toegewezen aan de Versie van de productiestromen waarin u werkt.  

## <a name="add-a-successor"></a>Een opvolgende activiteit toevoegen
1. Klik op Opvolgende activiteit.
2. Klik in het veld Activiteit op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer het gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Schakel het selectievakje Beperking in.
6. Voer in het veld Waarde van beperking een waarde in.
    * De beperkingtijd is de tijd die moet worden gepland tussen het geplande einde van de voorafgaande activiteit (vervaldatum en tijd) en het geplande begin van de opvolgende activiteit.  
7. Typ een waarde in het veld Eenheden.
8. Voer in het veld Cyclusduurverhouding een nummer in.
    * Als beide activiteiten met dezelfde snelheid worden uitgevoerd, moet de cyclusduurverhouding 1 zijn. Als de voorgaande taak twee keer zo snel wordt uitgevoerd als de opvolgende taak, moet de verhouding 2 zijn.   De cyclusduurverhouding wordt gebruikt om de afzonderlijke cyclustijden te berekenen voor activiteiten van de productiestroom.  
9. Klik op OK.
10. Sluit de pagina.
11. Klik op het tabblad Rasterdeelvenster.
12. Sluit de pagina.
13. Vernieuw de pagina.

