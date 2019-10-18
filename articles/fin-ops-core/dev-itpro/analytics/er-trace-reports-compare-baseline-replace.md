---
title: Verbeteringen in het traceren van de resultaten van gegenereerde ER-rapporten en het vergelijken hiervan met basislijnwaarden
description: Dit onderwerp bevat informatie over hoe de ER-basislijnfunctie is verbeterd in Microsoft Dynamics 365 for Finance and Operations 10.0.3 (juni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: a260be0f8659106907b26bf69bee3b33b09d0c24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181330"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a>Verbeteringen in het traceren van de resultaten van gegenereerde ER-rapporten en het vergelijken hiervan met basislijnwaarden

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de eerste verbeteringen beschreven die zijn aangebracht in de basisfunctie van het raamwerk voor elektronische rapportage (ER). Deze verbeteringen zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations 10.0.3 (juni 2019) en hoger.

## <a name="automate-the-setting-of-baseline-rules"></a>De instelling van basislijnregels automatiseren

In het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) wordt uitgelegd hoe u het ER-raamwerk kunt configureren voor het verzamelen van informatie over de uitvoering van ER-indelingen en het evalueren van de resultaten van die uitvoeringen. In het voorbeeld in dit onderwerp worden de stappen weergegeven die moeten worden uitgevoerd.

Hieronder ziet u enkele van deze stappen:

- Voer een ER-indeling uit om een uitgaand bestand te genereren en sla het bestand lokaal op.
- Voeg het lokaal opgeslagen bestand toe als bijlage van de basislijn die is toegevoegd voor een ER-indeling.
- Configureer de basislijnregel voor de toegevoegde basislijn. Deze configuratie omvat de volgende stappen:

    - Geef een ER-indelingselement op dat wordt gebruikt om een uitgaand bestand te genereren.
    - Selecteer de bijlage die verwijst naar het gegenereerde uitgaande bestand.

> [!NOTE]
> Deze stappen moeten handmatig worden uitgevoerd, ook al kunnen ze dankzij de nieuwe ER-mogelijkheden worden geautomatiseerd. Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Voorbeeld: De instelling van basislijnregels automatiseren

Als u de stappen in dit voorbeeld wilt uitvoeren, moet u eerst de stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren, tot en met de sectie Een nieuwe basislijn toevoegen voor een ontworpen ER-indeling.

### <a name="review-added-baseline"></a>Toegevoegde basislijn evalueren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Basislijnen**.

    > [!NOTE]
    > De knop **Basislijnen** in het actievenster is alleen beschikbaar wanneer de ER-gebruikersparameter **Uitvoeren in foutoplossingsmodus** is ingeschakeld voor het huidige bedrijf.

De basislijn is toegevoegd voor de geselecteerde indeling **Indeling voor leren van ER-basislijnen**, maar de basislijnregels zijn nog niet toegevoegd voor deze basislijn.

