---
title: Gegevens importeren uit SharePoint configureren
description: In dit onderwerp wordt uitgelegd hoe u gegevens importeert uit Microsoft SharePoint.
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Gegevens importeren uit SharePoint configureren

[!include[banner](../includes/banner.md)]

Om gegevens te importeren uit een binnenkomend bestand met behulp van het raamwerk voor elektronische aangifte (ER), moet u een ER-indeling configureren die de import ondersteunt en vervolgens een modeltoewijzing van het type **Tot bestemming** uitvoeren die deze indeling als gegevensbron gebruikt. Om gegevens te importeren moet u navigeren naar het bestand dat u wilt importeren. Het inkomende bestand kan handmatig worden geselecteerd door de gebruiker. Met de nieuwe ER-mogelijkheid ter ondersteuning van importeren van gegevens uit Microsoft SharePoint, kan dit proces worden geconfigureerd als zonder toezicht. U kunt ER-configuraties gebruiken om gegevens te importeren uit bestanden die zijn opgeslagen in Microsoft SharePoint-mappen. In dit onderwerp wordt uitgelegd hoe u het importeren van SharePoint naar Microsoft Dynamics 365 for Finance and Operations voltooit. De voorbeelden gebruiken leverancierstransacties als zakelijke gegevens.

## <a name="prerequisites"></a>Vereisten
Om de voorbeelden in dit onderwerp te kunnen voltooien, moet u toegang tot het volgende hebben:

- Toegang verkrijgen tot Finance and Operations voor een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Toegang tot het exemplaar van de Microsoft SharePoint-server die voor gebruik met Finance and Operations is geconfigureerd
- ER-indeling en modelconfiguraties voor 1099-betalingen

### <a name="create-required-er-configurations"></a>Vereiste ER-configuraties maken
Speel de taakbegeleiders **ER-gegevens importeren uit een Microsoft Excel-bestand** af, die deel uitmaken van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**. Deze taakbegeleiders begeleiden u bij het ontwerpen en gebruiken van ER-configuraties om interactief leverancierstransacties te importeren uit externe Microsoft Excel-bestanden. Zie voor meer informatie [Inkomende documenten in Microsoft Excel parseren](parse-incoming-documents-excel.md). Ten slotte moet u het volgende doen:

- ER-configuraties:

    - ER-modelconfiguratie, **1099 Payments model**
    - ER-indelingsconfiguratie, **Indeling voor het importeren van transacties van leveranciers vanuit Excel**

