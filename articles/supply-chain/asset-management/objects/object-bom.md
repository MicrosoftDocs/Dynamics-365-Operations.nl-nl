---
title: Activumstuklijsten
description: Dit artikel beschrijft activumstuklijsten in Activabeheer.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 665c705e3ffb617fc159a1223cb3f776878d5cd2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016241"
---
# <a name="asset-boms"></a>Activumstuklijsten

[!include [banner](../../includes/banner.md)]

 

Dit artikel beschrijft activumstuklijsten in Activabeheer. Op de pagina **Activumstuklijst** wordt een lijst weergegeven met alle artikelen (reserveonderdelen en andere artikelen) die gedurende de hele levensduur op een activum worden gebruikt. Wanneer u een nieuw activum maakt, moet u overwegen om een activumstuklijst in te stellen als onderdeel van de instellingsprocedure. Op deze manier kunt u de artikelhistorie voor het activum bijhouden vanaf de aanmaakdatum.

Nadat u een onderhoudstaak hebt voltooid en het artikelverbruik is geregistreerd op een werkorder, kunt u het verbruik van reserveonderdelen en andere artikelen bijhouden die voor het activum zijn gebruikt. Met deze functionaliteit kunt u een volledig artikelverbruikrecord bijhouden voor al uw activa. U kunt de record bijvoorbeeld gebruiken om te controleren of een specifiek reserveonderdeel vaak wordt vervangen of om de reserveonderdelen of andere artikelen bij te houden die momenteel voor een activum worden gebruikt.

> [!NOTE]
> Op een werkorder kan artikelverbruik zowel reserveonderdelen als andere extra artikelen bevatten, zoals smeermiddelen, bouten en pakkingen.

Een activumstuklijst kan automatisch worden bijgewerkt op basis van de instellingen in Activabeheer. Als de levenscyclusstatus van een werkorder is gemaakt voor het afhandelen van afgeronde of voltooide werkorders en als de optie **Activumstuklijst bijwerken** voor de levenscyclusstatus van de werkorder is ingesteld op **Ja** op de pagina **Levenscyclusstatussen van werkorders**, worden alle artikelen die op de werkorder zijn gebruikt, automatisch bijgewerkt op de pagina **Activumstuklijst** wanneer de werkorder wordt bijgewerkt naar die levenscyclusstatus. 


U kunt een activumstuklijst ook handmatig bijwerken door nieuwe artikelregels te maken op de pagina **Activumstuklijst**.

Op de pagina **Activumstuklijst** kunt u de historie van reserveonderdelen bijhouden voor activa nadat het artikelverbruik is geregistreerd op een werkorder. Als u deze functionaliteit wilt gebruiken, moet u de artikelgroepen selecteren die moeten worden gebruikt voor de registratie van reserveonderdelen op de pagina **Artikelgroepen reserveonderdelen**.

Als u de functionaliteit activumstuklijst wilt gebruiken, moet u eerst de vereiste artikelgroepen voor reserveonderdelen instellen. Als u vervolgens wilt dat de activumstuklijst automatisch wordt bijgewerkt wanneer een werkorder is voltooid, kunt u een levenscyclusstatus van een werkorder instellen om die update af te handelen. 


## <a name="set-up-spare-parts-item-groups"></a>Artikelengroepen voor reserveonderdelen instellen

Het instellen van de historie van reserveonderdelen is gebaseerd op artikelgroepen die zijn gemaakt in de module **Voorraad- en magazijnbeheer**. In Activabeheer stelt u artikelgroepen in, zodat u de historie van reserveonderdelen voor de artikelen in de geselecteerde artikelgroepen kunt bijhouden.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activum** \> **Artikelgroepen reserveonderdelen**.
2. Selecteer **Nieuw** om een artikelgroep in te stellen.
3. Selecteer de groep in het veld **Artikelgroep**. De naam van de groep wordt automatisch in het veld **Naam** ingevoerd.

## <a name="view-and-update-asset-boms"></a>Activumstuklijsten weergeven en bijwerken

Nadat u artikelverbruik op een werkorder hebt geboekt, kunt u het geregistreerde artikelverbruik weergeven op de pagina **Activumstuklijst**.

1. Selecteer **Activabeheer** \> **Activa** \> **Actieve activa**. Selecteer het activum in de lijst en selecteer **Activumstuklijst**.

    > [!NOTE]
    > Als u alle artikelverbruikregistraties voor alle activa wilt weergeven, selecteert u **Activabeheer** \> **Query's** \> **Activa** \> **Activumstuklijst**.

2. Selecteer **Activumstuklijst bijwerken**. U kunt desgewenst activa, activatypen en resources aan de update toevoegen met **Selecteren**. Selecteer **OK** om de update te starten. U kunt de functie Update ook instellen als batchtaak.
3. Als u meer informatie wilt zien die betrekking heeft op de artikelen, kunt u voorraaddimensies toevoegen. Selecteer **Voorraad** \> **Weergave van dimensies** en schakel vervolgens de selectievakjes in voor de dimensies die u wilt weergeven. Als u deze instellingen voor alle activa op de pagina **Activumstuklijst** wilt behouden , stelt u de optie **Instellingen opslaan** in op **Ja**.
4. Voor een overzicht van waar in Activabeheer het artikel op de geselecteerde regel wordt gebruikt in relatie tot activa, standaardwaarden voor taaktypen, reserveonderdelen en werkorders, selecteert u **Artikel waar gebruikt**. 
5. Als u alleen actieve artikelregels wilt zien, selecteert u **Weergeven** \> **Huidige**. Als u alle artikelregels wilt zien, inclusief regels waarvan de vervaldatum vóór de huidige datum valt, selecteert u **Weergeven** \> **Alles**.

> [!NOTE]
> Wanneer u een werkorder hebt voltooid en bepaalde artikelen of reserveonderdelen die samenhangen met het gerelateerde activum, zijn verlopen of zijn vervangen door andere artikelen of reserveonderdelen, kunt u de activumstuklijst het beste ook bijwerken.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Een nieuwe artikelregel maken in een activumstuklijst

U kunt handmatig artikelregels voor activa maken.

1. Selecteer **Nieuw** op de pagina **Activumstuklijst**.
2. Selecteer in het veld **Activum** het activum waarvoor u een artikelregel wilt toevoegen.
3. Voer in het veld **Regelnummer** een volgnummer voor de regel in.
4. Selecteer een begindatum voor het artikel in het veld **Geldig vanaf**.
5. Als het artikel vervalt, geeft u een einddatum op in het veld **Vervaldatum**.
6. Selecteer het artikel in het veld **Artikelnummer**. De naam wordt automatisch in het veld **Productnaam** ingevoerd.
7. Voer in het veld **Hoeveelheid** de gebruikte hoeveelheid in. Het veld **Eenheid** wordt automatisch bijgewerkt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]