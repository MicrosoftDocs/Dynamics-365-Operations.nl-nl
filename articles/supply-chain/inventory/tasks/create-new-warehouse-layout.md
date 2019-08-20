---
title: Een nieuwe magazijnindeling maken
description: Deze procedure laat zien hoe u de informatie over locaties in een magazijn instelt.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a52c5d68816a81a94db019387b9ea3ec3efc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845517"
---
# <a name="create-a-new-warehouse-layout"></a>Een nieuwe magazijnindeling maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u de informatie over locaties in een magazijn instelt. Dit geldt alleen voor magazijnen die zijn gemaakt met "basale magazijnen" in de module Voorraadbeheer, niet voor magazijnen die in de module Magazijnbeheer zijn gemaakt. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.


## <a name="set-the-default-location-capacity"></a>Stel de standaardlocatiecapaciteit in
1. Ga naar Voorraadbeheer > Instellingen > Parameters voor voorraad- en magazijnbeheer.
2. Klik op het tabblad Locaties.
3. Voer een getal in het veld Standaardbreedte in.
4. Voer een getal in het veld Standaarddiepte in.
5. Voer een getal in het veld Standaardhoogte in.
6. Klik op Opslaan.
7. Sluit de pagina.

## <a name="define-the-location-name-format"></a>De locatienaamindeling definiëren
1. Ga naar Voorraadbeheer > Instellen > Opsplitsing van voorraad > Magazijnen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Magazijn.
4. Typ een waarde in het veld Naam.
5. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer de gewenste record in de lijst.
7. Schakel de uitbreiding van de sectie Locatienamen om.
    * De opties in deze sectie definiëren de standaardindeling voor locatienamen. In ons voorbeeld nemen we het gangnummer, het reknummer en het planknummer op.  
8. Stel de optie Gang opnemen in op Ja.
9. Stel de optie Rek opnemen in op Ja. 
10. Typ in het veld Indeling voor het rek een waarde.
    * Bijvoorbeeld: -##  
11. Stel de optie Plank opnemen in op Ja.
12. Typ in het veld Indeling voor de plank een waarde.
    * Bijvoorbeeld: -##  

## <a name="define-warehouse-locations"></a>Magazijnlocaties definiëren
1. Klik in het actievenster op Magazijn.
2. Klik op Locatiewizard.
3. Klik op Volgende.
4. De optie Outbound docks deselecteren
5. De optie Bulklocaties deselecteren
6. Klik op Volgende.
7. Klik op Volgende.
8. Klik op Volgende.
9. Klik op Volgende.
10. Klik op Volgende.
11. Klik op Volgende.
12. Klik op Volgende.
    * Merk op dat de fysieke dimensies die op deze pagina worden weergegeven de dimensies zijn die u instelt aan het begin van deze procedure.  
13. Klik op Volgende.
14. Klik op Voltooien.
15. Sluit de pagina.
16. Vernieuw de pagina.

