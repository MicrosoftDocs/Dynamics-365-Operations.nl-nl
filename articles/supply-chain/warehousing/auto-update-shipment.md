---
title: Zendingen automatisch bijwerken
description: Dit onderwerp biedt een overzicht van de functionaliteit waarmee zendingen automatisch worden bijgewerkt.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6215bc21bd3ee377274556f09ba29231118e5002
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201359"
---
# <a name="shipment-auto-updates"></a>Zendingen automatisch bijwerken

[!include [banner](../includes/banner.md)]

De functie voor het automatisch bijwerken van zendingen werkt automatisch de hoeveelheden (zowel toe- als afname) bij op een ladingsregel die aan een zending is gekoppeld, nadat de lading aan een magazijn is vrijgegeven. Deze functionaliteit blijft ingeschakeld totdat de ladingsregel voor de verzending of lading wordt verwerkt in een wave. Wanneer de update wordt gebruikt, kunnen orderupdates automatisch doorstromen naar het magazijn, zonder dat er handmatig magazijntaken worden gemaakt.

Wanneer de functie voor het automatisch bijwerken van zendingen niet wordt gebruikt, worden alleen afnames van de hoeveelheid automatisch doorgestuurd totdat het magazijnwerk is gemaakt. Gebruikers moeten regels handmatig bijwerken of verwijderen en ze moeten vervolgens de regels opnieuw vrijgeven als er orderhoeveelheden worden verhoogd of als er nieuwe orderregels worden toegevoegd. Met de functie voor het automatisch bijwerken van zendingen kunnen bedrijven naadloos updates aan het magazijn doorgeven zonder bang te hoeven zijn dat bijbehorende verzendingen en ladingen niet overeenkomen met de orderregelupdates.

De functie voor het automatisch bijwerken van zendingen is van toepassing op zowel verkooporderregels als transferorderregels en wordt ingeschakeld voor een specifiek magazijn. Daarom kunnen bedrijven een ander beleid voor het automatisch bijwerken van zendingen toepassen voor een magazijn, als dat nodig is. Het beleid voor het automatisch bijwerken van de hoeveelheid wordt standaard toegepast voor alle magazijnen die gebruikmaken van magazijnbeheerprocessen. Wanneer deze standaardbeleidsinstelling wordt gebruikt, worden alleen afnames van de hoeveelheid automatisch doorgegeven aan een zending en lading totdat het magazijnwerk wordt gemaakt. Dit gedrag is hetzelfde als werd gebruikt voordat de functie voor automatische zendingupdates werd geïntroduceerd.

## <a name="main-elements-of-the-functionality"></a>Hoofdelementen van de functionaliteit

De functie voor het automatisch bijwerken van zendingen is met name afhankelijk van de verzendstatus om te bepalen of de hoeveelheid op een laadregel moet worden gewijzigd wanneer een wijziging wordt aangebracht op een verkooporderregel of transferorderregel. De functie werk ook primair met de status van de zending om te bepalen wanneer een nieuwe laadregel automatisch moet worden toegevoegd aan een bestaande lading. Wanneer de status van de zending **In wave** of hoger is, vindt er geen automatische update plaats.

Er wordt ook rekening gehouden met de wavestatus voor automatische updates. Wanneer de wave die betrekking heeft op de ladingsregel, de status **Geblokkeerd**, **In uitvoering**, **Vrijgegeven**, **Orderverzameld** of **Verzonden** heeft, en een gebruiker de hoeveelheid op een ladingsregel probeert te verminderen ( via een vermindering van de hoeveelheid op de verkooporder regel of de transferorderregel), wordt het volgende foutbericht weer gegeven: "Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen". Ook wanneer de wave een van de eerder vermelde statussen heeft en een gebruiker de hoeveelheid van de ladingsregel indirect probeert te vergroten door de hoeveelheid op de verkooporder regel of de transferorderregel te verlagen, wordt de hoeveelheid op de ladingsregel niet automatisch verhoogd. In dit geval moet de ladingsregel handmatig worden bijgewerkt.

## <a name="scenarios"></a>Scenario's

De functie voor het automatisch bijwerken van zendingen ondersteunt vier scenario's: het toevoegen van een nieuwe orderregel, het vergroten van de hoeveelheid op een orderregel, het verlagen van de hoeveelheid op een orderregel en het verwijderen van een orderregel.

