---
title: De indirecte wisselkoers opgeven
description: Dit onderwerp biedt informatie over indirecte wisselkoersen in Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46ac3324a985810ede61072190014538d0b7ed36f7eedfc387468619cc88cb2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737012"
---
# <a name="specify-the-cross-rate"></a>De indirecte wisselkoers opgeven

[!include [banner](../includes/banner.md)]

In dit hoofdstuk wordt het doel van een breed tarief uitgelegd en hoe dit brede tarief ingesteld kan worden bij het doen van een betaling via een factuur. Gebruik een breed tarief als alle van de volgende criteria van toepassing zijn: 
-   U vereffent een betaling met een factuur. 
-   De valuta´s van de betalingsregel en de factuurregel zijn verschillend. 
-   Geen van beide valuta´s is de valuta voor de boekhouding. 

De indirecte wisselkoers wordt niet gebruikt voor de omrekening van de betalingstransactievaluta naar de boekhoudvaluta van de betaling. In plaats daarvan worden de valutakoersen uit de wisselkoerstabellen opgehaald om de waarde te berekenen van het bedrag van de betalingstransactievaluta en het bedrag van de boekhoudvaluta. 

De boekhoudvaluta is bijvoorbeeld USD, de factuurvaluta is CAD en de betalingsvaluta is EUR. Met een breed tarief kunt u een wisselkoers invoeren die rechtstreeks tussen CAD en EUR vertaalt, waardoor er niet door USD vertaald hoeft te worden. Wanneer u een factuur en een primaire betaling selecteert, kunt u een indirecte wisselkoers invoeren voor de factuurregel. De indirecte wisselkoers is de wisselkoers tussen de valuta's voor de desbetreffende transacties, die geldt op de vereffeningsdatum.

1.  Ga naar een van de volgende pagina's:
- **Klanten > Algemeen > Klanten > Alle klanten** 
- **Leveranciers > Algemeen > Leveranciers > Alle leveranciers** 
- **Inkoop en sourcing > Algemeen > Leveranciers > Alle leveranciers**
2.  Selecteer de klant of leverancier van wie u de openstaande transacties vereffent. 
3.  Ga voor een klant op de lijstpagina **Alle klanten** naar **Verzamelen > Openstaande transacties vereffenen**. Ga voor een leverancier op de lijstpagina **Alle leveranciers** naar **Factuur > Openstaande transacties vereffenen**. 
4.  Selecteer de transactie die de primaire betaling vormt en klik vervolgens op **Betaling markeren**. Het selectievakje in de kolom **Markeren** is ingeschakeld en er wordt een informatiepictogram weergegeven in de kolom **Primaire betaling**. 
5.  Voer in het veld **Indirecte wisselkoers** de wisselkoers in tussen de factuurvaluta en de betalingsvaluta die geldt op de vereffeningsdatum. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]