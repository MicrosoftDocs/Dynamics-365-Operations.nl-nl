--- 
title: Een productnummer voor vooraf gedefinieerde productvarianten maken
description: In deze taakbegeleiding wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.
author: BibiSp
manager: AnnBe
ms.date: 11/03/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c423aab341ddad9383c4c95b9dbb63c9875c99ef
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Een productnummer voor vooraf gedefinieerde productvarianten maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

In deze taakbegeleiding wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. De nieuwe productnummernomenclatuur wordt toegewezen aan de productdimensiegroep Kleur en grootte. Deze taak wordt meestal uitgevoerd door een productontwerper.


## <a name="create-a-product-number-nomenclature"></a>Een productvariantnummer-nomenclatuur maken
1. Klik op Definitie van productvariantmodel.
2. Klik op Productnomenclatuur.
3. Klik op Nieuw.
4. Typ in het veld Naam een naam voor de nomenclatuur waaraan u de productdimensiegroep van het doel kunt herkennen, bijvoorbeeld Kleur en grootte.
5. Typ een waarde in het veld Omschrijving.
6. Klik op Toevoegen.
7. Klik op Nummer van basismaster.
8. Klik op Toevoegen.
9. Klik op Tekstconstante.
10. Typ een waarde in het veld Tekst.
11. Klik op Toevoegen.
12. Klik op Kleur.
13. Klik op Toevoegen.
14. Klik op Tekstconstante.
15. Typ een waarde in het veld Tekst.
16. Klik op Toevoegen.
17. Klik op Grootte.
18. Sluit de pagina.

## <a name="assign-the-nomenclature-to-a-product-master"></a>De nomenclatuur toewijzen aan een productmodel
1. Klik op Productdimensiegroepen.
2. Selecteer de productdimensiegroep SizeCol.
3. Klik op Bewerken.
4. Selecteer Ja in het veld Nomenclatuur gebruiken.
5. Typ of selecteer een waarde in het veld Productvariantnummer-nomenclatuur.
6. Sluit de pagina.


