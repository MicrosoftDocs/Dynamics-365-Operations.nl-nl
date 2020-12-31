---
title: ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven
description: In dit onderwerp wordt uitgelegd hoe u ER-indelingen (Elektronische rapportage) kunt configureren voor het gebruik van parameters die worden opgegeven per rechtspersoon.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0ed1442403ae82dfc820212e3e235737f37f21a4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679721"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht

In veel van de speciale indelingen voor elektronische rapporten die u zult ontwerpen, moet u gegevens filteren met behulp van een set waarden die specifiek zijn voor elke rechtspersoon van uw exemplaar (bijvoorbeeld een set belastingcodes om btw-transacties te filteren). Op dit moment worden waarden die afhankelijk zijn van de rechtspersoon (bijvoorbeeld btw-codes) gebruikt in expressies van de ER-indeling gebruikt om regels voor gegevensfiltering op te geven wanneer filters van dit type zijn geconfigureerd in een ER-indeling. Daarom wordt de ER-indeling rechtspersoonspecifiek gemaakt en moet u, om de vereiste rapporten te kunnen genereren, afgeleide kopieën van de oorspronkelijke ER-indeling maken voor elke rechtspersoon waarvoor u de ER-indeling moet uitvoeren. Elke afgeleide ER-indeling moet worden bewerkt om rechtspersoonspecifieke waarden in te voeren, opnieuw gebaseerd wanneer de oorspronkelijke (basis)versie is bijgewerkt, geëxporteerd vanuit een testomgeving en geïmporteerd in een productieomgeving wanneer deze moet worden geïmplementeerd voor productiegebruik enzovoort. Het onderhoud van dit type geconfigureerde ER-oplossing is daarom zeer ingewikkeld en tijdrovend om verschillende redenen:

-   Hoe meer rechtspersonen er zijn, des te meer configuraties voor ER-indelingen moeten worden bijgehouden.
-   Voor onderhoud aan ER-configuraties moeten zakelijke gebruikers over ER-kennis beschikken.

Met de functie voor toepassingsspecifieke ER-parameters kunnen hoofdgebruikers gegevens filteren in een ER-indeling, zodat deze is gebaseerd op een set abstracte regels. Deze set regels kan worden geconfigureerd voor gebruik van de gegevensbronnen die beschikbaar zijn in een ER-indeling. Zakelijke gebruikers kunnen vervolgens echte regels opgeven die verder gaan dan het nieuwe ER-raamwerk door de gebruikersinterface (UI) te gebruiken die automatisch wordt gegenereerd op basis van de instellingen van de overeenkomstige ER-indeling en de huidige gegevens van de rechtspersoon die worden gebruikt door de gegevensbronnen van de ER-indeling. De set regels die is opgegeven voor een ER-indeling kan worden geëxporteerd vanuit de huidige rechtspersoon van het exemplaar van Dynamics 365 Finance (Finance). Het kan vervolgens worden geïmporteerd in een andere rechtspersoon van hetzelfde exemplaar van Finance of een ander exemplaar als een set regels voor dezelfde ER-indeling.

## <a name="prerequisites"></a>Vereisten

Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot het exemplaar van Regulatory Configuration Services (RCS) dat is ingericht voor dezelfde tenant als Finance voor een van de volgende rollen:

- Ontwikkelaar elektronische rapportage
- Functioneel consultant elektronische rapportage
- Systeembeheerder

U wordt aangeraden de stappen in het onderwerp [Ondersteuning bieden voor parameteraanroepen van ER-gegevensbronnen van een BEREKEND VELD-type](er-calculated-field-type.md) te voltooien. Als u deze stappen al hebt uitgevoerd, kunt u de stappen in de daaropvolgende sectie **ER-configuraties importeren in RCS** overslaan.

## <a name="import-er-configurations-into-rcs"></a>ER-configuraties importeren in RCS

