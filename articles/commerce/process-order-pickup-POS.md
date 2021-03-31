---
title: Ophalen van klantorders in POS verwerken
description: In dit onderwerp wordt de functionaliteit uitgelegd die beschikbaar is in de POS-toepassing (Point of Sale) voor de verwerking van het ophalen van klantorders.
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e7df580557486c67fc82af19f742bc8002cb881
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231075"
---
# <a name="process-customer-order-pickups-in-pos"></a>Ophalen van klantorders in POS verwerken

[!include [banner](includes/banner.md)]

Wanneer een [klantorder](customer-orders-overview.md) wordt gemaakt om in de winkel op te halen, kan een winkelgebruiker de POS-toepassing gebruiken om het ophalen van voorraad te starten. In het POS wordt waar nodig de laatste betalingsvastlegging uitgevoerd. Daarnaast worden de voorraad en de financiële boeking voltooid voor de hoeveelheden die worden opgehaald.

Als u een winkelgebruiker bent, kunt u de ophaalbewerking uitvoeren met de bewerking **Order intrekken** of **Orderafhandeling** in het POS. U moet eerst een van de volgende stappen uitvoeren om de bewerking **Ophalen** beschikbaar te maken:

- Als u de bewerking **Order intrekken** wilt gebruiken, zoekt u naar de order en selecteert u de order die wordt opgehaald.
- Als u de bewerking **Orderafhandeling** wilt gebruiken, zoekt u naar een of meer orderregels en selecteert u deze.

Als de geselecteerde order of orderregels niet zijn geconfigureerd voor ophalen in die specifieke winkel of als de order al volledig is opgehaald, is de bewerking **Ophalen** niet beschikbaar.

![Ophaalbewerking](media/pickupoperation.png)

In Microsoft Dynamics 365 Commerce 10.0.17 en hoger kan de functie **Verbeterde gebruikerservaring voor de verwerking van afhaalorders in Point of Sale** worden ingeschakeld via Functiebeheer in Commerce Headquarters. Als deze functie is uitgeschakeld, kunnen gebruikers geen ophaalhoeveelheden selecteren. De volledige hoeveelheid die voor de regel is besteld, is standaard de hoeveelheid die wordt opgehaald. Deze ervaring kan problematisch zijn, omdat gebruikers kunnen vergeten om enkele artikelen voor ophalen te selecteren wanneer ze de ophaalbewerking uitvoeren via orderafhandeling.

De functie **Verbeterde gebruikerservaring voor de verwerking van afhaalorders in Point of Sale** geeft gebruikers meer controle over de selectie van producten die worden opgehaald en de hoeveelheid die wordt opgehaald. Gebruikers hoeven niet elke regel van de verkooporder op de pagina voor orderafhandeling te selecteren voordat ze **Ophalen** selecteren. Alle artikelen die kunnen worden opgehaald, worden weergegeven. Gebruikers kunnen meerdere regels voor ophalen opgeven, zelfs als er slechts één productregel is geselecteerd.

Wanneer de functie **Verbeterde gebruikerservaring voor de verwerking van afhaalorders in Point of Sale** wordt ingeschakeld en u de bewerking **Ophalen** selecteert, wordt het dialoogvenster **Ophalen** weergegeven. Hier kunt u de artikelen en hoeveelheden selecteren die worden opgehaald. Standaard wordt elke bestelde hoeveelheid met voorraad in een verzamelde of verpakte staat beschouwd als in aanmerking komend voor ophalen. Standaard wordt deze hoeveelheid ingesteld als ophaalhoeveelheid. U kunt de ingevoerde hoeveelheid wijzigen, als de hoeveelheid niet 0 (nul) is en de totale openstaande (niet-gefactureerde) hoeveelheid voor de geselecteerde regel niet wordt overschreden.

![Het dialoogvenster Ophalen](media/pickupselect.png)

Nadat u de hoeveelheden hebt geselecteerd die worden opgehaald en vervolgens **Ophalen** selecteert, wordt de transactiepagina weergegeven. Als de functie voor [betalingen voor meerdere kanalen](omni-channel-payments.md) is ingeschakeld er vooraf geautoriseerde creditcardbetalingen geregistreerd zijn, moet u de betaling toepassen.

Op de transactiepagina berekent het systeem de verschuldigde bedragen door het totaal te berekenen dat moet worden betaald voor de geselecteerde ophaalartikelen en vervolgens eventuele eerder toegepaste stortingen of geautoriseerde creditcardbetalingen af te trekken. U moet de betaling verwerken om de ophaaltransactie te voltooien. Als de [schermindeling](pos-screen-layouts.md) van de transactiepagina zo is geconfigureerd dat de bewerking **Transactie afsluiten** is opgenomen, zonder dat er een bedrag verschuldigd is, kunt u de transactie voltooien zonder een betaalwijze te selecteren. Als de bewerking **Transactie afsluiten** niet beschikbaar is, kunt u de **koppeling voor het verschuldigde bedrag van $ 0,00** in het deelvenster **Totalen** selecteren om de transactie af te sluiten zonder een betaalwijze te hoeven selecteren.

![Transactiepagina voor ophaaltransactie voor een klantorder](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Ophaalregels of -hoeveelheden wijzigen

Als u de ophaalhoeveelheid moet wijzigen nadat u de artikelen hebt geselecteerd die worden opgehaald, kunt u **Hoeveelheid instellen** selecteren. U kunt de ophaalhoeveelheid niet instellen op **0** (nul) of verhogen naar een waarde die hoger is dan de niet-gefactureerde hoeveelheid die overblijft voor de bestelde regel. Als u een ophaalregel uit het winkelwagentje voor de transactie wilt verwijderen, selecteert u **Ongeldig gemaakte transactie**. De huidige transactie wordt gestopt en de stroom voor de bewerking **Ophalen** wordt opnieuw gestart.

Als de functie **Verbeterde gebruikerservaring voor de verwerking van afhaalorders in Point of Sale** is ingeschakeld, kunnen organisaties een knop voor de bewerking **Ophaalregels wijzigen** toevoegen aan de schermindeling van de transactiepagina. Nadat u het winkelwagentje voor de ophaaltransactie in het POS hebt gemaakt en artikelen hebt geselecteerd, kunt u **Ophaalregels wijzigen** selecteren als u de ophaalartikelen moet wijzigen, maar niet de hele transactie ongeldig wilt maken. In het dialoogvenster **Ophaalregels wijzigen** dat verschijnt, kunt u de ophaalartikelen en -hoeveelheden wijzigen. Het winkelwagentje voor de transactie wordt vervolgens bijgewerkt om uw wijzigingen weer te geven.

![Het dialoogvenster Ophaalartikelen wijzigen](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]