---
title: Gegevensbronnen voor GEGEVENSVERZAMELING in elektronische rapportageindelingen gebruiken
description: In dit onderwerp wordt uitgelegd hoe u gegevensbronnen voor GEGEVENSVERZAMELING kunt gebruiken in elektronische rapportageindelingen (ER).
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: f001734baf9aee59f0a61d21ca5a99af0c55b56f
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413588"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>Gegevensbronnen voor GEGEVENSVERZAMELING in elektronische rapportageindelingen gebruiken

[!include [banner](../includes/banner.md)]

U kunt de Operations-ontwerper van het [ER](general-electronic-reporting.md)-raamwerk gebruiken om de [indelings](general-electronic-reporting.md#FormatComponentOutbound)component te configureren van een ER-oplossing die wordt gebruikt om uitgaande documenten in verschillende indelingen te genereren. De hiërarchische structuur van de geconfigureerde indelingscomponent bestaat uit indelingselementen van verschillende typen. Deze indelingselementen worden gebruikt om gegenereerde documenten te vullen met de vereiste informatie tijdens runtime. Wanneer u een ER-indeling uitvoert, worden de indelingselementen standaard in dezelfde volgorde uitgevoerd als waarin deze worden weergegeven in de opmaakhiërarchie: één voor één, van boven naar beneden.

Wanneer er een opmaakelement via ER wordt uitgevoerd dat een binding bevat, wordt de formule van die binding uitgevoerd en voegt het opmaakelement de waarde toe aan een gegenereerd document. De binding kan bijvoorbeeld de waarde van een [gegevensmodel](general-electronic-reporting.md#data-model-and-model-mapping-components)veld doorgeven aan een opmaakelement. U kunt een gegevensbron voor GEGEVENSVERZAMELING dusdanig configureren dat het waarden van gegevensmodelvelden tijdens runtime verzamelt, deze waarden optelt en een gegenereerd document met de verzamelde waarden vult. Om deze benadering te gebruiken, wijzigt u de eerste binding dusdanig dat de geconfigureerde gegevensbron voor GEGEVENSVERZAMELING wordt gebruikt om de waarde van een gegevensmodelveld aan een opmaakelement door te geven. Door waarden via de gegevensbron voor GEGEVENSVERZAMELING door te geven, kunt u de vereiste gegevens voor verder gebruik verzamelen.

Wanneer u een gegevensbron voor GEGEVENSVERZAMELING configureert, geeft u een waardetype op dat in de gegevensbron zal worden beheerd. De volgende [gegevenstypen](er-formula-supported-data-types-primitive.md) worden momenteel ondersteund voor het verzamelen van waarden:

- Booleaans
- Datum
- DateTime
- Guid
- Int64
- Geheel getal
- Real-modus
- Tekenreeks
- Tijd

U kunt de `Collect(Value)` methode van een gegevensbron voor GEGEVENSVERZAMELING gebruiken om een waarde voor verzameling door te geven aan een gegevensbron. Bij deze methode is het `Value`-argument een constante of het geldige pad van een gegevensbronveld van het relevante gegevenstype.

Gebruik de `Result`-eigenschap van een gegevensbron voor GEGEVENSVERZAMELING om toegang te krijgen tot de lijst met verzamelde waarden. Deze eigenschap levert een [recordlijst](er-formula-supported-data-types-composite.md#record-list) op. De records in de recordlijst bevatten het veld `Value` dat u kunt gebruiken om de verzamelde waarden te openen.

Een gegevensbron voor GEGEVENSVERZAMELING verzamelt standaard alleen unieke waarden.

Als u alle waarden wilt verzamelen, stelt u het veld **Alle waarden verzamelen** van de geconfigureerde gegevensbron voor GEGEVENSVERZAMELING in op **Ja**. Wanneer het veld **Alle waarden verzamelen** ingesteld is op **Ja**, wordt de geparametriseerde `Sum(Flag)`-eigenschap beschikbaar. U kunt deze eigenschap gebruiken om het totaalbedrag op te halen van alle waarden die op dat moment verzameld zijn. In deze eigenschap is het `Flag`-argument een [Booleaanse](er-formula-supported-data-types-primitive.md#boolean) waarde die wordt gebruikt om aan te geven of de totale waarde opnieuw moet worden ingesteld.

- Wanneer de waarde **False** is opgegeven, wordt de som van het eerder verzamelde bedrag doorgezet.
- Wanneer de waarde **True** is opgegeven, wordt begonnen met het nieuwe totaal.

De volgende gegevenstypen worden momenteel ondersteund voor het optellen:

- Int64
- Geheel getal
- Real-modus

Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Voorbeeld: een ER-indeling dusdanig configureren dat het op(telt) met behulp van een gegevensbron voor GEGEVENSVERZAMELING

Dit voorbeeld laat zien hoe een gebruiker met de rol Systeembeheerder of Functioneel consultant voor elektronische rapportage een ER-indeling kan configureren met een gegevensbron voor GEGEVENSVERZAMELING die gebruikt wordt om lopende totalen te berekenen en opgetelde waarden te verzamelen.

De procedures in dit voorbeeld kunnen in het bedrijf USMF worden uitgevoerd in Microsoft Dynamics 365 Finance.

### <a name="upload-and-use-the-provided-er-solution"></a>De geleverde ER-oplossing uploaden en gebruiken

1. [De ER-voorbeeldconfiguraties importeren](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Een configuratieprovider activeren](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [De geïmporteerde modeltoewijzing controleren](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [De geïmporteerde indeling controleren](er-defer-sequence-element.md#review-the-imported-format).
5. [De geïmporteerde indeling uitvoeren](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>De indeling van de aangeleverde ER-oplossing uitvoeren

1. Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.
2. Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport**.
3. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand dat de resultaten bevat van de uitvoering van de oorspronkelijke indeling](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>De indeling van de ER-oplossing wijzigen om het lopende btw-totaal te berekenen

Als het volume van transacties veel groter is dan het volume in het huidige voorbeeld, kan de opteltijd toenemen en resulteren in prestatieproblemen. Door de instellingen van de indeling te wijzigen, kunt u deze prestatieproblemen voorkomen. Aangezien u toegang tot belastingswaarden hebt om deze op te nemen in het gegenereerde rapport, kunt u deze informatie opnieuw gebruiken om belastingswaarden op te tellen.

1. Selecteer op de pagina **Indelingsontwerper** in het tabblad **Toewijzing** de optie **Root toevoegen**.
2. Selecteer in het dialoogvenster **Gegevensbron toevoegen** de optie **Functies** \> **Gegevensverzameling**.
3. Volg deze stappen in het dialoogvenster **'Gegevensverzameling'-gegevensbroneigenschappen**:

    1. Voer in het veld **Naam** de waarde **Verzamelde belastingwaarden** in.
    2. Selecteer in het veld **Itemtype** **Werkelijk**.
    3. Selecteer **Ja** in het veld **Alle waarden verzamelen**.
    4. Selecteer **OK**.

4. Selecteer het opmaakelement **Rapport\\Regels\\Record\\BelastingBedrag**.

    > [!NOTE]
    > Op dit moment wordt de `@.Value`-binding voor dit element geconfigureerd. Daarom wordt een gegenereerd document gevuld met btw-waarden uit het veld `model.Data.List.Value`.

5. Selecteer **Formule bewerken**.
6. Voer op de pagina **Formuleontwerper** de volgende stappen uit:

    1. Vervang in het veld **Formule** `@.Value` door `CollectedTaxValues.Collect(@.Value)`.
    2. Sla uw wijzigingen op en sluit de pagina.

    > [!NOTE]
    > Via de nieuwe binding worden dezelfde btw-waarden aan een gegenereerd document doorgegeven. Deze waarden worden echter ook verzameld in de gegevensbron **Verzamelde btw-waarden**.

7. Selecteer het opmaakelement **Rapport\\Regels\\Record\\BelastingBedrag**.
8. Selecteer **Formule bewerken**.
9. Voer op de pagina **Formuleontwerper** de volgende stappen uit:

    1. Voer in het veld **Formule** `CollectedTaxValues.Sum(false)` in.
    2. Sla uw wijzigingen op en sluit de pagina.

    > [!NOTE]
    > De nieuwe binding geeft, in een gegenereerd document, het totaalbedrag van de belastingwaarden door die al zijn ingevoerd.

    ![Numerieke elementen die bijgewerkte bindingen hebben op de pagina Opmaakontwerper](./media/er-data-collection-data-sources-02.png)

10. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
11. Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport**.
12. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand dat de resultaten bevat van de uitvoering van de gewijzigde indeling](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>De opmaak wijzigen om de lijst met verzamelde btw-waarden te evalueren

1. Selecteer op de pagina **Opmaakontwerper** in het tabblad **Opmaak** het numerieke opmaakelement **Rapport\\Regels\\Record\\RunningTotaal** en volg vervolgens deze stappen:

    1. Wijzig in het veld **Numeriek type** de waarde van **Real** in **Geheel getal**.
    2. Wijzig in het veld **Numerieke opmaak** de waarde van **F2** in **F0**.

3. Selecteer in het tabblad **Toewijzing** de optie **Formule bewerken**.
4. Voer op de pagina **Formuleontwerper** de volgende stappen uit:

    1. Voer in het veld **Formule** `COUNT(CollectedTaxValues.Result)` in.
    2. Sla uw wijzigingen op en sluit de pagina.

    > [!NOTE]
    > De nieuwe binding draagt, in een gegenereerd document, het aantal records in de lijst over waar de btw-waarden worden verzameld.

5. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
6. Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport**.
7. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand dat de resultaten bevat van de uitvoering van nog een gewijzigde indeling](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Wat is het verschil tussen het gebruik van een gegevensbron voor GEGEVENSVERZAMELING en het gebruik van de ingebouwde functies voor GEGEVENSVERZAMELING als ik lopende totalen moet berekenen en gegevens moet verzamelen?

Zowel een gegevensbron voor GEGEVENSVERZAMELING als de ingebouwde functies voor [GEGEVENSVERZAMELING](er-functions-category-data-collection.md) kunnen worden gebruikt voor het verzamelen, samenvatten en optellen van gegevens op basis van informatie die wordt doorgegeven aan een gegenereerd uitgaand document. Wanneer u echter probeert te bepalen welke techniek u wilt gebruiken, moet u rekening houden met de volgende punten.

| Gegevensbron | Ingebouwde functies |
|-------------| ------------------ |
| Er worden alleen waarden verzameld. | <p>Er worden benoemde waarden verzameld. Totalen kunnen dus worden berekend voor afzonderlijke waardengroepen.</p><p>Bovendien kunnen groepen als een lijst worden geëxtraheerd.</p><p>Er kunnen ook tekstwaarden worden verzameld.</p> |
| Er worden automatisch unieke waarden verzameld. | Er zijn aanvullende instellingen nodig om een lijst met unieke waarden op te halen uit de verzamelde waarden. |
| De prestaties zijn afhankelijk van het volume van de verzamelde waarden. | In de praktijk zijn de prestaties niet afhankelijk van het volume van de verzamelde waarden. |
| Deze techniek werkt voor alle soorten uitgaande documenten. | Deze techniek werkt alleen voor tekst- en XML-documenten. |

## <a name="additional-resources"></a>Aanvullende bronnen

- [Indeling configureren voor tellen en totaliseren](./tasks/er-format-counting-summing-1.md)
- [De uitvoering van reekselementen in ER-indelingen uitstellen](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