Download vanuit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=851448) het ZIP-bestand (gecomprimeerd) **Ondersteuning bieden voor parameteraanroepen van ER-gegevensbronnen van een BEREKEND VELD-type**. Dit ZIP-bestand bevat de volgende ER-configuraties die lokaal moeten worden uitgepakt en opgeslagen.

| **Omschrijving inhoud**                        | **Bestandsnaam**                                        |
|------------------------------------------------|------------------------------------------------------|
| Voorbeeldconfiguratie van **ER-gegevensmodel**    | Model voor het leren van parameteraanroepen.versie.1.xml     |
| Voorbeeldconfiguratiebestand voor **ER-metagegevens**      | Metagegevens voor het leren van parameteraanroepen.versie.1.xml  |
| Voorbeeldconfiguratiebestand voor **ER-modeltoewijzing** | Toewijzing voor het leren van parameteraanroepen.versie.1.xml |
| Voorbeeldconfiguratie voor **ER-indeling**             | Indeling voor het leren van parameteraanroepen.versie.1.xml  |

Meld u vervolgens aan bij uw RCS-exemplaar.

In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc. Voordat u de stappen in deze procedure kunt uitvoeren, moet u eerst de stappen in het onderwerp [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) in RCS voltooien.

1.  Selecteer **Elektronische aangifte** in het standaarddashboard.
2.  Selecteer **Rapportageconfiguraties**.
3.  Importeer de ER-configuraties die u eerder hebt gedownload naar RCS, in deze volgorde: gegevensmodel, metagegevens, modeltoewijzing en indeling. Volg deze stappen voor elke ER-configuratie:

    1.  Selecteer **Uitwisselen**.
    2.  Selecteer **Laden uit XML-bestand**.
    3.  Selecteer **Bladeren** om het bestand voor de vereiste ER-configuratie in XML-indeling te selecteren.
    4.  Selecteer **OK**.

## <a name="review-the-er-solution-that-is-provided"></a>De ER-oplossing controleren die wordt aangeboden

1.  Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.
2.  Selecteer het item **Indeling voor het leren van parameteraanroepen**.
3.  Selecteer **Ontwerper**.
4.  Selecteer **Uitvouwen/samenvouwen**.

    De ER-indeling **Indeling voor het leren van parameteraanroepen** is ontworpen voor het genereren van een btw-aangifte in XML-indeling die verschillende belastingniveaus (normaal, verlaagd en geen) presenteert. Elk niveau heeft een verschillend aantal details.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Vouw op het tabblad **Toewijzing** de items **Model**, **Gegevens** en **Samenvatting** uit.

    De gegevensbron **Model.Data.Summary** retourneert de lijst met btw-transacties. Deze transacties worden samengevat per btw-code. Voor deze gegevensbron is het berekende veld **Model.Data.Summary.Level** geconfigureerd voor het retourneren van de code voor het belastingniveau van elke samengevatte record. Voor elke btw-code die bij de uitvoering kan worden opgehaald uit de gegevensbron **Model.Data.Summary**, retourneert het berekende veld de code voor het belastingniveau (**Normaal**, **Verlaagd**, **Geen** of **Overige**) als een tekstwaarde. Het berekende veld **Model.Data.Summary.Level** wordt gebruikt om records te filteren van de gegevensbron **Model.Data.Summary** en om de gefilterde gegevens in elk XML-element in te voeren dat een belastingniveau vertegenwoordigt met behulp van de velden **Model.Data2.Level1**, **Model.Data2.Level2** en **Model.Data2.Level3**.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Het berekende veld **Model.Data.Summary.Level** is zo geconfigureerd dat het een ER-expressie bevat. Opmerking: de btw-codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** en **InVAT0**) zijn in de code vastgelegd in deze configuratie. Deze ER-indeling is daarom afhankelijk van de rechtspersoon waar deze btw-codes zijn geconfigureerd.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Als u een andere set belastingcodes voor elke rechtspersoon wilt ondersteunen, moet u de volgende stappen uitvoeren:

    - Maak een afgeleide versie van de ER-indeling voor elke rechtspersoon.
    - Werk de btw-codes in het berekende veld **Model.Data.Summary.Level** bij op basis van de instelling van de rechtspersoon.