[![ER-configuraties voor het importeren van gegevens uit SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Voorbeeld van het inkomende bestand voor het importeren van gegevens:

    - Excel-bestand **1099import-data.xlsx**, met leverancierstransacties die moeten worden geïmporteerd in Finance and Operations

[![Voorbeeld Microsoft Excel-bestand voor het importeren van SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> De indeling voor het importeren van leverancierstransacties is geselecteerd als de standaardmodeltoewijzing. Dus als u een modeltoewijzing uitvoert van het **1099 Payments model** en die modeltoewijzing van het type **Tot bestemming** is, voert de modeltoewijzing deze indeling uit om gegevens uit externe bestanden te importeren. Vervolgens worden deze gegevens gebruikt om toepassingstabellen bij te werken.

## <a name="configure-document-management-parameters"></a>Parameters voor documentbeheer configureren
1. Configureer op de pagina **Parameters voor documentbeheer** toegang tot het exemplaar van de SharePoint-server dat door het bedrijf wordt gebruikt waarbij u momenteel bent aangemeld. In dit voorbeeld is het bedrijf USMF.
2. Test de verbinding met het exemplaar van de SharePoint-server om er zeker van te zijn dat u toegang hebt gekregen.

[![Documentbeheerinstelling – SharePoint-server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Open de geconfigureerde SharePoint-site en maak de volgende mappen waar inkomende bestanden kunnen worden opgeslagen:

    - Bron voor importeren van bestanden (hoofd)
    - Bron voor importeren van bestanden (alternatief)

[![Documentbeheerinstelling – SharePoint-server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Documentbeheerinstelling – SharePoint-server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. Maak in Finance and Operations op de pagina **Documenttypen** de volgende documenttypen die worden gebruikt om toegang te krijgen tot de SharePoint-mappen die u zojuist hebt gemaakt:

    - SP hoofd
    - SP alternatief

5. Voer voor gemaakte documenttypen in het veld **Groep** **Bestand** in en in het veld **Locatie** **SharePoint**. Voer vervolgens het adres van de SharePoint-map in:

    - Voor het documenttype **SP hoofd**: Bron voor importeren van bestanden (hoofd)
    - Voor het documenttype **SP alternatief**: Bron voor importeren van bestanden (alternatief)

[![SharePoint-instelling - nieuw documenttype](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER-bronnen voor de ER-indeling configureren
1. Ga naar **Organisatiebeheer** > **Elektronische rapportage** > **Bron van elektronische rapportage**.
2. Configureer op de pagina **Bron van elektronische rapportage** de bronbestanden voor gegevensimport door de geconfigureerde ER-indeling te gebruiken.
3. Geef een bestandsnaammasker op, zodat alleen bestanden met de extensie .xlsx worden geïmporteerd. Het bestandsnaammasker is optioneel en wordt alleen gebruikt als het is gedefinieerd. U kunt slechts één masker voor elke ER-indeling definiëren.
4. Selecteer beide SharePoint-mappen die u eerder hebt gemaakt.

[![Broninstelling voor ER-bestanden](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>De ER-*bron* wordt voor elk toepassingsbedrijf afzonderlijk gedefinieerd. ER-*configuraties* worden echter gedeeld door bedrijven.

> [!NOTE]
> Wanneer u een ER-broninstelling voor een ER-indeling verwijdert, worden alle verbonden bestandsstatussen (zie hieronder) ook verwijderd.

## <a name="review-the-files-states-for-the-er-format"></a>Controleer de bestandsstatussen voor de ER-indeling
1. Selecteer op de pagina **Bron van elektronische rapportage** **Bestandsstatus voor de bronnen** om de inhoud te controleren van de geconfigureerde bestandsbronnen voor de huidige ER-indeling.
2. Controleer de lijst met bestanden in het gedeelte **Bestanden**. Deze lijst bevat het volgende:

    - Bronbestanden die van toepassing zijn, op basis van het bestandsnaammasker (als er een is gedefinieerd), en die gereed zijn voor het importeren van gegevens. Voor deze bestanden is het gedeelte **Logboeken van bronnen voor importindeling** leeg.
    - Eerder geïmporteerde bestanden. Voor elk van deze bestanden in het gedeelte **Logboeken van bronnen voor importindeling** kunt u de historie van de import van dit bestand controleren.

U kunt ook de pagina **Bestandsstatus voor de bronnen** openen door **Organisatiebeheer** \> **Elektronische rapportage** \> **Bestandsstatus voor de bronnen** te selecteren. In dit geval biedt de pagina informatie over bestandsbronnen voor alle ER-indelingen waarvoor bestandsbronnen zijn geconfigureerd in het bedrijf waar u momenteel bij bent aangemeld.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Gegevens importeren uit Excel-bestanden die zich in een SharePoint-map bevinden
1. Upload in SharePoint het Microsoft Excel-bestand **1099import-data.xlsx** dat leverancierstransacties bevat, naar de SharePoint-map **Bron voor importeren van bestanden (hoofd)** die u eerder hebt gemaakt.

[![SharePoint-inhoud – Microsoft Excel-bestand voor importeren](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Selecteer in Finance and Operations op de pagina **Bestandsstatus voor de bronnen** de optie **Vernieuwen** om de pagina te vernieuwen. Het Excel-bestand dat was geüpload naar SharePoint, werd op dit formulier weergegeven met de status **Gereed**. De volgende statussen worden momenteel ondersteund:

    - **Gereed**: automatisch toegewezen voor elk nieuw bestand in een SharePoint-map. Deze status betekent dat het bestand gereed voor import is.
    - **Importeren** - automatisch toegewezen door een ER-rapport wanneer het bestand wordt vergrendeld door het importproces om te voorkomen dat het door andere processen wordt gebruikt (als er veel tegelijkertijd worden uitgevoerd).
    - **Geïmporteerd** - automatisch toegewezen door een ER-rapport wanneer het bestand importeren met succes is voltooid. Deze status betekent dat het geïmporteerde bestand is verwijderd uit de geconfigureerde bestandsbron (SharePoint-map).
    - **Mislukt** - automatisch toegewezen door een ER-rapport wanneer het bestand importeren met fouten of uitzonderingen is voltooid.
    - **In wachtstand** - handmatig toegewezen door de gebruiker op dit formulier. Deze status betekent dat het bestand niet op dit moment wordt geïmporteerd. Deze status kan worden gebruikt voor het uitstellen van het importeren van sommige bestanden.

[![ER-bestand vermeldt pagina voor de geselecteerde bronnen](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Gegevens importeren uit SharePoint-bestanden
1. Open de ER-configuratiestructuur, selecteer het **1099 Payment model** en vouw de lijst met ER-modelcomponenten uit.
2. Selecteer de naam van de modeltoewijzing om de lijst van modeltoewijzingen van de geselecteerde ER-modelconfiguratie te openen.

[![ER-bestand vermeldt pagina voor de geselecteerde bronnen](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Selecteer **Uitvoeren** om de geselecteerde modeltoewijzing uit te voeren. Omdat u bestandsbronnen voor de ER-indeling hebt geconfigureerd, kunt u de instelling van het **Bronbestand** indien nodig wijzigen. Als u de instelling van deze optie houdt, worden de .xslx-bestanden geïmporteerd van de geconfigureerde bronnen (de mappen van SharePoint in dit voorbeeld).

    In dit voorbeeld importeert u slechts één bestand. Als er echter meerdere bestanden zijn, worden ze voor importeren geselecteerd in de volgorde waarin ze zijn toegevoegd aan de SharePoint-map. Elke uitvoering van een ER-indeling importeert één geselecteerd bestand.

[![ER-modeltoewijzing uitvoeren](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. De modeltoewijzing kan onbeheerd worden uitgevoerd in de batchmodus. In dit geval wordt elke keer dat een batch deze ER-indeling uitvoert, één bestand geïmporteerd van de geconfigureerde bestandsbronnen. Gebruik de volgende code om deze batchuitvoering te implementeren.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Wanneer een bestand met succes wordt geïmporteerd uit de SharePoint-map, wordt het verwijderd uit die map.

5. Voer de boekstuk-id, zoals **V-00001**, in en selecteer vervolgens **OK**.

[![ER-modeltoewijzing uitvoeren](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Selecteer op de pagina **Bestandsstatus voor de bronnen** de optie **Vernieuwen** om de pagina te vernieuwen.

[![ER-bestand vermeldt pagina voor de geselecteerde bronnen](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Controleer de lijst met bestanden in het gedeelte **Bestanden**. De sectie **Logboeken van bronnen voor importindeling** bieden de historie van de Excel-bestandsimport. Omdat dit bestand met succes geïmporteerd is, wordt het gemarkeerd als **Verwijderd** in de SharePoint-map.
8. Controleer de SharePoint-map **Bron voor importeren van bestanden (hoofd)**. De Excel-bestanden die met succes zijn geïmporteerd, zijn uit deze map verwijderd.
9. Selecteer in Finance and Operations **Crediteuren** \> **Periodieke taken** \> **1099-belasting** \> **Vereffening van leverancier voor 1099-aangiften**.
10. Geef in de velden **Datum vanaf** en **Datum tot** de gewenste waarden op. Selecteer vervolgens **Handmatige 1099-transacties**.

    De leverancierstransacties die zijn geïmporteerd vanuit de Excel-bestanden in SharePoint voor boekstuk **V-00001**, worden op de pagina weergegeven.

[![pagina met 1099-leverancierstransacties](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Een Excel-bestand voor import voorbereiden
1. Open het Excel-bestand dat u eerder hebt gebruikt. Voeg in rij 3, kolom 1 een leverancierscode toe die niet in de toepassing bestaat. Voeg extra onware leveranciersgegevens toe aan de rij.

[![Voorbeeld Microsoft Excel-bestand voor het importeren van SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Upload het bijgewerkte Excel-bestand met leverancierstransacties naar de SharePoint-map **Bron voor importeren van bestanden (hoofd)**.
3. Open in Finance and Operations de ER-configuratiestructuur, selecteer het **1099 Payment model** en vouw de lijst met ER-modelcomponenten uit.
4. Selecteer de naam van de modeltoewijzing om de modeltoewijzing bij te werken, zodat de onjuiste leverancierscode wordt gezien als een fout tijdens het importeren van gegevens.
5. Selecteer **Ontwerper**.
6. Op het tabblad **Validaties** moet u de actie na validatie wijzigen voor de validatieregel die is geconfigureerd om te bepalen of de leveranciersrekening die wordt geïmporteerd, in de toepassing bestaat. Wijzig de waarde van het veld **Actie na validatie** in **Uitvoering stoppen**, sla uw wijzigingen op en sluit de pagina.

[![pagina ER-modeltoewijzing ontwerpen](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Sla uw wijzigingen op en sluit de ontwerper van ER-modeltoewijzingen.
8. Selecteer **Uitvoeren** om de gewijzigde ER-modeltoewijzing uit te voeren.
9. Voer de boekstuk-id, zoals **V-00002**, in en selecteer vervolgens **OK**.

    Het infologboek bevat de melding dat een bestand in de SharePoint-map een onjuiste leveranciersrekening bevat en niet kan worden geïmporteerd.

[![ER-modeltoewijzing uitvoeren](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Selecteer op de pagina **Bestandsstatus voor de bronnen** de optie **Vernieuwen** en bekijk de lijst met bestanden in het gedeelte **Bestanden**.

[![ER-bestand vermeldt pagina voor de geselecteerde bronnen](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

De sectie **Logboeken van bronnen voor importindeling** geeft aan dat het importproces is mislukt en dat het bestand nog steeds in de SharePoint-map staat (het selectievakje **Is verwijderd** is niet ingeschakeld). Als u dit bestand in SharePoint corrigeert door de juiste leverancierscode toe te voegen en de status van het bestand vervolgens wijzigt van **Mislukt** in **Gereed** in de sectie **Logboeken van bronnen voor importindeling**, kunt u het bestand opnieuw importeren.

11. Controleer de SharePoint-map **Bron voor importeren van bestanden (hoofd)**. U ziet dat het Excel-bestand dat is niet geïmporteerd, zich nog steeds in deze map bevindt.
12. Selecteer in Finance and Operations **Crediteuren** \> **Periodieke taken** \> **1099-belasting** \> **Vereffening van leverancier voor 1099-aangiften**, voer de juiste waarden in de velden **Datum vanaf** en **Datum tot** in en selecteer vervolgens **Handmatige 1099-transacties**.

    Alleen transacties voor boekstuk V-00001 zijn beschikbaar. Er zijn geen transacties voor boekstuk V-00002 beschikbaar, hoewel de fout voor de laatste geïmporteerde transactie in het Excel-bestand is gevonden.

