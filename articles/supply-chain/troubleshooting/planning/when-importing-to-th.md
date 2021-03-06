---
title: U wordt gevraagd de instellingen voor artikelbehoefteplanning op te slaan, ook als u geen wijzigingen hebt aangebracht
description: U wordt gevraagd de instellingen voor artikelbehoefteplanning op te slaan, ook als u geen wijzigingen hebt aangebracht.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049460"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>U wordt gevraagd de instellingen voor artikelbehoefteplanning op te slaan, ook als u geen wijzigingen hebt aangebracht

KB-nummer: 4615588

## <a name="symptoms"></a>Symptomen

In sommige scenario's ontvangt u mogelijk het volgende bericht wanneer u de pagina **Artikelbehoefteplanning** opent nadat u artikelen hebt geïmporteerd via de entiteit *Artikelbehoefteplanning V2*:

> Wilt u uw wijzigingen opslaan alvorens te sluiten?

U ontvangt dit bericht ook als u geen wijzigingen hebt aangebracht.

## <a name="resolution"></a>Oplossing

De pagina **Artikelbehoefteplanning** bevat complexe standaardlogica die ertoe kan leiden dat het bericht wordt weergegeven nadat er recent directe wijzigingen in de database zijn aangebracht, bijvoorbeeld via het importeren van entiteiten. Het entiteitsveld `AREGENERALSETTINGSOVERRIDDEN` is bijvoorbeeld ingesteld op *Nee*, maar u importeert een bestand dat nieuwe of gewijzigde waarden bevat voor velden zoals `PRODUCTCOVERAGEGROUPID` en/of `VENDORACCOUNTNUMBER`. Omdat het veld `AREGENERALSETTINGSOVERRIDDEN` in dit geval is ingesteld op *Nee*, worden de waarden automatisch uit de velden gewist wanneer u de pagina **Artikelbehoefteplanning** voor de eerste keer na het importeren opent. Als u de wijzigingen opslaat wanneer daarom in het berichtvak wordt gevraagd, worden deze opgeslagen in de database. Anders ontvangt u hetzelfde bericht wanneer u de pagina de volgende keer opent.

Om dit gedrag te voorkomen, maar ook waarden op te nemen voor velden, zoals `PRODUCTCOVERAGEGROUPID` via entiteitsimport, stelt u `AREGENERALSETTINGSOVERRIDDEN` in op *Ja* wanneer u importeert.
