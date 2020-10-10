---
title: Foutbeheer
description: In dit onderwerp wordt foutbeheer in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 72d6c8d750a5a0903017b4c77b3ce5d9521cf99b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889356"
---
# <a name="fault-management"></a>Foutbeheer

[!include [banner](../../includes/banner.md)]

 

In Activabeheer kunt u de foutontwerper gebruiken om foutsymptomen, foutgebieden en foutsoorten in te stellen voor typen activa. Op deze manier kunt u fouten beheren die op activa zijn gedetecteerd. Bovendien kunnen de foutoorzaken en suggesties voor het corrigeren van fouten op een werkorder worden geregistreerd.

Het proces voor foutregistratie en -beheer bestaat uit de volgende stappen.

1. Een lijst met foutsymptomen, foutgebieden en foutsoorten maken die mogelijk voorkomen op uw typen activa.
2. In de foutontwerper stelt u symptomen, foutgebieden en fouttypen in.

Hier volgen enkele voorbeelden om u te helpen het verschil te begrijpen tussen foutsymptomen, foutgebieden en fouttypen.

**Foutsymptomen:**

- Onevenwichtige spanningen
- Kortsluiting
- Lawaai
- Lek
- Trillingen

**Foutgebieden:**

- Elektrisch
- Mechanisch
- Hydraulisch
- Pneumatisch

**Foutsoorten:**

- Defecte hoofdstatorwikkeling
- Defecte diode
- Vervuilde wikkelingen
- Defecte generator
- Defecte sensor

## <a name="create-fault-symptoms"></a>Foutsymptomen maken

Voer de volgende stappen uit om een lijst met symptomen te maken die kunnen worden gebruikt in de foutontwerper.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutsymptomen**.
2. Selecteer **Nieuw** om een record te maken.
3. Voer in het veld **Foutsymptoom** een naam in voor het foutsymptoom.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer **Opslaan**.

## <a name="create-fault-areas"></a>Foutgebieden maken

Voer de volgende stappen uit om een lijst met gebieden of locaties te maken die kunnen worden gebruikt in de foutontwerper.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutsymptomen**.
2. Selecteer **Nieuw** om een record te maken.
3. Voer in het veld **Foutsymptoom** een naam in voor het foutsymptoom.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer **Opslaan**.

## <a name="create-fault-types"></a>Foutsoorten maken

Voer de volgende stappen uit om een lijst met foutsoorten te maken die kunnen worden gebruikt in de foutontwerper.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Type fouten**.
2. Selecteer **Nieuw** om een record te maken.
3. Voer in het veld **Type fout** een naam op voor het type fout.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer **Opslaan**.

## <a name="set-up-the-fault-designer"></a>De foutontwerper instellen

In de foutontwerper stelt u foutgegevens in voor typen activa.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutontwerper**.
2. Selecteer in het linkerdeelvenster het type activa waarvoor u een foutrecord wilt instellen.
3. Selecteer in het Sneltabblad **Foutsymptoom** de optie **regel toevoegen** en selecteer vervolgens in het veld **Foutsymptoom** een foutsymptoom.
4. Selecteer in het Sneltabblad **Foutgebied** de optie **Regel toevoegen** en selecteer vervolgens in het veld **Foutgebied** een foutgebied.
5. Selecteer in het Sneltabblad **Fouttype** de optie **Regel toevoegen** en selecteer vervolgens in het veld **Fouttype** een fouttype.
6. Om snel combinaties van alle bestaande foutsymptomen, -gebieden en -typen voor het geselecteerde activatype te maken, selecteert u **Foutcombinaties** maken. Deze functie is handig als u veel foutsymptomen, -gebieden en -typen hebt toegevoegd. Het is eenvoudiger om de regels te verwijderen voor alle combinaties die niet relevant zijn voor het type activum dan om handmatig nieuwe regels te maken.

    > [!NOTE]
    > Als u de instellingen van foutsymptomen, -gebieden en -typen van het ene type activum naar het geselecteerde type activum wilt kopiëren, selecteert u **Kopiëren vanuit activum type**.

7. Klik op **Opslaan** om uw wijzigingen op te slaan.

![Pagina Foutontwerper](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Foutoorzaken maken

Volg deze stappen om een lijst met bekende foutoorzaken te maken die kunnen worden toegevoegd aan een werkorder of een onderhoudsaanvraag.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutoorzaken**.
2. Selecteer **Nieuw** om een record te maken.
3. Voer in het veld **Foutoorzaak** een naam op voor de foutoorzaak.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer **Opslaan**.

## <a name="create-fault-remedies"></a>Foutoplossingen maken

Volg deze stappen om een lijst met suggesties voor oplossing en reparatie te maken die kunnen worden toegevoegd aan een werkorder of een onderhoudsaanvraag.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Fout** \> **Foutoplossing**.
2. Selecteer **Nieuw** om een record te maken.
3. Voer in het veld **Foutoplossing** een naam in voor de foutoplossing.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer **Opslaan**.

> [!NOTE]
> U kunt de namen van uw foutsymptomen, -gebieden, -typen, -oorzaken en -oplossingen wijzigen als dat nodig is. De naamswijzigingen worden automatisch weergegeven in de gerelateerde foutregistraties.
