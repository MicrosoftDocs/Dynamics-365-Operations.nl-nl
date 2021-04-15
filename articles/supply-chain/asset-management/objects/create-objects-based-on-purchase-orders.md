---
title: Activa maken op basis van inkooporders
description: In dit onderwerp wordt uitgelegd hoe u een lijst met activumartikelen maakt die kunnen worden gebruikt als basis voor het maken van activa voor onderhoudstaken in Activabeheer.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51896f512a00bd41617fd02c2cd364c4e00eb774
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811153"
---
# <a name="create-assets-based-on-purchase-orders"></a>Activa maken op basis van inkooporders

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt uitgelegd hoe u een lijst met activumartikelen maakt die kunnen worden gebruikt als basis voor het maken van activa voor onderhoudstaken in Activabeheer. Op basis van de activumartikelen kunt u een lijst weergeven van de inkooporderregels die voor die artikelen zijn gemaakt. Het doel van deze functionaliteit is om op basis van een inkooporder eenvoudig een activum te maken in Activabeheer.

Eerst stelt u vanuit een inkooporder in **Activumartikelen** de artikelen in die moeten worden gebruikt voor het maken van activa. Nadat u een inkooporderregel hebt gemaakt, maakt u de activa in **Activa in behandeling**. Het is mogelijk om te bepalen in welk stadium van de inkooporder het activum moet worden gemaakt.


## <a name="select-asset-items"></a>Activumtypen selecteren

1. Klik op **Activabeheer** > **Instellen** > **Activa** > **Artikelen**.
2. Klik op **Nieuw** om een nieuwe activumartikel te maken.
3. Selecteer het artikel in het veld **Artikelnummer**. Wanneer u dit veld verlaat, wordt de artikelnaam automatisch ingevoegd in het veld **Productnaam**.
4. Selecteer op het sneltabblad **Algemeen** een activumtype voor het artikel.
5. Selecteer de fabrikant en het model van het activumartikel.
6. Sla het artikel op.


## <a name="create-assets-from-pending-assets"></a>Activa maken van activa in behandeling

1. Klik op **Activabeheer** > **Algemeen** > **Activa** > **Activa in behandeling**.
2. U ziet een bijgewerkte lijst van de inkooporders op basis van de artikelen die zijn geselecteerd in **Activumartikelen**.
3. U kunt de status van inkooporders filteren om te selecteren in welke levenscyclusstatus het activum moet worden gemaakt. U wilt bijvoorbeeld alleen activa maken wanneer een productontvangstbon voor een inkooporder is geboekt.
4. Selecteer de koppeling **Referentienummer** op een inkooporderregel om gedetailleerde informatie over het artikel weer te geven.
5. Als u wilt bewerken welke dimensies worden weergegeven op het sneltabblad **Voorraaddimensies**, klikt u op de knop **Dimensies weergeven** en maakt u uw selecties.
6. Als u een activum wilt maken op basis van een inkooporderregel, schakelt u het selectievakje in de kolom **Markeren** voor die regel in op de lijstpagina en klikt u op **Activa maken**. Er wordt een bericht weergegeven met informatie over de activum-id.
7. Selecteer het activum in de lijst **Alle activa** en klik op **Bewerken** als u meer informatie aan het activum wilt toevoegen.
8. Als u in **Activa in behandeling** een regel wilt verwijderen omdat u geen activum wilt maken, schakelt u het selectievakje in de kolom **Markeren** voor die regel in en klikt u op **Activa in behandeling verwijderen**. Er wordt een bericht weergegeven met informatie over de activum-id. U verwijdert de inkooporder of verkooporder niet, maar alleen de record op basis waarvan u een activum had kunnen maken in **Activabeheer**.

>[!NOTE]
>Alle productdimensies (grootte, kleur, configuratie, enzovoort) worden automatisch overgebracht naar de kenmerken van het activum. Traceringsdimensies (serienummer) worden rechtstreeks in het activum opgeslagen wanneer het activum wordt gemaakt.


## <a name="find-pending-assets"></a>Activa in behandeling zoeken

U kunt de functie **Activa in behandeling tellen** uitvoeren om te controleren op activa in behandeling. Deze functie kan bijvoorbeeld worden gebruikt als u een melding wilt ontvangen telkens wanneer een activum in behandeling gereed is om als een activum te worden gemaakt.

1. Klik op **Activabeheer** > **Periodiek** > **Activa** > **Activa in behandeling tellen**.
2. Klik op **OK** om de taak uit te voeren en de lijst in **Activa in behandeling** bij te werken.
3. U kunt deze taak zo instellen dat deze als een batchtaak wordt uitgevoerd, bijvoorbeeld eenmaal per dag.

**Waarschuwing:** als gegevens op een inkooporder worden gewijzigd *nadat* u een activum hebt gemaakt op basis van het betreffende artikel, worden deze wijzigingen niet doorgevoerd in het activum.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]