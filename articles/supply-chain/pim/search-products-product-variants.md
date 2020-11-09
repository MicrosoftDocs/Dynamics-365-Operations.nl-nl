---
title: Producten en productvarianten zoeken tijdens orderinvoer
description: Met het veld **Artikelnummer** kunt u zoeken naar producten en productvarianten, wanneer u handmatig een verkoop- of inkooporderregel maakt. Zo kunt u snel productvarianten zoeken wanneer u alleen de configuratietekenreeks of een van de beschikbare productdimensies hebt.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, PurchTablePart, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 532f437bee490743847cf5617579c579f9202b71
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018325"
---
# <a name="search-for-products-and-product-variants-during-order-entry"></a>Producten en productvarianten zoeken tijdens orderinvoer

[!include [banner](../includes/banner.md)]

Met het veld **Artikelnummer** kunt u zoeken naar producten en productvarianten, wanneer u handmatig een verkoop- of inkooporderregel maakt.  Zo kunt u snel productvarianten zoeken wanneer u alleen de configuratietekenreeks of een van de beschikbare productdimensies hebt.

Soms kunt u door de bomen het bos niet meer zien. Dit is vooral het geval als u diverse sterk op elkaar lijkende producten voert en u artikelnummers of productnamen voor zoekopdrachten wilt onthouden om het juiste product op een verkooporder te kunnen zetten. U kunt het veld **Artikelnummer** op een in- of verkooporderregel gebruiken als zoekveld. U kunt een willekeurig deel van een naam, nummer of dimensie van een product invoeren. In een opzoekweergave worden vervolgens alle artikelen getoond die voldoen aan uw zoekterm.

## <a name="how-searchworks"></a>Hoe het zoeken functioneert
Wanneer u zoekt naar producten of productvarianten, moet u weten hoe de zoekfunctie de producten vindt die overeenkomen met de door u ingevoerde tekst. Hieronder worden de belangrijkste regels voor zoeken met goede resultaten aangestipt:

-   Zoekresultaten retourneren alle records die aan de criteria voldoen, ongeacht in welk veld de zoektermen zijn ingevoerd.
-   De zoektekst moet volledig voorkomen in een record om een match op te leveren.
-   Een match komt zelfs voor als de zoektekst in het midden van een tekenreeks in de overeenkomstige record wordt gevonden. De tekst hoeft niet aan het begin van een tekenreeks te staan.
-   De zoektekst wordt beschouwd als een enkele tekenreeks, zelfs als er spaties in voorkomen.

### <a name="examples"></a>Voorbeelden

In de volgende voorbeelden wordt door middel van producten en productvarianten getoond hoe het zoeken in diverse scenario's worden afgehandeld. **Vereiste:**  onder **Verkoop en marketing &gt; Instellingen &gt; Zoeken &gt; Zoekparameters &gt; Zoektype** moet de optie  **Volledige overeenkomst** zijn geselecteerd.

| Producttype     | Productnaam    | Productweergavenummer | artikelnummer | Configuratie |
|------------------|-----------------|------------------------|-------------|---------------|
| Verschillend product | LuidsprekerMidRange | D0001                  | D0001       | N.v.t.            |
| Productvariant  | Actieve luidspreker  | D0010:::zwart:         | D0010       | 000005        |
| Productvariant  | Actieve luidspreker  | D0010:::wit:         | D0010       | Wit         |

Als u in het veld **Artikelnummer** de tekst 'sprek' typt, krijgt u alle bovenstaande producten als resultaat in de opzoekweergave. Als u **Artikelnummer** de tekst 'zwart' typt, krijgt u alleen het tweede product als resultaat, omdat de tekst 'zwart' voorkomt in het productweergavenummer. Deze twee voorbeelden laten zien dat het zoeken niet alleen aan het begin van het veld voorkomt. Een overeenkomst wordt ook gevonden als de zoektekst in het midden van een tekenreeks in de overeenkomstige record wordt aangetroffen.  

Als u '05' typt, vindt u alleen de tweede productvariant, omdat hier in de configuratie de tekst '05' voorkomt. Dit laat zien dat het zoeken gebeurt in alle ingeschakelde velden op de pagina **Zoekcriteria**.  

De zoektekst 'sprek 05' levert geen enkel resultaat op. Dit komt doordat de zoekopdracht zoekt naar de volledige ingevoerde tekst. De zoekactie probeert niet eerst 'sprek' te vinden en vervolgens de resultaten te verfijnen tot degene die '05' bevatten.  

