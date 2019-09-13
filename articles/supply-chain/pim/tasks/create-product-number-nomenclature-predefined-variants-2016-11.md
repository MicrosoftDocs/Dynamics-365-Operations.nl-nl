---
title: Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten
description: In dit onderwerp wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cf0efeac2851e6ead6fc5e15a016370dfa620bc
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914902"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. De nieuwe productnummernomenclatuur wordt toegewezen aan de productdimensiegroep Kleur en grootte. Deze taak wordt meestal uitgevoerd door een productontwerper.


## <a name="create-a-product-number-nomenclature"></a>Een productvariantnummer-nomenclatuur maken
1. Selecteer **Definitie van productvariantmodel**.
2. Selecteer **Nomenclatuur voor productnummers**.
3. Selecteer **Nieuw**.
4. Typ in het veld **Naam** een naam voor de nomenclatuur waaraan u de productdimensiegroep van het doel kunt herkennen, bijvoorbeeld `ColorSize`.
5. Typ een waarde in het veld **Beschrijving**.
6. Selecteer **Toevoegen**.
7. Selecteer **Nummer van basismaster**.
8. Selecteer **Toevoegen**.
9. Selecteer **Tekstconstante**.
10. Typ een waarde in het veld **Tekst**.
11. Selecteer **Toevoegen**.
12. Selecteer **Kleur**.
13. Selecteer **Toevoegen**.
14. Selecteer **Tekstconstante**.
15. Typ een waarde in het veld **Tekst**.
16. Selecteer **Toevoegen**.
17. Selecteer **Grootte**.
18. Sluit de pagina.

## <a name="assign-the-nomenclature-to-a-product-master"></a>De nomenclatuur toewijzen aan een productmodel
1. Selecteer **Productdimensiegroepen**.
2. Selecteer de **productdimensiegroep SizeCol**.
3. Selecteer **Bewerken**.
4. Selecteer **Ja** in het veld **Nomenclatuur gebruiken**.
5. Typ of selecteer een waarde in het veld **Productvariantnummer-nomenclatuur**.
6. Sluit de pagina.

