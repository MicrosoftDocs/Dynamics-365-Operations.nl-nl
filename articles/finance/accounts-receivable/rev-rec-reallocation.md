---
title: Hertoewijzing van opbrengsttoerekening
description: Dit artikel biedt informatie over hertoewijzing, waarmee organisaties opbrengstprijzen opnieuw kunnen berekenen wanneer de voorwaarden van een contractuele verkoop worden gewijzigd. Het bevat koppelingen naar andere onderwerpen waarin wordt beschreven hoe opbrengst in meerdere scenario's moet worden toegerekend.
author: kweekley
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a79288fd69a2e7780ff03952b05b99db2ed88e41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903415"
---
# <a name="revenue-recognition-reallocation"></a>Hertoewijzing van opbrengsttoerekening

[!include [banner](../includes/banner.md)]

Door middel van hertoewijzing kunnen organisaties opbrengstprijzen opnieuw berekenen wanneer de voorwaarden van een contractuele verkoop worden gewijzigd. Voor opbrengsttoerekening worden de verkooporderdocumenten als het contract beschouwd.

Uw organisatie moet zelf bepalen of hertoewijzing noodzakelijk is. De toevoeging van een nieuwe regel aan een verkooporder of de toevoeging van een nieuwe verkooporder voor een klant kan mogelijk niet als wijziging van het contract worden beschouwd. In de volgende scenario's is hertoewijzing mogelijk noodzakelijk:

- Een klant heeft artikelen aan een verkooporder toegevoegd of artikelen uit de verkooporder verwijderd nadat de order volledig of gedeeltelijk is gefactureerd.
- Er zijn meerdere verkooporders, bevestigd of gefactureerd, ingevoerd voor hetzelfde overeengekomen contract.
- Een klant heeft een krediet voor een artikel geretourneerd of ontvangen nadat de oorspronkelijke verkooporder volledig of gedeeltelijk is gefactureerd.

Er gelden enkele belangrijke beperkingen ten aanzien van het hertoewijzingsproces:

- Het proces kan maar één keer worden uitgevoerd. Het is daarom belangrijk dat u het pas uitvoert nadat alle wijzigingen zijn doorgevoerd.

    - Deze beperking wordt verwijderd in versie 10.0.17 en hoger.

- Het proces kan niet worden uitgevoerd voor projectverkooporders.

    - Deze beperking wordt verwijderd in versie 10.0.17 en hoger.

- Als het om meerdere verkooporders gaat, moeten deze voor dezelfde klantrekening bedoeld zijn.
- Alle verkooporders die opnieuw worden toegewezen, moeten in dezelfde transactievaluta zijn opgesteld.
- Het proces kan na uitvoering niet worden omgekeerd of ongedaan worden gemaakt.

    - Deze beperking wordt verwijderd in versie 10.0.17 en hoger.

- Hertoewijzing kan alleen worden uitgevoerd voor verkoop- of projectverkooporders, niet voor een combinatie van verkooporders en projectverkooporders.

    - Deze beperking wordt verwijderd in versie 10.0.17 en hoger.

## <a name="set-up-reallocation"></a>Hertoewijzing instellen

Eén parameter heeft invloed op het hertoewijzingsproces.

Omdat hertoewijzing kan worden uitgevoerd voor een verkooporder die gedeeltelijk of volledig is gefactureerd, moeten alle eerdere journaalregels voor de factuur worden gecorrigeerd op basis van de nieuwe, opnieuw toegewezen opbrengstprijzen. U kunt deze correctie uitvoeren door de journaalregel van de oorspronkelijke factuur om te keren en een nieuwe journaalregel te boeken die is gebaseerd op de opnieuw toegewezen opbrengstprijzen.

