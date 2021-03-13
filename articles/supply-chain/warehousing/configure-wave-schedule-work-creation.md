---
title: Het maken van werk plannen tijdens waves
description: In dit onderwerp wordt beschreven hoe u de waveverwerkingsmethode Werk maken plannen instelt en gebruikt.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078248"
---
# <a name="schedule-work-creation-during-wave"></a>Het maken van werk plannen tijdens waves

[!include [banner](../includes/banner.md)]

Gebruik de functie *Werk maken plannen* als onderdeel van uw waveproces om de waveverwerkingsdoorvoer te verbeteren door het systeem werk te laten maken met parallelle verwerking.

Wanneer de functionaliteit is ingeschakeld, wordt automatisch gepland werk gemaakt, waarmee uiteindelijk werkelijk werk wordt gemaakt. Als het aantal waveladingregels een vooraf bepaalde drempel bereikt, wordt het werkelijke werk sneller gemaakt door parallelle asynchrone verwerking toe te passen.

## <a name="enable-the-schedule-work-creation-feature"></a>De functie Werk maken plannen inschakelen

### <a name="enable-the-feature-in-feature-management"></a>De functie in Functiebeheer inschakelen

Voordat u de functie *Werk maken plannen* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Werk maken plannen*

> [!NOTE]
> De functie *Werk blokkeren voor de hele organisatie* moet zijn ingeschakeld voordat u *Werk maken plannen* kunt inschakelen.

### <a name="manually-enable-batch-processing-of-waves"></a>Batchverwerking van waves handmatig inschakelen

Als u wilt profiteren van een parallelle asynchrone methode voor het maken van magazijnwerk, moet uw waveproces worden uitgevoerd in batch. Dit instellen:

1. Ga naar  **Magazijnbeheer \> Instellen \> Parameters voor magazijnbeheer**.

1. Stel op het tabblad **Algemeen** de optie **Waves verwerken in batch** in op *Ja*. U kunt eventueel ook een specifieke **Batchgroep voor waveverwerking** selecteren om te voorkomen dat de batchwachtrijverwerking wordt uitgevoerd op hetzelfde moment als andere processen.

1. Stel de **tijd Wachten op vergrendeling (ms)** in. Dit is van toepassing wanneer verschillende waves tegelijkertijd worden verwerkt. Voor de meeste grotere waveprocessen raden we een waarde van *60000* aan.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>De nieuwe wave-stapmethode voor bestaande wavesjablonen handmatig inschakelen

Begin met het maken van de nieuwe wave-stapmethode en het inschakelen van deze methode voor parallelle asynchrone taakverwerking.

1. Ga naar  **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.

1. Selecteer  **Methoden opnieuw genereren** en merk op dat *WHSScheduleWorkCreationWaveStepMethod* is toegevoegd aan de lijst met waveprocesmethoden die u kunt gebruiken in uw verzendwavesjablonen.

1. Selecteer de record met de **methodenaam** *WHSScheduleWorkCreationWaveStepMethod* en selecteer **Taakconfiguratie**.

1. Selecteer in het actievenster **Nieuw** om een rij toe te voegen aan het raster en gebruik de volgende instellingen:

    - **Magazijn**: selecteer het magazijn dat u wilt gebruiken voor de verwerking van de planning voor het maken van werk.

    - **Maximum aantal batchtaken**: een maximum aantal batchtaken opgeven. In de meeste gevallen moet deze waarde binnen het bereik van 8-16 liggen, maar we raden u aan om te experimenteren met de optimale instelling voor uw scenario's.

    - **Batchgroep voor verwerking van waves**: selecteer een specifieke batchgroep voor verwerking van uw waves om de batchwachtrijverwerking te optimaliseren.

U kunt nu een bestaande wavesjabloon bijwerken (of een nieuwe sjabloon maken) om de waveverwerkingsmethode *Werk maken plannen* te gebruiken.

1. Ga naar  **Magazijnbeheer  \> Instellen \> Waves \> Wavesjablonen**.

1. Selecteer **Bewerken** in het actievenster.

1. Selecteer in het lijstdeelvenster de wavesjabloon die u wilt bijwerken (als u test met demonstratiegegevens, kunt u *24 Standaardverzending* gebruiken).

1. Vouw het sneltabblad **Methoden** uit en selecteer de rij met de **naam** *Werk maken plannen* in het raster **Resterende methoden**.

1. Selecteer de pijl die naar de kolom **Geselecteerde methoden** verwijst om de geselecteerde rij naar die kolom te verplaatsen. (U kunt slechts één geselecteerde methode tegelijk gebruiken waarbij ofwel *WHSScheduleWorkCreationWaveStepMethod* of *createWork* wordt gebruikt zodat de bestaande rij met **Methodenaam** *createWork* automatisch wordt verplaatst naar het raster **Resterende methoden**.)

## <a name="set-wave-task-processing-threshold-data"></a>Drempelgegevens voor wavetaakverwerking instellen

Het systeem maakt standaarddrempelgegevens voor wave-taakverwerking wanneer een waveproces voor de eerste keer met behulp van op taken gebaseerde verwerking wordt uitgevoerd. De gegevens worden gebruikt om te bepalen wanneer waveverwerking asynchroon wordt uitgevoerd en op taken is gebaseerd, waardoor werk parallel kan worden verwerkt en gemaakt.

De standaardgegevens gebruiken in eerste instantie een drempelwaarde van 15 voor het minimum aantal belastingregels (MINIMUMLOADLINES). Dit betekent dat wanneer het systeem een wave met meer dan 15 belastingregels verwerkt, asynchrone taakverwerking wordt gebruikt. U kunt deze gegevens handmatig invoegen/bijwerken in de tabel **WHSWaveTaskProcessingThresholdParameters** in uw testomgevingen. Als u deze instelling in een productieomgeving wilt wijzigen, moet u contact opnemen met Microsoft Support om de update aan te vragen.

## <a name="work-with-the-feature"></a>Werken met de functie

Wanneer de functie *Werk maken plannen* is ingeschakeld, wordt er door waveverwerking gepland werk gemaakt, dat uiteindelijk wordt gebruikt door het nieuwe werkaanmaakproces. Tijdens het maken van het werk wordt het werk geblokkeerd met de functie *Werk blokkeren voor de hele organisatie*.

In het volgende stroomdiagram is te zien hoe gepland werk tijdens de verwerking van waves wordt gemaakt.

![Werk maken plannen](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Gepland werk

Op de pagina **Details gepland werk** (**Magazijnbeheer \> Werk \> Details gepland werk**) ziet u info over het geplande werk dat aanvankelijk is gemaakt tijdens waveverwerking. De volgende waarden **Processtatus** zijn beschikbaar:

- **In de wachtrij**: het geplande werk wacht om te worden gebruikt om werk te maken.
- **Voltooid** - Het geplande werk is gebruikt om werk te maken.
- **Mislukt:** de waveverwerking is mislukt. Houd er rekening mee dat het geplande werk een status **Mislukt** kan hebben met of zonder bijbehorend werkelijk werk. Wanneer het daadwerkelijke maken van het werk mislukt, blijft de status van het werkelijke werk *Geannuleerd*.

### <a name="batch-job-for-the-work-creation-process"></a>Batchtaak voor werk maken

Als u de batchtaken voor het verwerken van waves wilt weergeven, selecteert u **Batchtaken** in het actievenster op de pagina **Alle waves**.

In deze weergave kunt u alle details van de batchtaak voor elk van de batchtaak-ID´s weergeven.
