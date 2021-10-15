---
title: Updates voor standaardkosten beheren
description: 'Updates van standaardkostengegevens kunnen worden beheerd met twee verschillende benaderingen: de benadering met één versie en de benadering met twee versies.'
author: AndersGirke
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 942b144c78176e9a00cdc12101e2948e8aa4685e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579755"
---
# <a name="manage-standard-cost-updates"></a>Updates voor standaardkosten beheren

[!include [banner](../includes/banner.md)]

Updates van standaardkostengegevens kunnen worden beheerd met twee verschillende benaderingen: de benadering met één versie en de benadering met twee versies.

Bij de benadering met één versie wordt één kostprijsberekeningsversie gebruikt die alle kostenregistraties bevat. Deze registraties omvatten de oorspronkelijke koten en alle kostenupdates.

Bij de methode met twee versies wordt één versie gebruikt die registraties van de oorspronkelijke kosten bevat en een tweede versie die registraties alle van kostenupdates bevat. Het belangrijkste voordeel van de methode met twee versies is de duidelijke afbakening en tracering van kostenupdates in een aparte kostprijsberekeningsversie, zonder dat dit gevolgen heeft voor de oorspronkelijke kostprijsberekeningsversie. De methode met twee versies kan worden gebruikt om meerdere incrementele updates te identificeren, waarbij elke incrementele update een aparte kostprijsberekeningsversie heeft die de incrementele kostenrecords bevat.

## <a name="example"></a>Voorbeeld

Het volgende voorbeeld illustreert hoe de methoden met één versie en met twee versies kunnen worden gebruikt voor het bijwerken van standaardkosten in een productieomgeving. Bijvoorbeeld updates die nieuwe artikelen of foutcorrecties weerspiegelen. Ga ervanuit dat één kostprijsberekeningsversie de standaardkosten voor het huidige jaar voorstelt. De id voor deze versie is 2020-STD. Versie 2020-STD bevat de huidige actieve kosten voor alle artikelen. Bovendien bevat ze alle route-gerelateerde kostencategorieën en overheadberekeningsformules die aan het begin van het jaar 2020 bekend waren. 2020-STD is de oorspronkelijke kostprijsberekeningsversie.

- **Methode met één versie voor updates van kostengegevens** − In de methode met één versie, bevat de oorspronkelijke kostprijsberekeningsversie 2020-STD alle kostenregistraties. Kostenupdates worden in 2020-STD vastgelegd en de status ervan wordt ingesteld op In behandeling. De kosten in behandeling kunnen handmatig worden ingevoerd voor een nieuw inkoopartikel of kunnen worden berekend voor een geproduceerd artikel om correcties weer te geven. Wanneer de methode met één versie wordt gebruikt, vereisen de stuklijstberekeningen geen terugvalgegevensbron, omdat alle actieve kosten in de kostprijsberekeningsversie zijn opgenomen. Nadat de kosten in behandeling actief worden, bevat de oorspronkelijke kostprijsberekeningsversie 2020-STD opnieuw alle huidige actieve kosten.
- **Methode met twee versies voor updates van kostengegevens** − De methode met twee versies vereist een extra kostprijsberekeningsversie die alleen de kostenupdates bevat. De id voor deze versie is 2020-STD-WIJZIGINGEN. Kostenupdates worden in 2020-STD-WIJZIGINGEN vastgelegd en de status ervan wordt ingesteld op In behandeling. Bij de methode met twee kostprijsberekeningsversies vereisen de stuklijstberekeningen van wachtende kosten voor gefabriceerde artikelen een terugvalgegevensbron. Dit is zo omdat de extra kostprijsberekeningsversie 2020-STD-WIJZIGINGEN alleen een subset van kostengegevens bevat. De terugval kan worden uitgedrukt als de actieve kosten, of als de opgegeven kostprijsberekeningsversie 2020-STD, omdat beide de bron van kostengegevens identificeren wanneer die niet bestaat in 2020-STD-WIJZIGINGEN. Nadat de kosten in behandeling zijn geactiveerd, bevat de kostprijsberekeningsversie 2020-STD-WIJZIGINGEN de huidige actieve kosten die de updates weergeven, terwijl de oorspronkelijke kostprijsberekeningsversie 2020-STD niet wordt beïnvloed. Bij de methode met twee kostprijsberekeningsversies worden updates voorkomen door blokkeringsbeleid voor de oorspronkelijke kostprijsberekeningsversie. De extra kostprijsberekeningsversie moet precies hetzelfde blokkeringsbeleid hebben als de oorspronkelijke kostprijsberekeningsversie, met uitzondering van de opgegeven begindatum en het selectieve gebruik van blokkeringsbeleid om updates toe te staan. De opgegeven begindatum moet bij elke batch wijzigingen worden bijgewerkt om de geplande activeringsdatum te reflecteren.

In het voorgaande voorbeeld werd één extra kostprijsberekeningsversie gebruikt om updates tijdens het jaar 2020 te beheren. Er kan meer dan een extra kostprijsberekeningsversie worden gebruikt, bijvoorbeeld een aparte versie voor elke batch met updates. Wanneer meer dan één extra kostprijsberekening wordt gebruikt, dan moet de terugval worden uitgedrukt als de actieve kosten, omdat de actieve kosten over meerdere kostprijsberekeningsversies zijn verdeeld.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Financiële dimensies voor de standaardkostenherwaardering

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Wanneer een nieuwe standaardprijs wordt geactiveerd, wordt de waarde van de voorhanden voorraad doorgaans geherwaardeerd met de transacties voor standaardkostenherwaardering. De financiële dimensies van het artikel worden vervolgens gewoonlijk geboekt op de transacties. Als u echter wilt bepalen of en hoe de financiële dimensies worden geboekt, gebruikt u [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de functie met de naam *Opties voor standaard financiële dimensies voor de standaardherwaardering van de kosten van de voorraad* in te schakelen. Nadat u deze functie hebt ingeschakeld, gaat u naar **Kostenbeheer > Instelling voor boekhoudingbeleid voorraad > Parameters** en stelt u de nieuwe vervolgkeuzelijst **Oorsprong van financiële dimensie** in op een van de volgende waarden:

- **Geen**: er worden geen financiële dimensies geboekt op de herwaarderingstransacties. Als u een vereiste financiële dimensie hebt in uw rekeningstructuur, wordt het herwaarderingsproces nog steeds uitgevoerd, maar worden boekhoudvermeldingen gemaakt die geen financiële dimensies hebben. In dit geval ontvangen gebruikers eerst een waarschuwingsbericht, zodat ze de herwaardering zo nodig kunnen annuleren.
- **Tabel**: de financiële dimensies van het artikel worden geboekt op de herwaarderingstransacties. Dit is de standaardinstelling en is consistent met het oorspronkelijke systeemgedrag zonder de functie *Opties voor standaard financiële dimensies voor de standaardherwaardering van de kosten van de voorraad* in te schakelen.
- **Boeking**: de financiële dimensies van de geherwaardeerde transactie worden geboekt op de herwaarderingstransacties. Standaard worden de financiële dimensies van de voorraadrekening van de oorspronkelijke transactie gebruikt voor zowel de voorraadrekening als de herwaarderingsrekening.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]