---
title: Ondersteuning van parameteraanroepen voor ER-gegevensbronnen van het type Berekend veld
description: Dit onderwerp biedt informatie over het gebruik van het type Berekend veld voor ER-gegevensbronnen.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c68f0a0e2481c69add8c50a1581466ad0b1483c0
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759906"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Ondersteuning van parameteraanroepen voor ER-gegevensbronnen van het type Berekend veld

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een ER-gegevensbron (elektronische rapportage) kunt ontwerpen met behulp van het type **Berekend veld**. Deze gegevensbron kan een ER-expressie bevatten die bij uitvoering kan worden bestuurd door de waarden van de parameterargumenten die zijn geconfigureerd in een binding die deze gegevensbron aanroept. Door parameteraanroepen voor een dergelijke gegevensbron te configureren, kunt u één gegevensbron in veel bindingen opnieuw gebruiken. Dit vermindert het totale aantal gegevensbronnen dat moet worden geconfigureerd in ER-modeltoewijzingen of ER-indelingen. Het vereenvoudigt ook het geconfigureerde ER-onderdeel, wat de onderhoudskosten en de kosten van gebruik door andere gebruikers verlaagt.

## <a name="prerequisites"></a>Vereisten
Om de voorbeelden in dit onderwerp te kunnen voltooien, moet u toegang tot het volgende hebben:

- Maak gebruik van een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Toegang tot RCS (Regulatory Configuration Services) die zijn ingericht voor dezelfde tenant als Finance and Operations voor een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

U moet ook de volgende bestanden downloaden en lokaal opslaan.

