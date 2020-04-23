---
title: Nummerplaat ontvangen via de Warehouse Mobile App
description: In dit onderwerp wordt uitgelegd hoe u de Warehouse Mobile App kunt instellen om het ontvangstproces met nummerplaat in de fysieke voorraad te ondersteunen.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261318"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a>Nummerplaat ontvangen via de Warehouse Mobile App

In dit onderwerp wordt uitgelegd hoe u de Warehouse Mobile App kunt instellen om het ontvangstproces met nummerplaat in de fysieke voorraad te ondersteunen.

Met deze functie kunt u snel de ontvangst van de inkomende voorraad vastleggen die is gerelateerd aan een voorschotbericht (advance shipping notice, ASN). Het systeem maakt automatisch een ASN wanneer magazijnbeheerprocessen worden gebruikt om een transferorder te verzenden. Voor het inkooporderproces kan een ASN handmatig worden vastgelegd of kan deze automatisch worden geïmporteerd met behulp van een inkomend ASN-gegevensentiteitproces.

De ASN-gegevens worden gekoppeld aan ladingen en zendingen via *de verpakkingsstructuren*, waarbij pallets (bovenliggende nummerplaten) dozen kunnen bevatten (geneste nummerplaten).

> [!NOTE]
> Om het aantal voorraadtransacties te verminderen wanneer de verpakkingsstructuren met geneste nummerplaten worden gebruikt, registreert het systeem de fysieke voorhanden voorraad op de bovenliggende nummerplaat. Om de verplaatsing van de fysieke voorhanden voorraad van de bovenliggende nummerplaat naar de geneste nummerplaat te activeren, op basis van de verpakkingsstructuurgegevens, moet het mobiele apparaat een menuopdracht geven die is gebaseerd op het werkaanmaakproces *Verpakken naar geneste nummerplaten*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>De pagina met het ontvangstoverzicht weergeven of overslaan

U kunt de functie *Bepalen of de pagina met het ontvangstoverzicht wordt weergegeven op mobiele apparaten* gebruiken om te profiteren van de extra gedetailleerde magazijnbeheer-appstroom als onderdeel van het nummerplaatontvangstproces.

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Bepalen of de pagina met het ontvangstoverzicht wordt weergegeven op mobiele apparaten*

Als deze functie is ingeschakeld, bevatten de menuopdrachten van het mobiele apparaat voor het ontvangen en opslaan van nummerplaten de instelling **Pagina met het ontvangstoverzicht weergeven**. Deze instelling heeft de volgende opties:

- **Een gedetailleerd overzicht weergeven**: tijdens het ontvangen van een nummerplaat krijgen de werknemers een extra pagina te zien waarop de volledige ASN-informatie wordt weergegeven.
- **Het overzicht overslaan**: werknemers kunnen de volledige ASN-informatie niet zien. Magazijnmedewerkers kunnen ook geen beschikkingscode instellen of uitzonderingen toevoegen tijdens het ontvangstproces.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn

Een ontvangstproces voor een nummerplaat kan niet worden gebruikt als een ASN een nummerplaat-id bevat die al bestaat en fysieke voorraadgegevens bevat op een magazijnlocatie anders dan de magazijnlocatie waar de nummerplaatregistratie wordt uitgevoerd.

Voor transferorderscenario's waarbij het transitmagazijn geen nummerplaten volgt (en dus ook geen fysieke voorhanden voorraad per nummerplaat bijhoudt), kunt u de functie *Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn* gebruiken om fysieke voorraadupdates te voorkomen in nummerplaten in transit.

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn*

Voer de volgende stappen uit om de functionaliteit te beheren wanneer deze functie beschikbaar is.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het tabblad **Algemeen** op het sneltabblad **Nummerplaten** het veld **Beleid voor nummerplaten transitmagazijn** in op een van de volgende waarden:

    - **Hergebruik toestaan van niet-getraceerde nummerplaat**: het systeem werkt op dezelfde manier als wanneer functie de *Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn* niet beschikbaar is. Deze waarde is de standaardinstelling wanneer u de functie voor het eerst activeert.
    - **Hergebruik verhinderen van niet-getraceerde nummerplaat**: alleen voorhanden updates die zijn gerelateerd aan een geleverde nummerplaat worden toegestaan in het doelmagazijn totdat de transferorder is ontvangen.

## <a name="more-information"></a>Meer informatie

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Zie [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md) voor meer informatie over menuopties voor mobiele apparaten.
