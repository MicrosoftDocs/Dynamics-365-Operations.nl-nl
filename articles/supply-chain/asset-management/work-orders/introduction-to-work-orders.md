---
title: Inleiding op werkorders
description: Dit onderwerp bevat een overzicht van werkorders in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875596"
---
# <a name="introduction-to-work-orders"></a>Inleiding op werkorders

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Werkorders worden gebruikt voor het beheren van, het verstrekken van vereiste informatie voor en het registreren van verbruik voor onderhoudstaken. Een werkorder kan een of meer werkordertaken bevatten en een of meer activa kunnen worden gekoppeld aan een werkorder. Elke werkorderregel definieert een onderhoudstaak die is gepland voor het activum.

Werkorders kunnen automatisch of handmatig worden gemaakt:

- Automatisch met het formulier **Schema voor onderhoudsplannen**, voor onderhoudsplannen op basis van kalenders die zijn ingesteld op Automatisch maken.  

- Automatisch met het formulier **Schema voor onderhoudsronden**, voor onderhoudsronden die zijn ingesteld op Automatisch maken.  

- Op basis van een onderhoudsplanning. Dit kunnen preventieve onderhoudstaken of onderhoudsverzoeken zijn.  

- Maak handmatig een werkorder.  

- Maak een werkorder via **Alle onderhoudsverzoeken**, **Actieve onderhoudsaanvragen** of **De onderhoudsverzoeken van mijn functionele locatie**.

>[!NOTE]
>Werkordertaken die aan hetzelfde activum zijn gekoppeld, zijn gekoppeld aan dezelfde project-id.

## <a name="all-work-orders"></a>Alle werkorders

Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** om de lijst te openen. **Alle werkorders** bevat een lijst met alle werkorders en er worden enkele gegevens over een werkorder weergegeven.

![Figuur 1](media/01-work-orders.png)

- Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Actieve werkorders** om een lijst met actieve werkorders weer te geven.

- Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Mijn functionele locatie van onderhoudstaken voor werkorders** om een lijst met werkordertaken weer te geven die activa bevatten die zijn geïnstalleerd op functionele locaties waaraan u bent gerelateerd als werknemer (ingesteld in [Onderhoudsmedewerkers en groepen werknemers](../setup-for-objects/workers-and-worker-groups.md)).

- Klik in de lijst **Alle werkorders** (rasterweergave) op een koppeling in de kolom **Werkorder** om de detailweergave van de geselecteerde record weer te geven. Klik op de knop **Bewerken**.  

- De detailweergave bevat gedetailleerde informatie die is gerelateerd aan de werkorder.  

- Selecteer in de detailweergave de koppeling **Regels** om de werkordertaakdetails weer te geven of de koppeling **Koptekst** om werkorderdetails te bekijken.  

- Het verticale deelvenster **Verwante informatie** rechts van het scherm bevat aanvullende informatie die betrekking heeft op werkorders. Vouw het deelvenster uit om gerelateerde informatie voor de geselecteerde werkorder weer te geven.  


![Figuur 2](media/02-work-orders.png)


De knoppen in het actievenster zijn geordend op tabbladen. Hier volgt een korte omschrijving van de knoppen met betrekking tot activabeheer voor ondernemers:



