---
title: Werken met geserialiseerde artikelen in het POS
description: In dit onderwerp wordt uitgelegd hoe u geserialiseerde artikelen kunt beheren in de verkooppunttoepassing (POS).
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978358"
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

## <a name="additional-resources"></a>Aanvullende bronnen

[Binnenkomende voorraadbewerking in POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Uitgaande voorraadbewerking in POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
