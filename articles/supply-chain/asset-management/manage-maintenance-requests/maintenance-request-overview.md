---
title: Onderhoudsverzoeken
description: Dit artikel bevat een overzicht van het beheer van onderhoudsverzoeken in Activabeheer
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 488b6505aba246aa3a6ea69436514a274403bf49
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015633"
---
# <a name="maintenance-requests"></a>Onderhoudsaanvragen

[!include [banner](../../includes/banner.md)]

Onderhoudsverzoeken zijn notities of verklaringen die zijn gemaakt om een manager of planner te informeren dat een activum mogelijk onderhoud of reparatie nodig heeft, maar zonder dat een werkorder wordt gemaakt. Als de inhoud van een onderhoudsverzoek als geldig wordt beschouwd, kan een werkorder worden gemaakt op basis van het onderhoudsverzoek.

Onderhoudsverzoeken kunnen worden gemaakt voor elk activum in Activabeheer. Er kunnen verschillende soorten onderhoudsverzoeken worden gemaakt, afhankelijk van de manier waarop uw bedrijf onderhoudsverzoeken gebruikt. Hieronder vindt u enkele voorbeelden:

- Onderhoudsaanvragen
- Opmerkingen
- Correcties of verbeteringen
- Investeringen
- Depotreparatie (dit type wordt gebruikt wanneer u activa van een andere locatie ontvangt, zodat u een onderhouds- of reparatietaak kunt uitvoeren, en het activum retourneert nadat de taak is voltooid.)

## <a name="view-maintenance-requests"></a>Onderhoudsverzoeken weergeven

Als u onderhoudsaanvragen wilt weergeven, selecteert u **Activabeheer** \> **Onderhoudsverzoeken** \> **Alle onderhoudsverzoeken**, **Actieve onderhoudsverzoeken** of **De onderhoudsverzoeken van mijn functionele locatie**. Elke lijstpagina bevat een deel van de informatie die is gerelateerd aan een onderhoudsverzoek.

![Onderhoudsverzoeken weergeven.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Gebruik de pagina met de lijst **De onderhoudsverzoeken van mijn functionele locatie** om een lijst met onderhoudsverzoeken weer te geven die functionele locaties bevatten waaraan u bent gerelateerd als werknemer of activa die zijn geïnstalleerd op functionele locaties waaraan u bent gerelateerd als werknemer. (Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor informatie over het instellen van onderhoudsmedewerkers en functionele locaties.)
> 
> Hoewel klantaccountinformatie beschikbaar is in Activaservicebeheer (extern onderhoud), is deze niet beschikbaar in Activabeheer (intern onderhoud).

Als u de detailweergave van een record wilt openen, selecteert u op de pagina met de lijst **Alle onderhoudsverzoeken** in rasterweergave een koppeling in kolom **Onderhoudsverzoek**.

![Details van onderhoudsverzoek weergeven.](media/02-manage-maintenance-requests.png)

De knoppen in het actievenster zijn geordend op tabbladen. In de volgende tabel worden kort de knoppen beschreven die betrekking hebben op Activabeheer.

| Knopnaam                      | Beschrijving |
|----------------------------------|-------------|
| Bewerken                             | Bewerk het geselecteerde artikel onderhoudsverzoek. |
| Nieuw                              | Maak een nieuw onderhoudsverzoek. |
| Verwijderen                           | Verwijder het geselecteerde onderhoudsverzoek. |
| Werkordergroep                  | Verbind het geselecteerde onderhoudsverzoek aan een werkordergroep. |
| Werkorder                       | Maak een werkorder op basis van het geselecteerde onderhoudsverzoek. |
| Fout in activum                      | Klik op **Activafouten**, waar u een foutregistratie op het geselecteerde onderhoudsverzoek kunt maken. |
| Werkorders                      | Geen een lijst met alle werkorders weer die verbonden zijn aan het geselecteerde onderhoudsverzoek. |
| Status van onderhoudsverzoek bijwerken | Werk de status van het onderhoudsverzoek bij. |
| Logboek levenscyclusstatus              | Geef een logboek weer waarin de levenscyclusstatussen van het geselecteerde onderhoudsverzoek worden weergegeven. |
| Details van het onderhoudsverzoek      | Druk een rapport af met de details van het geselecteerde onderhoudsverzoek. |
| Geleend activum verzenden                  | Selecteer een geleend activum dat een tijdelijke vervanging moet zijn voor het activum dat is geselecteerd op het geselecteerde onderhoudsverzoek. |
| Een geleend activum retourneren                | Registreer het geleende activum als geretourneerd. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]