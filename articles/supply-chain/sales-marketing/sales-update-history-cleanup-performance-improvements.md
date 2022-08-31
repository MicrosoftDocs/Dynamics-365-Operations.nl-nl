---
title: Opschonen van verkoophistoriegegevens plannen
description: In dit artikel wordt beschreven hoe u de systeemprestaties kunt verbeteren door te plannen dat de periodieke taak Opschoning van verkoophistorie voor update regelmatig wordt uitgevoerd.
author: myvakalo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e9a4dd5372afa8a0452449d1cb9121107e6e1610
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335498"
---
# <a name="schedule-sales-history-data-cleanup"></a>Opschonen van verkoophistoriegegevens plannen

[!include [banner](../includes/banner.md)]

Als onderdeel van de standaardbewerking worden in Microsoft Dynamics 365 Supply Chain Management doorlopend updategegevens voor de verkoophistorie gegenereerd en opgeslagen. Na een bepaalde periode kan een groot aantal verouderde verkoophistoriegegevens in het systeem worden verzameld. Deze verzamelde gegevens kunnen leiden tot prestatie- en functionele problemen wanneer documenten met betrekking tot verkooporders worden geboekt. (Deze documenten bevatten verkooporderbevestigingen, verkooppakbonnen, verkooporderverzamellijsten en facturen). Daarom moet u instellen dat de periodieke taak *Opschoning van verkoophistorie voor update* regelmatig wordt uitgevoerd. Met deze taak worden alle updategegevens voor de verkoophistorie verwijderd die niet meer nodig zijn.

