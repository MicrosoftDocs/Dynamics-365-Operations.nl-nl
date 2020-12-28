---
title: Inleiding op werkorders
description: Dit onderwerp bevat een overzicht van werkorders in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7997b4b9521b43e1e00cfa22f9df12a29582455a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425264"
---
# <a name="introduction-to-work-orders"></a>Inleiding tot werkorders

[!include [banner](../../includes/banner.md)]



Werkorders worden gebruikt voor het beheren van, het verstrekken van vereiste informatie voor en het registreren van verbruik voor onderhoudstaken. Elke werkorder kan een of meer werkordertaken bevatten en een of meer activa kunnen worden gekoppeld aan elke werkorder. Elke werkordertaak definieert een onderhoudstaak die is gepland voor het activum.

Werkorders kunnen op de volgende manieren worden gemaakt:

- Automatisch met [Schema voor onderhoudsplannen](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md), voor onderhoudsplannen op basis van kalenders die zijn ingesteld op "Automatisch maken".

- Automatisch met [Onderhoudsrondes plannen](../preventive-and-reactive-maintenance/maintenance-rounds.md), voor onderhoudsrondes op basis van kalenders die zijn ingesteld op "Automatisch maken".

- Op basis van [Onderhoudsplanning](../preventive-and-reactive-maintenance/maintenance-schedule.md) voor preventieve onderhoudstaken of onderhoudsverzoeken.

- Handmatig

- Vanuit **Alle onderhoudsverzoeken**, **Actieve onderhoudsverzoeken** of de pagina **De onderhoudsverzoeken van mijn functionele locatie**.

>[!NOTE]
>Werkordertaken die aan hetzelfde activum zijn gekoppeld, zijn gekoppeld aan dezelfde project-id.

## <a name="all-work-orders"></a>Alle werkorders

Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** en open de de lijstpagina **Alle werkorders**. Op deze pagina worden alle werkorders weergegeven plus een deel van de informatie die aan elk hiervan is gerelateerd.

In de onderstaande afbeelding ziet u een voorbeeld van de lijstpagina **Alle werkorders**.

