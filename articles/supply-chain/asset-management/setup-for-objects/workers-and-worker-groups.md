---
title: Onderhoudsmedewerkers en medewerkersgroepen
description: In dit onderwerp worden onderhoudsmedewerkers en medewerkersgroepen in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c85fc24cdf0b3cd1a188ccf0f477ffbfa5fab960
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783170"
---
# <a name="maintenance-workers-and-worker-groups"></a>Onderhoudsmedewerkers en medewerkersgroepen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In dit onderwerp worden onderhoudsmedewerkers en medewerkersgroepen in Activabeheer uitgelegd. In Activabeheer kunt u onderhoudsmedewerkers verbinden met functionele locaties. (Zie [Functionele locaties maken](../functional-locations/create-functional-locations.md) voor meer informatie over functionele locaties.) Deze functionaliteit kan handig zijn als u bijvoorbeeld een onderhoudstaak wilt plannen op een machine die zich op functionele locatie 01 bevindt en u onderhoudsmedewerkers wilt toewijzen vanaf dezelfde locatie om de taak uit te voeren.

U kunt ook groepen onderhoudsmedewerkers maken en hieraan onderhoudsmedewerkers koppelen. Deze functionaliteit is handig wanneer u een eenvoudige werkorderplanning maakt en u een groep onderhoudsmedewerkers voor een werkorder wilt plannen. U kunt onderhoudsmedewerkers en groepen onderhoudsmedewerkers gebruiken om voorkeursonderhoudsmedewerkers en verantwoordelijke onderhoudsmedewerkers in te stellen. 


## <a name="create-workers"></a>Medewerkers maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Medewerkers** \> **Medewerkers**.
2. Selecteer **Nieuw** om een medewerker toe te voegen aan de lijst.
3. Selecteer de medewerker in het veld **Medewerker**.
4. Stel de optie **Actief** in op **Ja** om de medewerker te plannen voor werkorders.

    Op het sneltabblad **Algemeen** worden de velden **Resource** en **Beschrijving** automatisch ingevuld als er een resource is geselecteerd voor de medewerker. Het veld **Kalender** wordt eveneens automatisch ingevuld, op voorwaarde dat u de medewerker als een resource hebt ingesteld en een kalender aan die resource hebt toegewezen op de pagina **Resources** (**Organisatiebeheer** \> **Resources** \> **Resources**).

5. Selecteer op het sneltabblad **Groepen** de optie **Toevoegen** en selecteer vervolgens een groep onderhoudsmedewerkers voor de medewerker. Een medewerker kan meer dan één groep worden gekoppeld.
6. In de standaardinstelling is de koppeling van een medewerker aan een groep van kracht vanaf de datum waarop u de groep toevoegt en verloopt deze nooit. Deze datum wordt weergegeven in het veld **Geldig vanaf**. Als u het veld **Geldig vanaf** wilt zien, selecteert u **Weergeven** \> **Alle**. Als de koppeling van de medewerker met een groep moet worden beperkt tot een bepaalde periode, gebruikt u de velden **Geldig vanaf** en **Vervaldatum** om de periode te definiëren.
7. Selecteer op het sneltabblad **Functionele locaties** de optie **Toevoegen** en selecteer vervolgens een functionele locatie voor de onderhoudsmedewerker. Geef ook op welke locatie de primaire functionele locatie voor de medewerker is.

    > [!NOTE]
    > Wanneer u functionele locaties aan een werknemer toevoegt, worden alle actieve activa die zijn gerelateerd aan die functionele locaties weergegeven in verschillende menuopties, zoals **Mijn activa activa** en **Mijn actieve functionele locaties**. Ze worden ook weergegeven in de zoekopdrachten voor activa die worden weergegeven wanneer u een nieuw activum of een nieuwe onderhoudsaanvraag of werkorder maakt.

    De velden op het sneltabblad **Details** tonen het aantal groepen onderhoudsmedewerkers en functionele locaties waaraan de geselecteerde onderhoudsmedewerker is gekoppeld.

## <a name="create-worker-groups"></a>Medewerkersgroepen maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Medewerkers** \> **Onderhoudsmedewerkersgroepen**
2. Selecteer **Nieuw** om een medewerkersgroep toe te voegen aan de lijst.
3. Voer in het veld **Onderhoudsmedewerkersgroep** een groep-id in.
4. Voer in het veld **Naam** een naam in.
5. Selecteer op het sneltabblad **Medewerkers** de optie **Toevoegen** en selecteer vervolgens een onderhoudsmedewerker voor de medewerkersgroep. Zie stap 6 in de vorige procedure voor informatie over de velden **Geldig vanaf** en **Vervaldatum**.
6. Als een resourcegroep moet worden gerelateerd aan de geselecteerde onderhoudsmedewerkersgroep, selecteert u **Kopiëren uit resourcegroep**. Selecteer in het veld **Groep** de resourcegroep waarvan u de kalenderinstellingen wilt kopiëren. Selecteer vervolgens in het veld **Medewerkersgroep** de medewerkersgroep waar u de kalenderinstellingen van de resourcegroep naartoe wilt kopiëren. Deze stap is alleen relevant als u wilt dat onderhoudsmedewerkers de kalender gebruiken die is gerelateerd aan een resource (werkplaats) tijdens de planning van de werkorder.

    Het veld op het sneltabblad **Details** toont het aantal groepen onderhoudsmedewerkers dat is ingesteld voor de geselecteerde groep onderhoudsmedewerkers.
