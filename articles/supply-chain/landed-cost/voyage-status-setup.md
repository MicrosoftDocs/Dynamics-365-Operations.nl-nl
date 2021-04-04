---
title: Status van transport instellen
description: In dit onderwerp wordt beschreven hoe u de statuswaarden kunt bepalen die gebruikers aan transporten kunt toewijzen.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500881"
---
# <a name="voyage-status-setup"></a>Status van transport instellen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Op de pagina **Transportstatussen** kunt u de set statuswaarden instellen die gebruikers kunnen toewijzen aan transporten. Gebruikers kunnen statuswaarden voor transporten toewijzen aan alle niveaus van een transport: transport, verzendcontainer, folio, inkooporder en artikel (inkoopregels en transferorderregels). Deze worden voor twee doelen gebruikt:

- De gebruiker informeren over de status van transport, verzendcontainer, folio, inkooporder of artikel (inkoopregels en transferorderregels).
- Het gebruik beperken van het kostengebied door wijziging of verwijdering te voorkomen.

Als u uw transportstatussen wilt instellen, gaat u naar **Francoprijzen \> Instellen \> Transportstatussen**. Hier kunt u statussen toevoegen, verwijderen en bewerken met de knoppen in het actievenster.

Elk kostengebied heeft een eigen set en hiërarchie van transportstatussen. Daarom moet u op de pagina **Transportstatussen**, in het veld **Kostengebied**, eerst het kostengebied selecteren waarvoor u transportstatussen wilt weergeven of maken. Stel vervolgens voor elke transportstatus de velden in die in de volgende tabel worden beschreven. De status van een transport kan ook automatisch door systeemgebeurtenissen worden gewijzigd, zoals regels die zijn vastgesteld met behulp van het traceringscontrolecentrum.

| Veld | Beschrijving |
|---|---|
| Reisstatus | Voer de naam van de transportstatus in. |
| Beschrijving | Voer een beschrijving van de transportstatus in. |
| Wijzigen | Schakel dit selectievakje in als gebruikers transporten met deze status mogen wijzigen. |
| Delete | Schakel dit selectievakje in als gebruikers transporten met deze status mogen verwijderen. |
| Verplicht | Schakel dit selectievakje in om de transportstatus verplicht te maken, zodat deze niet kan worden overgeslagen. |
| Ouder | Gebruik dit veld om een hiërarchie tussen de statuswaarden te bepalen. Transportstatussen kunnen alleen in neerwaartse richting in de hiërarchie worden gewijzigd (handmatig of automatisch), van een bovenliggende status naar een van de onderliggende statussen.

> [!NOTE]
> U hoeft alleen de specifieke transportstatussen in te stellen die uw organisatie gebruikt. Standaard transportstatussen zijn onder andere *Bevestigd*, *Goederen in transit*, *Ontvangen*, *Gereed voor kostprijsberekening* en *Kostprijs berekend*. Er kunnen echter ook andere statussen aanwezig zijn.