![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-AddBaseline2.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")

### <a name="make-a-new-baseline-rule"></a>Een nieuwe basislijnregel maken

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw in de structuur **Model voor leren van ER-basislijnen** uit.
3. Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.
4. Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
5. Geef in het veld **Id opgeven** het cijfer **1** op.
6. Stel de optie **Basislijnbestanden maken** op **Ja** in.
7. Selecteer **OK**.

    ![Het dialoogvenster Parameters elektronisch rapport](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Schermafbeelding van het dialoogvenster Parameters elektronisch rapport")

8. Selecteer **Basislijnen**.

    ![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")

    Het gegenereerde uitgaande bestand wordt automatisch gekoppeld aan de basislijn van de uitgevoerde ER-indeling. De basislijnregel is automatisch toegevoegd aan deze basislijn en bevat ook de verwijzing naar het bijgevoegde bestand.

9. Voer in het veld **Naam** de tekst **Basislijn 1** in.
10. Voer in het veld **Masker bestandsnaam** de waarde **.xml** in.
11. Selecteer **Opslaan**.

### <a name="run-the-format"></a>De indeling uitvoeren

U kunt nu de resterende stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren, vanaf de sectie De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren.

> [!NOTE]
> Wanneer u de automatisch toegevoegde basislijnregel verwijdert op het sneltabblad **Basislijnen**, wordt de bijlage waarnaar wordt verwezen niet automatisch verwijderd.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>De basislijn zo configureren dat voortdurend veranderende delen van de ER-uitvoer worden genegeerd

Wanneer een ER-indeling is ontworpen om informatie te bevatten die wordt gewijzigd wanneer de indeling wordt uitgevoerd, moet de indeling vereist zijn als u de ER-basislijnfunctie wilt gebruiken om de gegenereerde resultaten met basislijnwaarden te vergelijken. De informatie kan bijvoorbeeld de verwerkingsdatum en -tijd zijn of de unieke id van een gegenereerd document in verschillende indelingen (\[GUID\], enzovoort). Met de nieuwe ER-mogelijkheden kunt u de basislijnregel zo configureren dat veranderlijke elementen van een ER-indeling worden genegeerd wanneer de indeling wordt uitgevoerd met het doel om basislijnwaarden te vergelijken met de resultaten van de uitvoering van de indeling. Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Voorbeeld: De basislijn zo configureren dat voortdurend veranderende delen van de ER-uitvoer worden genegeerd

Als u de stappen in dit voorbeeld wilt uitvoeren, moet u eerst de stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren.

### <a name="modify-a-configured-er-format"></a>Een geconfigureerde ER-indeling wijzigen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw in de structuur **Model voor leren van ER-basislijnen** uit.
3. Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.
4. Selecteer **Ontwerper**.
5. Selecteer **Output\\Document** in de structuur.
6. Selecteer **Toevoegen**.
7. Ga naar het vervolgkeuzemenu en selecteer **XML\\Kenmerk** in de structuur.
8. Voer in het veld **Naam** de waarde **ProcessingDateTime** in.
9. Selecteer **OK**.
10. Selecteer **Uitvoer\\Document\\ProcessingDateTime** in de structuur op het tabblad **Toewijzing**.
11. Selecteer **Formule bewerken**.
12. Voer in het veld **Formule** de volgende expressie in: **DATETIMEFORMAT(NOW(), "O")**
13. Selecteer **Opslaan** en vervolgens **Testen**.
14. Selecteer opnieuw **Testen** om de geconfigureerde expressie opnieuw te testen.

    ![De pagina Formuleontwerper](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Schermafbeelding van de pagina Formuleontwerper")

    > [!NOTE]
    > Op het tabblad **Testresultaten** ziet u dat de geconfigureerde expressie telkens een andere datum- en tijdwaarde oplevert wanneer deze wordt aangeroepen.

15. Sluit de pagina **Formuleontwerper** en selecteer **Opslaan**.

    ![De pagina Indelingsontwerper](media/GER-BaselineSample-FormatMappingDesign2.PNG "Schermafbeelding van de pagina Indelingsontwerper")

16. Sluit de pagina **Indelingsontwerper**.

### <a name="remove-an-existing-baseline-rule"></a>Een bestaande basislijnregel verwijderen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Basislijnen**.
3. Selecteer in de lijst met basislijnen de basislijn die is geconfigureerd voor de indeling **Indeling voor leren van ER-basislijnen**.
4. Selecteer op het sneltabblad **Basislijnen** de optie **Verwijderen** om de basislijnregel te verwijderen die u eerder hebt geconfigureerd.

![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-AddBaseline3.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Vervangingen definiëren voor de bindingen van ontworpen ER-indeling

1. Selecteer op de pagina **Configuraties** op het sneltabblad **Vervangingen** de optie **Onderdelen selecteren**.
2. Vouw in de structuur met indelingsonderdelen **Uitvoer** uit, vervolgens **Uitvoer\\Document** en schakel het selectievakje voor **Uitvoer\\Document\\ProcessingDateTime** in.

    ![Het dialoogvenster Onderdelen selecteren](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Schermafbeelding van het dialoogvenster Onderdelen selecteren")

3. Selecteer **OK**.

![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-AddBaseline4.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")

Het geselecteerde ER-indelingsonderdeel is toegevoegd aan de lijst met onderdelen op het sneltabblad **Vervangingen**. Wanneer de basis-ER-indeling wordt uitgevoerd in de foutoplossingsmodus, wordt de indelingsbinding voor elk onderdeel vervangen door de binding die wordt weergegeven in de kolom **Binding**. Selecteer **Bewerken** om de standaardbinding te wijzigen voor een onderdeel dat wordt weergegeven op het sneltabblad **Vervangingen**.

### <a name="make-a-new-baseline-rule"></a>Een nieuwe basislijnregel maken

Volg de stappen in de sectie Voorbeeld: De instelling van basislijnregels automatiseren eerder in dit onderwerp. Er wordt een melding weergegeven dat het uitgaande bestand is gegenereerd met behulp van basislijninstellingen en dat er een geforceerde vervanging van de indelingsbindingen heeft plaatsgevonden.

![Melding op de pagina Configuraties](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Schermafbeelding van de melding op de pagina Configuraties")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Waarschuwingen over het vervangen van indelingsbindingen onderdrukken

Door specifieke ER-parameters in te stellen, kunt u meldingen onderdrukken die waarschuwen bij het vervangen van indelingsbindingen. Deze onderdrukking kan handig zijn indelingsbindingen in een modus zonder toezicht worden vervangen met behulp van Regression Suite Automation Tool. In dit geval kan de waarschuwing worden beschouwd als een fout van de testcase die wordt uitgevoerd.

1. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** de optie **Gebruikersparameters**.
2. Stel de optie **Waarschuwingen voor basislijn** in op **Ja** en selecteer **OK**.

![Het dialoogvenster Gebruikersparameters](media/GER-BaselineSample-ERUserParameters1.png "Schermafbeelding van het dialoogvenster Gebruikersparameters")

### <a name="review-the-generated-baseline-file"></a>Het gegenereerde basislijnbestand bekijken

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Basislijnen**.
3. Selecteer **Bijlagen**.

    ![De pagina Bijlagen](media/GER-BaselineSample-AttachedBaselineFile.PNG "Schermafbeelding van de pagina Bijlagen")

    > [!NOTE]
    > Het gegenereerde bestand bevat de tekst voor de verwerkingsdatum en -tijd (**"#"**) uit de binding die is geconfigureerd in de toegevoegde basislijnregel, niet uit de binding van de indeling.

4. Sluit de pagina **Bijlagen**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw in de structuur **Model voor leren van ER-basislijnen** uit.
3. Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.
4. Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
5. Geef in het veld **Id opgeven** het cijfer **1** op.
6. Selecteer **OK**.
7. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Foutopsporingslogboeken voor configuraties**.

Het uitvoeringslogboek bevat informatie over de resultaten van de vergelijking van het gegenereerde bestand met de geconfigureerde basislijn. In het logboek wordt aangegeven dat het gegenereerde bestand en de basislijn overeenkomen, ook al bevat de uitgevoerde indelingen de binding om een steeds veranderende datum- en tijdwaarde in het uitgaande bestand in te voeren.

> [!NOTE]
> Hoewel het uitgaande bestand is gegenereerd met behulp van basislijninstellingen die de vervanging van de bindingen van de indeling forceren, ontvangt u geen waarschuwingen over de vervanging.

## <a name="exchange-baseline-settings-between-environments"></a>Basislijninstellingen tussen omgevingen uitwisselen

### <a name="export-baseline-settings"></a>Basislijninstellingen exporteren

Met de nieuwe ER-mogelijkheden kunt u basislijninstellingen voor de geselecteerde ER-indeling exporteren uit de huidige omgeving exporteren en deze opslaan als XML-bestanden. 

Als u basislijninstellingen wilt exporteren, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Exporteren**.

### <a name="import-baseline-settings"></a>Basislijninstellingen importeren

Geëxporteerde basislijninstellingen kunnen in een andere omgeving worden geïmporteerd. De omgeving moet eerst worden geïmporteerd als ER-indeling. Vervolgens kunt u de basislijninstellingen importeren.

Als u basislijninstellingen vanuit een lokaal opgeslagen XML-bestand wilt importeren, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Importeren** en vervolgens selecteert u **Bladeren** om het XML-bestand te selecteren.

![Het dialoogvenster Basislijninstellingen importeren](media/GER-BaselineSample-ImportBaseline1.PNG "Schermafbeelding van het dialoogvenster Basislijninstellingen importeren")

Als u basislijninstellingen wilt importeren vanuit een XML-bestand dat op de Microsoft SharePoint-server is opgeslagen, op basis van de huidige instellingen voor documentbeheer en het geselecteerde documenttype, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Importeren uit bron**. Selecteer het documenttype en het XML-bestand. Het vereiste documenttype voor toegang tot de SharePoint-map moet vooraf worden geconfigureerd.

![Het dialoogvenster Importeren uit bron](media/GER-BaselineSample-ImportBaseline2.PNG "Schermafbeelding van het dialoogvenster Importeren uit bron")

> [!NOTE]
> U kunt Taakregistratie gebruiken om de stappen vast te leggen voor het selecteren van het vereiste documenttype en de bestandsnaam in het dialoogvenster **Importeren vanuit bron**. Op deze manier kunt u de vereiste basislijninstellingen op de SharePoint-server behouden en deze vervolgens automatisch importeren door een taakregistratie af te spelen wanneer u automatische tests uitvoert met behulp van Regression Suite Automation Tool.

## <a name="additional-resources"></a>Aanvullende resources

- [Gegenereerde rapportresultaten traceren en vergelijken met basislijnwaarden](er-trace-reports-compare-baseline.md)
- [Taakregistratie](../user-interface/task-recorder.md)
