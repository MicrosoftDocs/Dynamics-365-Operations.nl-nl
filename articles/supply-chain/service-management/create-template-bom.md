---
title: Een sjabloonstuklijst maken
description: Met verschillende methoden kunt u een sjabloonstuklijst maken.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 169b54a0509a2e11ce2e888404da10fd81db475e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678201"
---
# <a name="create-a-template-bom"></a>Een sjabloonstuklijst maken   

[!include [banner](../includes/banner.md)]


Met de onderstaande methoden kunt u een sjabloonstuklijst maken. Voor alle methoden zijn de velden **Datum vanaf** en **Datum t/m** optioneel en dienen ze alleen ter informatie.

## <a name="create-a-template-bom-manually"></a>Handmatig een sjabloonstuklijst maken

1.  Ga naar **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.

2.  Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.

3.  Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Handmatig**.

4.  Selecteer in het veld **Artikelnummer** een artikel van het type **Stuklijst**.

5.  Voer in het veld **Naam** een naam voor de sjabloon in.

6.  Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.

7.  Selecteer **OK**.

Er is een nieuwe lege sjabloonstuklijst gemaakt.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Een sjabloonstuklijst maken op basis van een andere sjabloonstuklijst

1.  Selecteer **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.

2.  Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.

3.  Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Sjabloonstuklijst**.

4.  Selecteer in het veld **Referentienummer** een bestaande sjabloonstuklijst die u naar uw nieuwe sjabloonstuklijst wilt kopiëren.

5.  Voer in het veld **Naam** een naam voor de sjabloon in.

6.  Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.

7.  Selecteer **OK**.

Er is een nieuwe sjabloonstuklijst gemaakt met regels die overeenkomen met de regels in de oorspronkelijke sjabloonstuklijst.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Een sjabloonstuklijst maken op basis van een artikelstuklijst

1.  Selecteer **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.

2.  Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.

3.  Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Stuklijst**.

4.  Selecteer in het veld **Referentienummer** een stuklijstversie. Er wordt een artikel van het type stuklijst naar het veld **Artikelnummer** gekopieerd.

5.  Voer in het veld **Naam** een naam voor de sjabloon in.

6.  Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.

7.  Selecteer **OK**.

Er is een nieuwe sjabloonstuklijst gemaakt met regels die overeenkomen met de regels van de stuklijst die wordt vermeld in **Stuklijsten**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Een sjabloonstuklijst maken op basis van een productiestuklijst

1.  Selecteer **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.

2.  Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.

3.  Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Productie**.

4.  Selecteer in het veld **Referentienummer** een productiestuklijst.

5.  Voer in het veld **Naam** een naam voor de sjabloon in.

6.  Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.

7.  Selecteer **OK**.

Er is een nieuwe sjabloonstuklijst gemaakt met regels die overeenkomen met de regels van de stuklijst die wordt vermeld in **Stuklijst**.

## <a name="see-also"></a>Zie ook

[Sjabloonstuklijsten](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]