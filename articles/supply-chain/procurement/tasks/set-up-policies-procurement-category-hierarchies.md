---
title: Beleid instellen voor categoriehiërarchieën voor aanschaffing
description: Gebruik deze procedure voor het instellen van regels voor het bestellen van producten in een categorie.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569909"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Beleid instellen voor categoriehiërarchieën voor aanschaffing

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gebruik deze procedure voor het instellen van regels voor het bestellen van producten in een categorie. De regels worden gedefinieerd voor een specifiek inkoopbeleid. De regel voor categorietoegang bepaalt tot welke aanschaffingscategorieën werknemers toegang hebben bij het maken van een inkoopopdracht. Wanneer een inkoopopdracht wordt gemaakt, worden het inkoopbeleid en de regel voor categorietoegang die moeten worden toegepast bepaald door de rechtspersoon en de operationele eenheid waartoe de werknemer behoort. U kunt deze procedure gebruiken in het demobedrijf USMF. Deze taak wordt meestal uitgevoerd door een inkoopmanager.


## <a name="find-the-procurement-policy"></a>Het inkoopbeleid zoeken
1. Ga naar Inkoopbeheer > Instellingen > Beleid > Inkoopbeleid.
2. Klik op de koppeling in het beleid Aanschaffingsbeleid USMF.
    * Dit is het beleid waaraan u een regel wilt toevoegen. Dit moet een actief beleid zijn.  

## <a name="create-a-category-access-rule"></a>Een categorietoegangsregel maken
1. Selecteer de beleidsregel voor categorietoegang.
    * Als de knop Beleidsregel maken grijs wordt weergegeven, komt dat doordat er al een actieve beleidsregel voor categorietoegang is. Schakel de velden Ingangsdatum en Vervaldatum in om te bepalen welke dat is, selecteer deze vervolgens en klik op Beleidsregel deactiveren. Als de knop Beleidsregel maken beschikbaar is, hoeft u niets te doen.  
2. Klik op Beleidsregel maken.
3. Typ in het veld Begindatum de datum en een tijd.
    * De tijd mag niet overlappen met een andere regel die al actief is.  
    * Selecteer een categorie waarop de regel van toepassing is. Maak een notitie van welke categorie dit is. Deze informatie hebt u later nodig. Wanneer u een categorie selecteert, worden alle bovenliggende categorieën eveneens toegevoegd aan de lijst Geselecteerde categorieën.  
    * Als u wilt dat de regel geldt voor alle subcategorieën van de geselecteerde categorie, schakelt u het selectievakje Subcategorieën opnemen in.  
4. Klik op Toevoegen.
    * Als u de optie Bovenliggende regel opnemen wilt instellen op Ja, wordt de beleidsregel die u definieert voor een bovenliggende categorie ook toegewezen aan de onderliggende categorieën als er geen beleidsregel is gedefinieerd voor de onderliggende categorieën.  
5. Klik op OK.

## <a name="create-a-category-policy-rule"></a>Een categoriebeleidsregel maken.
1. Beleidsregel voor categorietoegang selecteren
    * Als de knop Beleidsregel grijs wordt weergegeven, selecteert u de actieve beleidsregel en klikt u vervolgens op Beleidsregel deactiveren.  
2. Klik op Beleidsregel maken.
3. Typ in het veld Begindatum de datum en een tijd.
4. Klik op Toevoegen.
5. Selecteer dezelfde categorie als u voor de toegangsregel voor categorie hebt gebruikt.
6. Selecteer een optie in het veld Leverancier selecteren.
    * Selecteer een regel om te bepalen welk type leveranciers kan worden geselecteerd voor de categorie bij het maken van bestelopdrachten.  
7. Klik op Sluiten.
    * De beleidsregels die u hebt gedefinieerd zijn voor bestelopdrachten van het type Verbruik. Als u beleid wilt definiëren voor bestelopdrachten van het type Aanvulling, maakt u een regel voor het type beleidsregel genaamd "Toegangsbeleidsregel voor aanvullingscategorie".  

