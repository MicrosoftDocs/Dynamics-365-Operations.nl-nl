---
title: Een nieuwe magazijnindeling maken
description: In dit onderwerp wordt beschreven hoe u informatie instelt voor locaties in een magazijn.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09666e95cc90913f1bf8555b9ff2c48aa55369ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214016"
---
# <a name="create-a-new-warehouse-layout"></a>Een nieuwe magazijnindeling maken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u informatie instelt voor locaties in een magazijn. Dit geldt alleen voor magazijnen die zijn gemaakt met "basale magazijnen" in de module Voorraadbeheer, niet voor magazijnen die in de module Magazijnbeheer zijn gemaakt. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.


## <a name="set-the-default-location-capacity"></a>Stel de standaardlocatiecapaciteit in
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Parameters voor voorraad- en magazijnbeheer**.
2. Selecteer het tabblad **Locatietypen**.
3. Voer een getal in het veld **Standaardbreedte** in.
4. Voer een getal in het veld **Standaarddiepte** in.
5. Voer een getal in het veld **Standaardhoogte** in.
6. Selecteer **Opslaan**.
7. Sluit de pagina.

## <a name="define-the-location-name-format"></a>De locatienaamindeling definiëren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Opsplitsing van voorraad > Magazijnen**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Magazijn**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer in het veld **Vestiging** de gewenste record in de zoeklijst.
6. Schakel de uitbreiding van de sectie **Locatienamen** om. De opties in deze sectie definiëren de standaardindeling voor locatienamen. In ons voorbeeld nemen we het gangnummer, het reknummer en het planknummer op.  
7. Stel de optie **Gang opnemen** in op **Ja**.
8. Stel de optie **Rek opnemen** in op **Ja**. 
9. Typ in het veld **Indeling** voor het rek een waarde.
10. Stel de optie **Plank opnemen** in op **Ja**.
11. Typ in het veld **Indeling** voor de plank een waarde.

## <a name="define-warehouse-locations"></a>Magazijnlocaties definiëren
1. Selecteer **Magazijn** in het actievenster.
2. Selecteer **Locatiewizard**.
3. Selecteer **Volgende**.
4. De optie **Outbound docks** deselecteren
5. De optie **Bulklocaties** deselecteren
6. Selecteer **Volgende** totdat u de optie **Voltooien** hebt geselecteerd.
7. Sluit de pagina.
8. Vernieuw de pagina.

