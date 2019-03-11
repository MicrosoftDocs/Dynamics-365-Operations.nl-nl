---
title: Leveranciers goedkeuren voor specifieke aanschaffingscategorieën
description: Wanneer een opdracht tot inkoop is gemaakt, kan er een vereiste zijn om een goedgekeurde leverancier of voorkeursleverancier te selecteren, afhankelijk van hoe het aanschaffingsbeleid is ingesteld.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "308386"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Leveranciers goedkeuren voor specifieke aanschaffingscategorieën

[!include [task guide banner](../../includes/task-guide-banner.md)]

Wanneer een opdracht tot inkoop is gemaakt, kan er een vereiste zijn om een goedgekeurde leverancier of voorkeursleverancier te selecteren, afhankelijk van hoe het aanschaffingsbeleid is ingesteld. Deze procedure laat zien hoe u kunt opgeven dat een leverancier is goedgekeurd of een voorkeursleverancier is voor een specifieke aanschaffingscategorie. Deze taak wordt meestal uitgevoerd door een inkoopmedewerker. U kunt deze procedure gebruiken in het demobedrijf USMF.

1. Ga naar Inkoop en sourcing > Leveranciers > Alle leveranciers.
2. Selecteer de leverancier die u als goedgekeurde leverancier of voorkeursleverancier voor een categorie wilt instellen.
3. Klik in het actievenster op Algemeen.
4. Klik op Categorieën.
5. Klik op Categorie toevoegen.
6. Selecteer in het veld Categorie de optie OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).
7. Selecteer 'Voorkeur' in het veld Categoriestatus leverancier.
    * Het is mogelijk om meer dan één voorkeursleverancier voor een categorie op te geven.  
8. Klik op Opslaan.
9. Ga naar Inkoop en sourcing > Inkoopcategorieën.
10. Selecteer 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES' in de structuur.
11. Vouw de sectie Leveranciers uit.
    * Controleer of de leverancier die u hebt geselecteerd als voorkeursleverancier voor kantoor- en bureau-accessoires staat vermeld. Als u deze procedure als taakhandleiding uitvoert, moet u mogelijk op de knop Ontgrendelen klikken om omlaag naar de lijst met leveranciers te kunnen bladeren.  Het is ook mogelijk om voorkeursleveranciers en goedgekeurde leveranciers toe te voegen op deze pagina.  
12. Vouw 'OFFICE AND DESK ACCESSORIES' uit in de structuur.
13. Selecteer 'Scharen' in de structuur.
14. Selecteer Nee in het veld Leveranciers opnemen uit bovenliggende categorie:.
15. Selecteer Ja in het veld Leveranciers opnemen uit bovenliggende categorie:.

