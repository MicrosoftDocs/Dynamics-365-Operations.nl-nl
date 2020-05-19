---
title: Werken met geserialiseerde artikelen in het POS
description: In dit onderwerp wordt uitgelegd hoe u geserialiseerde artikelen kunt beheren in de verkooppunttoepassing (POS).
author: boycezhu
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1e0d6aa7cd5576578378e70c6ee808833314aff3
ms.sourcegitcommit: 919620b4aca425e6a1248ee12f50a622d2531e58
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290765"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Werken met geserialiseerde artikelen in het POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Veel detailhandelaren verkopen producten waarvoor seriebeheer vereist is. Deze artikelen worden *geserialiseerde artikelen* genoemd. Sommige detailhandelaren willen mogelijk serienummers bijhouden voor traceringsdoeleinden. Andere detailhandelaren willen mogelijk serienummers vastleggen tijdens het verkoopproces, voor service- en garantiedoeleinden. In dit onderwerp wordt uitgelegd hoe u geserialiseerde artikelen kunt beheren in de Microsoft Dynamics 365 Commerce-verkooppunttoepassing (POS).

## <a name="serial-number-configurations"></a>Configuratie van serienummers

Een artikel wordt beschouwd als een geserialiseerd artikel als er een traceringsdimensiegroep is toegewezen die is ingesteld op het toestaan van serienummers. U moet serienummers voor het voorraadproces inschakelen in Commerce Headquarters door de optie **Actief** te selecteren op de pagina **Traceringsdimensiegroepen**. Als u serienummers voor het verkoopproces wilt inschakelen, selecteert u de optie **Actief in verkoopproces**.

Als op het sneltabblad **Traceringsdimensies** de optie **Lege ontvangst is toegestaan** is ingeschakeld, is het invoeren van het serienummer optioneel tijdens het voorraadontvangstproces. Als de optie is uitgeschakeld, is het serienummer vereist.

Als op het snelttabblad **Serienummers** de optie **Serienummercontrole** is ingeschakeld, moet het serienummer uniek zijn per eenheid. Dubbele serienummers zijn dus niet toegestaan.

## <a name="serialized-items-in-the-receiving-process"></a>Geserialiseerde artikelen in het ontvangstproces

Met de bewerking **Inkomende voorraad** in de POS-toepassing kunnen gebruikers de volgende taken uitvoeren voor geserialiseerde artikelen:

- Serienummers registreren voor geserialiseerde artikelen wanneer deze artikelen worden ontvangen in de winkel via een inkooporder.
- Vooraf geregistreerde serienummers voor geserialiseerde artikelen valderen wanneer deze artikelen worden ontvangen in de winkel via een inkooporder of een transferorder.

> [!NOTE]
> Als u de bewerking **Inkomende voorraad** wilt gebruiken om een geserialiseerd artikel te registreren of te valideren, moet aan het artikel een traceringsdimensiegroep worden toegewezen die is ingesteld voor het toestaan van serienummers voor de optie **Actief** maar niet voor de optie **Actief in verkoopproces**.

Als u het ontvangstproces wilt starten, kunt u beginnen in de bewerking **Inkomende voorraad** in de weergave **Nu ontvangen** door de streepjescode van het artikel te scannen of de artikel-id op te geven. U kunt ook in de weergave **Volledige orderlijst** beginnen door het artikel handmatig te selecteren.

Als het artikel dat wordt geselecteerd of ontvangen een geserialiseerd artikel is, bevat het **detailvenster** voor het artikel een koppeling **Serie nummer beheren** waarmee de pagina **Serienummerbeheer** wordt geopend. U kunt ook de pagina **Serienummerbeheer** openen door **Serienummer** te selecteren op de app-balk van de weergave Orderdetails of door **Serienummer beheren** te selecteren in het dialoogvenster waarin u instructies ziet tijdens het ontvangstproces. Op de pagina **Serienummerbeheer** worden alle openstaande serienummerregels weergegeven die nog moeten worden geregistreerd of gevalideerd. Deze pagina kan twee tabbladen bevatten: één voor het huidige artikel en één voor alle geserialiseerde artikelen in de order.

