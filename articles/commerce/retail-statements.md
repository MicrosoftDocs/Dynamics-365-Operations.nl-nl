---
title: Detailhandeloverzichten
description: In dit artikel wordt beschreven hoe overzichten worden gemaakt en geboekt.
author: ashishmsft
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0717c1198171f411e3c52233200ecfcc213dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878452"
---
# <a name="retail-statements"></a>Detailhandeloverzichten

[!include [banner](includes/banner.md)]

In Dynamics 365 Commerce wordt het boekingsproces voor overzichten gebruikt voor de transacties die plaats vinden in de Cloud POS of MPOS (Moderne POS). Het boekingsproces voor overzichten gebruikt de distributieplanning voor het ophalen van een set POS-transacties naar het hoofdkantoor (HQ) van de client. De parameters die zijn gedefinieerd op de pagina's **Commerce-parameters** en **Winkels**, worden gebruikt om de transacties te selecteren die worden opgehaald in afzonderlijke overzichten.

In het volgende illustratie geeft het overzichtboekingsproces weer. In dit proces worden transacties die zijn vastgelegd in de POS naar de client verzonden door de Commerce-planner te gebruiken. Nadat de client de transacties ontvangen heeft, kunt u het transactieoverzicht voor de winkel maken, berekenen en boeken.

[![Boekingsproces overzicht.](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Overzichten maken en boeken

U kunt overzichten handmatig maken of via ingestelde batchprocessen die u gedurende de dag periodiek uitvoert. In beide gevallen worden de volgende stappen gebruikt voor het maken en boeken van overzichten.

### <a name="create-the-statement"></a>U maakt het overzicht

In deze stap wordt de winkel aangeduid waarvoor het overzicht handmatig wordt gemaakt. Als u een batchproces configureert, kunt u automatisch voor alle winkels, op basis van een schema dat u definieert, overzichten maken.

### <a name="calculate-the-statement"></a>U berekent het overzicht

In deze stap worden de transactieregels geselecteerd op basis van criteria die voor iedere winkel zijn gedefinieerd op de pagina's **Commerce-parameters** en **Winkels**. Op deze pagina's stelt u de criteria in en bepaalt u hoe de transacties berekend worden. Voor het weergeven van een lijst met transacties die in het overzicht zijn opgenomen voordat u het overzicht berekent, gebruikt u de pagina **Transacties**.

In een overzicht worden kascontroles uit de kassa's gebruikt als het getelde bedrag. U kunt er ook voor kiezen om het getelde bedrag handmatig in te voeren. In het overzicht wordt het verschil weergegeven tussen het transactieverkoopbedrag en het werkelijk getelde bedrag van alle betalingsmethoden. Het overzicht wordt alleen geboekt, als dit verschil niet groter is dan het maximum dat voor de winkel voor het boeken van verschillen is gedefinieerd.

> [!NOTE]
> Het berekeningsproces voor het afschrift gebruikt de algemene nummerreeks.

Wanneer u een overzicht berekent, voert de berekening onder andere de volgende taken uit:

- Markeren van transacties die niet zijn opgenomen in een eerdere overzichtsberekening voor het geselecteerde datumbereik.
- Berekenen van de totale bedragen die zijn opgenomen in de geselecteerde transacties. De resultaten worden op de overzichtsregels weergegeven, afhankelijk van de methode voor het overzicht:

    - Als de overzichtsmethode **Totaal** is ingesteld, wordt er een regel gemaakt voor elke betalingsmethode in de geselecteerde transacties.
    - Als de overzichtsmethode **Personeel** is ingesteld, wordt er een regel gemaakt voor elke betalingsmethode in transacties die worden uitgevoerd door het geselecteerde personeelslid.
    - Als de overzichtsmethode **POS-terminal** is ingesteld, wordt er een regel gemaakt voor elke betalingsmethode in transacties die worden uitgevoerd op de geselecteerde kassa.
    - Als de overzichtsmethode **Dienst** is ingesteld, wordt er een regel gemaakt voor elke betalingsmethode in transacties die worden uitgevoerd gedurende een dienst.

Als het selectievakje **Splitsing per overzichtsmethode** is ingeschakeld op de pagina **Winkels**, wordt een afzonderlijk overzicht gemaakt op basis van de waarde die is geselecteerd in het veld **Overzichtsmethode**.

Als de openingstijden van uw winkel na middernacht liggen, kunt u overzichten boeken zo configureren dat het is gebaseerd op het einde van de werkdag in plaats van het einde van de kalenderdag.

Voer op de pagina **Winkels** op het sneltabblad **Overzicht/afsluiting** in het veld **Einde van werkdag** de tijd in waarop de laatste transactie vastgelegd moet worden om opgenomen te worden in het overzicht van de werkdag. Selecteer het selectievakje **Als werkdag boeken** voor het boeken van de transacties binnen dezelfde werkdag. Als het overzicht geboekt wordt, kunnen transacties die binnen dezelfde werkdag vastgelegd worden, opgenomen worden in dezelfde verkooporder. Dit kan zelfs als sommige transacties voor middernacht en andere transacties na middernacht plaatsvinden.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Voorbeeld: Boeken van een overzicht voor een werkdag die over twee kalenderdagen verdeeld is

Een winkel is geopend tussen 8:00 en 3:00 uur en het selectievakje **Als werkdag boeken** is ingeschakeld in de configuratie van de winkel. Op 31 mei legt winkel transacties vast tussen 8:00 uur en middernacht. De winkel registreert ook transacties tussen 0:01 uur en 3:00 uur op 1 juni.

Als de winkel haar overzicht boekt voor het einde van de werkdag, wordt de verkooporder gegenereerd waarin alle transacties zijn opgenomen die zijn vastgelegd tussen de openingstijden van 8:00 en 3:00 uur, ook al vonden de transacties plaats op twee dagen, 31 mei en 1 juni.

Als het selectievakje **Als werkdag boeken** is uitgeschakeld voor dezelfde winkel, worden er afzonderlijke verkooporders gegenereerd als de winkel haar overzicht boekt voor het sluiten van de werkdag. Eén verkooporder bevat transacties die zijn vastgelegd tussen de openingstijden 8:00 uur en middernacht op 31 mei, en een tweede verkooporder bevat transacties die zijn vastgelegd tussen 00:01 en 3:00 uur op 1 juni.

> [!NOTE]
> Voordat u de overzichten kunt maken, moet u de ploegen in de overzichtsperiode sluiten.

### <a name="post-the-statement"></a>U boekt het overzicht

Als u een overzicht boekt, worden verkooporders en facturen gemaakt voor de verkoop in het overzicht.

- Cash and carry-verkopen worden naar één verkooporder geaggregeerd en voor de standaardklant gefactureerd die is toegewezen aan de winkel.
- Verkopen waarvoor een klant was toegevoegd aan de transactie in POS genereren afzonderlijke verkooporders en facturen, één voor elke unieke klant.

Betalingsdagboeken worden automatisch gemaakt voor de betalingen in de instructie en de voorraad wordt bijgewerkt voor de POS-winkel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]