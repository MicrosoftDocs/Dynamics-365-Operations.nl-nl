---
title: Een order vanuit een andere winkel verzenden
description: In dit onderwerp wordt de verzendfunctie Toeslag beschreven.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: nl-nl
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a>Een order vanuit een andere winkel verzenden

Met de verzendfunctie Toeslag in Dynamics 365 for Retail kunnen klantorders in de ene winkel worden geplaatst en vanuit een andere winkel worden verzonden. Klantorders in de POS-client (Point Of Sale) ondersteunen meerdere afhandelingsopties. Enkele voorbeelden van afhandelingsopties:
-   Ophalen uit dezelfde locatie op een andere datum.
-   Ophalen uit een andere locatie op dezelfde of een andere datum.
-   Verzenden vanuit het standaardmagazijn van verzending die is toegewezen aan de winkel en op een bepaalde datum leveren.

Met de verzendfunctie Toeslag worden de volgende POS-bewerkingen gebruikt: Alle producten verzenden en Geselecteerde producten verzenden. Hierdoor kan de medewerker van de winkel de verzendlocatie selecteren waar de order of orderregel kan worden afgehandeld. Standaard is de verzendlocatie het magazijn van verzending dat is gekoppeld aan de winkel. De medewerker van de winkel kan deze locatie echter wijzigen en een winkel selecteren die is gedefinieerd in de winkellocatorgroep die aan de winkel is toegewezen. 

De mogelijkheid om afleveradressen te selecteren, blijft ongewijzigd. 

De verzendmethoden die kunnen worden gebruikt om te voldoen aan de orderregel zijn gebaseerd op de configuratie van geldige leveringsmethoden voor producten en adressen. Omdat de regels over geldige leveringsmethoden alleen worden beheerd in Detailhandel Hoofdkantoor, voert de POS-client een real-time aanroep uit om de geldige leveringsmethoden voor een verzendregel op te halen. 

