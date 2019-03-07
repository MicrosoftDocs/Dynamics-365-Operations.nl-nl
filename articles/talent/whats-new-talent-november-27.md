---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (27 november 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303849"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (27 november 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2064**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.


## <a name="changes"></a>Wijzigingen

### <a name="unable-to-create-a-note-in-case-management"></a>Kan geen notitie maken in Casebeheer

Er is een wijziging doorgevoerd voor een probleem wanneer u een notitie probeert te bewerken of te maken in het caselogboek van Casebeheer.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Onjuist gespeld woord op het tabblad Analyses in het compensatiewerkgebied 

Een wijziging is doorgevoerd om de spelling van Etnische afkomst in het diagram Compensatieanalyse in het werkgebied Compensatie te corrigeren.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Werkgebied Selfservice werknemer wordt niet weergegeven wanneer een gebruiker niet aan een werknemer wordt toegewezen 

Een wijziging is aangebracht wanneer het werkgebied **Selfservice werknemer** is geselecteerd als de beginpagina bij het opstarten van een gebruiker die niet aan een werknemer is toegewezen. In dit geval wordt het standaarddashboard weergegeven.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Fout in Verlof en verzuim: de objectverwijzing is niet ingesteld op een exemplaar van een object

Er zijn wijzigingen aangebracht in Verlof en verzuim om deze fout na het goedkeuren van verlof- en verzuimrecords in de lijst **Aan mij toegewezen werkitems** op te lossen.

### <a name="unable-to-recall-an-image-workflow"></a>Kan een afbeeldingswerkstroom niet intrekken

Na het intrekken van een afbeeldingswerkstroom, wordt de werkstroom ingesteld op 'geannuleerd' en kan de bestaande aanvraag worden verwijderd in het werkgebied Selfservice werknemer.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Opnieuw aangenomen werknemers of contractanten worden na beëindiging meerdere keren weergegeven 

Met deze update worden ontslagen werknemers die opnieuw worden aangenomen slechts één keer weergegeven in de lijst met vertrokken werknemers. 

## <a name="known-issue"></a>Bekend probleem

- **Probleem**: bij het toevoegen van een nieuwe bijlage aan een werknemer zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar. 
- **Tijdelijke oplossing:** voordat u de bijlagepagina opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten. Als de feitenvakken worden gesloten wanneer de pagina **Werknemer** wordt geladen, worden de bijlageknoppen ingeschakeld. (Dit probleem wordt opgelost in de volgende platformupdate.)
