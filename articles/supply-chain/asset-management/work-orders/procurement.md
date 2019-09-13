---
title: Inkoop
description: In dit onderwerp wordt de inkoop in Activabeheer uitgelegd.
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
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875586"
---
# <a name="procurement"></a>Inkoop


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In Activabeheer kunt u een overzicht bekijken van opdrachten tot inkoop en inkooporders met betrekking tot werkorders. Het is ook mogelijk om vanuit een werkorder een inkooporder of opdracht tot inkoop te maken.

In de lijst **Opdracht tot inkoop voor werkorder** (**Activabeheer** > **Algemeen** > **Inkoop** > **Opdracht tot inkoop voor werkorder**) ziet u een lijst van opdrachten tot inkoop die betrekking hebben op werkorders.

- Selecteer een werkordertaak in de lijst **Opdracht tot inkoop voor werkorder** en klik op de knop **Opdracht tot inkoop** om de betreffende opdracht tot inkoop te openen.  
- Selecteer een werkordertaak in de lijst **Opdracht tot inkoop voor werkorder** en klik op de knop **Werkorder** om de betreffende werkorder te openen.  
- Selecteer een werkordertaak in de lijst **Opdracht tot inkoop voor werkorder** en klik op de knop **Artikel waar gebruikt** voor een overzicht van waar het artikel op de geselecteerde regel in Activabeheer wordt gebruikt in relatie tot activa, standaardwaarden voor onderhoudstaaktypen, reserveonderdelen en werkorders. 

![Figuur 1](media/08-work-orders.png)


In de lijst **Opdracht tot inkoop voor werkorder** (**Activabeheer voor bedrijven** > **Algemeen** > **Inkoop** > **Opdracht tot inkoop voor werkorder**) ziet u een lijst van inkooporders die betrekking hebben op werkorders.

- Selecteer een werkordertaak in de lijst **Opdracht tot inkoop voor werkorder** en klik op de knop **Inkooporder** om de betreffende inkooporder te openen.  
- Selecteer een werkordertaak in de lijst **Inkoop werkorder** en klik op de knop **Werkorder** om de betreffende werkorder te openen.  
- Selecteer een werkordertaak in de lijst **Inkoop werkorder** en klik op de knop **Artikel waar gebruikt** voor een overzicht van waar het artikel op de geselecteerde regel in Activabeheer wordt gebruikt in relatie tot activa, standaardwaarden voor onderhoudstaaktypen, reserveonderdelen en werkorders. 

![Figuur 2](media/09-work-orders.png)


In de lijsten hierboven ziet u rechts op elke regel een pictogram met betrekking tot de leveringsdatum. Als het pictogram een uitroepteken in een rode cirkel bevat, betekent dit dat de levering voor de betreffende opdracht tot inkoop of inkooporder mogelijk is vertraagd.

Op een opdracht tot inkoop vindt u de datum die wordt gebruikt om een mogelijke vertraging te berekenen in het formulier **Opdrachten tot inkoop** > sneltabblad **Koptekst van opdracht tot inkoop**> veld **Gevraagde datum**. Deze datum wordt op dezelfde manier vergeleken met de beschikbare datum op de werkorder of werkordertaak als de datum van de inkooporder.

De datum op een inkooporder die wordt gebruikt om een mogelijke vertraging te berekenen, is de datum die is gekoppeld aan de inkooporderregel. Deze wordt weergegeven in het formulier **Inkooporder** > selecteer inkooporderregel > sneltabblad **Regeldetails** > tabblad **Instellingen** > **Bevestigde leveringsdatum**. Als dat veld niet is ingevuld, wordt de datum in het veld **Leveringsdatum** op het sneltabblad **Inkooporderkoptekst** gebruikt. Een van deze datums wordt in de volgende volgorde vergeleken met de beschikbare datum op de werkorder of werkordertaak:

- Werkelijke begindatum op de werkorder of  

- Geplande begindatum op de betreffende werkordertaak of  

- Geplande begindatum op de werkorder of  

- Verwachte begindatum op de werkorder  


## <a name="create-purchase-order-from-a-work-order"></a>Een inkooporder maken op basis van een werkorder

Selecteer in **Alle werkorders** een werkordertaak en maak een bijbehorende inkooporder of opdracht tot inkoop. U zorgt er zo voor dat projectrelaties tussen de inkooporder of de opdracht tot inkoop en de werkorder behouden blijven.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer in de lijst **Alle werkorders** of **Actieve werkorders** de werkorder waarvoor u een inkooporder wilt maken. Klik vervolgens op **Bewerken**.

3. Selecteer in het formulier **Werkorder** > tabblad **Onderhoudstaken voor werkorders** de werkordertaak waarvoor u de inkooporder wilt maken.

4. Klik op **Artikeltaken** > **Inkooporder van werkordertaak**.

5. Klik op de lijstpagina **Projectinkooporders** op **Nieuw**.

6. Maak de inkooporder.

>[!NOTE]
>Het maken van een opdracht tot inkoop is bijna gelijk aan het maken van een inkooporder. Het enige verschil is dat u in de bovenstaande procedure in stap 2 op **Artikeltaken** > **Opdracht tot inkoop van werkordertaak** klikt.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projectrelatie tussen werkorder en inkooporder of opdracht tot inkoop

Een inkooporderregel of regel in een opdracht tot inkoop is gerelateerd aan een werkordertaak via het werkorderproject en het gerelateerde nummer van de projectactiviteit. Wanneer u een inkooporder of opdracht tot inkoop maakt vanuit een werkordertaak, is het bijbehorende nummer van de projectactiviteit verplicht. Het nummer van de projectactiviteit wordt automatisch ingevoegd op een inkooporder of opdracht tot inkoop als de bijbehorende werkorder werkordertaken bevat die allemaal hetzelfde type onderhoudstaak gebruiken. Als de werkordertaken verschillende onderhoudstaaktypen bevatten, moet u het nummer van de projectactiviteit handmatig invoegen.

Als u het activiteitsnummer met betrekking tot een inkooporderregel wilt bekijken of invoegen, opent u **Inkoop werkorder** > selecteert u de inkooporderrecord > klikt u op de inkooporder in de kolom **Inkooporder** > sneltabblad **Regeldetails** > tabblad **Project** > veld **Activiteitsnummer**.


![Figuur 3](media/10-work-orders.png)


En als u het activiteitsnummer met betrekking tot een regel in de opdracht tot inkoop voor werkorder wilt bekijken of invoegen, opent u **Opdracht tot inkoop voor werkorder** > selecteert u de record van de opdracht tot inkoop > klikt u op de opdracht tot inkoop in de kolom **Opdracht tot inkoop** > sneltabblad **Regeldetails** > tabblad **Project** > veld **Activiteitsnummer**.

