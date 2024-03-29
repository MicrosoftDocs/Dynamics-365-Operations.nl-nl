---
title: Batchverwerking van waarschuwingen
description: Dit artikel biedt informatie over batchverwerking van waarschuwingen.
author: RichdiMSFT
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: ba17ebe1bdd95b8780b99b8f82b566bf527aca89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860063"
---
# <a name="batch-processing-of-alerts"></a>Batchverwerking van waarschuwingen

[!include [banner](../includes/banner.md)]

Waarschuwingen worden verwerkt met de functionaliteit voor batchverwerking. Stel batchverwerking in vóór het proces en het verzenden van waarschuwingen.

Batchverwerkingsfunctionaliteit ondersteunt twee soorten gebeurtenissen:

- Gebeurtenissen die worden geactiveerd door gebeurtenissen op basis van een wijziging. Deze gebeurtenissen worden ook wel gebeurtenissen voor het maken/verwijderen en bijwerken genoemd.
- Gebeurtenissen geactiveerd door vervaldatums.

U kunt batchprocessen instellen voor elk gebeurtenistypen.

## <a name="batch-processing-for-change-based-events"></a>Batchverwerking voor gebeurtenissen op basis van wijzigingen

Het systeem leest alle gebeurtenissen op basis van wijzigingen, die hebben plaatsgevonden sinds het batchproces was uitgevoerd. Op wijzigingen gebaseerde gebeurtenissen bevatten updates voor velden, het verwijderen van registraties en het maken van registraties. Deze gebeurtenissen worden vergeleken met de voorwaarden die zijn ingesteld in waarschuwingsregels. Het batchproces genereert een waarschuwing wanneer een gebeurtenis voldoet aan de voorwaarden van de regel.

### <a name="frequency-for-change-based-events"></a>Frequentie instellen voor gebeurtenissen op basis van wijzigingen

U kunt voor gebeurtenissen op basis van wijzigingen een batchtaak instellen waarmee de verwerking van een gebeurtenis wordt gestart nadat de gebeurtenis door het systeem is vastgelegd. Als u de instelling maakt om de batchtaak vaker te herhalen, ontvangen gebruikers hun waarschuwingen sneller nadat wijzigingen optreden. Een hoge frequentie voor batchverwerking kan echter een nadelige invloed hebben op de systeemprestaties.

Anderzijds kan een batchtaak die minder vaak terugkeert en die u plant voor momenten dat de systeembelasting laag is, helpen om de systeemprestaties te verbeteren. Een lage frequentie voor batchverwerking kan mogelijk niet voldoen aan de eisen van een gebruiker voor tijdige waarschuwingen.

Bij het instellen van de frequentie voor batchverwerking van gebeurtenissen op basis van wijzigingen, moet u dus een balans zien te vinden tussen de tijdigheid van waarschuwingen en de prestaties van het systeem. Dit is nog belangrijker wanneer een groot aantal gebruikers waarschuwingsregels maakt. De frequentie is niet van invloed op het aantal gebeurtenissen dat het systeem verwerkt. Als er meer gebruikers regels maken, voert het proces meer controles uit. De systeemprestaties kunnen door dit type gegevensuitwisseling worden beïnvloed.

#### <a name="the-risks-of-low-batch-frequency"></a>De risico's van een lage batchfrequentie

Als u een lage frequentie instelt voor batchverwerking voor gebeurtenissen op basis van wijzigingen, worden de gegevens die relevant zijn voor de voorwaarden in de waarschuwingsregels mogelijk gewijzigd vóór de verwerking. Daarom worden er mogelijk waarschuwingen gemist.

Stel bijvoorbeeld dat u een waarschuwing maakt om te activeren wanneer de gebeurtenis **wijzigingen in contactgegevens klant** en de voorwaarde **klant = BB** is. Met andere woorden wanneer de contactpersoon van de klant voor klant BB verandert, wordt de gebeurtenis vastgelegd. Het batchverwerkingssysteem is echter zo ingesteld, zodat de batchverwerking minder vaak voorkomt dan de gegevensinvoering. Als de klantnaam verandert van **BB** in **AA**, voordat de gebeurtenis is verwerkt, komen de gegevens in de database niet meer overeen met de voorwaarde in de regel, **klant = BB**. Wanneer de gebeurtenis ten slotte wordt verwerkt, wordt er geen waarschuwing gegenereerd.

