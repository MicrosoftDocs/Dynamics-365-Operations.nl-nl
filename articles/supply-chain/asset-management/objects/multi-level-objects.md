---
title: Activa met meerdere niveaus
description: In dit onderwerp wordt uitgelegd hoe u activa met meerdere niveaus maakt en verwijdert.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425579"
---
# <a name="multi-level-assets"></a>Activa met meerdere niveaus

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt uitgelegd hoe u activa met meerdere niveaus maakt en verwijdert. U kunt activa en gerelateerde subactiva maken in een hiërarchische boomstructuur. Op deze manier kunt u relaties en afhankelijkheden tussen activa weergeven. Onderhoudstaken kunnen worden gerelateerd aan alle niveaus van de boomstructuur. Ook kunnen statistieken worden gemaakt voor een individueel niveau of als een som van alle subactivaniveaus.

Op de lijstpagina **Alle activa** (**Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**), worden activa in hiërarchische volgorde weergegeven in de kolom **Activum**. De kolom **Bovenliggende** bevat het gerelateerde bovenliggende activum. Bovendien worden, als er al activa en subactiva zijn gemaakt, in de sectie **Activastructuur** in het deelvenster **Verwante informatie** de activa in een boomstructuur weergegeven.

Zie [Een activum maken](../objects/create-an-object.md) voor meer informatie over het maken van een activum. Als u een subactivum wilt maken, selecteert u het bovenliggende activum in het veld **Bovenliggende** op het sneltabblad **Algemeen**.

## <a name="copy-an-asset-or-asset-structure"></a>Een activa of activastructuur kopiëren

Als uw bedrijf meerdere vergelijkbare activastructuren heeft, kunt u de functie Kopiëren in Activabeheer gebruiken om deze snel te maken.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**.
2. Selecteer op de lijstpagina **Alle activa** het activum dat u wilt kopiëren. Als u bijvoorbeeld de gehele activastructuur, inclusief subactiva, wilt kopiëren, selecteert u een bovenliggend activum.
3. Selecteer **Activum kopiëren**. In de sectie **Kopiëren van** is het veld **Activum** ingesteld op het activum dat u op de lijstpagina hebt geselecteerd.
4. Voer in de sectie **Kopiëren naar** in het veld **Activum** de naam van het nieuwe activum in.
5. Als het activum dat u maakt, deel moet uitmaken van een bestaande activastructuur, selecteert u in de sectie **Bovenliggend activum**, in het veld **Activum** een id van een bovenliggende item.
6. Selecteer **OK**. De nieuwe activastructuur wordt weergegeven op de lijstpagina **Alle activa**. Alle activakenmerken, onderhoudsplannen en onderhoudsronden die zijn gerelateerd aan het activum dat u hebt gekopieerd, worden overgebracht naar het nieuwe activum of de nieuwe activastructuur.

Wanneer u een activastructuur kopieert, hebben de subactiva in de nieuwe structuur dezelfde naam als de subactiva die u hebt gekopieerd. Nadat de kopieerprocedure is voltooid, kunt u de naam en andere instellingen voor een activum eenvoudig wijzigen. Selecteer het activum op de lijstpagina **Alle activa** en selecteer vervolgens de knop **Bewerken**.

> [!NOTE]
> Wanneer u een activum of activastructuur kopieert, wordt de levenscyclusstatus van de nieuwe activa opnieuw ingesteld op de status die u hebt gedefinieerd als de initiële levenscyclusstatus voor activa. De functionele locatie wordt teruggezet naar de standaard functionele locatie.

## <a name="delete-an-asset-or-asset-structure"></a>Een activa of activastructuur verwijderen

Als een activum gerelateerde subactiva heeft, kunt u deze alleen verwijderen als er geen onderhoudsaanvragen, werkordertaken, foutregistraties of toestandsbeoordelingen zijn geregistreerd voor een van de activa.

1. Selecteer op de lijstpagina **Alle activa** het activum dat u wilt verwijderen.
2. Selecteer **Verwijderen**.

> [!NOTE]
> Als u een activum niet kunt verwijderen met behulp van deze procedure, kunt u de verwijdering op een andere wijze uitvoeren door een levenscyclusstatus van activa in te stellen voor dit doel. Zo kunt u bijvoorbeeld een levenscyclusstatus **Buiten gebruik gesteld** of **Verwijderd** instellen op de pagina **Levenscyclusstatussen van activa**.
