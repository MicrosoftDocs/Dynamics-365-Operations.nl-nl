---
title: Rekeningstructuren maken
description: Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "356387"
---
# <a name="create-account-structures"></a>Rekeningstructuren maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur. De stappen gebruiken het demobedrijf USMF.

1. Ga naar Grootboek > Rekeningschema > Structuren > Rekeningstructuren configureren.
2. Klik op Nieuw om het verwijderdialoogvenster te openen.
3. Typ in het veld Rekeningstructuur een naam om het doel van de rekeningstructuur te beschrijven.
4. Typ in het veld Beschrijving een beschrijving om het doel van de rekeningstructuur op te geven.
5. Klik op Maken.
6. Klik op Segment toevoegen.
7. Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.
8. Klik op Segment toevoegen.
9. Klik op Segment toevoegen.
10. Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.
11. Klik op Segment toevoegen.
12. Klik op Segment toevoegen.
13. Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.
14. Klik op Segment toevoegen.
15. Selecteer in het raster het segment om de toegestane waarden te bewerken.
    * Klik bijvoorbeeld in Hoofdrekening.  
16. Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.
17. Typ een waarde in het veld Waarde.
    * Bijvoorbeeld 600000.  
18. Typ een waarde in het veld Tot.
    * Bijvoorbeeld 699999.  
19. Klik op Toepassen.
20. Selecteer in het raster het segment om de toegestane waarden te bewerken.
    * Bijvoorbeeld Afdeling.  
21. Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.
22. Typ een waarde in het veld Waarde.
    * Bijvoorbeeld 022.  
23. Typ een waarde in het veld Tot.
    * Bijvoorbeeld 031.  
24. Klik op Nieuwe criteria toevoegen.
25. Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.
26. Typ een waarde in het veld Waarde.
    * Bijvoorbeeld 033.  
27. Typ een waarde in het veld Tot.
    * Bijvoorbeeld 034.  
28. Klik op Toepassen.
29. Selecteer in het raster het segment om de toegestane waarden te bewerken.
    * Bijvoorbeeld Kostenplaats.  
30. Typ een waarde in het veld CostCenter.
    * Bijvoorbeeld 007..021.  
31. Klik op Toevoegen.
32. Typ een waarde in het veld MainAccount.
    * Bijvoorbeeld 600000..699999  
33. Selecteer in het raster het segment om de toegestane waarden te bewerken.
    * Bijvoorbeeld Afdeling.  
34. Typ een waarde in het veld Afdeling.
    * Bijvoorbeeld 032.  
35. Typ een waarde in het veld CostCenter.
    * Bijvoorbeeld 086.  
36. Klik op Valideren.
37. Klik op Activeren.
38. Klik op Activeren.