### <a name="set-up-processing-for-change-based-alerts"></a>Verwerking van waarschuwingen op basis van wijzigingen instellen

1. Ga naar **Systeembeheer** &gt; **Periodieke taken** &gt; **Waarschuwingen** &gt; **Waarschuwingen op basis van wijzigingen**.
2. Voer de gewenste gegevens in in het dialoogvenster **Waarschuwingen op basis van wijzigingen**.

## <a name="batch-processing-for-due-date-events"></a>Batchverwerking voor gebeurtenissen met vervaldatums

Het systeem detecteert alle gebeurtenissen die zijn veroorzaakt door vervaldatums en deze gebeurtenissen worden vergeleken met de voorwaarden die zijn ingesteld in waarschuwingsregels. Het batchproces genereert een waarschuwing wanneer een gebeurtenis voldoet aan de voorwaarden van de regel.

### <a name="frequency-for-due-date-events"></a>Frequentie voor gebeurtenissen met vervaldatums

U kunt voor gebeurtenissen met vervaldatums batchtaken instellen die 's nachts of op specifieke tijdstippen overdag worden uitgevoerd om het systeem zo gelijkmatig mogelijk te belasten. Het is raadzaam dat u de batchtaak zo instelt dat deze ten minste één keer per dag wordt uitgevoerd. Als waarschuwingen zo snel mogelijk moeten worden verzonden, stelt u de batch in om te worden verwerkt direct nadat de systeemdatum verandert. Als u waarschuwingen wilt genereren op basis van gebeurtenissen met vervaldatums die plaatsvinden nadat de batchtaak al waarschuwingen heeft verwerkt, kunt u de batchtaak nogmaals op dezelfde dag uitvoeren.

Er is bijvoorbeeld een batchtaak uitgevoerd op een bepaalde dag. Vervolgens maakt u een inkooporder met een vervaldatum die een waarschuwing op dezelfde dag moet activeren. Om de waarschuwing op die dag te ontvangen, moet u de batchtaak opnieuw uitvoeren nadat de inkooporder is gemaakt. Als u de batchtaak echter niet nogmaals op die dag uitvoert, worden met de batchtaak van de volgende dag alle gebeurtenissen met vervaldatums gedetecteerd, die niet op de voorgaande dagen zijn verwerkt.

> [!NOTE]
> Zelfs al wordt het batchproces meerdere malen per dag uitgevoerd, dan worden waarschuwingen nooit tweemaal gekopieerd voor de gebeurtenis en voorwaarden met dezelfde vervaldatum. Waarschuwingen worden alleen voor de vervaldatums gegenereerd als gevolg van wijzigingen in het systeem die hebben plaatsgevonden nadat de laatste batchtaak werd uitgevoerd.

### <a name="batch-processing-window"></a>Batchverwerkingsvenster

De verwerking van waarschuwingsregels in een bedrijf kan om verschillende redenen worden gestopt. Deze redenen zijn vakanties, systeemfouten of andere problemen waardoor batchtaken een bepaalde tijd niet worden uitgevoerd.

Om te voorkomen dat waarschuwingen voor vervaldatums verouderd raken, omdat de batchtaak enkele dagen niet is uitgevoerd, kunt u een venster voor batchverwerking instellen. Met een venster voor batchverwerking stelt u in dat een batchtaak een bepaald aantal dagen niet wordt uitgevoerd.

Als u een venster voor batchverwerking instelt, wordt er een waarschuwing verzonden wanneer de waarschuwingsregel wordt verwerkt, zelfs als de waarschuwing de tijdslimiet overschrijdt die is opgegeven in de criteria voor de vervaldatum. Een waarschuwing wordt continu verzonden, net zolang als de periode die is opgegeven door deze tijdslimiet en het venster voor batchverwerking niet worden overschreden. Wanneer de periode de waarde overschrijdt die is gedefinieerd door de tijdslimiet plus het venster batchverwerking, wordt er geen waarschuwing meer verzonden.

### <a name="set-up-processing-for-due-date-alerts"></a>Verwerking van waarschuwingen voor vervaldata instellen

1. Ga naar **Systeembeheer** &gt; **Periodieke taken** &gt; **Waarschuwingen** &gt; **Waarschuwingen voor vervaldatum**.
2. Voer de gewenste gegevens in in het dialoogvenster **Waarschuwingen voor vervaldatum**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
