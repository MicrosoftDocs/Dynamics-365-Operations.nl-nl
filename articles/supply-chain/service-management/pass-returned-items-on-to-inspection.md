---
title: Geretourneerde artikelen doorgeven voor inspectie
description: Bepaal bij het registreren van een geretourneerd artikel dat een artikel ter controle moet worden verzonden voordat het naar de voorraad wordt geretourneerd of op een andere manier wordt afgestoten.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 959df8e1ecbc493dc11e4793120f352b94b8b635
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676742"
---
# <a name="pass-returned-items-on-to-inspection"></a>Geretourneerde artikelen doorgeven voor inspectie 

[!include [banner](../includes/banner.md)]


Bij het registreren van een geretourneerd artikel kunt u ervoor kiezen een artikel ter controle te verzenden voordat het wordt geretourneerd naar de voorraad of op een andere manier wordt afgestoten.

1.  Ga naar **Voorraadbeheer** \> **Journaalposten** \> **Artikelontvangst** \> **Artikelontvangst**.
    
    \-of-
    
    Klik op **Voorraadbeheer** \> **Journaalen** \> **Artikelontvangst** \> **Productie-invoer**.

2.  Registreer de ontvangst van een artikel zoals gebruikelijk in het formulier **Locatiejournaal**.
    

    > [!NOTE]
    > <P>Zie voor informatie over het registreren van de ontvangst van geretourneerde artikelen <A href="register-the-receipt-of-returned-items.md">De ontvangst van geretourneerde artikelen registreren</A></P>



3.  Op het tabblad **Standaardwaarden** in het gebied **Verwerkingsmethode** schakelt u het vakje **Quarantainebeheer** in.

Er wordt automatisch een quarantaineorder gemaakt en de persoon of afdeling die controles uitvoert, reageert op deze order met het formulier **Quarantaineorder**.

## <a name="see-also"></a>Zie ook

[Retourartikelen aan een inspectie onderwerpen](take-returned-items-through-inspection.md)

[Opgeven op welke wijze retourartikelen moeten worden afgestoten](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]