![Figuur 1](media/01-work-orders.png)

Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Actieve werkorders** om een lijst met alleen actieve werkorders weer te geven. 

Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Mijn functionele locatie van onderhoudstaken voor werkorders** om een lijst met werkordertaken weer te geven die activa bevatten die zijn geïnstalleerd op functionele locaties waaraan u bent gerelateerd als werknemer. (De relatie tussen werknemers en functionele locaties wordt ingesteld op de pagina **Werknemers**. Zie [Onderhoudsmedewerkers en medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor meer informatie.)

Hier volgen enkele manieren waarop u de pagina **Alle werkorders** kunt gebruiken:

- Selecteer in de rasterweergave een koppeling in de kolom **Werkorder** om de detailweergave van de geselecteerde record weer te geven. Selecteer vervolgens **Bewerken** om de record te openen en te bewerken.

- De detailweergave bevat gedetailleerde informatie die is gerelateerd aan de werkorder.  

- Selecteer in de detailweergave het tabblad **Regels** om de werkordertaakdetails weer te geven of het tabblad **Koptekst** om werkorderdetails te bekijken.  

- Vouw het deelvenster **Gerelateerde informatie** aan de rechterkant van de pagina uit om aanvullende informatie over de geselecteerde werkorder weer te geven.

In de onderstaande afbeelding ziet u een voorbeeld van de detailweergave **Alle werkorders**.

![Figuur 2](media/02-work-orders.png)


De knoppen in het actievenster zijn geordend op tabbladen. In de volgende tabel worden kort de knoppen beschreven die betrekking hebben op Activabeheer:



| Knopnaam                     | Beschrijving                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bewerken                            | De geselecteerde werkorder bewerken.                                                                                                                                                                                                                                           |
| Nieuw                             | Nieuwe werkorder maken.                                                                                                                                                                                                                                                  |
| Delete                          | De geselecteerde werkorder verwijderen.                                                                                                                                                                                                                                         |
| Werkordergroep                 | De geselecteerde werkorder toevoegen aan of verwijderen uit een werkordergroep.                                                                                                                                                                                           |
| Aanpassen                          | Informatie over de verwachte begin- en einddatum, het serviceniveau, de verantwoordelijke onderhoudsmedewerker of verantwoordelijke onderhoudsmedewerkergroep voor geselecteerde werkorders aanpassen.                                                                                                                                     |
| Gerelateerde werkorder              | Een nieuwe werkorder maken die is gerelateerd aan de geselecteerde werkordertaak. Dit is handig als u primaire en secundaire werkorders wilt registreren.                                                                                                                              |
| Werkorder kopiëren                 | Een nieuwe werkorder maken op basis van een bestaande werkorder.                                                                                                                                                                                                               |
| Gebeurtenishistorie                   | De registratiehistorie voor de werkorder weergeven                                                                                                                                                                                                                |
| Notities over onderhoudstaak voor werkorders                           | Een omschrijving voor een werkorder maken of opmerkingen invoegen. Selecteer eerst **Tijdstempel toevoegen** om uw gebruikersnaam en een tijdstempel aan de notitie toe te voegen. Notities worden weergegeven op het tabblad **Omschrijving** op het sneltabblad **Regeldetails** van de pagina **Werkorder**.         |
| Hulpmiddelen                           | Een lijst met vereiste hulpmiddelen voor een werkorder maken. Hulpmiddelen worden ingesteld als resources in **Organisatiebeheer** > **Resources** > **Resources**.                                                                                                      |
| Onderhoudscontrolelijst           | De controlelijst weergeven voor het activum dat is verbonden aan de werkorder.                                                                                                                                                                                                              |
| Fout in activum                     | Foutinformatie over een activum weergeven of registreren. Deze informatie wordt gebruikt voor foutbeheer.                                                                                                                                                                                      |
| Uitvaltijd voor onderhoud            | Uitvaltijd voor onderhoud voor een werkorder opgeven.                                                                                                                                                                                                                               |
| Evaluatie van voorwaarden            | Metingen van toestandsbeoordelingen voor een werkorder registreren.                                                                                                                                                                                                             |
| Activumtellers                 | Registraties van tellers maken of weergeven.                                                                                                                                                                                                                     |
| Prognose                        | Prognoses voor een werkorder weergeven of maken.                                                                                                                                                                                                                               |
| Journalen                        | Werkorderjournalen weergeven of maken. U kunt journaalregels kopiëren uit prognoses.                                                                                                                                                                                         |
| Projecttransacties            | Alle geboekte transacties weergeven die zijn gerelateerd aan werkorders die voor het activum zijn gemaakt.                                                                                                                                                                                             |
| Status van werkorder bijwerken           | De levenscyclusstatus van werkorders bijwerken.                                                                                                                                                                                                                                                |
| Logboek levenscyclusstatus                      | Een logboek weergeven met de levenscyclusstatussen van de geselecteerde werkorder.                                                                                                                                                                                                                   |
| Activadocumenten                | De lijst met documenten weergeven die zijn gekoppeld aan activa die zijn gerelateerd aan een werkorder. Deze documenten worden ingesteld in **Activabeheer** > **Instellingen** > **Activadocumenten**.                                                                                                 |
| Planning                        | De geselecteerde werkorders plannen.                                                                                                                                                                                                                                      |
| Verzenden            | De geselecteerde werkorder voor één medewerker plannen.                                                                                                                                                                                                                        |
| Planning verwijderen                 | De planning voor de geselecteerde werkorder verwijderen.                                                                                                                                                                                                                          |
| Geplande onderhoudstaken voor werkorders             | De lijstpagina **Geplande onderhoudstaken voor werkorder** openen.                                                                                                                                                                                                                             |
| Opdracht tot inkoop voor werkorder | De lijstpagina **Opdracht tot inkoop voor werkorder** openen.                                                                                                                                                                                                                 |
| Inkoop werkorder             | De lijstpagina **Inkoop werkorder** openen.                                                                                                                                                                                                                             |
| Kostenbeheer                    | Budgetkosten en werkelijke kosten voor de werkorder vergelijken.                                                                                                                                                                                                                |
| Urenbeheer                    | Prognose-uren en werkelijke uren voor de werkorder met elkaar vergelijken.                                                                                                                                                                                                                |
| Werkorderrapport               | Een werkorderrapport afdrukken.                                                                                                                                                                                                                                                |
| Verbruik werkorder          | Een verbruiksrapport afdrukken.                                                                                                                                                                                                                                               |


De knoppen in de groep **Project** op het tabblad **Werkorder** van het actievenster hebben betrekking op de functionaliteit in de module **Projectbeheer en boekhouding** ten aanzien van prognoses, journalen en facturering.

>[!NOTE]
>Prognoses die voor een werkorder zijn gemaakt, kunnen worden opgenomen wanneer de hoofdplanning wordt uitgevoerd door het prognosemodel te gebruiken dat is geselecteerd op de pagina **Parameters voor activabeheer**.

