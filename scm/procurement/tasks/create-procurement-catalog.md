--- 
title: Een inkoopcatalogus maken
description: Deze handleiding laat zien hoe u een aanschaffingscatalogus maakt.
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 19d053a0bdbdcc764b3361fe5a326e8c68cdc682
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-procurement-catalog"></a>Een inkoopcatalogus maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze handleiding laat zien hoe u een aanschaffingscatalogus maakt. Deze taak wordt gewoonlijk uitgevoerd door een inkoopmedewerker. U komt ook te weten hoe werknemers de catalogus kunnen gebruiken wanneer zij een bestelopdracht maken. Voordat u een catalogus kunt maken, moet er een hiërarchie van aanschaffingscategorieën in uw systeem worden ingesteld. De hiërarchie wordt overgenomen door de nieuwe catalogus, samen met alle producten in de hiërarchie. U kunt deze handleiding in het demobedrijf USMF gebruiken waar de hiërarchie van aanschaffingscategorieën beschikbaar is, evenals de voorbeelden die zijn gebruikt in de procedurestappen.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Controleren of er een hiërarchie van aanschaffingscategorieën bestaat
1. Ga naar Inkoop en sourcing > Inkoopcategorieën.
    * In het USMF-demobedrijf is een hiërarchie van aanschaffingscategorieën beschikbaar en er zijn producten toegevoegd aan de categorie Kantoormachines/Computers. Als u deze procedure uitvoert als taakbegeleiding, moet u de taakbegeleiding ontgrendelen als u door de categorie wilt bladeren. Als er geen hiërarchie beschikbaar was, zou u deze maken door op Nieuw te klikken. Dit kan slechts één keer worden gedaan.  
2. Sluit de pagina.

## <a name="create-a-catalog"></a>Een catalogus maken
1. Ga naar Inkoopbeheer > Catalogi > Inkoopcatalogi.
2. Klik op Nieuwe aanschaffingscatalogus om het dialoogvenster voor beëindigen te openen.
3. Typ een waarde in het veld Naam.
4. Klik op OK.
5. Vouw in de structuur 'CORP-AANSCHAFFINGSCATEGORIEËN' uit.
6. Vouw 'KANTOORMACHINES' uit in de structuur.
7. Selecteer 'Computers' in de structuur.
    * De producten uit de aanschaffingscategorie worden weergegeven in de lijst. Als u een product aan de categorie wilt toevoegen, moet u dit doen op de pagina Hiërarchie van inkoopcategorieën of op de pagina Artikelgegevens.  
    * Het standaard bijwerktype bepaalt of nieuwe producten die aan de hiërarchie van aanschaffingscategorieën zijn toegevoegd direct zichtbaar zijn in de catalogus. Als het bijwerktype is ingesteld op Dynamisch, zijn wijzigingen direct zichtbaar. Als het bijwerktype Statisch is, zijn nieuwe producten alleen zichtbaar voor mensen die de catalogus gebruiken nadat de catalogus opnieuw is uitgegeven. De actie Publiceren is beschikbaar in het actievenster boven aan de pagina. Als producten worden verwijderd uit de hiërarchie van aanschaffingscategorieën, is de wijziging direct zichtbaar, ongeacht de waarde in het Veld het Standaard bijwerktype.  
8. Zoek en selecteer de gewenste record in de lijst.
9. Klik op Verbergen.
10. Klik in het actievenster op Categorienavigatie.
11. Klik op Uitschakelen.
12. Klik in het actievenster op Categorienavigatie.
13. Klik op Inschakelen.
14. Klik op Catalogus activeren.
15. Sluit de pagina.

## <a name="make-the-catalog-visible"></a>De catalogus zichtbaar maken
1. Ga naar Inkoopbeheer > Instellingen > Beleid > Inkoopbeleid.
2. Selecteer Aanschaffingsbeleid USMF.
    * U moet het aanschafbeleid selecteren voor de rechtspersoon waarvoor de medewerker die met uw gebruikersprofiel is verbonden producten mag bestellen. In de USMF-demogegevens, is de gebruiker Beheerder gekoppeld aan de medewerker genaamd Julia Funderburk en zij bestelt standaard producten in USMF.  
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Selecteer de catalogus die u zojuist hebt gemaakt.
5. Klik op OK.
6. Sluit de pagina.
7. Sluit de pagina.

## <a name="use-the-catalog"></a>De catalogus gebruiken
1. Ga naar Inkoopbeheer > Opdrachten tot inkoop > Alle opdrachten tot inkoop.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Klik op OK.
5. Klik op Producten toevoegen.
6. Zoek en selecteer de gewenste record in de lijst.
    * U kunt de categoriehiërarchie aan de linkerkant of het filter boven aan de lijst gebruiken om de producten te filteren.  
7. Klik op Regels toevoegen.
8. Zoek en selecteer de gewenste record in de lijst.
9. Klik op Regels toevoegen.
10. Klik op OK.


