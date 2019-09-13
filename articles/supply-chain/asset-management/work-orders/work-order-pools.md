---
title: Werkordergroepen
description: In dit onderwerp wordt beschreven hoe u met werkordergroepen in Activabeheer werkt.
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875589"
---
# <a name="work-order-pools"></a>Werkordergroepen


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


U kunt werkordergroepen gebruiken om werkorders te groeperen die iets gemeenschappelijk hebben. U kunt bijvoorbeeld werkordergroepen maken voor

- werkploegen, zoals Onderhoudsploeg A, Onderhoudsploeg B  

- professionele vaardigheden, zoals elektriciens of loodgieters  

- fysieke locaties  

- tijdschema's, zoals weken of andere perioden  


Indien nodig kan één werkorder in een groot aantal werkordergroepen worden geplaatst.


## <a name="create-work-order-pool"></a>Werkordergroep maken

In **Alle werkordergroepen** of **Actieve werkordergroepen** kunt u een overzicht van uw werkordergroepen bekijken en nieuwe groepen maken.

1. Klik op **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** of **Actieve werkordergroepen**.

2. Klik op **Nieuw**.

3. Geef een werkordergroep-id op in het veld **Groep** en een naam in het veld **Naam**.

4. Selecteer Ja met de wisselknop **Actief** om aan te geven dat de werkordergroep actief is.

5. Selecteer Ja met de wisselknop **Werkorderrelaties verwijderen** als u wilt dat werkorders automatisch uit de werkordergroep moeten worden verwijderd.

6. Selecteer in het veld **Levenscyclusstatus verwijderen** de status van de levenscyclus van de werkorder. De levenscyclusstatus voor het voltooien van een werkorder kan bijvoorbeeld worden ingesteld om automatisch relaties met werkordergroepen te verwijderen.

7. U kunt direct beginnen met het toevoegen van werkorders aan uw werkordergroep. Klik op het sneltabblad **Werkorders** op **Regel toevoegen**.

8. Selecteer een werkorder in het veld **Werkorder**. De gerelateerde velden worden automatisch bijgewerkt.

9. Herhaal stap 7-8 als u meer werkorders wilt toevoegen.

10. In het veld **Sorteervolgorde** kunt u aangeven of de werkorders in een bepaalde volgorde moeten worden uitgevoerd. Voeg getallen 1, 2, 3, enzovoort in om een specifieke volgorde voor de geselecteerde werkorders aan te geven.

11. Klik op de knop **Werkorders** om een lijst weer te geven van alle werkorders in de werkordergroep.

12. Klik op de knop **Capaciteitsbelasting** als u **Capaciteitsbelasting** wilt openen om de capaciteitsbelasting te berekenen en weer te geven voor onderhoudsplanning, niet-geplande werkorders en geplande werkorders.

13. Klik op de knop **Artikelprognose** om de **Artikelprognose** te openen waar u prognoses voor artikelen (reserve-onderdelen en andere vereiste artikelen) kunt berekenen en weergeven met betrekking tot onderhoudsplanning, niet-geplande werkorders en geplande werkorders.

14. Klik op de knop **Opdracht tot inkoop voor werkorder** om de lijst **Opdracht tot inkoop voor werkorder** te openen en een lijst weer te geven van inkoopbestelopdrachten die betrekking hebben op de werkorders in de werkordergroep.

15. Klik op de knop **Inkoop werkorder** om de lijst **Inkoop werkorder** te openen en een lijst weer te geven van inkooporders die betrekking hebben op de werkorders in de werkordergroep.

>[!NOTE]
>Wanneer een werkordergroep niet meer relevant is voor uw werkplanning, stelt u het selectievakje **Actief** voor die groep in de lijstweergave van de **Werkordergroep** in op Nee.

Schakel het selectievakje **Werkorderrelaties verwijderen** in als u alle werkorderregels wilt verwijderen, bijvoorbeeld om een lege groep te maken die u later voor andere werkorders kunt gebruiken. Vergeet niet om het selectievakje **Werkorderrelaties verwijderen** uit te schakelen als u de werkordergroep later wilt gebruiken om nieuwe werkorderrelaties te maken.


![Figuur 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Werkorder toevoegen aan een werkordergroep

Zoals in bovenstaande sectie is beschreven, kunt u werkorders aan een werkordergroep toevoegen wanneer u de groep maakt. U kunt een werkorder ook aan een werkordergroep toevoegen vanuit de lijst **Alle werkorders**.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder in de lijst en klik op **Werkordergroep**.

3. Selecteer Toevoegen in het veld **Toevoegen/verwijderen**.

4. Selecteer de werkordergroep in het veld **Groep**.

5. Klik op **OK**.

6. Nadat u een werkorder aan een werkordergroep hebt toegevoegd, kunt u de werkorders in een bepaalde volgorde in de groep plaatsen. Open een van de lijstpagina's met werkordergroepen, selecteer de groep en klik op **Bewerken**. Pas de sorteervolgorde van de werkorders in de groep aan in het formulier **Werkordergroep** > sneltabblad **Werkorders** > veld **Sorteervolgorde**.

Als u de geselecteerde werkorder uit een werkordergroep wilt verwijderen, selecteert u in stap 3 de optie Verwijderen.

