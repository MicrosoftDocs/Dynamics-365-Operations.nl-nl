---
title: Activa installeren op functionele locaties
description: In dit onderwerp wordt uitgelegd hoe u activa installeert op functionele locaties in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
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
ms.openlocfilehash: c585bce468f87a32204893ea20ce6954e92b0e38
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571801"
---
# <a name="install-assets-on-functional-locations"></a>Activa installeren op functionele locaties

[!include [banner](../../includes/banner.md)]

 

Nadat u structuren voor functionele locaties hebt gemaakt, is de volgende stap het installeren van activa op de relevante functionele locaties. In dit onderwerp wordt uitgelegd hoe u activa installeert op deze functionele locaties in Activabeheer. Zie [Activa](../objects/introduction-to-objects.md) voor meer informatie over het maken van activa.

Als u een activastructuur hebt gemaakt, moet de hele activastructuur worden geïnstalleerd op een functionele locatie. Daarom kunnen alleen bovenliggende activa (activa op het hoogste niveau die geen bovenliggend activum hebben) worden geselecteerd op een functionele locatie. Alle gerelateerde onderliggende activa (subactiva) worden ook op de functionele locatie geïnstalleerd. Wanneer u activa op een functionele locatie installeert, worden de financiële dimensies van de functionele locatie mogelijk automatisch naar deze activa overgebracht. Dit is afhankelijk van de instellingen voor het type functionele locatie dat voor de functionele locatie is geselecteerd. Zie [Typen functionele locaties](../setup-for-functional-locations/functional-location-types.md) voor meer informatie over het instellen van typen functionele locaties.

> [!NOTE]
> U kunt activumtypen instellen voor het type functionele locatie dat voor een functionele locatie worden gebruikt. Als u in dit geval activa installeert op de functionele locatie, worden in de lijst met activa alleen bovenliggende activa weergegeven met hetzelfde type activum dat op de functionele locatie kan worden geïnstalleerd.

Nadat u activa op een functionele locatie hebt geïnstalleerd, kunt u een bovenliggend activum of een activastructuur vervangen als dat nodig is. Wanneer u activa installeert, selecteert u een bovenliggend activum dat u wilt vervangen. Alle gerelateerde onderliggende activa zullen ook worden vervangen. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Een activastructuur installeren op een functionele locatie

1. Selecteer **Activabeheer** \> **Algemeen** \> **Functionele locaties** \> **Alle functionele locaties** of **Alle functionele locaties**.
2. Selecteer de functionele locatie waarop u een activum wilt installeren.
3. Selecteer **Activum installeren**.

    De sectie **Kenmerken** bevat een lijst met de activakenmerkvereisten die zijn ingesteld voor het type functionele locatie dat is geselecteerd voor de functionele locatie. Deze kenmerken zijn alleen bedoeld voor informatieve doeleinden. Het systeem valideert de kenmerken niet op basis van de activumkenmerken die zijn ingesteld voor het activum dat u installeert. U moet deze validatie uitvoeren nadat u een activum hebt geselecteerd in het veld **Activum**.

4. Selecteer in het veld **Activum** het bovenliggende activum dat u wilt installeren. Alle gerelateerde onderliggende activa worden automatisch opgenomen in de installatie.

    De sectie **Activumkenmerken**, rechts van de lijst met activa, bevat de activumkenmerken die zijn gerelateerd aan het geselecteerde activum.

5. Selecteer in het veld **Effectief** de datum en tijd vanaf wanneer de activuminstallatie geldig is. Na die datum en tijd zijn de kosten voor het activum en de bijbehorende subactiva gerelateerd aan de functionele locatie.

    > [!NOTE]
    > De activumkenmerken die zijn ingesteld voor het activum, worden toegevoegd aan de sectie **Kenmerken**. Zo is de vereiste van het kenmerk **Gewicht** toegevoegd als een vereiste voor zowel het activum als de functionele locatie. Als het activum kenmerkvereisten heeft van hetzelfde type als de functionele locatie, worden de waarden van de kenmerkvereisten van het activum ingevoerd in de **Waarde**-velden. Daarom kunt u de activawaarden valideren aan de hand van de kenmerkvereisten die zijn ingesteld op de functionele locatie. De kenmerkvereisten die zijn ingesteld op de functionele locatie, zijn gemarkeerd met een vinkje.

