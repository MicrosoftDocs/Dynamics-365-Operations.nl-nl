---
title: ER-modeltoewijzingen configureren die afhankelijk zijn van de landcontext
description: In dit onderwerp wordt uitgelegd hoe u ER-modeltoewijzingen zo kunt instellen dat deze afhankelijk zijn van de land-/regiocontext van de rechtspersoon die het gebruik ervan beheert.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: a9035f128a1db4bcd126f09c0fe30c1857fa884a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680870"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>ER-modeltoewijzingen configureren die afhankelijk zijn van de landcontext

[!include[banner](../includes/banner.md)]

U kunt ER-modeltoewijzingen (Elektronische rapportage) zo configureren dat deze een generiek ER-gegevensmodel implementeren, die wel specifiek zijn voor Dynamics 365 Finance. In dit onderwerp wordt uitgelegd hoe u meerdere ER-modeltoewijzingen kunt ontwerpen voor een ER-gegevensmodel om te bepalen hoe deze worden gebruikt door overeenkomstige ER-indelingen die worden uitgevoerd vanuit bedrijven met verschillende land- of regiocontexten.

## <a name="prerequisites"></a>Vereisten

Om de voorbeelden in dit onderwerp te kunnen voltooien, moet u toegang tot het volgende hebben:

- Toegang tot Financiën voor een van de volgende rollen:
    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Toegang tot het exemplaar van Regulatory Configuration Services (RCS) dat is ingericht voor dezelfde tenant als Financiën voor een van de volgende rollen:
    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

Voor sommige stappen in dit onderwerp is de uitvoering van een ER-indeling vereist. In sommige gevallen wordt de uitvoering van een ER-indeling beïnvloed door de land-/regiocontext van het bedrijf waarbij u momenteel bent aangemeld. U kunt een ER-indeling uitvoeren in het huidige RCS-exemplaar als het bedrijf met de vereiste land- of regiocontext beschikbaar is in RCS. Anders moet u een voltooide versie van de ER-modeltoewijzing en ER-indelingsconfiguraties die het ER-gegevensmodel uploaden naar uw exemplaar van Financiën en vervolgens de ER-indeling uitvoeren in dat exemplaar. Zie [Configuraties importeren uit RCS](rcs-download-configurations.md) voor informatie over het importeren van RCS-configuraties in een exemplaar van Financiën.

## <a name="single-model-mapping-case"></a>Case met één modeltoewijzing

