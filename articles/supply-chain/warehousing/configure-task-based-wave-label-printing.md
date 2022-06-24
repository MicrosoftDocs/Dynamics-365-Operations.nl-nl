---
title: Wavelabel afdrukken plannen tijdens wave
description: In dit artikel wordt beschreven hoe u de functionaliteit voor afdrukken van wavelabels op basis van taken kunt instellen en gebruiken.
author: perlynne
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ac2bc4cce42bada43334b82301d716414cd6d654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889452"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Wavelabel afdrukken plannen tijdens wave

[!include [banner](../../includes/banner.md)]

Gebruik de functie *Wavelabels afdrukken op basis van taken* als onderdeel van uw waveproces voor het verbeteren van de efficiëntie en om het systeem wavelabels en werk te laten maken in afzonderlijke taken.

Het proces van het configureren van wavelabels afdrukken is complex en is gebaseerd op nauwkeurige configuratie en hoofdgegevens. Genereren van wavelabelrecords mislukt wel eens en wanneer dat gebeurt, wordt de hele waveverwerking teruggedraaid. Met de functie *Wavelabels afdrukken op basis van taken* kunt u voorkomen dat u werk- en werkregels opnieuw moet maken telkens wanneer een wavelabel onjuist wordt afgedrukt.

Wanneer u de functie *Wavelabels afdrukken op basis van taken* gebruikt, worden eerst werk- en werkregels gemaakt. Er worden vervolgens wavelabels gemaakt en afgedrukt. Als de wavelabels correct zijn gemaakt, worden het werk en de wave voor orderverzameling vrijgegeven.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>De functie Wavelabels afdrukken op basis van taken in Functiebeheer inschakelen

Als u de functies wilt gebruiken die in dit artikel worden beschreven, moeten deze zijn ingeschakeld voor uw systeem. Gebruik werkgebied voor [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de functies in deze volgende in te schakelen:

1. *Wavelabels afdrukken*: deze functie is vereist om de procesmethode voor wavelabels afdrukken in te kunnen schakelen.
1. *Werk blokkeren voor de hele organisatie*: deze functie is vereist voor zowel handmatige als automatische configuratie van geplande werkcreatie. (Vanaf Supply Chain Management versie 10.0.21 is deze functie verplicht, waardoor deze standaard wordt ingeschakeld en niet meer kan worden uitgeschakeld.)
1. *Wavelabels afdrukken op basis van taken*: deze functie is nodig om afdrukken van wavelabels af te splitsen in een afzonderlijk transactiebereik.

## <a name="manually-enable-the-new-wave-step-method"></a>De nieuwe wavestapmethode handmatig inschakelen

U moet eerst de nieuwe wavestapmethode maken en deze methode inschakelen voor parallelle asynchrone taakverwerking.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.
1. Selecteer in het actievenster **Methode opnieuw genereren**. U ziet dat *waveLabelPrinting* is toegevoegd aan de lijst met procesmethoden die u kunt gebruiken in uw verzendwavesjablonen.
1. Selecteer de record waarin het veld **Naam methode** is ingesteld op *waveLabelPrinting* en selecteer vervolgens **Taakconfiguratie** in het actievenster.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Magazijn**: selecteer het magazijn dat u wilt gebruiken om werkcreatieverwerking te plannen. (Als u demogegevens gebruikt voor testdoeleinden, kunt u magazijn *24* selecteren.)
    - **Maximum aantal batchtaken**: geef een maximum aantal batchtaken op. In de meeste gevallen moet de waarde van *8* tot en met *16* zijn. Het is echter raadzaam om te zoeken naar de optimale instelling voor uw scenario's.
    - **Batchgroep voor verwerking van waves**: selecteer een specifieke batchgroep voor waveverwerking om de batchwachtrijverwerking te optimaliseren.

U kunt een bestaande sjabloon nu bijwerken zodat deze gebruik maakt van de wave-verwerkingsmethode *Wavelabels afdrukken*. U kunt ook een nieuwe wavesjabloon maken die deze methode gebruikt.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer in het lijstvenster de wavesjabloon die u wilt bijwerken. (Als u demogegevens gebruikt voor testdoeleinden, kunt u wavesjabloon *24 Standaardverzending* selecteren.)
1. Selecteer op het sneltabblad **Methoden** in de kolom **Resterende methoden** de rij waarin het veld **Naam** is ingesteld op *waveLabelPrinting*.
1. Selecteer **toevoegen** (de knop pijl-rechts) om de geselecteerde rij te verplaatsen naar de kolom **Geselecteerde methoden**.
1. Voer in het veld **Wavestapcode** een wavestapcode in die wordt gebruikt om de wavesjabloon een wavelabelsjabloon te koppelen.

## <a name="set-wave-task-processing-threshold-data"></a>Drempelgegevens voor wavetaakverwerking instellen

De eerste keer dat een waveproces door middel van een op taken gebaseerde verwerking wordt uitgevoerd, maakt het systeem standaarddrempelgegevens voor wavetaakverwerking. Die gegevens worden gebruikt om te bepalen of waveverwerking asynchroon wordt uitgevoerd en op taken is gebaseerd, zodat wavelabels parallel kunnen worden verwerkt en gemaakt.

De standaardgegevens gebruiken in eerste instantie een drempelwaarde van *1* voor het minimum aantal werk-id's (`MinimumWorkThresholdForLabelPrinting`). Wanneer het systeem een wave met meerdere werk-id's verwerkt, wordt er gebruik gemaakt van op taken gebaseerde verwerking van wavelabels in een afzonderlijke transactie. U kunt deze gegevens handmatig invoegen of bijwerken in de tabel `WHSWaveTaskProcessingThresholdParameters` in uw testomgevingen. Als u de instelling wilt wijzigen in een productieomgeving, moet u contact opnemen met Microsoft Ondersteuning om de update aan te vragen.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Wijzigingen in de waveverwerkingslogica wanneer afdrukken van wavelabels op basis van taken wordt gebruikt

Als de wavelabelverwerking de verwerkingsdrempel voor de wavetaak overschrijdt, wordt een taakgebaseerde verwerking gestart. Bij de volgende waveverwerking die geschikt is voor de wavesjabloon, wordt afdrukken van wavelabels uitgevoerd in een op zichzelf staande *ttsbegin*/*ttscommit*-transactie, direct na het maken van het werk. Als vrijgave van werk (deblokkeren) in de wavesjabloon wordt geconfigureerd om automatisch te worden uitgevoerd, vindt deze alleen plaats nadat het afdrukproces voor wavelabels met succes is voltooid.

Als het genereren van wavelabels mislukt (bijvoorbeeld als de conversie van de werkhoeveelheid naar de wavelabelhoeveelheid is mislukt en een fout optreedt), mislukt alleen de betreffende transactie. Het werk dat eerder is gemaakt, blijft geblokkeerd. Volg deze stappen om fouten te corrigeren en de wavelabels af te drukken.

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de betreffende wave in het raster.
1. Selecteer in het actievenster op het tabblad **Wave** in de groep **Afdrukken** de optie **Wavelabels**.
1. Volg de instructies op het scherm om de labels te verzenden voor afdrukken.
1. Selecteer in het actievenster op het tabblad **Wave** in de groep **Wave** de optie **Vrijgeven** om het werk voor de geselecteerde wave handmatig vrij te geven.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Wavelabels afdrukken](configure-wave-label-printing.md)
- [Het maken van werk tijdens wave plannen](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
