---
title: Werkbelastingcapaciteit plannen
description: In dit onderwerp wordt uitgelegd hoe u de werkbelastingcapaciteit voor werknemers in een magazijn of voor een geheel magazijn kunt instellen en plannen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69b9c5590e6f9311696bbbed2e63a6eeba2a90bf
ms.openlocfilehash: 1b93cfaf098b4cff3e72ee9bb599eadfdac2a9b9
ms.contentlocale: nl-nl
ms.lasthandoff: 05/03/2018

---

# <a name="schedule-workload-capacity"></a>Werkbelastingcapaciteit plannen

[!include[banner](../includes/banner.md)]

U kunt de werkbelastingcapaciteit voor magazijnen plannen, en tevens kunt u de huidige en toekomstige werkbelasting voor de werknemers in individuele magazijnen voorstellen. U kunt de werkbelasting voor het hele magazijn opstellen of u kunt de werkbelasting apart voor inkomende en uitgaande werkbelasting opstellen.

Om de werkbelastingsuitvoer voor geselecteerde magazijnen te voorspellen, moeten de hoofdplanningsgegevens beschikbaar zijn voor die magazijnen. Zie voor meer informatie [Hoofdplannen](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Planning en weergave werklast voor een magazijn

Voor het plannen van de werkbelastingscapaciteit voor een magazijn, kunt u een werkbelasting instellen voor een of meerdere magazijnen en de werkbelastingsinstelling koppelen aan een hoofdplanning. In de werkbelastingcapaciteitsinstellingen kunt u beperkingen definiëren voor het gewicht of volume voor inkomende en uitgaande transacties. U kunt ook meerdere instellingen voor elk magazijn maken en de instelling vervolgens koppelen aan afzonderlijke hoofplanningen. U kunt deze aanpak bijvoorbeeld gebruiken om te voldoen aan seizoensgebonden wijzigingen in het personeelsbestand.

Als de werknemers voor een magazijn werken met transacties voor zowel inkomende als uitgaande werkbelasting, kunt u de instellingen voor de magazijncapaciteit zo configureren dat de werkbelasting in een gecombineerde weergave wordt voorspeld.

Als u werkbelasting voor magazijnen wilt plannen en bekijken, moet u de volgende taken uitvoeren:

1. Instellingen voor werkbelastingscapaciteit maken en de beperkingen van de werkbelastingscapaciteit voor een of meerdere magazijnen opgeven.
2. Koppel de instellingen voor de werkbelastingcapaciteit aan een hoofdplan om werkbelastingvoorspellingen te maken en aan te geven hoe lang de voorspellingen van toepassing zijn.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Instellingen werkbelastingscapaciteit voor een magazijn maken

1. Selecteer **Voorraadbeheer** \> **Instellen** \> **Magazijnbewaking** \> **Werkbelastingcapaciteit**.
2. Selecteer in het actievenster **Nieuw** om instellingen voor werkbelastingcapaciteit te maken.
3. Selecteer op het sneltabblad **Magazijnen** de optie **Nieuw** en voer waarden op de regel in om een magazijn te koppelen aan de instellingen voor werkbelastingcapaciteit.
4. Schakel het selectievakje **Gecombineerde inkomende en uitgaande werkbelasting** in als in het rapport **Werkbelastingcapaciteit** de totale werkbelasting voor inkomende en uitgaande transacties in één weergave moet worden weergegeven.
5. Selecteer op het sneltabblad **Transactietypen** de typen inkomende en uitgaande transacties waarop de werkbelastingslimieten van toepassing zijn.

    > [!NOTE]
    > U moet ten minste één transactietype voor zowel de inkomende als uitgaande werkbelasting selecteren.

#### <a name="define-limits-for-volume-or-weight"></a>Limieten voor volume of gewicht definiëren

U kunt limieten voor volume of gewicht instellen, afhankelijk van de beperking die relevant is voor het personeel van het magazijn. De limieten die u opgeeft, worden opgenomen in de voorspelling van de werkbelastingcapaciteit die u kunt bekijken in het rapport **Werkbelastingcapaciteit**.

Om informatie over volume en gewicht voor artikelen te voorspellen, moet het standaardvolume van één vooraadartikel en het gewicht van één vooraadartikel worden opgegeven voor alle producten. De velden die vereist, zijn beschikbaar in de volgende veldgroepen op het sneltabblad **Voorraad beheren** van de pagina**Vrijgegeven productdetails**:

- Verwerking
- Fysieke afmetingen
- Gewichtsmaten

Als deze informatie niet correct wordt opgegeven, ontvangt u een bericht als u het rapport **Werkbelastingcapaciteit** genereert. Vanuit het rapport kunt u vervolgens inzoomen om de ontbrekende informatie te identificeren die is vereist om de toekomstige werkbelasting te voorspellen.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Instelling werkbelastingscapaciteit aan een hoofdplan koppelen

1. Selecteer **Voorraadbeheer** \> **Periodiek** \> **Werkbelasting plannen**.
2. Selecteer in het veld **Hoofdplan** het hoofdplan dat moet worden gebruikt voor werkbelastingvoorspellingen.
3. Geef in het veld **Aantal dagen** het aantal dagen op waarop de werkbelastingvoorspelling betrekking heeft.
4. Selecteer in het veld **Werkbelasting** de werkbelastingsinstelling die moet worden gekoppeld aan het hoofdplan.

### <a name="view-workload-capacity"></a>Werkbelastingscapaciteit bekijken

1. Selecteer **Voorraadbeheer** \> **Query's en rapporten** \> **Fysieke-voorraadrapporten** \> **Werkbelastingcapaciteit**.
2. Geef in het veld **Aantal kolommen** het aantal kolommen op dat moet worden weergegeven in het rapport.
3. Selecteer in het veld **Ordertype** **Gepland en bevestigd**, **Gepland** of **Bevestigd** om het type orders aan te geven dat moet worden voorspeld in het rapport.
4. Selecteer in het veld **Type lading** een ladingtype om op te geven of de werkbelastingcapaciteit moet worden voorspeld voor volume of gewicht.
5. Selecteer in het veld **Werkbelastingcapaciteit** een instelling voor werkbelastingcapaciteit.

