---
title: Vaste ontvangstprijs
description: In dit artikel wordt uitgelegd hoe u vaste ontvangstprijzen kunt configureren en gebruiken in Microsoft Dynamics 365 Supply Chain Management.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 2630952f395d1a18202698b4d73b67ef4b760194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907575"
---
# <a name="fixed-receipt-price"></a>Vaste ontvangstprijs

[!include [banner](../includes/banner.md)]

**Vaste ontvangstprijs** is een optie die u kunt selecteren voor een artikelmodelgroep wanneer u een ander voorraadmodel gebruikt dan *Standaardkosten* of *Zwevend gewogen gemiddelde* gebruikt. In vroege versies van Microsoft Dynamics AX was deze optie genaamd **Standaardkosten**. De naam werd gewijzigd in **Vaste ontvangstprijs** toen het nieuwe voorraadmodel voor standaardkosten werd geïntroduceerd in Dynamics AX 2012. In dit artikel wordt uitgelegd hoe u vaste ontvangstprijzen kunt configureren en gebruiken in Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Vaste ontvangstprijzen

Wanneer u het selectievakje **Vaste ontvangstprijs** voor een artikel inschakelt op de pagina **Artikelmodelgroep**, wordt de ontvangstprijs gebruikt als standaardkosten voor de voorraadontvangst. Als de inkoopprijs en de standaardartikelkostprijs die voor een product zijn geconfigureerd niet overeenkomen, wordt het verschil geboekt naar de rekening **Winstrekening vaste ontvangstprijs** of **Verliesrekening vaste ontvangstprijs** en de verschuiving naar de rekening **Tegenrekening vaste ontvangstprijs** die u opgeeft op de pagina **Voorraadboekingsprofiel**.

Omdat de optie **Vaste ontvangstprijs** wordt gebruikt in combinatie met verschillende voorraadmodellen (zoals First In First Out (FIFO) Last In First Out (LIFO) en gewogen gemiddelde), worden met het proces *Voorraad afsluiten en aanpassen* nog steeds vereffeningen en correcties gemaakt volgens het voorraadprincipe dat u op de pagina **Artikelmodelgroep** selecteert. Correcties worden echter alleen aangebracht op uitgiften vanuit voorraad.

U hebt bijvoorbeeld een product geconfigureerd met een artikelmodelgroep waarvoor het veld **Voorraadmodel** is ingesteld op *FIFO* en de optie **Vaste ontvangstprijs** is geselecteerd. Wanneer u voorraad ontvangt via een inkooporder, wordt de voorraadwaarde ingesteld op de waarde van de standaard kostprijs van het artikel op het moment van de productontvangst. Als u de inkooporder factureert en de factuurprijs verschilt, wordt de standaard kostprijs van het vrijgegeven product naar de voorraadrekening geboekt. Het verschil wordt geboekt naar de winst- of verliesrekening van de vaste ontvangstprijs. Wanneer u het product later verkoopt of verbruikt, wordt het lopende gemiddelde voor het artikel gebruikt op het moment dat de verkooporderfactuur werd geboekt (tenzij u markering gebruikt).

Tijdens het proces *Voorraad afsluiten en aanpassen* wordt een vereffening gemaakt waarbij de eerste uitgifte wordt vereffend met de eerste ontvangst. Het verschil tussen de ontvangstprijs die is gebruikt voor de ontvangst en het lopende gemiddelde dat voor de uitgifte is gebruikt, wordt in een nieuw boekstuk geboekt.

## <a name="enable-fixed-receipt-prices"></a>Vaste ontvangstprijzen inschakelen

Als u vaste ontvangstprijzen voor een artikel wilt inschakelen, volgt u deze stappen.

1. Ga naar **Voorraadbeheer \> Instellen \> Voorraad \> Artikelmodelgroepen**.
2. Maak een nieuwe artikelmodelgroep of selecteer een bestaande modelgroep.
3. Schakel op het sneltabblad **Kostprijsmethode en kostenherkenning** het selectievakje **Vaste ontvangstprijs** in.

    > [!NOTE]
    > U kunt het selectievakje **Vaste ontvangstprijs** alleen inschakelen als het veld **Voorraadmodel** is ingesteld op *Standaardkosten* of *Zwevend gemiddelde*.

4. Sluit de pagina.

Nadat u de optie **Vaste ontvangstprijs** hebt ingeschakeld, moet u het voorraadboekingsprofiel met de volgende stappen bijwerken.

1. Ga naar **Voorraadbeheer \> Instellen \> Boeken \> Boeken**.
1. Selecteer op het tabblad **Inkooporder** in de kolom **Selecteren** de optie **Winstrekening vaste ontvangstprijs**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel de nieuwe rij zo in dat deze van toepassing is op de artikelmodelgroep waarvoor u vaste ontvangstprijzen hebt ingeschakeld en geef de hoofdrekening op die wordt gebruikt om winsten op basis van vaste ontvangstprijzen voor inkooporders te registreren. Configureer overige instellingen naar wens.
1. Selecteer **Verliesrekening vaste ontvangstprijs** in de kolom **Selecteren**. Voeg een nieuwe toe die van toepassing is op de artikelmodelgroep waarvoor u vaste ontvangstprijzen hebt ingeschakeld en geef de hoofdrekening op die wordt gebruikt om verliezen op basis van vaste ontvangstprijzen voor inkooporders te registreren. Configureer overige instellingen naar wens.
1. Selecteer **Tegenrekening vaste ontvangstprijs** in de kolom **Selecteren**. Voeg een nieuwe toe die van toepassing is op de artikelmodelgroep waarvoor u vaste ontvangstprijzen hebt ingeschakeld en geef de hoofdrekening op die wordt gebruikt om verschuivingen op basis van vaste ontvangstprijzen voor inkooporders te registreren. Configureer overige instellingen naar wens.
1. Selecteer op het tabblad **Voorraad** in de kolom **Selecteren** de optie **Winstrekening vaste ontvangstprijs**. Voeg een nieuwe toe die van toepassing is op de artikelmodelgroep waarvoor u vaste ontvangstprijzen hebt ingeschakeld en geef de hoofdrekening op die wordt gebruikt om winsten op basis van vaste ontvangstprijzen voor voorraad te registreren. Configureer overige instellingen naar wens.
1. Selecteer **Verliesrekening vaste ontvangstprijs** in de kolom **Selecteren**. Voeg een nieuwe toe die van toepassing is op de artikelmodelgroep waarvoor u vaste ontvangstprijzen hebt ingeschakeld en geef de hoofdrekening op die wordt gebruikt om verliezen op basis van vaste ontvangstprijzen voor voorraad te registreren. Configureer overige instellingen naar wens.

> [!NOTE]
> Het wordt meestal aangeraden om in de velden **Winstrekening vaste ontvangstprijs** en **Verliesrekening vaste ontvangstprijs** dezelfde hoofdrekening te gebruiken voor inkooporders en voorraad.

> [!IMPORTANT]
> Wanneer u de waarde in het veld **Prijs** op het sneltabblad **Kosten beheren** van de pagina **Vrijgegeven producten** wijzigt, wordt de voor voorhanden voorraad niet automatisch geherwaardeerd. Open als handmatige oplossing de pagina **Afsluiten en corrigeren** en selecteer **Correctie \> Voorhanden** in het actievenster. Selecteer vervolgens de artikelen die voorhanden zijn en pas deze aan de huidige prijs aan. Eén duidelijk voordeel van het gebruik van het voorraadmodel voor standaardkosten is dat de voorhanden voorraad automatisch wordt geherwaardeerd.
