---
title: Inkoop
description: In dit onderwerp wordt de inkoop in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f3e01dd85cbe8e2b2c9095431f3e0aead817a5a5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352757"
---
# <a name="procurement"></a>Inkoop

[!include [banner](../../includes/banner.md)]

In Activabeheer kunt u een overzicht bekijken van opdrachten tot inkoop en inkooporders die betrekking hebben op werkorders. U kunt ook vanuit een werkorder een inkooporder of opdracht tot inkoop maken.

De lijstpagina **Opdracht tot inkoop voor werkorder** (**Activabeheer** > **Algemeen** > **Inkoop** > **Opdracht tot inkoop voor werkorder**) toont een lijst van opdrachten tot inkoop die betrekking hebben op werkorders. Wanneer u op deze pagina een werkordertaak selecteert, kunt u de knoppen in de groep **Tonen** van het tabblad **Opdracht tot inkoop voor werkorder** van het actievenster gebruiken om diverse acties uit te voeren:

- Selecteer **Opdracht tot inkoop** om de gerelateerde opdracht tot inkoop te openen. 
- Selecteer **Werkorder** om de gerelateerde werkorder te openen.
- Voor een overzicht van waar het artikel op de geselecteerde regel wordt gebruikt in relatie tot activa, standaardwaarden voor taaktypen, reserveonderdelen en werkorders in Activabeheer, selecteert u **Artikel waar gebruikt**. Zie [Artikel waar gebruikt](../controlling-and-reporting/item-where-used.md) voor meer informatie over dit overzicht.

In de onderstaande afbeelding ziet u een voorbeeld van de lijstpagina **Opdracht tot inkoop voor werkorder**.

![Figuur 1.](media/08-work-orders.png)


De lijstpagina **Inkoop werkorder** (**Activabeheer** > **Algemeen** > **Inkoop** > **Inkoop werkorder**) toont een lijst van inkooporders die betrekking hebben op werkorders. Wanneer u op deze pagina een werkordertaak selecteert, kunt u de knoppen in de groep **Tonen** van het tabblad **Inkoop werkorder** van het actievenster gebruiken om diverse acties uit te voeren:

- Selecteer **Inkooporder** om de gerelateerde inkooporder te openen. 
- Selecteer **Werkorder** om de gerelateerde werkorder te openen.
- Voor een overzicht van waar het artikel op de geselecteerde regel wordt gebruikt in relatie tot activa, standaardwaarden voor taaktypen, reserveonderdelen en werkorders in Activabeheer, selecteert u **Artikel waar gebruikt**. Zie [Artikel waar gebruikt](../controlling-and-reporting/item-where-used.md) voor meer informatie over dit overzicht.

In de onderstaande afbeelding ziet u een voorbeeld van de lijstpagina **Inkoop werkorder**.

![Figuur 2.](media/09-work-orders.png)


Op de lijstpagina **Inkoop werkorder** en de lijstpagina **Opdracht tot inkoop voor werkorder** wordt er rechts van elke regel een symbool weergegeven dat is gerelateerd aan de controle van de leveringsdatum. Als het pictogram een uitroepteken in een rode cirkel is, betekent dit dat de levering van de betreffende inkooporder of opdracht tot inkoop mogelijk is vertraagd.

Voor een inkooporder heeft de datum betrekking op de inkooporderregel die is gebruikt om een mogelijke vertraging te berekenen. Als u deze datum wilt bekijken, selecteert u de inkooporderregel op de pagina **Inkooporder**. De datum wordt weergegeven in het veld **Bevestigde leveringsdatum** van het tabblad **Instellingen** van het sneltabblad **Regeldetails**. Als het veld **Bevestigde leveringsdatum** niet is ingesteld, wordt de datum in het veld **Leveringsdatum** van het sneltabblad **Inkooporderkoptekst** voor de berekening gebruikt. Een van deze datums wordt in de volgende volgorde vergeleken met de beschikbare datum op de werkorder of werkordertaak:

1. Werkelijke begindatum op de werkorder  

2. Geplande begindatum op de betreffende werkordertaak 

3. Geplande begindatum op de werkorder 

4. Verwachte begindatum op de werkorder 

Voor een opdracht tot inkoop wordt de datum in het veld **Gevraagde datum** op het sneltabblad **Inkooporderkoptekst** van de pagina **Opdrachten tot inkoop** gebruikt om een mogelijke vertraging te berekenen. De datum in dat veld wordt in dezelfde volgorde met de beschikbare datum op de werkorder of werkordertaak vergeleken als bij een inkooporder.


## <a name="create-a-purchase-order-from-a-work-order"></a>Een inkooporder maken op basis van een werkorder

Op de lijstpagina **Alle werkorders** kunt u een werkordertaak selecteren en vervolgens een bijbehorende inkooporder of opdracht tot inkoop maken. Op die manier kunt projectrelaties tussen de inkooporder of de opdracht tot inkoop en de werkorder bewerkstelligen.

1. Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder waarvoor u een inkooporder wilt maken en selecteer **Bewerken**.

3. Selecteer op het sneltabblad **Onderhoudstaken voor werkorders** de werkordertaak waarvoor u de inkooporder wilt maken.

4. Selecteer **Artikeltaken** > **Inkooporder van werkordertaak**.

5. Klik op de lijstpagina **Projectinkooporders** op **Nieuw**.

6. Maak de inkooporder.

>[!NOTE]
>Voer dezelfde stappen uit om een bijbehorende opdracht tot inkoop te maken. Selecteer in stap 4 echter **Artikeltaken** > **Opdracht tot inkoop van werkorder**.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projectrelatie tussen werkorder en inkooporder of opdracht tot inkoop

Een inkooporderregel of regel in een opdracht tot inkoop is gerelateerd aan een werkordertaak via het werkorderproject en het gerelateerde nummer van de projectactiviteit. Wanneer u een inkooporder of opdracht tot inkoop maakt vanuit een werkordertaak, is het bijbehorende nummer van de projectactiviteit verplicht. Als alle werkordertaken in de betreffende werkorder hetzelfde type onderhoudstaak hebben, wordt het nummer van de projectactiviteit automatisch ingevoegd op de inkooporder of opdracht tot inkoop. Als de werkordertaken verschillende typen onderhoudstaken hebben, moet u het nummer van de projectactiviteit handmatig op de inkooporder of opdracht tot inkoop invoeren.

Als u het activiteitsnummer wilt bekijken of invoeren dat aan een inkooporderregel is gekoppeld, selecteert u de inkooporderrecord op de lijstpagina **Inkoop werkorder** en selecteert u vervolgens in de kolom **Inkooporder** de koppeling voor de inkooporder. U vindt het veld **Activiteitsnummer** op het tabblad **Project** van het sneltabblad **Regeldetails**.

In onderstaande afbeelding ziet u een voorbeeld van de pagina **Inkooporder** met de focus op het **Activiteitsnummer**.

![Figuur 3.](media/10-work-orders.png)

En als u het activiteitsnummer wilt bekijken of invoeren dat aan een regel voor een opdracht tot inkoop voor werkorder is gekoppeld, selecteert u de record van de opdracht tot inkoop op de lijstpagina **Opdracht tot inkoop voor werkorder** en selecteert u in de kolom **Opdracht tot inkoop** de koppeling voor de opdracht tot inkoop. U vindt het veld **Activiteitsnummer** op het tabblad **Project** van het sneltabblad **Regeldetails**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]