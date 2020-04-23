---
title: Magazijnen voor overboekingsorders instellen
description: In dit onderwerp wordt beschreven hoe u magazijnen voor transferorders kunt instellen.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: aa5786df72f87da992f1020bbaaa1c2185adf043
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216707"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Magazijnen voor overboekingsorders instellen 

[!include [banner](../includes/banner.md)]

Met magazijnniveaus kunt u een hiërarchie maken die transferorders tussen magazijnen ondersteunt. Op basis van deze instelling worden met de hoofdplanning artikelbehoeften op het afzonderlijke magazijnniveau berekend en worden geplande transferorders vanuit een toegewezen bronmagazijn voor aanvullen gegenereerd.

1.  Klik op **Voorraadbeheer > Instellingen > Opsplitsing van voorraad > Magazijnen**.

2.  Selecteer het magazijn dat u wilt aanvullen.

3.  Kies op het sneltabblad **Hoofdplanning** het selectievakje **Aanvullen**.

4.  Selecteer in het veld **Hoofdmagazijn** het magazijn dat u wilt toewijzen als het magazijn voor aanvullen. Bij de hoofdplanning wordt een transferbehoefte voor het geselecteerde magazijn berekend en wordt een geplande transferorder vanuit het toegewezen **Hoofdmagazijn** gegenereerd.
   
    > [!NOTE]
    > <P>Als u het veld <STRONG>Aanvullen</STRONG> leegmaakt, wordt aan het geselecteerde magazijn een magazijnniveau met betrekking tot het <STRONG>Hoofdmagazijn</STRONG> toegewezen, maar wordt het <STRONG>Hoofdmagazijn</STRONG> niet als aanvullingsmagazijn ingesteld.</P>

5.  Sluit de pagina om de nieuwe instellingen toe te passen.


> [!TIP]
> <P>Als u een magazijn voor aanvullen wilt toewijzen, moet u eerst het magazijn in de pagina <STRONG>Opslagdimensiegroepen</STRONG> als een opslagdimensie instellen. Op deze pagina selecteert u het veld <STRONG>Actief</STRONG> en het veld <STRONG>Behoefteplan per dimensie</STRONG> voor het magazijn.</P>

## <a name="set-up-transport-lead-time"></a>Doorlooptijd voor transport instellen

U moet ook de doorlooptijd voor het transport tussen de magazijnen instellen op de pagina **Transportdagen**. 
1. Ga naar **Voorraadbeheer > instellingen > Distributie > Transportdagen**.
2. Selecteer in het veld **Plaats van ontvangst** **Magazijn**.
3. Selecteer het **Magazijn van verzending**, **Magazijn van ontvangst**, en **Transportdagen**. 
4. (Optioneel) U kunt ook de transporttijd, afhankelijk van de leveringsmethode, onder het tabblad **Transportdagen per leveringsmethode** instellen.
