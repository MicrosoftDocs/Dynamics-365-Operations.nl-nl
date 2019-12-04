---
title: Functionele locatietypen
description: In dit onderwerp wordt beschreven hoe u functionele locatietypen maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 0468cb0b1717b7cf0ccb391da09a4e7d788124f3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812209"
---
# <a name="functional-location-types"></a>Functionele locatietypen

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt beschreven hoe u functionele locatietypen maakt in Activabeheer. Functionele locatietypen worden gebruikt voor het beheren van vereisten voor functionele locaties, zoals hoe activa worden geïnstalleerd op een functionele locatie. U kunt vereisten instellen voor activumtypen, onderhoudsplannen, functionele locatiekenmerken en activakenmerken die moeten worden gebruikt op een functionele locatie die gebruikmaakt van het specifieke type functionele locatie. Wanneer u een functionele locatie maakt, is het functionele locatietype verplicht.

>[!NOTE] 
>Als u wilt werken met functionele locaties, moet u een standaard functionele locatie maken die alleen wordt gebruikt voor het maken van nieuwe activa. Voor die standaard functionele locatie moet u een standaardtype functionele locatie maken dat heel eenvoudig is en waarmee meerdere activa op de standaard functionele locatie kunnen worden geïnstalleerd. Zie [Functionele locaties maken](../functional-locations/create-functional-locations.md) voor meer informatie over het instellen van typen functionele locaties.

## <a name="create-a-default-functional-location-type"></a>Een standaardtype functionele locatie maken

Deze procedure laat zien hoe u een standaardtype functionele locatie maakt dat wordt gebruikt voor een standaard functionele locatie.

1. Selecteer **Activabeheer** > **Instellen** > **Functionele locaties** > **Functionele locatietypen**.
2. Selecteer **Nieuw** om een nieuw type functionele locatie te maken.
3. Geef een type-id voor de functionele locatie op in het veld **Type functionele locatie**, bijvoorbeeld "standaard", en een naam in het veld **Naam**.
4. Selecteer in het veld **Levenscyclusmodel van functionele locatie** een model voor de levenscyclus.
5. Selecteer "Ja" op de schakelknop **Meerdere activa** zodat met dit type meer activa kunnen worden geïnstalleerd op een functionele locatie (de standaard functionele locatie).

Nu wordt een standaardtype functionele locatie gemaakt dat alleen wordt gebruikt voor een standaard functionele locatie. Voeg niet extra vereisten of beperkingen toe aan dit standaardtype functionele locatie.


## <a name="create-functional-location-types"></a>Functionele locatietypen maken

1. Selecteer **Activabeheer** > **Instellen** > **Functionele locaties** > **Functionele locatietypen**.
2. Selecteer **Nieuw** om een nieuw type functionele locatie te maken.
3. Geef een type-id voor de functionele locatie op in het veld **Type functionele locatie** en een naam in het veld **Naam**.
4. Selecteer in het veld **Levenscyclusmodel van functionele locatie** een model voor de levenscyclus. Raadpleeg de [Status van levenscyclus voor functionele locaties](../setup-for-functional-locations/functional-location-stages.md) voor meer informatie over de levenscyclusstatussen van functionele locatie en levenscyclusmodellen.
5. Selecteer "Ja" op de schakelknop **Meerdere activa** als u wilt dat meerdere activa kunnen worden geïnstalleerd op een functionele locatie met dit functionele locatietype. Als u "Nee" selecteert, kunt u slechts *één* activum installeren op een functionele locatie met dit functionele locatietype.
6. Selecteer "Ja" op de wisselknop **Activumdimensie bijwerken** als u wilt dat activa die op een functionele locatie van dit type worden geïnstalleerd, automatisch de financiële dimensies te gebruiken die samenhangen met de functionele locatie. Dit betekent dat als u financiële dimensies wijzigt in het formulier [Functionele locaties maken](../functional-locations/create-functional-locations.md) en de functionele locatie een functioneel locatietype gebruikt waarbij deze wisselknop is ingesteld op Ja, financiële dimensies automatisch worden bijgewerkt voor alle activa die zijn geïnstalleerd op die functionele locatie.
7. Het veld **Activumtype** wordt gebruikt als u automatisch *één* activum wilt maken voor de functionele locatie met dezelfde id en naam als de functionele locatie die u maakt. Dit kan bijvoorbeeld relevant zijn als u een statische functionele locatie maakt, zoals een gebouw of een pijplijn. Selecteer in dat geval het activumtype dat u wilt gebruiken voor het automatisch gemaakte activum. Houd er rekening mee dat als u een selectie maakt in dit veld, de wisselknop **Meerdere activa** moet worden ingesteld op "Nee".
8. Selecteer op het sneltabblad **Activatypen** de activatypen die moeten worden gerelateerd aan het functionele locatietype. Selecteer **Regel toevoegen** en selecteer de activatypen. Als u hier activatypen toevoegt, kunnen alleen activa die deze activatypen gebruiken, op een functionele locatie worden geïnstalleerd met behulp van dit type functionele locatie. Als er geen activatypen zijn geselecteerd op het sneltabblad **Activatypen**, kunnen alle activatypen worden geïnstalleerd.
9. Selecteer op het sneltabblad **Onderhoudsplannen** de onderhoudsplannen die automatisch moeten worden ingesteld op nieuwe functionele locaties met dit type functionele locatie. Selecteer **Regel toevoegen** en selecteer de onderhoudsplannen. Als u hier onderhoudsplannen toevoegt, kunnen alleen die plannen worden gebruikt op een functionele locatie met dit type functionele locatie.
10. Stel op het sneltabblad **Vereisten voor kenmerken van activa** de activakenmerken in die automatisch moeten worden ingesteld op nieuwe functionele locaties met dit type functionele locatie. Selecteer **Regel toevoegen** en selecteer het kenmerk. Deze kenmerkvereisten fungeren als richtlijnen. Ze worden niet gevalideerd voor kenmerken die zijn ingesteld voor een activum **(Activabeheer** > **Algemeen** > **Activa** > **Alle activa** > activum selecteren op de lijstpagina > tabblad **Algemeen** > knop **Kenmerken**). De kenmerkvereisten worden weergegeven wanneer u activa op functionele locaties installeert.
11. Selecteer op het sneltabblad **Toegestane typen** de functionele locatietypen die geldig zijn voor functionele sublocatietypen die betrekking hebben op een bovenliggend type functionele locatie, die het geselecteerde functionele locatietype gebruikt.
12. Selecteer op het sneltabblad **Kenmerken** de kenmerken voor functionele locaties die automatisch moeten worden ingesteld op functionele locaties met dit type functionele locatie. Selecteer **Regel toevoegen** en selecteer het kenmerk.


>[!NOTE] 
>Op het sneltabblad **Algemeen** krijgt u een overzicht van het aantal activatypen, onderhoudsplannen, kenmerkvereisten voor activa, toegestane typen, kenmerken en functionele locaties die zijn ingesteld voor het type functionele locatie. Het veld **Functionele locaties** bevat het aantal functionele locaties dat het type functionele locatie gebruikt. Gebruik de knop **Kopiëren** om instellingen van een functioneel locatietype naar het geselecteerde functionele locatietype te kopiëren.
