---
title: Magazijnen voor overboekingsorders instellen
description: In dit onderwerp wordt beschreven hoe u magazijnen voor overboekingsorders kunt instellen.
author: Mirzaab
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 9e4ea0f9720bd4e5d2724b507aa32525ac25fa52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823210"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Magazijnen voor overboekingsorders instellen 

[!include [banner](../includes/banner.md)]

Met magazijnniveaus kunt u een hiërarchie maken die overboekingsorders tussen magazijnen ondersteunt. Op basis van deze instelling worden met de hoofdplanning artikelbehoeften op het afzonderlijke magazijnniveau berekend en worden geplande overboekingsorders vanuit een toegewezen bronmagazijn voor aanvullen gegenereerd.

1.  Klik op **Voorraadbeheer > Instellingen > Opsplitsing van voorraad > Magazijnen**.

2.  Selecteer het magazijn dat u wilt aanvullen.

3.  Kies op het sneltabblad **Hoofdplanning** het selectievakje **Aanvullen**.

4.  Selecteer in het veld **Hoofdmagazijn** het magazijn dat u wilt toewijzen als het magazijn voor aanvullen. Bij de hoofdplanning wordt een transferbehoefte voor het geselecteerde magazijn berekend en wordt een geplande overboekingsorder vanuit het toegewezen **Hoofdmagazijn** gegenereerd.
   
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]