Voer de stappen in [Bijlage 1](#appendix1) van dit onderwerp uit om de vereiste ER-onderdelen te ontwerpen. U beschikt nu over de modeltoewijzingsconfiguratie **Toewijzing (algemeen)** die de modeltoewijzing bevat voor de definitie **Invoerpunt 1**.

![Pagina ER-configuraties](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>De geconfigureerde indeling uitvoeren

1.  Selecteer op de pagina **Configuraties** op het sneltabblad **Versies** de optie **Uitvoeren**.
2.  Selecteer **OK**.

In de webbrowser wordt aangeboden om het tekstbestand te downloaden dat door de uitgevoerde ER-indeling is gegenereerd. Omdat deze indeling is geconfigureerd voor het gebruik van de definitie **Invoerpunt 1** en er momenteel slechts één modeltoewijzing beschikbaar is voor het basismodel dat een toewijzing voor deze definitie bevat, is voor de uitgevoerde ER-indeling het toewijzingsmodel **Toewijzing (algemeen)** van de configuratie **Toewijzing (algemeen)** gebruikt als gegevensbron. Het gedownloade bestand bevat daarom de tekst **Algemene functionaliteit 1**.

## <a name="multiple-shared-model-mappings-case"></a>Case met meerdere gedeelde modeltoewijzingen

Voer de stappen in [Bijlage 2](#appendix2) van dit onderwerp uit om de vereiste ER-onderdelen te ontwerpen. U beschikt nu over de modeltoewijzingsconfiguraties **Toewijzing (algemeen)** en **Aangepaste toewijzing (algemeen)**, die beide de modeltoewijzing voor de definitie **Invoerpunt 1** bevatten.

![Pagina ER-configuraties](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>De geconfigureerde indeling uitvoeren

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor het leren van toewijzingen**.
2.  Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
3.  Selecteer **OK**.

Het uitvoeren van de geselecteerde ER-indeling is mislukt. Er wordt een foutbericht weergegeven dat er meer dan één modeltoewijzing bestaat voor het model **Model voor het leren van toewijzingen** en de definitie **Invoerpunt 1** in de modeltoewijzingsconfiguraties **Toewijzing (algemeen)** en **Aangepaste toewijzing (algemeen)**. Daarnaast wordt u aangeraden een van deze configuraties als de standaardconfiguratie te selecteren.

![Pagina ER-configuraties](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Een standaardtoewijzingsconfiguratie definiëren

Voer deze stappen uit om de modeltoewijzingsconfiguratie **Aangepaste toewijzing (algemeen)** te definiëren als de standaardconfiguratie, zodat de bijbehorende toewijzingen kunnen worden gebruikt als gegevensbronnen voor de ER-indeling **Indeling voor het leren van toewijzingen**.

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Aangepaste toewijzing (algemeen)**.
2.  Selecteer zo nodig **Bewerken** om de huidige pagina gereed te maken voor bewerking.
3.  Stel de optie **Standaard voor modeltoewijzing** in op **Ja**.
4.  Selecteer **Opslaan**.

![Pagina ER-configuraties](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>De geconfigureerde indeling uitvoeren

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor het leren van toewijzingen**.
2.  Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
3.  Selecteer **OK**.

De geselecteerde ER-indeling wordt uitgevoerd. In de webbrowser wordt aangeboden om het tekstbestand te downloaden dat door de uitgevoerde ER-indeling is gegenereerd. Omdat deze indeling is geconfigureerd voor het gebruik van de definitie **Invoerpunt 1** en de modeltoewijzingsconfiguratie **Aangepaste toewijzing (algemeen)** als standaardconfiguratie is geselecteerd, is voor de uitgevoerde ER-indeling het toewijzingsmodel **Kopie van toewijzing (algemeen)** van de configuratie **Aangepaste toewijzing (algemeen)** gebruikt als gegevensbron. Het gedownloade bestand bevat daarom de tekst **Aangepaste algemene functionaliteit 1**.

> [!NOTE]
> Als u het bedrijf wijzigt waarbij u momenteel bent aangemeld en deze ER-indeling opnieuw uitvoert, krijgt u dezelfde inhoud in het gegenereerde bestand omdat de standaardconfiguratie voor ER-modeltoewijzingen geen bedrijfsafhankelijke beperkingen bevat.

## <a name="multiple-mixed-model-mappings-case"></a>Case met meerdere gemengde modeltoewijzingen

Voer de stappen in [Bijlage 3](#appendix3) van dit onderwerp uit om de vereiste ER-onderdelen te ontwerpen. U beschikt nu over de modeltoewijzingsconfiguraties **Toewijzing (algemeen)** **Aangepaste toewijzing (algemeen)** en **Toewijzing van toewijzingsmodel (FR)** die de modeltoewijzing voor de definitie **Invoerpunt 1** bevatten.

U ziet dat versie 1 van de modeltoewijzingsconfiguratie **Toewijzing (FR)** zo is geconfigureerd dat deze alleen van toepassing is op ER-indelingen van het model **Model voor het leren van toewijzingen** die worden uitgevoerd in financiële bedrijven met Frans als land-/regiocontext.

![Pagina ER-configuraties](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>De geconfigureerde indeling uitvoeren

1.  Wijzig het bedrijf in **FRSI**.
2.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor het leren van toewijzingen**.
3.  Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
4.  Selecteer **OK**.

De geselecteerde ER-indeling wordt uitgevoerd. In de webbrowser wordt aangeboden om het tekstbestand te downloaden dat door de uitgevoerde ER-indeling is gegenereerd. Omdat deze indeling is geconfigureerd voor het gebruik van de definitie **Invoerpunt 1** en de modeltoewijzingsconfiguratie **Aangepaste toewijzing (algemeen)** als standaardconfiguratie is geselecteerd, is voor de uitgevoerde ER-indeling het toewijzingsmodel **Kopie van toewijzing (algemeen)** van de configuratie **Aangepaste toewijzing (algemeen)** gebruikt als gegevensbron. Het gedownloade bestand bevat daarom de tekst **Aangepaste algemene functionaliteit 1**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>De voor Frankrijk specifieke toewijzingsconfiguratie definiëren als de standaardconfiguratie

Voer deze stappen uit om de aangepaste modeltoewijzingsconfiguratie **Toewijzing (FR)** te definiëren als standaardconfiguratie. Aangezien deze toewijzing specifiek is voor Frankrijk, wordt dit beschouwd als de standaardtoewijzing tussen alle modeltoewijzingsconfiguraties waarvoor de landcode **FR** is opgegeven in het veld **ISO-codes land/regio**.

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Toewijzing (FR)**.
2.  Selecteer zo nodig **Bewerken** om de huidige pagina gereed te maken voor bewerking.
3.  Stel de optie **Standaard voor modeltoewijzing** in op **Ja**.
4.  Selecteer **Opslaan**.

![Pagina ER-configuraties](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>De geconfigureerde indeling uitvoeren

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor het leren van toewijzingen**.
2.  Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
3.  Selecteer **OK**.

De geselecteerde ER-indeling wordt uitgevoerd. In de webbrowser wordt aangeboden om het tekstbestand te downloaden dat door de uitgevoerde ER-indeling is gegenereerd. Omdat deze indeling is geconfigureerd voor het gebruik van de definitie **Invoerpunt 1** en de modeltoewijzingsconfiguratie **Toewijzing (FR)** als standaardconfiguratie is geselecteerd, is voor de uitgevoerde ER-indeling het toewijzingsmodel **Toewijzing (FR)** van de configuratie **Toewijzing (FR)** gebruikt als gegevensbron. Het gedownloade bestand bevat daarom de tekst **FR-functionaliteit 1**.

> [!NOTE]
> Als u het bedrijf wijzigt waarbij u momenteel bent aangemeld en deze ER-indeling opnieuw uitvoert, is de uitvoer afhankelijk van de land-/regiocontext van het geselecteerde bedrijf.

## <a name="other-model-mapping-cases"></a>Cases met andere modeltoewijzingen

Zoals u hebt gezien, werkt de selectie van een modeltoewijzing voor de uitvoering van een ER-indeling op de volgende manier:

- De modeltoewijzingsdefinitie die een ER-indeling gebruikt, wordt opgegeven (**Invoerpunt 1** in de voorbeelden in dit onderwerp).
- Alle toewijzingsconfiguraties die een toewijzing bevatten met de opgegeven definitie en die voldoen aan alle geconfigureerde land-/regiocontextbeperkingen, kunnen worden gebruikt om de ER-indeling (**Toewijzing (algemeen)**, **Aangepaste toewijzing (algemeen)** en **Toewijzing (FR)** in de voorbeelden in dit onderwerp) uit te voeren.
- Standaardmodeltoewijzingen met land-/regiocontextbeperkingen hebben de hoogste prioriteit voor selectie (**Toewijzing (FR)** in de voorbeelden in dit onderwerp).
- Standaardmodeltoewijzingen zonder land-/regiocontextbeperkingen hebben de op een na hoogste prioriteit voor selectie (**Aangepaste toewijzing (algemeen)** in de voorbeelden in dit onderwerp).
- Een modeltoewijzing met land-/regiocontextbeperkingen heeft een hogere prioriteit voor selectie dan een modeltoewijzing zonder land-/regiocontextbeperkingen.

De volgende tabel biedt informatie over de resultaten van de selectie van modeltoewijzingsselectie voor alle mogelijke cases voor modeltoewijzingsinstellingen:

- In kolom 1 wordt aangegeven of de eerste modeltoewijzing waarvoor geen land-/regiocontextbeperkingen gelden (bijvoorbeeld de gedeelde toewijzing **Toewijzing (algemeen)**) wordt weergegeven en, zo ja, of de optie **Standaard voor modeltoewijzing** is ingesteld op **Ja**.
- In kolom 2 wordt aangegeven of de tweede modeltoewijzing waarvoor geen land-/regiocontextbeperkingen gelden (bijvoorbeeld de gedeelde toewijzing **Algemene toewijzing (algemeen)**) wordt weergegeven en, zo ja, of de optie **Standaard voor modeltoewijzing** is ingesteld op **Ja**.
- In kolom 3 wordt aangegeven of de eerste modeltoewijzing met contextbeperkingen voor land/regio A (bijvoorbeeld de voor Frankrijk specifieke toewijzing **Toewijzing (FR)**) wordt weergegeven en, zo ja, of de optie **Standaard voor modeltoewijzing** is ingesteld op **Ja**.
- In kolom 4 wordt aangegeven of de tweede modeltoewijzing met contextbeperkingen voor land/regio A wordt weergegeven en, zo ja, of de optie **Standaard voor modeltoewijzing** is ingesteld op **Ja**.
- In kolom 5 wordt het resultaat weergegeven van de selectie van een modeltoewijzing voor de uitvoering van een ER-indeling onder controle van een bedrijf dat een context van land/regio A heeft.
- In kolom 6 wordt het resultaat weergegeven van de selectie van een modeltoewijzing voor de uitvoering van een ER-indeling onder controle van een bedrijf dat een context van land/regio B heeft.

In de tabel duidt een plusteken (+) de aanwezigheid van een modeltoewijzingsconfiguratie aan in het huidige exemplaar van de Microsoft Azure-service die wordt gebruikt om een ER-indeling (Finance of RCS) uit te voeren.

| Doos | Modeltoewijzing 1 zonder land-/regiocontext (MM1) | Modeltoewijzing 2 zonder land-/regiocontext (MM2) | Modeltoewijzing 1 met land-/regiocontext A (MM1A) | Modeltoewijzing 2 met land-/regiocontext A (MM2A) | Uitvoeren onder controle van een bedrijf met land-/regiocontext A | Uitvoeren onder controle van een bedrijf met land-/regiocontext B |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Fout (ontbrekende toewijzing)   | Fout (ontbrekende toewijzing)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Fout (meerdere toewijzingen) | Fout (meerdere toewijzingen)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Fout (meerdere toewijzingen) | MM1                        |
|     6   |     +   | standaard |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | standaard |         | MM1A                      | MM1                        |
|     8   |     +   |         | standaard |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | standaard | standaard | Fout (meerdere toewijzingen) | MM1                        |
|    10   | standaard |         |         |         | MM1                       | MM1                        |
|    11   | standaard |    +    |         |         | MM1                       | MM1                        |
|    12   | standaard |         |    +    |         | MM1                       | MM1                        |
|    13   | standaard | standaard |         |         | Fout (meerdere toewijzingen) | Fout (meerdere toewijzingen)  |
|    14   | standaard |         | standaard |         | MM1A                      | MM1                        |
|    15   | standaard |         | standaard | standaard | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | standaard | standaard | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Informatie over de gebruikte toewijzing voor het uitvoeren van een ER-indeling

### <a name="configure-er-user-parameters"></a>ER-gebruikersparameters configureren

1.  Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **CONFIGURATIES** de optie **Gebruikersparameters**.
2.  Stel de optie **Uitvoeren in foutoplossingsmodus** in op **Ja**.
4.  Selecteer **OK**.

### <a name="run-the-configured-format"></a>De geconfigureerde indeling uitvoeren

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor het leren van toewijzingen**.
2.  Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
3.  Selecteer **OK**.

### <a name="review-the-er-debug-log"></a>Het ER-logboek voor foutopsporing weergeven

1.  Ga in het navigatievenster naar **Modules \> Organisatiebeheer \> Elektronische rapportage \> Foutopsporingslogboeken voor configuraties**.
2.  Selecteer de knop **Deze pagina opnieuw laden**.

![De pagina ER-uitvoeringslogboeken](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Voor de uitgevoerde ER-indeling is een nieuwe record toegevoegd aan het ER-logboek voor foutopsporing. Omdat het veld **Niveau** van deze record is ingesteld op **Info**, is de record informatief. Omdat het veld Indelingscomponent is ingesteld op **Configuratie voor toewijzing**, geeft de record u informatie over een modeltoewijzing die is gebruikt tijdens het uitvoeren van de ER-indeling **Indeling voor het leren van toewijzingen** (geselecteerd in het veld **Configuratienaam**). In het veld **Gegenereerde tekst** wordt aangegeven dat de toewijzingscomponent **Toewijzing (FR)** die zich in de configuratie **Toewijzing (FR)** bevindt, is gebruikt om dit rapport uit te voeren.

## <a name="appendix-1"></a><a name="appendix1"></a> Bijlage 1

### <a name="configure-a-sample-data-model"></a>Een voorbeeldgegevensmodel configureren

Meld u aan bij uw RCS-exemplaar.

In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc. Eerst moet u in RCS de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) uitvoeren.

#### <a name="create-an-er-data-model-configuration"></a>Een ER-gegevensmodelconfiguratie maken

1.  Selecteer **Elektronische aangifte** in het standaarddashboard.
2.  Selecteer de tegel **Rapportageconfiguraties**.
3.  Selecteer **Configuratie maken** op de pagina **Configuraties**.
4.  Voer in het vervolgkeuzemenu in het veld **Naam** de tekst **Model voor het leren van toewijzingen** in.
5.  Selecteer **Configuratie maken**.
6.  Selecteer het sneltabblad **Configuratieonderdelen**.

U ziet dat conceptversie 1 van deze ER-configuratie kan worden bewerkt. Deze versie bevat het gegevensmodelonderdeel.

#### <a name="design-a-sample-data-model"></a>Een voorbeeldgegevensmodel ontwerpen

1.  Selecteer **Ontwerper** op de pagina **Configuraties**.
2.  Selecteer **Nieuw**.
3.  Voer in het vervolgkeuzemenu in het veld **Naam** de tekst **Invoerpunt 1** in.
4.  Selecteer **Toevoegen**.
5.  Selecteer **Nieuw**.
6.  Voer in het vervolgkeuzemenu in het veld **Naam** de tekst **Beschrijving van functionaliteit** in.
7.  Selecteer **Toevoegen**.
8.  Selecteer **Nieuw**.
9.  Selecteer in het vervolgkeuzemenu in de veldgroep **Nieuw knooppunt** de optie **Modelbasis**.
10. Voer in het veld **Naam** de waarde **Invoerpunt 2** in.
11. Selecteer **Invoerpunt 2**.
12. Selecteer **Toevoegen**.
13. Selecteer **Nieuw**.
14. Voer in het vervolgkeuzemenu in het veld **Naam** de tekst **Beschrijving van functionaliteit** in.
15. Selecteer **Toevoegen**.

    ![Pagina voor ontwerper van ER-gegevensmodel](./media/RCS-Context-specific-mapping-Model.PNG)

16. Selecteer **Opslaan**.
17. Sluit de pagina.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>De gewijzigde versie van de modelconfiguratie voltooien

1.  Selecteer op de pagina **Configuraties** op het sneltabblad **Versies** de optie **Status wijzigen**.

    > Wijzig de status van de ontworpen modelconfiguratie van **Concept** in **Voltooid**, zodat deze kan worden gebruikt om de vereiste modeltoewijzingen en -indelingen te ontwerpen.

2.  Selecteer **Voltooien**.
3.  Selecteer **OK**.

De gemaakte configuratie wordt opgeslagen als voltooide versie 1.

### <a name="configure-a-sample-model-mapping"></a>Een voorbeeldmodeltoewijzing configureren

#### <a name="create-an-er-model-mapping-configuration"></a>Een ER-modeltoewijzingsconfiguratie maken

1.  Selecteer **Configuratie maken** op de pagina **Configuraties**.
2.  Ga naar het vervolgkeuzemenu en selecteer in de veldgroep **Nieuw** de optie **Modeltoewijzing gebaseerd op gegevensmodel Model voor het leren van toewijzingen**.
3.  Voer in het veld **Naam** de waarde **Toewijzing (algemeen)** in.
4.  Selecteer **Invoerpunt 1** in het veld **Definitie gegevensmodel**.
5.  Selecteer **Configuratie maken**.

U ziet dat conceptversie 1 van deze ER-configuratie kan worden bewerkt. Deze versie bevat het gegevenstoewijzingsmodelonderdeel.

#### <a name="design-a-sample-model-mapping"></a>Een voorbeeldmodeltoewijzing ontwerpen

1.  Selecteer **Ontwerper** op de pagina **Configuraties**.

    De modeltoewijzing van het richtingtype **Naar model** is automatisch toegevoegd aan dit onderdeel voor de definitie **Invoerpunt 1**.
    
2.  Selecteer **Ontwerper** om te beginnen met het bewerken van de toegevoegde modeltoewijzing.
3.  Selecteer **Bewerken** in de sectie **Gegevensmodel**.
4.  Typ in het veld **Formule** de tekst **Algemene functionaliteit 1**.
5.  Selecteer **Opslaan**.
6.  Sluit de pagina **Formuleontwerper**.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Selecteer **Opslaan**.
8.  Sluit de pagina **Ontwerper modeltoewijzing**.
9.  Selecteer **Nieuw**.
10. Selecteer **Invoerpunt 2** in het veld **Definitie**.
11. Voer in het veld **Naam** de waarde **Toewijzing (algemeen) 2** in.
12. Selecteer **Ontwerper**.
13. Selecteer **Bewerken** in de sectie **Gegevensmodel**.
14. Typ in het veld **Formule** de tekst **Algemene functionaliteit 2**.
15. Selecteer **Opslaan**.
16. Sluit de pagina **Formuleontwerper**.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Selecteer **Opslaan**.
18. Sluit de pagina **Ontwerper modeltoewijzing**.

    ![De pagina ER-modeltoewijzingen ontwerpen](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Sluit de pagina **Modeltoewijzingen**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>De gewijzigde versie van de modeltoewijzingsconfiguratie voltooien

1.  Selecteer op de pagina **Configuraties** op het sneltabblad **Versies** de optie **Status wijzigen**.

    > Wijzig de status van de ontworpen modeltoewijzingsconfiguratie van **Concept** in **Voltooid**, zodat deze kan worden gebruikt door ER-indelingen.

2.  Selecteer **Voltooien**.
3.  Selecteer **OK**.

De gemaakte configuratie wordt opgeslagen als voltooide versie 1.

### <a name="configure-a-sample-format"></a>Een voorbeeldindeling configureren

#### <a name="create-an-er-format-configuration"></a>Een ER-indelingsconfiguratie maken

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Model voor het leren van toewijzingen**.
2.  Selecteer **Configuratie maken**.
3.  Ga naar het vervolgkeuzemenu en selecteer in de veldgroep **Nieuw** de optie **Indeling gebaseerd op gegevensmodel Model voor het leren van toewijzingen**.
4.  Voer in het veld **Naam** de tekst **Indeling voor het leren van toewijzingen** in.
5.  Selecteer **Invoerpunt 1** in het veld **Definitie gegevensmodel**.
6.  Selecteer **Configuratie maken**.

U ziet dat conceptversie 1 van deze ER-configuratie kan worden bewerkt. Deze versie bevat het indelingsonderdeel.

#### <a name="design-a-sample-format"></a>Een voorbeeldindeling ontwerpen

1.  Selecteer **Ontwerper** op de pagina **Configuraties**.
2.  Selecteer **Basis toevoegen**.
3.  Selecteer in de groep **Tekst** het item **Tekenreeks**.
4.  Selecteer **OK**.

#### <a name="bind-format-elements-to-a-data-source"></a>Indelingselementen aan een gegevensbron binden

1.  Vouw op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** de modelgegevensbron uit.
2.  Selecteer het veld **Beschrijving van functionaliteit**.
3.  Selecteer **Binden**.

    ![Pagina voor ontwerper van ER-indeling](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Selecteer **Opslaan**.
5.  Sluit de pagina.

## <a name="appendix-2"></a><a name="appendix2"></a> Bijlage 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Een voorbeeldmodeltoewijzing configureren voor algemene aanpassing

Mogelijk wilt u een modeltoewijzing aanpassen die een configuratieprovider (partner) aan u heeft verstrekt om vervolgens de aangepaste versie als gegevensbron te gebruiken voor uw ER-indelingen. In dat geval moet u een aangepaste ER-modeltoewijzingsconfiguratie maken om de vereiste wijzigingen aan te brengen in bestaande modeltoewijzingen. In de procedures in deze bijlage wordt de modeltoewijzing **Toewijzing (algemeen)** als voorbeeld gebruikt.

#### <a name="create-an-er-model-mapping-configuration"></a>Een ER-modeltoewijzingsconfiguratie maken

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Toewijzing (algemeen)**.
2.  Selecteer **Configuratie maken**.
3.  Selecteer in het vervolgkeuzemenu in de veldgroep **Nieuw** de optie **Afleiden van naam: Toewijzing (algemeen), Litware, Inc.**
4.  Voer in het veld **Naam** de waarde **Aangepaste toewijzing (algemeen)** in.
5.  Selecteer **Configuratie maken**.

U ziet dat conceptversie 1 van deze ER-configuratie kan worden bewerkt.

#### <a name="design-a-sample-model-mapping"></a>Een voorbeeldmodeltoewijzing ontwerpen

1.  Selecteer **Ontwerper** op de pagina **Configuraties**.

    > De modeltoewijzingen van de basisconfiguratie zijn automatisch naar deze configuratie gekopieerd.

2.  Selecteer de toewijzing **Kopie van toewijzing (algemeen)**.
3.  Selecteer **Ontwerper**.
4.  Selecteer **Bewerken** in de sectie **Gegevensmodel**.
5.  Typ in het veld **Formule** de tekst **Aangepaste algemene functionaliteit 1**.
6.  Selecteer **Opslaan**.
7.  Sluit de pagina.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Selecteer **Opslaan**.
9.  Sluit de pagina.
10. Selecteer de toewijzing **Kopie van toewijzing (algemeen) 2**.
11. Selecteer **Ontwerper**.
12. Selecteer **Bewerken** in de sectie **Gegevensmodel**.
13. Typ in het veld **Formule** de tekst **Aangepaste algemene functionaliteit 2**.
14. Selecteer **Opslaan**.
15. Sluit de pagina.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Selecteer **Opslaan**.
17. Sluit de pagina.

    ![De pagina ER-modeltoewijzingen ontwerpen](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Sluit de pagina.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>De gewijzigde versie van de modeltoewijzingsconfiguratie voltooien

1.  Selecteer op de pagina **Configuraties** op het sneltabblad **Versies** de optie **Status wijzigen**.

    > Wijzig de status van de ontworpen modeltoewijzingsconfiguratie van **Concept** in **Voltooid**, zodat deze kan worden gebruikt door ER-indelingen.

2.  Selecteer **Voltooien**.
3.  Selecteer **OK**.

De gemaakte configuratie wordt opgeslagen als voltooide versie 1.

## <a name="appendix-3"></a><a name="appendix3"></a> Bijlage 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Een voorbeeldmodeltoewijzing configureren voor land-/regiospecifieke aanpassing

Voor sommige ER-indelingen kunnen er land-/regiospecifieke vereisten zijn met betrekking tot het voorbereiden van gegevens. In dit geval kunt u een afzonderlijke ER-modeltoewijzingsconfiguratie beheren en de implementatie van deze land-/regiospecifieke vereisten van de algemene implementatie isoleren. Voor de procedures in deze bijlage worden de ER-indeling **Indeling voor het leren van toewijzingen** en specifieke Franse vereisten als voorbeeld gebruikt.

#### <a name="create-an-er-model-mapping-configuration"></a>Een ER-modeltoewijzingsconfiguratie maken

Maak eerst een nieuwe ER-modeltoewijzingsconfiguratie om de land-/regiospecifieke vereisten te implementeren. Gebruik de aangepaste ER-modeltoewijzingsconfiguratie als basis.

1.  Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Aangepaste toewijzing (algemeen)**.
2.  Selecteer **Configuratie maken**.
3.  Selecteer in het vervolgkeuzemenu in de veldgroep **Nieuw** de optie **Afleiden van naam: Algemene toewijzing (algemeen), Litware, Inc.**
4.  Voer in het veld **Naam** de waarde **Toewijzing (FR)** in.
5.  Selecteer **Configuratie maken**.

U ziet dat conceptversie 1 van deze ER-configuratie kan worden bewerkt.

#### <a name="design-a-sample-model-mapping"></a>Een voorbeeldmodeltoewijzing ontwerpen

1.  Selecteer **Ontwerper** op de pagina **Configuraties**.

    > De modeltoewijzingen van de basisconfiguratie zijn automatisch naar deze configuratie gekopieerd.

2.  Selecteer de toewijzing **Kopie van toewijzing (algemeen)**.
3.  Wijzig de naam in **Toewijzing (FR)**.
4.  Selecteer **Ontwerper**.
5.  Selecteer **Bewerken** in de sectie **Gegevensmodel**.
6.  Typ in het veld **Formule** de tekst **FR-functionaliteit 1**.
7.  Selecteer **Opslaan**.
8.  Sluit de pagina.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Selecteer **Opslaan**.
10. Sluit de pagina.
11. Selecteer de toewijzing **Kopie van toewijzing (algemeen) 2**.
12. Wijzig de naam in **Toewijzing (FR) 2**.
13. Selecteer **Ontwerper**.
14. Selecteer **Bewerken** in de sectie **Gegevensmodel**.
15. Typ in het veld **Formule** de tekst **FR-functionaliteit 2**.
16. Selecteer **Opslaan**.
17. Sluit de pagina.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Selecteer **Opslaan**.
19. Sluit de pagina.

    ![De pagina ER-modeltoewijzingen ontwerpen](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Sluit de pagina.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Land-/regiocontextbeperkingen opgeven die u wilt gebruiken

1.  Selecteer op de pagina **Configuraties** op het sneltabblad **ISO-land-/regiocodes** de optie **Nieuw**.
2.  Selecteer **FR** in het veld **ISO**.
3.  Selecteer **Opslaan**.

U moet u aanmelden bij een specifiek bedrijf in Finance om een ER-indeling uit te voeren. Daarom kan dit bedrijf worden beschouwd als een partij die zowel de uitvoering van ER-indelingen als de selectie van de juiste ER-modeltoewijzing van het ER-basisgegevensmodel beheert. Door de landcode **FR** toe te voegen, geeft u op dat deze modeltoewijzing alleen beschikbaar is voor selectie met een ER-indeling van het basisgegevensmodel wanneer die indeling wordt uitgevoerd onder het beheer van een bedrijf met Franse land-/regiocontext.

U kunt meerdere land-/regiocodes toevoegen voor één versie van een ER-modeltoewijzingsconfiguratie. Op deze manier kunnen modeltoewijzingen in die modeltoewijzingsconfiguratie worden gebruikt voor een ER-indeling die wordt uitgevoerd onder het beheer van bedrijven met een andere land- of regiocontext.

De lijst met land-/regiocodes wordt opgegeven voor elke versie van een ER-modeltoewijzingsconfiguratie en kan per versie verschillen.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>De gewijzigde versie van de modeltoewijzingsconfiguratie voltooien

1.  Selecteer op de pagina **Configuraties** op het sneltabblad **Versies** de optie **Status wijzigen**.

    > Wijzig de status van de ontworpen modeltoewijzingsconfiguratie van **Concept** in **Voltooid**, zodat deze kan worden gebruikt door ER-indelingen.

2.  Selecteer **Voltooien**.
3.  Selecteer **OK**.

De gemaakte configuratie wordt opgeslagen als voltooide versie 1.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[ER-modeltoewijzing in afzonderlijke ER-configuraties beheren](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Land-/regiocontext toepassen](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Ik heb twee gedeelde ER-modeltoewijzingsconfiguraties geconfigureerd in RCS en een van deze configuraties gemarkeerd als standaardconfiguratie voor modeltoewijzing. Ik heb een ER-indeling uitgevoerd die voor dezelfde configuratie voor ER-basisgegevensmodellen is gemaakt, om modeltoewijzingen te testen. Ik heb vervolgens de volledige ER-oplossing (ER-gegevensmodel, twee ER-modeltoewijzingsconfiguraties en een ER-indelingsconfiguratie) in Finance geïmporteerd. Waarom ontvang ik een foutbericht wanneer ik dezelfde ER-indeling probeer uit te voeren in Finance?
De standaardinstelling voor modeltoewijzing is omgevingsspecifiek. Deze wordt geconfigureerd in RCS, maar wordt niet geëxporteerd naar Finance. Als u deze ER-indeling wilt uitvoeren, moet u een van de ER-modeltoewijzingsconfiguraties ook als de standaardconfiguratie voor modeltoewijzing in Finance markeren.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Ik heb één modeltoewijzing geconfigureerd als gedeelde modeltoewijzing en de conceptversie ervan voltooid. Ik heb vervolgens een nieuwe configuratie voor modeltoewijzing toegevoegd voor hetzelfde gegevensmodel en deze geconfigureerd als Frans-specifiek. Waarom wordt de gedeelde modeltoewijzing geselecteerd wanneer ik een ER-indeling uitvoer, hoewel deze ER-indeling gebruikmaakt van de juiste basisdefinitie en de uitvoering plaatsvindt onder beheer van het bedrijf met Franse land-/regiocontext?
Zorg dat de configuratie van de gedeelde modeltoewijzing niet is gemarkeerd als standaardconfiguratie voor modeltoewijzing. Anders krijgt de toewijzing een hogere prioriteit tijdens de toewijzingsselectie. Zorg er ook voor dat de specifieke Franse configuratie voor modeltoewijzing wordt overwogen wanneer een toewijzing wordt geselecteerd tijdens het uitvoeren van een ER-indeling. De configuratie van een ER-modeltoewijzing kan alleen worden geselecteerd als aan ten minste één van de volgende voorwaarden wordt voldaan:
- Minimaal één versie van de ER-modeltoewijzingsconfiguratie heeft de status **Voltooid** of **Gedeeld**. In dit geval wordt de versie met het hoogste versienummer gebruikt voor het uitvoeren van de ER-indeling.
- De optie **Concept uitvoeren** voor de configuratie van de ER-modeltoewijzing wordt ingeschakeld. In dit geval wordt de versie met de status **Concept** gebruikt voor het uitvoeren van de ER-indeling.
> De optie **Concept uitvoeren** wordt beschikbaar op de pagina **Configuraties** voor elke configuratie van ER-modeltoewijzingen wanneer de ER-gebruikersparameter **Instelling uitvoeren** is ingeschakeld.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]