Elke organisatie moet bepalen of met de correctie alleen Grootboek of ook Klanten moet worden bijgewerkt. De uiteindelijke beslissing van de organisatie bepaalt de juiste instelling van de optie **Factuurcorrecties boeken naar Klanten** op het tabblad **Opbrengsttoerekening** van de pagina **Grootboekparameters** (**Opbrengsttoerekening \> Instellen \> Grootboekparameters**). De juiste instelling is afhankelijk van het specifieke scenario. Gebruik de koppelingen in de sectie [Scenario's voor hertoewijzing](#scenarios-for-reallocation) later in dit artikel voor meer informatie over mogelijke scenario's.

[![Het tabblad Opbrengsttoerekening op de pagina Grootboekparameters.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Als de optie **Factuurcorrecties boeken naar Klanten** is ingesteld op **Ja**, levert het hertoewijzingsproces het volgende resultaat op:

- In Klanten wordt een creditdocument gemaakt om de te corrigeren factuur terug te boeken.

    - In het creditdocument wordt het oorspronkelijke factuurnummer opnieuw gebruikt, maar hieraan wordt '-1' toegevoegd.
    - Het creditdocument wordt automatisch vereffend met de oorspronkelijke factuur. Als de oorspronkelijke factuur al is vereffend met een ander creditdocument of een andere betaling, wordt deze vereffening automatisch teruggeboekt.
    - Het creditdocument wordt naar Grootboek geboekt om de journaalregel terug te boeken die in de oorspronkelijke factuur is geboekt. De transactieposten Voorraad en Kosten van verkochte goederen worden echter niet teruggeboekt.

- In Klanten wordt een nieuwe factuur gemaakt die is gebaseerd op de nieuwe, opnieuw toegewezen prijsbedragen.

    - In de nieuwe factuur wordt het oorspronkelijke factuurnummer opnieuw gebruikt, maar hieraan wordt '-2' toegevoegd.
    - De nieuwe factuur wordt automatisch vereffend met eventuele creditdocumenten of betalingen die eerder zijn vereffend met de oorspronkelijke factuur.
    - De nieuwe factuur wordt naar Grootboek geboekt met de nieuwe, opnieuw toegewezen opbrengstprijsbedragen. De factuur wordt niet opnieuw naar de rekeningen voor voorraad en kosten van verkochte goederen geboekt omdat deze posten worden bijgehouden in de journaalregel van de oorspronkelijke factuur.

Als de optie **Factuurcorrecties boeken naar Klanten** is ingesteld op **Nee**, levert het hertoewijzingsproces het volgende resultaat op:

- Er wordt alleen een journaalregel voor terugboeking naar Grootboek geboekt. Alle boekhouding uit de oorspronkelijke factuur wordt teruggeboekt, met uitzondering van de journaalregels voor voorraad en kosten van verkochte goederen.
- Er wordt alleen een nieuwe journaalregel naar Grootboek geboekt, op basis van de nieuwe, opnieuw toegewezen opbrengstprijzen. De factuur wordt niet opnieuw naar de rekeningen voor voorraad en kosten van verkochte goederen geboekt omdat deze posten worden bijgehouden in de journaalregel van de oorspronkelijke factuur.
- De factuur op de pagina **Klanttransacties** wordt niet beïnvloed of gewijzigd, maar bevat nog steeds de oorspronkelijke journaalregel. Er is geen verwijzing naar de terugboekingsregels of nieuwe journaalregels.

Zoals aangegeven kunt u alleen Grootboek bijwerken of zowel Grootboek als Klanten bijwerken. Beide benaderingen bieden voor- en nadelen. We raden u aan om de vereisten van uw organisatie te beoordelen om te bepalen welke optie u moet gebruiken. Als u zowel Grootboek als Klanten bijwerkt, worden de juiste journaalregels weergegeven in de nieuwe factuur en kunnen ze worden weergegeven vanuit het document op de pagina **Klanttransacties**. Daarnaast worden tijdens het vereffeningsproces de bijgewerkte journaalregels gebruikt om contantkortingen en winst of verlies te boeken. Aan de andere kant worden het creditdocument en de nieuwe factuur weergegeven in klantoverzichten en ouderdomsrapporten, net als andere creditdocumenten en klantfacturen. De omschrijving van die documenten geeft aan dat ze zijn gemaakt via een boekhoudcorrectie.

## <a name="run-the-reallocation-process"></a>Het hertoewijzingsproces uitvoeren

U start het hertoewijzingsproces door **Prijs opnieuw toewijzen met nieuwe orderregels** te selecteren in een verkooporder die u opnieuw moet toewijzen. U kunt ook naar **Opbrengsttoerekening \> Periodieke taken \> Prijs opnieuw toewijzen met nieuwe orderregels** gaan en de juiste filters invoeren, zoals de klantrekening.

[![De pagina Prijs opnieuw toewijzen met nieuwe orderregels.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Het bovenste raster op de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** heeft de naam **Verkoop**. Hier worden de verkooporders voor de klant weergegeven. Selecteer de verkooporders die opnieuw moeten worden toegewezen. Als een verkooporder een hertoewijzings-id heeft, is deze al voor hertoewijzing gemarkeerd door een andere gebruiker. Als een of meer verkooporders eerder opnieuw zijn toegewezen en in een andere hertoewijzing moeten worden opgenomen, moet de hertoewijzing van die verkooporders eerst ongedaan worden gemaakt. Vervolgens kunnen die verkooporders worden opgenomen in een nieuwe hertoewijzing. Zie de secties [Een hertoewijzing ongedaan maken](#undo-a-reallocation) en [Meerdere keren opnieuw toewijzen](#reallocate-multiple-times) verderop in dit artikel voor meer gedetailleerde informatie.

Het onderste raster op de pagina heeft de naam **Regels**. Als u een of meer verkooporders in het raster **Verkoop** selecteert, worden de verkooporderregels weergegeven in het raster **Regels**. Selecteer de verkooporderregels die opnieuw moeten worden toegewezen. Als u slechts één verkooporder hebt geselecteerd, moeten regels in dezelfde verkooporder opnieuw worden toegewezen. Deze situatie kan zich voordoen wanneer een van de verkooporderregels eerder is gefactureerd en er vervolgens een nieuwe regel is toegevoegd of een bestaande regel is verwijderd of geannuleerd. Als een regel is verwijderd, wordt deze niet weergegeven in het raster. De regel kan dan dus ook niet worden geselecteerd. Er wordt echter nog wel rekening mee gehouden wanneer het toewijzingsproces wordt uitgevoerd.

Als u de vereiste verkooporderregels hebt geselecteerd, gebruikt u de knoppen in het actiepaneel, zoals hier wordt beschreven:

- **Hertoewijzing bijwerken**: hiermee berekent u de nieuwe opbrengstprijsbedragen voor de geselecteerde verkooporderregels. Als een regel is verwijderd of geannuleerd, wordt de hertoewijzing alleen uitgevoerd voor de bestaande regels die u hebt geselecteerd. In de volgende afbeelding ziet u een voorbeeld van verkooporderregels voordat de hertoewijzing wordt bijgewerkt.

    [![Verkooporderregels voordat de hertoewijzing wordt bijgewerkt.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    De nieuwe bedragen van opbrengstprijzen worden weergegeven in de kolom **Opnieuw toegewezen bedrag** in het raster **Regels**. De hertoewijzing is nu verwerkt, maar nog niet berekend. In de volgende afbeelding ziet u een voorbeeld van verkooporderregels nadat de hertoewijzing is bijgewerkt.

    [![Verkooporderregels nadat de hertoewijzing is bijgewerkt.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Verwerken**: hiermee verwerkt of boekt u de opnieuw toegewezen opbrengstprijzen. Nadat u deze knop hebt geselecteerd, kan de hertoewijzing niet meer worden omgekeerd. Als u **Toewijzing bijwerken** niet selecteert voordat u **Verwerken** selecteert, wordt de hertoewijzing automatisch uitgevoerd.

    - Als er geen verkooporderregel is gefactureerd, worden de bedragen van opbrengstprijzen bijgewerkt voor de verkooporders die voor hertoewijzing zijn geselecteerd.
    - Als een of meer verkooporderregels zijn gefactureerd, worden corrigerende journaalregels geboekt en worden alle gemaakte opbrengstschemadetails voor de gefactureerde verkooporderregel gecorrigeerd.

- **Verwacht boekstuk**: hiermee geeft u een voorbeeld weer van de journaalregels die zijn gemaakt voor de verkooporderregels die zijn gefactureerd. Als er geen regels zijn gefactureerd, wordt er niets weergegeven. Als u **Toewijzing bijwerken** niet selecteert voordat u **Verwacht boekstuk** selecteert, wordt de hertoewijzing automatisch uitgevoerd.
- **Hertoewijzing opbrengst**: hiermee opent u een pagina met de opbrengstprijstoewijzing voor alle geselecteerde regels. U kunt de gegevens op de pagina niet wijzigen. Hier worden de regelbedragen weergegeven die zijn gebruikt voor de hertoewijzing.

    [![Regelbedragen die zijn gebruikt voor hertoewijzing.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Gegevens opnieuw instellen voor geselecteerde klant**: als het hertoewijzingsproces is gestart, maar nog niet is voltooid, wist u hiermee alleen de gegevens in de hertoewijzingstabel voor de geselecteerde klant. Stel dat u meerdere verkooporderregels markeert voor hertoewijzing, de pagina open laat zonder **Verwerken** te selecteren en er vervolgens een time-out optreedt op de pagina. In dit geval blijven de verkooporderregels gemarkeerd en zijn ze niet beschikbaar voor een andere gebruiker om het hertoewijzingsproces te voltooien. De pagina kan zelfs leeg zijn als deze wordt geopend. In deze situatie kunt u de knop **Gegevens opnieuw instellen voor geselecteerde klant** gebruiken om onverwerkte verkooporders te verwijderen, zodat een andere gebruiker het hertoewijzingsproces kan voltooien.

## <a name="undo-a-reallocation"></a>Een hertoewijzing ongedaan maken

U maakt een hertoewijzing ongedaan door nog een hertoewijzing uit te voeren. De hertoewijzing wordt opnieuw uitgevoerd en de gebruiker selecteert verschillende verkooporderregels om in het tweede hertoewijzingsproces op te nemen.

Als een hertoewijzing is uitgevoerd voor twee of meer afzonderlijke verkooporders, kunt u deze ongedaan maken door **Prijs opnieuw toewijzen met nieuwe orderregels** te selecteren in een verkooporder die in de hertoewijzing is opgenomen. U kunt niet naar **Opbrengsttoerekening \> Periodieke taken \> Prijs opnieuw toewijzen met nieuwe orderregels** gaan om de hertoewijzing ongedaan te maken omdat op de pagina die op deze manier wordt geopend alleen verkooporders zonder hertoewijzings-id worden weergegeven. De hertoewijzings-id wordt toegewezen nadat het document opnieuw is toegewezen.

Op de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** heft u de markering op voor de verkooporders die u van de contractuele overeenkomst wilt uitsluiten. Gebruik de betreffende knoppen in het actievenster, zoals **Hertoewijzing bijwerken** en **Verwerken**, om de hertoewijzing te verwerken. Als alleen de actieve verkooporder nog is gemarkeerd, wordt de hertoewijzings-id verwijderd wanneer de wijziging wordt verwerkt.

Als een hertoewijzing wordt uitgevoerd door een nieuwe regel toe te voegen aan een volledig of gedeeltelijk gefactureerde verkooporder, kan de hertoewijzing alleen ongedaan worden gemaakt door die regel uit de verkooporder te verwijderen en de hertoewijzing opnieuw uit te voeren. De verkooporderregel moet worden verwijderd omdat ervan wordt uitgegaan dat alle regels van een verkooporder deel uitmaken van hetzelfde contract. U kunt de markering van een verkooporderregel niet opheffen terwijl u zich op de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** bevindt.

## <a name="reallocate-multiple-times"></a>Meerdere keren opnieuw toewijzen

U kunt meerdere hertoewijzingen voor dezelfde verkooporder uitvoeren als er meerdere wijzigingen in het contract zijn aangebracht. Elke hertoewijzing activeert de toekenning van een hertoewijzings-id aan de verkooporder of groep verkooporders om de wijzigingen te groeperen. Als er meerdere hertoewijzingen worden uitgevoerd, wordt voor elke aanvullende hertoewijzing dezelfde hertoewijzings-id gebruikt als voor de eerste hertoewijzing.

Stel dat verkooporder 00045 wordt ingevoerd en deze verkooporder meerdere regels bevat. Als de verkooporder volledig is gefactureerd, wordt hieraan een nieuwe verkooporderregel toegevoegd. U kunt de hertoewijzing vervolgens uitvoeren door de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** vanuit verkooporder 00045 te openen of naar **Opbrengsttoerekening \> Periodieke taken \> Prijs opnieuw toewijzen met nieuwe orderregels** te gaan. De hertoewijzings-id **Reall000001** wordt aan de verkooporder toegewezen.

Er wordt een tweede verkooporder, 00052, voor hetzelfde contract gemaakt. De hertoewijzing kan opnieuw worden uitgevoerd door de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** te openen vanuit verkooporder 00045, maar niet vanuit verkooporder 00052. Als u de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** vanuit verkooporder 00052 opent, wordt verkooporder 00045 niet weergegeven omdat hieraan een hertoewijzings-id is toegewezen. Op de pagina worden alleen verkooporders zonder hertoewijzings-id weergegeven.

U kunt de tweede hertoewijzing opnieuw uitvoeren. U kunt de hertoewijzing van verkooporder 00045 ongedaan maken. In dit geval wordt de hertoewijzings-id verwijderd en kunt u de hertoewijzing opnieuw uitvoeren vanuit verkooporder 00045 of verkooporder 00052. U kunt de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** ook openen vanuit verkooporder 00045 en de tweede verkooporder toevoegen. Wanneer de hertoewijzing wordt verwerkt, wordt hertoewijzings-id **Reall000001** zowel aan verkooporder 00045 als aan verkooporder 00052 toegewezen.

## <a name="scenarios-for-reallocation"></a>Scenario's voor hertoewijzing

In de volgende onderwerpen worden verschillende scenario's voor opbrengsttoerekening besproken:

- [Hertoewijzing van opbrengsttoerekening - Scenario 1](rev-rec-reallocation-scenario-1.md) – Er worden twee verkooporders ingevoerd, maar ze worden alleen bevestigd. Hetzelfde scenario levert vergelijkbare resultaten op als meer dan twee verkooporders zijn bevestigd.
- [Hertoewijzing van opbrengsttoerekening - Scenario 2](rev-rec-reallocation-scenario-2.md) – Er worden twee verkooporders ingevoerd en vervolgens voegt de klant een artikel aan het contract toe nadat de eerste verkooporder is gefactureerd.
- [Hertoewijzing van opbrengsttoerekening - Scenario 3](rev-rec-reallocation-scenario-3.md) – Er wordt een nieuwe regel toegevoegd aan een bestaande, gefactureerde verkooporder.
- [Hertoewijzing van opbrengsttoerekening - Scenario 4](rev-rec-reallocation-scenario-4.md) – Er wordt een regel verwijderd uit een bestaande, gedeeltelijk gefactureerde verkooporder.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
