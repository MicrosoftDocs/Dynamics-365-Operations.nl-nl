---
title: Facturen indienen bij het werkstroomsysteem en productontvangstbonregels aan factuurregels koppelen (preview)
description: In dit onderwerp wordt het proces uitgelegd van het indienen van leveranciersfacturen bij het werkstroomsysteem en het automatisch vereffenen van geboekte productontvangstbonregels met leveranciersfacturen.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cde164ee89b542d769d81d8d483049fb7ca001c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441805"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines-preview"></a>Facturen indienen bij het werkstroomsysteem en productontvangstbonregels aan factuurregels koppelen (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt het proces uitgelegd van het indienen van leveranciersfacturen bij het werkstroomsysteem en het automatisch vereffenen van geboekte productontvangstbonregels met leveranciersfacturen.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Ggeïmporteerde leveranciersfacturen indienen bij het werkstroomsysteem en geboekte productontvangstbonregels vereffenen met leveranciersfactuurregels die in behandeling zijn

Als onderdeel van een contactloos factureringsproces van Leveranciers kunt u het systeem automatisch een geïmporteerde factuur laten indienen bij het werkstroomsysteem. U kunt het proces voor het indienen van geïmporteerde facturen naar het werkstroomsysteem configureren op het tabblad **Automatisering van leveranciersfacturering** van de pagina **Parameters van module Leveranciers** (**Leveranciers \> Instellen \> Parameters van module Leveranciers**). Het proces voor indiening bij de werkstroom wordt op de achtergrond uitgevoerd met een frequentie die u (per uur of per dag) opgeeft.

Wanneer u automatisch facturen naar het werkstroomsysteem verzendt, moet u beginnen met een geïmporteerde factuur. Om ervoor te zorgen dat de factuur vanaf het begin tot het einde zonder handmatige interventie kan worden verwerkt, moet u een geautomatiseerde boekingstaak opnemen in de werkstroomconfiguratie. Facturen die gerelateerd zijn aan inkooporders (IO's) en facturen die een niet-IO-inkoopcategorie en niet-voorraadregels bevatten, kunnen automatisch bij het werkstroomsysteem worden ingediend. Facturen die handmatig worden ingevoerd, moeten handmatig naar het werkstroomsysteem worden verzonden.

De waarde **Ingediend door** in de werkstroom is de gebruikers-id die is ingevoerd voor de achtergrondtaak **Leveranciersfacturen indienen bij werkstroom** op de pagina **Procesautomatisering**. De gebruiker die deze gebruikers-id heeft, kan de factuur indien nodig terugroepen van het werkstroomsysteem.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Geboekte productontvangstbonnen vereffenen met factuurregels die een drieweg-overeenstemmingsbeleid hebben

Als onderdeel van een contactloos proces voor leveranciersfacturering kan het systeem automatisch de geboekte productontvangstbonnen vereffenen met factuu regels. Voor deze taak moet een drieweg-overeenstemmingsbeleid worden gedefinieerd. Deze functie is beschikbaar als de functie **Automatisering van leveranciersfacturering** is ingeschakeld op de pagina **Functiebeheer**.

Het proces wordt uitgevoerd totdat de hoeveelheid van de vereffende productontvangstbonnen gelijk is aan de factuurhoeveelheid. Als onderdeel van dit proces kunt u het maximum aantal keren opgeven dat het systeem moet proberen de productontvangstbonnen aan een factuurregel te koppelen voordat wordt geconcludeerd dat het proces is mislukt. Het proces wordt op de achtergrond uitgevoerd, elk uur of per dag. U kunt het geautomatiseerde vereffeningsproces uitvoeren als onderdeel van het proces voor het indienen van facturen bij het werkstroomsysteem. U kunt het ook als een zelfstandig proces uitvoeren. De instellingen voor het proces voor vereffening van productontvangstbonnen met factuurregels worden geconfigureerd op het tabblad **Automatisering van leveranciersfacturering** van de pagina **Parameters van module Leveranciers** (**Leveranciers \> Instellen \> Parameters van module Leveranciers**).

Factuurregels met een drieweg-overeenstemmingsbeleid waarbij de hoeveelheid op de afgestemde ontvangst kleiner is dan de factuurhoeveelheid, worden opgenomen in het proces voor automatische afstemming met productontvangstbonnen.

Als u de status **Laatste overeenkomst** wilt weergeven voor facturen die geen deel uitmaken van het geautomatiseerde proces voor indiening bij de werkstroom, opent u de factuur vanaf de pagina **Leveranciersfacturen**. Wanneer u de factuur bekijkt, worden de overeenkomende validatiegegevens bijgewerkt.

Een factuurregel wordt van de geautomatiseerde verwerking uitgesloten als aan een van de volgende voorwaarden is voldaan:

- De waarde **Afstemmingsstatus van automatische ontvangst** van de factuurregel is **Mislukt**.
- De factuur wordt gebruikt.
- De factuur bevindt zich in het werkstroomsysteem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]