---
title: Algemene parameters voor mobiele apparaten
description: In dit onderwerp wordt beschreven hoe u instellingen voor mobiele apparaten instelt op de pagina Parameters voor magazijnbeheer.
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0ae04c86ff1eafb649fcef7c34ace66bdc3e5cb8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679160"
---
# <a name="global-mobile-device-parameters"></a>Algemene parameters voor mobiele apparaten

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u algemene parameters voor magazijnbeheer instelt die van invloed zijn op de interactie tussen het systeem en mobiele apparaten.

Voor meer informatie over het instellen van magazijnmedewerkers zie [Magazijnmedewerkers beheren](manage-warehouse-workers.md). Zie voor meer informatie over de afhandeling van nummerplaten op mobiele apparaten [Nummerplaat ontvangen via de mobiele app Warehouse Management](warehousing-mobile-device-app-license-plate-receiving.md). Voor meer informatie over de processen voor cyclustelling zie [Cyclustelling](cycle-counting.md) en [Voorbeeldscenario's voor cyclustelling](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Open de pagina Parameters voor magazijnbeheer

Om de pagina **Parameters voor magazijnbeheer** te openen, gaat u naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**. Vervolgens kunt u de velden instellen die betrekking hebben op werken met mobiele apparaten, zoals wordt beschreven in het volgende onderdeel van dit onderwerp.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Sneltabblad Mobiele apparaten op het tabblad Algemeen

De algemene instellingen voor mobiele apparaten zijn te vinden op het sneltabblad **Mobiele apparaat** van het tabblad **Algemeen** van de pagina **Parameters voor magazijnbeheer**. De volgende velden zijn beschikbaar.

| Veld | Beschrijving |
|---|---|
| Notitietype voor mobiel apparaat | Selecteer het type informatie dat wordt getoond aan werknemers bij het verzamelen van verkooporders. |
| Gescande hoeveelheidslimiet | Voer de maximale artikelhoeveelheid in die een werknemer tijdens elke sessie kan scannen met een menu-item op een mobiel apparaat dat bij **Procedure voor het maken van werk** de waarde *Correctie in* heeft. Dit veld is niet invloed op scans die worden uitgevoerd met een ander type menu-item. |
| Logboekregistratie van mobiel apparaat gebruiken | Stel deze optie in op *Ja* om een logboek bij te houden van de aanmeldingshistorie van werknemers. Om het logboek weer te geven, gaat u naar **Sessie werkgebruikers \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Sessies werkgebruikers**. |
| Aantal opgeslagen fouten | Voer het maximumaantal foutrecords in dat het systeem moet opslaan. Om het foutenlogboek weer te geven, gaat u naar **Sessie werkgebruikers \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Sessies werkgebruikers**. |
| Standaardjournaal voor magazijnoverboeking | Selecteer het journaal dat wordt gebruikt wanneer werknemers een mobiel apparaat gebruiken om producten tussen magazijnen te verplaatsen. |
| Registratie van inkooporderregel toestaan indien Bij externe herziening | Stel deze optie in op *Ja* als werknemers met een mobiel apparaat orderregels moeten kunnen registreren voor inkooporders die bij **Goedkeuringsstatus** de status *Bij externe herziening* hebben. Stel deze optie in op *Nee* om niet toe te staan dat werknemers regels te registreren voor inkooporders waarvoor externe controle wordt uitgevoerd. |
| RSAT-ondersteuning inschakelen | Het veld schakelt de taakvalidator in voor de mobiele app Warehouse Management. Hierna wordt elke stap die de app uitvoert, gelogd en gevalideerd. Aangezien dit proces het systeem aanzienlijk langzamer kan maken, raden we aan de validator alleen tijdens het testen in te schakelen. Schakel deze nooit in voor een productieomgeving. |
