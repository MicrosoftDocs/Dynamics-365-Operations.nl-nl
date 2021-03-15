---
title: Werkordergroepen
description: In dit onderwerp wordt beschreven hoe u met werkordergroepen in Activabeheer werkt.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: afea5b8d0f958c3ab53d6cef8c9a0e9030d7c67b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017512"
---
# <a name="work-order-pools"></a>Werkordergroepen

[!include [banner](../../includes/banner.md)]


U kunt werkordergroepen gebruiken om werkorders te groeperen die iets gemeenschappelijk hebben. Hier volgen enkele voorbeelden van zaken waarvoor u werkordergroepen kunt maken:

- Werkploegen, zoals Onderhoudsploeg A of Onderhoudsploeg B  

- Professionele vaardigheden, zoals elektriciens of loodgieters  

- Fysieke locaties  

- Tijdschema's, zoals weken of andere perioden  

U kunt een werkorder zo nodig in meerdere werkplaatsgroepen plaatsen.


## <a name="create-a-work-order-pool"></a>Een werkordergroep maken

Op de lijstpagina **Alle werkordergroepen** of **Actieve werkordergroepen** kunt u een overzicht van uw werkordergroepen bekijken en nieuwe groepen maken.

1. Selecteer **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** of **Actieve werkordergroepen**.

2. Selecteer **Nieuw**.

3. Voer in het veld **Groep** een id voor de werkordergroep in.

4. in het veld **Naam** een naam in.

5. Stel de optie **Actief** in op **Ja** om aan te geven dat de werkordergroep actief is.

6. Stel de optie **Werkorderrelaties verwijderen** in op **Ja** als u wilt dat werkorders automatisch uit de werkordergroep moeten worden verwijderd.

7. Selecteer in het veld **Levenscyclusstatus verwijderen** de status van de levenscyclus van de werkorder. De levenscyclusstatus voor het voltooien van een werkorder kan bijvoorbeeld worden ingesteld om automatisch relaties met werkordergroepen te verwijderen.

    U kunt direct beginnen met het toevoegen van werkorders aan uw werkordergroep.

8. Selecteer op het sneltabblad **Werkorders** de optie **Regel toevoegen**.

9. Selecteer een werkorder in het veld **Werkorder**. De gerelateerde velden worden automatisch bijgewerkt.

10. Herhaal stap 8 en 9 als u nog meer werkorders wilt toevoegen.

11. Als de werkorders die u hebt toegevoegd in een bepaalde volgorde moeten worden uitgevoerd, kunt u in het veld **Sorteervolgorde** de getallen **1**, **2**, **3**, enzovoort, invoeren om die volgorde op te geven.

12. Als u een lijst wilt weergeven met alle werkorders die in de werkordergroep zijn opgenomen, gaat u in het actievenster naar het tabblad **Werkordergroep** en selecteert u in de groep **Voor werkordergroep weergeven** de optie **Werkorders** om de lijstpagina **Alle werkorders** te openen.

13. Als u de capaciteitsbelasting voor de onderhoudsplanning, niet-geplande werkorders en geplande werkorders wilt berekenen en weergeven, gaat u naar het actievenster en selecteert u op het tabblad **Werkordergroep** in de groep **Voor werkordergroep weergeven** de optie **Capaciteitsbelasting** om het dialoogvenster **Capaciteitsbelasting berekenen** te openen.

14. Als u de prognoses voor artikelen (reserve-onderdelen en andere noodzakelijke artikelen) voor de onderhoudsplanning, niet-geplande werkorders en geplande werkorders wilt berekenen en weergeven, gaat u naar het actievenster en selecteert u op het tabblad **Werkordergroep** in de groep **Voor werkordergroep weergeven** de optie **Artikelprognose** om het dialoogvenster **Artikelprognose berekenen** te openen.

15. Als u een lijst wilt weergeven met opdrachten tot inkoop voor de werkorders in de werkordergroep, gaat u in het actievenster naar het tabblad **Werkordergroep** en selecteert u in de groep **Inkoop** de optie **Opdracht tot inkoop voor werkorder** om de lijstpagina **Opdracht tot inkoop voor werkorder** te openen.

16. Als u een lijst wilt weergeven met opdrachten voor de werkorders in de werkordergroep, gaat u in het actievenster naar het tabblad **Werkordergroep** en selecteert u in de groep **Inkoop** de optie **Opdracht tot inkoop voor werkorder** om de lijstpagina **Opdracht tot inkoop voor werkorder** te openen.

>[!NOTE]
>Wanneer een werkordergroep niet meer relevant is voor uw werkplanning, stelt u de optie **Actief** voor die groep in de lijstweergave van de **Werkordergroep** in op **Nee**.

Als u alle werkorderregels wilt verwijderen, stelt u de optie **Werkorderrelaties verwijderen** in op **Ja**. Deze optie is handig als u bijvoorbeeld een lege groep wilt maken die u later voor andere werkorders kunt gebruiken. Wanneer u later de werkordergroep wilt gebruiken om nieuwe werkorderrelaties te maken, mag u niet vergeten om de optie **Werkorderrelaties verwijderen** in te stellen op **Nee**.

In de onderstaande afbeelding ziet u een voorbeeld van de lijstpagina **Werkordergroep**.

![Figuur 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Een werkorder toevoegen aan een werkordergroep

Zoals in de voorgaande sectie is beschreven, kunt u werkorders aan een werkordergroep toevoegen wanneer u die groep maakt. U kunt werkorders ook aan een werkordergroep toevoegen via de lijstpagina **Alle werkorders** of **Actieve werkorders**.

1. Selecteer de werkorder en selecteer vervolgens in het actievenster op het tabblad **Werkorder** in de groep **Onderhoud** de optie **Werkordergroep**.

2. Selecteer de werkorder in de lijst en klik op **Werkordergroep**.

3. Selecteer in het dialoogvenster **Werkordergroep onderhouden** in het veld **Toevoegen/verwijderen** de optie **Toevoegen**.

4. Selecteer in het veld **Groep** de werkordergroep.

5. Selecteer **OK**.

6. Als u de werkorder die u hebt toegevoegd in een bepaalde volgorde in de werkordergroep wilt plaatsen, selecteert u de groep op de lijstpagina **Alle werkordergroepen** of **Actieve werkordergroepen** en selecteert u **Bewerken**. Klik vervolgens op de pagina **Werkordergroep** op het sneltabblad **Werkorders** en gebruik het veld **Sorteervolgorde** om de sorteervolgorde van de werkorders in de groep aan te passen.

Als u een werkorder uit een werkordergroep wilt verwijderen, herhaalt u deze stappen, maar selecteert u in stap 3 de optie **Verwijderen**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]