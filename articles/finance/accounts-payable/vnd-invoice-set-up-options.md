---
title: Instellingsopties voor de automatisering van leveranciersfacturering (preview)
description: In dit onderwerp worden de opties beschreven die beschikbaar zijn voor het instellen en configureren van automatisering van leveranciersfacturen.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4411e2c6113c7e42abd4247f79c59ed2cc47c7af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248097"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Instellingsopties voor de automatisering van leveranciersfacturering

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de opties beschreven die beschikbaar zijn voor het instellen en configureren van automatisering van leveranciersfacturen. Voor de functies voor automatisering van facturen worden de volgende typen instellingsparameters gebruikt:

- Parameters voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem en het vereffenen van geboekte productontvangstbonregels met leveranciersfactuurregels die in behandeling zijn.
- Parameters voor procesautomatisering van achtergrondtaken. Het raamwerk voor procesautomatisering wordt gebruikt om geïmporteerde leveranciersfacturen in te dienen bij het werkstroomsysteem. Het wordt ook gebruikt om geboekte productontvangstbonregels automatisch te vereffenen met leveranciersfactuurregels in behandeling en om factuurvereffening te valideren voor handmatige facturen die automatisch aan productontvangstbonregels zijn gekoppeld. Verschillende bedrijfsprocessen gebruiken dit raamwerk om te definiëren hoe vaak het geselecteerde proces wordt uitgevoerd. De beschikbare frequenties voor de achtergrondprocessen **Productontvangst afstemmen met factuurregels** en **Leveranciersfacturen indienen bij werkstroom** omvatten **Uur** en **Dagelijks**.

Als u informatie over een achtergrondtaak wilt instellen of weergeven, gaat u naar **Systeembeheer \> Instellen \> Procesautomatiseringen** en selecteert u het tabblad **Achtergrondtaak**.

U moet een werkstroom voor leveranciersfacturen instellen om te zorgen voor een contactloze automatisering van het importproces via het boeken van leveranciersfacturen. Stel een werkstroom in door naar **Leveranciers > Instellen > Leverancierswerkstromen** te gaan. Om ervoor te zorgen dat de factuur vanaf het begin tot het einde zonder handmatige interventie kan worden verwerkt, moet u een geautomatiseerde boekingstaak opnemen in uw werkstroomconfiguratie.

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parameters voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem

Er worden specifieke parameters gebruikt voor het indienen van geïmporteerde leveranciersfacturen bij het werkstroomsysteem. Bovendien worden bepaalde parameters gebruikt om geboekte productontvangstbonregels te vereffenen met leveranciersfactuurregels die in behandeling zijn. Op het tabblad **Automatisering van leveranciersfacturering** van de pagina **Parameters van module Leveranciers** worden de parameters die u moet instellen, verdeeld over de volgende secties:

- Werkstroom voor leveranciersfacturen
- Productontvangsten automatisch afstemmen

De volgende parameters zijn beschikbaar:

- **Automatisch geïmporteerde facturen indienen bij het werkstroomsysteem**: als u deze optie instelt op **Ja**, worden geïmporteerde facturen automatisch naar het werkstroomsysteem verzonden. Als deze optie is ingesteld op **Nee**, moeten facturen handmatig worden ingediend. Door deze optie op **Ja** in te stellen, maakt u via boeken een contactloos proces mogelijk vanuit de importresultaten.

    U kunt deze optie alleen instellen op **Ja** als er een actieve werkstroom voor leveranciersfacturen is ingesteld voor uw rechtspersoon. Stel een werkstroom in door naar **Leveranciers \> Instellen \> Leverancierswerkstroom** te gaan.

- **Productontvangstbonnen verrekenen met factuurregels vóór automatische indiening**: als u deze optie instelt op **Ja**, kan de geïmporteerde factuur pas automatisch worden ingediend bij het werkstroomsysteem als de hoeveelheid van de overeenkomende productontvangstbon gelijk is aan de factuurhoeveelheid. Als u deze optie instelt op **Ja**, wordt de automatische vereffening van geboekte productontvangstbonnen ingeschakeld voor factuurregels waarvoor een drieweg-overeenstemmingsbeleid is gedefinieerd. Dat proces wordt uitgevoerd totdat de hoeveelheid van de vereffende productontvangstbonnen gelijk is aan de factuurhoeveelheid. Op dat moment wordt de factuur automatisch naar het werkstroomsysteem verzonden.

    De optie 'Productontvangstbonnen afstemmen met factuurregels vóór automatische indiening' is alleen beschikbaar als de optie **Factuurvereffeningsvalidatie inschakelen** is ingeschakeld. Als deze optie is geselecteerd, wordt de optie **Productontvangstbonnen automatisch afstemmen met factuurregels** automatisch geselecteerd.

- **Vereisen dat de berekende totalen gelijk zijn aan geïmporteerde totalen voor het automatisch indienen van werkstromen**: als u deze optie instelt op **Ja**, kan de factuur pas automatisch naar het werkstroomsysteem worden verzonden als de totalen die voor de factuur zijn berekend, gelijk zijn aan de geïmporteerde totalen. Als deze optie is ingesteld op **Nee**, kan de factuur automatisch worden ingediend bij het werkstroomsysteem, maar kan deze pas worden geboekt als de berekende totalen zijn gecorrigeerd, zodat deze overeenkomen met de geïmporteerde totalen. Als u het factuurbedrag of het btw-bedrag niet importeert, moet u deze optie instellen op **Nee**.
- **Automatisch productontvangstbonnen afstemmen met factuurregels**: als u deze optie instelt op **Ja**, kan achtergrondverwerking worden gebruikt om de automatische vereffening van geboekte productontvangstbonnen uit te voeren voor factuurregels waarvoor een drieweg-overeenstemmingsbeleid is gedefinieerd. Dat proces wordt uitgevoerd totdat de hoeveelheid van de afgestemde productontvangstbon gelijk is aan de factuurhoeveelheid of totdat de waarde van het veld **Aantal keren dat wordt geprobeerd automatisch af te stemmen** wordt bereikt. Het proces kan worden uitgevoerd totdat de factuur is ingediend bij het werkstroomsysteem.

    Deze optie is alleen beschikbaar als de optie **Factuurvereffeningsvalidatie inschakelen** is geselecteerd.

    Als u de optie **Productontvangstbonnen afstemmen met factuurregels vóór automatische indiening** instelt op **Ja**, kan deze optie niet worden ingesteld op **Nee**. Als u deze optie instelt op **Nee**, moet u eerst de optie **Productontvangstbonnen afstemmen met factuurregels vóór automatische indiening** instellen op **Nee**.

- **Aantal keren dat wordt geprobeerd automatisch af te stemmen**: selecteer het aantal keren dat het systeem moet proberen de productontvangstbonnen aan een factuurregel te koppelen voordat wordt geconcludeerd dat het proces is mislukt. Wanneer het opgegeven aantal pogingen is bereikt, wordt de factuur verwijderd uit de automatiseringsverwerking.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]