U kunt het aantal zoekresultaten beperken door middel van het veld **Aantal resultaten** op de pagina **Verkoop en marketing &gt; Instellingen &gt; Zoeken &gt; parameters** . Als u dit veld instelt op 0, worden alle zoekresultaten geretourneerd. Als u het bijvoorbeeld instelt op 10, worden maximaal 10 zoekresultaten geretourneerd.

## <a name="configure-the-productsearch"></a>De productzoekfunctie configureren
Voordat u de functie voor het zoeken van producten en productvarianten kunt gebruiken, moet u deze functie configureren volgens de onderstaande stappen. [![Drie stappen voor het configureren van de productzoekopdracht\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Stap 1: Alle relevante identificerende kenmerken en dimensies voor producten en productvarianten toevoegen aan de zoekcriteria.

Voorbeelden van identificerende kenmerken en dimensies voor producten en productvarianten waarop u kunt zoeken, zijn  **Productnaam, Artikelnummer,** **Productweergavenummer, Configuratie, Kleur, Grootte, Stijl, Zoeknaam, enzovoort**.  

Ga naar de pagina **Verkoop en marketing &gt; Instellen &gt; Zoeken &gt; Zoekcriteria**. Op de pagina **Zoekcriteria** kunt u criteria definiëren voor het zoeken naar klanten, prospects en producten. Zorg ervoor dat u de pagina filtert door middel van zoekcriteria voor producten. Schakel hiervoor in het menu van de pagina over naar **Product**.  

Als u het weergegeven productnummer wilt toevoegen aan de zoekcriteria, klikt u op **Nieuw** in het menu van de pagina. Hierdoor wordt een nieuwe record toegevoegd in het raster **Zoekcriteria**. Open de opzoekweergave van de kolom **Veldnaam** en kies **DisplayProductNumber**. Om de configuratie van het product aan de zoekcriteria te voegen, maakt u een nieuwe record in het raster **Zoekcriteria** en kiest u in de kolom **Veldnaam** de waarde **configId**. Maak op dezelfde manier een registratie met de **Veldnamen** **InventColorId** voor de dimensie Kleur, **InventSizeId** voor de dimensie Grootte en **InventStyleId** voor de dimensie Stijl.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Stap 2: De databasetabel vullen die voor het zoeken naar producten wordt gebruikt

Klik op de pagina **Zoekcriteria** op de knop **Zoekgegevens bijwerken**. Let erop dat in het dialoogvenster **Zoekgegevens bijwerken** de waarde in  **Bron** is ingesteld op **Product** en klik vervolgens op **OK**. Het systeem voegt in één tabel alle geselecteerde zoekcriteria samen die zijn opgegeven bij stap 1. Als u een groot aantal producten en productvarianten hebt, kan deze bewerking lang duren. U krijgt hiervoor een waarschuwing. Het wordt aangeraden om het vullen van de zoektable op de batchserver in te plannen op een tijdstip waarop de server niet erg druk is.  

De productzoekfunctie geeft pas correcte resultaten als de tabel is gevuld. Als u geen zoekresultaten krijgt, controleer dan of deze tabel is gevuld.  

De tabel moet alleen worden gevuld als de zoekcriteria worden gewijzigd. Nieuw vrijgegeven producten en varianten worden automatisch aan de tabel toegevoegd. Verwijderde producten en varianten worden automatisch uit de tabel verwijderd.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Stap 3: De opzoekweergave voor producten inschakelen voor verkoop- en inkooporderregels

U kunt deze functionaliteit als volgt inschakelen: ga naar **Verkoop en marketing &gt; Instellen &gt; Zoeken &gt; Zoekparameters** en stel op het tabblad **Algemeen** de optie **Zoekveld inschakelen om producten te zoeken** in op **Ja**.  

Voor invoer van verkooporderregels is het standaardgedrag als volgt: open de pagina  **Product zoeken** wanneer u begint te typen in het veld  **Artikelnummer**. Druk vervolgens op de  **Tab** -toets. De context van de pagina **Product zoeken** wordt tijdens het aanmaken van een orderregel gewijzigd, waardoor de pagina als opdringerig worden ervaren. Als de zoekresultaten liever in een zoekveld krijgt en de context niet wilt verliezen tijdens de orderregelinvoer, kunt u in plaats daarvan de opzoekweergave van de zoekopdracht gebruiken. Als u een product of productvariant zoekt, maar niets selecteert in de opzoekweergave en op de **Tab** -toets drukt, wordt de pagina  **Product zoeken** weergeven.



