---
title: Functionele locaties maken
description: In dit onderwerp wordt uitgelegd hoe u een functionele locatie maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b5b81d7c318ba0a195dbc6324d700ccb8d39bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018216"
---
# <a name="create-functional-locations"></a>Functionele locaties maken

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt uitgelegd hoe u een functionele locatie maakt in Activabeheer.

Wanneer u een functionele locatiestructuur maakt, moet u er rekening mee houden dat wanneer u een functionele locatie hebt gemaakt, u deze niet kunt verplaatsen vanaf de oorspronkelijke locatie. Dit betekent dat u de structuur van uw functionele locaties zorgvuldig moet overwegen voordat u begint met het maken hiervan in Activabeheer. Als u spijt hebt van een functionele locatie, kunt u deze verwijderen, op voorwaarde dat deze nog niet in gebruik is genomen.

Om te kunnen werken met functionele locaties, begint u met het maken van twee "categorieën" functionele locaties:

- Maak *één* standaard functionele locatie zonder sublocaties. Deze functionele locatie wordt alleen gebruikt als de standaardlocatie voor activa wanneer u nieuwe activa maakt.  
- Maak de functionele locatiestructuren die nodig zijn voor het beheer van onderhoudstaken in uw bedrijf.

## <a name="create-a-default-functional-location"></a>Een standaard functionele locatie maken

Wanneer u functionele locaties gebruikt, begint u met het maken van één standaardlocatie die moet worden gebruikt wanneer u nieuwe activa maakt. Deze functionele locatie is degene die u selecteert in **Activabeheer** > **Instellingen** > **Parameters voor activabeheer** > koppeling **Activa** > veld **Standaard functionele locatie**. De standaard functionele locatie kan worden gebruikt wanneer u nieuwe activa maakt en u nog geen functionele locatiestructuur voor die activa hebt ingesteld.

1. Selecteer **Activabeheer** > **Algemeen** > **Functionele locaties** > **Alle functionele locaties**.  
2. Selecteer **Nieuwe** in **Alle functionele locaties**.
3. Typ een id in het veld **Functionele locatie**, bijvoorbeeld '0000' of 'Standaard', om aan te geven dat dit een speciale functionele locatie is.
4. Voeg een naam in voor de standaard functionele locatie in het veld **Naam**.
5. Selecteer *geen* bovenliggend item in het veld **Bovenliggend item**. Laat dit veld leeg.
6. Selecteer in het veld **Type functionele locatie** het type functionele locatie dat moet worden gebruikt voor de standaard functionele locatie. Zie [Typen functionele locatie](../setup-for-functional-locations/functional-location-types.md) voor meer informatie over het instellen van typen functionele locatie.
7. Selecteer **OK**. Voeg geen extra gegevens toe aan deze functionele locatie omdat deze alleen wordt gebruikt als een tijdelijke locatie voor nieuwe activa totdat u de activa installeert op de functionele locaties die worden gebruikt door uw bedrijf.

## <a name="create-functional-locations"></a>Functionele locaties maken

In de volgende procedure wordt beschreven hoe u de functionele locaties maakt die nodig zijn voor onderhoudsbeheer in uw bedrijf.

1. Selecteer **Activabeheer** > **Algemeen** > **Functionele locaties** > **Alle functionele locaties**. U kunt een functionele locatie maken vanuit de rasterweergave of de detailweergave.
2. Selecteer de knop **Nieuw**.
3. Typ een id in het veld **Functionele locatie**.
4. Typ een naam voor de functionele locatie in het veld **Naam**.
5. Als de functionele locatie een sublocatie in een structuur is, selecteert u de bovenliggende locatie in het veld **Bovenliggend item**.
6. Selecteer een type het veld **Type functionele locatie**.
7. Selecteer **OK**.
8. Selecteer de functionele locatie en klik op de knop **Bewerken** om meer informatie toe te voegen.

>[!NOTE]
>Afhankelijk van de instellingen voor de levenscyclusstatussen van de functionele locatie, moet u mogelijk alle sublocaties voor een functionele locatie maken en vervolgens de levenscyclusstatus van de functionele locatie wijzigen voordat u kunt beginnen met het installeren van activa. Zie [Activa installeren op functionele locaties](../functional-locations/install-objects-on-functional-locations.md) voor meer informatie over de installatie van activa. Zie [Levenscyclusstatussen van functionele locaties](../setup-for-functional-locations/functional-location-stages.md) voor meer informatie over het instellen van levenscyclusstatussen van functionele locaties.

