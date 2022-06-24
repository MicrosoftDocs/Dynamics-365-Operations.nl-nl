---
title: Belasting wordt niet berekend of het btw-bedrag is nul
description: Dit artikel bevat informatie die kan helpen bij het oplossen van problemen als het belastingbedrag 0 (nul) is of als de belasting niet wordt berekend.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: f2a5bb0d1cef93ec1fea2e21c1750fe94a454c18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849839"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Belasting wordt niet berekend of het belastingbedrag is nul

[!include [banner](../includes/banner.md)]

Een transactie kan een regelbedrag hebben dat niet 0 (nul) is, maar de belasting wordt niet berekend of het berekende belastingbedrag is 0. Volg de stappen in de volgende secties zoals vereist om dit probleem op te lossen.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Controleer of de juiste belastingcodes zijn geselecteerd door de transactie

Als de transactie niet de juiste belastingcodes selecteert of als er helemaal geen belastingcodes worden geselecteerd, wordt er geen belasting berekend. Volg deze stappen om te controleren of de juiste belastingcodes worden geselecteerd door de transactie. 

1. Controleer op de transactieregel, op het sneltabblad **Regeldetails**, op het tabblad **Instellingen**, in de sectie **Btw** of de juiste belastinggroepen zijn geselecteerd in de velden **Btw-groep artikel** en **Btw-groep**. Als de juiste belastinggroepen niet zijn geselecteerd, selecteer ze dan.

    [![Velden Btw-groep artikel en Btw-groep.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-groepen**.
3. Selecteer de juiste btw-groep en maak vervolgens op het sneltabblad **Instellingen** een notitie van de belastingcode in het veld **Btw-code**.

    [![Pagina met Btw-groepen.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-groepen artikel**.
5. Selecteer de juiste btw-groep voor het artikel en controleer vervolgens op het sneltabblad **Instellingen** of de belastingcode in het veld **Btw-code** overeenkomt met de belastingcode van de btw-groep.

    [![Pagina met Btw-groepen artikelen.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Als de belastingcodes niet overeenkomen, moet u de btw-code voor een van de groepen bijwerken.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Controleer of de geselecteerde belastingcodes niet zijn vrijgesteld en of ze het juiste belastingtarief hebben

Als de belastingcodes zijn vrijgesteld of als het belastingtarief 0 (nul) is, is het resultaat van de belastingberekening 0. Volg deze stappen om te bepalen of de geselecteerde belastingcodes zijn vrijgesteld en om te controleren of het juiste belastingtarief op deze codes wordt toegepast.

1. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-groepen**.
2. Selecteer de juiste btw-groep en controleer vervolgens op het sneltabblad **Instellingen** of het selectievakje **Vrijstelling** leeg is. Als dit is geselecteerd, maakt u het leeg.

    [![Selectievakje Vrijstelling op de pagina Btw-groepen.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-codes**.
4. Selecteer de betreffende btw-code en controleer of het belastingtarief in het veld **Waarde** niet 0 (nul) is. Als het 0 is, moet u het veld bijwerken met het juiste belastingtarief.

    [![Waarde veld op de pagina Waarden btw-codes.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Bepaal of nul het juiste belastingbedrag is

In sommige gevallen is het juist als het belastingbedrag 0 (nul) is. Volg deze stappen om te bepalen of 0 het juiste belastingbedrag voor uw transactie is.

1. Ga naar **Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**.
2. Controleer op het tabblad **Btw** in het veld **Berekeningsmethode** of **Totaal** is geselecteerd.

    [![Het veld Berekeningsmethode op de pagina Grootboekparameters.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-codes**.
4. Selecteer de juiste btw-code, selecteer **Berekening** \> **Marginale basis** en controleer of de marginale basis is ingesteld op **Nettobedrag factuursaldo** of **Totaal factuur incl. andere btw-bedragen**. Zie [Totaal factuur incl. andere btw-bedragen](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts) voor meer informatie.
5. Als de juiste waarden zijn ingesteld in stap 2 en 4, bepaalt u of het totaalbedrag van de transactie 0 (nul) is. Als het totaalbedrag 0 is, is een belastingbedrag van 0 het verwachte resultaat. Omdat de belastingberekening wordt gebaseerd op het totaalbedrag van het factuursaldo en niet op elke regel, wordt het belastingbedrag van 0 toegewezen aan elke regel na de belastingberekening.

## <a name="determine-whether-customization-exists"></a>Bekijk of er een aanpassing bestaat

Als u de stappen in de vorige secties hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat. Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
