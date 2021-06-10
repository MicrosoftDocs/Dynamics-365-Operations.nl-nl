---
title: BYOD geplande batchtaken optimaliseren
description: In dit onderwerp wordt uitgelegd hoe u prestaties optimaliseert wanneer u de BYOD-functie (Uw eigen database gebruiken) gebruikt met Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: ed3ebbf09403090a1173c3cda1a4b11b74419b90
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052668"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>BYOD geplande batchtaken optimaliseren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt uitgelegd hoe u prestaties optimaliseert wanneer u de BYOD-functie (Uw eigen database gebruiken). Meer informatie over BYOD vindt u in [Uw eigen database gebruiken (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Prestatieoverwegingen voor het exporteren van gegevens

Wanneer entiteiten zijn gepubliceerd naar de doeldatabase, kunt u de functie Exporteren in de werkruimte **Gegevensbeheer** gebruiken om gegevens te verplaatsen. Met de functie Exporteren kunt u een gegevensverplaatsingstaak definiëren die een of meer entiteiten bevat. Meer informatie over het exporteren van gegevens vindt u in [Overzicht van gegevensimport- en exporttaken](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

U kunt de pagina **Exporteren** gebruiken om gegevens te exporteren naar verschillende doelgegevensindelingen, zoals een CSV-bestand (Comma Separated Values). Deze pagina ondersteunt ook SQL-databases als een andere bestemming.

U kunt een gegevensproject met meerdere entiteiten maken en een batchtaak gebruiken om te plannen dat het gegevensproject wordt uitgevoerd. Als u de optie **Exporteren in batch** selecteer, kunt u plannen dat de gegevensexporttaak periodiek wordt uitgevoerd.

Om u de algehele betrouwbaarheid van de BYOD-export te bevorderen, moet u voorzichtig zijn wanneer u meerdere entiteiten aan een exportproject toevoegt. Wanneer u het aantal entiteiten bepaalt dat aan hetzelfde project moet worden toegevoegd, moet u rekening houden met de volgende parameters:

- De complexiteit van de entiteiten
- Het verwachte gegevensvolume per entiteit
- De totale tijd die nodig is om de export uit te voeren op het taakniveau

Voor de beste prestaties kunt u beter geen honderden entiteiten toevoegen aan één project. Het is raadzaam om meerdere taken te maken, die elk minder entiteiten bevatten.

## <a name="scheduling-byod-batch-jobs"></a>Batchtaken voor BYOD plannen

Om de impact op gebruikers van Microsoft Dynamics 365 Human Resources te beperken, voert u BYOD-batchtaken 's nachts of buiten kantooruren uit. Zorg dat u ook de tijdzone voor terugkerende batchtaken controleert. Er zijn batchtaken die mogelijk een andere tijdzone gebruiken.

Om prestatieproblemen te voorkomen, moet u rekening houden met de volgende factoren wanneer u de planningsfrequentie voor BYOD-batchtaken configureert:

- De tijd die nodig is om elke batchtaak te voltooien
- De bedrijfsbehoefte van de gegevens in BYOD

Stel de frequentie voor elke batchtaak in op een dusdanige waarde dat de taak ruim voor de volgende geplande uitvoeringstijd kan worden uitgevoerd. Vermijd de gelijktijdige uitvoering van meerdere taken, omdat deze benadering de prestaties van Human Resources negatief kan beïnvloeden.

Voor de beste prestaties gebruikt u altijd de optie **Exporteren in batch** op de pagina **Exporteren** om batchtaken voor BYOD te plannen. Vermijd de planning van terugkerende exports op **Beheren \> Terugkerende gegevenstaken beheren**.

## <a name="incremental-export"></a>Incrementele export

Wanneer u een entiteit toevoegt voor gegevensexport, kunt u een incrementele pushbewerking (export) of een volledige push uitvoeren. Met een volledige push verwijdert u alle bestaande records uit een entiteit in de BYOD-database. Vervolgens wordt de huidige set records uit de entiteit Human Resources ingevoegd.

Als u een incrementele push wilt uitvoeren, moet u Wijzigingen bijhouden inschakelen voor elke entiteit op de pagina **Entiteiten**. Meer informatie vindt u in [Wijzigingen bijhouden voor entiteiten inschakelen](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Als u een incrementele push selecteert, is de eerste push altijd een volledige push. SQL houdt wijzigingen bij ten opzichte van deze eerste volledige push. Wanneer een nieuwe record wordt ingevoegd of wanneer een record wordt bijgewerkt of verwijderd, wordt de wijziging gereflecteerd in de doelentiteit.

## <a name="time-outs"></a>Time-outs

Hier volgen de standaard time-outs voor BYOD-exports:

- Tien minuten voor afkapbewerkingen
- Een uur voor bulk insert-bewerkingen

Wanneer volumes hoog zijn, zijn deze time-outinstellingen mogelijk niet voldoende. Als u deze wilt bijwerken, gaat u naar **Gegevensbeheer \> Raamwerkparameters \> Uw eigen database gebruiken**. Deze time-outs zijn bedrijfsspecifiek en moeten voor elk bedrijf afzonderlijk worden ingesteld.

## <a name="known-limitations"></a>Bekende beperkingen

De functie BYOD heeft de volgende beperkingen:

- Tijdens de synchronisatie mogen er geen actieve vergrendelingen voor de database zijn. Actieve vergrendelingen kunnen leiden tot langzame schrijfbewerkingen of zelfs het niet kunnen exporteren van gegevens naar de Azure SQL-database.
- U kunt geen samengestelde entiteiten exporteren naar uw eigen database. Momenteel worden samengestelde entiteiten niet ondersteund. U moet afzonderlijke entiteiten exporteren die samen de samengestelde entiteit vormen. U kunt echter beide entiteiten in hetzelfde gegevensproject exporteren.
- Entiteiten die geen unieke sleutels hebben, kunnen niet worden geëxporteerd met een incrementele push. Deze beperking doet zich met name voor wanneer u records uit enkele kant-en-klare entiteiten incrementeel wilt exporteren. Omdat deze entiteiten zijn ontworpen om het importeren van gegevens mogelijk te maken, hebben ze geen unieke sleutel.

## <a name="troubleshooting"></a>Problemen oplossen

### <a name="incremental-push-doesnt-work-correctly"></a>Incrementele push werkt niet correct

**Probleem:** wanneer er voor een entiteit een volledige push wordt uitgevoerd, ziet u een grote set records in BYOD wanneer u een **select**-instructie gebruikt. Wanneer u echter een incrementele push uitvoert, ziet u slechts enkele records in BYOD. Het lijkt alsof de incrementele push alle records heeft verwijderd en alleen de gewijzigde records in BYOD heeft toegevoegd.

**Oplossing:** de SQL-tabellen voor het bijhouden van wijzigingen hebben mogelijk niet de verwachte status. In dit soort gevallen wordt aangeraden om Wijzigingen bijhouden uit te schakelen voor de entiteit en vervolgens weer in te schakelen. Meer informatie vindt u in [Wijzigingen bijhouden voor entiteiten inschakelen](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Faseringstabellen worden niet geleegd

**Probleem**: Wanneer u fasering voor het project gebruikt, worden de faseringstabellen niet op de juiste manier geleegd. Er worden steeds meer gegevens aan de tabellen toegevoegd, wat tot prestatieproblemen leidt.

**Oplossing**: In de faseringstabellen wordt zeven dagen historie aangehouden. Historische gegevens ouder dan zeven dagen worden automatisch uit de faseringstabellen gewist door de batchtaak **Exportfasering opschonen**. Als deze taak niet correct wordt uitgevoerd, worden de tabellen niet op de juiste manier leeggemaakt. Als u deze batchtaak opnieuw start, wordt het proces voortgezet om de faseringstabellen automatisch op te schonen.

## <a name="see-also"></a>Zie ook

[Overzicht van Gegevensbeheer](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Uw eigen database gebruiken (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Overzicht van Gegevensimport- en exporttaken](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Wijzigingen bijhouden voor entiteiten inschakelen](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
