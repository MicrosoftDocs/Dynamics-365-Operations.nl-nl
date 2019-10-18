---
title: Magazijnmedewerkers beheren
description: In dit artikel wordt beschreven hoe u de Warehouse App van Dynamics 365 Supply Chain Management kunt gebruiken om het werk te helpen beheren en controleren dat door werknemers in uw magazijnen wordt uitgevoerd.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0de87e10f9213838dd5e5436b8b5699b19547bf
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018616"
---
# <a name="manage-warehouse-workers"></a>Magazijnmedewerkers beheren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de Warehouse App van Dynamics 365 Supply Chain Management kunt gebruiken om het werk te helpen beheren en controleren dat door werknemers in uw magazijnen wordt uitgevoerd.

Als u de functionaliteit in Magazijnbeheer gebruikt, wordt naar alle bewerkingen van magazijnwerknemers verwezen als *werk*. Werk zoals het orderverzamelen, verplaatsen en tellen van voorhanden voorraad wort geregistreerd door mobiele apparaten te gebruiken. Voordat een magazijnwerknemer werk kan uitvoeren, moet hij of zij aan een werknemer in Human resources worden gekoppeld. Aan elk **Werknemer**-account kunnen meerdere magazijnwerkgebruikers zijn gekoppeld. Deze werkgebruikers kunnen in verschillende magazijnen werken en kunnen verschillende niveaus van toegang tot de verschillende menu's voor mobiele apparaten hebben. U kunt de gebruikers van het magazijnwerk zien als meerdere aanmeldingen voor de geselecteerde werknemer. Elke werkgebruiker heeft een standaardmagazijn en de specifieke workflows worden beschikbaar gemaakt door de menuopties die voor die werkgebruiker beschikbaar zijn. 

Om een nieuwe werkgebruiker te maken, klikt u op de pagina **Medewerkers** op het tabblad **Algemeen** in de sectie **Magazijnen** op **Medewerker** . U moet een gebruikers-ID, gebruikersnaam, standaardmagazijn en menunaam opgeven. Dit menu wordt geladen als de gebruiker zich aanmeldt bij de magazijn-portal voor mobiele apparaten en stelt u in staat te definiëren tot welke menuopties de gebruiker toegang heeft. 

Als onderdeel van de instellingen voor elke werkgebruiker kunt u ook specifieke procesworkflows definiëren. U kunt bijvoorbeeld het veld **Is een cyclustellingssupervisor** gebruiken om op te geven of de gebruiker correcties in cyclustellingsdiscrepanties kan verwerken tijdens een telbewerking of dat deze correcties eerst door iemand anders moeten worden bekeken.

## <a name="defining-labor-standards"></a>Arbeidsstandaards definiëren
Op de pagina **Arbeidsstandaarden** kunt u de berekeningsmethoden definiëren die het systeem gebruikt om de geschatte vereiste tijd voor bepaalde typen werk te berekenen. Deze definitie kan op een generiek niveau of op een specifiek niveau worden ingesteld. U kunt bijvoorbeeld definiëren hoeveel tijd vereist moet zijn om een verkooporderverzameling per gewicht te verwerken voor een specifieke eenheidsdefinitie wanneer een specifiek verzamelproces wordt gebruikt. Tegelijkertijd kunt u de tijd vastleggen, op basis van een andere berekeningsmethode, voor de plaatsbewerking van de voorhanden voorraad die wordt verzameld. 

Om de arbeidsstandaarden in te schakelen die u hebt gedefinieerd, moet u de optie **Arbeidsstandaarden toestaan** selecteren voor elk magazijn waar arbeidsstandaarden worden gebruikt.

## <a name="monitoring-and-controlling-warehouse-work"></a>Magazijnwerk bewaken en beheren
Op de pagina **Alle werk** kunt u al het werk controleren en beheren dat is gepland, wordt uitgevoerd, en voltooid. Vanaf deze pagina kunt u verschillende processen, zoals toewijzingen van magazijnwerkgebruikers en werkprioriteit bijwerken. U kunt ook inzoomen op de details die aan de werkkoptekst en het de werkregels zijn gekoppeld om inzicht te krijgen in de verwachte of voltooide processen. 

Als u de optie **Arbeidsstandaarden** inschakelt, kunt u de berekende geschatte tijd voor het werk zien. Wanneer nu het werk wordt uitgevoerd, wordt ook de werkelijke tijd weergegeven voor elke werkbewerking. Op deze manier kunt u de geraamde tijdberekeningen vergelijken met de werkelijke tijd. 

Bovendien kunt u de geschatte tijd gebruiken in de regels om automatisch werk te splitsen tijdens het maken van werk. Op deze manier kunt u taken verdelen op basis van de verwachte tijd om de taken te voltooien. 

De analyse van de tijd die wordt gebruikt om werkitems te verwerken, kan helpen verbeteringen van de efficiëntie van magazijnmedewerkers te bereiken. De volgende rapporten zijn beschikbaar om met deze analyse te helpen:

-   **Arbeid door gebruiker** - Dit rapport bevat werknemersproductiviteit op basis van werkelijke tijden, vergeleken met verwachte tijden.
-   **Transactietype voor arbeid door werk** U kunt dit rapport gebruiken om ondoelmatigheden in specifieke magazijnprocessen te onderzoeken. U ziet bijvoorbeeld dat verzamelingen voor transferorders deze week langer duren dan in vorige weken. U kunt deze informatie vervolgens gebruiken voor verder onderzoek.




