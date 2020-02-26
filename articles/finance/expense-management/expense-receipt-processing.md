---
title: Verwerking van onkostenkwitanties
description: Dit onderwerp biedt informatie over de verwerking van optische tekenherkenning (OCR) voor kwitanties. Deze functie is bedoeld om de gebruikerservaring te verbeteren bij het maken van onkostennota's in Microsoft Dynamics 365 Finance.
author: stevensporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ead9039de63e2cf4f3a7faddd1702b9614d7f99
ms.sourcegitcommit: 6aceca43c53c4dde46954c0b6b855d488eb44ed2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027898"
---
# <a name="public-preview-expense-receipt-processing"></a>Openbaar voorbeeld: verwerking van onkostenkwitanties

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Onkosteninvoer is verbeterd via de introductie van de OCR-verwerking (Optical Character Recognition) voor kwitanties. Deze functie is bedoeld om de gebruikerservaring te verbeteren bij het maken van onkostennota's.

## <a name="key-features"></a>Belangrijke functies

- De handelaarsnaam, de datum en het totaalbedrag worden opgehaald uit ontvangsten.
- De functie probeert niet-gekoppelde kwitanties te koppelen aan niet-gekoppelde onkostentransacties.
- Gebruikers kunnen handmatig ingevoerde onkostentransacties maken vanuit kwitanties.

## <a name="usage-examples"></a>Voorbeelden van gebruik

- **Kwitanties automatisch koppelen waarin creditcardtransacties zijn opgenomen wanneer een onkostennota wordt gemaakt.**

    1. Open het werkgebied **Onkostenbeheer**.
    2. Controleer op het tabblad **Ontvangstbewijzen** of er niet-gekoppelde ontvangstbewijzen zijn. U kunt ook ontvangstbewijzen uploaden op het tabblad **Ontvangstbewijzen**.
    3. Controleer op het tabblad **Onkosten** of er niet-gekoppelde onkosten zijn. De onkostenbeheerder importeert deze onkosten meestal van de creditcardprovider.
    4. Selecteer **Nieuwe onkostennota**. Zoals u ziet, kunt u onkosten en ontvangsten nu ook opnemen wanneer u een onkostennota maakt. Als u zowel onkosten als ontvangsten toevoegt, wordt automatisch afstemmen van ontvangstbewijzen op onkosten geactiveerd.

- **Maak onkosten of stem onkosten af op een ontvangstbewijs.**

    1. Voeg op het tabblad **Ontvangstbewijzen** van een onkostennota een ontvangstbewijs toe door **Ontvangstbewijzen toevoegen** te selecteren.
    2. Onder de geüploade kopie van het ontvangstbewijs ziet u de opties **Maken** en **Afstemmen**.

        - Selecteer **Maken** om een handmatig ingevoerde onkostentransactie te maken en vul de waarden in die worden opgehaald uit het ontvangstbewijs.
        - Als u **Afstemmen** selecteert, probeert het systeem de bestaande onkosten te koppelen aan het ontvangstbewijs.

## <a name="installation"></a>Installatie

Deze functie werkt in combinatie met de functie **Nieuwe invulling voor het begrip onkostennota's** om de onkostenervaring te vereenvoudigen.

Als u deze geavanceerde onkostenmogelijkheden wilt gebruiken, installeert u de invoegtoepassing Service voor onkostenbeheer voor Microsoft Dynamics 365 Finance en schakelt u de functies in uw instantie in. U kunt de invoegtoepassing vanuit uw project openen in Microsoft Dynamics Lifecycle Services (LCS).

1. Meld u aan bij LCS en open de gewenste omgeving.
2. Ga naar **Volledige details**.
3. Selecteer **Onderhouden** of ga omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.
4. Selecteer **Een nieuwe invoegtoepassing installeren**.
5. Selecteer **Service voor onkostenbeheer**.
6. Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.
7. Selecteer **Installeren**.

Schakel in het werkgebied **Functiebeheer** de volgende functies in:

- Nieuwe invulling voor het begrip onkostennota's
- Automatisch afstemmen en onkosten maken op basis van ontvangst

Wanneer u deze functies inschakelt, worden de volgende acties uitgevoerd:

- Het bestaande werkgebied **Onkostenbeheer** wordt vervangen door het nieuwe werkgebied.
- Er is een nieuwe menuopdracht voor zichtbaarheid van onkostenvelden toegevoegd.
- U kunt de vorige pagina **Onkostennota's** nog steeds openen door naar **Onkostenbeheer > Mijn onkosten > Onkostennota's** te gaan.
- Met workflows en eventuele goedkeuringen gaat u nog steeds naar de bestaande pagina voor onkostennota's.
- Ontvangstbewijzen worden verwerkt via Microsoft Azure Cognitive Services en metagegevens worden opgehaald en toegevoegd.
- Er wordt een optie toegevoegd waarmee u een onkostennota kunt maken die overeenkomende niet-gekoppelde ontvangstbewijzen bevat.
- Met een optie die wordt toegevoegd aan onkostennota's kunt u een onkostenregel maken op basis van een ontvangst of wordt geprobeerd een bestaand ontvangstbewijs te koppelen aan een bestaande onkostenregel.

Zie [Nieuwe invulling voor het begrip onkostennota's](ExpenseWorkspaceNew.md) voor meer informatie over de nieuwe functie voor onkostennota's.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

**Worden mijn gegevens door Microsoft gebruikt voor modellen?**

Nee, Microsoft heeft een algemeen machinetrainingsmodel voor de verwerkingsservice voor ontvangstbewijzen. Dit model is niet gebaseerd op de ontvangstbewijzen die u uploadt.

**Waar is deze functie beschikbaar en wordt deze verwerkt?**

Momenteel worden de Verenigde Staten ondersteund.

**Waar gaan mijn ontvangstbewijzen naartoe?**

Finance neemt contact op met Cognitive Services om de veldgegevens op te halen. Cognitive Services behoudt een kopie van uw ontvangstbewijs gedurende maximaal 24 uur terwijl de verwerking plaatsvindt. Nadat de verwerking is voltooid, wordt het ontvangstbewijs door Cognitive Services verwijderd. Ontvangstbewijzen worden nog steeds in Finance opgeslagen.

Zie [Ontvangstbewijzen begrijpen inschakelen met de nieuwe mogelijkheid Formulierherkenning](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) voor meer informatie.