In de detailweergave ziet u sneltabbladen waarop u informatie over de functionele locatie kunt toevoegen en bewerken.

## <a name="general-information"></a>Algemene gegevens

Deze sectie bevat een overzicht van bovenliggende en onderliggende informatie in de functionele locatiestructuur. In de sectie **Details** ziet u het aantal kenmerken van activa, onderhoudsplannen en activa die betrekking hebben op de functionele locatie. In de sectie **Voorraad** kunt u de site en het magazijn selecteren waaraan de functionele locatie is gekoppeld. Site en magazijn worden gebruikt in combinatie met werkorderartikelprognoses. Wanneer u een artikelprognose maakt, worden site- en magazijngegevens van de functionele locatie van het activum automatisch gebruikt. In de sectie **Levenscyclusstatus** wordt informatie over de levenscyclusstatus van de functionele locatie weergegeven.

## <a name="installed-assets"></a>Geïnstalleerde activa

Raadpleeg [Activa installeren op functionele locaties](../functional-locations/install-objects-on-functional-locations.md) voor meer informatie over de installatie van activa. U kunt de knop **Weergeven** op dit sneltabblad gebruiken om meer velden op het sneltabblad te tonen. De velden **Geldig vanaf** en **Subactivum** kunnen in het raster worden weergegeven.

## <a name="asset-attribute-requirements"></a>Vereisten voor kenmerken van activa

Op dit sneltabblad kunt u specifieke kenmerkvereisten toevoegen voor de activa die u op de functionele locatie installeert. Deze vereisten dienen uitsluitend ter informatie. Zij verhinderen niet dat u activa installeert met andere kenmerkvereisten. Selecteer **Regel toevoegen** en selecteer het kenmerktype. Vervolgens voegt u de relevante **waarde** in, selecteert u een drempel in het veld **Drempelcriteria** en slaat u de record op.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Onderhoudsplannen en onderhoudsronden

Hier kunt u onderhoudsplannen en onderhoudsronden toevoegen aan de functionele locatie, met inbegrip van een begindatum. Voor de activa die zijn geïnstalleerd op een functionele locatie kunnen andere onderhoudsplannen zijn ingesteld. Alle onderhoudsplannen en onderhoudsronden kunnen worden gebruikt voor het plannen van activakalenderposten voor een functionele locatie en de bijbehorende momenteel geïnstalleerde activa.

>[!NOTE]
>Als u de instellingen van activatypen, activamerken en activamodellen bijwerkt in onderhoudsplannen in de detailweergave **Alle functionele locaties** > sneltabblad **Onderhoudsplannen** nadat u onderhoudsplannen hebt gepland, worden bestaande onderhoudsplannen die betrekking hebben op die functionele locatie automatisch verwijderd. Als u nieuwe planningsvermeldingen wilt maken die overeenkomen met de bijgewerkte instellingen voor onderhoudsplannen op de functionele locatie, moet u een nieuw schema voor onderhoudsplannen uitvoeren voor die functionele locatie. 

## <a name="address"></a>Adres

Typ het adres van de functionele locatie op het sneltabblad **Adres**. Adressen op functionele locaties worden overgenomen, wat betekent dat als er geen adres is gedefinieerd voor een sublocatie, het adres van de bovenliggende locatie wordt gebruikt.

## <a name="workers"></a>Medewerkers

Op dit sneltabblad kunt u medewerkers toevoegen die zijn gekoppeld aan de functionele locatie, en u kunt een functionele locatie selecteren als primair voor de medewerker. 

## <a name="attributes"></a>Kenmerken

Op dit sneltabblad kunt u waarden instellen voor kenmerken van functionele locaties. Deze kenmerken kunnen worden gebruikt om eigenschappen of kenmerken te beschrijven die relevant zijn voor de functionele locatie, bijvoorbeeld structurele eigenschappen, gebouwtype, gebiedsbeschrijvingen of locatie boven of onder de grond.

