---
title: Verwerking instellen en uitvoeren om een eenvoudige ER-exportindeling aan te roepen en een Excel-rapport te genereren
description: In dit onderwerp vindt u een voorbeeld van het instellen en gebruiken van elektronische berichten.
author: liza-golub
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 25721f1b79d8f0fbf8ca2112ed21fa2d8cd0bc84
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433774"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Verwerking instellen en uitvoeren om een eenvoudige ER-exportindeling aan te roepen en een Excel-rapport te genereren

[!include [banner](../includes/banner.md)]

Nadat u uw ER-indeling hebt gemaakt, hebt toegewezen aan gegevensbronnen en hebt voltooid, kunt u deze uitvoeren vanuit het werkgebied **Elektronische rapportage**. Nadat het rapport is gegenereerd, kunt u het lokaal opslaan.

Als u de volgende aspecten van het rapportageproces wilt beheren, stelt u de verwerking van elektronische berichten in:

- Informatie vastleggen over wie het rapport heeft gegenereerd.
- Informatie vastleggen over wanneer het rapport is gegenereerd.
- De rapporten opslaan die zijn gegenereerd voor vorige perioden.

In het volgende voorbeeld wordt aangegeven hoe u elektronische berichten kunt instellen om een rapport te genereren dat is gebaseerd op een ER-exportindeling voor Microsoft Excel. Als u dit voorbeeld wilt volgen, moet u al een ER-exportindeling voor Excel hebben gemaakt, hebben toegewezen aan gegevensbronnen en hebben voltooid. Bovendien moet er al een nummerreeks zijn ingesteld voor elektronische berichten.

Bij het samenstellen van de verwerking is het handig om eerst op te geven welke verwerkingsacties en statussen moeten worden ingesteld. In de volgende afbeelding wordt de verwerking voor dit voorbeeld weergegeven.

![Schema voor verwerking](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Berichtstatussen maken

1. Ga naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Berichtstatussen**.
2. Maak de volgende berichtstatussen:

    - Nieuw
    - Voorbereid
    - Gegenereerd

    ![Berichtstatussen](media/message-statuses.png)

3. Schakel op de regel voor de status **Nieuw** het selectievakje **Verwijderen toestaan** in om gebruikers in staat te stellen berichten met deze status te verwijderen.

## <a name="create-additional-fields"></a>Extra velden maken

1. Ga naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Aanvullende velden**.
2. Voeg een extra veld met bijbehorende waarden toe.
3. Stel de optie **Bewerking door gebruiker** in op **Ja** om gebruikers in staat te stellen het veld te bewerken.

![Aanvullende velden](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Berichtverwerkingsacties maken

Voor dit voorbeeld maakt u de volgende acties voor berichtverwerking:

- **Bericht maken**
- **Bijwerken naar Voorbereid**
- **Rapport genereren**
- **Bijwerken naar beginstatus** (optioneel)

Volg deze stappen om de acties te maken.

1. Ga naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Acties berichtverwerking**.
2. Maak een actie met de naam **Bericht maken**. Op het sneltabblad **Algemeen** selecteert u **Bericht maken** in het veld **Actietype**.
3. Maak een actie met de naam **Bijwerken naar Voorbereid** en stel de volgende velden in:

    - Op het sneltabblad **Algemeen** selecteert u **Verwerking door gebruiker van berichtniveau** in het veld **Actietype**.
    - Selecteer op het sneltabblad **Aanvankelijke statussen** de optie **Nieuw** in het veld **Berichtstatus**.
    - Selecteer op het sneltabblad **Resulterende statussen** de optie **Voorbereid** in het veld **Berichtstatus**. Voer in het veld **Antwoordtype** de waarde **Uitgevoerd** in.

4. Maak een actie met de naam **Rapport genereren** en stel de volgende velden in:

    - Op het sneltabblad **Algemeen** selecteert u **Export van elektronische rapportage** in het veld **Actietype**. Selecteer de ER-exportindeling in het veld **Indelingstoewijzing**. De opties zijn **Excel**, **XML**, **JSON**, **Tekst** en **Overig**.
    - Selecteer op het sneltabblad **Aanvankelijke statussen** de optie **Voorbereid** in het veld **Berichtstatus**.
    - Selecteer op het sneltabblad **Resulterende statussen** de optie **Gegenereerd** in het veld **Berichtstatus**. Voer in het veld **Antwoordtype** de waarde **Uitgevoerd** in.

    ![De actie Rapport genereren](media/generate-report-action.png)

5. Optioneel: als u wilt dat gebruikers een rapport meerdere keren opnieuw kunnen genereren, kunt u een actie ggenaamd **Bijwerken naar beginstatus** maken en de volgende velden instellen:

    - Op het sneltabblad **Algemeen** selecteert u **Verwerking door gebruiker van berichtniveau** in het veld **Actietype**.
    - Selecteer op het sneltabblad **Aanvankelijke statussen** de optie **Gegenereerd** in het veld **Berichtstatus**.
    - Op het sneltabblad **Resultaatstatussen** voegt u een aparte regel toe voor elk van de twee berichtstatussen (**Voorbereid** en **Nieuw**). Stel voor beide regels het veld **Antwoordtype** in op **Uitgevoerd**.

## <a name="electronic-message-processing"></a>Elektronisch bericht verwerken

Voor dit voorbeeld moeten de acties zo worden ingesteld dat ze afzonderlijk worden uitgevoerd. Er wordt vanuit gegaan dat de gebruiker elke actie initialiseert.

1. Ga naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Elektronisch bericht verwerken**.
2. Voeg een record voor uw verwerking en alle eerder gedefinieerde acties en een extra veld toe.
3. Optioneel: definieer op het sneltabblad **Beveiligingsrollen** beveiligingsrollen voor uw verwerking om toegang te beperken tot specifieke rapportage.
4. Ga naar **Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Elektronische berichten**.
5. Selecteer **Nieuw** om een bericht te maken. Vervolgens kunt u datums en een omschrijving toevoegen. U kunt ook de waarde van het extra veld bijwerken.

    ![Een elektronisch bericht maken](media/create-electronic-message.png)

    Het raster op het sneltabblad **Actielogboek** wordt automatisch gevuld met alle acties die worden uitgevoerd op het bericht.

    U kunt de status van het bericht nu verwijderen of bijwerken. 

6. Selecteren **Status bijwerken** om de berichtstatus bij te werken. Selecteer in het veld **Nieuwe status** **Voorbereid** en selecteer vervolgens **OK**.

    ![De berichtstatus bijwerken](media/update-status.png)

    De berichtstatus wordt bijgewerkt naar **Voorbereid**.

7. Genereer het rapport door **Rapport genereren** te selecteren.

    Het rapport wordt gegenereerd en de berichtstatus en het actielogboek worden bijgewerkt.

8. Als u het gegenereerde rapport wilt weergeven, selecteert u de knop **Bijlage** (paperclipsymbool) in de rechterbovenhoek van de pagina.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