- **Een nieuwe orderregel toevoegen**: wanneer het veld **Zending automatisch bijwerken** op het sneltabblad **Magazijn** van de pagina **Magazijnen** (**Magazijnbeheer \> Instellingen \> Magazijn \> Magazijnen**) is ingesteld op**Altijd**, wordt de bestaande lading niet bijgewerkt als er een verzending is voor de order en er een nieuwe orderregel wordt toegevoegd aan een verkooporder of transferorder nadat er al een lading is gemaakt voor de verkooporder. Er wordt een nieuwe ladingsregel zonder verwijzing naar de bestaande lading gemaakt en aan de bestaande zending gekoppeld. De nieuwe regel wordt toegevoegd aan de lading en vrijgegeven.
- **De hoeveelheid op een orderregel verhogen**: wanneer het veld **Zending automatisch bijwerken** is ingesteld op **Altijd**, als er een zending bestaat voor de order en de hoeveelheid op een bestaande verkooporderregel of transferorderregel wordt verhoogd wanneer er al een lading is gemaakt voor de verkooporder, wordt de ladingsregel verhoogd met dezelfde hoeveelheid als de orderregel. Als de lading is vrijgegeven maar er geen werk is gemaakt, wordt de ladingsregel verhoogd met dezelfde hoeveelheid als de orderregel.
- **De hoeveelheid op een orderregel verlagen**: wanneer het veld **Zending automatisch bijwerken** is ingesteld op **Altijd** of op **Bij afname van hoeveelheid**, als er een verzending voor de order is en de hoeveelheid op een bestaande verkooporderregel of transferorderregel wordt verlaagd nadat er al een lading voor de verkooporder is gemaakt, wordt de hoeveelheid op de bijbehorende ladingsregel aangepast, tenzij de hoeveelheid op de ladingsregel al gelijk is aan of kleiner is dan de nieuwe hoeveelheid op de orderregel. In dat geval wordt de ladingsregel niet beïnvloed. Als de lading is vrijgegeven maar er geen werk is gemaakt, wordt de hoeveelheid op de bijbehorende ladingsregel aangepast, tenzij de hoeveelheid op de ladingsregel al gelijk is aan of kleiner is dan de nieuwe hoeveelheid op de orderregel. In dat geval wordt de ladingsregel wel beïnvloed.
- **Een orderregel verwijderen**: wanneer het veld **Zending automatisch bijwerken** is ingesteld op **Altijd** of op **Bij afname van hoeveelheid**, als de gebruiker probeert een orderregel te verwijderen waarvoor een ladingsregel bestaat, wordt een foutbericht weergegeven.

## <a name="example-scenario"></a>Voorbeeldscenario

Voor deze scenario moeten demogegevens worden geïnstalleerd en moet u het **USMF**-voorbeeld-gegevensbedrijf gebruiken.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>De functie voor automatische updates van zending inschakelen

Voer de volgende stappen uit om de functie voor automatische updates van zending in te schakelen.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
2. Selecteer magazijn **24**.
3. Wijzig in het sneltabblad **Magazijn** in het veld **Zending automatisch bijwerken** de waarde van **Bij afname van hoeveelheid** in **Altijd**.

Nadat u de waarde hebt gewijzigd in **Altijd**, worden alle verhogingen of afnames in de hoeveelheden op verkooporderregels en transferorderregels en eventuele toevoegingen van nieuwe regels weerspiegeld in zendingen en ladingen voor het geselecteerde magazijn, rekening houdend met de hierboven genoemde beperkingen.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>De wavesjabloon wijzigen zodat de ladingsregels niet automatisch worden verwerkt

Voer de volgende stappen uit om de wavesjabloon zo te configureren dat deze niet automatisch ladingsregels verwerkt.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
2. Selecteer wavesjabloon **24 Standaardverzending**.
3. Selecteer **Bewerken**.
4. Stel op het sneltabblad **Algemeen** de optie voor **Het maken van waves automatiseren** in op **Ja** en zorg ervoor dat alle andere opties zijn ingesteld op **Nee**.

Het is belangrijk dat er geen werk automatisch wordt gemaakt en vrijgegeven als onderdeel van het proces voor het maken van waves. Nadat het werk is gemaakt dat is gerelateerd aan de ladingsregel die is gemaakt voor de verkooporderregel, wordt de ladingsregel niet meer automatisch bijgewerkt als de hoeveelheid op de verkooporderregel wordt gewijzigd.

### <a name="create-a-sales-order"></a>Verkooporder maken

Volg de onderstaande stappen om een verkooporder te maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
2. Selecteer klant **US-003**.
3. Maak een regel voor artikelnummer **A0001**.
4. Voer een hoeveelheid van **10** in. (Zorg ervoor dat u magazijn **24** gebruikt.)
5. Selecteer **Opslaan**.
6. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**. Er worden een zending en een wave gemaakt.

Omdat u de wavesjabloon in de vorige procedure hebt gewijzigd, wordt er geen lading of werk gemaakt. De status van de zending is **Open** en de wavestatus is **Gemaakt**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>De hoeveelheid op een verkooporder verlagen