Selecteer **Regel toevoegen** en selecteer het kenmerktype. Voeg vervolgens de **waarde** in voor het kenmerktype in en sla de record op.

## <a name="financial-dimensions"></a>Financiële dimensies

U kunt financiële dimensies selecteren voor de functionele locatie. [Typen functionele locatie](../setup-for-functional-locations/functional-location-types.md) kunnen zo worden ingesteld dat financiële dimensies automatisch kunnen worden bijgewerkt vanaf een functionele locatie. Dit betekent dat activa die op een financiële dimensie zijn geïnstalleerd, automatisch de financiële dimensies voor de functionele locatie krijgen. Dit is handig als u verschillende kostenplaatsen wilt, afhankelijk van locaties.

Wanneer gegevens met betrekking tot **Site**, **Magazijn**, **Adres** en **Financiële dimensies** worden bijgewerkt op een bovenliggende functionele locatie, kunnen de gerelateerde subfunctielocaties dienovereenkomstig worden bijgewerkt als u die selectie maakt tijdens de update. Er wordt een dialoogvenster geopend waarin u de updateopties worden aangeboden.

## <a name="copy-a-functional-location-structure"></a>Een functionele locatiestructuur kopiëren

Als uw bedrijf verschillende functionele locaties met vergelijkbare locatiestructuren heeft, kunt u de kopieerfunctie in Activabeheer gebruiken om snel een aantal vergelijkbare locatiehiërarchieën te maken. Wanneer u een specifieke functionele locatie of een hele structuur kopieert, heeft de nieuwe locatie of structuur dezelfde naam als die u hebt gekopieerd. Nadat de kopieerprocedure is voltooid, kunt u eenvoudig de naam of andere instellingen op de nieuwe functionele locatie wijzigen, op voorwaarde dat de levenscyclusstatus van de functionele locatie die is geselecteerd voor de nieuwe functionele locatie dit toestaat.

1. Selecteer in **Alle functionele locaties** de functionele locatie die u wilt kopiëren. Zo selecteert u bijvoorbeeld een toplocatie (bovenliggend item) als u de volledige functionele locatiestructuur inclusief sublocaties wilt kopiëren.
2. Selecteer de knop **Functionele locatiestructuur kopiëren**. De locatie die u op de lijstpagina hebt geselecteerd, wordt weergegeven in het veld **Kopiëren van**.
3. Voeg de naam van de nieuwe locatie in het veld **Nieuwe functionele locatie** in.
4. Voeg in het veld **Bovenliggend item om onder te plakken** alleen een bovenliggende id in als de locatie die u maakt deel moet uitmaken van een bestaande functionele locatiestructuur.
5. Klik op **OK**. De nieuwe functionele locatiestructuur wordt weergegeven in **Alle functionele locaties**.

>[!NOTE]
>Wanneer u een functionele locatiestructuur kopieert, worden de levenscyclusstatussen van functionele locaties in de nieuwe structuur ingesteld op de 'eerste status' die u hebt gemaakt voor functionele locaties. Of u een functionele locatie kunt hernoemen of verwijderen met de knoppen **Naam wijzigen** en **Verwijderen** in **Alle functionele locaties**, is afhankelijk van de huidige levenscyclusstatus van de functionele locatie.

## <a name="delete-a-functional-location"></a>Een functionele locatie verwijderen

Een functionele locatie met gerelateerde sublocaties kan worden verwijderd als er geen activa zijn geïnstalleerd op een van de functionele locaties die u probeert te verwijderen en als de huidige levenscyclusstatus van de functionele locatie dit toestaat.

1. Selecteer in **Alle functionele locaties** de functionele locatie die u wilt verwijderen.
2. Werk, indien nodig, de functionele locatie bij naar een levenscyclusstatus van functionele locaties die het verwijderen van een functionele locatie toestaat.
3. Selecteer **Verwijderen**.

>[!NOTE]
>Als u een functionele locatie niet kunt verwijderen, kunt u in plaats daarvan de verwijdering afhandelen door een levenscyclusstatus van functionele locaties in te stellen voor dit doel. Zo kunt u bijvoorbeeld een fase 'Buiten gebruik gesteld' of 'Verwijderd' instellen, die geen actieve fase mag zijn, in het formulier **Levenscyclusstatussen van functionele locaties**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]