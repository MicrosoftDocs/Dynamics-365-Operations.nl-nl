---
title: Facturen indienen bij het werkstroomsysteem en productontvangstbonregels koppelen
description: In dit artikel wordt het proces uitgelegd van het indienen van leveranciersfacturen bij het werkstroomsysteem en het automatisch vereffenen van geboekte productontvangstbonregels met leveranciersfacturen.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 960a08eb5e98cac034bbd41335b616ff41bf6fd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861613"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Facturen indienen bij het werkstroomsysteem en productontvangstbonregels koppelen

[!include [banner](../includes/banner.md)]

In dit artikel wordt het proces uitgelegd van het indienen van leveranciersfacturen bij het werkstroomsysteem en het automatisch vereffenen van geboekte productontvangstbonregels met leveranciersfacturen.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Ggeïmporteerde leveranciersfacturen indienen bij het werkstroomsysteem en geboekte productontvangstbonregels vereffenen met leveranciersfactuurregels die in behandeling zijn

Als onderdeel van een contactloos factureringsproces van Leveranciers kan een geïmporteerde factuur automatisch worden ingediend bij het werkstroomsysteem. U kunt het proces voor het indienen van geïmporteerde facturen naar het werkstroomsysteem configureren op het tabblad **Automatisering van leveranciersfacturering** van de pagina **Parameters van module Leveranciers** (**Leveranciers \> Instellen \> Parameters van module Leveranciers**). Het proces voor indiening bij de werkstroom wordt op de achtergrond uitgevoerd met een frequentie die u (per uur of per dag) opgeeft.

Wanneer u automatisch facturen naar het werkstroomsysteem verzendt, moet u beginnen met een geïmporteerde factuur. Om ervoor te zorgen dat de factuur vanaf het begin tot het einde zonder handmatige interventie kan worden verwerkt, moet u een geautomatiseerde boekingstaak opnemen in de werkstroomconfiguratie. Facturen die gerelateerd zijn aan inkooporders (IO's) en facturen die een niet-IO-inkoopcategorie en niet-voorraadregels bevatten, kunnen automatisch bij het werkstroomsysteem worden ingediend. Facturen die handmatig worden ingevoerd, moeten handmatig naar het werkstroomsysteem worden verzonden.

De waarde **Ingediend door** in de werkstroom is de gebruikers-id die is ingevoerd voor de achtergrondtaak **Leveranciersfacturen indienen bij werkstroom** op de pagina **Procesautomatisering**. De gebruiker die deze gebruikers-id heeft, kan de factuur indien nodig intrekken van het werkstroomsysteem.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Geboekte productontvangstbonnen vereffenen met factuurregels die een drieweg-overeenstemmingsbeleid hebben

Als onderdeel van een contactloos proces voor leveranciersfacturering kan het systeem automatisch de geboekte productontvangstbonnen vereffenen met factuurregels. Voor deze taak moet een drieweg-overeenstemmingsbeleid worden gedefinieerd. Deze functie is beschikbaar als de functie **Automatisering van leveranciersfacturering** is ingeschakeld op de pagina **Functiebeheer**.

Het vereffeningsproces wordt uitgevoerd totdat de hoeveelheid van de vereffende productontvangstbonnen gelijk is aan de factuurhoeveelheid. Als er echter meerdere productontvangsten zijn voor één factuurregel, moet u het proces meerdere keren uitvoeren om de volledige hoeveelheid te vereffenen. U kunt het maximum aantal keren opgeven dat het systeem moet proberen de productontvangstbonnen aan een factuurregel te koppelen voordat wordt geconcludeerd dat het proces is mislukt. Het proces wordt op de achtergrond uitgevoerd, elk uur of per dag. 

U kunt het geautomatiseerde vereffeningsproces uitvoeren als onderdeel van het proces voor het indienen van facturen bij het werkstroomsysteem. U kunt het ook als een zelfstandig proces uitvoeren. De instellingen voor het proces voor vereffening van productontvangstbonnen met factuurregels worden geconfigureerd op het tabblad **Automatisering van leveranciersfacturering** van de pagina **Parameters van module Leveranciers** (**Leveranciers \> Instellen \> Parameters van module Leveranciers**).

Factuurregels met een drieweg-overeenstemmingsbeleid waarbij de hoeveelheid op de afgestemde ontvangst kleiner is dan de factuurhoeveelheid, worden opgenomen in het proces voor automatische afstemming met productontvangstbonnen.

Als u de status **Laatste overeenkomst** wilt weergeven voor facturen die geen deel uitmaken van het geautomatiseerde proces voor indiening bij de werkstroom, opent u de factuur vanaf de pagina **Leveranciersfacturen**. Wanneer u de factuur bekijkt, worden de overeenkomende validatiegegevens bijgewerkt. De status **Laatste overeenkomst** kan automatisch worden bijgewerkt met de achtergrondtaak **Factuurvereffening valideren**. U kunt het proces van het automatisch bijwerken van de status **Laatste overeenkomst** op het tabblad **Achtergrondprocessen** van de pagina **Procesautomatiseringen** (**Systeembeheer \> Instellingen \> Procesautomatiseringen**).

Een factuurregel wordt van de geautomatiseerde verwerking uitgesloten als aan een van de volgende voorwaarden is voldaan:

- De waarde **Afstemmingsstatus van automatische ontvangst** van de factuurregel is **Mislukt**.
- De factuur wordt gebruikt.
- De factuur bevindt zich in het werkstroomsysteem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
