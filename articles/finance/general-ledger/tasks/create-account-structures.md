---
title: Rekeningstructuren maken
description: Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8ce37ab642277ff843e6320a880fac40d41acb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235784"
---
# <a name="create-account-structures"></a>Rekeningstructuren maken

[!include [banner](../../includes/banner.md)]

Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur. De stappen gebruiken het demobedrijf USMF.

1. Ga in het navigatievenster naar **Modules > Grootboek > Rekeningschema > Structuren > Regelstructuren configureren**.
2. Klik in het **actievenster** op **Nieuw** om het dialoogvenster voor beëindigen te openen.
3. Typ in het veld **Rekeningstructuur** een naam om het doel van de rekeningstructuur te beschrijven.
4. Typ in het veld **Beschrijving** een beschrijving om het doel van de rekeningstructuur op te geven.
5. Klik op **Maken**.
6. Klik in **Segmenten en toegestane waarden** op **Segment toevoegen**.
7. Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.
8. Klik aan het einde van de lijst op **Segment toevoegen**.
9. Herhaal stap 6 tot en met 9 zo nodig.
10. Selecteer in de sectie **Details van toegestane waarden** het segment om de toegestane waarden te bewerken.
    Klik bijvoorbeeld in het veld **Hoofdrekening**.  
11. Selecteer in het veld **Operator** een optie, zoals 'ligt tussen' en 'bevat'.
12. Typ een waarde in het veld **Waarde**. Bijvoorbeeld 600000.  
13. Typ een waarde in het veld **Tot en met**. Bijvoorbeeld 699999.  
14. Klik in de sectie **Details van toegestane waarden** op **Toepassen**.
15. Herhaal stap 10 tot en met 15 zo nodig.  
16. Klik in de sectie **Details van toegestane waarden** op **Nieuwe criteria toevoegen**.
17. Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.
18. Typ een waarde in het veld **Waarde**. Bijvoorbeeld 033.  
19. Typ een waarde in het veld **Tot en met**. Bijvoorbeeld 034.  
20. Klik op **Toepassen**.
21. Selecteer in het raster het segment om de toegestane waarden te bewerken. Bijvoorbeeld Kostenplaats.  
22. Typ een waarde in het veld **CostCenter**. Bijvoorbeeld 007..021.  
23. Klik in **Segmenten en toegestane waarden** op **Toevoegen**.
24. Typ een waarde in het veld **MainAccount**. Bijvoorbeeld 600000..699999  
25. Selecteer in het raster het segment om de toegestane waarden te bewerken. Bijvoorbeeld Afdeling.  
26. Typ een waarde in het veld Afdeling. Bijvoorbeeld 032.  
27. Typ een waarde in het veld CostCenter. Bijvoorbeeld 086.  
28. Klik in het **actievenster** op **Valideren**.
29. Klik in het **actievenster** op **Activeren**.
30. Klik op **Activeren**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]