---
title: Fouten in de boeking van het overzicht als gevolg van niet-beschikbare voorraad of updateconflicten
description: Dit artikel biedt mogelijke oplossingen voor voorraadgerelateerde problemen tijdens het boeken van overzichten in Microsoft Dynamics 365 Commerce.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887625"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Fouten in de boeking van het overzicht als gevolg van niet-beschikbare voorraad of updateconflicten

[!include [banner](../../includes/banner.md)]

Dit artikel biedt mogelijke oplossingen voor voorraadgerelateerde problemen tijdens het boeken van overzichten in Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Description

Tijdens het boeken van Commerce-transacties kunt u foutberichten ontvangen die te maken hebben met voorraadproblemen of updateconflicten.

### <a name="inventory-issues-error-message"></a>Foutbericht voorraadproblemen

Als er voorraadproblemen zijn, ziet het foutbericht dat u ontvangt eruit als in dit voorbeeld:

> xx kan niet worden verzameld, omdat alleen yy uit voorraad beschikbaar is (zijn)

### <a name="update-conflict-error-messages"></a>Foutberichten voor updateconflicten

Het probleem updateconflict kan optreden wanneer de voorraadwaarderingsmethode *standaardkosten* of *zwevend gemiddelde* is. Aangezien beide methoden permanente kostprijsmethoden zijn, worden bij het boeken de uiteindelijke kosten bepaald.

Als u de methode *zwevend gemiddelde* gebruikt, lijkt het foutbericht dat u ontvangt over het updateconflict op dit voorbeeld:

> Voorraadwaarde xx,xx wordt niet verwacht na de berekening van proportionele onkosten

Als u de methode *standaardkosten* gebruikt, lijkt het foutbericht dat u ontvangt over het updateconflict op dit voorbeeld:

> De standaardkosten komen niet overeen met de financiële voorraadwaarde na het bijwerken. Waarde = xx,xx, Hoeveelheid = yy,yy, Standaardkosten = zz,zz

## <a name="resolutions"></a>Oplossingen

### <a name="workaround-for-the-inventory-error"></a>Oplossing voor de voorraadfout

U kunt de voorraadfout beperken door de voorraad voor het artikel handmatig bij te werken of door fysieke negatieve voorraad in te schakelen voor de artikelmodelgroep die is gekoppeld aan het artikel in Commerce Headquarters.

Voor een naadloze boekingservaring adviseert Microsoft negatieve fysieke voorraad voor de artikelmodelgroep in te schakelen. In sommige scenario´s kunnen negatieve overzichten alleen worden geboekt als negatieve fysieke voorraad is ingeschakeld.

Er is bijvoorbeeld geen voorraad beschikbaar voor een artikel, maar een kassamedewerker retourneert het artikel en voegt het vervolgens weer toe aan dezelfde transactie tegen een gereduceerde prijs om een prijsverschil te verwerken. In dit geval wordt zowel de retourtransactie als de verkooptransactie in hetzelfde overzicht opgenomen voor de enkele klantorder. Aangezien er echter geen garantie is dat de retourregel (waardoor de voorraad toeneemt) wordt geboekt voordat de verkoopregel wordt geboekt (waardoor de voorraad wordt verkleind) kunnen er voorraadfouten optreden. Als negatieve fysieke voorraad in dit scenario wordt ingeschakeld, wordt de transactieboeking niet negatief beïnvloed en wordt de voorraad in het systeem weergegeven.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Negatieve fysieke voorraad inschakelen voor een artikelmodelgroep

Als u negatieve fysieke voorraad voor een artikelmodelgroep in Commerce Headquarters wilt inschakelen, gaat u als volgt te werk.

1. Ga naar **Voorraadbeheer \> Instellen \> Voorraad**.
1. Selecteer de artikelmodelgroep in het navigatievenster aan de linkerkant.
1. Schakel in de sectie **Voorraadbeleid** onder **Negatieve voorraad** het selectievakje **Fysieke negatieve voorraad** in.

![Fysieke negatieve voorraad ingeschakeld.](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Oplossing voor de updateconflictfout

Zie voor mogelijke oplossingen om de updateconflictfout te corrigeren [Updateconflict opgetreden wanneer de voorraadwaarderingsmethode standaardkosten of zwevend gemiddelde is](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation).

> [!NOTE]
> Voor de updateconflictsfout hoeft u de klantorders die zijn gegenereerd met behulp van de samenvoegingsstap van de boeking, niet te verwijderen. Nadat u de voorgestelde oplossingen hebt geïmplementeerd, moet het overzicht worden geboekt als u de overzichtsboeking opnieuw wilt uitvoeren.