6.  Sluit de pagina **Indelingsontwerper**.

## <a name="create-a-derived-format"></a>Een afgeleide indeling maken

Vervolgens gebruikt u de specifieke parameters van de ER-toepassing om een andere set belastingcodes voor elke rechtspersoon te ondersteunen in een enkele ER-indeling.

1.  Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.
2.  Selecteer het item **Indeling voor het leren van parameteraanroepen**.
3.  Selecteer **Configuratie maken**.
4.  Selecteer de optie **Afleiden van naam: Indeling voor het leren van parameteraanroepen, Microsoft**.
5.  Voer in het veld **Naam** de tekst **Indeling voor het opzoeken van LE-gegevens** in.
6.  Selecteer **Configuratie maken**.

## <a name="configure-a-derived-format"></a>Een afgeleide indeling configureren

### <a name="add-a-format-enumeration"></a>Een opsomming van indelingen toevoegen

Vervolgens voegt u een nieuwe opsomming van ER-indelingen toe. De waarden van deze indelingsopsomming worden weergegeven aan zakelijke gebruikers die rechtspersoonafhankelijke sets belastingcodes opgeven voor de verschillende belastingniveaus die worden gebruikt in de ER-indeling.

1.  Selecteer **Ontwerper**.
2.  Selecteer **Indelingsopsommingen**.
3.  Selecteer **Toevoegen**.
4.  Voer in het veld **Naam** de tekst **Lijst met belastingniveaus** in.
5.  Selecteer **Opslaan**.
6.  Selecteer op het tabblad **Waarden voor indelingopsomming** de optie **Toevoegen**.
7.  Voer in het veld **Naam** de tekst **Normale belasting** in.
8.  Selecteer opnieuw **Toevoegen**.
9.  Voer in het veld **Naam** de tekst **Verlaagde belasting** in.
10. Selecteer opnieuw **Toevoegen**.
11. Voer in het veld **Naam** de tekst **Geen belasting** in.
12. Selecteer opnieuw **Toevoegen**.
13. Voer in het veld **Naam** de tekst **Overige** in.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Omdat de zakelijke gebruikers mogelijk verschillende talen gebruiken om rechtspersoonafhankelijke sets belastingcodes op te geven, raden wij u aan de waarden van deze opsomming om te zetten in de talen die zijn geconfigureerd als de voorkeurstalen voor die gebruikers in Finance.

14. Selecteer de record **Geen belasting**.
15. Klik in het veld **Label**.
16. Selecteer **Vertalen**.
17. Voer in het deelvenster **Tekstvertaling** in het veld **Label-id** de waarde **LBL_LEVELENUM_NO** in.
18. Voer in het veld **Tekst in standaardtaal** de tekst **Geen belasting** in.
19. Selecteer in het veld **Taal** de waarde **DE** in.
20. Voer in het veld **Vertaalde tekst** de tekst **keine Besteuerung** in.
21. Selecteer **Vertalen**.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Selecteer **Opslaan**.
23. Sluit de pagina **Indelingsopsommingen**.

### <a name="add-a-new-lookup-data-source"></a>Een nieuwe gegevensbron voor opzoeken toevoegen

Vervolgens voegt u een nieuwe gegevensbron toe om aan te geven hoe zakelijke gebruikers rechtspersoonafhankelijke regels moeten opgeven om het juiste belastingniveau te herkennen voor elke samengevatte transactierecord.

1.  Selecteer op het tabblad **Toewijzing** de optie **Toevoegen**.
2.  Selecteer **Indelingsopsomming\Zoekopdracht**.

    U hebt zojuist vastgesteld dat elke regel die door zakelijke gebruikers wordt opgegeven voor het herkennen van het belastingniveau een waarde van een ER-indelingsopsomming retourneert. Het type gegevensbron **Zoekopdracht** is toegankelijk onder de blokken **Gegevensmodel** en **Dynamics 365 for Operations** en in het blok **Indelingsopsomming**. Hierdoor kunnen er geen ER-gegevensmodelopsommingen en toepassingsopsommingen worden gebruikt om het type waarden op te geven dat wordt geretourneerd voor gegevensbronnen van dat type.
    
