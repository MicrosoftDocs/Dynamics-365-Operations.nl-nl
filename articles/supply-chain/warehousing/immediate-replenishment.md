---
title: Directe aanvulling
description: In dit onderwerp wordt beschreven hoe u directe aanvulling kunt gebruiken voor het aanvullen van voorraad wanneer met een richtlijn van de locatie voorraad niet kan worden toegewezen.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c69a9c9fd595280ba4f05a11409a3e672e4b1691
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425835"
---
# <a name="immediate-replenishment"></a>Directe aanvulling

[!include [banner](../includes/banner.md)]

Met directe aanvulling kunt u de voorraad meteen aanvullen wanneer met een richtlijn van de locatie voorraad niet kan worden toegewezen. De aanvulling is gebaseerd op één regel in de instellingen van de locatie-instructie. Aanvulling van die eenheid vindt onmiddellijk plaats als voorraad niet voorhanden is in de maateenheid die is opgegeven in die regel.

Directe aanvulling biedt een alternatief voor de methode waarbij de toewijzing van de voorraad is gebaseerd op meer regels in de locatie-instructie en waar de vraag aan het einde van de toewijzing wordt opgeteld en aangevuld in de maateenheid die is opgegeven door de laatste regel van de locatie-instructie.

De voordelen van onmiddellijke aanvulling zijn dat de aanvulling kan worden beperkt door specifieke eenheden en de hoeveelheid kan worden doorgestuurd naar specifieke locaties.

## <a name="business-scenario"></a>Bedrijfsscenario

U hebt bijvoorbeeld een magazijn met afzonderlijke orderverzamelgebieden voor de maateenheden 'doos' en 'stuk'. U wilt de orderverzamelprocedure optimaliseren door zoveel mogelijk dozen te verzamelen en daarna de resterende hoeveelheid die kleiner is dan een doos te verzamelen in het gebied 'stuk'.

In dit geval kunt u directe aanvulling gebruiken. In de locatie-instructie kunt u directe aanvulling instellen voor dozen zodat aanvulling op vraag wordt gebruikt zodra er een tekort is aan dozen die kunnen worden verzameld voor de vraaghoeveelheid. Op deze manier optimaliseert u het orderverzamelproces en omvat de orderverzameling zoveel mogelijk dozen. Directe aanvulling zorgt voor aanvulling van de dozen en de vraag wordt niet doorgegeven, zodat de hoeveelheden worden verzameld in de maateenheid 'stuk'. Met andere woorden, alleen de hoeveelheden die moeten worden verzameld in de maateenheid 'stuk' (dat wil zeggen hoeveelheden die kleiner zijn dan een doos) worden verzameld uit het gebied 'stuk'. Als er een tekort optreedt in het gebied 'doos', kunt u zo veel mogelijk dozen buiten de totale vraag ophalen. De resterende hoeveelheden wordt vervolgens worden opgehaald uit het gebied 'stuk'.

## <a name="where-it-applies"></a>Waar van toepassing

Directe aanvulling wordt gebruikt tijdens het uitvoeren van een wave als toewijzing mislukt voor een locatie-instructieregel waarvoor een aanvullingssjabloon is ingesteld.

## <a name="set-up-immediate-replenishment"></a>Directe aanvulling instellen

- Ga naar **Magazijnbeheer** \> **Instellen** \> **Locatie-instructies** en selecteer vervolgens op het tabblad **Regels** in de lijst **Sjabloon voor directe aanvulling** een aanvullingssjabloon voor de wavevraag.

De aanvullingssjabloon wordt toegepast als de locatie-instructieregel een specifieke maateenheid niet kan toewijzen.

## <a name="troubleshooting"></a>Problemen oplossen

Als directe aanvulling wordt geselecteerd voor een locatie-instructieregel, maar geen aanvullingswerk wordt gegenereerd als u vraagaanvullingssjablonen voor die locatie-instructieregel gebruikt, moeten twee mogelijke oorzaken worden onderzocht:

- Zorg ervoor dat de toegepaste vraagaanvullingssjabloon is ingesteld om de juiste locatiesjablonen en werksjablonen te gebruiken van het type **Aanvulling**.
- Zorg ervoor dat er voldoende voorhanden voorraad beschikbaar is op de locaties waar de vraagaanvullingssjabloon naar voorhanden voorraad voor aanvulling zoekt.
