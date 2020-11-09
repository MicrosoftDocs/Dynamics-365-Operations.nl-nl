---
title: Instellingsopties voor de automatisering van leveranciersfacturering (preview)
description: In dit onderwerp worden de opties beschreven die beschikbaar zijn voor het instellen en configureren van automatisering van leveranciersfacturen.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: articl
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
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c3ee1112a409f87fdb433d5d43442a858dbd1798
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022585"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Instellingsopties voor de automatisering van leveranciersfacturering

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de opties beschreven die beschikbaar zijn voor het instellen en configureren van automatisering van leveranciersfacturen. Voor de functies voor automatisering van facturen worden de volgende typen instellingsparameters gebruikt:

- Parameters voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels met leveranciersfactuurregels die in behandeling zijn.
- Parameters voor achtergrondtaken voor procesautomatisering. Het raamwerk voor procesautomatisering wordt gebruikt om geïmporteerde leveranciersfacturen in te dienen bij het werkstroomsysteem. Het wordt ook gebruikt om geboekte productontvangstbonregels automatisch te vereffenen met leveranciersfactuurregels die in behandeling zijn. Verschillende bedrijfsprocessen gebruiken dit raamwerk om te definiëren hoe vaak het geselecteerde proces wordt uitgevoerd. De beschikbare frequenties voor de achtergrondprocessen **Productontvangst afstemmen met factuurregels** en **Leveranciersfacturen indienen bij werkstroom** omvatten **Uur** en **Dagelijks**.

Als u informatie over een achtergrondtaak wilt instellen of weergeven, gaat u naar **Systeembeheer \> Instellen \> Procesautomatiseringen** en selecteert u het tabblad **Achtergrondtaak**.

U moet een werkstroom voor leveranciersfacturen instellen om te zorgen voor een contactloze automatisering van het importproces via het boeken van leveranciersfacturen. Stel een werkstroom in door naar **Leveranciers > Instellen > Leverancierswerkstromen** te gaan. Om ervoor te zorgen dat de factuur vanaf het begin tot het einde zonder handmatige interventie kan worden verwerkt, moet u een geautomatiseerde boekingstaak opnemen in uw werkstroomconfiguratie. .

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parameters voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem

Er worden specifieke parameters gebruikt voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem. Bovendien worden bepaalde parameters gebruikt om geboekte productontvangstbonregels te vereffenen met leveranciersfactuurregels die in behandeling zijn. Op het tabblad **Automatisering van leveranciersfacturering** van de pagina **Parameters van module Leveranciers** worden de parameters die u moet instellen, verdeeld over de volgende secties:

- Werkstroom voor leveranciersfacturen
- Productontvangsten automatisch afstemmen

De volgende parameters zijn beschikbaar:

- **Automatisch geïmporteerde facturen indienen bij het werkstroomsysteem** : als u deze optie instelt op **Ja** , worden geïmporteerde facturen automatisch naar het werkstroomsysteem verzonden. Als deze optie is ingesteld op **Nee** , moeten facturen handmatig worden ingediend. Door deze optie op **Ja** in te stellen, maakt u via boeken een contactloos proces mogelijk vanuit de importresultaten.

    U kunt deze optie alleen instellen op **Ja** als er een actieve werkstroom voor leveranciersfacturen is ingesteld voor uw rechtspersoon. Stel een werkstroom in door naar **Leveranciers \> Instellen \> Leverancierswerkstroom** te gaan.

- **Productontvangstbonnen verrekenen met factuurregels vóór automatische indiening** : als u deze optie instelt op **Ja** , kan de geïmporteerde factuur pas automatisch worden ingediend bij het werkstroomsysteem als de hoeveelheid van de overeenkomende productontvangstbon gelijk is aan de factuurhoeveelheid. Als u deze optie instelt op **Ja** , wordt de automatische vereffening van geboekte productontvangstbonnen ingeschakeld voor factuurregels waarvoor een drieweg-overeenstemmingsbeleid is gedefinieerd. Dat proces wordt uitgevoerd totdat de hoeveelheid van de vereffende productontvangstbonnen gelijk is aan de factuurhoeveelheid. Op dat moment wordt de factuur automatisch naar het werkstroomsysteem verzonden.

    De optie 'Productontvangstbonnen afstemmen met factuurregels vóór automatische indiening' is alleen beschikbaar als de optie **Factuurvereffeningsvalidatie inschakelen** is ingeschakeld. Als deze optie is geselecteerd, wordt de optie **Productontvangstbonnen automatisch afstemmen met factuurregels** automatisch geselecteerd.

- **Vereisen dat de berekende totalen gelijk zijn aan geïmporteerde totalen voor het automatisch indienen van werkstromen** : als u deze optie instelt op **Ja** , kan de factuur pas automatisch naar het werkstroomsysteem worden verzonden als de totalen die voor de factuur zijn berekend, gelijk zijn aan de geïmporteerde totalen. Als deze optie is ingesteld op **Nee** , kan de factuur automatisch worden ingediend bij het werkstroomsysteem, maar kan deze pas worden geboekt als de berekende totalen zijn gecorrigeerd, zodat deze overeenkomen met de geïmporteerde totalen. Als u het factuurbedrag of het btw-bedrag niet importeert, moet u deze optie instellen op **Nee**.
- **Automatisch productontvangstbonnen afstemmen met factuurregels** : als u deze optie instelt op **Ja** , kan achtergrondverwerking worden gebruikt om de automatische vereffening van geboekte productontvangstbonnen uit te voeren voor factuurregels waarvoor een drieweg-overeenstemmingsbeleid is gedefinieerd. Dat proces wordt uitgevoerd totdat de hoeveelheid van de afgestemde productontvangstbon gelijk is aan de factuurhoeveelheid of totdat de waarde van het veld **Aantal keren dat wordt geprobeerd automatisch af te stemmen** wordt bereikt. Het proces kan worden uitgevoerd totdat de factuur is ingediend bij het werkstroomsysteem.

    Deze optie is alleen beschikbaar als de optie **Factuurvereffeningsvalidatie inschakelen** is geselecteerd.

    Als u de optie **Productontvangstbonnen afstemmen met factuurregels vóór automatische indiening** instelt op **Ja** , kan deze optie niet worden ingesteld op **Nee**. Als u deze optie instelt op **Nee** , moet u eerst de optie **Productontvangstbonnen afstemmen met factuurregels vóór automatische indiening** instellen op **Nee**.

- **Aantal keren dat wordt geprobeerd automatisch af te stemmen** : selecteer het aantal keren dat het systeem moet proberen de productontvangstbonnen aan een factuurregel te koppelen voordat wordt geconcludeerd dat het proces is mislukt. Wanneer het opgegeven aantal pogingen is bereikt, wordt de factuur verwijderd uit de automatiseringsverwerking.
- **Alleen valideren als de overeenkomende hoeveelheid op de productontvangstbon gelijk is aan de factuurhoeveelheid** : als u deze optie selecteert, wordt factuurvereffening alleen automatisch gevalideerd wanneer de overeenkomende hoeveelheid op de productontvangstbon van de factuurregel gelijk is aan de factuurhoeveelheid van de factuurregel. Als deze optie is uitgeschakeld, wordt factuurvereffening gevalideerd telkens wanneer het systeem automatisch overeenkomt met een productontvangstbon voor een factuurregel.