3.  Voer in het veld **Naam** de tekst **Selectie** in.
4.  Selecteer in het veld **Indelingspsomming** de optie **Lijst met belastingniveaus**.

    U hebt zojuist opgegeven dat een zakelijke gebruiker voor elke regel die in deze gegevensbron is opgegeven een van de waarden van de indelingsopsomming **lijst met belastingniveaus** moet selecteren als geretourneerde waarde.
    
5.  Selecteer **Zoekopdracht bewerken**.
6.  Selecteer **Kolommen**.
7.  Vouw het item **Model** uit.
8.  Vouw het item **Gegevens** uit.
9.  Vouw het item **Belasting** uit.
10. Selecteer het item **Model.Data.Tax.Code**.
11. Selecteer de knop **Toevoegen** (de pijl naar rechts).

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    U hebt zojuist opgegeven dat een zakelijke gebruiker voor elke regel die in deze gegevensbron is opgegeven voor herkenning van het belastingniveau een van de belastingcodes moet selecteren als een voorwaarde. De lijst met belastingcodes die de zakelijke gebruiker kan selecteren, wordt geretourneerd door de gegevensbron **Model.Data.Tax**. Omdat deze gegevensbron het veld **Naam** bevat, wordt de naam van de belastingcode weergegeven voor elke waarde van een belastingcode in de zoekopdracht die aan de zakelijke gebruiker wordt gepresenteerd.
    
12. Selecteer **OK**.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Zakelijke gebruikers kunnen meerdere regels toevoegen als records van deze gegevensbron. Elke record wordt genummerd met een regelcode. Regels worden geëvalueerd in volgorde van oplopend regelnummer.

    Omdat u het veld **Belastingcode** hebt geselecteerd als voorwaarde voor regels in deze gegevensbron voor opzoeken en omdat **Belastingcode** is ingesteld als veld van het gegevenstype **Tekenreeks**, wordt elke regel geëvalueerd tijdens de uitvoering door de belastingcode te vergelijken die wordt doorgegeven aan de gegevensbron met de belastingcode die in deze record van de gegevensbron is gedefinieerd.

    Wanneer een regel wordt gevonden die aan de geconfigureerde voorwaarde voldoet, retourneert deze gegevensbron de opzoekwaarde van de regel die is gedefinieerd in het veld **Zoekresultaat**. Als er geen regel wordt gevonden, wordt er een uitzondering gegenereerd om de gebruiker te laten weten dat de huidige gegevensbron geen juiste waarde kan retourneren.

