---
title: Werken met geserialiseerde artikelen in het POS
description: In dit onderwerp wordt uitgelegd hoe u geserialiseerde artikelen kunt beheren in de verkooppunttoepassing (POS).
author: boycezhu
manager: annbe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: ee79fef3300ebea476ea37adc4cc61a9bbadb5d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231243"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Werken met geserialiseerde artikelen in het POS

[!include [banner](includes/banner.md)]

Veel detailhandelaren verkopen producten waarvoor seriebeheer vereist is. Deze producten worden *geserialiseerde artikelen* genoemd. Sommige detailhandelaren willen mogelijk serienummers in de winkel- of magazijnvoorraad bijhouden voor traceringsdoeleinden. Andere detailhandelaren willen mogelijk serienummers vastleggen tijdens het verkoopproces, voor service- en garantiedoeleinden. In dit onderwerp wordt uitgelegd hoe u geserialiseerde artikelen kunt beheren in de Microsoft Dynamics 365 Commerce-verkooppunttoepassing (POS).

## <a name="serial-number-configurations"></a>Configuratie van serienummers

Een artikel wordt beschouwd als een geserialiseerd artikel als er een traceringsdimensiegroep is toegewezen die is ingesteld op het toestaan van serienummers. Selecteer in Commerce Headquarters op de pagina **Traceringsdimensiegroepen** de optie **Actief** om serienummers voor het voorraadproces in te schakelen of selecteer de optie **Actief in verkoopproces** om serienummers voor het verkoopproces in te schakelen.

Schakel op het sneltabblad **Traceringsdimensies** de parameter **Lege ontvangst is toegestaan** in om serienummers als optionele invoer toe te staan tijdens het voorraadontvangstproces van geserialiseerde artikelen. Als u deze parameter uitschakelt, wordt het serienummer vereist als invoer. Op dezelfde manier bepaalt de parameter **Lege uitgifte is toegestaan** of serienummers vereist zijn tijdens het voorraadverzendingsproces.

> [!NOTE]
> Als u de POS-bewerkingen **Inkomende voorraad** en **Uitgaande voorraad** wilt gebruiken om serienummers te registreren of te valideren voor een geserialiseerd artikel, moet u configureren dat aan dat artikel een traceringsdimensiegroep wordt toegewezen die is ingesteld voor het toestaan van serienummers voor de optie **Actief**, maar niet voor de optie **Actief in verkoopproces**.

## <a name="serial-number-management-page"></a>De pagina Serienummerbeheer

Als in de POS-bewerkingen **Inkomende voorraad** en **Uitgaande voorraad** het artikel dat wordt geselecteerd, ontvangen of verzonden een geserialiseerd artikel is, bevat het deelvenster **Details** een optie **Serienummer beheren** die naar de pagina **Serienummerbeheer** leidt waar u serienummers voor het artikel kunt registreren of valideren. U kunt ook de pagina **Serienummerbeheer** openen door de actie **Serienummer** te selecteren op de app-balk van de weergave Orderdetails of door **Serienummer beheren** te selecteren in het dialoogvenster waarin u instructies ziet tijdens het ontvangst- of verzendproces. 

Op de pagina **Serienummerbeheer** worden alle openstaande serienummerregels weergegeven die nog moeten worden geregistreerd of gevalideerd. Deze pagina kan twee tabbladen bevatten: één voor het huidige artikel en één voor alle geserialiseerde artikelen in de order.

In het veld **Status** op de pagina **Serienummerbeheer** vindt u informatie over de huidige fase waarin elk serienummer zich bevindt:

- **Niet geregistreerd**: het serienummer is niet opgegeven of het geregistreerde serienummer is nog niet gevalideerd (in het ontvangstproces).
- **Registratie bezig**: het serienummer is geregistreerd en lokaal opgeslagen in de kanaaldatabase van de winkel of het vooraf geregistreerde serienummer is gevalideerd. Alleen serienummers met de status **Registratie bezig** worden naar Commerce Headquarters verzonden wanneer de ontvangst is voltooid of afgehandeld.

## <a name="receive-serialized-items"></a>Geserialiseerde artikelen ontvangen

Met de POS-bewerking **Inkomende voorraad** kunnen gebruikers de volgende taken uitvoeren voor geserialiseerde artikelen:

- Serienummers registreren voor geserialiseerde artikelen wanneer deze artikelen worden ontvangen in de winkel via een inkooporder.
- Vooraf geregistreerde serienummers voor geserialiseerde artikelen valderen wanneer deze artikelen worden ontvangen in de winkel via een inkooporder of een transferorder.

