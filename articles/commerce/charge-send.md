---
title: Orders verzenden vanuit een andere winkel met behulp van de verzendfunctie Toeslag
description: In dit onderwerp wordt de verzendfunctie Toeslag beschreven.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800466"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Orders verzenden vanuit een andere winkel met behulp van de verzendfunctie Toeslag

[!include [banner](includes/banner.md)]

Met de verzendfunctie Toeslag in Commerce kunnen klantorders in de ene winkel worden geplaatst en vanuit een andere winkel worden verzonden.

Klantorders in de POS-client (Point Of Sale) ondersteunen meerdere afhandelingsopties. Enkele voorbeelden van afhandelingsopties:

- Ophalen uit dezelfde locatie op een andere datum.
- Ophalen uit een andere locatie op dezelfde of een andere datum.
- Verzenden vanuit het standaardmagazijn van verzending die is toegewezen aan de winkel en op een bepaalde datum leveren.

Met de verzendfunctie Toeslag worden de volgende POS-bewerkingen gebruikt: Alle producten verzenden en Geselecteerde producten verzenden. Hierdoor kan de medewerker van de winkel de verzendlocatie selecteren waar de order of orderregel kan worden afgehandeld. Standaard is de verzendlocatie het magazijn van verzending dat is gekoppeld aan de winkel. De medewerker van de winkel kan deze locatie echter wijzigen en een winkel selecteren die is gedefinieerd in de winkellocatorgroep die aan de winkel is toegewezen.

De mogelijkheid om afleveradressen te selecteren, blijft ongewijzigd.

De verzendmethoden die kunnen worden gebruikt om te voldoen aan de orderregel zijn gebaseerd op de configuratie van geldige leveringsmethoden voor producten en adressen. Omdat de regels over geldige leveringsmethoden alleen worden beheerd in Headquarters, voert de POS-client een realtime aanroep uit om de geldige leveringsmethoden voor een verzendregel op te halen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]