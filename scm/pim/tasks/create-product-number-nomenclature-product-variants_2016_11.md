--- 
title: Een productnummer voor geconfigureerde productvarianten maken
description: In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt.
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 8a9bf8241a0dc66f34715513d2d201569b810582
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-number-for-configured-product-variants"></a>Een productnummer voor geconfigureerde productvarianten maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt. In deze procedure ziet u ook hoe u een configuratienomenclatuur samenstelt voor een component van een productconfiguratiemodel. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. De nieuwe productnummernomenclatuur is toegewezen aan het productmodel D0004. Deze taak wordt meestal uitgevoerd door een productontwerper.


## <a name="create-a-product-number-nomenclature"></a>Een productvariantnummer-nomenclatuur maken
1. Klik op Definitie van productvariantmodel.
2. Klik op Productnomenclatuur.
3. Klik op Nieuw.
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Omschrijving.
6. Klik op Toevoegen.
7. Klik op Nummer van basismaster.
8. Klik op Toevoegen.
9. Klik op Tekstconstante.
10. Markeer in de lijst de geselecteerde rij.
11. Typ een waarde in het veld Tekst.
12. Klik op Toevoegen.
13. Klik op Configuratie.
14. Sluit de pagina.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>De productnummernomenclatuur toewijzen aan een productmodel
1. Klik op Basisproducten.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld het veld Productnummer op de waarde 'D'.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op Bewerken.
5. Selecteer Ja in het veld Nomenclatuur gebruiken.
6. Typ of selecteer een waarde in het veld Productvariantnummer-nomenclatuur.
7. Sluit de pagina.
8. Sluit de pagina.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Een nomenclatuur maken voor een productconfiguratiemodelcomponent
1. Klik op Productconfiguratiemodellen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op Bewerken.
5. Selecteer Ja in het veld Configuratienomenclatuur gebruiken.
6. Klik op Toevoegen.
7. Klik op Kenmerkwaarde.
8. Markeer in de lijst de geselecteerde rij.
9. Typ of selecteer een waarde in het veld Kenmerk.
10. Klik op Toevoegen.
11. Klik op Tekstconstante.
12. Markeer in de lijst de geselecteerde rij.
13. Typ een waarde in het veld Tekst.
14. Klik op Toevoegen.
15. Klik op Kenmerkwaarde.
16. Markeer in de lijst de geselecteerde rij.
17. Typ of selecteer een waarde in het veld Kenmerk.
18. Klik op Toevoegen.
19. Klik op Tekstconstante.
20. Markeer in de lijst de geselecteerde rij.
21. Typ een waarde in het veld Tekst.
22. Klik op Toevoegen.
23. Klik op Kenmerkwaarde.
24. Markeer in de lijst de geselecteerde rij.
25. Typ of selecteer een waarde in het veld Kenmerk.
26. Klik op Toevoegen.
27. Klik op Tekstconstante.
28. Markeer in de lijst de geselecteerde rij.
29. Typ een waarde in het veld Tekst.
30. Klik op Toevoegen.
31. Klik op Kenmerkwaarde.
32. Markeer in de lijst de geselecteerde rij.
33. Typ of selecteer een waarde in het veld Kenmerk.
34. Klik op Toevoegen.
35. Klik op Tekstconstante.
36. Markeer in de lijst de geselecteerde rij.
37. Typ een waarde in het veld Tekst.
38. Klik op Toevoegen.
39. Klik op Nummerreekswaarde.
40. Markeer in de lijst de geselecteerde rij.
41. Typ of selecteer een waarde in het veld Nummerreeks.
42. Sluit de pagina.
43. Sluit de pagina.
44. Sluit de pagina.