### <a name="register-serial-numbers-against-serialized-items"></a>Serienummers registreren voor geserialiseerde artikelen

Voor een inkooporder ziet u tijdens het ontvangstproces van een geserialiseerd artikel de optie **Serienummer beheren** in een dialoogvenster. U kunt deze optie selecteren om de pagina **Serienummerbeheer** te openen en om serienummers te registreren. U kunt deze stap ook overslaan tijdens het ontvangstproces en de invoer later opgeven voordat de ontvangst wordt geboekt.

Standaard wordt het tabblad voor het huidige artikel weergegeven. Alle serienummerregels hebben een lege waarde voor het serienummer en de status **Niet geregistreerd**. U kunt streepjescodes voor serienummers scannen of u kunt **Serienummer** op de app-balk selecteren om continu serienummers in te voeren. De serienummers die u invoert, worden weergegeven in de lijst en hun status wordt gewijzigd in **Registratie bezig**. Het maximum aantal serienummers dat u in de lijst kunt registreren, is gelijk aan de ontvangsthoeveelheid. Als u een fout maakt, kunt u in het **detailvenster** de optie **Bewerken** of **Wissen** selecteren om wijzigingen aan te brengen in de serienummers die u hebt ingevoerd.

U kunt serienummers ook registreren op het tabblad **Alle geserialiseerde artikelen** van de pagina **Serienummerbeheer**. Selecteer in de lijst het artikel waarvoor u de serienummers wilt registreren.

### <a name="validate-serial-numbers-on-serialized-items"></a>Serienummers op geserialiseerde artikelen valideren

Voor een transferorder moeten aan de uitgaande zijde de serienummers van de geserialiseerde artikelen worden geregistreerd tijdens het verzendproces. Voor een inkooporder kan de leverancier informatie over serienummers opgeven via een Advance Shipment Notice (ASN) en kunt u de nummers vooraf registreren voor de artikelen die worden verzonden. In beide gevallen zijn de serienummers bekend vóór de ontvangst. Aan de inkomende zijde hoeft u dus alleen te valideren dat u hebt ontvangen wat u had moeten ontvangen.

Om serienummers te valideren, kunt u de pagina **Serienummerbeheer** openen tijdens het ontvangstproces of op elk moment voordat de ontvangst wordt geboekt. Voor elk geserialiseerd artikel met vooraf geregistreerde serienummers worden alle serienummers op deze pagina automatisch ingesteld op de beginstatus **Niet geregistreerd**. Als u serienummers wilt valideren, kunt u ze scannen of invoeren. Als serienummers worden ingevoerd, wordt door de toepassing gecontroleerd of ze overeenkomen met de voorgeregistreerde serienummers. Als ze overeenkomen, wordt de status gewijzigd in **Registratie bezig**. Anders ontvangt u een foutbericht. U kunt ook rechtstreeks een serienummer selecteren en vervolgens de optie **Serienummer valideren** in het deelvenster **Details** selecteren om het desbetreffende serienummer snel te markeren als gevalideerd. Het maximum aantal serienummers dat u in de lijst kunt valideren, is gelijk aan de ontvangsthoeveelheid.

U kunt serienummers ook valideren op het tabblad **Alle geserialiseerde artikelen** van de pagina **Serienummerbeheer**. Selecteer in de lijst het artikel waarvoor u de serienummers wilt valideren.

## <a name="ship-serialized-items"></a>Geserialiseerde artikelen verzenden

U kunt de POS-bewerking **Uitgaande voorraad** gebruiken om serienummers te registreren voor geserialiseerde artikelen wanneer deze via een transferorder vanuit de huidige winkel worden verzonden.

### <a name="register-serial-numbers-against-serialized-items"></a>Serienummers registreren voor geserialiseerde artikelen

Voor een transferorder ziet u tijdens het verzendproces van een geserialiseerd artikel de optie **Serienummer beheren** in een dialoogvenster. U kunt de optie selecteren om de pagina **Serienummerbeheer** te openen en om serienummers te registreren. U kunt deze stap ook overslaan tijdens het verzendproces en de invoer later opgeven voordat de zending wordt geboekt.

Standaard wordt het tabblad voor het huidige artikel weergegeven. Alle serienummerregels hebben een lege waarde voor het serienummer en de status **Niet geregistreerd**. U kunt streepjescodes voor serienummers scannen of u kunt **Serienummer** op de app-balk selecteren om continu serienummers in te voeren. De serienummers die u invoert, worden weergegeven in de lijst en hun status wordt gewijzigd in **Registratie bezig**. Het maximum aantal serienummers dat u in de lijst kunt registreren, is gelijk aan de verzendhoeveelheid. Als u een fout maakt, kunt u in het **detailvenster** de optie **Bewerken** of **Wissen** selecteren om wijzigingen aan te brengen in de serienummers die u hebt ingevoerd.

