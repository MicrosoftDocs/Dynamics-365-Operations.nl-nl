---
title: Beleid instellen voor categoriehiërarchieën voor aanschaffing
description: Gebruik deze procedure voor het instellen van regels voor het bestellen van producten in een categorie.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d113181b5c78c0f35292b5f14cedd12bacdc7364
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207526"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Beleid instellen voor categoriehiërarchieën voor aanschaffing

[!include [banner](../../includes/banner.md)]

Gebruik deze procedure voor het instellen van regels voor het bestellen van producten in een categorie. De regels worden gedefinieerd voor een specifiek inkoopbeleid. De regel voor categorietoegang bepaalt tot welke aanschaffingscategorieën werknemers toegang hebben bij het maken van een inkoopopdracht. Wanneer een inkoopopdracht wordt gemaakt, worden het inkoopbeleid en de regel voor categorietoegang die moeten worden toegepast bepaald door de rechtspersoon en de operationele eenheid waartoe de werknemer behoort. U kunt deze procedure gebruiken in het demobedrijf USMF. Deze taak wordt meestal uitgevoerd door een inkoopmanager.


## <a name="find-the-procurement-policy"></a>Het inkoopbeleid zoeken
1. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Instellen > Beleid > Inkoopbeleid**.
2. Klik op de koppeling in het beleid Aanschaffingsbeleid USMF. Dit is het beleid waaraan u een regel wilt toevoegen. Dit moet een actief beleid zijn.  

## <a name="create-a-category-access-rule"></a>Een categorietoegangsregel maken
1. Vouw het sneltabblad **Beleidsregels** uit.
2. Selecteer in de lijst **Beleidsregeltype** de **Toegangsbeleidsregel voor categorie**. Als de knop **Beleidsregel maken** grijs wordt weergegeven, komt dat doordat er al een actieve toegangsbeleidsregel voor de categorie is. Controleer de velden **Ingangsdatum** en **Vervaldatum** om na te gaan welke het zijn. Selecteer ze en klik op **Beleidsregel buiten gebruik stellen**. Als de knop **Beleidsregel maken** beschikbaar is, hoeft u niets te doen.  
3. Klik op **Beleidsregel maken**.
4. Voer in het veld **Ingangsdatum** een datum en tijd in. De tijd mag niet overlappen met een andere regel die al actief is.  
5. Selecteer een categorie waarop de regel van toepassing is. Maak een notitie van deze categorie. Deze informatie hebt u later nodig. Wanneer u een categorie selecteert, worden alle bovenliggende categorieën eveneens toegevoegd aan de lijst Geselecteerde categorieën. Als u wilt dat de regel wordt toegepast op alle subcategorieën van de geselecteerde categorie, schakelt u het selectievakje **Subcategorieën opnemen** in.
6. Klik op de pijl-rechts als u deze wilt toevoegen aan de lijst **Geselecteerde categorieën**.  
4. Klik op **OK**. Als u de optie **Bovenliggende regel opnemen** instelt op Ja, wordt de beleidsregel die u voor een bovenliggende categorie definieert, ook toegewezen aan de onderliggende categorieën als er geen beleidsregel is gedefinieerd voor de onderliggende categorieën.

## <a name="create-a-category-policy-rule"></a>Een categoriebeleidsregel maken.
1. Selecteer in de lijst **Beleidsregeltype** de **Beleidsregel voor categorie**. Als de knop **Beleidsregel maken** grijs wordt weergegeven, selecteert u de actieve beleidsregel en klikt u op **Beleidsregel buiten gebruik stellen**.  
2. Klik op **Beleidsregel maken**.
3. Voer in het veld **Ingangsdatum** een datum en tijd in.
4. Klik op **Toevoegen**.
5. Selecteer in het veld **Categorie** dezelfde categorie als die u voor de **Toegangsregel voor categorie** hebt gebruikt.
6. Selecteer een optie in het veld **Leveranciersselectie**. Selecteer een regel om te bepalen welk type leveranciers kan worden geselecteerd voor de categorie bij het maken van bestelopdrachten.  
7. Klik op **Sluiten**. De beleidsregels die u hebt gedefinieerd zijn voor bestelopdrachten van het type Verbruik. Als u beleid wilt definiëren voor bestelopdrachten van het type Aanvulling, maakt u een regel voor het type beleidsregel genaamd Toegangsbeleidsregel voor aanvullingscategorie.  

