---
title: Inleiding tot activa
description: Dit onderwerp bevat een overzicht van activa in Activabeheer.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f2737824af92d15d71c75f4e0a0700e6fa93741
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337046"
---
# <a name="introduction-to-assets"></a>Inleiding tot activa

[!include [banner](../../includes/banner.md)]

 

Dit onderwerp bevat een overzicht van activa in Activabeheer. Een *activum* is elk type apparatuur, zoals een machine of een machineonderdeel, waarvoor onderhoud, service of reparatie nodig is.

Een activum wordt automatisch bijgewerkt met gerelateerde informatie. Deze informatie kan bijvoorbeeld betrekking hebben op nieuwe of bijgewerkte werkorders. U kunt activa maken met de menuopdracht **Alle activa** of de menuopdracht **Activa in behandeling**. In dit onderwerp wordt uitgelegd hoe u activat maakt met de menuopdracht **Alle activa**. Zie [Activa maken op basis van inkooporders](../objects/create-objects-based-on-purchase-orders.md) voor informatie over het maken van activa met behulp van de menuopdracht **Activa in behandeling**.

## <a name="all-assets"></a>Alle activa

Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**. De lijstpagina **Alle activa** bevat alle activa en een deel van de informatie die aan hen is gerelateerd. Als u alleen actieve activa wilt weergeven, selecteert u **Actieve activa**. Als u alleen activa wilt weergeven die zijn geïnstalleerd op de functionele locaties waarmee u als onderhoudsmedewerker bent verbonden, selecteert u **Mijn actieve activa**. (Deze relatie is ingesteld op de pagina **Medewerkers**. Zie [Onderhoudsmedewerkers en medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor meer informatie.)

Selecteer in de rasterweergave **Alle activa** een koppeling in de kolom **Activum** om de details van de geselecteerde record weer te geven. Als u de record wilt bewerken, selecteert u de knop **Bewerken**. De detailweergave bevat gedetailleerde informatie die is gerelateerd aan het activum. Een deelvenster **Verwante informatie** aan de rechterkant bevat aanvullende aan het activum gerelateerde informatie. Vouw het deelvenster uit om de gerelateerde informatie voor het geselecteerde activum weer te geven.

De knoppen in het actievenster zijn geordend op tabbladen. In de volgende tabel worden kort de knoppen beschreven die betrekking hebben op Activabeheer.

| Knopnaam          | Beschrijving                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bewerken                 | Het geselecteerde activum bewerken.                                                                                                                                         |
| Nieuw                  | Een nieuw activum maken.                                                                                                                                                |
| Verwijderen               | Het geselecteerde activum verwijderen.                                                                                                                                       |
| Activum verplaatsen           | Activa verplaatsen naar een andere activastructuur of naar een andere locatie in dezelfde activastructuur.                                                                                         |
| Activum vervangen        | Eén onderliggend activum in een activahiërarchie vervangen door een ander activum.                                                                                                  |
| Activum installeren        | Een activum installeren op een functionele locatie.                                                                                                                          |
| Activum kopiëren           | Een activahiërarchie kopiëren naar een ander activum.                                                                                                                          |
| Aanvragen             | Open de lijstpagina **Actieve aanvragen**, waar u onderhoudsaanvragen kunt bekijken die voor het geselecteerde activum zijn gemaakt.                                                                         |
| Gebeurtenishistorie        | Een overzicht weergeven van de verschillende registraties die zijn uitgevoerd voor het activum.                                                                                                         |
| Activumstuklijst            | Een lijst weergeven met alle artikelen (reserveonderdelen en andere artikelen) die voor een activum worden gebruikt.                                                                                  |
| Werkorders          | Open de lijstpagina **Actieve werkorders**, waar u werkorders voor het activum kunt weergeven.                                                                                        |
| Controlelijst            | Een overzicht weergeven van controlelijsten en metingen voor onderhoud die voor het activum zijn geregistreerd.                                                                                                 |
| Uitvaltijd voor onderhoud | Registraties van uitvaltijd voor onderhoud maken of weergeven.                                                                                                       |
| Projecttransacties | Alle geboekte transacties weergeven die zijn gerelateerd aan werkorders die voor het activum zijn gemaakt.                                                                                       |
| Activametingen       | Activametingen voor het activum maken of weergeven.                                                                                                               |
| Onderhoudsschema | Open de lijstpagina **Onderhoudsschema**, waar u onderhoudsplannen, onderhoudsaanvragen en onderhoudsronden kunt weergeven die aan het activum zijn gekoppeld en die de status **Gemaakt** hebben. |
| Activastatus bijwerken   | De levenscyclusstatus van het activum bijwerken. U kunt meerdere activa selecteren op de lijstpagina **Alle activa** en vervolgens de levenscyclusstatus van alle activa tegelijk bijwerken.              |
| Logboek voor levenscyclusstatus  | Een logboek openen waarin de levenscyclusstatussen van het geselecteerde activum worden weergegeven.                                                                                                                 |
| Activadocumenten      | Een lijst met documenten weergeven die aan een activum zijn gekoppeld. Deze documenten worden ingesteld in **Activabeheer** \> **Instellingen** \> **Activadocumenten**.                 |
| Kenmerken           | Activakenmerken maken of weergeven.                                                                                                                             |
| Afbeelding                | Een afbeelding selecteren voor het activum.                                                                                                                                   |
| Bovenliggende activa        | Historie van bovenliggende activa voor het geselecteerde activum weergeven.                                                                                                                |
| Functionele locaties | Historie van functionele locatie voor het geselecteerde activum weergeven.                                                                                                          |
| Toestandsbeoordeling | Metingen van toestandsbeoordelingen voor het activum registreren.                                                                                                         |
| Fouten               | Open de lijstpagina **Activafouten**, waar u fouten kunt weergeven die voor het activum zijn geregistreerd.                                                                                             |
| Kostenbeheer         | Budgetkosten en werkelijke kosten voor het activum vergelijken.                                                                                                              |
| Uurcontrole         | Prognose-uren en werkelijke uren voor het activum met elkaar vergelijken.                                                                                                              |
| KPI's voor activa           | KPI's (Key Performance indicators) voor het activum berekenen en weergeven.                                                                                              |
| Functietypen            | Een overzicht weergeven van de huidige standaard taaktypen voor het activum.                                                                                                            |
| Typen kritieke eigenschappen    | Typen kritieke eigenschappen van het activum weergeven of bijwerken.                                                                                                                              |
| Reserveonderdelen          | Een lijst met goedgekeurde en alternatieve reserveonderdelen weergeven die voor het activum kunnen worden gebruikt.                                                                               |
| Activaverbruik    | Een rapport afdrukken waarin verbruiksregistraties voor het activum worden weergegeven.                                                                                                |
| Activafout          | Een rapport afdrukken waarin foutregistraties voor het activum worden weergegeven.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]