U kunt serienummers ook registreren op het tabblad **Alle geserialiseerde artikelen** van de pagina **Serienummerbeheer**. Selecteer in de lijst het artikel waarvoor u de serienummers wilt registreren.

U kunt eventueel validatie van de beschikbaarheid van serienummers inschakelen tijdens de registratie van serienummers voor een uitgaande transferorder. Als u deze validatie uitvoert en een serienummer probeert te verzenden dat niet beschikbaar is in de voorraad van de verzendende winkel, ontvangt u een foutbericht en moet u een ander nummer opgeven.

Als u een dergelijke validatie wilt inschakelen, moet u de volgende taken plannen zodat deze regelmatig worden uitgevoerd:

- **Detailhandel en Commerce** > **IT detailhandel en Commerce** > **Producten en voorraad** > **Beschikbaarheid product met traceringsdimensies**.
- **Detailhandel en Commerce** > **Distributieplanningen** > **1130** (**Productbeschikbaarheid**)

## <a name="sell-serialized-items-in-pos"></a>Geserialiseerde artikelen verkopen in POS

Hoewel de POS-toepassing altijd de verkoop van geserialiseerde artikelen heeft ondersteund, kunnen organisaties in Commerce, versie 10.0.17 en hoger, functionaliteit inschakelen waarmee de bedrijfslogica wordt verbeterd die wordt geactiveerd bij de verkoop van producten die zijn geconfigureerd voor het bijhouden van serienummers.

Wanneer de functie **Verbeterde serienummervalidatie bij het vastleggen en afhandelen van POS-orders** is ingeschakeld, worden de volgende productconfiguraties geëvalueerd bij de verkoop van geserialiseerde producten in POS:

- Instellen van **Serietype** voor het product (**actief** of **actief in verkoop**).
- Instellingen voor **Lege uitgifte is toegestaan** voor het product.
- Instellingen voor **Fysieke negatieve voorraad** voor het product en/of het verkopende magazijn.

### <a name="active-serial-configurations"></a>Actieve seriële configuraties

Wanneer artikelen worden verkocht in POS die zijn geconfigureerd met een **actieve** traceringsdimensie voor serienummers, wordt een validatielogica gestart om te voorkomen dat gebruikers de verkoop van een geserialiseerd artikel voltooien met een serienummer dat niet kan worden gevonden in de huidige voorraad van het verkopende magazijn. Er zijn twee uitzonderingen op deze validatieregel:

- Als het artikel ook is geconfigureerd met **Lege uitgifte is toegestaan** ingeschakeld, kunnen gebruikers de invoer van het serienummer overslaan en het artikel verkopen zonder serienummeraanduiding.
- Als het artikel en/of het verkopende magazijn zijn geconfigureerd wanneer **Fysieke negatieve voorraad** is ingeschakeld, accepteert en verkoopt de toepassing een serienummer dat niet kan worden bevestigd als in voorraad in het magazijn waaruit het wordt verkocht. Met deze configuratie kan de voorraadtransactie voor dat specifieke artikel-/serienummer negatief worden en het systeem kan daarom de verkoop van onbekende serienummers toestaan.

> [!IMPORTANT]
> Om er zeker van te zijn dat de POS-toepassing op de juiste manier kan controleren of de serienummers die worden verkocht voor artikelen van het seriële type **Actief** in de voorraad van het verkopende magazijn aanwezig zijn, moeten organisaties de taak **Beschikbaarheid product met traceringsdimensies** en de bijbehorende taak voor de distributie van productbeschikbaarheid **1130** regelmatig uitvoeren in Commerce Headquarter. Wanneer er nieuwe geserialiseerde voorraad wordt ontvangen in de verkoopmagazijnen, moet het voorraadmodel regelmatig de kanaaldatabase bijwerken met de meest recente gegevens over de voorraadbeschikbaarheid, zodat het POS de voorraadbeschikbaarheid kan valideren van serienummers die worden verkocht. Voor de taak **Beschikbaarheid product met traceringsdimensies** wordt een actuele momentopname van de hoofdvoorraad gemaakt, inclusief serienummers, voor alle magazijnen van het bedrijf. Bij de distrbutietaak **1130** wordt die momentopname van de voorraad genomen en gedeeld met alle geconfigureerde kanaaldatabases.

### <a name="active-in-sales-process-serial-configurations"></a>Actieve seriële configuraties in verkoopprocessen

