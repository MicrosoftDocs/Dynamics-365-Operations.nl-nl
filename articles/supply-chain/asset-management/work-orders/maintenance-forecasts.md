---
title: Prognoses voor onderhoud
description: In dit artikel wordt uitgelegd wat prognoses voor onderhoud zijn in Activabeheer.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c2dbd968a22f2bded29cff3517dacbafc79ff8f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902106"
---
# <a name="maintenance-forecasts"></a>Prognoses voor onderhoud

[!include [banner](../../includes/banner.md)]



Wanneer u een werkorder maakt, kunt u werkordertaken maken die gerelateerde activa en typen onderhoudstaken hebben. Wanneer u een type onderhoudstaak selecteert dat prognoses voor onderhoud bevat, worden de prognoses automatisch naar de werkorder gekopieerd.

U kunt mogelijk prognoseregels toevoegen aan of verwijderen uit een werkorder. De instelling van de levenscyclusstatus van de werkorder, het gerelateerde projecttype en de faseregels die betrekking hebben op het projecttype bepalen of u journaalregels kunt toevoegen of bewerken. Zie [Prognoses, werkorders en projecten](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)voor meer informatie over levenscyclusstatussen van werkorders en gerelateerde projectfasen.

1. Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder in de lijst en selecteer vervolgens in het actievenster > tabblad **Werkorder** > groep **Project** de optie **Prognose**. Op de pagina **Prognose voor onderhoud** worden de prognoseregels van het type onderhoudstaak dat in de werkordertaak is geselecteerd, weergegeven.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Een urenprognose aan een werkorder toevoegen

1. Selecteer op de pagina **Onderhoudsprognose voor werkorders** de werkordertaak waaraan u een prognose wilt toevoegen.

2. Selecteer op het sneltabblad **Uren** de optie **Toevoegen** om een nieuwe regel te maken.

3. Selecteer een categorie in het veld **Categorie**.

4. Voer het aantal voorspelde uren in het veld **Uren** in.

5. Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.


## <a name="add-an-items-forecast-to-a-work-order"></a>Een prognose voor artikelen toevoegen aan een werkorder

Er zijn drie manieren om artikelen aan een onderhoudsprognose voor werkorders toe te voegen. U kunt regels maken voor artikelen (reserve-onderdelen) die niet zijn opgenomen in de lijst met reserve-onderdelen of activumstuklijst, u kunt reserve-onderdelen selecteren in de lijst met goedgekeurde onderdelen of u kunt artikelen selecteren in de activumstuklijst.

- Selecteer op de pagina **Onderhoudsprognose voor werkorders** de werkordertaak waaraan u een prognose wilt toevoegen.

- Voeg op het sneltabblad **Artikelen** de artikelen toe aan de onderhoudsprognose via de desbetreffende methode.

Als u een nieuwe regel wilt maken voor een reserve-onderdeel dat nog niet voorkomt in de lijst met reserve-onderdelen of de activumstuklijst, voert u de volgende stappen uit:

1. Selecteer **Toevoegen**.
2. Selecteer het artikel in het veld **Artikelnummer**.
3. Voer in het veld **Verkoophoeveelheid** de hoeveelheid in.
4. Selecteer de maateenheid van de hoeveelheid in het veld **Eenheid**.
5. Geef in de velden **Kostprijs** en **Valuta** de gewenste waarden op.
6. Selecteer een regeleigenschap in het veld **Regeleigenschap**.
7. Als u de lijst met dimensies wilt wijzigen die op de artikelregels wordt weergegeven, selecteert u **Voorraad** > **Weergavedimensies**, selecteert u de dimensies en stelt u de optie **Instellingen opslaan** in op **Ja**.

Voer de volgende stappen uit om een reserveonderdeel toe te voegen uit een lijst met goedgekeurde reserveonderdelen:

1. Selecteer **Reserveonderdelen toevoegen**.
2. Selecteer het reserveonderdeel en bewerk zo nodig de gerelateerde gegevens.
3. Selecteer **OK**.

Voer de volgende stappen uit om een artikel toe te voegen vanuit de activumstuklijst:

1. Selecteer **Stuklijstartikelen toevoegen**.
2. Selecteer het onderdeel en bewerk zo nodig de gerelateerde gegevens.
3. Selecteer **OK**.

Voor een overzicht van waar het artikel op de geselecteerde regel wordt gebruikt in relatie tot activa, standaardwaarden voor taaktypen, reserveonderdelen en werkorders in Activabeheer, selecteert u **Artikel waar gebruikt**. Zie [Artikel waar gebruikt](../controlling-and-reporting/item-where-used.md) voor meer informatie over dit overzicht.


## <a name="add-an-expense-forecast-to-a-work-order"></a>Een onkostenprognose toevoegen aan een werkorder

1. Selecteer op de pagina **Onderhoudsprognose voor werkorders** de werkordertaak waaraan u een prognose wilt toevoegen.

2. Selecteer op het sneltabblad **Onkosten** de optie **Toevoegen** om een regel te maken.

3. Selecteer een categorie in het veld **Categorie**.

4. Voer in het veld **Hoeveelheid** de hoeveelheid in.

5. Voer de desbetreffende waarden in in de velden **Kostprijs**, **Verkoopvaluta** en **Verkoopprijs**.

6. Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.

>[!NOTE]
>Op het sneltabblad **Totalen van prognose voor onderhoud** wordt een overzicht weergegeven van het aantal regels dat op elk sneltabblad is gemaakt, voor de geselecteerde werkordertaak en voor de werkorder. U ziet ook het totaal van de voorspelde werkuren voor de werkordertaak en de werkorder.

In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Onderhoudsprognose werkorder**.

![Figuur 1.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Prognoses van werkorders automatisch bijwerken

Als uurkosten, artikelkosten en onkosten worden bijgewerkt in andere Microsoft Dynamics 365 for Finance and Operations-modules, kunnen prognoses voor werkorders in Activabeheer automatisch worden bijgewerkt met deze wijzigingen. Deze functie helpt garanderen dat altijd de laatste kostprijzen in uw prognoses voor werkorders gebruikt. U kunt ook soortgelijke updates uitvoeren voor [prognoses voor onderhoudstaken](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Selecteer **Activabeheer** > **Periodiek** > **Prognose** > **Prognose voor werkorder bijwerken**.

2. In het dialoogvenster **Prognose voor werkorder bijwerken** kunt u in het sneltabblad **Op te nemen records** zo nodig selecties toevoegen met betrekking tot specifieke werkorders of werkordertaken. Klik op **Filter** om de relevante selecties te maken.

3. Indien nodig kunt u de automatische update op het Sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.

4. Selecteer **OK** om de update van de prognose te starten.


In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Prognose voor werkorder bijwerken**.

![Figuur 2.](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]