13. Selecteer **Opslaan**.
14. Sluit de pagina **Ontwerpfunctie voor zoekopdrachten**.
15. Selecteer **OK**.

    U ziet dat u een nieuwe gegevensbron hebt toegevoegd waarmee het belastingniveau wordt geretourneerd als waarde van de indelingsopsomming **Lijst met belastingniveaus** voor elke belastingcode die aan de gegevensbron wordt doorgegeven als argument van de parameter **Code** van het gegevenstype **Tekenreeks**.
    
    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    De evaluatie van geconfigureerde regels hangt af van het gegevenstype van de velden die zijn geselecteerd om de voorwaarden van deze regels te definiëren. Wanneer u een veld selecteert dat is geconfigureerd als veld van het gegevenstype **Numeriek** of **Datum**, wijken de criteria af van de criteria die eerder werden beschreven voor het gegevenstype **Tekenreeks**. Voor velden **Numeriek** en **Datum** moet de regel worden opgegeven als een bereik van waarden. Aan de voorwaarde van de regel wordt geacht te zijn voldaan wanneer een waarde die aan de gegevensbron wordt doorgegeven in het geconfigureerde bereik valt.
    
    In de volgende afbeelding ziet u een voorbeeld van dit type instelling. Naast het veld **Model.Data.Tax.Code** van het gegevenstype **Tekenreeks**, wordt het veld **Model.Tax.Summary.Base** van het gegevenstype **Reëel** gebruikt om voorwaarden voor een gegevensbron voor zoeken op te geven.
    
    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Omdat de velden **Model.Data.Tax.Code** en **Model.Tax.Summary.Base** zijn geselecteerd voor deze gegevensbron voor zoeken, wordt elke regel van deze gegevensbron als volgt geconfigureerd:
    
    -   In de lijst die wordt weergegeven, moet de waarde van de indelingsopsomming **Lijst met belastingniveaus** worden geselecteerd als geretourneerde waarde.
    -   De belastingcode moet als voorwaarde voor deze regel worden ingevoerd. Alleen belastingcodes die door de gegevensbron **Model.Data.Tax** zijn geleverd zijn van toepassing.
    -   De minimum- en maximumwaarden van het basisbedrag voor belasting moeten als voorwaarden voor deze regel worden ingevoerd.

    Elke regel van deze gegevensbron wordt als volgt geëvalueerd tijdens de uitvoering:
    -   Is de code van het gegevenstype **Tekenreeks** dat aan deze gegevensbron is doorgegeven gelijk aan de belastingcode van een regel?
    -   Ligt de waarde van het gegevenstype **Reëel** dat aan deze gegevensbron is doorgegeven, tussen de specifieke minimum- en maximumwaarden?

    Een regel wordt als van toepassing beschouwd als aan beide voorwaarden is voldaan.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Het label vertalen van de gegevensbron voor zoeken die is toegevoegd

Omdat zakelijke gebruikers mogelijk verschillende talen gebruiken om rechtspersoonafhankelijke sets belastingcodes op te geven, raden wij u aan de label van een gegevensbron voor zoeken die u toevoegt te vertalen zodat deze wordt gepresenteerd in de voorkeurstaal van elke gebruiker op de desbetreffende pagina.

1.  Selecteer de gegevensbron **Model.Data.Selector**.
2.  Selecteer **Bewerken**.
3.  Klik in het veld **Label**.
4.  Selecteer **Vertalen**.
5.  Voer in het deelvenster **Tekstvertaling** in het veld **Label-id** de waarde **LBL_SELECTOR_DS** in.
6.  Voer in het veld **Tekst in standaardtaal** de tekst **Belastingniveau selecteren per belastingcode** in.
7.  Selecteer in het veld **Taal** de waarde **DE** in.
8.  Voer in het veld **Vertaalde tekst** de tekst **Steuerebene für Steuerkennzeichen auswählen** in.
9.  Selecteer **Vertalen**.
10. Selecteer **OK**.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Een nieuw veld toevoegen om de geconfigureerde zoekopdracht te gebruiken

1.  Vouw het item **Model.Data** uit.
2.  Selecteer het item **Model.Data.Summary**.
3.  Selecteer **Toevoegen**.
4.  Selecteer **Functies/Berekend veld**.
5.  Voer in het veld **Naam** de tekst **LevelByLookup** in.
6.  Selecteer **Formule bewerken**.
7.  Voer in het **Formuleveld** de tekst **Model.Selector(Model.Data.Summary.Code)** in.
8.  Selecteer **Opslaan**.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Sluit de pagina **Formule-editor**.
10. Selecteer **OK**.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Het berekende veld **LevelByLookup** dat u hebt toegevoegd, retourneert het belastingniveau als de waarde van de indelingsopsomming **Lijst met belastingniveaus** voor elke samengevatte belastingtransactierecord. De belastingcode van de record wordt doorgegeven aan de gegevensbron voor zoeken **Model.Selector** en de set regels voor deze gegevensbron wordt gebruikt om het juiste belastingniveau te selecteren.

