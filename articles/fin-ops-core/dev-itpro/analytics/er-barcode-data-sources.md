---
title: Gegevensbronnen voor streepjescodes gebruiken om streepjescode-afbeeldingen te genereren
description: In dit onderwerp wordt uitgelegd hoe u gegevensbronnen voor streepjescodes gebruikt om streepjescode-afbeeldingen te genereren.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: cbc2b5870e855ff4d4a099a51cbb6887dd30bba7
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893547"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Gegevensbronnen voor streepjescodes gebruiken om streepjescode-afbeeldingen te genereren

[!include[banner](../includes/banner.md)]

U kunt het [ER-raamwerk (elektronische rapportage)](general-electronic-reporting.md) gebruiken om [ER-opmaakcomponenten](general-electronic-reporting.md#FormatComponentOutbound) te ontwerpen die u kunt uitvoeren om elektronische en afdrukbare uitgaande documenten te genereren die u nodig hebt. Als u een uitgaand document in Microsoft Office-formaat wilt genereren, moet u de rapportindeling opgeven door een Microsoft Excel-document of Microsoft Word-document te gebruiken als rapportsjabloon. In de [ER Operations-ontwerper](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) kunt u een Excel- of Word-document als sjabloon voor een ER-indeling koppelen. De volgende benoemde elementen in de gekoppelde sjabloon hangen samen met de elementen van de geconfigureerde opmaakcomponent:

- Inhoudsbesturingselementen in Word
- Benoemde bladen, bereiken, cellen, vormen en afbeeldingen in Excel

Deze benoemde elementen worden gebruikt als tijdelijke aanduidingen voor gegevens die in een gegenereerd document worden ingevoerd wanneer een ER-indeling wordt uitgevoerd. ER-opmaakelementen zijn gebonden aan gegevensbronnen. In deze gegevens bronnen worden de gegevens opgegeven die tijdens runtime in de gegenereerde documenten worden ingevoerd. Zie [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md) voor meer informatie.

Het gegevensbrontype **Streepjescode** wordt nu ondersteund in ER. Daarom kunt u nu een afbeelding genereren die de streepjescode voor de opgegeven tekst vertegenwoordigt. Wanneer u een ER-indeling configureert, kunt u gegevensbronnen van het type **Streepjescode** opgeven om streepjescode-afbeeldingen te genereren. U kunt deze afbeeldingen vervolgens toevoegen aan gegenereerde bedrijfsdocumenten, zoals orders, facturen, pakbonnen en ontvangstbewijzen. U kunt ze ook toevoegen aan verschillende soorten etiketten, zoals product- en planketiketten, en verpakkings- en verzendlabels.

U kunt de volgende tijdelijke aanduidingen in rapportsjablonen gebruiken om streepjescode-afbeeldingen in te voeren:

- Inhoudsbesturingselement voor [afbeeldingen](/office/client-developer/word/content-controls-in-word) voor Word
- [Afbeeldings](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344)object in Excel

Door een gegevensbron van het type **Streepjescode** te gebruiken, kunt u streepjescodes genereren in de volgende indelingen:

- Eendimensionale streepjescodes:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Intelligent Mail
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Tweedimensionale streepjescodes:

    - Aztec
    - Data Matrix
    - QR-code

Wanneer u een gegevensbron voor een **Streepjescode** configureert, kunt u specifieke weergaveparameters definiëren die worden gebruikt om een afbeelding te genereren:

- **Breedte**: geef de breedte van de streepjescode op in pixels. De waarde **0** (nul) geeft aan dat de standaardbreedte wordt gebruikt. De betekenis kan per indeling verschillen.
- **Hoogte**: geef de hoogte van de streepjescode op in pixels. De waarde **0** (nul) geeft aan dat de standaardhoogte wordt gebruikt. De betekenis kan per indeling verschillen.
- **Marge**: geef de grootte van de marge van de streepjescode op in pixels. De marge is het gebied aan beide zijden van een streepjescode dat vrij moet blijven (stille zone). De waarde **0** (nul) geeft aan dat de standaardmarge wordt gebruikt. De betekenis kan per indeling verschillen.
- **Uitvoerinhoud**: stel de waarde in op **Ja** om een streepjescode-afbeelding te maken die de gecodeerde informatie als tekst bevat. De standaardwaarde is **Nee**.
- **Codering**: geef het type tekens op dat is gecodeerd in de gegenereerde afbeelding van de streepjescode. Standaard wordt de **UTF-8**-codering gebruikt.

> [!IMPORTANT]
> Wanneer u een nieuwe gegevensbron voor een **Streepjescode** toevoegt, moet u deze onder een ander item (container) plaatsen als een genest element.
>
> Wanneer u een gegevensbron voor een **Streepjescode** koppelt aan een celelement in een indeling en het celelement een inhoudsbesturingselement van Word of een Excel-afbeelding vertegenwoordigt, wordt de gegevensbron in die binding weergegeven als een functie met één parameter van het type **Tekenreeks**. U moet deze parameter gebruiken om de tekst op te geven die moet worden omgezet in een streepjescode-afbeelding en die moet worden gelezen wanneer een gegenereerde streepjescode wordt gescand.

Voor meer informatie over deze functie kunt u de voorbeelden in dit onderwerp uitvoeren.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Voorbeeld: een betaalcheque genereren die een streepjescode bevat waarmee het te betalen bedrag wordt gecodeerd

In dit voorbeeld ziet u hoe een gebruiker in de rol **systeembeheerder** of **ER-consultant** een ER-indeling kan configureren die een sjabloon bevat waarmee een uitgaand document met streepjescode wordt gegenereerd in de Excel-indeling. Hier volgt een overzicht van de stappen die hierbij worden uitgevoerd.

1. [Voldoen aan de vereisten](#ExamplePrerequisites).
2. [Een configuratieprovider activeren](#ExampleProvider).
3. [De geleverde ER-oplossing importeren](#ExampleImportSolution).
4. [Een betaalcheque genereren](#ExampleGenerateCheque)
5. [De gegenereerde betaalcheque controleren](#ExampleReviewGeneratedCheque).
6. [De indeling van de aangeleverde ER-oplossing wijzigen](#ExampleModifyFormat).

    1. [Een nieuwe chequesjabloon toepassen](#ExampleModifyFormatApplyTemplate).
    2. [Een nieuwe gegevensbron voor streepjescode toevoegen](#ExampleModifyFormatAddDataSource).
    3. [Een nieuw opmaakelement binden](#ExampleModifyFormatBindFormatElement).
    4. [De gewijzigde versie beschikbaar maken voor testruns](#ExampleModifyFormatMakeVersionAvailable).

        1. [De gewijzigde indelingsversie voltooien](#CompleteToRun).
        2. [De conceptversie beschikbaar maken voor gebruik](#MarkToRun).

7. [Een betaalcheque genereren](#ExampleGenerateCheque2)
8. [De gegenereerde cheque converteren naar een PDF](#ExampleConvertToPDF).

In dit voorbeeld gebruikt u de geleverde ER-oplossing die is geconfigureerd voor het genereren van betaalcheques. Met deze oplossing worden betaalcheques gegenereerd waarbij het te betalen bedrag als een getal en als tekst wordt geschreven. U gaat deze ER-oplossing aanpassen zodat de cheque ook een gegenereerde streepjescode bevat waarin het te betalen bedrag is gecodeerd en kan worden gelezen met behulp van een streepjescodescanner.

De stappen kunnen worden uitgevoerd in het bedrijf **USMF** in Microsoft Dynamics 365 Finance.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Voldoen aan de vereisten

Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot het bedrijf USMF in Finance voor een van de volgende rollen:

- Functioneel consultant elektronische rapportage
- Systeembeheerder

Als u het voorbeeld nog niet hebt voltooid in het onderwerp [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md), downloadt u de volgende configuraties van de voorbeeld-ER-oplossing.

| Omschrijving inhoud         | Bestandsnaam                   |
|-----------------------------|-----------------------------|
| Configuratie van model voor ER-gegevens | Model for cheques.xml       |
| ER-indelingsconfiguratie     | Cheques printing format.xml |

Download ook het volgende Excel-bestand dat de gewijzigde sjabloon bevat voor de meegeleverde ER-oplossing.

| Omschrijving inhoud | Bestandsnaam                 |
|---------------------|---------------------------|
| Rapportsjabloon     | Check template Excel.xlsx |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Een configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Controleer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** of de [configuratieprovider](general-electronic-reporting.md#Provider) voor het voorbeeldbedrijf **Litware, Inc.** wordt vermeld en of het is gemarkeerd als Actief. Als deze niet wordt vermeld of als deze niet is gemarkeerd als actief, volgt u de stappen in het onderwerp [Een configuratieprovider maken en als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Het voorbeeldbedrijf op actief instellen op de pagina Lokalisatieconfiguraties](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>De geleverde ER-oplossing importeren.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Als op de pagina **Configuraties** de configuratie **Model voor cheques** niet beschikbaar is in de configuratiestructuur, importeert u als volgt de ER-gegevensmodelconfiguratie:

    1. In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.
    2. Selecteer **Bladeren** in het dialoogvenster, zoek en selecteer het bestand **Model for cheques.xml** en selecteer **OK**.

4. Als de configuratie **Afdrukindeling van cheques** niet beschikbaar is in de configuratiestructuur, importeert u als volgt de ER-gegevensmodelconfiguratie:

    1. In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.
    2. Selecteer **Bladeren** in het dialoogvenster, zoek en selecteer het bestand **Cheques printing format.xml** en selecteer **OK**.

5. Vouw in de configuratiestructuur **Model voor cheques** uit.
6. Bekijk de lijst met geïmporteerde ER-configuraties in de configuratiestructuur.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Een betaalcheque genereren

1. Ga naar **Contanten en bankbeheer** \> **Bankrekeningen** \> **Bankrekeningen**.
2. Selecteer op de pagina **Bankrekeningen** de rekening **USMF OPER**.
3. Selecteer **Cheque** op de pagina met bankrekeningdetails in het actievenster op het tabblad **Instellen** in de groep **indeling**.
4. Selecteer **Bewerken** op de pagina **Cheque-indeling**.
5. Stel op het sneltabblad **Algemeen** de optie **Algemene elektronische exportindeling** in op **Ja**.
6. Selecteer in het veld **Indelingsconfiguratie exporteren** de ER-indeling **Afdrukindeling van cheques** die u eerder hebt geïmporteerd.
7. Selecteer **Test afdrukken** in het actievenster.
8. Stel in het dialoogvenster de optie **Overdraagbare cheque-indeling** in op **Ja** en selecteer **OK**.

    ![Dialoogvenster Cheque-indeling - Test afdrukken](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>De gegenereerde betaalcheque controleren

- Open de gegenereerde cheque in Excel.
2. Controleer de gegenereerde cheque.

    ![Ggenereerde betaalcheque in Excel](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>De indeling van de aangeleverde ER-oplossing wijzigen

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Een nieuwe chequesjabloon toepassen

U kunt de Excel-bureaubladtoepassing gebruiken om het bestand **Cheque template Excel.xlsx** te openen dat u eerder hebt geïmporteerd. Deze sjabloon wijkt af van de sjabloon die u hebt gebruikt om een betaalcheque te genereren in de geleverde oplossing. Daarnaast bevat het een **AmountBarcode**-element voor de streepjescode-afbeelding.

![AmountBarcode-element in de Excel-sjabloon](./media/er-barcode-data-source-cheque2.png)

U moet nu de ER-oplossing wijzigen en vervolgens de gewijzigde sjabloon [opnieuw toepassen](modify-electronic-reporting-format-reapply-excel-template.md).

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de optie **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur **Model voor cheques** uit en selecteer **Afdrukindeling van cheques**.
4. Selecteer **Ontwerper** in het actievenster.
5. Selecteer in de ER Operations-ontwerper het tabblad **Toewijzing** aan de rechterkant van de pagina en selecteer vervolgens **Uitvouwen/samenvouwen** in het venster met de opmaakstructuur.
6. U ziet dat alle celopmaakelementen afhankelijk zijn van de desbetreffende gegevensbronnen.

    ![Binding van celopmaakelementen aan gegevensbronnen koppelen in de ER Operations-ontwerper](./media/er-barcode-data-source-cells-bound.png)

7. Selecteer het tabblad **Opmaak** aan de rechterkant van de pagina.
8. Selecteer in het actievenster het weglatingsteken (**...**) en selecteer **Importeren**.
9. Selecteer in de groep **Importeren** de optie **Bijwerken vanuit Excel** en selecteer vervolgens **Sjabloon bijwerken**.
10. Blader in het dialoogvenster naar het bestand **Cheque template Excel.xlsx** dat op uw computer is opgeslagen, selecteer het bestand en selecteer **OK** om te bevestigen dat de geselecteerde sjabloon moet worden toegepast.
11. Selecteer het tabblad **Toewijzing** aan de rechterkant van de pagina en selecteer vervolgens **Uitvouwen/samenvouwen** in het venster met de opmaakstructuur.
12. U ziet dat het celelement **AmountBarcode** aan de indeling is toegevoegd. Dit element is gekoppeld aan het element **AmountBarcode** dat aan de gewijzigde Excel-sjabloon is toegevoegd als tijdelijke aanduiding voor een streepjescode-afbeelding.

    ![Celelement AmountBarcode toegevoegd aan de indeling in de ER Operations-ontwerper](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Een nieuwe gegevensbron voor streepjescode toevoegen.

Vervolgens moet u een nieuwe gegevensbron toevoegen voor het type **Streepjescode**.

1. Selecteer in de ER Operations-ontwerper op het tabblad **Toewijzing** aan de rechterkant van de pagina de gegevensbron **print**.
2. Selecteer **Toevoegen** en vervolgens in de groep **Functies** het gegevensbrontype **Streepjescode**.

    ![Het gegevensbrontype Streepjescode selecteren](./media/er-barcode-data-source-add.png)

3. Voer in het dialoogvenster in het veld **Naam** de tekst **barcode** in.
4. Selecteer **Code 128** bij **Indeling streepjescode**.
5. Typ **500** in het veld **Breedte**.
6. Selecteer **OK**.

    ![Dialoogvenster Gegevensbroneigenschappen](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Een nieuw opmaakelement binden

Vervolgens moet u het nieuwe opmaakelement binden aan de gegevensbron die u zojuist hebt toegevoegd.

1. Selecteer in de ER Operations-ontwerper op het tabblad **Toewijzing** aan de rechterkant van de pagina de gegevensbron **print\\barcode**.
2. Selecteer in het deelvenster met de opmaakstructuur het celelement **AmountBarcode** en vervolgens **Binden**.
3. Selecteer **Details weergeven** in het actievenster.
4. Omdat de gegevensbron **Streepjescode** in de binding wordt weergegeven als een functie die één parameter bevat, wordt de naam van het gebonden opmaakelement automatisch als argument van die parameter beschouwd.

    ![Details van de gegevensbron Streepjescode in de ER Operations-ontwerper](./media/er-barcode-data-source-bind1.png)

5. Selecteer **Formule bewerken** om de binding aan te passen.

    U wilt niet dat de naam van het celelement als resultaat wordt gegeven. Daarom moet u een expressie configureren die tekst retourneert die het te betalen bedrag van de huidige cheque bevat. Omdat het bovenliggende bereik **ChequeLines** aan de gegevensbron **model.cheques** is gebonden, is het te betalen bedrag van de huidige cheque beschikbaar in het veld **model.cheques.attributs.amount** van het gegevenstype **Werkelijk**.

6. Voer in het veld **Formule** **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))** in.
7. Selecteer **Opslaan** en sluit de [ER Operations-ontwerper](general-electronic-reporting-formula-designer.md).
8. Zoals u ziet, is de binding aangepast.

    ![Aangepaste binding in de ER Operations-ontwerper](./media/er-barcode-data-source-bind2.png)

9. Selecteer **Opslaan** en sluit de ER Operations-ontwerper.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>De gewijzigde versie beschikbaar maken voor testruns

Standaard worden alleen de versies met de status **Voltooid** en **Gedeeld** gebruikt wanneer u een ER-indeling uitvoert.

Als u uw wijzigingen hebt voltooid, kunt u uw werk met de huidige conceptversie voltooien en uw wijzigingen beschikbaar maken voor gebruik. Zie de sectie [Gewijzigde indelingsversie voltooien](#CompleteToRun) hieronder voor instructies.

Als u wilt doorgaan met de huidige conceptversie, maar u deze wilt gebruiken om cheques te genereren, moet u expliciet opgeven dat u de conceptversie van de indeling voor uitvoering wilt gebruiken. Zie de sectie [De conceptversie beschikbaar maken voor gebruik](#MarkToRun) voor instructies.

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>De gewijzigde indelingsversie voltooien

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de optie **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur **Model voor cheques** uit en selecteer **Afdrukindeling van cheques**.
4. Selecteer op het sneltabblad **Versies** de record met de status **Concept**.
5. Selecteer **Status wijzigen** en selecteer **Voltooien**.
6. Selecteer **OK** in het dialoogvenster.

De status van de huidige versie wordt gewijzigd van **Concept** in **Voltooid** en een nieuwe versie met de status **Concept** wordt gemaakt. U kunt deze nieuwe conceptversie gebruiken om extra wijzigingen toe te passen.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>De conceptversie beschikbaar maken voor gebruik

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de optie **Rapportconfiguraties**.
3. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
4. Stel in het dialoogvenster de optie **Instelling uitvoeren** in op **Ja** en selecteer **OK**.
5. Vouw in de configuratiestructuur **Model voor cheques** uit en selecteer **Afdrukindeling van cheques**.
6. Stel de optie **Concept uitvoeren** in op **Ja**.
7. Selecteer **Opslaan**.

De conceptversie van de geselecteerde indeling wordt gemarkeerd als beschikbaar voor gebruik wanneer de geselecteerde indeling wordt uitgevoerd.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Een betaalcheque genereren

1. Ga naar **Contanten en bankbeheer** \> **Bankrekeningen** \> **Bankrekeningen**.
2. Selecteer op de pagina **Bankrekeningen** de rekening **USMF OPER**.
3. Selecteer **Cheque** op de pagina met bankrekeningdetails in het actievenster op het tabblad **Instellen** in de groep **indeling**.
4. Selecteer op de pagina **Cheque-indeling** in het actievenster de optie **Test afdrukken**.
5. Stel in het dialoogvenster de optie **Overdraagbare cheque-indeling** in op **Ja**.
6. Selecteer **OK**.
7. Controleer de gegenereerde cheque. U ziet dat er een streepjescode is gegenereerd om het te betalen bedrag van de cheque te coderen.

    ![Gegenereerde betaalcheque met streepjescode in Excel](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Er wordt een uitzondering gegenereerd als het argument van een gegevensbron **Streepjescode** niet voldoet aan de toepasselijke vereisten die specifiek zijn voor de opmaak van de streepjescode. Als de gegevensbron **Streepjescode** bijvoorbeeld wordt aangeroepen om een [EAN-8](https://wikipedia.org/wiki/EAN-8)-streepjescode te genereren voor de opgegeven tekst, wordt er een uitzondering gegenereerd als de lengte van de tekst langer is dan zeven tekens.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>De gegenereerde cheque converteren naar een PDF

Zoals wordt beschreven in het onderwerp [Afdrukbare FTI-formulieren genereren](er-generate-printable-fti-forms.md#finland), kunt u een speciaal lettertype gebruiken om streepjescodes te produceren in een gegenereerd document. In dit geval is het mogelijk dat extra transformaties van het gegenereerde document afhankelijk zijn van de beschikbaarheid van dat lettertype in de transformatie-omgeving. Als u bijvoorbeeld een document wilt converteren naar PDF-indeling of als voorbeeld wilt weergeven in een omgeving waarin het lettertype ontbreekt, worden streepjescodes niet goed weergegeven.

Wanneer u de gegevensbron **Streepjescode** gebruikt om streepjescodes te produceren, is de weergave van die streepjescodes echter niet afhankelijk van het lettertype. Daarom kunt u documenten die streepjescodes bevatten, eenvoudig converteren naar PDF-indeling. In de volgende afbeelding ziet u een voorbeeld van een gegenereerde betaalcheque die is [geconverteerd](electronic-reporting-destinations.md#OutputConversionToPDF) naar een PDF, op basis van de instelling van de geconfigureerde [ER-bestemming](electronic-reporting-destinations.md).

![Voorbeeld van de PDF van een betaalcheque](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Beperkingen

> [!NOTE]
> Sommige typen streepjescodes worden gegenereerd met een vaste hoogte-breedteverhouding. Dit gedrag is zinvol als u de functie **Gebruik van EPPlus-bibliotheek inschakelen in het ER-raamwerk** hebt ingeschakeld om met Excel-documenten in ER te werken. In dat geval wordt een afbeelding ingevoerd in een tijdelijke aanduiding met een vergrendelde hoogte-breedteverhouding. Wanneer de afmetingen van een tijdelijke aanduiding in een sjabloon overeenkomen met de verhouding van een afbeelding die wordt ingevoerd, kan het formaat van een echte afbeelding in een gegenereerd document worden gewijzigd om de vereiste hoogte-breedteverhouding te behouden. Gebruik een tijdelijke aanduiding met een verwachte hoogte-breedteverhouding om te voorkomen dat de foto wordt vergroot of verkleind.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [Bestemmingen van Elektronische rapportage](electronic-reporting-destinations.md)
- [Formuletaal in Elektronische rapportage](er-formula-language.md)
- [Functie NUMBERFORMAT](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]