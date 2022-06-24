---
title: Orders verzenden vanuit een andere winkel met behulp van de verzendfunctie Toeslag
description: In dit artikel wordt de verzendfunctie Toeslag beschreven.
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
ms.openlocfilehash: d73a21bfe9a284bd6e222e73bb0250648912b230
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863508"
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