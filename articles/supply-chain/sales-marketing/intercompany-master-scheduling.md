---
title: Intercompany-hoofdplanning
description: In dit artikel wordt de intercompany-hoofdplanning beschreven
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4993f981b268127af7c9259aa0e73a8e4a75015a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851444"
---
# <a name="intercompany-master-scheduling"></a>Intercompany-hoofdplanning

[!include [banner](../../includes/banner.md)]

Intercompany-hoofdplanning is de manier waarop u behoeften berekent en geplande intercompany-orders in diverse interne bedrijven genereert. De intercompany-hoofdplanning wordt uitgevoerd over het aantal iteraties dat u opgeeft. Om Microsoft Dynamics 365 Supply Chain Management de intercompany-hoofdplanning te laten uitvoeren moet u in elk van de intercompany-bedrijven een hoofdplanning opstellen. Dit brengt een aantal iteraties met zich mee waarin door Microsoft Dynamics 365 Supply Chain Management automatisch een intercompany-inkooporder wordt gemaakt, waardoor automatisch een intercompany-verkooporder wordt gemaakt, wat vervolgens weer leidt tot nieuwe aanvragen.

U stelt de intercompany-hoofdplanning en de intercompany-planningsvolgorde in de parameters van de **Hoofdplanning** in elk van de intercompany-bedrijven in.

Als u de vraag in de gehele intercompany-keten wilt doorvoeren, moet u parameters instellen om er zeker van te zijn dat de geplande inkooporders automatisch worden gefiatteerd, dat wil zeggen dat de tijd en hoeveelheid in de orders niet meer kunnen worden gewijzigd. Stel de **Time fence voor fiattering** in voor de behoefteplanningsgroep of voor de **Time fence voor fiattering** in het hoofdplan. Als er geen **Time fence voor fiattering** is ingesteld, worden er niet automatisch intercompany-inkooporders gemaakt. Alleen de eerste uitvoering van de hoofdplanning resulteert in geplande orders. Omdat er echter geen intercompany-inkooporder wordt gemaakt, wordt er geen intercompany-verkooporder gemaakt en worden er dus geen intercompany-inkooporders meer gemaakt enzovoort.

Wanneer u de intercompany-hoofdplanning start, voert Microsoft Dynamics 365 Supply Chain Management één hoofdplanning in elk intercompany-bedrijf uit, wordt er vervolgens een tweede hoofdplanning in elk intercompany-bedrijf uitgevoerd enzovoort, totdat het opgegeven aantal iteraties is bereikt. Er kunnen maximaal 30 iteraties worden opgegeven. Hoe meer iteraties u kiest, des te langer duurt het om de planning uit te voeren.

Omdat de hoofdplanning in de bedrijven wordt aangestuurd door de intercompany-planningreeks, dat wil zeggen de volgorde waarin door het programma prioriteiten aan de hoofdplanningen tussen de intercompany-bedrijven worden toegewezen, kunt u de intercompany-hoofdplanning vanuit een van de intercompany-bedrijven starten. Omdat de volgorde waarin de hoofdplanning wordt uitgevoerd in de bedrijven wordt bepaald door de schemareeks, is het niet van belang waar de intercompany-hoofdplanning wordt gestart. In elke iteratie wordt het huidige bedrijf als laatste uitgevoerd.

> [!NOTE]
> De beste manier is om de intercompany-hoofdplanning vanuit één Microsoft Dynamics 365 Supply Chain Management-bedrijf te laten starten.

Op de pagina **Intercompany-hoofdplanning** kunt u een hoofdplanningsreeks starten, waarmee een hoofdplanning de eerste keer wordt gestart met de methode voor het bijwerken van de behoeftenberekening die u voor de eerste iteratie voor alle intercompany-bedrijven hebt geselecteerd. Bij de volgende iteraties wordt de tweede methode gebruikt die u hebt geselecteerd voor de volgende iteratie. Deze methode wordt toegepast totdat het aantal opgegeven iteraties is bereikt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
