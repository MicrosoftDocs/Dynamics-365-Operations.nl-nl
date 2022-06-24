---
title: Verbruiksrapporten maken
description: In dit artikel wordt uitgelegd hoe u rapporten over verbruik maakt in Activabeheer.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 136d6248db8012e5870e0627ddbd3703aa63703b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852895"
---
# <a name="create-consumption-reports"></a>Verbruiksrapporten maken

[!include [banner](../../includes/banner.md)]

 

Wanneer u verbruiksregistraties voor werkorders in Activabeheer hebt gemaakt en geboekt, zijn er twee rapporten beschikbaar om verbruiksgegevens weer te geven.


## <a name="asset-consumption-report"></a>Het rapport Activaverbruik

Wanneer u verbruik voor werkorders hebt geboekt, kunt u een verbruiksrapport voor activa afdrukken. In het rapport worden uren, uurkosten, artikelkosten en geboekte onkosten voor activa weergegeven.

1. Klik op **Activabeheer** > **Rapporten** > **Activa** > **Activaverbruik**.

2. Selecteer in het dialoogvenster **Activaverbruik** de parameters en het detailniveau dat u wilt zien door **Ja** te selecteren voor de relevante wisselknoppen en een niveau voor functionele locaties in de sectie **Weergeven** in te voegen.
    - U kunt het veld **Niveaus** gebruiken om aan te geven hoe gedetailleerd de regels voor activa moeten zijn met betrekking tot functionele locaties. 
    
        Als u bijvoorbeeld het getal 1 invoert in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activa voor een functionele locatie weergegeven op het hoogste niveau. Daarom kan een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. 
        
        Als u het getal 0 in het veld **Niveaus** invoert, wordt er een gedetailleerd resultaat met alle activa weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben. 
        
    - Selecteer **Ja** voor de wisselknop **Som van alle subactiva** als u de totalen voor elk subactivum in het rapport wilt weergeven.

3. Selecteer een datuminterval in de sectie **Datums**.

4. Geef op op het sneltabblad **Bestemming** op of u het rapport op het scherm wilt weergeven, wilt afdrukken of wilt opslaan als bestand of e-mailbericht.

5. U kunt zo nodig specifieke activa selecteren die in het rapport moeten worden weergegeven. Klik op het sneltabblad **Op te nemen records** op **Filter** en voeg de activa toe die u in het rapport wilt opnemen.

6. Klik op **OK** om het rapport te genereren.


## <a name="work-order-consumption-report"></a>Het rapport Werkorderverbruik

Wanneer u verbruik voor werkorders hebt geboekt, kunt u een verbruiksrapport voor werkorders afdrukken. In het rapport worden uren, uurkosten, artikelkosten en geboekte onkosten voor werkorders weergegeven.

1. Klik op **Activabeheer** > **Rapporten** > **Werkorders** > **Werkorderverbruik**.

2. Selecteer in het dialoogvenster **Werkorderverbruik** de parameters die u in het rapport wilt opnemen door **Ja** te selecteren voor de relevante wisselknoppen in de sectie **Weergeven**.

3. Selecteer een datuminterval in de sectie **Datums**.

4. Geef op op het sneltabblad **Bestemming** op of u het rapport op het scherm wilt weergeven, wilt afdrukken of wilt opslaan als bestand of e-mailbericht.

5. U kunt zo nodig specifieke werkorders selecteren die in het rapport moeten worden weergegeven. Klik op het sneltabblad **Op te nemen records** op **Filter** en voeg de werkorders toe die u in het rapport wilt opnemen.

6. Klik op **OK** om het rapport te genereren.


>[!NOTE]
>U kunt ook een [werkorderrapport](../work-orders/work-order-report.md) genereren dat meer werkordergegevens bevat.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]