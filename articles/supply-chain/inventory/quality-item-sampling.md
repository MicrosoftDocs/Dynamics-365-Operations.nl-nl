---
title: Artikelbemonstering voor kwaliteitsbeheer
description: In dit onderwerp wordt beschreven hoe u artikelbemonstering instelt.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956602"
---
# <a name="quality-management-item-sampling"></a>Artikelbemonstering voor kwaliteitsbeheer

Artikelbemonstering wordt gebruikt als onderdeel van een kwaliteitskoppeling. In de artikelbemonstering wordt het bedrag gedefinieerd van de huidige fysieke voorraad die moet worden geïnspecteerd. Bemonstering kan worden gebaseerd op een vaste hoeveelheid, een percentage of een volledige nummerplaat.

## <a name="set-up-item-sampling"></a>Artikelbemonstering instellen

Ga als volgt te werk om artikelbemonstering in te stellen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Artikelbemonstering**.
1. Selecteer **Nieuw**.
1. Voer een waarde in het veld **Artikelbemonstering** in.
1. Voer een waarde in het veld **Beschrijving** in.
1. Typ een getal in het veld **Waarde**. Deze waarde heeft betrekking op de waarde voor de hoeveelheidsspecificatie die in het aangrenzende veld is geselecteerd.
1. Schakel in de sectie **Proces** het selectievakje **Volledige blokkering** in als de hoeveelheid van de hele partij of de orderregel moet worden geblokkeerd als een test is mislukt. Als dit selectievakje is uitgeschakeld, worden alleen de artikelen in de kwaliteitsorder geblokkeerd als een test is mislukt.
1. Selecteer **Opslaan**.
1. Sluit de pagina.

> [!NOTE]
> Met de functie *Kwaliteitsbeheer voor magazijnprocessen* worden extra voorzieningen voor artikelbemonstering toegevoegd. Het concept van *artikelbemonsteringsbereik* wordt toegevoegd en u kunt een volledige nummerplaat als hoeveelheidsspecificatie definiëren. Als u deze functie hebt ingeschakeld, vindt u in [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md) meer informatie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
