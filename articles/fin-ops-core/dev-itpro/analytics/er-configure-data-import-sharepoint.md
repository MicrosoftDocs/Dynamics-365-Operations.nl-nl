---
title: Gegevensimport uit SharePoint configureren
description: In dit onderwerp wordt uitgelegd hoe u gegevens importeert uit Microsoft SharePoint.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6cd717c0c599d68574a5a064761c8d6777418515
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675340"
---
# <a name="configure-data-import-from-sharepoint"></a>Gegevensimport uit SharePoint configureren

[!include[banner](../includes/banner.md)]

Om gegevens te importeren uit een binnenkomend bestand met behulp van het raamwerk voor elektronische aangifte (ER), moet u een ER-indeling configureren die de import ondersteunt en vervolgens een modeltoewijzing van het type **Tot bestemming** uitvoeren die deze indeling als gegevensbron gebruikt. Om gegevens te importeren moet u navigeren naar het bestand dat u wilt importeren. Het inkomende bestand kan handmatig worden geselecteerd door de gebruiker. Met de nieuwe ER-mogelijkheid ter ondersteuning van het importeren van gegevens uit Microsoft SharePoint, kan dit proces worden geconfigureerd als zonder toezicht. U kunt ER-configuraties gebruiken om gegevens te importeren uit bestanden die zijn opgeslagen in Microsoft SharePoint-mappen. In dit onderwerp wordt uitgelegd hoe u de import van SharePoint kunt voltooien. De voorbeelden gebruiken leverancierstransacties als zakelijke gegevens.

## <a name="prerequisites"></a>Vereisten
Om de voorbeelden in dit onderwerp te kunnen voltooien, moet u toegang tot het volgende hebben:

- Maak gebruik van een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Start het exemplaar van de Microsoft SharePoint-server die voor gebruik met de toepassing is geconfigureerd.
- ER-indeling en modelconfiguraties voor 1099-betalingen.

### <a name="create-required-er-configurations"></a>Vereiste ER-configuraties maken
Speel de taakbegeleidingen **ER-gegevens importeren uit een Microsoft Excel-bestand** af, die deel uitmaken van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**. Deze taakbegeleidingen begeleiden u bij het ontwerpen en gebruiken van ER-configuraties om interactief leverancierstransacties te importeren uit Microsoft Excel-bestanden. Zie voor meer informatie [Inkomende documenten in Excel-indeling parseren](parse-incoming-documents-excel.md). Nadat u de taakbegeleidingen hebt voltooid, hebt u de volgende instelling.

#### <a name="er-configurations"></a>ER-configuraties

- ER-modelconfiguratie, **1099 Payments model**
- ER-indelingsconfiguratie, **Indeling voor het importeren van transacties van leveranciers vanuit Excel**

