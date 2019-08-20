---
title: Een kanbanberekeningsbeleid aan een kanbanregel toevoegen
description: Deze procedure is gericht op het maken van een beleid voor berekening van de kanbanhoeveelheid en het toevoegen hiervan aan een kanbanregel om de grootte en hoeveelheden van de kanban te optimaliseren.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 401b01a6128babd6ed345342a65705a0262540e8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837945"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Een kanbanberekeningsbeleid aan een kanbanregel toevoegen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht op het maken van een beleid voor berekening van de kanbanhoeveelheid en het toevoegen hiervan aan een kanbanregel om de grootte en hoeveelheden van de kanban te optimaliseren. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de waardestroombeheerder. Deze procedure is een vereiste voor het maken van de procedure Suggesties voor kanbanhoeveelheid berekenen. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Een beleid voor het berekenen van de kanbanhoeveelheid maken
1. Ga naar Productiebeheer > Periodieke taken > Berekening kanbanhoeveelheid > Beleid voor berekenen kanbanhoeveelheid.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
    * Typ bijvoorbeeld Speaker2016.  
4. Klik in het veld Hoofdplan op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer StaticPlan om de vraag te berekenen.  
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik op Opslaan.
8. Voer in het veld Minimale kanbanhoeveelheid "1" in.
    * Dit is het aanvullende aantal kanbans dat in de berekening van kanbanhoeveelheid is opgenomen.  
9. Stel Veiligheidsfactor in op "1".
    * Dit is de factor die wordt gebruikt om aanvullende hoeveelheid van beveiligingsvoorraad te berekenen.  
10. Voer "30" in het veld Dagen voor in.
    * Dit is het aantal dagen vóór de kanbanberekeningsdatum dat vraag in de berekening is opgenomen in de vraagberekening.  
11. Voer "30" in het veld Dagen achter in.
    * Dit is het aantal dagen vooruit vanaf de kanbanberekeningsdatum dat vraag in de berekening is opgenomen in de vraagberekening.  De formule wordt gebruikt voor de berekening wordt weergegeven met de werkelijke waarden. Bijvoorbeeld: Kanbanhoeveelheid = ((Gemiddelde dagelijkse vraag x doorlooptijd x 2,00)/Producthoeveelheid per materiaalverwerkingseenheid) + 1  
12. Sluit de pagina.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Het beleid voor het toevoegen van de berekening van de kanbanhoeveelheid toevoegen aan de kanbanregel
1. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer kanbanregel 000020 voor deze procedure.  
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Schakel de uitbreiding van de sectie voor het beleid voor berekening van de kanbanhoeveelheid om.
5. Klik op Toevoegen.
    * Voeg het berekeningsbeleid voor de kanbanhoeveelheid toe die u zojuist in de vorige deeltaak hebt gemaakt.  
6. Markeer in de lijst de geselecteerde rij.
7. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer het beleid Speaker2016 dat u zojuist in de vorige deeltaak hebt gemaakt.  