Artikelen die met de serienummers zijn geconfigureerd als **Actief in verkoopproces**, doorlopen geen logica voor voorraadvalidatie, omdat deze configuratie inhoudt dat de voorraadserienummers niet vooraf in de voorraad zijn geregistreerd en dat de serienummers alleen worden vastgelegd op het moment van verkoop.  

Als **Lege uitgifte is toegestaan** ook is geconfigureerd voor artikelen die zijn geconfigureerd voor **Actief in verkoopproces**, kan de invoer van serienummers worden overgeslagen. Als **Lege uitgifte is toegestaan** niet is geconfigureerd, moet de gebruiker van de toepassing een serienummer invoeren, ook al wordt het nummer niet gevalideerd tegen de beschikbare voorraad.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Serienummers toepassen tijdens het maken van POS-transacties

De POS-toepassing vraagt gebruikers onmiddellijk om serienummers vast te leggen bij de verkoop van een artikel met een serienummer, maar de toepassing staat gebruikers niet toe om de invoer van serienummers tot op een bepaald punt in het verkoopproces over te slaan. Wanneer de gebruiker een betaling begint vast te leggen, dwingt de toepassing de invoer van een serienummer af voor alle artikelen die niet zijn geconfigureerd om te worden afgehandeld via toekomstige zendingen of het ophalen van artikelen. Voor alle geserialiseerde artikelen die geconfigureerd zijn voor cash-and-carry- of carryout-afhandeling, moet de gebruiker het serienummer vastleggen (of akkoord gaan dat deze optie wordt leeggelaten als de artikelconfiguratie dit toestaat) voordat de verkoop wordt afgerond.

Voor geserialiseerde artikelen die worden verkocht voor toekomstige ophalen of zending, kunnen POS-gebruikers het invoeren van het serienummer overslaan en nog steeds het maken van de klantorder voltooien.   

> [!NOTE]
> Wanneer geserialiseerde producten worden verkocht of afgehandeld via de POS-toepassing, wordt een hoeveelheid van 1 afgedwongen voor de geserialiseerde artikelen in de verkooptransactie. Dit is het resultaat van de manier waarop de serienummergegevens in de verkoopregel worden bijgehouden. Wanneer u een transactie voor meerdere geserialiseerde artikelen verkoopt of afhandelt via POS, moet elke verkoopregel alleen worden geconfigureerd met de hoeveelheid '1'. 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Serienummers toepassen tijdens het afhandelen van klantorders of het ophalen

Wanneer klantorderregels voor geserialiseerde producten worden uitgevoerd met de bewerking **Orderafhandeling** in POS, wordt in POS het vastleggen van serienummers afgedwongen vóór de uiteindelijke afhandeling van de order. Als er tijdens het vastleggen van de aanvankelijke order geen serienummer is opgegeven, moet dat nummer worden vastgelegd tijdens het verzamelen, verpakken of verzenden in POS. Bij elke stap wordt een validatie uitgevoerd en de gebruiker wordt alleen om serienummergegevens gevraagd als deze ontbreken of niet meer geldig zijn. Als een gebruiker bijvoorbeeld de stappen voor het verzamelen of verpakken overslaat en direct een zending start en een serienummer niet is geregistreerd voor de regel, vereist POS dat het serienummer eerst moet worden ingevoerd voordat de laatste factureringsstap wordt voltooid. Wanneer u het vastleggen van het serienummer afdwingt tijdens bewerkingen voor de afhandeling van de order in POS, zijn alle regels die eerder in dit onderwerp werden genoemd nog steeds van toepassing. Alleen geserialiseerde artikelen die als **Actief** zijn geconfigureerd, doorlopen een validatie van serienummers in voorraad. Artikelen die zijn geconfigureerd als **Actief in verkoopproces**, worden niet gevalideerd. Als **Fysieke negatieve voorraad** is toegestaan voor producten die zijn geconfigureerd als **Actief**, wordt een serienummer geaccepteerd, ongeacht de voorraadbeschikbaarheid. Voor artikelen met de status **Actief** en **Actief in verkoopproces**, als **Lege uitgifte is toegestaan** is geconfigureerd, kan een gebruiker serienummers leeglaten als dit is toegestaan tijdens het verzamelen, verpakken en verzenden.

Validaties voor serienummers worden ook uitgevoerd wanneer een gebruiker de bewerkingen voor ophalen voor klantorders in POS. In de POS-toepassing kan het ophalen van een product met serienummers pas worden afgerond als de eerder genoemde validaties zijn doorlopen. De validaties zijn altijd gebaseerd op de traceringsdimensie van het product en de configuraties van het verkoopmagazijn. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Binnenkomende voorraadbewerking in POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Uitgaande voorraadbewerking in POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]