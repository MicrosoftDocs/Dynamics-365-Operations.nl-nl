---
title: Een inkoopcatalogus maken
description: In dit onderwerp wordt uitgelegd hoe u een aanschaffingscatalogus maakt.
author: kamaybac
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59117df519b7aa525713d3acd70195cc42614b9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812393"
---
# <a name="create-a-procurement-catalog"></a>Een inkoopcatalogus maken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een aanschaffingscatalogus maakt. Deze taak wordt gewoonlijk uitgevoerd door een inkoopmedewerker. U komt ook te weten hoe werknemers de catalogus kunnen gebruiken wanneer zij een bestelopdracht maken. Voordat u een catalogus kunt maken, moet er een hiërarchie van aanschaffingscategorieën in uw systeem worden ingesteld. De hiërarchie wordt overgenomen door de nieuwe catalogus, samen met alle producten in de hiërarchie. U kunt deze handleiding in het demobedrijf USMF gebruiken waar de hiërarchie van aanschaffingscategorieën beschikbaar is, evenals de voorbeelden die zijn gebruikt in de procedurestappen.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Controleren of er een hiërarchie van aanschaffingscategorieën bestaat
1. Ga naar het **Navigatievenster > Modules > Inkoopbeheer > Aanschaffingscategorieën**. In het USMF-demobedrijf is een hiërarchie van aanschaffingscategorieën beschikbaar en er zijn producten toegevoegd aan de categorie **Kantoormachines/Computers**. Als u deze procedure uitvoert als taakbegeleiding, moet u de taakbegeleiding ontgrendelen als u door de categorie wilt bladeren. Als er geen hiërarchie beschikbaar was, zou u deze maken door op **Nieuw** te klikken. Dit kan slechts één keer worden gedaan.  
2. Sluit de pagina.

## <a name="create-a-catalog"></a>Een catalogus maken
1. Ga naar het **Navigatievenster > Modules > Inkoopbeheer > Catalogi > Aanschaffingscategorieën**.
2. Selecteer **Nieuwe aanschaffingscatalogus** om het uitklapvenster te openen.
3. Typ een waarde in het veld **Naam**.
4. Selecteer **OK**.
5. Vouw in de structuur **CORP-AANSCHAFFINGSCATEGORIEËN** uit.
6. Vouw in de structuur **KANTOORMACHINES** uit.
7. Selecteer in de structuur **Computers**.

  - De producten uit de aanschaffingscategorie worden weergegeven in de lijst. Als u een product aan de categorie wilt toevoegen, moet u dit doen op de pagina **Hiërarchie van aanschaffingscategorieën** of op de pagina **Artikelgegevens**.  
  - Het bijwerktype **Standaard** bepaalt of nieuwe producten die aan de hiërarchie van aanschaffingscategorieën zijn toegevoegd, direct zichtbaar zijn in de catalogus. Als het bijwerktype is ingesteld op **Dynamisch**, zijn wijzigingen direct zichtbaar. Als het bijwerktype **Statisch** is, zijn nieuwe producten alleen zichtbaar voor mensen die de catalogus gebruiken nadat de catalogus opnieuw is uitgegeven. De actie **Publiceren** is beschikbaar in het actievenster bovenaan de pagina. Als producten worden verwijderd uit de hiërarchie van aanschaffingscategorieën, is de wijziging direct zichtbaar, ongeacht de waarde in het bijwerktypeveld **Standaard**.  

8. Selecteer in het actievenster de optie **Categorienavigatie** en controleer of **Inschakelen** is geselecteerd.
9. Selecteer **Catalogus activeren**.
10. Sluit de pagina.

## <a name="make-the-catalog-visible"></a>De catalogus zichtbaar maken
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Instellen > Beleid > Inkoopbeleid**.
2. Selecteer **Aanschaffingsbeleid-USMF**. U moet het aanschafbeleid selecteren voor de rechtspersoon waarvoor de medewerker die met uw gebruikersprofiel is verbonden producten mag bestellen. In de USMF-demogegevens is de gebruiker met beheerdersrechten gekoppeld aan de medewerker **Julia Funderburk** en zij bestelt standaard producten in USMF.  
3. Selecteer de catalogus die u zojuist hebt gemaakt.
4. Selecteer **OK**.

## <a name="use-the-catalog"></a>De catalogus gebruiken
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Opdrachten tot inkoop > Alle opdrachten tot inkoop**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Naam**.
4. Selecteer **OK**.
5. Selecteer **Producten toevoegen**.
6. Zoek en selecteer de gewenste record in de lijst. U kunt de categoriehiërarchie aan de linkerkant of het filter boven aan de lijst gebruiken om de producten te filteren.  
7. Selecteer **Toevoegen aan regels**.
8. Selecteer **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]