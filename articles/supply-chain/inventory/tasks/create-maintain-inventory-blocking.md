---
title: Een voorraadblokkering maken en beheren
description: In dit onderwerp wordt beschreven hoe u met een voorraadblokkering voorkomt dat fysieke voorhanden voorraad wordt gereserveerd door andere uitgaande brondocumenten.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956153"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Een voorraadblokkering maken en beheren

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u met een voorraadblokkering voorkomt dat fysieke voorhanden voorraad wordt gereserveerd door andere uitgaande brondocumenten. Voordat u met deze procedure begint, moet u een artikel met fysieke, beschikbare voorhanden voorraad hebben.

## <a name="block-inventory"></a>Voorraad blokkeren

Volg deze stappen om een voorraadblokkeringsrecord te maken zodat voorraad wordt geblokkeerd.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Voorraadblokkering**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de header van de nieuwe blokkeringsrecord het veld **Artikelnummer** in op het artikel dat u wilt blokkeren en voer een beschrijving in.
1. Typ op het sneltabblad **Algemeen** in het veld **Hoeveelheid** het aantal in dat u wilt blokkeren van het artikel.
1. Geef op het sneltabblad **Voorraaddimensies** de locatie en het magazijn op waar de artikelen zich momenteel bevinden die u wilt blokkeren.
1. Selecteer **Opslaan** in het actievenster.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>De voorwaarden van de voorraadblokkering bijwerken

Volg deze stappen om een voorraadblokkeringsrecord bij te werken.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Voorraadblokkering**.
1. Selecteer in het lijstvenster de betreffende blokkeringsrecord.
1. Bewerk de record waar nodig. U kunt bijvoorbeeld de waarde van het veld **Verwachte datum** wijzigen om aan te geven wanneer de geblokkeerde voorraad naar verwachting beschikbaar komt voor reservering. Als de optie **Verwachte ontvangsten** is geselecteerd, wordt de datum bij de verwachte transactie weergegeven. (De optie **Verwachte ontvangsten** is standaard geselecteerd wanneer u handmatig een blokkeringsrecord maakt.)
1. Selecteer **Opslaan** in het actievenster.

## <a name="unblock-inventory"></a>Voorraad deblokkeren

Volg deze stappen om een voorraadblokkeringsrecord te verwijderen, zodat voorraad wordt vrijgegeven.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Voorraadblokkering**.
1. Selecteer in het lijstvenster de betreffende blokkeringsrecord.
1. Selecteer in het actievenster **Verwijderen**.
1. U wordt gevraagd om de bewerking te bevestigen. Selecteer **Ja** om door te gaan.
1. Sluit de pagina.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
