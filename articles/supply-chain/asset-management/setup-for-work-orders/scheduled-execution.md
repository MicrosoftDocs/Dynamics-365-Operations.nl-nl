---
title: Geplande uitvoering
description: In dit onderwerp wordt geplande uitvoering in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215511"
---
# <a name="scheduled-execution"></a>Geplande uitvoering

[!include [banner](../../includes/banner.md)]

 

U kunt serviceniveaus van werkorders gebruiken om geplande uitvoering in te stellen. (Zie [Serviceniveau en omschrijving](service-level-and-description.md)voor meer informatie over service niveaus van werkorders.) Geplande uitvoering biedt flexibiliteit bij werkplanning voor onderhoudsmedewerkers, omdat u meer gedetailleerde of minder gedetailleerde vereisten kunt instellen voor het interval waarin een werkorder moet worden voltooid. Een onderhoudsmedewerker die een taak sneller dan verwacht in een productiefaciliteit voltooid, kan bijvoorbeeld naar een andere nabijgelegen taak gaan die gepland is voor de huidige week, maar niet noodzakelijkerwijs voor de huidige dag. Deze aanpak maakt optimalisatie van werknemersplanning en taakvoltooiing mogelijk.

De instellingen van de geplande uitvoering, die betrekking hebben op werkorders, kunnen algemeen of specifiek zijn. U kunt algemene regels instellen die niet beperkt zijn tot specifieke typen werkorders, activatypen, enzovoort. U kunt ook geplande uitvoeringsregels maken die van toepassing zijn op een specifiek type werkorder, activatype, type onderhoudstaak, enzovoort.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Geplande uitvoering**.
2. Selecteer **Nieuw** om een geplande uitvoeringsregel te maken.
3. Selecteer in de **Functionele locatie**, **Type werkorder**, **Activatype**, **Fabrikant**, **Model**, **Categorie type onderhoudstaak**, **Type onderhoudstaak**, **Type onderhoudstaak Variant** en **Handels**-velden. Selecteer waarden als u ze nodig hebt.
4. Selecteer in het veld **Serviceniveau** een serviceniveau van een werkorder. Als u dit veld leeg laat, kunt u het meest algemene type geplande uitvoeringsregel maken. Zie het eerste record in de volgende afbeelding voor een voor beeld van een algemene regel. Op die regel kunnen alle werkorders waarvoor geen serviceniveau is ingesteld, voor een bepaalde datum en tijd worden gepland.
5. Selecteer de tijdseenheid in het veld **Geplande uitvoering**.
6. Selecteer **Opslaan**.

![Geplande uitvoering](media/20-setup-for-work-orders.png)
