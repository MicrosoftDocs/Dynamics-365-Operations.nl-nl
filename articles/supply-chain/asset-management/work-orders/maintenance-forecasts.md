---
title: Prognoses voor onderhoud
description: In dit onderwerp wordt uitgelegd wat prognoses voor onderhoud zijn in Activabeheer.
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
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875591"
---
# <a name="maintenance-forecasts"></a>Prognoses voor onderhoud

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Wanneer u een werkorder maakt, kunt u werkordertaken maken met gerelateerde activa en typen onderhoudstaken. Wanneer u een type onderhoudstaak selecteert dat prognoses voor onderhoud bevat, worden de prognoses automatisch naar de werkorder gekopieerd.

U kunt mogelijk prognoseregels toevoegen aan of verwijderen uit een werkorder. De instelling van de levenscyclusstatus van een werkorder, het gerelateerde projecttype en de faseregels die betrekking hebben op het projecttype bepalen of u prognoseregels kunt toevoegen of bewerken. 

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder in de lijst en klik op **Prognose**. In **Prognose voor onderhoud** worden de prognoseregels van het type onderhoudstaak dat in de werkordertaak is geselecteerd, weergegeven.


## <a name="add-hours-forecast-to-a-work-order"></a>Urenprognose aan een werkorder toevoegen

1. Selecteer de werkordertaak waaraan u een prognose wilt toevoegen.

2. Ga naar het sneltabblad **Uren** en klik op **Toevoegen** om een nieuwe regel te maken.

3. Selecteer een categorie in het veld **Categorie**.

4. Voer het aantal voorspelde uren in het veld **Uren** in.

5. Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.


## <a name="add-items-forecast-to-a-work-order"></a>Artikelen toevoegen aan een werkorder

Er zijn drie manieren om artikelen aan een prognose voor werkorderonderhoud toe te voegen: u kunt regels maken voor artikelen (reserve-onderdelen) die niet zijn opgenomen in de lijst met reserve-onderdelen of activumstuklijst, u kunt reserve-onderdelen selecteren in de lijst met goedgekeurde onderdelen en u kunt artikelen selecteren in de activumstuklijst.

1. Selecteer de werkordertaak waaraan u een prognose wilt toevoegen.

2. Selecteer het sneltabblad **Artikelen**.

3. Klik op **Toevoegen** als u een nieuwe regel wilt maken voor een reserve-onderdeel dat nog niet voorkomt in de lijst met reserve-onderdelen of de activumstuklijst.

4. Selecteer het artikel in het veld **Artikelnummer**.

5. Typ een hoeveelheid in het veld **Verkoophoeveelheid** en selecteer een hoeveelheidseenheid in het veld **Eenheid**.

6. Voeg de kostprijs en valuta in de betreffende velden in en selecteer een **Regeleigenschap**.

7. Als u de lijst met dimensies wilt wijzigen die op de artikelregels wordt weergegeven, klikt u op **Voorraad** > **Weergavedimensies**, selecteert u de dimensies en selecteert u Ja op de wisselknop **Instellingen opslaan**.

8. Als u een goedgekeurd reserve-onderdeel aan de prognose voor onderhoud wilt toevoegen, klikt u op **Reserve-onderdelen toevoegen**, selecteert u het reserve-onderdeel, wijzigt u indien nodig gerelateerde gegevens en klikt u op **OK**.

9. Als u activumstuklijstartikelen aan de prognose wilt toevoegen, klikt u op **Stuklijstartikelen toevoegen**, selecteert u het artikel, wijzigt u gerelateerde informatie als dat nodig is en klikt u op **OK**.

10. Klik op **Artikel waar gebruikt** voor een overzicht van waar het artikel op de geselecteerde regel in Activabeheer wordt gebruikt in relatie tot activa, standaardwaarden voor onderhoudstaaktypen, reserveonderdelen en werkorders. 



## <a name="add-expense-forecast-to-a-work-order"></a>Onkostenprognose toevoegen aan een werkorder

1. In dit onderwerp wordt uitgelegd hoe u een onkostenprognose aan een werkorder toevoegt. Selecteer de werkordertaak waaraan u een prognose wilt toevoegen in de linkerzijde van het formulier.

2. Selecteer het sneltabblad **Onkosten**.

3. Klik op **Toevoegen** om een nieuwe regel te maken.

4. Selecteer een categorie in het veld **Categorie**.

5. Voer in het veld **Hoeveelheid** een hoeveelheid in.

6. Voeg kostprijs, verkoopvaluta en verkoopprijs in de relevante velden in.

7. Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.

>[!NOTE]
>Op het sneltabblad **Totalen van prognose voor onderhoud** kunt u een overzicht bekijken van het aantal regels dat op elk tabblad is gemaakt, voor de geselecteerde werkordertaak en voor de werkorder. U kunt ook een som weergeven van de voorspelde werkuren voor de werkordertaak en de werkorder.

![Figuur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Prognoses van werkorders automatisch bijwerken

In Activabeheer kunt u eventuele wijzigingen in prognoses voor werkorders die betrekking hebben op uurkosten, artikelkosten en onkosten, automatisch bijwerken als ze zijn bijgewerkt in andere Dynamics 365 for Finance and Operations-modules. Op die manier worden altijd de laatste kostprijzen in uw prognoses voor werkorders gebruikt. Het is ook mogelijk om soortgelijke updates te maken voor [prognoses voor onderhoudstaken](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Klik op **Activabeheer** > **Periodiek** > **Prognose** > **Prognose voor werkorder bijwerken**.

2. In het vervolgkeuzevenster **Prognose voor werkorder bijwerken** kunt u zo nodig selecties toevoegen met betrekking tot specifieke werkorders of werkordertaken. Klik op **Filter** om deze selecties te maken.

3. Indien nodig kunt u de automatische update op het sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.

4. Klik op **OK** om de update van de prognose te starten.


![Figuur 2](media/07-work-orders.png)

