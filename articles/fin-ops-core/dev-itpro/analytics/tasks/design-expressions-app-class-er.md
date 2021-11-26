---
title: ER-expressies ontwerpen om methoden voor toepassingsklassen aan te roepen
description: Dit onderwerp bevat informatie over het opnieuw gebruiken van de bestaande toepassingslogica in ER-configuraties (elektronische rapportage) door vereiste methoden van toepassingsklassen aan te roepen.
author: NickSelin
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81fae8d3603677afd7dd4b09b9073805f73582b4
ms.sourcegitcommit: e6b4844a71fbb9faa826852196197c65c5a0396f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2021
ms.locfileid: "7751701"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>ER-expressies ontwerpen om methoden voor toepassingsklassen aan te roepen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt behandeld hoe u de bestaande toepassingslogica hergebruikt in [Elektronische rapportage (ER)](../general-electronic-reporting.md)-configuraties door vereiste methoden van toepassingsklassen aan te roepen in ER-expressies. Waarden van argumenten voor het aanroepen van klassen kunnen dynamisch bepaald worden tijdens runtime. De waarden kunnen bijvoorbeeld gebaseerd worden op informatie in het parseerdocument, om de juistheid ervan te waarborgen.

In dit onderwerp ontwerpt u bijvoorbeeld een proces ontwerpt voor het parseren van inkomende bankafschriften voor het bijwerken van toepassingsgegevens. U ontvangt de binnenkomende bankafschriften als tekstbestanden (.txt)-bestanden met IBAN-codes (International Bank Account Number). Als onderdeel van het importproces van de bankafschriften moet u de juistheid van de IBAN-code valideren met behulp van de logica die al beschikbaar is.

## <a name="prerequisites"></a>Vereisten

De procedures in dit onderwerp zijn bedoeld voor gebruikers met de rol **Systeembeheerder** of **Elektronische rapportageontwikkelaar**.

De procedures kunnen worden voltooid met elke gegevensset.

Om ze te voltooien, moet u het volgende bestand downloaden en opslaan: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

In dit onderwerp maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf, Litware, Inc. Voordat u de procedures in dit onderwerp uitvoert, moet u daarom de volgende stappen uitvoeren.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Controleer op de pagina **Lokalisatieconfiguraties** of de configuratieprovider voor het voorbeeldbedrijf **Litware, Inc.** beschikbaar is en gemarkeerd is als actief. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md) uitvoeren.

## <a name="import-a-new-er-model-configuration"></a>Een nieuwe ER-modelconfiguratie importeren

1. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel voor de configuratieprovider **Microsoft**.
2. Selecteer **Opslagplaatsen**.
3. Selecteer op de pagina **Lokalisatieopslagplaatsen** de optie **Filters weergeven**.
4. Als u de record voor de algemene opslagplaats wilt selecteren, voegt u een veld voor het **naam** filter toe.
5. Voer in het veld **Naam** de tekst **Algemeen** in. Selecteer vervolgens de filteroperator **bevat**.
6. Selecteer **Toepassing**.
7. Selecteer **[Openen](../er-download-configurations-global-repo.md#open-configurations-repository)** om de lijst met ER-configuraties in de geselecteerde opslagplaats te controleren.
8. Selecteer op de pagina **Configuratieopslagplaats** in de configuratiestructuur **Betalingsmodel**.
9. Als op het sneltabblad **Versies** de knop **Importeren** beschikbaar is, selecteer die dan, en selecteer dan **Ja**.

    Als de knop **Importeren** niet beschikbaar is, hebt u de geselecteerde versie van de ER-configuratie **Betalingsmodel** al geïmporteerd.

10. Sluit de pagina **Configuratieopslagplaats** en sluit vervolgens de pagina **Lokalisatieopslagplaatsen**.

## <a name="add-a-new-er-format-configuration"></a>Een nieuwe ER-indelingsconfiguratie toevoegen

Voeg een nieuwe ER-indeling toe om inkomende bankafschriften in TXT-indeling te parseren.

1. Selecteer op de pagina **Lokalisatieconfiguraties** de tegel **Rapportconfiguraties**.
2. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel**.
3. Selecteer **Configuratie maken**. 
4. Voer de volgende stappen uit in het dialoogvenster:

    1. Voer in het veld **Nieuw** **Indeling gebaseerd op gegevensmodel PaymentModel** in.
    2. Typ in het veld **Naam** **Importindeling bankafschrift (voorbeeld)**.
    3. Selecteer **Ja** in het veld **Ondersteunt gegevensimport**.
    4. Selecteer **Configuratie maken** om de configuratie af te maken.

## <a name="design-the-er-format-configuration--format"></a>De configuratie voor de ER-indeling ontwerpen - Indeling

Ontwerp een ER-indeling die de verwachte structuur van het externe bestand in TXT-indeling vertegenwoordigt.

1. Selecteer voor de indelingsconfiguratie **Importindeling bankafschrift (voorbeeld)** die u hebt toegevoegd, de optie **Ontwerper**.
2. Selecteer op de pagina **Indelingsontwerper**, in de opmaakstructuur in het linkerdeelvenster, de optie **Hoofdmap toevoegen**.
3. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer in de boomstructuur **Tekst\\Reeks** om een indelingsonderdeel **Reeks** toe te voegen.
    2. Voer in het veld **Naam** **Hoofdmap** in.
    3. Selecteer in het veld **Speciale tekens** de optie **Nieuwe regel - Windows (CR LF)**. Op basis van deze instelling wordt elke regel in het parseerbestand beschouwd als een afzonderlijke record.
    4. Selecteer **OK**.

4. Selecteer **Toevoegen**.
5. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer in de structuur **Tekst\\Reeks**.
    2. Geef in het veld **Naam** de tekst **Rijen** op.
    3. Selecteer in het veld **Multiplicity** **Eén veel**. Op basis van deze instelling wordt verwacht dat ten minste één regel aanwezig is in het parseerbestand.
    4. Selecteer **OK**.

6. Selecteer **Hoofdmap\\Rijen** in de boomstructuur en selecteer **Reeks toevoegen**.
7. Voer de volgende stappen uit in het dialoogvenster:

    1. Voer in het veld **Naam** de tekst **Velden** in.
    2. Selecteer in het veld **Multipliciteit** de optie **Precies één**.
    3. Selecteer **OK**.

8. Selecteer **Hoofdmap\\Rijen\\Velden** en selecteer **Toevoegen**.
9. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer **Tekst\\Tekenreeks** in de boomstructuur.
    2. Geef in het veld **Naam** de tekst **IBAN** op.
    3.. Selecteer **OK**.

10. Selecteer **Opslaan**.

Volgens de configuratie bevat elke regel in het parseerbestand alleen de IBAN-code.

![De indelingsconfiguratie Importindeling bankafschrift (voorbeeld) op de pagina Indelingsontwerper.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>De configuratie voor de ER-indeling - Toewijzen aan een gegevensmodel

Ontwerp een ER-indelingstoewijzing die de informatie uit het parseerbestand gebruikt om een gegevensmodel in te vullen.

1. Selecteer op de pagina **Indelingsontwerper** in het actiedeelvenster de optie **Indeling toewijzen aan model**.
2. Selecteer **Nieuw** op de pagina **Model voor gegevensbrontoewijzing** in het actievenster.
3. Selecteer in het veld **Definitie** de optie **BankToCustomerDebitCreditNotificationInitiation**.
4. Voer in het veld **Naam** **Toewijzen aan gegevensmodel** in.
5. Selecteer **Opslaan**.
6. Selecteer **Ontwerper**.
7. Selecteer op de pagina **Ontwerper modeltoewijzing** in de boomstructuur **Typen gegevensbronnen** **Dynamics 365 for Operations\\Klasse**.
8. Selecteer in de sectie **Gegevensbronnen** de optie **Hoofdmap toevoegen** om een gegevensbron toe te voegen die de bestaande toepassingslogica voor de validatie van IBAN-codes aanroept.
9. Voer de volgende stappen uit in het dialoogvenster:

    1. Voer in het veld **Naam** de tekst **Check\_codes** in.
    2. Typ of selecteer **ISO7064** in het veld **Klasse**.
    3. Selecteer **OK**.

10. Volg deze stappen in de boomstructuur **Eigenschappen van gegevensbron**:

    1. Vouw de gegevensbron van de **indeling** uit.
    2. Vouw **indeling\\Root: Sequence(Root)** uit.
    3. Vouw **indeling\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)** uit.
    4. Vouw **indeling\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)** uit.

11. Volg deze stappen in de boomstructuur **Gegevensmodel**:

    1. Vouw het veld **Betalingen** van het gegevensmodel uit.
    2. Vouw **Betalingen\\Creditor Account(CreditorAccount)** uit.
    3. Vouw **Betalingen\\Creditor Account(CreditorAccount)\\Identificatie** uit.
    4. Vouw **Betalingen\\Creditor Account(CreditorAccount)\\Identificatie\\IBAN** uit.

