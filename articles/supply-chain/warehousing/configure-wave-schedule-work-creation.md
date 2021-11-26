---
title: Het maken van werk plannen tijdens waves
description: In dit onderwerp wordt beschreven hoe u de waveverwerkingsmethode Werk maken plannen instelt en gebruikt.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5e9dc9b7cf33f9393f408d8f8a458e9b0ea47639
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778372"
---
# <a name="schedule-work-creation-during-wave"></a>Het maken van werk plannen tijdens waves

[!include [banner](../../includes/banner.md)]

Gebruik de functie *Werk maken plannen* als onderdeel van uw waveproces om de waveverwerkingsdoorvoer te verbeteren door het systeem werk te laten maken met parallelle verwerking.

Wanneer de functionaliteit is ingeschakeld, wordt automatisch gepland werk gemaakt, waarmee uiteindelijk werkelijk werk wordt gemaakt. Als het aantal waveladingregels een vooraf bepaalde drempel bereikt, wordt het werkelijke werk sneller gemaakt door parallelle asynchrone verwerking toe te passen.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>De functies voor het maken van gepland werk inschakelen in functiebeheer

Als u de functies wilt gebruiken die in dit onderwerp worden beschreven, moeten deze zijn ingeschakeld voor uw systeem. Gebruik de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de volgende functies in deze volgende in te schakelen:

1. **Werk blokkeren voor de hele organisatie**: vereist voor zowel handmatige als automatische configuratie van geplande werkcreatie. (Vanaf Supply Chain Management versie 10.0.21 is deze functie verplicht, waardoor deze standaard wordt ingeschakeld en niet meer kan worden uitgeschakeld.)
1. **Werk maken plannen**: vereist voor zowel handmatige als automatische configuratie van geplande werkcreatie.
1. **Wavemethode "Werk maken plannen" voor de hele organisatie**: vereist voor automatische configuratie van geplande werkcreatie. U hebt deze functie niet nodig als u alleen handmatige configuratie gebruikt.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Geplande werkcreatie automatisch configureren

Als u de functie *Wavemethode "Werk maken plannen" voor de hele organisatie* inschakelt, gebeurt automatisch het volgende in uw systeem:

- De wavemethode *Werk maken plannen* (`WHSScheduleWorkCreationWaveStepMethod`) wordt toegevoegd en geconfigureerd om parallel te worden uitgevoerd voor alle rechtspersonen.
- Voor wavesjablonen van alle rechtspersonen die **Type wavesjabloon** hebben ingesteld op *Verzenden* en **Sjabloonstatus** op *Geldig*, wordt de methode *Werk maken* vervangen door de methode *Werk maken plannen*. Wavesjablonen van rechtspersonen waarbij de methode *Werk maken* kan worden herhaald, worden echter niet gewijzigd.
- Taakconfiguraties voor de methode *Maken van werk plannen* worden gemaakt voor alle magazijnen van alle rechtspersonen waarvoor **Processen voor magazijnbeheer gebruiken** is ingeschakeld. Dit betekent dat de methode *Maken van werk plannen* nu standaard parallel wordt uitgevoerd. Bestaande magazijnen waarvoor u **Processen voor magazijnbeheerprocessen gebruiken** wijzigt van *Nee* naar *Ja*, gebruikt, voeren deze methode standaard ook parallel uit.
- Alle rechtspersonen verwerken waves in batches en **Wachten op vergrendeling (ms)** wordt ingesteld op een standaardwaarde van *60.000* ms als deze eerder was ingesteld op *0* ms.
- Alle nieuwe wavesjablonen die u maakt, hebben de wavemethode *Werk maken plannen* in plaats van de methode *Werk maken*.

De bestaande taak- en waveverwerkingsconfiguraties worden ook bewaard voor alle rechtspersonen die al zijn geconfigureerd voor het verwerken van wqaves in batches en voor alle magazijnen die al zijn geconfigureerd om de methode *Maken van werk plannen* parallel gebruiken.

Indien nodig kunt u een of alle instellingen die automatisch zijn gemaakt handmatig terugzetten wanneer u de functie *Wavemethode "Werk maken plannen" voor de hele organisatie* hebt ingeschakeld door het volgende te doen:

- Ga voor wavesjablonen naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**. Vervang de methode *Werk maken plannen* door *Werk maken*.
- Ga voor magazijnparameters naar **Magazijnbeheer \> Instellen \> Parameters voor magazijnbeheer**. Pas op het tabblad **Golfverwerking** de gewenste waarden toe voor **Waves verwerken in batch** en **Wachten op vergrendeling (ms)**.
- Ga voor de wavemethoden naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**. Selecteer `WHSScheduleWorkCreationWaveStepMethod` en selecteer **Taakconfiguratie** in het actievenster. Wijzig of verwijder het aantal batchtaken en de toegewezen wavegroep voor elk vermeld magazijn indien nodig.

## <a name="manually-configure-scheduled-work-creation"></a>Werkcreatie handmatig configureren

Als u de [functie *Wavemethode "Werk maken plannen" voor de hele organisatie*](#Auto-enable-schedule-work-creation) niet hebt ingeschakeld, kunt u de procedures in deze sectie gebruiken om geplande werkcreatie handmatig te configureren als dat nodig is.

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
1. Selecteer de pijl die naar de kolom **Geselecteerde methoden** verwijst om de geselecteerde rij naar die kolom te verplaatsen. (U kunt slechts één geselecteerde methode tegelijk gebruiken waarbij ofwel `WHSScheduleWorkCreationWaveStepMethod` of `createWork` wordt gebruikt zodat de bestaande rij met **Methodenaam** `createWork` automatisch wordt verplaatst naar het raster **Resterende methoden**.)

## <a name="set-wave-task-processing-threshold-data"></a>Drempelgegevens voor wavetaakverwerking instellen

Het systeem maakt standaarddrempelgegevens voor wave-taakverwerking wanneer een waveproces voor de eerste keer met behulp van op taken gebaseerde verwerking wordt uitgevoerd. De gegevens worden gebruikt om te bepalen wanneer waveverwerking asynchroon wordt uitgevoerd en op taken is gebaseerd, waardoor werk parallel kan worden verwerkt en gemaakt.

De standaardgegevens gebruiken in eerste instantie een drempelwaarde van 15 voor het minimum aantal belastingregels (`MINIMUMWAVELOADLINES`). Dit betekent dat wanneer het systeem een wave met meer dan 15 belastingregels verwerkt, asynchrone taakverwerking wordt gebruikt. U kunt deze gegevens handmatig invoegen/bijwerken in de tabel `WHSWaveTaskProcessingThresholdParameters` in uw testomgevingen. Als u deze instelling moet wijzigen in een productieomgeving, moet u contact opnemen met Microsoft Ondersteuning om de update aan te vragen.

## <a name="work-with-the-scheduled-work-creation"></a>Werken met de geplande werkcreatie

Zie [Waves maken en verwerken](wave-processing.md) voor meer informatie over het werken met geplande werkcreatie. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