![ER-configuraties voor het importeren van gegevens uit SharePoint.](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Voorbeeld van het inkomende bestand voor het importeren van gegevens

- Excel-bestand **1099import-data.xlsx**, met leverancierstransacties die moeten worden geïmporteerd.

![Voorbeeld Excel-bestand voor importeren vanuit SharePoint.](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> De indeling voor het importeren van leverancierstransacties is geselecteerd als de standaardmodeltoewijzing. Dus als u een modeltoewijzing uitvoert van het **1099 Payments model** en die modeltoewijzing van het type **Tot bestemming** is, voert de modeltoewijzing deze indeling uit om gegevens uit externe bestanden te importeren. Vervolgens worden deze gegevens gebruikt om toepassingstabellen bij te werken.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>Toegang tot SharePoint voor opslag van bestanden configureren
Als u elektronische rapportbestanden op een SharePoint-locatie wilt opslaan, moet u de toegang tot het SharePoint Server-exemplaar configureren dat wordt gebruikt door het huidige bedrijf. In dit voorbeeld is het bedrijf USMF. Zie voor instructies [SharePoint-oplag configureren](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Voer de stappen in [SharePoint-opslag configureren](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage) uit.
2. Open de geconfigureerde SharePoint-site.
3. Maak de volgende mappen waarin inkomende bestanden voor elektronische aangifte kunnen worden opgeslagen:

     - Bron voor importeren van bestanden (hoofd) (voorbeeld weergegeven in onderstaande schermafbeelding)
     - Bron voor importeren van bestanden (alternatief)

    ![Bron voor importeren van bestanden (hoofd).](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Optioneel) Maak de volgende mappen waarin de bestanden na het importeren kunnen worden opgeslagen. 

    - Archiefmap voor bestanden - Deze map zou worden gebruikt voor geïmporteerde bestanden.
    - Map voor bestanden met waarschuwing - Deze map zou worden gebruikt voor bestanden die zijn geïmporteerd met een waarschuwing.
    - Map voor bestanden met een fout - Deze map zou worden gebruikt voor bestanden die niet kunnen worden geïmporteerd.

4. Ga naar **Organisatiebeheer > Documentbeheer > Documenttypen**.
5. Maak de volgende documenttypen die worden gebruikt om toegang te krijgen tot de SharePoint-mappen die u hebt gemaakt. Zie [Documenttypen configureren](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) voor instructies.

|Documenttype       | Groep              | Locatie      | SharePoint-map      |
|--------------------|--------------------|---------------|------------------------|
|SP hoofd             |Bestand                |SharePoint     |Bron voor importeren van bestanden (hoofd)|
|SP alternatief             |Bestand                |SharePoint     |Bron voor importeren van bestanden (alternatief)|
|SP-archief             |Bestand                |SharePoint     |Archiefmap voor bestanden|
|SP-waarschuwing             |Bestand                |SharePoint     |Map voor bestanden met waarschuwing|
|SP-fout             |Bestand                |SharePoint     |Map voor bestanden met een fout|

![SharePoint-instelling - nieuw documenttype.](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER-bronnen voor de ER-indeling configureren
1. Klik op **Organisatiebeheer** \> **Elektronische rapportage** \> **Bron van elektronische rapportage**.
2. Configureer op de pagina **Bron van elektronische rapportage** de bronbestanden voor gegevensimport door de geconfigureerde ER-indeling te gebruiken.
3. Geef een bestandsnaammasker op, zodat alleen bestanden met de extensie .xlsx worden geïmporteerd. Het bestandsnaammasker is optioneel en wordt alleen gebruikt als het is gedefinieerd. U kunt slechts één masker voor elke ER-indeling definiëren.
4. Wijzig **Bestanden sorteren vóór het importeren** in **Niet sorteren** wanneer verschillende bestanden moeten worden geïmporteerd en als de volgorde van importeren niet belangrijk is
5. Selecteer alle SharePoint-mappen die u eerder hebt gemaakt.

    [![Broninstelling voor ER-bestanden.](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - De ER-*bron* wordt voor elk toepassingsbedrijf afzonderlijk gedefinieerd. ER-*configuraties* worden echter gedeeld door bedrijven.
> - Wanneer u een ER-broninstelling voor een ER-indeling verwijdert, worden alle verbonden bestandsstatussen (zie hieronder) ook verwijderd, na bevestiging.

## <a name="review-the-files-states-for-the-er-format"></a>Controleer de bestandsstatussen voor de ER-indeling
1. Selecteer op de pagina **Bron van elektronische rapportage** **Bestandsstatus voor de bronnen** om de inhoud te controleren van de geconfigureerde bestandsbronnen voor de huidige ER-indeling.
2. Controleer de lijst met bestanden in het gedeelte **Bestanden**. Deze lijst bevat het volgende:

    - Bronbestanden die van toepassing zijn, op basis van het bestandsnaammasker (als er een is gedefinieerd), en die gereed zijn voor het importeren van gegevens. Voor deze bestanden is het gedeelte **Logboeken van bronnen voor importindeling** leeg.
    - Eerder geïmporteerde bestanden. Voor elk van deze bestanden in het gedeelte **Logboeken van bronnen voor importindeling** kunt u de historie van de import van dit bestand controleren.

U kunt ook de pagina **Bestandsstatus voor de bronnen** openen door **Organisatiebeheer** \> **Elektronische rapportage** \> **Bestandsstatus voor de bronnen** te selecteren. In dit geval biedt de pagina informatie over bestandsbronnen voor alle ER-indelingen waarvoor bestandsbronnen zijn geconfigureerd in het bedrijf waar u momenteel bij bent aangemeld.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Gegevens importeren uit Excel-bestanden die zich in een SharePoint-map bevinden
1. Upload in SharePoint het Microsoft Excel-bestand **1099import-data.xlsx** dat leverancierstransacties bevat, naar de SharePoint-map **Bron voor importeren van bestanden (hoofd)** die u eerder hebt gemaakt.

    [![SharePoint-inhoud: Microsoft Excel -bestand voor het importeren.](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Selecteer op de pagina **Bestandsstatus voor de bronnen** de optie **Vernieuwen** om de pagina te vernieuwen. Het Excel-bestand dat is geüpload naar SharePoint werd op deze pagina weergegeven met de status **Gereed**. De volgende statussen worden momenteel ondersteund:

    - **Gereed**: automatisch toegewezen voor elk nieuw bestand in een SharePoint-map. Deze status betekent dat het bestand gereed voor import is.
    - **Importeren**: automatisch toegewezen door een ER-rapport wanneer het bestand wordt vergrendeld door het importproces om te voorkomen dat het door andere processen wordt gebruikt (als er veel tegelijkertijd worden uitgevoerd).
    - **Geïmporteerd**: automatisch toegewezen door een ER-rapport wanneer het bestand importeren met succes is voltooid. Deze status betekent dat het geïmporteerde bestand is verwijderd uit de geconfigureerde bestandsbron (SharePoint-map).
    - **Mislukt**: automatisch toegewezen door een ER-rapport wanneer het bestand importeren met fouten of uitzonderingen is voltooid.
    - **In wachtstand**: handmatig toegewezen door de gebruiker op deze pagina. Deze status betekent dat het bestand niet op dit moment wordt geïmporteerd. Deze status kan worden gebruikt voor het uitstellen van het importeren van sommige bestanden.

    [![Vernieuwd ER-bestand vermeldt pagina voor de geselecteerde bronnen.](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Gegevens importeren vanuit SharePoint-bestanden
1. Open de ER-configuratiestructuur, selecteer het **1099 Payment model** en vouw de lijst met ER-modelcomponenten uit.
2. Selecteer de naam van de modeltoewijzing om de lijst van modeltoewijzingen van de geselecteerde ER-modelconfiguratie te openen.

    [![Configuratiepagina.](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Selecteer **Uitvoeren** om de geselecteerde modeltoewijzing uit te voeren. Omdat u bestandsbronnen voor de ER-indeling hebt geconfigureerd, kunt u de instelling van het **Bronbestand** indien nodig wijzigen. Als u de instelling van deze optie houdt, worden de .xslx-bestanden geïmporteerd van de geconfigureerde bronnen (de mappen van SharePoint in dit voorbeeld).

    In dit voorbeeld importeert u slechts één bestand. Als er echter meerdere bestanden zijn, worden ze voor importeren geselecteerd in de volgorde waarin ze zijn toegevoegd aan de SharePoint-map. Elke uitvoering van een ER-indeling importeert één geselecteerd bestand.

    [![Importeren vanuit SharePoint en ER-modeltoewijzing uitvoeren.](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. De modeltoewijzing kan [onbeheerd](#limitations) worden uitgevoerd in de batchmodus. In dit geval wordt elke keer dat een batch deze ER-indeling uitvoert, één bestand geïmporteerd van de geconfigureerde bestandsbronnen.

    Wanneer een bestand is geïmporteerd uit de SharePoint-map, wordt het verwijderd uit die map en verplaatst naar de map voor geïmporteerde bestanden of de map voor geïmporteerde bestanden met waarschuwingen. In het andere geval wordt het bestand verplaatst naar de map voor niet-geïmporteerde bestanden of blijft het in deze map als de map voor niet-geïmporteerde bestanden niet is ingesteld. 

5. Voer de boekstuk-id, zoals **V-00001**, in en selecteer vervolgens **OK**.

    [![ER-modeltoewijzing uitvoeren.](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Selecteer op de pagina **Bestandsstatus voor de bronnen** de optie **Vernieuwen** om de pagina te vernieuwen.

    [![Statussen van ER-bestand voor bronnenpagina.](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Controleer de lijst met bestanden in het gedeelte **Bestanden**. De sectie **Logboeken van bronnen voor importindeling** bieden de historie van de Excel-bestandsimport. Omdat dit bestand met succes geïmporteerd is, wordt het gemarkeerd als **Verwijderd** in de SharePoint-map.
8. Controleer de SharePoint-map **Bron voor importeren van bestanden (hoofd)**. De Excel-bestanden die met succes zijn geïmporteerd, zijn uit deze map verwijderd.
9. Selecteer **Leveranciers** \> **Periodieke taken** \> **1099-belasting** \> **Vereffening van leverancier voor 1099-aangiften**.
10. Geef in de velden **Datum vanaf** en **Datum tot** de gewenste waarden op. Selecteer vervolgens **Handmatige 1099-transacties**.

    De leverancierstransacties die zijn geïmporteerd vanuit de Excel-bestanden in SharePoint voor boekstuk **V-00001**, worden op de pagina weergegeven.

    [![pagina met 1099-leverancierstransacties.](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Een Excel-bestand voor import voorbereiden
1. Open het Excel-bestand dat u eerder hebt gebruikt. Voeg in rij 3, kolom 1 een leverancierscode toe die niet in de toepassing bestaat. Voeg extra onware leveranciersgegevens toe aan de rij.

    [![Voorbeeldbestand in Microsoft Excel voor het importeren uit SharePoint.](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Upload het bijgewerkte Excel-bestand met leverancierstransacties naar de SharePoint-map **Bron voor importeren van bestanden (hoofd)**.
3. Open de ER-configuratiestructuur, selecteer het **1099 Payment model** en vouw de lijst met ER-modelcomponenten uit.
4. Selecteer de naam van de modeltoewijzing om de modeltoewijzing bij te werken, zodat de onjuiste leverancierscode wordt gezien als een fout tijdens het importeren van gegevens.
5. Selecteer **Ontwerper**.
6. Op het tabblad **Validaties** moet u de actie na validatie wijzigen voor de validatieregel die is geconfigureerd om te bepalen of de leveranciersrekening die wordt geïmporteerd, in de toepassing bestaat. Wijzig de waarde van het veld **Actie na validatie** in **Uitvoering stoppen**, sla uw wijzigingen op en sluit de pagina.

    [![pagina ER-modeltoewijzing ontwerpen.](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Sla uw wijzigingen op en sluit de ontwerper van ER-modeltoewijzingen.
8. Selecteer **Uitvoeren** om de gewijzigde ER-modeltoewijzing uit te voeren.
9. Voer de boekstuk-id, zoals **V-00002**, in en selecteer vervolgens **OK**.

    Het infologboek bevat een melding dat een bestand in de SharePoint-map een onjuiste leveranciersrekening bevat en niet kan worden geïmporteerd.

    [![Voltooide uitvoering van ER-modeltoewijzing.](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Selecteer op de pagina **Bestandsstatus voor de bronnen** de optie **Vernieuwen** en bekijk de lijst met bestanden in het gedeelte **Bestanden**.

    [![ER-bestand vermeldt pagina voor de geselecteerde bronnen.](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   De sectie **Logboeken van bronnen voor importindeling** geeft aan dat het importproces is mislukt en dat het bestand nog in de SharePoint-map voor foutbestanden staat (het selectievakje **Is verwijderd** is niet ingeschakeld). Als u dit bestand in SharePoint corrigeert door de juiste leverancierscode toe te voegen en het vervolgens verplaatst naar de SharePoint-map Bron voor importeren van bestanden (hoofd), kunt u het bestand opnieuw importeren.

11. Selecteer **Crediteuren** \> **Periodieke taken** \> **1099-belasting** \> **Vereffening van leverancier voor 1099-aangiften**, voer de juiste waarden in de velden **Datum vanaf** en **Datum tot** in en selecteer vervolgens **Handmatige 1099-transacties**.

    Alleen transacties voor boekstuk V-00001 zijn beschikbaar. Er zijn geen transacties voor boekstuk V-00002 beschikbaar, hoewel de fout voor de laatste geïmporteerde transactie in het Excel-bestand is gevonden.

## <a name=""></a><a name="limitations">Beperkingen</a>

Het ER-raamwerk biedt geen mogelijkheid om een nieuwe batchtaak te starten waarmee een modeltoewijzing wordt uitgevoerd in de onbeheerde modus voor gegevensimport. Hiervoor moet u nieuwe logica ontwikkelen, zodat de geconfigureerde modeltoewijzing kan worden aangeroepen vanuit de gebruikersinterface van de toepassing om gegevens uit inkomende bestanden te importeren. Daarom zijn technische aanpassingen vereist. 

Voor meer informatie over de relevante ER-API raadpleegt u de sectie [Code voor het uitvoeren van een indelingstoewijzing voor gegevensimport](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) in het onderwerp [Wijzigingen in API voor ER-raamwerk in Application update 7.3](er-apis-app73.md).

Bekijk de code in de klasse `BankImport_RU` van het model `Application Suite` om te zien hoe uw aangepaste logica kan worden geïmplementeerd. Deze klasse breidt de klasse `RunBaseBatch` uit. Bekijk in het bijzonder de methode `runER()` waarin het object `ERIModelMappingDestinationRun` wordt gemaakt als de uitvoerder van een ER-modeltoewijzing.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Wijzigingen in API voor ER-raamwerk in Application update 7.3](er-apis-app73.md)

[Wijzigingen in API voor ER-raamwerk in Application update 10.0.23](er-apis-app10-0-23.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
