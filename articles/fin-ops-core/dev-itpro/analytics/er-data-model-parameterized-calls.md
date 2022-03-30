---
title: Parameteraanroepen van ER-gegevensmodellen ondersteunen
description: In dit onderwerp wordt uitgelegd hoe u parameteraanroepen van ER-gegevensmodellen voor Elektronische rapportage kunt implementeren.
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419467"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Parameteraanroepen van ER-gegevensmodellen ondersteunen

[!include [banner](../includes/banner.md)]

Als u bedrijfsdocumenten wilt genereren, configureert u een [ER-oplossing](general-electronic-reporting.md) die de volgende ER-onderdelen bevat:

- **[Indeling](er-overview-components.md#format-component)**: dit onderdeel geeft de structuur van een bedrijfsdocument aan.
- **Indelingstoewijzing**: dit onderdeel bepaalt hoe een bedrijfsdocument wordt ingevuld tijdens runtime.
- **[Modeltoewijzing](er-overview-components.md#model-mapping-component)**: met dit onderdeel wordt opgegeven wat uit de toepassing wordt opgehaald in de een indelingstoewijzing.
- **[Gegevensmodel](er-overview-components.md#data-model-component)**: dit onderdeel geeft gegevens tussen afzonderlijke onderdelen door.

Wanneer u een ER-indeling uitvoert, wordt elk indelingselement uitgevoerd, te beginnen met het hoofdindelingselement. Wanneer een indelingselement dat wordt uitgevoerd, een binding met een [gegevensbron](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) bevat, wordt de gegevensbron uitgevoerd om de verwachte gegevens te leveren en te gebruiken om het indelingselement in te vullen. Wanneer een gegevensbron van het *modeltype* wordt aangeroepen, wordt de juiste modeltoewijzing aangeroepen om gegevens uit de toepassing op te halen op basis van de modeltoewijzingsinstellingen.

Eerder kunnen deze modeltoewijzingsaanroepen niet worden geparametreerd om ze afhankelijk te maken van de logica van de uit te voeren indeling. Alleen de volgende gegevensstroom werd ondersteund.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Indelingselement<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;aanvraag&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;&lt;
</td>
<td><b>Indelingstoewijzing</b><br>
Gegevensbron<br>
&nbsp;
</td>
<td>
<i>Gegevensmodel</i><br>
&gt;&nbsp;aanvraag&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;&lt;
</td>
<td>
<b>Modeltoewijzing</b><br>
Gegevensbron<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;aanvraag&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;&lt;
</td>
<td>
<b>Tabel</b><br>
Registreren<br>
Veld
</td>
</tr>
</tbody>
</table>

In versie 10.0.15 en hoger kunt u echter gegevensmodelvelden configureren die alleen kunnen worden aangeroepen als de waarden van de geconfigureerde parameters zijn opgegeven. Wanneer een dergelijk veld wordt geconfigureerd en aangeroepen vanuit een indelingscomponent, moeten de vereiste parameters worden opgegevens in een indelingsbinding als argumenten van de aanroep. In deze gevallen kunnen de waarden van de argumenten worden opgegeven op basis van opmaakspecifieke waarden. U kunt daarom **dynamische runtimeparameters** voor gegevensmodelaanroepen gebruiken om de volgende gegevensstroom te ondersteunen.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Indelingselement&nbsp;1<br>
<br>
Indelingselement&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;aanvraag&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;aanvraag&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Indelingstoewijzing</b><br>
Gegevensbron&nbsp;1<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Gegevensmodel</i><br>
&gt;&nbsp;field1&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;waarde&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Modeltoewijzing</b><br>
Gegevensbron&nbsp;1<br>
<br>
Gegevensbron&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;aanvraag&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;aanvraag&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;waarde&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tabel&nbsp;1</b><br>
Record&nbsp;1<br>
Veld&nbsp;1<br>
<b>Tabel&nbsp;2</b><br>
Record&nbsp;2<br>
Veld&nbsp;2
</td>
</tr>
</tbody>
</table>

Met de nieuwe functionaliteit kunt u paremeters voor de aanroep opgeven voor een gegevensmodelveld van het type [*Record*](er-formula-supported-data-types-composite.md#record) of [*Recordlijst*](er-formula-supported-data-types-composite.md#record-list). De volgende gegevenstypen worden ondersteund voor de parameters van een gegevensmodelveld:

- [Booleaanse waarde](er-formula-supported-data-types-primitive.md#boolean)
- [Container](er-formula-supported-data-types-composite.md#container)
- [Datum](er-formula-supported-data-types-primitive.md#date)
- [DateTime](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Geheel getal](er-formula-supported-data-types-primitive.md#integer)
- [Real-modus](er-formula-supported-data-types-primitive.md#real)
- [Tekenreeks](er-formula-supported-data-types-primitive.md#string)

U kunt elke parameter van een gegevensmodelveld opgeven waarvoor het argument kan worden geleverd als één waarde van het gedefinieerde gegevenstype en de [*lijst*](er-formula-supported-data-types-composite.md#record-list) met dergelijke waarden.

> [!NOTE]
> De standaardwaarde voor de parameter van een gegevensmodelveld wordt niet ondersteund. Als u een parameter toevoegt aan een veld in een gegevensmodel en de versie van dat gegevensmodel is al vrijgegeven en gepubliceerd, moet u alle bijbehorende modeltoewijzingen en -indelingen [rebasen](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) voor de nieuwe versie van dit model, omdat dit gegevensmodel niet achterwaarts compatibel is.

U kunt velden van geparametreerde gegevensmodellen configureren om de indeling van modeltoewijzingsaanroepen specifiek te maken. Door deze benadering kunt u het aantal modeltoewijzingen verminderen dat moet worden geconfigureerd voor een groot aantal indelingen van één gegevensmodel. U kunt deze methode ook gebruiken om de uitvoeringsprestaties van uw indelingen te verbeteren en de tijd te beperken die nodig is om bedrijfsdocumenten te genereren. Voor meer informatie over deze functie kunt u het voorbeeld in dit onderwerp uitvoeren.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Voorbeeld: Parameteraanroepen van ER-gegevensmodellen gebruiken

De volgende stappen leggen uit hoe een gebruiker in de rol Systeembeheerder of Ontwikkelaar elektronische rapportage een ER-oplossing kan ontwerpen die een gegevensmodel, een modeltoewijzing en een ER-indelingsonderdeel bevat die geconfigureerd zijn voor het aanroepen van een modeltoewijzing vanuit een indeling door het leveren van een argument voor de aanroep, waarvan de waarde tijdens runtime is berekend met behulp van de formule van de lopende indeling. 

Deze stappen kunnen in het **DEMF**-bedrijf worden uitgevoerd. Er zijn geen codewijzigingen vereist. 

In dit voorbeeld maakt u de vereiste ER-[configuraties](general-electronic-reporting.md#Configuration) voor het voorbeeldbedrijf, **Litware, Inc.**. Controleer of de configuratieprovider voor het voorbeeldbedrijf **Litware, Inc.** (`http://www.litware.com`) wordt vermeld voor het ER-raamwerk en of het is gemarkeerd is als **Actief**. Als deze configuratieprovider niet wordt vermeld of als deze niet is gemarkeerd als **Actief**, volgt u de stappen in het onderwerp [Een configuratieprovider maken en als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Bedrijfsscenario

U hebt een ER-oplossing, die een indeling bevat die u kunt uitvoeren om een elektronisch document te genereren voor controledoeleinden. Deze indeling bevat btw-transacties die zijn gerelateerd aan verkoop- en inkooporders en die de vereiste gegevens hebben, zoals de transactiedatum en btw-waarde. De structuur van dit document is met het nieuwe boekjaar gewijzigd. U moet nu een uitgebreid document indienen met aanvullende gegevens (namen) van alle partijen (klanten en leveranciers) van wie de transacties in gegenereerde rapporten worden weergegeven. Daarom moet u uw ER-oplossing wijzigen zodat het documenten genereert die voldoen aan deze nieuwe vereiste.

### <a name="configure-the-er-framework"></a>Het ER-raamwerk configureren

Voer de stappen in [Het ER-raamwerk configureren](er-quick-start2-customize-report.md#ConfigureFramework) uit om de minimale set ER-parameters in te stellen. U moet deze instellingen voltooien voordat u het ER-raamwerk gaat gebruiken om een nieuwe ER-oplossing te ontwerpen.

### <a name="design-a-domain-specific-data-model"></a>Domeinspecifiek gegevensmodel ontwerpen

U moet een nieuwe ER-configuratie maken die het vereiste gegevensmodel bevat. Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u een ER-indeling ontwerpt om een auditrapport te genereren.

Volg deze stappen om het vereiste gegevensmodel te importeren uit een XML-bestand dat door Microsoft wordt geleverd.

1. Download het bestand [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Sample audit model model.version.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

    ![Configuratie van het geïmporteerde ER-gegevensmodel op de pagina Configuraties.](./media/er-data-model-parameterized-calls-imported-model.png)

In de volgende afbeelding ziet u de bewerkbare versie van het geconfigureerde gegevensmodel op de pagina **Gegevensmodel ontwerpen**.

![Structuur van het ER-gegevensmodel op de pagina Gegevensmodelontwerper.](./media/er-data-model-parameterized-calls-model1.png)

Op dit moment is het model ontworpen om alleen belastingtransacties beschikbaar te maken die de vereiste details hebben.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Een modeltoewijzing voor het geconfigureerde gegevensmodel ontwerpen

Als gebruiker in de rol van ER-ontwikkelaar moet u een nieuwe ER-configuratie maken die een modeltoewijzingsonderdeel bevat voor het gegevensmodel Voorbeeldaudit. Dit onderdeel implementeert het geconfigureerde gegevensmodel voor Microsoft Dynamics 365 Finance en is specifiek voor die app. U moet het modeltoewijzingsonderdeel configureren om de toepassingsobjecten op te geven die moeten worden gebruikt voor het invullen met toepassingsgegevens van het geconfigureerde gegevensmodel tijdens runtime. Als u deze taak wilt voltooien, moet u begrijpen hoe de gegevensstructuur van het belastingbedrijfsdomein wordt geïmplementeerd in Finance.

Volg deze stappen om het vereiste modeltoewijzing te importeren uit een XML-bestand dat door Microsoft wordt geleverd.

1. Download het bestand [Sample audit model mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Sample audit model mapping.version.1.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

    ![Configuratie van geïmporteerde ER-modeltoewijzing op de pagina Configuraties.](./media/er-data-model-parameterized-calls-imported-mapping.png)

In de volgende afbeelding wordt de bewerkbare versie van de geconfigureerde modeltoewijzing weergegeven op de pagina **Ontwerper modeltoewijzing**.

![Structuur van de ER-modeltoewijzing op de pagina Ontwerper modeltoewijzing.](./media/er-data-model-parameterized-calls-mapping1.png)

Op dit moment is de modeltoewijzing ontworpen om belastingtransacties beschikbaar te maken die de vereiste details hebben. Deze gegevens worden opgehaald uit de toepassingstabel `TaxTrans` met behulp van de geconfigureerde ER-gegevensbronnen `TaxTrans` en `TaxTransFiltered`.

### <a name="design-a-new-format"></a>Een nieuwe indeling ontwerpen

Als gebruiker in de rol van ER-functieconsultant moet u een nieuwe configuratie maken die een indelingsonderdeel bevat. U moet het indelingsonderdeel configureren om gegenereerde rapporten in te vullen met btw-transacties met alle vereiste details.

Volg deze stappen om de vereiste indeling te importeren uit een XML-bestand dat door Microsoft wordt geleverd.

1. Download het bestand [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Sample audit format.version.1.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

    ![Configuratie van het geïmporteerde ER-indeling op de pagina Configuraties.](./media/er-data-model-parameterized-calls-imported-format.png)

In de volgende afbeelding wordt de bewerkbare versie van de geconfigureerde indeling weergegeven op de pagina **Indelingsontwerper**.

![Structuur van de ER-indeling op de pagina Indelingsontwerper.](./media/er-data-model-parameterized-calls-format1.png)

De ER-indeling wordt geconfigureerd voor het genereren van een rapport als tekstbestand in CSV-indeling (Comma Separated Values).

### <a name="run-the-imported-format"></a>De geïmporteerde indeling uitvoeren

1. Selecteer op de pagina **Configuraties** de configuratie **Indeling voorbeeldaudit** en selecteer **Uitvoeren** in het actievenster.
2. Selecteer in het dialoogvenster **ER-parameters** op het tabblad **Op te nemen records** de optie **Filter**.
3. Geef de voorwaarden op voor het selecteren van de belastingtransacties van de boekstukken **PIV-110000004** en **INV-10000001**.
4. Selecteer **OK**.
5. Selecteer **OK**.
6. Controleer het gegenereerde document dat belastingtransacties van de geselecteerde boekstukken bevat.

    ![Bekijk het voorbeeld van het gegenereerde document met belastingtransacties.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>De geïmporteerde ER-oplossing aanpassen

Volgens de nieuwe vereiste moet het document dat u indient, de namen bevatten van klanten en leveranciers van wie de transacties zijn opgenomen. Daarom moet u de geïmporteerde ER-oplossing wijzigen zodat het een document genereert dat voldoet aan deze nieuwe vereiste.

Bepaal hoe u de vereiste wijzigingen van de geïmporteerde ER-onderdelen wilt implementeren.

De eerste aanpak is het doorvoeren van de volgende wijzigingen:

- Voeg in het gegevensmodel het nieuwe gegevensmodelveld `Transaction.Party.Name` van het type *Tekenreeks* toe.
- Configureer in uw modeltoewijzing de binding voor het nieuwe gegevensmodelveld door de beschikbare tabelrelaties te gebruiken om toegang te krijgen tot de relevante record van de toepassingstabel `DirPartyTable` en de waarde van het veld `Name` op te halen.

Hoewel deze aanpak werkt, kunnen er prestatieproblemen optreden in de SQL-database, omdat `TaxTrans` de transactietabel is en daarom een groot aantal records kan bevatten. In dit geval moet het aantal aanroepen voor `DirPartyTable` gelijk zijn aan het aantal records in tabel `TaxTrans` wat prestatieproblemen kan veroorzaken.

U kunt ook de volgende wijzigingen doorvoeren:

- Voeg in uw gegevensmodel de nieuwe hoofdmap `Party` toe en het nieuwe veld `Party.Name`.
- Voeg in de modeltoewijzing een nieuwe gegevensbron toe waarin alle records van tabellen die worden gebruikt in tabelrelaties, worden samengevoegd om toegang te krijgen tot de relevante record van de toepassingstabel `DirPartyTable`, te beginnen vanuit de tabel `TaxTrans`.

Hoewel deze benadering werkt, kan dit problemen met het geheugenverbruik veroorzaken. Zelfs wanneer een nieuwe [JOIN-gegevensbron](er-join-data-sources.md) wordt uitgevoerd als een enkele SQL-aanvraag voor de toepassingsdatabase om prestatieproblemen van de database te voorkomen, moet het resultaat worden opgehaald in het geheugen van de toepassingsserver. Omdat het aantal records en het aantal velden in die records erg groot zal zijn, kan deze benadering veel geheugen verbruiken. Er kan zelf een runtime-uitzondering voor te weinig geheugen optreden.

U kunt de wijzigingen implementeren wanneer door een lopende indeling in het geheugen de unieke identificatiecodes van klanten en leveranciers worden verzameld voor alle belastingtransacties die in een gegenereerd rapport worden weergegeven. Aangezien alleen unieke codes behouden moeten blijven, is de uiteindelijke set codes niet groot genoeg om het geheugenverbruik te beïnvloeden. De set codes wordt vervolgens doorgegeven aan de modeltoewijzing als argument van een andere aanroep van de gegevensbron van het type *Model*. Op basis van die aanroep wordt door de modeltoewijzing een nieuwe ER-gegevensbron uitgevoerd, waardoor met een enkele SQL-aanvraag voor de toepassingsdatabase uit de tabel `DirPartyTable` alleen records worden opgehaald voor de partijen van wie de codes worden weergegeven in de opgegeven set codes.

### <a name="adjust-the-imported-data-model"></a>Het geïmporteerde gegevensmodel aanpassen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Voorbeeldauditmodel**.
3. Selecteer op het sneltabblad **Versies** versie **2** met de status **[Concept](general-electronic-reporting.md#component-versioning)**.
4. Selecteer het sneltabblad **Configuratieonderdelen**.
5. Selecteer **Ontwerper** om het gegevensmodel te openen voor bewerken.
6. Zorg dat op de pagina **Gegevensmodel** het veld `Root` is geselecteerd en selecteer vervolgens **Nieuw**.
7. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer in de veldgroep **Nieuw knooppunt als** de optie **Onderliggende waarde van een actief knooppunt**.
    2. Voer in het veld **Naam** de tekst **Partij** in.
    3. Selecteer in het veld **Itemtype** **Recordlijst**.
    4. Selecteert **Toevoegen** om het nieuwe veld toe te voegen.

8. Zorg dat het veld `Root.Party` is geselecteerd en selecteer vervolgens op het tabblad **Knooppunt** de optie **Parameters**.
9. Voer de volgende stappen uit in het dialoogvenster **Parameters**:

    1. Selecteer op het tabblad **Parameters** de optie **Nieuw**.
    2. Voer in het veld **Naam** **PartyRefRecId** in.
    3. Selecteer in het veld **Type** de optie **Int64**.
    4. Schakel het selectievakje **Lijst** in.
    5. Selecteer **OK** om het invoeren van de parameters te voltooien.

    > [!NOTE]
    > U hebt het gegevensmodelveld `Root.Party` geconfigureerd als een veld dat wordt aangeroepen wanneer een waarde wordt opgegeven in de parameter **PartyRefRecId**. Deze waarde moet aanwezig zijn in de lijst met records die een veld `Value` van het gegevenstype *Int64* bevatten.

    ![Dialoogvenster Parameters.](./media/er-data-model-parameterized-calls-model2a.png)

10. Zorg ervoor dat het veld `Root.Party` nog steeds is geselecteerd en selecteer **Nieuw**.
11. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer in de veldgroep **Nieuw knooppunt als** de optie **Onderliggende waarde van een actief knooppunt**.
    2. Geef in het veld **Naam** de tekst **Naam** op.
    3. Selecteer in het veld **Itemtype** **Tekenreeks**.
    4. Selecteert **Toevoegen** om het nieuwe veld toe te voegen.

12. Selecteer **Opslaan** en sluit de pagina **Gegevensmodel**.

    ![Structuur van het aangepaste ER-gegevensmodel op de pagina Gegevensmodelontwerper.](./media/er-data-model-parameterized-calls-model2b.png)

13. Selecteer op het sneltabblad **Versies** voor versie **2** de optie **Status wijzigen** \> **Voltooien**. Selecteer vervolgens **OK**.

    > [!NOTE]
    > Wijzigingen in uw gegevensmodel worden opgeslagen in de tweede revisie van het gegevensmodelonderdeel **Voorbeeldauditmodel** dat zich bevindt in de tweede versie van de ER-configuratie **Voorbeeldauditmodel**.

![Configuratie van het bijgewerkte ER-gegevensmodel op de pagina Configuraties.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>De geïmporteerde modeltoewijzing aanpassen

1. Breid op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Voorbeeldauditmodel** uit.
2. Selecteer **Voorbeeld-auditmodeltoewijzing** en selecteer vervolgens in het sneltabblad **Versies** de tweede toewijzingsversie die is gebaseerd op de eerste gegevensmodelversie (versie **1.2**) en die de status **Concept** heeft.
3. Selecteer **Rebase**.
4. Laat in het veld **Doelversie** versie **2** van het basismodel **Voorbeeldauditmodel** staan.
5. Selecteer **OK** om de modeltoewijzing opnieuw te maken en af te stemmen op recente wijzigingen in het gegevensmodel.

    Het versienummer van uw bewerkbare modeltoewijzing is gewijzigd van **1.2** in **2.2** om aan te geven dat de tweede modelversie momenteel als basis wordt gebruikt.

6. Selecteer **Ontwerper**.
7. Selecteer **Ontwerper** op de pagina **Model aan gegevensbrontoewijzing** voor de huidige modeltoewijzing.
8. Volg deze stappen om een nieuwe gegevensbron toe te voegen om toegang te krijgen tot de toepassingstabel `DirPartyTable`:

    1. Selecteer in het deelvenster **Type gegevensbronnen** **Dynamics 365 for Operations \> Tabelrecords**.
    2. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    3. Voer in het veld **Naam** **PartyTable** in.
    4. Voer in het veld **Tabel** **DirPartyTable** in.
    5. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

9. Volg deze stappen om een nieuwe gegevensbron toe te voegen voor het aanvragen van `DirPartyTable`-records op basis van de opgegeven lijst met recordidentificatiecodes:

    1. Selecteer in het deelvenster **Type gegevensbronnen** **Algemeen \> Lege container**.
    2. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    3. Geef in het veld **Naam** de tekst **Gegevens** op.
    4. Klik op **OK** om de nieuwe gegevensbron toe te voegen.
    5. Selecteer in het deelvenster **Gegevensbronnen** de gegevensbron **Gegevens**.
    6. Selecteer in het deelvenster **Type gegevensbronnen** **Functies \> Berekend veld**.
    7. Selecteer **Toevoegen** in het deelvenster **Gegevensbronnen**.
    8. Voer in het veld **Naam** de tekst **DirParty** in.
    9. Selecteer **Formule bewerken**.
    10. Selecteer **Parameters** op de pagina **Formuleontwerper**.
    11. Voer de volgende stappen uit in het dialoogvenster **Parameters**:

        1. Selecteer op het tabblad **Parameters** de optie **Nieuw**.
        2. Voer in het veld **Naam** de tekst **DirPartyId** in.
        3. Selecteer in het veld **Type** de optie **Int64**.
        4. Schakel het selectievakje **Lijst** in.
        5. Selecteer **OK**.

        > [!NOTE]
        > U hebt dit berekende veld geconfigureerd, zodat het bij runtime het argument van één parameter accepteert dat is geconfigureerd als een recordlijst met één `Value`-veld van het type *Int64*.

    12. Voer in het veld **Formule** de volgende expressie in:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > U hebt het berekende veld `DirParty` zo geconfigureerd dat alleen `DirPartyTable`-records worden opgehaald waarvoor de recordidentificatiecodes zijn opgenomen in de lijst `DirPartyId` die als argument wordt geleverd wanneer het veld `DirParty` wordt aangeroepen.

        ![Formule om partijnamen op te halen uit de toepassingstabel op de formuleontwerperpagina.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.
    14. Selecteer **Opslaan** en **OK** om het toevoegen van de nieuwe gegevensbron te voltooien.

10. Volg deze stappen om de nieuwe gegevensbron aan het nieuwe gegevensmodelveld te verbinden, zodat het gegevensmodel wordt gebruikt om partijnamen beschikbaar te maken:

    1. Selecteer in het deelvenster **Gegevensmodel** het veld `Root.Party`-gegevensmodel.
    2. Selecteer **Bewerken** in het deelvenster **Gegevensmodel**.
    3. Voer op de pagina **Formuleontwerper** in het veld **Formule** de expressie `Data.DirParty(PartyRefRecId)` in.
    4. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.

        > [!NOTE]
        > U hebt de binding zo geconfigureerd dat de geconfigureerde `Data.DirParty`-gegevensbron wordt aangeroepen en de lijst met recordidentificatiecodes wordt aangeleverd die worden opgegeven in de indeling wanneer in het veld `Root.Party`-gegevensmodel wordt aangeroepen.

    5. Selecteer in het deelvenster **Gegevensmodel** het veld `Root.Party.Name`-gegevensmodel.
    6. Selecteer **Bewerken** in het deelvenster **Gegevensmodel**.
    7. Vouw op de pagina **Formuleontwerper** in het deelvenster **Gegevensbron** **Gegevens \> DirParty** uit en selecteer **Naam**.
    8. Selecteer **Gegevensbron toevoegen**.
    9. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.

    ![Structuur van de aangepaste ER-modeltoewijzing op de pagina Ontwerper modeltoewijzing.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Selecteer **Opslaan** en sluit de pagina **Ontwerper modeltoewijzing**.
12. Sluit de pagina **Model aan gegevensbrontoewijzing**.
13. Selecteer op het sneltabblad **Versies** voor versie **2.2** de optie **Status wijzigen \> Voltooien**. Selecteer vervolgens **OK**.

### <a name="adjust-the-imported-format"></a>De geïmporteerde indeling aanpassen

1. Selecteer **Voorbeeldauditindeling** op de pagina **Configuraties**.
2. Selecteer op het sneltabblad **Versies** versie **1.2** met de status **Concept**.
3. Selecteer **Rebase**.
4. Laat in het veld **Doelversie** versie **2** van het basismodel **Voorbeeldauditmodel** staan.
5. Selecteer **OK** om de modeltoewijzing opnieuw te maken en uw indeling af te stemmen op recente wijzigingen in het gegevensmodel.
6. Selecteer **Ontwerper**.
7. Selecteer op de pagina **Indelingsontwerper**, in de opmaakstructuur in het linkerdeelvenster, de optie **Uitbreiden/Samenvouwen**.
8. Volg deze stappen om een nieuw indelingselement toe te voegen om recordidentificatiecodes te verzamelen van partijen waarvan transacties worden weergegeven in gegenereerde rapporten.

    1. Selecteer in de indelingsstructuur het volgorde-element **Report.Row.Trans**.
    2. Selecteer **Toevoegen**.
    3. Selecteer in het dialoogvenster **Toevoegen** de optie **Gegevensbron \> Item**.
    4. Voer in het dialoogvenster **Onderdeeleigenschappen**, in het veld **Naam**, **Id** in.
    5. Selecteer **Int64** in het veld **Gegevenstype**.
    6. Selecteer **OK**.

    > [!NOTE]
    > Een element **Gegevensbron \> Item** kan alleen worden gebruikt voor het uitvoeren van interne berekeningen en gegevenstransformaties in de scope van de lopende indeling. Als u dit indelingselement toevoegt, kunt u de inhoud van een gegenereerd document daarom niet wijzigen.

9. Voer deze stappen uit om nieuwe indelingselementen toe te voegen om partijnamen in gegenereerde rapporten in te voeren:

    1. Selecteer het volgorde-element **Report.Row**.
    2. Selecteer **Toevoegen**.
    3. Selecteer in het dialoogvenster **Toevoegen** **Tekst \> Volgorde**.
    4. Voer in het dialoogvenster **Onderdeeleigenschappen**, in het veld **Naam**, **Partij** in.
    5. Selecteer **OK**.
    6. Selecteer het volgorde-element **Report.Row.Party**.
    7. Selecteer **Toevoegen**.
    8. Selecteer in het dialoogvenster **Toevoegen** **Tekst \> Tekenreeks**.
    9. Voer in het dialoogvenster **Onderdeeleigenschappen**, in het veld **Naam**, **Naam** in.
    10. Selecteer **OK**.

10. Volg deze stappen om een nieuwe gegevensbron toe te voegen om recordidentificatiecodes te verzamelen van partijen waarvan transacties worden weergegeven in gegenereerde rapporten.

    1. Selecteer op het tabblad **Toewijzing** de optie **Hoofdmap toevoegen**.
    2. Selecteer in het dialoogvenster **Gegevensbron toevoegen** de optie **Functies \> Gegevensverzameling**.
    3. Voer in het dialoogvenster **Gegevensbroneigenschappen Gegevensverzameling** in het veld **Naam** de waarde **PartyIds** in.
    4. Selecteer **Int64** in het veld **Itemtype**.
    5. Selecteer **OK**.

11. Volg deze stappen om een nieuwe binding toe te voegen om recordidentificatiecodes te verzamelen van partijen waarvan transacties worden weergegeven in gegenereerde rapporten.

    1. Selecteer in de indelingsstructuur het gegevensitem-element **Report.Row.Trans.Id**.
    2. Selecteer **Formule bewerken**.
    3. Voer de pagina **Formuleontwerper** de expressie `PartyIds.Collect(model.Transaction.Party.RecId)` in.
    4. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.

12. Voer deze stappen uit om nieuwe bindingen toe te voegen om partijnamen in gegenereerde rapporten in te voeren:

    1. Selecteer in de indelingsstructuur het volgorde-element **Report.Party**.
    2. Selecteer **Formule bewerken**.
    3. Voer de pagina **Formuleontwerper** de expressie `model.Party(PartyIds.Result)` in.
    4. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.
    5. Selecteer in de indelingsstructuur het volgorde-element **Report.Party.Name**.
    6. Selecteer op het tabblad **Toewijzing** het gegevensmodelveld `model.Party.Name`.
    7. Selecteer **Binden**.

    ![Structuur van de aangepaste ER-indeling op de pagina Indelingsontwerper.](./media/er-data-model-parameterized-calls-format2.png)

13. Selecteer **Opslaan** en sluit de pagina **Indelingsontwerper**.
14. Sluit de pagina **Model aan gegevensbrontoewijzing**.
15. Selecteer op het sneltabblad **Versies** voor versie **2.2** de optie **Status wijzigen** \> **Voltooien**. Selecteer vervolgens **OK**.

### <a name="run-the-adjusted-format"></a>De aangepaste indeling uitvoeren

1. Selecteer op de pagina **Configuraties** **Voorbeeldauditindeling** en selecteer **Uitvoeren** in het actievenster.
2. Selecteer in het dialoogvenster **ER-parameters** op het tabblad **Op te nemen records** de optie **Filter**.
3. Geef de voorwaarden op voor het selecteren van belastingtransacties van de boekstukken **PIV-110000004** en **INV-10000001**.
4. Selecteer **OK**.
5. Selecteer **OK**.
6. Controleer het gegenereerde document dat belastingtransacties bevat van de geselecteerde boekstukken en de namen van de overeenkomende klant en leverancier.

    ![Bekijk het voorbeeld van het gegenereerde document met belastingtransacties en partijnamen.](./media/er-data-model-parameterized-calls-output2.png)

7. Ga naar **Leveranciers** \> **Leveranciers** \> **Alle leveranciers** en controleer de details van het geselecteerde boekstuk **PIV-110000004**, inclusief de naam van de leverancier.

    ![Controleer de gegevens van het inkoopboekstuk op de pagina's Alle leveranciers en Factuurjournaal.](./media/er-data-model-parameterized-calls-review1.gif)

8. Ga naar **Klanten** \> **Klanten** \> **Alle klanten** en controleer de details van het geselecteerde boekstuk **INV-10000001**, inclusief de naam van de klant.

    ![Controleer de details van het verkoopboekstuk op pagina's Alle klanten en Geboekte btw.](./media/er-data-model-parameterized-calls-review2.gif)

Voor meer details over deze uitvoering van de ER-oplossing gebruikt u de ingebouwde ER-parser voor [prestatietracering](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Aanvullende bronnen

- [Ondersteuning van parameteraanroepen voor ER-gegevensbronnen van het type Berekend veld](er-calculated-field-type.md)
- [De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)
- [Gegevensbronnen voor GEGEVENSVERZAMELING in elektronische rapportageindelingen gebruiken](er-data-collection-data-sources.md)
- [ER-functie ValueInLarge](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