| Knopnaam                     | Beschrijving                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bewerken                            | De geselecteerde werkorder bewerken.                                                                                                                                                                                                                                           |
| Nieuw                             | Nieuwe werkorder maken.                                                                                                                                                                                                                                                  |
| Verwijderen                          | De geselecteerde werkorder verwijderen.                                                                                                                                                                                                                                         |
| Werkordergroep                 | Een geselecteerde werkorder toevoegen aan of verwijderen uit een werkordergroep.                                                                                                                                                                                           |
| Aanpassen                          | Informatie over de verwachte begin- en einddatum, het serviceniveau, de verantwoordelijke onderhoudsmedewerker of verantwoordelijke onderhoudsmedewerkergroep voor geselecteerde werkorders aanpassen.                                                                                                                                     |
| Gerelateerde werkorder              | Een nieuwe werkorder maken die is gerelateerd aan de geselecteerde werkordertaak. Dit is handig als u primaire en secundaire werkorders wilt registreren.                                                                                                                              |
| Werkorder kopiëren                 | Een nieuwe werkorder maken op basis van een bestaande werkorder.                                                                                                                                                                                                                |
| Gebeurtenishistorie                   | De registratiehistorie voor de werkorder bekijken.                                                                                                                                                                                                                |
| Notities over onderhoudstaak voor werkorders                           | Een omschrijving maken of opmerkingen invoegen in een werkorder. Klik eerst op de knop **Tijdstempel toevoegen** om uw gebruikersnaam en een tijdstempel aan de notitie toe te voegen. Notities worden weergegeven in het formulier **Werkorder** > sneltabblad **Regeldetails** > tabblad **Omschrijving**. |
| Hulpmiddelen                           | Een lijst met vereiste hulpmiddelen voor een werkorder maken. Hulpmiddelen worden ingesteld als resources in **Organisatiebeheer** > **Algemeen** > **Resources** > **Resources**.                                                                                                      |
| Onderhoudscontrolelijst           | De controlelijst weergeven voor het activum dat is verbonden aan de werkorder.                                                                                                                                                                                                              |
| Fout in activum                     | Foutinformatie weergeven of registreren voor een activum dat moet worden gebruikt voor foutbeheer.                                                                                                                                                                                        |
| Uitvaltijd voor onderhoud            | Uitvaltijd voor onderhoud voor een werkorder opgeven.                                                                                                                                                                                                                               |
| Evaluatie van voorwaarden            | Metingen van toestandsbeoordelingen voor een werkorder registreren.                                                                                                                                                                                                             |
| Activumtellers                 | Registraties van tellers maken of weergeven.                                                                                                                                                                                                                     |
| Prognose                        | Prognoses voor een werkorder weergeven of maken.                                                                                                                                                                                                                               |
| Journalen                        | Werkorderjournalen weergeven of maken. U kunt journaalregels kopiëren uit prognoses.                                                                                                                                                                                         |
| Projecttransacties            | Alle geboekte transacties weergeven die zijn gerelateerd aan werkorders die voor het activum zijn gemaakt.                                                                                                                                                                                             |
| Status van werkorder bijwerken                | Levenscyclusstatussen van werkorder bijwerken.                                                                                                                                                                                                                                                |
| Logboek levenscyclusstatus                       | Het logboek waarin de levenscyclusstatus van de geselecteerde werkorder wordt weergegeven.                                                                                                                                                                                                                   |
| Activadocumenten                | Een lijst met documenten weergeven die zijn gekoppeld aan activa die zijn gerelateerd aan een werkorder. Deze documenten worden ingesteld in **Activabeheer** > **Instellingen** > **Activadocumenten**.                                                                                                 |
| Planning                        | De geselecteerde werkorders plannen.                                                                                                                                                                                                                                      |
| Verzenden            | De geselecteerde werkorder voor één medewerker plannen.                                                                                                                                                                                                                        |
| Planning verwijderen                 | De planning voor de geselecteerde werkorder verwijderen.                                                                                                                                                                                                                          |
| Geplande onderhoudstaken voor werkorder             | De lijstpagina **Geplande onderhoudstaken voor werkorder** openen.                                                                                                                                                                                                                             |
| Opdracht tot inkoop voor werkorder | De lijstpagina **Opdracht tot inkoop voor werkorder** openen.                                                                                                                                                                                                                 |
| Inkoop werkorder             | De lijstpagina **Inkoop werkorder** openen.                                                                                                                                                                                                                             |
| Kostenbeheer                    | Budgetkosten en werkelijke kosten voor de werkorder vergelijken.                                                                                                                                                                                                                |
| Urenbeheer                    | Prognose-uren en werkelijke uren voor de werkorder met elkaar vergelijken.                                                                                                                                                                                                                |
| Werkorderrapport               | Werkorderrapport afdrukken.                                                                                                                                                                                                                                                |
| Verbruik werkorder          | Verbruiksrapport afdrukken.                                                                                                                                                                                                                                               |


De knoppen op het tabblad **Werkorder** > de groep **Project** hebben betrekking op de functionaliteit in de module **Projectbeheer en boekhouding** ten aanzien van prognoses, journalen en facturering.

>[!NOTE]
>Prognoses die voor een werkorder zijn gemaakt, kunnen worden opgenomen wanneer de hoofdplanning wordt uitgevoerd door het prognosemodel te gebruiken dat is geselecteerd in het formulier **Parameters voor activabeheer**.

