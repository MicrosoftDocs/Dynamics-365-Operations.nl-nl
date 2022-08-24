---
title: Een batchtaak maken
description: Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.
author: matapg007
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
ms.openlocfilehash: 06fb9a18e70c316be97645ba76f9462cd3ccc729
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292445"
---
# <a name="create-a-batch-job"></a>Een batchtaak maken

[!include [banner](../../includes/banner.md)]

Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden. Batchtaken worden uitgevoerd met behulp van de beveiligingsgegevens van de gebruiker die de taak heeft gemaakt. Voer de volgende procedure uit om een batchtaak te maken. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-the-batch-job"></a>De batchtaak maken
1. Ga naar **Navigatievenster > Modules > Systeembeheer > Query's > Batchtaken**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Taakomschrijving** een beschrijving van de batchtaak in.
4. Voer in het veld **Geplande begindatum/-tijd** de datum en het tijdstip in waarop de batchtaak moet worden uitgevoerd.
5. Selecteer **Opslaan**.

## <a name="create-a-recurrence"></a>Een terugkeerpatroon maken
1. Selecteer in het actievenster de optie **Batchtaak**.
2. Selecteer **Terugkeerpatroon**. Gebruik deze opties om een bereik en terugkeerpatroon in te voeren.  
3. Selecteer **OK**.

## <a name="add-alerts"></a>Waarschuwingen toevoegen
1. Selecteer in het actievenster de optie **Batchtaak**.
2. Selecteer **Waarschuwingen**. Geef aan of u waarschuwingsberichten wilt laten verzenden wanneer de batchtaak is voltooid, wanneer er een fout optreedt of wanneer de batchtaak wordt geannuleerd. Geef vervolgens op of u waarschuwingen wilt laten weergeven als pop-upberichten.   
3. Selecteer **OK**.

## <a name="add-a-task-to-a-batch-job"></a>Een taak toevoegen aan een batchtaak
1.  Selecteer op de pagina **Batchtaken** de optie **Taken weergeven**.
2.  Selecteer **Ctrl+N** om een taak te maken.
3.  Voer een beschrijving van de batchtaak in.
4.  Selecteer in het veld **Bedrijfsrekeningen** de bedrijfsdatabase waarin de taak moet worden uitgevoerd.
5.  Selecteer in het veld **Klassennaam** het proces dat door de taak moet worden uitgevoerd. 
6.  Selecteer indien nodig een batchgroep voor de taak.

    Clienttaken moeten aan een batchgroep worden toegewezen. Zij worden automatisch toegewezen aan de standaardbatchgroep (ook wel de lege batchgroep genoemd).

7.  Selecteer **Ctrl+S** om de taak op te slaan.
8.  Als u de geselecteerde taak afhankelijk wilt maken van een andere taak in de klus, selecteert u het raster **Heeft voorwaarden** en volgt u deze stappen voor elke voorwaarde die u wilt definiëren:

    1. Selecteer **Ctrl+N** om een voorwaarde te maken.
    2. Selecteer de taak-id van de bovenliggende taak.
    3. Selecteer de status die de bovenliggende taak moet bereiken voordat de afhankelijke taak kan worden uitgevoerd.
    4. Selecteer **Ctrl+S** om de voorwaarde op te slaan.

    Als u meerdere voorwaarden definieert en als aan *alle* voorwaarden moet worden voldaan om de afhankelijke taak te kunnen laten uitvoeren, selecteert u het voorwaardetype **Alle**. Als de afhankelijk taak al mag worden uitgevoerd als er aan *een van de* voorwaarden wordt voldaan, selecteert u **Willekeurig** als voorwaardetype.

9.  Selecteren hoe taakproblemen moeten worden afgehandeld. Als u het mislukken van een specifieke taak wilt negeren, selecteert u op het tabblad **Algemeen** de optie **Taakfout negeren** voor die taak. Als deze optie is geselecteerd, kan de taak toch worden uitgevoerd ondanks het mislukken van de taak. U kunt ook in het veld **Maximaal aantal pogingen** opgeven hoe vaak er mag worden geprobeerd een taak uit te voeren voordat die taak als mislukt wordt beschouwd. Het is raadzaam om het veld **Maximaal aantal pogingen** niet in te stellen op een waarde van meer dan **5**.

    Zie [Nieuwe pogingen voor batch inschakelen](../retryable-batch.md) voor meer informatie over nieuwe pogingen voor batchverwerking.

## <a name="adjust-batch-job-status"></a>Status van batchtaak aanpassen
1. Ga naar **Systeembeheer > Query's > Batchtaken**.
2. Selecteer de gewenste batchtaak.
3. Selecteer in het actievenster de optie **Batchtaak > Functies > Status wijzigen**.
4. Selecteer de gewenste status:
    - **Inhouden**: stel de batchtaak in op **Inhouden**, zodat deze niet wordt opgenomen in de planner van batchtaken. Staat gelijk aan *Stoppen*.
    - **Wachten**: stel de batchtaak in op **Wachten** om deze in de wachtrij voor de planner van batchtaken te zetten. Staat gelijk aan *Gaan*.
5. Selecteer **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
