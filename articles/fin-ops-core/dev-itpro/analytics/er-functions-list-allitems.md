---
title: De ER-functie ALLITEMS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ALLITEMS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aa226be8bc27817b4369b9e5b24faee8ea52b88
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042223"
---
# <a name="ALLITEMS">De ER-functie ALLITEMS</a>

[!include [banner](../includes/banner.md)]

De functie `ALLITEMS` wordt uitgevoerd als een selectie in het geheugen en geeft als resultaat een nieuwe afgevlakte *recordlijstwaarde* als een lijst met records voor alle artikelen die overeenkomen met het opgegeven pad.

## <a name="syntax"></a>Syntaxis

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumenten

`path`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Het pad moet worden gedefinieerd als een geldig gegevensbronpad van een gegevensbronelement van het gegevenstype *Recordlijst*. Gegevenselementen zoals de padreeks en datum moeten tijdens het ontwerp tot een fout leiden in ER Expression Builder.

We raden u af deze functie te gebruiken voor transactionele gegevensbronnen die een grote hoeveelheid gegevens kunnen bevatten. Overweeg in plaats daarvan de functie [ALLTEMSQUERY](er-functions-list-allitemsquery.md) te gebruiken.

## <a name="example-1"></a>Voorbeeld 1

Als u `SPLIT("abcdef" , 2)` als gegevensbron **DS** invoert, geeft de expressie `COUNT( ALLITEMS (DS))` als resultaat **3**.

## <a name="example-2"></a>Voorbeeld 2

Als u **Leverancier** invoert als de gegevensbron van het gegevenstype van *Recordlijst* die naar de toepassingstabel VendTable verwijst, retourneert de expressie `ALLITEMS (Vend.'<Relations'.ContactPerson)` een afgevlakte lijst met records met de tabelstructuur **ContactPerson** die alle contactpersonen bevat. Deze is toegankelijk via de relatie **ContactPerson.ContactForParty == VendTable.Party** en beschikbaar voor alle leveranciers uit de leverancierstabel waarnaar wordt verwezen.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