### <a name="add-a-new-format-enumeration-based-data-source"></a>Een nieuwe op een indelingsopsomming gebaseerde gegevensbron toevoegen

Vervolgens voegt u een nieuwe gegevensbron toe die verwijst naar de indelingsopsomming die u eerder hebt toegevoegd. Waarden van deze gegevensbron worden later in een ER-indelingsexpressie gebruikt.

1.  Selecteer **Basis toevoegen**.
2.  Selecteer **Indelingsopsommingen\Opsomming**.
3.  Voer in het veld **Naam** de tekst **TaxationLevel** in.
4.  Selecteer in het veld **Indelingspsomming** de optie **Lijst met belastingniveaus**.
5.  Selecteer **Opslaan**.

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>Een bestaand veld wijzigen om te beginnen met zoeken

Vervolgens wijzigt u het bestaande berekende veld zodat dit de geconfigureerde gegevensbron voor zoeken gebruikt om de juiste waarde voor het belastingniveau te retourneren, afhankelijk van de belastingcode.

1.  Selecteer het item **Model.Data.Summary.Level**.
2.  Selecteer **Bewerken**.
3.  Selecteer **Formule bewerken**.

    Merk op dat de huidige expressie van het veld **Model.Data.Summary.Level** de volgende in de code vastgelegde belastingcodes bevat:
    
    CASE (@.Code, "VAT19", "Normaal", "InVAT19", "Normaal", "VAT7", "Verlaagd", "InVAT7", "Verlaagd", "THIRD", "Geen", "InVAT0", "Geen", "Overige")

4.  Voer in het veld **Formule** de tekst **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Normaal", TaxationLevel.'Reduced taxation', "Verlaagd", TaxationLevel.'No taxation', "Geen", "Overige")** in.

    ![Pagina voor ER Operations-ontwerper](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    De expressie van het veld **Model.Data.Summary.Level** retourneert nu het belastingniveau op basis van de belastingcode van de huidige record en de set regels die een zakelijke gebruiker configureert in de gegevensbron voor zoeken **Model.Data.Selector**.
    
5.  Selecteer **Opslaan**.
6.  Sluit de pagina **Formuleontwerper**.
7.  Selecteer **OK**.
8.  Selecteer **Opslaan**.
9.  Sluit de pagina **Indelingsontwerper**.

## <a name="complete-the-draft-version-of-a-derived-format"></a>De conceptversie van een afgeleide indeling voltooien

1.  Selecteer op het sneltabblad **Versies** de optie **Status wijzigen**.
2.  Selecteer **Voltooien**.
3.  Selecteer **OK**.

## <a name="export-completed-version-of-modified-format"></a>Voltooide versie van een gewijzigde indeling exporteren

1.  Selecteer het item **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.
2.  Selecteer op het sneltabblad **Versies** de record met de status **Voltooid**.
3.  Selecteer **Uitwisselen**.
4.  Selecteer **Exporteren als XML-bestand**.
5.  Selecteer **OK**.
6.  De webbrowser downloadt een bestand **Indeling voor het opzoeken van LE-gegevens.xml**. Sla dit bestand lokaal op.

Herhaal de stappen in dit gedeelte voor de bovenliggende items van de indeling **Indeling voor het opzoeken van LE-gegevens** en sla de volgende bestanden lokaal op:

-   Indeling voor het leren van parameteraanroepen.xml
-   Toewijzing voor het leren van parameteraanroepen.xml
-   Model voor het leren van parameteraanroepen.xml

Als u wilt leren hoe u de geconfigureerde ER-indeling **Indeling voor het opzoeken van LE-gegevens** kunt gebruiken voor het instellen van rechtspersoonafhankelijke sets belastingcode om belastingtransacties te filteren op basis van verschillende belastingniveaus, voert u de stappen uit in het onderwerp [De parameters van een ER-indeling per rechtspersoon instellen](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Aanvullende resources

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[De parameters van een ER-indeling per rechtspersoon instellen](er-app-specific-parameters-set-up.md)
