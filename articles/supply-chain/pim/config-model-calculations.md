---
title: Berekeningen van productconfiguratiemodel
description: In dit artikel wordt beschreven hoe u berekeningen maakt voor kenmerken in een productconfiguratiemodel
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35057a4fc59732fea24e4d953cafed633a936ec1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878927"
---
# <a name="product-configuration-model-calculations"></a>Berekeningen van productconfiguratiemodel

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u berekeningen maakt voor kenmerken in een productconfiguratiemodel.

## <a name="prerequisites"></a>Vereisten

Berekeningen worden gebruikt in een productconfiguratiemodel om de configuratiewaarden voor een product te berekenen. Voordat u begint met het instellen van berekeningen, moet het bijbehorende productconfiguratiemodel bestaan. Zie [Een productconfiguratiemodel instellen](set-up-maintain-product-configuration-model.md) voor een overzicht van het installatieproces voor configuratiemodellen en de bijbehorende taken.

## <a name="create-a-calculation"></a>Een berekening maken

Een berekening bestaat uit een expressie en een doelkenmerk. Zie [Veelgestelde vragen over berekeningen voor productonfiguratiemodellen](calculate-product-configuration-models.md) voor meer informatie.

Volg deze stappen om een berekening voor een bestaand productmodel te maken.

1. Ga naar **Productgegevensbeheer \> Algemeen \> Productconfiguratiemodellen**.
1. Open een productconfiguratiemodel en selecteer vervolgens **Bewerken**.
1. Selecteer op het sneltabblad **Berekeningen** de optie **Toevoegen** om een berekening toe te voegen en stel vervolgens de onderstaande velden in:

    - **Naam**: voer een naam in voor de berekening.
    - **Beschrijving**: voer een beschrijving van de berekening in.
    - **Doelkenmerk**: selecteer het kenmerk waarvoor u de berekening maakt.

1. Selecteer **Expressie bewerken**.
1. Voeg in het dialoogvenster **Een berekening invoeren** de vereiste kenmerken, operatoren en waarden toe aan de expressie. Zie [Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen](expression-constraints-table-constraints-product-configuration-models.md) voor meer informatie over hoe u kunt werken met deze elementen.
1. Wanneer uw expressie gereed is, selecteert u **OK**.

## <a name="calculation-examples"></a>Voorbeelden van berekening

In deze sectie vindt u enkele voorbeelden die laten zien hoe berekeningen werken.

### <a name="example-1"></a>Voorbeeld 1

Het doelkenmerk s Booleaans en de berekening gebruikt de volgende voorwaardelijke expressie:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Deze expressie retourneert een waarde van *True* naar het doelkenmerk als `decimalAttribute2` groter is dan of gelijk is aan `decimalAttribute1`. Anders wordt de waarde *False* geretourneerd.

### <a name="example-2"></a>Voorbeeld 2

In dit voorbeeld wordt het tekstkenmerk `textFixedList` gebruikt als doelkenmerk. Dit kenmerk bevat de volgende vaste lijst.

| Waarde | Oplossingswaarde |
|---|---|
| V | 1a |
| B | 2b |
| C | 2c |

In de volgende schermopname ziet u hoe de instellingen voor dit kenmerk er mogelijk uitzien in uw systeem.

![Instellingen voor kenmerktypen, bijvoorbeeld 2.](media/model-calculations-example2.png "Instellingen voor kenmerktypen, bijvoorbeeld 2")

Het kenmerk wordt gebruikt in de volgende voorwaardelijke instructie:

`If[integerAttribute < 150, 0, 2]`

Als `integerAttribute` kleiner is dan 150, retourneert deze instructie de tekstwaarde van de eerste record in de vaste lijst, *A*. Anders retourneert het de tekstwaarde van de derde record in de vaste lijst, *C*.

> [!NOTE]
> De vaste lijst is gelijk aan een op nul gebaseerde opsomming (enum) en de waarden ervan worden geopend met de juiste geheel getalwaarde. Daarom wordt de eerste vaste lijstwaarde (*A*) gekoppeld aan *0*, wordt de tweede waarde (*B*) gekoppeld aan *1* en wordt de derde waarde (*C*) gekoppeld aan *2*.

### <a name="example-3"></a>Voorbeeld 3

In dit voorbeeld wordt het doelkenmerk `textFixedList` uit het vorige voorbeeld gebruikt. Het maakt ook gebruik van een ander tekstkenmerk, `textAttribute`, dat de volgende vaste lijst bevat.

| Waarde | Oplossingswaarde |
|---|---|
| AA | 1aa |
| BB | 2bb |

In de volgende schermopname ziet u hoe de instellingen voor dit kenmerk er mogelijk uitzien in uw systeem.

![Instellingen voor kenmerktypen, bijvoorbeeld 3.](media/model-calculations-example3.png "Instellingen voor kenmerktypen, bijvoorbeeld 3")

De waarde voor het kenmerk `textFixedList` wordt berekend met behulp van de volgende voorwaardelijke instructie:

`If[textAttribute == "1aa", 0, 2]`

Als de waarde `textAttribute` een oplosserwaarde heeft die gelijk is aan *1aa*, retourneert deze expressie de tekstwaarde van de eerste record in de vaste lijst voor `textFixedList`, *A*. Anders retourneert het de tekstwaarde van de derde record in de vaste lijst voor `textFixedList`, *C*.

> [!NOTE]
> - De voorwaardelijke instructie moet de oplosserwaarde van het kenmerk gebruiken.
> - Alleen tekstkenmerken met een vaste lijst kunnen worden gebruikt in berekeningen.

## <a name="see-also"></a>Zie ook

- [Berekeningen voor productconfiguratiemodellen: veelgestelde vragen](calculate-product-configuration-models.md)
- [Een expressiebeperking toevoegen aan een productconfiguratiemodel](tasks/add-expression-constraint-product-configuration-model.md)
- [Overzicht productconfiguratiemodellen](product-configuration-models.md)