| **Inhoud**                           | **Bestandsnaam**                                        |
|---------------------------------------|------------------------------------------------------|
| Voorbeeldconfiguratie van model voor ER-gegevens    | [Model voor het leren van parameteraanroepen.versie.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| Voorbeeldconfiguratie van ER-metagegevens      | [Metagegevens voor het leren van parameteraanroepen.versie.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| Voorbeeldconfiguratie van ER-modeltoewijzing | [Toewijzing voor het leren van parameteraanroepen.versie.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| Voorbeeldconfiguratie van ER-indeling        | [Indeling voor het leren van parameteraanroepen.versie.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a>Meld u aan bij uw RCS-exemplaar
In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc. Eerst moet u in RCS de stappen uitvoeren in de procedure [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md):

1. Selecteer **Elektronische aangifte** in het standaarddashboard.
2. Selecteer **Rapportageconfiguraties**.
3. Importeer de gedownloade configuraties naar RCS in deze volgorde: gegevensmodel, metagegevens, modeltoewijzing, indeling. Voer de volgende stappen uit voor elke ER-configuratie:

    1. Selecteer **Uitwisselen**.
    2. Selecteer **Laden uit XML-bestand**.
    3. Selecteer **Bladeren** en selecteer vervolgens de vereiste ER-configuratie in XML-indeling.
    4. Selecteer **OK**.

## <a name="review-the-provided-er-solution"></a>De geleverde ER-oplossing controleren

### <a name="review-model-mapping"></a>Modeltoewijzing controleren

1. Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.
2. Selecteer **Toewijzing voor het leren van parameteraanroepen**.
3. Selecteer **Ontwerper**.
4. Selecteer **Ontwerper**.  
   
    Deze ER-modeltoewijzing is ontworpen om het volgende te doen:

    - Het ophalen van de lijst met btw-codes (**Btw**-gegevensbron) in de tabel **TaxTable**.
    - Het ophalen van de lijst met btw-transacties (**Trans**-gegevensbron) in de tabel **TaxTrans**:
    
        - Het groeperen van opgehaalde trans acties (**GR**-gegevensbron) op btw-code.
        - Het berekenen voor gegroepeerde transacties na geaggregeerde waarden per btw-code:

            - Het optellen van btw-basiswaarden.
            - Het optellen van btw-waarden.
            - Het bepalen van het minimale toegepaste belastingtarief.

    Met de modeltoewijzing in deze configuratie wordt het basisgegevensmodel geïmplementeerd voor elke ER-indeling die voor dit model is gemaakt en in Finance and Operations wordt uitgevoerd. Dat betekent dat de inhoud van de gegevensbronnen **Btw** en **GR** worden weergegeven voor ER-indelingen zoals abstracte gegevensbronnen.

    ![De pagina Ontwerper modeltoewijzingen met Btw- en GR-gegevensbronnen](media/er-calculated-field-type-01.png)

5.  Sluit de pagina **Ontwerper modeltoewijzing**.
6.  Sluit de pagina **Modeltoewijzing**.

### <a name="review-format"></a>Indeling controleren

1. Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.
2. Selecteer **Indeling voor het leren van parameteraanroepen**.
3. Selecteer **Ontwerper**. Deze ER-indeling is ontworpen om het volgende te doen:

    - Het genereren van een belastingaangifte in XML-indeling.
    - Het opgeven van de volgende belastingniveaus in de belastingaangifte: normaal, verlaagd en geen.
    - Het opgeven van meerdere details voor elk belastingniveau, met een verschillend aantal details op elk niveau.

    ![Pagina Indelingsontwerper](media/er-calculated-field-type-02.png)

4. Selecteer **Toewijzing**.
5. Vouw de items **Model**, **Gegevens** en **Overzicht** uit. 

    Het berekende veld **Model.Data.Summary.Level** bevat de expressie die de code van het belastingniveau (**Normaal**, **Verlaagd**, **Geen** of **Overige**) als een tekstwaarde retourneert voor elke belastingcode die in runtime kan worden opgehaald uit de gegevensbron **Model.Data.Summary**.

    ![Pagina Indelingsontwerper met details van het gegevensmodel Model voor het leren van parameteraanroepen](media/er-calculated-field-type-03.png)

6. Vouw het item **Model**.**Data2** uit.
7. Vouw het item **Model**.**Data2.Summary2** uit.
   
    De gegevensbron **Model**.**Data2.Summary2** is geconfigureerd om de transactiegegevens van de gegevensbron **Model.Data.Summary** te groeperen op belastingniveau (geretourneerd door het berekende veld **Model.Data.Summary.Level**) en de aggregaties te berekenen.

    ![Pagina Indelingsontwerper met details van de gegevensbron Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. Controleer de berekende velden **Model**.**Data2.Level1**, **Model**.**Data2.Level2** en **Model**.**Data2.Level3**. Deze berekende velden worden gebruikt om de lijst met **Model**.**Data2. Summary2**-records te filteren en alleen de records weer te geven die een bepaald belastingniveau vertegenwoordigen.
9. Sluit de pagina **Indelingsontwerper**.

## <a name="create-a-derived-format"></a>Een afgeleide indeling maken
U kunt de opgegeven indeling verbeteren door één berekend veld toe te voegen om het vereiste belastingniveau te filteren in plaats van de drie velden **Model**.**Data2.Level1**, **Model**.**Data2.Level2** en **Model**.**Data2.Level3** te gebruiken. Het vereiste belastingniveau kan worden opgegeven op de locatie waar dit nieuwe berekende veld wordt aangeroepen.

1. Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.
2. Selecteer **Indeling voor het leren van parameteraanroepen**.
3. Selecteer **Configuratie maken**.
4. Selecteer **Afleiden van naam: Indeling voor het leren van parameteraanroepen, Microsoft**.
5. Voer in het veld **Naam** de tekst **Indeling voor het leren van parameteraanroepen** in.
6. Selecteer **Configuratie maken**.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Een berekend parameterveld configureren dat een lijst met records retourneert

### <a name="start-adding-a-new-calculated-field"></a>Het toevoegen van een nieuw berekend veld starten

1. Selecteer **Ontwerper**.
2. Selecteer **Uitvouwen/Samenvouwen** om alle indelingsitems uit te vouwen.
3. Selecteer **Toewijzing**.
4. Vouw het item **Model** uit.
5. Selecteer het item **Model.Data2**.
6. Selecteer **Toevoegen**.
7. Selecteer **Functies\\Berekend veld**.
8. Voer in het veld **Naam** de tekst **Niveaus** in.
9. Selecteer **Formule bewerken**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Een parameter definiëren voor het toevoegen van een berekend veld

1. Selecteer **Parameters**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Naam** de tekst **Belastingniveau** in.
4. Selecteer in het veld **Type** de optie **Tekenreeks**.

    Alleen primitieve gegevenstypen kunnen worden gebruikt om het type argument van de parameter op te geven. Daarom kunnen de typen **Lijst met records**, **Record** en **Opsomming** niet voor dit doel worden gebruikt.

    Het maximum aantal parameters dat kan worden opgegeven voor één berekend veld is 8.

    ![Lijst met parametergegevensbronnen](media/er-calculated-field-type-05.png)

5. Selecteer **OK**.

Door deze parameter toe te voegen, geeft u de voorwaarde op die moet gelden om dit berekend veld aan te roepen. Wanneer u dit berekend veld aanroept, moet u het argument van de parameter **Belastingniveau** opgeven als een waarde met de indeling **Tekenreeks**.

   Zorg dat u alleen parameters definieert voor de berekende velden die zich in een container **(** Lijst met records, **Record** of **Container**) bevinden.

   De geconfigureerde parameter is beschikbaar in de lijst met gegevensbronnen voor dit berekend veld. U kunt de parameter toevoegen aan de geconfigureerde expressie door **Gegevensbron toevoegen** te selecteren.

   ![Gegevensbronvelden](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Een expressie definiëren voor het toevoegen van een berekend veld

1. Voer in het veld **Formule** het volgende in: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Selecteer de parameter **Belastingniveau** in de lijst met gegevensbronnen.
3. Selecteer **Gegevensbron toevoegen**.
4. Maak de expressie in het veld **Formule** als volgt af:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Belastingniveau')**

5. Selecteer **Opslaan**.

    ![Informatie Gegevensbronveld](media/er-calculated-field-type-07.png)

6. Sluit de pagina **Formuleontwerper**.

### <a name="finish-adding-a-new-calculated-field"></a>Het toevoegen van een nieuw berekend veld voltooien

- Selecteer **OK**.

Op de pagina **Indelingsontwerper** heeft het geconfigureerde berekende parameterveld **Niveaus** een argument van het type **Tekenreeks** nodig.

![Uitgevouwen lijst met berekende veldniveaus](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Het geconfigureerde berekende veld gebruiken voor het binden van indelingselementen

1. Selecteer **Model.Data2.Levels** om het geconfigureerde berekende veld te selecteren.
2. Selecteer het indelingselement **Statement.Taxation.Regular**.
3. Selecteer **Binden**.
4. Selecteer **Ja** om de vervanging van de op dat moment gebruikte gegevensbron, **Niveau1**, door de nieuwe gegevensbron **Niveaus** in alle geneste opmaakelementen van het geselecteerde indelingselement te bevestigen.

    Toegepaste binding is opgebouwd als een aanroep van het berekende parameterveld. De naam van het gebonden indelingselement wordt onder de volgende voorwaarden standaard gebruikt als argument voor het berekende parameterveld:

      - Het berekende veld is geconfigureerd voor het gebruik van één parameter.
      - Het gegevens type van deze parameter is gedefinieerd als **Tekenreeks**.

    Wanneer de naam van het gebonden indelingselement leeg is, wordt de naam van de gegevensbron van dit element gebruikt bij toegepaste binding.

5. Selecteer het indelingselement **Statement.Taxation.Reduced**.
6. Selecteer **Binden**.
7. Selecteer **Ja** om de vervanging van de op dat moment gebruikte gegevensbron, **Niveau2**, door de nieuwe gegevensbron **Niveaus** in alle geneste opmaakelementen onder het geselecteerde indelingselement te bevestigen.
8. Selecteer het indelingselement **Statement.Taxation.None**.
9. Selecteer **Binden**.
10. Selecteer **Ja** om de vervanging van de op dat moment gebruikte gegevensbron, **Niveau3**, door de nieuwe gegevensbron **Niveaus** in alle geneste opmaakelementen onder het geselecteerde indelingselement te bevestigen.

   Wanneer u het argument van het berekende parameterveld voor het XML-element dat het belastingniveau vertegenwoordigt (bijvoorbeeld **Model.Data2.Levels("Verlaagd")** opgeeft als tekstwaarde), hoeft u dit niet meer te doen voor geneste XML-kenmerken. De bindingen nemen automatisch de waarde over van het argument dat is gedefinieerd op het bovenliggende niveau (**Model.Data2.Levels.aggregated.Base**, niet **Model.Data2.Levels("Verlaagd").aggregated.Base**).

Terugkerende aanroepen van berekende parametervelden worden niet ondersteund.

U kunt **Formule bewerken** selecteren en het standaard toegepaste argument van het berekende parameterveld in de geselecteerde binding wijzigen. Als dit argument ontbreekt, kan dit in runtime leiden tot fouten. Gebruikers krijgen een melding over een dergelijke situatie wanneer de huidige indeling wordt gevalideerd.

![Melding met validatiewaarschuwing](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Een berekend parameterveld configureren dat een record retourneert
Wanneer een berekend parameterveld een record retourneert, moet u binding van afzonderlijke velden van deze record ondersteunen om elementen in te delen. In dergelijke gevallen is er geen bovenliggende binding die de waarde van een argument bevat voor het aanroepen van een berekend parameterveld. Deze waarde moet worden gedefinieerd in de binding van het veld van één record.

### <a name="start-adding-a-new-calculated-field"></a>Het toevoegen van een nieuw berekend veld starten

1. Selecteer het item **Model.Data2**.
2. Selecteer **Toevoegen**.
3. Selecteer **Functies\\Berekend veld**.
4. Voer in het veld **Naam** **LevelRecord** in.
5. Selecteer **Formule bewerken**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Een parameter definiëren voor het toevoegen van een berekend veld

1. Selecteer **Parameters**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Naam** de tekst **Belastingniveau** in.
4. Selecteer in het veld **Type** de optie **Tekenreeks**.
5. Selecteer **OK**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Een expressie definiëren voor het toevoegen van een berekend veld

1. Voer in het veld **Formule** het volgende in:  
    
    **FIRSTORNULL(\@.Levels(**

2. Selecteer de parameter **Belastingniveau**.
3. Selecteer **Gegevensbron toevoegen**.
4. Voeg in het veld **Formule** de tekst **'Belastingniveau'))** toe aan wat u in stap 1 hebt ingevoerd om de expressie als volgt te voltooien:  
    
    **FIRSTORNULL(\@.Levels('Belastingniveau'))**

5. Selecteer **Opslaan**.
6. Sluit de pagina **Formuleontwerper**.

### <a name="finish-adding-a-new-calculated-field"></a>Het toevoegen van een nieuw berekend veld voltooien

-   Selecteer **OK**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Het geconfigureerde berekende veld gebruiken om indelingselementen te binden

1. Vouw **Model.Data2.LevelRecord** uit om het geconfigureerde berekende veld te selecteren.
2. Vouw de container **Model.Data2.LevelRecord.aggregated** van het geconfigureerde berekende veld uit.
3. Selecteer het veld **Model.Data2.LevelRecord.aggregated.Base**.
4. Selecteer het indelingselement **Statement.Taxation.None**.
5. Selecteer **Verbinding verbreken**.
6. Selecteer het indelingselement **Statement.Taxation.None.Base**.
7. Selecteer **Binden**.
8. Selecteer **Formule bewerken**.
9. Wijzig de expressie in **Model.Data2.LevelRecord("Geen").aggregated.Base**.

![Bijgewerkte expressie](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Ongebruikte berekende velden verwijderen

1. Selecteer **Model.Data2.Level1**.
2. Selecteer **Verwijderen**.
3. Selecteer **Model.Data2.Level2**.
4. Selecteer **Verwijderen**.
5. Selecteer **Model.Data2.Level3**.
6. Selecteer **Verwijderen**.
7. Selecteer **Opslaan**.

  > [!NOTE]
  > U hebt hetzelfde berekende veld **Model.Data2.Levels** een aantal keer gebruikt in indelingsbindingen. Het is veel eenvoudiger om één berekend veld te gebruiken en te onderhouden in plaats van dit voor meerdere soortgelijke velden te doen.

8. Sluit de pagina **Indelingsontwerper**.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Aangepaste versie van een afgeleide indeling voltooien

1. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen**.
2. Selecteer **Voltooien**.

## <a name="export-completed-version-of-a-derived-format"></a>Voltooide versie van een afgeleide indeling exporteren

1. Selecteer de indeling **Indeling voor het leren van parameteraanroepen (aangepast)** in de configuratiestructuur.
2. Selecteer op het sneltabblad **Versies** de voltooide versie 1.1.1.
3. Selecteer **Uitwisselen**.
4. Selecteer **Exporteren als XML-bestand**.
5. Sla de gedownloade configuratie lokaal op in de XML-indeling.

## <a name="test-er-formats"></a>ER-indelingen testen 
U kunt de initiële en verbeterde ER-indelingen uitvoeren om te controleren of de geconfigureerde berekende parametervelden goed werken.

### <a name="import-er-configurations"></a>ER-configuraties importeren
U kunt gecontroleerde configuraties vanuit RCS importeren door de ER-opslagplaats van het type **RCS** te gebruiken. Als u de stappen in het onderwerp [Configuraties voor Elektronische rapportage (ER) importeren uit Regulatory Configuration Services (RCS)](rcs-download-configurations.md) al hebt uitgevoerd, gebruikt u de geconfigureerde ER-opslagplaats om de configuraties die eerder in dit onderwerp zijn besproken in uw omgeving te importeren. Volg anders deze stappen:

1. Selecteer het bedrijf **DEMF** en selecteer in het standaarddashboard de optie **Elektronische rapportage**.
2. Selecteer **Rapportageconfiguraties**.
3. Importeer de configuraties vanuit het Microsoft Downloadcentrum in deze volgorde: gegevensmodel, modeltoewijzing, indeling. Voer de volgende stappen uit voor elke ER-configuratie:

    1. Selecteer **Uitwisselen**.
    2. Selecteer **Laden uit XML-bestand**.
    3. Selecteer **Bladeren** om de vereiste ER-configuratie in XML-indeling te selecteren.
    4. Selecteer **OK**.

4. Importeer de uit RCS geëxporteerde voltooide versie 1.1.1 van de indeling **Indeling voor het leren van parameteraanroepen (aangepast)**:

    1. Selecteer **Uitwisselen**.
    2. Selecteer **Laden uit XML-bestand**.
    3. Selecteer **Bladeren** om de lokaal opgeslagen bestand **Indeling voor het leren van parameteroproepen (aangepast)** in de XML-indeling.
    4. Selecteer **OK**.

### <a name="run-er-formats"></a>ER-indelingen uitvoeren

1. Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.
2. Selecteer **Indeling voor het leren van parameteraanroepen**.
3. Selecteer **Uitvoeren** op het bovenste lint.
4. Sla de lokaal gegenereerde uitvoer op.
5. Selecteer het item **Indeling voor het leren van parameteraanroepen (aangepast)**.
6. Selecteer **Uitvoeren** op het bovenste lint.
7. Sla de gegenereerde uitvoer lokaal op. 
8. Vergelijk de inhoud van de gegenereerde uitvoer.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Formuleontwerper in elektronische rapportage (ER)](general-electronic-reporting-formula-designer.md)
- [De prestaties van ER-oplossingen verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen](er-calculated-field-ds-performance.md)