Als u de periodieke taak *Opschoning van verkoophistorie voor update* gebruikt, raden we u aan om de functie *Prestatieverbeteringen bij opschonen van verkoophistorie* in te schakelen om de taak effectiever uit te voeren. (U kunt de taak echter ook uitvoeren zonder deze functie in te schakelen.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>De functies voor het opschonen van de verkoophistorie inschakelen

Als u de periodieke taak *Opschoning van verkoophistorie voor update* wilt instellen en gebruiken met alle functies die in dit artikel worden beschreven, moet u de functies *Prestatieverbeteringen bij opschonen van verkoophistorie* en *Verkoophistorie voor update opschonen op basis van ouderdom* in Functiebeheer inschakelen, zoals wordt beschreven in de volgende subsecties.

### <a name="sales-history-cleanup-performance-improvements"></a>Prestatieverbeteringen bij opschonen van verkoophistorie

De periodieke batchtaak **Opschoning van verkoophistorie** kan veel tijd kosten als deze niet vaak in omgevingen wordt uitgevoerd met veel verkoopupdates. In deze situaties kan de functie *Prestatieverbeteringen bij opschonen van verkoophistorie* de uitvoeringsduur verminderen en de betrouwbaarheid verbeteren.

Met deze functie kunt u de bestaande opschoonfunctie op de volgende manieren verbeteren:

- De opschoning wordt opgesplitst in batches (u kunt de batchgrootte wijzigen via aanpassingen).
- De opschoning wordt maximaal 2 uur uitgevoerd (u kunt de duur wijzigen via aanpassingen).
- Waar mogelijk wordt gebruik gemaakt van databasemogelijkheden om vergrendelconflicten tot een minimum te beperken en samenvoeging van transactietabellen tijdens opschonen te voorkomen.

Nadat u de functie hebt ingeschakeld, wordt de batchtaak **Opschoning van verkoophistorie** (**Verkoop en marketing \> Periodieke taken \> Opschonen \> Opschoning van verkoophistorie**) uitgevoerd zoals eerder, maar met betere prestaties en maximaal twee uur. Dit betekent dat de taak mogelijk meerdere keren moet worden uitgevoerd om alle gegevens op te schonen voor een bepaalde periode.

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** *Verkoop en marketing*
- **Functienaam:** *Prestatieverbeteringen bij opschonen van verkoophistorie*

### <a name="clean-up-sales-update-history-based-on-age"></a>Verkoophistorie voor update opschonen op basis van ouderdom

Met de functie *Verkoophistorie voor update opschonen op basis van ouderdom* kunt u de maximale ouderdom instellen van records die u wilt behouden wanneer de periodieke taak *Opschoning van verkoophistorie voor update* wordt uitgevoerd. Oudere records worden verwijderd. Deze functie is handig wanneer u de taak zo instelt dat deze periodiek wordt uitgevoerd, omdat de ouderdom altijd wordt berekend in relatie tot de datum waarop de taak wordt uitgevoerd. Als u deze functie niet gebruikt, kunt u alleen een specifieke datum instellen voor de oudste records die u kunt bewaren.

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Verkoophistorie voor update opschonen op basis van ouderdom* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>De periodieke taak voor het opschonen van de verkoophistorie instellen en plannen

Als u de periodieke taak *Opschonen van verkoophistorie* wilt instellen en plannen, gaat u als volgt te werk.

1. Analyseer de behoeften van uw bedrijf om te bepalen hoeveel dagen aan historische boekingsgegevens voor verkooporders u moet bewaren. Het is meestal raadzaam om de opschoontaak elke drie maanden en uiterlijk elke zes maanden uit te voeren.
1. Ga naar **Verkoop en marketing \> Periodieke taken \> Opschonen \> Opschoning van verkoophistorie**.
1. Stel in het dialoogvenster **Verkoophistorie voor update opschonen** op het sneltabblad **Parameters** de volgende velden in:

    - **Opschonen**: selecteer een van de volgende waarden om op te geven welk type records u wilt opschonen:

        - **Uitgevoerd**: verwijder alleen records die volledig zijn verwerkt. Aangezien u waarschijnlijk nog vaker gebruik wilt maken van deze records, is deze optie het veiligst.
        - **Uitgevoerd en foutief**: zowel volledig verwerkte records als records met een fout worden verwijderd. Deze optie wordt het meest gebruikt. Misschien wilt u foutieve records controleren en zelfs herstellen in plaats van ze automatisch te laten opschonen. Veel bedrijven kiezen er echter ook voor om deze records na ongeveer een maand op te schonen, omdat ze op dat moment waarschijnlijk niet meer relevant zijn.
        - **Alle**: Uitgevoerde, foutieve en wachtende records worden verwijderd. Wachtende records zijn geldig, maar zijn nog niet volledig verwerkt. In de meeste gevallen wilt u deze waarschijnlijk niet automatisch verwijderen. In bepaalde situaties kunt u er echter voor kiezen deze automatisch te verwijderen nadat een bepaalde tijd is verstreken.

    - **Records behouden op basis van ouderdom**: geef op of u records wilt opschonen op basis van hun leeftijd op de dag waarop de taak wordt uitgevoerd of records wilt verwijderen die vóór een vaste datum zijn gemaakt. Als u het opschonen wilt plannen als een terugkerende taak, moet u deze optie instellen op *Ja* omdat de ouderdom altijd wordt berekend in relatie tot de datum waarop de taak wordt uitgevoerd.

        - Stel deze optie in op *Ja* om het veld **Maximale ouderdom** in te schakelen. U gebruikt dit veld om de maximale ouderdom op te geven van de records die moeten worden behouden wanneer de taak wordt uitgevoerd. Het veld **Gemaakt tot** wordt genegeerd.
        - Stel deze optie in op *Nee* om het veld **Gemaakt tot** in te schakelen. U gebruikt dit veld om de oudste aanmaakdatum op te geven van de records die moeten worden behouden wanneer de taak wordt uitgevoerd. Het veld **Maximale ouderdom** wordt genegeerd.

    - **Gemaakt tot**: deze instelling is alleen van toepassing als de optie **Records behouden op basis van ouderdom** op *Nee* is ingesteld. Geef de oudste aanmaakdatum op van de records die moeten worden behouden wanneer de taak wordt uitgevoerd. Records die voor deze datum zijn gemaakt, worden verwijderd.
    - **Maximale ouderdom**: deze instelling is alleen van toepassing als de optie **Records behouden op basis van ouderdom** op *Ja* is ingesteld. Geef de maximale ouderdom (in dagen) op van de records die moeten worden behouden wanneer de taak wordt uitgevoerd. Oudere records worden verwijderd.

1. Geef op het sneltabblad **Uitvoeren op de achtergrond** op hoe, wanneer en hoe vaak het taak wordt uitgevoerd. Gebruik deze instellingen om de planning te implementeren die u hebt vastgesteld in stap 1. De velden werken op dezelfde manier als bij andere typen [batchtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK** om de instellingen toe te passen en het dialoogvenster te sluiten.