6. Selecteer **OK**.

    > [!NOTE]
    > Als u de installatie van een activum wilt wijzigen door deze op een nieuwe functionele locatie te installeren, volgt u stap 1 tot en met 6 van deze procedure. Wanneer u een activum op een nieuwe functionele locatie installeert, wordt het activum automatisch verwijderd uit de vorige functionele locatie. Eventuele actieve onderhoudsverzoeken of werkorders die voor het activum zijn gemaakt vóór de installatie ervan op een nieuwe functionele locatie worden **niet** automatisch overgebracht naar de nieuwe functionele locatie. Als deze onderhoudsverzoeken en werkorders nog steeds vereist zijn voor het activum, moet u deze handmatig opnieuw maken nadat het activum op de nieuwe locatie is geïnstalleerd.

7. Voor een lijst van alle activa, inclusief subactiva, die op de functionele locatie zijn geïnstalleerd, selecteert u de functionele locatie op de pagina **Alle functionele locaties** en selecteert u **Activa**.
8. Voor een lijst met actieve onderhoudsverzoeken, actieve werkorders of foutregistraties die zijn gerelateerd aan de activa die op een functionele locatie zijn geïnstalleerd, selecteert u de functionele locatie op de pagina **Alle functionele locaties** en selecteert u **Verzoeken**, **Werkorders** of **Fouten**.

> [!NOTE]
> Wanneer activumgerelateerde gegevens worden gewijzigd, worden deze automatisch bijgewerkt op de functionele locatie waarop het activum is geïnstalleerd. Deze automatische update heeft betrekking op wijzigingen in onderhoudsverzoeken, werkorders, activumfoutregistraties, registraties van uitvaltijd voor onderhoud en registraties van activummetingen.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Automatisch één activum maken op een functionele locatie

U kunt functionele-locatiefasen en functionele-locatietypen instellen om het automatisch maken van *één* activum op een functionele locatie te verwerken. Het activum krijgt dezelfde id en naam als de functionele locatie. Deze functionaliteit kan handig zijn bij het afhandelen van onderhoud op een groot, statisch activum, zoals een gebouw.

Voordat u automatisch een activum op een functionele locatie kunt maken, moeten de volgende instellingsgegevens beschikbaar zijn:

- Maak een type functionele locatie om het automatisch maken van een activum te verwerken. Selecteer een activatype in het veld **Activatype**. Zie [Typen functionele locaties](../setup-for-functional-locations/functional-location-types.md) voor meer informatie.
- Maak een levenscyclusstatus voor functionele locaties om het automatisch maken van een activum te verwerken. Stel de optie **Activum maken** in op **Ja**. Zie [Levenscyclusstatussen van functionele locaties](../setup-for-functional-locations/functional-location-stages.md) voor meer informatie.

Wanneer de instellingsgegevens beschikbaar zijn, kunt u een activum gaan maken.

1. Controleer op de pagina **Alle functionele locaties** of de functionele locatie waar u wilt dat het activum automatisch wordt gemaakt, gebruikmaakt van het type functionele locatie dat u voor dit doel hebt gemaakt.
2. Alle de functionele locatie in de lijst.
3. Selecteer **Status van functionele locatie bijwerken** en selecteer vervolgens de levenscyclusstatus die u voor dit doel hebt gemaakt. Er wordt nu automatisch één activum op de functionele locatie geïnstalleerd. Dit activum heeft dezelfde naam als de functionele locatie.
