---
title: Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten
description: In dit artikel wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77c8eabe1657f7fbfef71747627207dccff3b60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887307"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten

[!include [banner](../../includes/banner.md)]

In dit artikel wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. De nieuwe productnummernomenclatuur wordt toegewezen aan de productdimensiegroep Kleur en grootte. Deze taak wordt meestal uitgevoerd door een productontwerper.


## <a name="create-a-product-number-nomenclature"></a>Een productvariantnummer-nomenclatuur maken

1. Ga naar **Productgegevensbeheer \> Instellingen \> Productnomenclatuur**.
1. Selecteer **Nieuw**.
1. Typ in het veld **Naam** een naam voor de nomenclatuur waaraan u de productdimensiegroep van het doel kunt herkennen, bijvoorbeeld `ColorSize`.
1. Typ een waarde in het veld **Beschrijving**.
1. Selecteer **Toevoegen**.
1. Selecteer **Nummer van basismaster**.
1. Selecteer **Toevoegen**.
1. Selecteer **Tekstconstante**.
1. Typ een waarde in het veld **Tekst**.
1. Selecteer **Toevoegen**.
1. Selecteer **Kleur**.
1. Selecteer **Toevoegen**.
1. Selecteer **Tekstconstante**.
1. Typ een waarde in het veld **Tekst**.
1. Selecteer **Toevoegen**.
1. Selecteer **Grootte**.
1. Sluit de pagina.

## <a name="assign-the-nomenclature-to-a-product-master"></a>De nomenclatuur toewijzen aan een productmodel

1. Selecteer **Productdimensiegroepen**.
2. Selecteer de **productdimensiegroep SizeCol**.
3. Selecteer **Bewerken**.
4. Selecteer **Ja** in het veld **Nomenclatuur gebruiken**.
5. Typ of selecteer een waarde in het veld **Productvariantnummer-nomenclatuur**.
6. Sluit de pagina.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]