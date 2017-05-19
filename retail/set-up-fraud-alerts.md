---
title: Fraudewaarschuwingen instellen
description: "Dit onderwerp wordt beschreven hoe u regels instelt om klantenservice medewerkers van potentieel frauduleuze informatie te waarschuwen wanneer bestellingen zijn verwerkt. U kunt speciale codes definiëren die automatisch of handmatig verdachte orders stopzetten."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ddcf68b9d9d35d63cb092225d468dd4a6a3d4446
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-fraud-alerts"></a>Fraudewaarschuwingen instellen

[!include[banner](includes/banner.md)]


Dit onderwerp wordt beschreven hoe u regels instelt om klantenservice medewerkers van potentieel frauduleuze informatie te waarschuwen wanneer bestellingen zijn verwerkt. U kunt speciale codes definiëren die automatisch of handmatig verdachte orders stopzetten. 

Voordat u fraudecontroleregels instelt en gebruikt, moet u fraudecontrole inschakelen en de elementaire fraudecontrolewaarden definiëren in de parameters van het callcenter. Er zijn twee typen frauderegels:

-   **Statische regels** gebruiken een specifieke waarde, zoals een telefoonnummer dat op de zwarte lijst is geplaatst.
-   **Dynamische regels** kunnen worden samengesteld uit variabelen en voorwaarden.

Voordat u een dynamische regel maakt, moet u de variabelen en de voorwaarden maken die bepalen op welke producten de regel van toepassing is en wanneer de regel moet worden toegepast. U wilt bijvoorbeeld een regel maken om te vereisen dat elke verkooporder die klant 1202 plaatst en die 1.000,00 of meer waard is, in de wachtstand moet worden geplaatst tot de klantbetaling kan worden gecontroleerd. In dit geval zijn de variabelen klant 1202 en een ordertotaal van 1,000.00. De voorwaarde geeft aan dat als klant 1202 een order plaatst en het totale bedrag van de order gelijk is aan of groter is dan 1000,00, de verkooporder in de wachtstand moet worden geplaatst tot
klantbetaling kan worden gecontroleerd.