In het veld **Status** op de pagina **Serienummerbeheer** vindt u informatie over de huidige fase waarin elk serienummer zich bevindt:

- **Niet geregistreerd**: het serienummer is niet opgegeven of het geregistreerde serienummer is nog niet gevalideerd.
- **Registratie bezig**: het serienummer is geregistreerd en lokaal opgeslagen in de kanaaldatabase van de winkel of het vooraf geregistreerde serienummer is gevalideerd. Alleen serienummers met de status **Registratie bezig** worden naar Commerce Headquarters verzonden wanneer de ontvangst is voltooid.

### <a name="register-serial-numbers-against-serialized-items"></a>Serienummers registreren voor geserialiseerde artikelen

Voor een inkooporder ziet u in een dialoogvenster met instructies tijdens het ontvangstproces van een geserialiseerd artikel de optie **Serienummer beheren**. U kunt deze optie selecteren om de pagina **Serienummerbeheer** te openen en om serienummers te registreren. U kunt deze stap ook overslaan tijdens het ontvangstproces en de invoer later opgeven voordat de ontvangst wordt geboekt.

Standaard wordt het tabblad voor het huidige artikel weergegeven. Alle serienummerregels hebben een lege waarde voor het serienummer en de status **Niet geregistreerd**. U kunt streepjescodes voor serienummers scannen of u kunt **Serienummer** op de app-balk selecteren om continu serienummers in het dialoogvenster in te voeren. De serienummers die u invoert, worden weergegeven in de lijst en de status van de serienummerregels wordt gewijzigd in **Registratie bezig**. Het maximumaantal serienummers dat u in de lijst kunt registreren, is gelijk aan de ontvangsthoeveelheid. Als u een fout maakt, kunt u in het **detailvenster** de optie **Bewerken** of **Wissen** selecteren om wijzigingen aan te brengen in de serienummers die u hebt ingevoerd.

U kunt serienummers ook registreren op het tabblad **Alle geserialiseerde artikelen** van de pagina **Serienummerbeheer**. Selecteer in de lijst het artikel waarvoor u de serienummers wilt registreren.

Tijdens het registreren van het serienummer op deze pagina wordt de duplicatievalidatie uitgevoerd. Als u probeert een dubbel serienummer in te voeren voor een artikel waarvoor controle op serienummers is ingeschakeld, ontvangt u een foutbericht en moet u een ander nummer opgeven.

### <a name="validate-serial-numbers-on-serialized-items"></a>Serienummers op geserialiseerde artikelen valideren

Voor een transferorder moeten aan de uitgaande zijde de serienummers van de geserialiseerde artikelen worden geregistreerd tijdens het verzendproces. Voor een inkooporder kan de leverancier informatie over serienummers opgeven via een Advance Shipment Notice (ASN) en kunt u de nummers vooraf registreren voor de artikelen die worden verzonden. In beide gevallen zijn de serienummers bekend vóór de ontvangst. Aan de inkomende zijde hoeft u dus alleen te valideren dat u hebt ontvangen wat u had moeten ontvangen.

Om serienummers te valideren, kunt u de pagina **Serienummerbeheer** openen tijdens het ontvangstproces of op elk moment voordat de ontvangst wordt geboekt. Voor elk geserialiseerd artikel met vooraf geregistreerde serienummers worden alle serienummers op deze pagina automatisch ingesteld op de beginstatus **Niet geregistreerd**. Als u serienummers wilt valideren, kunt u ze scannen of invoeren. Als serienummers worden ingevoerd, wordt door de toepassing gecontroleerd of ze overeenkomen met de voorgeregistreerde serienummers. Als ze overeenkomen, wordt de status gewijzigd in **Registratie bezig**. Anders ontvangt u een foutbericht. Het maximumaantal serienummers dat u in de lijst kunt valideren, is gelijk aan de ontvangsthoeveelheid.

U kunt serienummers ook valideren op het tabblad **Alle geserialiseerde artikelen** van de pagina **Serienummerbeheer**. Selecteer in de lijst het artikel waarvoor u de serienummers wilt valideren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Binnenkomende voorraadbewerking in POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
