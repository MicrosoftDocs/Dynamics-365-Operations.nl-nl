---
title: Validatie van factuurvereffening instellen voor leveranciers
description: Bij deze registratie wordt het demobedrijf USMF gebruikt.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a26a057b524f162e4b288b88e8c30f7c5db7a45
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "346842"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Validatie van factuurvereffening instellen voor leveranciers

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bij deze registratie wordt het demobedrijf USMF gebruikt. De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren. Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd. Als uw rechtspersoon uitgaven bijhoudt, zoals verzendkosten, door kosten te berekenen, moet u er voor zorgen dat de configuratiesleutel Toeslagen is geselecteerd.  Factuurmatching in Klanten is het proces van het vergelijken van de leverancierfactuur-, inkooporder- en productontvangstgegevens. Verschillen in deze documenten worden matchingverschillen genoemd. Matchingverschillen worden vergeleken met de gespecificeerde toleranties. Als een matchingverschil het tolerantiepercentage of -bedrag overschrijdt, worden er pictogrammen voor het vereffeningsverschil weergegeven in het formulier Leveranciersfactuur en in het formulier Factuurvereffeningsgegevens.

1. Ga naar Leveranciers > Instellingen > Parameters van module Leveranciers.
2. Klik op het tabblad Factuurvalidatie.
3. Schakel het selectievakje Factuurvereffeningsvalidatie inschakelen in of uit.
    * Selecteer of goedkeuring vereist is voordat een factuur die verschillen vertoont voor factuurvereffening kan worden geboekt. Als dit is ingesteld op Toestaan met waarschuwing, geeft de grafische indicatie weer wanneer een verschil voor factuurvereffening groter is dan de tolerantie. U kunt de factuur echter wel boeken. Als u workflows gebruikt samen met factuurvereffeningsvalidatie, moet u controleren of het veld Factuur met verschillen boeken is ingesteld op Toestaan met waarschuwing om meerdere keren goedkeuren te voorkomen.  
    * Selecteer in het veld Status factuurkoptekst automatisch bijwerken of de vereffening automatisch door het systeem wordt uitgevoerd tijdens de invoer van factuurgegevens. De aanbevolen instelling is Ja, tenzij u problemen ondervindt met de prestaties voor gegevensinvoer. Als automatische updates worden uitgeschakeld, worden de systeemprestaties mogelijk sneller omdat de factuurvereffeningsvalidatie worden genegeerd tijdens de gegevensinvoer. De medewerker die de gegevensinvoer doet moet handmatig de vereffeningsstatus bijwerken om de resultaten van de factuurvereffeningsvalidatie te bekijken wanneer dit is ingesteld op Nee.  
4. Schakel de uitbreiding van de sectie Vereffening van factuurtotalen om.
5. Schakel het selectievakje Factuurtotalen vereffenen in of uit om de feitelijke factuurtotalen te vereffenen met de verwachte totalen.
    * Selecteer of een pictogram wordt weergegeven als een verschil voor factuurvereffening groter is dan de tolerantie. U kunt kiezen om het pictogram weer te geven als een positieve discrepantie groter is dan de tolerantie, of wanneer een positieve of een negatieve discrepantie de tolerantie overschrijdt.  
    * Bijvoorbeeld: de tolerantie is 5 procent en het totale factuurbedrag op de inkooporder is 100,00. Daarom wordt een pictogram voor prijsvereffening weergegeven als het totale factuurbedrag op de factuur hoger is dan 105,00. Als u Indien groter of kleiner dan tolerantie selecteert, wordt het pictogram ook weergegeven als het factuurbedrag minder dan 95,00 bedraagt.  
6. Voer in het veld Tolerantiepercentage voor factuurtotalen een getal in.
7. Schakel de uitbreiding van de sectie Prijs- en hoeveelheidsvereffening om.
    * Selecteer in het veld Regelovereenstemmingsbeleid een waarde om te gebruiken als standaardbeleid voor de rechtspersoon waarmee u werkt. "Niet vereist" betekent er geen controle van afzonderlijke prijzen op factuurregels ten opzichte van inkooporderprijzen of factuurhoeveelheden ten opzichte van pakbonhoeveelheden is vereist. "Tweewegs overeenstemming" betekent dat de verificatie van factuurregels is vereist maar dat alleen de inkooporder en de factuurdocumenten van de leverancier zijn betrokken bij de verificatie. Er wordt geen rekening gehouden met de productontvangst bij de overeenstemmingsvalidaties. "Driewegs overeenstemming" betekent dat de netto-eenheidprijs van de factuur wordt vergeleken met de netto-eenheidsprijs van de inkooporder en dat de overeenkomstige productontvangsthoeveelheid wordt vergeleken met de factuurhoeveelheid.  
    * Als u een overeenstemmingsbeleid voor regels van Tweewegs overeenstemming of Driewegs overeenstemming gebruikt, kunt u prijstolerantiepercentages instellen voor uw rechtspersoon, artikelen en leveranciers op de pagina Artikelprijstolerantie. Als de leveranciersfacturen vergeleken worden met de informatie op inkooporders, wordt gezocht naar het van toepassing zijnde percentage voor prijstolerantie.  
8. Selecteer een optie in het veld Regelovereenstemmingsbeleid.
    * Selecteer een waarde in het veld Overschrijven van overeenstemmingsbeleid toestaan om toe te staan dat een ander vereffeningsniveau voor een artikel, leverancier, combinatie van leverancier en artikel of inkooporderregel wordt toegepast. Het regelovereenstemmingsbeleid van de rechtspersoon kan worden genegeerd voor een specifieke leverancier, een specifiek artikel of een specifieke combinatie van leverancier op de pagina Overeenstemmingbeleid.  
    * U kunt prijstotalen voor regelartikelen op facturen vereffenen door een waarde te selecteren in het veld Totaalprijzen vereffenen. Dit type aanpassing is handig wanneer de leverancier meerdere facturen voor dezelfde inkooporderregel verzendt. U kunt prijsgegevens vergelijken voor het nettobedrag van iedere regel van de factuur en alle in behandeling zijnde en eerder geboekte factuurregels, met het nettobedrag van de overeenkomstige inkooporderregel.  
9. Selecteer een optie in het veld Totaalprijzen vereffenen.
10. Voer in het veld Tolerantie totale inkoopprijs een getal in.
11. Schakel de uitbreiding van de sectie Vereffening van toeslagen om.
12. Om de feitelijke kosten te vereffenen met de verwachte kosten, gebaseerd op de informatie in de inkooporder, schakelt u het selectievakje Vereffening van toeslagen in.
13. Sluit de pagina.

