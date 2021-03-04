---
title: Leveranciers goedkeuren voor specifieke aanschaffingscategorieën
description: In dit onderwerp wordt uitgelegd hoe u leveranciers voor specifieke inkoopcategorieën kunt goedkeuren in Dynamics 365 Supply Chain Management.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425388"
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