Voer de volgende stappen uit om de hoeveelheid op een verkooporderregel te verlagen.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
2. Selecteer de verkooporder die u net hebt vrijgegeven aan het magazijn.
3. Selecteer de verkooporderregel. Wijzig in het veld **Hoeveelheid** de waarde van **10** in **8**.
4. Selecteer vanuit de verkooporderregel **Magazijn \> Details van zending**. Op de pagina **Details van zending** op het sneltabblad **Ladingsregels** wordt de wijziging weergegeven in de hoeveelheid op de verkooporderregel.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>De hoeveelheid op een verkooporder verhogen

Voer de volgende stappen uit om de hoeveelheid op een verkooporderregel te verhogen.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
2. Selecteer de verkooporder die u eerder hebt vrijgegeven aan het magazijn.
3. Wijzig de regelhoeveelheid van **8** in **12**.
4. Selecteer **Opslaan**.
5. Ga terug naar de pagina **Alle verkooporders** en selecteer opnieuw de verkooporder.
5. Selecteer in het Actievenster op het tabblad **Magazijn** in de groep **Verwante informatie** de optie **Details van zending**. Op de pagina **Details van zending** op het sneltabblad **Ladingsregels** wordt de wijziging weergegeven in de hoeveelheid op de verkooporderregel.

Hoewel de hoeveelheid op de ladingsregel is verhoogd van 8 naar 12, worden er maar acht artikelen gereserveerd, tenzij automatische reservering is ingeschakeld. Omdat de hoeveelheid die aan de bestaande zending is toegevoegd, niet is gereserveerd, als de wave op dit punt wordt verwerkt zonder reservering, wordt alleen werk gemaakt voor de hoeveelheid die al is gereserveerd.

> [!NOTE]
> Wanneer de hoeveelheid op een orderregel afneemt, wordt de hoeveelheid op de ladingsregel niet beïnvloed als deze al gelijk is aan of kleiner is dan de nieuwe hoeveelheid op de orderregel. Wanneer de hoeveelheid op een orderregel wordt verhoogd, wordt de ladingsregel verhoogd met dezelfde hoeveelheid als de orderregel. Als de hoeveelheid op de orderregel verschilt van de hoeveelheid op de ladingsregel, blijft het verschil behouden.

### <a name="add-a-sales-order-line"></a>Een verkooporderregel toevoegen

Als u een verkooporderregel wilt toevoegen, volgt u deze stappen.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
2. Selecteer de verkooporder die u eerder hebt vrijgegeven aan het magazijn.
3. Maak een regel voor artikelnummer **A0002**.
4. Typ **10** in het veld **Hoeveelheid**. (Zorg ervoor dat u magazijn **24**gebruikt.) De nieuwe regel wordt automatisch aan de bestaande zending toegevoegd.
5. Selecteer **Opslaan**.
6. Ga terug naar de pagina **Alle verkooporders** en selecteer opnieuw de verkooporder.
7. Selecteer in het Actievenster op het tabblad **Magazijn** in de groep **Verwante informatie** de optie **Details van zending**. Op de pagina **Details van zending** op het sneltabblad **Ladingsregels** ziet u de tweede regel.

Omdat de verkooporderregel die u zojuist aan de bestaande zending hebt toegevoegd, niet is gereserveerd, wordt als de wave op dit punt wordt verwerkt, alleen werk gemaakt voor de hoeveelheid op de eerste verkooporderregel en de eerste ladingsregel.

### <a name="process-a-wave"></a>Een wave verwerken

Volg deze stappen om een wave te verwerken.

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
2. Selecteer de wave die u eerder hebt gemaakt.
3. Selecteer in het actievenster op het tabblad **Wave** in de groep **Wave** de optie **Verwerken**.

De wave wordt verwerkt en de hoeveelheid werk wordt gemaakt voor de gereserveerde hoeveelheden op de ladingsregels. De verzendstatus wordt bijgewerkt van **Geopend** naar **In wave**. Wanneer de verzendstatus wordt gewijzigd in **In wave**, hebben eventuele wijzigingen zoals het verminderen of verhogen van de regelhoeveelheden of het toevoegen van nieuwe regels aan de verkooporder, geen invloed op de bestaande ladingsregels die aan de wavezending zijn gekoppeld.

Als een verzending de status **In wave** of hoger heeft, worden updates van de hoeveelheid op een verkooporderregel niet weergegeven of gevalideerd op basis van een ladingsregel die aan de zending is gekoppeld. Wijzigingen in de hoeveelheid op een ladingsregel moeten direct op de ladingsregel worden aangebracht.

De validatie wordt uitgevoerd nadat het werk voor de ladingsregel is gemaakt en er een reservering is gemaakt. Een verlaging van de hoeveelheid op de verkooporderregel wordt vervolgens gevalideerd tegen de reservering van de werkregel.
