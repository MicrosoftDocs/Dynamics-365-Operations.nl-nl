--- 
title: "Een hiërarchie van aanschaffingscategorieën instellen"
description: "Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: nl-nl
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Een hiërarchie van aanschaffingscategorieën instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt. Deze taken worden meestal uitgevoerd door een inkoopmanager. Voordat u deze procedure kunt starten, moet er een categoriehiërarchie van het type Inkoop zijn. Als u een demobedrijf gebruikt, kunt u deze procedure in het bedrijf USMF uitvoeren.


## <a name="add-a-new-procurement-category"></a>Een nieuwe inkoopcategorie toevoegen
1. Ga naar Inkoop en sourcing > Inkoopcategorieën.
2. Klik op Categoriehiërarchie bewerken.
    * De huidige hiërarchie van aanschaffingscategorieën wordt weergegeven aan de linkerkant van de pagina. U gaat de hiërarchie wijzigen.  
3. Klik op Nieuw categorieknooppunt.
    * Het systeem selecteert standaard het bovenste knooppunt. Als u deze procedure als taakbegeleiding uitvoert, kunt u op de knop Ontgrendelen klikken en een ander bovenliggend knooppunt selecteren om uw nieuw knooppunt in te plaatsen. Zodra dat is gedaan, vergrendelt u de taakbegeleiding opnieuw en klikt u op het categorieknooppunt Nieuw.  
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Omschrijving.
6. Typ een waarde in het veld Beschrijvende naam.
    * De beschrijvende naam is optioneel. Deze wordt in categoriezoekopdrachten met de categorienaam weergegeven.  
7. Klik op Opslaan.

## <a name="add-products-to-your-new-procurement-category"></a>Producten aan uw nieuwe aanschaffingscategorie toevoegen
1. Ga naar Inkoop en sourcing > Inkoopcategorieën.
    * Selecteer het knooppunt dat u zojuist hebt toegevoegd. Als u de procedure als taakbegeleiding uitvoert, moet u de taakbegeleiding wellicht ontgrendelen om het knooppunt te selecteren.  
2. Schakel de uitbreiding van de sectie Producten om.
3. Klik op Toevoegen om producten te koppelen aan de aanschaffingscategorie.
4. Selecteer het product dat u wilt toevoegen aan de aanschaffingscategorie.
5. Klik op de pijl om het product te selecteren.
6. Selecteer een ander product dat u wilt toevoegen aan de aanschaffingscategorie.
7. Klik op de pijl om het product te selecteren.
8. Klik op OK.

## <a name="add-approved-and-preferred-vendors"></a>Goedgekeurde en voorkeursleveranciers toevoegen
1. Schakel de uitbreiding van de sectie Leveranciers om.
2. Klik op Toevoegen.
    * U kunt nu een leverancier aan een aanschaffingscategorie toevoegen en opgeven of een leverancier de voorkeur heeft of alleen is goedgekeurd voor de categorie. Wanneer u een leverancier uit een categorie verwijdert, worden de historische transacties met de leverancier in de categorie niet verwijderd.   
3. Zoek de leverancier die u wilt toevoegen aan de categorie.
4. Klik op de pijl om de leverancier te selecteren.
5. Klik op OK.
6. Selecteer op de leveranciersrij die u wilt wijzigen.
7. Selecteer een optie in het veld Leveranciersstatus.
    * De instelling van de leverancierselectie in de categoriebeleidsregel bepaalt of favoriete, goedgekeurde of alle leveranciers beschikbaar zijn voor opdrachten tot inkoop.   

## <a name="add-additional-information-to-the-category"></a>Extra informatie aan de categorie toevoegen
1. Schakel de uitbreiding van de sectie Groepen evaluatiecriteria voor leveranciers om.
    * Op dit tabblad kunt u definiëren op basis van welke criteria de leveranciers in de aanschaffingscategorie moeten worden beoordeeld. Om dit te doen moet u klikken op Toevoegen en vervolgens een leverancierevaluatiegroep selecteren die de gewenste criteria bevat.  
2. Schakel de sectie Vragenlijsten om.
    * Met dit tabblad kunt u vragenlijsten toevoegen die op de bestelaanvraag worden weergegeven, zolang u het activiteittype instelt op 'Bestelaanvraag'. De aanvrager moet vervolgens een vragenlijst invullen voordat hij of zij een aanvraag voor het specifieke producten of producten in de aanschaffingscategorie kan indienen.  
3. Schakel de uitbreiding van de sectie Btw-groepen voor artikel om.
4. Klik in het veld Btw-groep voor artikel: op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Een btw-groep selecteren.
6. Schakel de uitbreiding van de sectie Categoriepagina om.
    * Categoriepagina's worden gemaakt op de pagina Categoriehiërarchie. Ze bevatten informatie over de aanschaffingscategorie, zoals informatie over het type producten in een categorie, afbeeldingen van producten in een categorie of aankondigingen, zoals de verkoopkortingen die beschikbaar zijn in een categorie. De informatie op een categoriepagina wordt weergegeven in bestelaanvragen.  
7. Sluit de pagina.


