---
title: Voorbeeld van de verwerking van aanmaningen
description: In dit onderwerp wordt een voorbeeld bekeken van het proces van het maken, afdrukken en boeken van aanmaningen.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e813b4f0c6408a8046fa8203007a0a356ca2c794
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347803"
---
# <a name="process-collection-letters-example"></a>Voorbeeld van de verwerking van aanmaningen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt een voorbeeld bekeken van het proces van het maken, afdrukken en boeken van aanmaningen. Het voorbeeld is gebaseerd op de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** in Crediteringen en aanmaningen. Het gebruikt gegevens in het demobedrijf USMF en een nieuwe klant, US-045.

Om te beginnen gaat u naar **Klanten \> Klanten \> Alle klanten**. Vervolgens selecteert u **Nieuw** en voert u vervolgens de vereiste informatie in om klant US-045 te maken.

Voer als u gereed bent de volgende stappen uit.

1. Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningsreeks instellen** en stel de aanmaningsreeks in zoals wordt weergegeven in de volgende tabel die is toegewezen aan het klantboekingsprofiel.

|     Aanmaningscode      |     Beschrijving                           |     Valuta      |     Hoofdrekening        |     Bijzondere kosten in valuta     |     Minimum achterstallig saldo        |     Dagen blokkeren      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Aanmaning 1         |     Tweede melding met bijzondere kosten        |     USD           |                           |     0,00                  |     0,00                  |     2                 |
|     Aanmaning 2         |     Tweede melding met bijzondere kosten        |     USC           |     403150                |     20.00                 |     10.00                 |     3                 |
|     Aanmaning                    |     Laatste melding met bijzondere kosten         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

In de volgende afbeelding wordt de informatie in de tabel weergegeven zoals deze op de pagina **Aanmaningen** zou verschijnen. 

[![Een aanmaningsreeks instellen.](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 U moet nu de twee parameters instellen die voor dit voorbeeld zijn vereist.

2. Ga naar **Crediteringen en aanmaningens \> Instellingen \> Parameters van module Klanten** en voer deze stappen uit:

    1. Stel op het tabblad **Aanmaningen** de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** in op **Ja**.
    2. Zorg ervoor dat het veld **Aanmaning maken per** is ingesteld op **Klant**.

    [![Parameters van de module Klanten instellen voor aanmaningen.](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**, selecteer **Nieuw** en voer vervolgens deze stappen uit:

    1. Selecteer **US-045** in het veld **Klantrekening**.
    2. Voer in het veld **Factuurdatum** de waarde **15-01-2021** in.
    3. Voer in het veld **Vervaldatum** de waarde **16-01-2021** in.
    4. Voer op het sneltabblad **Factuurregels** in het veld **Hoofdrekening** de waarde **401100** in.
    5. Voer in het veld **Eenheidsprijs** **500.00** in.
    6. Selecteer **Boeken**.

    U moet nu twee creditnota's voor de klant invoeren.

4. Selecteer **Nieuw** en voer de volgende stappen uit:

    1. Selecteer **US-045** in het veld **Klantrekening**.
    2. Voer in het veld **Factuurdatum** de waarde **15-01-2021** in.
    3. Voer in het veld **Vervaldatum** de waarde **16-01-2021** in.
    4. Voer op het sneltabblad **Factuurregels** in het veld **Hoofdrekening** de waarde **401100** in.
    5. Voer **-100,00** in het veld **Eenheidsprijs** in.
    6. Selecteer **Boeken**.

5. Herhaal stap 4 maar geef **-200,00** op in het veld **Eenheidsprijs**.
6. Ga naar **Klanten \> Klanten \> Alle klanten** en selecteer klant **US-045**. Selecteer vervolgens in het actievenster **Transacties \> Transactes** om de klanttransacties te bekijken die u eerder hebt geboekt.

    [![De geboekte klanttransacties controleren.](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    U moet nu aanmaningen maken voor klant US-045.

7. Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen maken** en voer deze stappen uit:

    1. Stel de opties **Factuur** en **Creditnota** in op **Ja**.

        Het veld **Aanmaning** moet standaard worden ingesteld op **Aanmaning per klant**.

    2. Voer in het veld **Aanmaningsdatum** de waarde **19-01-2021** in.
    3. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** en voeg vervolgens in het veld **Klantrekening** de waarde **US-045** toe.
    4. Selecteer **OK**.
    5. Selecteer **OK** om aanmaningen te maken.

8. Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen controleren en verwerken** en voer deze stappen uit:

    1. De aanmaningscode op zowel de koptekst als de transactieregels is **Aanmaning 1**, omdat deze aanmaning de eerste aan aanmaning in de reeks is. (Als u de transactieregels wilt weergeven, moet u mogelijk het sneltabblad **Transacties** selecteren.)

   [![Controleren of dezelfde aanmaningscode wordt weergegeven in de koptekst en op de regels.](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Selecteer **Boeken** in het actievenster.
    3. Voer in het veld **Boekingsdatum** de waarde **19-01-2021** in.

    U moet nu opnieuw aanmaningen maken voor klant US-045.

9. Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen maken** en voer deze stappen uit:

    1. Stel de opties **Factuur** en **Creditnota** in op **Ja**.

        Het veld **Aanmaning** moet standaard worden ingesteld op **Aanmaning per klant**.

    2. Voer in het veld **Aanmaningsdatum** de waarde **23-01-2021** in.
    3. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** en voeg vervolgens in het veld **Klantrekening** de waarde **US-045** toe.
    4. Selecteer **OK**.
    5. Selecteer **OK** om aanmaningen te maken.

10. Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen controleren en verwerken** en voer deze stappen uit:

    1. De aanmaningscode in de koptekst is **Aanmaning 1**. De code op de transactieregels is echter **Aanmaning 2**.

   [![Controleert of verschillende aanmaningscodes worden weergegeven in de koptekst en op de regels.](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  De codes verschillen omdat de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** is ingesteld op **Ja**.

  2. Boek deze aanmaning niet.

11. Ga naar **Crediteringen en aanmaningen \> Instellen \> Parameters van module Klanten** en stel vervolgens op het tabblad **Aanmaningen** de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** in op **Nee**.

    [![De optie Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode instellen op Nee.](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    U moet nu opnieuw aanmaningen maken voor klant US-045.

12. Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen maken** en voer deze stappen uit:

    1. Stel de opties **Factuur** en **Creditnota** in op **Ja**.

        Het veld **Aanmaning** moet standaard worden ingesteld op **Aanmaning per klant**.

    2. Voer in het veld **Aanmaningsdatum** de waarde **23-01-2021** in.
    3. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** en voeg vervolgens in het veld **Klantrekening** de waarde **US-045** toe.
    4. Selecteer **OK**.
    5. Selecteer **OK** om aanmaningen te maken.

13. Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen controleren en verwerken**. U ziet nu dat de aanmaningscode op zowel de koptekst als de transactieregels **Aanmaning 2** is.

    [![Opnieuw tonen dat dezelfde aanmaningscode wordt weergegeven in de koptekst en op de regels.](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Op beide plekken wordt dezelfde code weergegeven omdat de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** nu is ingesteld op **Nee**.
