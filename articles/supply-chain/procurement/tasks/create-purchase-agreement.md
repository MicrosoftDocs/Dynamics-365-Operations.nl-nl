---
title: Een inkoopovereenkomst maken
description: Dit onderwerp begeleidt u door het maken van een inkoopovereenkomst.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92c9b429a05a2c25672cc14a0c9ee7adfef42631
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016826"
---
# <a name="create-a-purchase-agreement"></a>Een inkoopovereenkomst maken

[!include [banner](../../includes/banner.md)]

Dit onderwerp begeleidt u door het maken van een inkoopovereenkomst. Dit wordt gewoonlijk gedaan door een inkoopmanager. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. U moet de classificaties van inkoopovereenkomsten hebben ingesteld voordat u begint. Nadat u een overeenkomst hebt gemaakt, kunt u deze gebruiken wanneer u een inkooporder maakt. De voorwaarden van de inkoopovereenkomst worden dan gekopieerd naar de koptekst en naar regels in de order die door de overeenkomst worden beïnvloed.


## <a name="create-a-new-purchase-agreement"></a>Een nieuwe inkoopovereenkomst maken
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Inkoopovereenkomsten > Inkooporders**.
2. Klik op **Nieuw**.
3. Selecteer in het veld **Leveranciersrekening** de vervolgkeuzelijst en selecteer de nieuwe rij de gewenste record.
4. Selecteer in het veld **Classificatie van inkoopovereenkomst** de vervolgkeuzelijst en selecteer de nieuwe rij de gewenste record.
5. Vouw de het sneltabblad **Algemeen**.
6. Voer een datum in het veld **Vervaldatum** in.

    - Deze vervaldatum wordt de standaardwaarde voor alle toezeggingsregels zijn en bepaalt hoe lang elke specifieke toezegging geldig is.  

7. Typ in het veld **Documenttitel** een naam voor uw inkoopovereenkomst.

    - Laat het veld **Standaardtoezegging** ingesteld op **Toezegging producthoeveelheid** (of wijzig het als het hier niet op is ingesteld).  
    - De waarde van de standaardtoezegging bepaalt uw opties op de overeenkomstregels. Als u een nieuw toezeggingstype nodig hebt wanneer u de overeenkomstregels maakt, moet u de standaardtoezegging in de koptekst wijzigen. Er zijn 4 typen toezeggingen: **Toezegging producthoeveelheid** - voor een bepaalde hoeveelheid van een product; **Toezegging productwaarde** - voor een specifiek valutabedrag van een product; **Waardetoezegging productcategorie** - voor een specifiek valutabedrag in een aanschaffingscategorie waar het bedrag voor een catalogusartikel of een niet-catalogus artikel kan zijn; **Waardetoezegging** - voor een specifiek valutabedrag dat kan worden afgehandeld door elk product of elke aanschaffingscategorie.  

8. Selecteer **OK**.

## <a name="add-a-commitment"></a>Een toezegging toevoegen
1. Selecteer **Regel toevoegen**.
2. Selecteer in het veld **Artikelnummer** de gewenste record in het vervolgkeuzemenu.
3. Voer een getal in het veld **Hoeveelheid** in. Dit is de totale hoeveelheid die u bent overeengekomen te kopen van uw leverancier.  
4. Voer een nummer in het veld **Eenheidsprijs** in.
5. Vouw de sectie **Regeldetails** uit.
6. Stel de optie **Max is afgedwongen** in op **Ja**. De optie **Max is afgedwongen** beperkt het gebruik van de toezegging. U kunt slechts maximaal de hoeveelheid kopen die is opgegeven in het veld **Hoeveelheid** voor de regel.  

## <a name="add-header-conditions"></a>Koptekstvoorwaarden toevoegen
1. Selecteer **Opties** in het actievenster.
2. Selecteer **Weergave wijzigen**.
3. Selecteer **Weergave kopteksten**.
4. Vouw de sectie **Voorwaarden** uit.
5. Selecteer in het veld **Betalingsmethode** de gewenste record in het vervolgkeuzemenu. De betalingsvoorwaarden van de leverancierrekening worden hier standaard weergegeven.  
6. Selecteer in het veld **Leveringsmethode** de gewenste record in het vervolgkeuzemenu.
7. Selecteer in het veld **Leveringsvoorwaarden** de vervolgkeuzeknop om de zoekopdracht te openen.

## <a name="confirm-and-activate-the-agreement"></a>De verkoopovereenkomst bevestigen en activeren
1. Klik in het actievenster op **Inkoopovereenkomst**.
2. Selecteer **Bevestiging**. Stel de optie **Overeenkomst als effectief markeren** in op **Ja**.  
3. Selecteer **OK**.
4. Klik in het actievenster op **Inkoopovereenkomst**.
5. Selecteer **Bevestigingen van inkoopovereenkomst**. Met de optie **Voorbeeld/afdrukken** kunt u een document voor de inkoopovereenkomst genereren dat u vervolgens kunt afdrukken of naar de leverancier kunt verzenden. Als u de overeenkomst later wilt bijwerken en opnieuw wilt bevestigen, worden hier beide versies weergegeven.  
6. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]