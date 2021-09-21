---
title: Kan de ingangsdatum van een goedgekeurde leverancier niet wijzigen
description: De ingangsdatum kan niet worden gewijzigd in de lijst met goedgekeurde leveranciers op productentiteit
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475968"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Kan de ingangsdatum van een goedgekeurde leverancier niet wijzigen


## <a name="symptoms"></a>Symptomen

Een product heeft een goedgekeurde leverancier die bijvoorbeeld een ingangsdatum heeft van 11 januari 2018 (*01/11/2018*) en de vervaldatum *Nooit*. Als u de ingangsdatum probeert te wijzigen in 10 januari 2018 (*01/10/2018*) of 12 januari 2018 (*01/12/2018*), wordt het volgende foutbericht weergegeven:

> Kan geen record maken in lijst met goedgekeurde leveranciers (PdsApproveVendorList). De waarde voor Vervaldatum moet groter zijn dan of gelijk zijn aan die van de Ingangsdatum.

## <a name="resolution"></a>Oplossing

U kunt alleen de periode verlengen waarvoor de leverancier is goedgekeurd. De volgende regels zijn van toepassing:

- Als u de ingangsdatum zo wilt wijzigen dat deze eerder is dan een van de bestaande records (perioden) voor de leverancier van het artikel, moet de vervaldatum van de nieuwe periode eerder zijn dan de vervaldatums in de bestaande records.
- Als u de vervaldatum zo wilt wijzigen dat deze later is dan een van de bestaande perioden, moet de ingangsdatum na de laatste vervaldatum in een bestaande record vallen.
- Als u de totale periode waarvoor de leverancier is goedgekeurd, wilt verkorten, moet u bestaande records verwijderen of wijzigen. U kunt ook de schakeloptie **Afkappen** gebruiken tijdens het importeren. Met deze schakeloptie verwijdert u alle bestaande records in de tabel voor goedgekeurde leveranciers per artikel.

Voor het voorbeeldscenario dat in de beschrijving van het probleem wordt beschreven, waarbij een record de ingangsdatum *01/11/2018* en de vervaldatum van *Nooit* heeft, kunt u een nieuwe record importeren met de ingangsdatum *01/10/2018* en de vervaldatum *Nooit*. Het is echter niet mogelijk om via gegevensbeheer de periode zo te verkleinen dat de ingangsdatum wordt bijgewerkt naar *01/12/2018*. U moet deze wijziging aanbrengen in de gebruikersinterface.
