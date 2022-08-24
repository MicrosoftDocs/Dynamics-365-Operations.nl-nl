---
title: Gegevens importeren uit handmatig geselecteerde bestanden in batchmodus
description: In dit artikel wordt uitgelegd hoe u gegevens uit handmatig geselecteerde bestanden in batchmodus importeert.
author: kfend
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
ms.openlocfilehash: 21a2ab5f0eb07dda92baf9cc04ee36caeff8b4ec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288223"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Gegevens importeren uit handmatig geselecteerde bestanden in batchmodus

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Als u het raamwerk voor [ER (Electronic Reporting)](general-electronic-reporting.md) wilt gebruiken om gegevens te importeren uit handmatig geselecteerde inkomende bestanden in batchmodus, configureert u een ER-[indeling](er-overview-components.md#format-component) die de import ondersteunt. Voer vervolgens een [modeltoewijzing](er-overview-components.md#model-mapping-component) van het type **Naar bestemming** uit waarbij deze indeling als een gegevensbron wordt gebruikt. Als u gegevens wilt importeren, bladert u naar het bestand dat u wilt importeren en selecteert u het handmatig. 

Met de nieuwe ER-mogelijkheid ter ondersteuning van het importeren van gegevens in batchmodus kan dit proces worden geconfigureerd als onbeheerd. U kunt ER-configuraties gebruiken om gegevensimport uit te voeren door een nieuwe batchtaak te plannen via de ER-gebruikersinterface (UI).

In dit artikel wordt uitgelegd hoe u gegevens uit handmatig geselecteerde bestanden in batchmodus importeert. De voorbeelden gebruiken leverancierstransacties als zakelijke gegevens. De stappen van deze voorbeelden kunnen worden uitgevoerd in het bedrijf **USMF**. U hoeft hiervoor geen code te schrijven.

## <a name="prerequisites"></a>Vereisten

Om de voorbeelden in dit artikel te kunnen voltooien, moet u over de volgende toegangsrechten beschikken:

- Een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- ER-indeling en modelconfiguraties voor 1099-betalingen

### <a name="create-the-required-er-configurations"></a>De vereiste ER-configuraties maken

Voer de volgende stappen uit om de vereiste ER-configuraties te maken en andere vereisten te regelen:

- Speel de taakbegeleidingen **ER-gegevens importeren uit een Microsoft Excel-bestand** af, die deel uitmaken van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**. Deze taakbegeleidingen helpen u bij het ontwerpen en gebruiken van ER-configuraties waarmee leverancierstransacties interactief uit Microsoft Excel-bestanden worden geïmporteerd. Zie voor meer informatie [Inkomende documenten in Excel-indeling parseren](parse-incoming-documents-excel.md).
- Voltooi de voorbeelden in [Gegevensimport configureren vanuit SharePoint](er-configure-data-import-sharepoint.md). Deze voorbeelden helpen u bij het ontwerpen en gebruiken van ER-configuraties waarmee leverancierstransacties interactief worden geïmporteerd uit Excel-bestanden die zijn opgeslagen in een SharePoint-map.

### <a name="download-the-required-er-configurations"></a>De vereiste ER-configuraties downloaden

1. Download de volgende ER-configuraties en sla ze lokaal op.

    | Omschrijving inhoud | Bestand |
    |---------------------|------|
    | ER-gegevensmodelconfiguratie **1099-betalingsmodel** | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | ER-indelingsconfiguratie **voor het importeren van transacties van leveranciers (Excel)** | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Gebruik de ER-optie [Laden uit XML-bestand](er-defer-sequence-element.md#import-the-sample-er-configurations) om de gedownloade ER-configuraties in uw exemplaar van Dynamics 365 Finance te importeren in de volgende volgorde:

    1. Configuratie van model voor ER-gegevens
    2. ER-indelingsconfiguratie

### <a name="download-the-required-excel-files"></a>De vereiste Excel-bestanden downloaden

- Download de volgende voorbeeldgegevensset en sla deze lokaal op.

    | Omschrijving inhoud | Bestand |
    |---------------------|------|
    | Het inkomende bestand **1099import-data.xlsx** dat voorbeeldgegevens voor import bevat | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>De vereisten bekijken

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Bekijk op de pagina **Configuraties** de voorbereide ER-oplossing voor het importeren van gegevens in batchmodus.
3. Bekijk de indelingsconfiguratie **voor het importeren van transacties van leveranciers (Excel)**.

    - Het indelingsonderdeel van deze configuratie is ontworpen om een inkomend Excel-bestand te parseren.
    - Het modeltoewijzingsonderdeel van deze configuratie wordt gebruikt om het basisgegevensmodel in te vullen door gegevens uit het geparseerde Excel-bestand te gebruiken.

    ![De configuratie van de ER-indeling voor het importeren van gegevens in batchmodus vanuit de ER-gebruikersinterface.](./media/er-configure-data-import-batch-configurations-1.png)

4. Bekijk de gegevensmodelconfiguratie **1099-betalingsmodel**.

    - Het modelonderdeel van deze configuratie vertegenwoordigt de structuur van het gegevensmodel dat wordt gebruikt om gegevens tussen actieve ER-onderdelen door te geven.
    - Het modeltoewijzingsonderdeel van deze configuratie wordt gebruikt om gegevens op te halen uit het uitgevoerde indelingsonderdeel en vervolgens toepassingstabellen bij te werken.

    ![Configuratie van ER-gegevensmodel voor het importeren van gegevens in batchmodus vanuit de ER-gebruikersinterface.](./media/er-configure-data-import-batch-configurations-2.png)

5. Open het bestand **1099import-data.xlsx** in Excel.

    ![Excel-voorbeeldbestand met gegevens voor import in batchmodus.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Batchgegevensimport voor ER vanuit de gebruikersinterface inschakelen

1. Ga naar **Systeembeheer** \> **Werkruimten** \> **Functiebeheer**.
2. Selecteer in het werkgebied **Functiebeheer** de functie **ER-import van handmatig geüploade documenten in batch uitvoeren** en selecteer vervolgens **Nu inschakelen**.

## <a name="import-data-from-manually-selected-excel-files"></a>Gegevens importeren vanuit handmatig geselecteerde Excel-bestanden

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** de gegevensmodelconfiguratie **1099-betalingsmodel**.
3. Selecteer op het sneltabblad **Configuratieonderdelen** de koppeling **Voor import van handmatige 1099-transacties**.
4. Op de pagina **Toewijzing model aan gegevensbron** is de modeltoewijzing **Voor import van handmatige 1099-transacties** vooraf geselecteerd. Selecteer **Uitvoeren**.
5. Selecteer op het tabblad **Parameters** de optie **Bladeren**. Zoek en selecteer het bestand **1099import-data.xlsx** en selecteer vervolgens **OK**.
6. Voer in het veld **Boekstuk-id invoeren** **V-00001** in.
7. Stel op het tabblad **Op de achtergrond uitvoeren** de optie **Batchverwerking** in op **Ja**.

    Het veld **Taakomschrijving** is ingesteld op **Uitvoeren van modeltoewijzing voor import van handmatige 1099-transacties, configuratie '1099-betalingsmodel'**. Deze waarde geeft aan dat de uitvoering van de geselecteerde modeltoewijzing wordt gepland als een nieuwe batchtaak.

    ![Details opgeven van de gegevensimport in de batchmodus in het dialoogvenster Parameters elektronisch rapport.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Selecteer **OK**. Een bericht informeert u dat een nieuwe batchtaak is gepland.

    ![Bericht over een nieuwe geplande batchtaak op de pagina Toewijzing model aan gegevensbron.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>De resultaten van het importeren van gegevens bekijken op de pagina Batchtaak

1. Ga naar **Algemeen** \> **Query's** \> **Batchtaken** \> **Mijn batchtaken**.
2. Filter op pagina **Batchtaak** de lijst met batchtaken om de geplande batch te zoeken en selecteer deze vervolgens.
3. Selecteer de koppeling **Taak-id** om taakdetails te controleren.
4. Selecteer op het sneltabblad **Batchtaken** **Logboek**.

    ![De knop Logboek op de pagina Batchtaak.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Bekijk de uitvoeringsdetails.

    ![Het uitvoeringslogboek van de geplande batchtaak op de pagina Batchtaak.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>De parameters voor gegevensimport wijzigen

Nadat de batch is gepland en deze nog niet is uitgevoerd, kunt u de parameters van de geplande gegevensimport wijzigen.

1. Ga naar **Algemeen** \> **Query's** \> **Batchtaken** \> **Mijn batchtaken**.
2. Filter op pagina **Batchtaak** de lijst met batchtaken om de geplande batch te zoeken en selecteer deze vervolgens.
3. Selecteer **Status wijzigen**.
4. Selecteer in het dialoogvenster **Nieuwe status selecteren** de optie **Inhouden** en selecteer vervolgens **OK**.
5. Selecteer de koppeling **Taak-id** om toegang te krijgen tot de taakdetails.
6. Selecteer op het sneltabblad **Batchtaken** **Parameters**.
7. Voer in het dialoogvenster **Parameters elektronisch rapport** de volgende stappen uit:

    1. Selecteer **Bladeren** om het alternatieve bestand voor gegevensimport te selecteren.
    2. Selecteer **Boekstuk-id invoeren** om het boekstuknummer voor het importeren van leverancierstransacties te wijzigen.

        ![De parameters van de gegevensimport wijzigen voor de geplande batchtaak in het dialoogvenster Parameters elektronisch rapport.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Selecteer **OK**.

8. Zorg ervoor dat de batch nog steeds is geselecteerd en selecteer **Status wijzigen** vervolgens opnieuw.
9. Selecteer in het dialoogvenster **Nieuwe status selecteren** de optie **Wachtend** en selecteer vervolgens **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>De resultaten van het importeren van gegevens bekijken op de pagina ER-bron

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Bron van elektronische rapportage**.
2. Selecteer de record **Voor het importeren van leverancierstransacties (Excel)** die tijdens het importeren van gegevens automatisch is gemaakt.

    ![Record voor de configuratie 'Voor het importeren van leverancierstransacties (Excel) op de pagina Bron van elektronische rapportage.](./media/er-configure-data-import-batch-files-source-1.png)

3. Selecteer **Bestandsstatus voor de bronnen**.
4. Bekijk de importdetails op de sneltabbladen **Bestanden** en **Logboeken van bronnen voor importindeling**.
5. Selecteer de record op het sneltabblad **Bestanden**. Het geïmporteerde bestand wordt aan deze record gekoppeld.

    ![Geïmporteerd bestand dat is gekoppeld aan de record op de pagina Bestandsstatus voor de bronnen.](./media/er-configure-data-import-batch-files-source-2.png)

6. Selecteer **Bijlagen** om het geïmporteerde bestand te controleren.

    ![Geïmporteerd bestand op de pagina Documentweergave.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Als u deze bijlagen wilt behouden, gebruikt het ER-raamwerk een documenttype dat is [ingesteld](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) voor het huidige bedrijf in het veld **Overig** van de ER-parameters.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>De resultaten van het importeren van gegevens bekijken op de pagina Vereffening van leverancier voor 1099-aangiften

1. Ga naar **Leveranciers** \> **Periodieke taken** \> **1099-belasting** \> **Vereffening van leverancier voor 1099-aangiften**.
2. Voer in het veld **Begindatum** de waarde **31/12/2017** (31 december 2017) in.
3. Selecteer **Handmatige 1099-transacties**.

    ![Geïmporteerde leverancierstransacties op de pagina 1099-belastingtransacties.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
