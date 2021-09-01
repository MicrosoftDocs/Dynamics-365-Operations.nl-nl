---
title: Een order maken voor het vervangen van een artikel
description: Artikelvervangingsorders worden meestal gemaakt wanneer een product is geretourneerd en geïnspecteerd.
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57bbb8eb638b990914dc00f9700ff0c1925c48852862b02e09f3f26415d3e347
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745497"
---
# <a name="create-an-item-replacement-order"></a>Een order maken voor het vervangen van een artikel 

[!include [banner](../includes/banner.md)]


Artikelvervangingsorders worden meestal gemaakt wanneer een product is geretourneerd en geïnspecteerd. Als een artikel moet worden vervangen voordat deze is geretourneerd of als het oorspronkelijke artikel niet wordt geretourneerd, kunt u direct een artikelvervangingsorder maken nadat u een retourorder hebt gemaakt.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Een vervangingsorder maken nadat u een artikel ontvangt dat werd geretourneerd

1.  Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.

2.  Maak een nieuwe retourorder of selecteer een geretourneerde order in de lijst om het formulier **Retourorder - RMA-nummer: %1, %2** te openen.

3.  Klik op **Retourregel** en selecteer vervolgens **Vervangingsartikel**.

4.  Selecteer het artikel om het geretourneerde artikel te vervangen. Voer de artikelspecificaties in en klik op **Toepassen**.

5.  Klik op **Pakbon** om de pakbon te genereren voor de retourorder. Een verkooporder wordt gegenereerd voor het vervangende artikel dat u hebt geselecteerd.
    
    Nadat de verkooporder is gemaakt voor het vervangingsartikel, worden verkoopovereenkomsten automatisch doorzocht en als er een toepasselijke verkoopovereenkomst is, wordt deze toegepast op de verkooporder.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Een vervangingsorder maken voordat u een artikel ontvangt dat wordt geretourneerd

1.  Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.

2.  Maak een nieuwe retourorder of selecteer een retourorder in de lijst om het formulier **Retourorder - RMA-nummer: %1, %2** te openen.

3.  Klik op **Verkooporder zoeken** als u de verkooporder voor het geretourneerde artikel wilt identificeren. Vul het formulier **Verkooporder zoeken** in en klik vervolgens op **OK** om het formulier te sluiten en terug te keren naar het formulier **Retourorder - RMA-nummer: %1, %2**. De verkooporderregel voor het geretourneerde artikel wordt gekopieerd naar de retourorder.

4.  Klik op **Vervangingsorder** om het formulier **Verkooporder** te openen.

5.  Schakel het selectievakje **Retourorderregels kopiëren** in om de gegevens van de retourorder die u hebt geselecteerd in het formulier **Retourorder - RMA-nummer: %1, %2** te kopiëren naar deze verkooporder.

6.  Voer zo nodig gegevens in of wijzig deze.
    
    Als u de verkooporder in stap 3 hebt geïdentificeerd en als de verkooporderregel voor het geretourneerde artikel is gekoppeld aan een verkoopovereenkomst, wordt de id van de toepasselijke verkoopovereenkomst voor de artikelvervanging automatisch weergegeven in het veld **Verkoopovereenkomst-ID**.

7.  Klik op **OK** om het formulier **Verkooporder maken** te sluiten en het formulier **Verkooporder** te openen waar u kunt doorgaan met het invoeren van gegevens voor de nieuwe verkooporder. Toepasselijke retourorderregels worden gekopieerd naar de nieuwe verkooporder. 
    
    Als de id van de verkoopovereenkomst automatisch wordt weergegeven in het veld **Verkoopovereenkomst-ID**, is de verkoopovereenkomst gekoppeld aan de koptekst van de verkooporder voor het vervangingsorder voor het artikel. Als er een verbintenis van toepassing is in de verkoopovereenkomst die nog niet is voldaan en de verkooporder wordt gemaakt voordat de verkoopovereenkomst verloopt, wordt een koppeling gemaakt tussen de verkoopovereenkomstregel en de verkooporderregel. Daarom wordt informatie van de verkoopovereenkomst, zoals artikelprijs, gekopieerd naar de nieuwe verkooporderregel. 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]