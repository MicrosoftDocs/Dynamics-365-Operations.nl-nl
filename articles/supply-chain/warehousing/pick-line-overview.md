---
title: Een menuoptie voor een mobiel apparaat instellen om een overzicht van orderverzamelregels te bieden
description: In dit artikel wordt uitgelegd hoe u kunt definiëren wanneer een lijst met alle werkregels wordt weergegeven voor magazijnmedewerkers die magazijnwerk op een mobiel apparaat verwerken. Deze mogelijkheid kan handig zijn voor magazijnmedewerkers die vaak een overzicht van de orderverzamelregels in een werkorder nodig hebben zodat ze de orderverzamelvolgorde kunnen optimaliseren.
author: Mirzaab
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aeadca6f3c31d5d8c1ef9d334b0e531896ac99b1
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336300"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Een menuoptie voor een mobiel apparaat instellen om een overzicht van orderverzamelregels te bieden

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u opties kunt configureren die betrekking hebben op het overzicht van orderverzamelregels voor menuopties van mobiele apparaten die worden gebruikt om werkzaamheden voor het verzamelen van orders te verwerken. Met het overzicht van orderverzamelregels kunnen magazijnmedewerkers een lijst met alle werkregels bekijken die betrekking hebben op de huidige taak, en kunnen ze een selectie maken in die lijst. Met deze mogelijkheid kunnen medewerkers de orderverzamelvolgorde optimaliseren. De functie bevat opties waarmee de standaardknop **Overslaan** wordt vervangen waarmee medewerkers de regels een voor een in een vaste volgorde kunnen doorlopen. (De mogelijkheid om die knop te gebruiken is echter nog steeds beschikbaar.)

Beheerders kunnen elke menuoptie afzonderlijk configureren om te bepalen hoe, wanneer en waar de mobiele app Magazijnbeheer het overzicht van orderverzamelregels laat zien.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>De functie Overzicht van werkorderverzamelregels inschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** _Magazijnbeheer_
- **Functienaam:** _Overzicht van werkorderverzamelregels_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Menuopties configureren om een lijst met alle werkregels weer te geven

Als u een menuoptie voor een mobiel apparaat wilt instellen om een overzicht van orderverzamelregels te bieden, voert u de volgende stappen uit.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer of maak een menuoptie die verband houdt met werkorderverzameling en stel de volgende waarden in:

    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Ja*
    - **Bestuurd door:** *Door gebruiker bestuurd* of *Door systeem bestuurd*

    Zie voor meer informatie over het maken van menuopties en het gebruik van de verschillende instellingen die beschikbaar zijn op de pagina **Menuopties voor mobiel apparaat** [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md).

1. Configureer op het sneltabblad **Algemeen** de functie door het veld **Lijst met werkregels weergeven** op een van de volgende waarden in:

    - **Alleen op aanvraag weergeven** : medewerkers kunnen ervoor kiezen de lijst met orderverzamelregels te bekijken door de knop **Ga verder naar** in de mobiele app Magazijnbeheer te selecteren.
    - **Weergeven aan het begin van elke verzameling**: medewerkers zien de lijst telkens wanneer ze een orderverzamelregel starten of voltooien. Ze kunnen de lijst ook opnieuw bekijken door de knop **Ga verder naar** in de mobiele app Magazijnbeheer te selecteren.
    - **Alleen weergeven bij het begin van de eerste verzameling**: medewerkers zien de lijst telkens wanneer ze nieuwe orderverzamelingswerkzaamheden starten, maar niet na elke regel. Ze kunnen de lijst ook opnieuw bekijken door de knop **Ga verder naar** in de mobiele app Magazijnbeheer te selecteren.
    - **Nooit weergeven**: de standaardknop **Overslaan** wordt weergegeven in de mobiele app Magazijnbeheer en de weergave van de lijst met werkregels is uitgeschakeld. Met de knop **Overslaan** kunnen medewerkers de regels een voor een in een vaste volgorde doorlopen. Ze kunnen de lijst ook zo vaak als nodig is doorlopen, totdat alle regels zijn verwerkt.

1. Selecteer **Opslaan** in het actievenster.

    Als u het veld **Lijst met werkregels weergeven** instelt op een willekeurige waarde behalve *Nooit weergeven*, wordt de knop **Veldenlijst** in het actievenster beschikbaar.

1. Selecteer **Veldenlijst** in het actievenster.
1. Configureer op de pagina **Veldenlijst** de informatie die in de mobiele app Magazijnbeheer voor elke regel in de lijst wordt weergegeven.

    - Het veld **Primair besturingselement** wordt altijd ingesteld op *LineNum*. Daarom begint elke rij in de lijst met een regelnummer.
    - Gebruik de resterende **Weergaveveld**-velden om desgewenst maximaal zeven extra weergavevelden toe te voegen. Selecteer de naam van een werkregelveld in elk **Weergaveveld**-veld. Op elke regel wordt vervolgens een waarde voor dat veld weergegeven. De waarden worden weergegeven in de volgorde die u hier selecteert. U kunt sommige velden van **Weergaveveld** leeg laten als u niet alle zeven waarden nodig hebt.

1. Selecteer **Opslaan** in het actievenster en sluit de pagina **Veldenlijst**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]