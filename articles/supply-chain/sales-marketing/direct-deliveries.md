---
title: Directe leveringen
description: Dit artikel bevat informatie over directe leveringen. Directe leveringen zijn leveringen die rechtstreeks van de leverancier naar uw klant worden verzonden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c4a695c591865c52ad5ee6d37a515139f58bf8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "312273"
---
# <a name="direct-deliveries"></a>Directe leveringen

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over directe leveringen. Directe leveringen zijn leveringen die rechtstreeks van de leverancier naar uw klant worden verzonden.

Directe leveringen zorgen voor een kortere leveringstijd en lagere opslagkosten van de voorraad, omdat u de producten niet in uw magazijn bewaart voordat deze naar de klant worden verzonden.  

Op de pagina **Verkooporder** kunt u directe leveringen maken. Maak eerst een verkooporder en orderregels. Selecteer vervolgens in het actievenster op het tabblad **Verkooporder** de optie **Directe levering**. Geef ten slotte de regels op die moeten worden verwerkt als een directe levering. Er wordt nu een koppeling gemaakt tussen de verkooporderregels voor directe levering en de bijbehorende inkooporderregels.  

**Opmerking:** als een deel van de bestelde hoeveelheid al is geleverd, moet u de resterende hoeveelheid splitsen. Maak een nieuwe regel voor de hoeveelheid die rechtstreeks moet worden geleverd en trek die hoeveelheid af van de hoeveelheid op de oorspronkelijke regel. Als de oorspronkelijke hoeveelheid bijvoorbeeld 15 is en er zijn vijf eenheden geleverd, dan moet u een nieuwe regel maken voor de resterende hoeveelheid van 10, en vervolgens de oorspronkelijke hoeveelheid verminderen met dat bedrag.  

Nadat u de koppeling van de directe levering tussen de verkooporderregels en de inkooporderregels hebt gemaakt, kunt u de verkooporder bijwerken met behulp van een pakbon. Voer een update van de pakbon of een update van de factuur van de inkooporder uit. U moet een factuurupdate maken van de verkooporder via de pagina **Verkooporder**. Een factuurupdate kan er niet voor zorgen dat de hoeveelheid op de verkooporder groter is dan de hoeveelheid die is geregistreerd als ontvangen. Een verkooporderregel bevat bijvoorbeeld 10 stuks, maar slechts 5 stuks van de verkooporderregel zijn met behulp van een pakbon bijgewerkt. Als u **Alle** selecteert in de lijst **Hoeveelheid** wanneer u de factuur voor de verkooporder bijwerkt, wordt de factuur alleen bijgewerkt voor de artikelen die fysiek zijn ontvangen, of die zijn bijgewerkt via een pakbon. De gehele verkooporderregel wordt niet bijgewerkt.

## <a name="delivery-date"></a>Leveringsdatum
Wanneer u het veld **Gevraagde ontvangstdatum** op de verkooporderregel bijwerkt, wordt het veld **Leveringsdatum** op de bijbehorende inkooporderregel ook bijgewerkt. Wanneer u het veld **Bevestigd** op de inkooporderregel bijwerkt, worden de velden **Bevestigde ontvangstdatum** en **Bevestigde verzenddatum** op de bijbehorende verkooporderregel eveneens bijgewerkt.

## <a name="delivery-address"></a>Afleveradres
Het afleveradres voor een inkooporder is meestal het adres van het bedrijf. Wanneer u echter een directe levering maakt, voert u het adres van de klant als afleveradres in. Als u het afleveradres op een inkooporderregel van het leveringstype **Directe levering** wijzigt, wordt het afleveradres voor de bijbehorende verkooporderregel ook bijgewerkt. Op dezelfde manier wordt het afleveradres op de inkooporder bijgewerkt als het afleveradres op de verkooporderregel ook wordt bijgewerkt.

## <a name="deleting-order-lines"></a>Orderregels verwijderen
Als u een verkooporderregel met een leveringstype **Directe levering** probeert te verwijderen, wordt in een berichtvak weergegeven dat er inkooporderregels zijn gekoppeld aan de regel. Als de verkooporderregel gedeeltelijk is geleverd, kunt u de verkooporderregel of de gekoppelde inkooporderregels niet verwijderen.

## <a name="warehouse"></a>Magazijn
Wanneer u een directe levering maakt, komen de artikelen die verkoopt nooit fysiek in uw magazijn. U moet echter nog steeds een magazijn opgeven op de verkooporderregel. Evenzo kunnen orderverzamelvereisten worden opgegeven voor de artikelmodelgroep voor het artikel. Echter, aangezien artikelen nooit fysiek bij uw magazijn aankomen, worden deze vereisten genegeerd wanneer de+ verkooporder een directe levering is.