12. Volg deze stappen om onderdelen van de geconfigureerde indeling te binden aan gegevensmodelvelden:

    1. Selecteer **indeling\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**.
    2. Selecteer **Betalingen**.
    3. Selecteer **Binden**. Op basis van deze instelling wordt elke regel in het parseerbestand beschouwd als één betaling.
    4. Selecteer **indeling\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)\\IBAN: String(IBAN)**.
    5. Selecteer **Betalingen\\Creditor Account(CreditorAccount)\\Identificatie\\IBAN**.
    6. Selecteer **Binden**. Op basis van deze instelling wordt het veld **IBAN** van het gegevensmodel gevuld met de waarde van het parseerbestand.

    ![Binding van indelingsonderdelen aan gegevensmodelvelden op de pagina Modeltoewijzingsontwerper.](../media/design-expressions-app-class-er-02.png)

13. Op het tabblad **Validaties** volgt u deze stappen om een [validatie](../general-electronic-reporting-formula-designer.md#Validation)regel toe te voegen die een foutmelding geeft voor elke regel in het parseerbestand die een ongeldige IBAN-code bevat:

    1. Selecteer **Nieuw** en selecteer vervolgens **Voorwaarde bewerken**.
    2. Vouw op de pagina **Formuleontwerper** in de boomstructuur **Gegevensbron** de gegevensbron **Check\_codes** uit die de toepassingsklasse **ISO7064** vertegenwoordigt om de beschikbare methoden van deze klasse weer te geven.
    3. Selecteer **Check\_codes\\verifyMOD1271\_36**.
    4. Selecteer **Gegevensbron toevoegen**.
    5. Typ in het veld **Formule** de volgende [expressie](../general-electronic-reporting-formula-designer.md#Binding): **Check\_codes.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)**.
    6. Selecteer **Opslaan** en sluit de pagina.
    7. Selecteer **Bericht bewerken**.
    8. Typ op de pagina **Formuleontwerper** in het veld **Formule** het volgende: **CONCATENATE("Ongeldige IBAN-code gevonden:&nbsp;", format.Root.Rows.Fields.IBAN)**.
    9. Selecteer **Opslaan** en sluit de pagina.

    Op basis van deze instellingen retourneert de validatievoorwaarde *[FALSE](../er-formula-supported-data-types-primitive.md#boolean)* voor elke ongeldige IBAN-code door de bestaande methode **verifyMOD1271\_36** van de **ISO7064**-toepassingsklasse aan te roepen. Houd er rekening mee dat de waarde van de IBAN-code dynamisch wordt gedefinieerd tijdens de uitvoering als het argument van de aanroepende methode op basis van de inhoud van het tekst-parseerbestand.

    ![Validatieregel op de pagina Ontwerper modeltoewijzing.](../media/design-expressions-app-class-er-03.png)

14. Selecteer **Opslaan**.
15. Sluit de pagina **Ontwerper modeltoewijzing** en sluit de pagina **Model voor gegevensbrontoewijzing**.

## <a name="run-the-format-mapping"></a>De toewijzing van de bestandsindeling uitvoeren

Voer voor testdoeleinden de toewijzing van de indeling uit met behulp van het SampleIncomingMessage.txt-bestand dat u eerder hebt gedownload. De gegenereerde uitvoer omvat gegevens die worden geïmporteerd vanuit het geselecteerde tekstbestand en overgezet naar het aangepaste gegevensmodel tijdens de daadwerkelijke import.

1. Selecteer **Uitvoeren** op de pagina **Model voor gegevensbrontoewijzing** .
2. Op de pagina **Parameters voor elektronische rapporten** kiest u **Bladeren**, bladert u naar het bestand **SampleIncomingMessage.txt** dat u gedownload hebt, en selecteert u het.
3. Selecteer **OK**.
4. Merk op dat de pagina **Model voor gegevensbrontoewijzing** een foutmelding geeft over een ongeldige IBAN-code.

    ![Resultaat van uitvoering van de indelingstoewijzing op de pagina Model voor gegevensbrontoewijzing.](../media/design-expressions-app-class-er-04.png)

5. Bekijk de uitvoer in XML-indeling, die de gegevens vertegenwoordigt die zijn geïmporteerd vanuit het geselecteerde bestand en overgezet naar het gegevensmodel. Er zijn slechts drie regels van het geïmporteerde tekstbestand verwerkt zonder fouten. De IBAN-code op regel 4 is niet geldig en is overgeslagen.

    ![XML-uitvoer.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
