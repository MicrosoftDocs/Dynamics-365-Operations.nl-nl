---
title: Leveranciers goedkeuren voor specifieke aanschaffingscategorieën
description: In dit onderwerp wordt uitgelegd hoe u leveranciers voor specifieke inkoopcategorieën kunt goedkeuren in Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 65a42e10edda7b492e86029ca05655d7c0175c23589dc55573c7ac5976e820d3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717209"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Leveranciers goedkeuren voor specifieke aanschaffingscategorieën

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u leveranciers voor specifieke inkoopcategorieën kunt goedkeuren in Dynamics 365 Supply Chain Management. Wanneer een opdracht tot inkoop is gemaakt, kan er een vereiste zijn om een goedgekeurde leverancier of voorkeursleverancier te selecteren, afhankelijk van hoe het aanschaffingsbeleid is ingesteld. Deze procedure laat zien hoe u kunt opgeven dat een leverancier is goedgekeurd of een voorkeursleverancier is voor een specifieke aanschaffingscategorie. Deze taak wordt meestal uitgevoerd door een inkoopmedewerker. U kunt deze procedure gebruiken in het demobedrijf USMF.

1. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**.
2. Selecteer de leverancier die u als goedgekeurde leverancier of voorkeursleverancier voor een categorie wilt instellen.
3. Selecteer **Algemeen** in het actievenster.
4. Selecteer **Categorieën**.
5. Selecteer **Categorie toevoegen**.
6. Selecteer in het veld **Categorie** de optie **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.
7. Selecteer **Voorkeur** in het veld **Categoriestatus leverancier**. Het is mogelijk om meer dan één voorkeursleverancier voor een categorie op te geven.  
8. Selecteer **Opslaan**.
9. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Aanschaffingscategorieën**.
10. Selecteer **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES** in de structuur.
11. Vouw de sectie **Leveranciers** uit. Controleer of de geselecteerde leverancier is vermeld als voorkeursleverancier voor de categorie kantoor- en bureau-accessoires. Als u deze procedure als taakhandleiding uitvoert, moet u mogelijk de knop **Ontgrendelen** selecteren om omlaag naar de lijst met leveranciers te kunnen bladeren.  Het is ook mogelijk om voorkeursleveranciers en goedgekeurde leveranciers toe te voegen op deze pagina.  
12. Klik in de structuur op **OFFICE AND DESK ACCESSORIES** en selecteer **Scharen**.
13. Selecteer **Nee** in het veld **Leveranciers opnemen uit bovenliggende categorie:**.
14. Selecteer **Ja** in het veld **Leveranciers opnemen uit bovenliggende categorie:**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]