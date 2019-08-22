---
title: Veldomschrijvingen weergeven en exporteren
description: In dit artikel wordt beschreven hoe veldbeschrijvingen worden weergegeven en hoe de pagina Veldbeschrijvingen kan worden gebruikt van om beschrijvingen te exporteren.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a94f7ab9df19200754e39ba5a46f13bfdb1a3ab
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852100"
---
# <a name="view-and-export-field-descriptions"></a>Veldomschrijvingen weergeven en exporteren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe veldbeschrijvingen worden weergegeven en hoe de pagina Veldbeschrijvingen kan worden gebruikt van om beschrijvingen te exporteren.

Microsoft Dynamics 365 for Finance and Operations bevat beschrijvingen voor enkele van de complexere velden. Deze beschrijvingen worden weergegeven wanneer u de muisaanwijzer op een veld plaatst. U kunt ook beschrijvingen weergeven en exporteren op de pagina **Veldbeschrijvingen**.

Niet alle pagina's hebben veldomschrijvingen. We willen alleen beschrijvingen geven voor de complexere velden en niet voor de velden waarvoor het gebruik duidelijk is. Daarom hebben sommige pagina's geen veldbeschrijvingen, sommige pagina's een paar beschrijvingen en sommige van de meer complexe pagina's, zoals veel van de pagina's met parameters, veel beschrijvingen.

Als u toegang hebt tot de Finance and Operations-ontwikkelomgeving, kunt u nieuwe veldbeschrijvingen toevoegen en bestaande beschrijvingen aanpassen. U kunt bijvoorbeeld bedrijfsspecifieke informatie toevoegen aan een veldbeschrijving. Zie [Help voor velden aanpassen](../../dev-itpro/user-interface/customize-field-help.md) voor meer informatie.

## <a name="see-field-descriptions-in-the-user-interface"></a>Zie veldbeschrijvingen in de gebruikersinterface.

U kunt veldomschrijvingen weergeven door de cursor boven een veld te houden. Als er geen beschrijving beschikbaar is, ziet u de veldnaam wanneer u de muisaanwijzer op het veld plaatst.

> [!NOTE]
> In Dynamics AX 7.0 (februari 2016) kunnen veldbeschrijvingen alleen worden bekeken op de pagina **Veldbeschrijvingen**.

In de volgende afbeelding ziet u de beschrijving die wordt weergegeven wanneer u de muisaanwijzer op het veld **Artikelen vergrendelen tijdens telling** plaatst.

[![Voorbeeld van een veldbeschrijving](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>De pagina Veldbeschrijvingen gebruiken om Help voor velden weer te geven en te exporteren

Op de pagina **Veldbeschrijvingen** kunt u veldbeschrijvingen weergeven en exporteren. U kunt de omschrijvingen zien die tegelijk voor een pagina beschikbaar zijn.

### <a name="view-the-descriptions-for-a-page"></a>De omschrijvingen voor een pagina weergeven

Volg deze stap om de beschrijvingen voor een pagina weer te geven.

- Typ de naam van de pagina in het veld **Selecteer een pagina**. Of klik op de pijl om een lijst van alle pagina's te openen en blader of filter de lijst.

U kunt de naam van de pagina gebruiken die in de gebruikersinterface (UI) wordt weergegeven (bijvoorbeeld **Klanten**) of de codenaam (AOT-naam) die u kunt zien door met de rechtermuisknop op een pagina te klikken (bijvoorbeeld **CustTable**).

Zie de sectie 'Zoeken naar een pagina' verderop in dit artikel voor meer informatie over de verschillende manieren om de lijst met pagina's te filteren.

Als u de optie **Velden zonder beschrijving opnemen** instelt op **Ja**, worden alle velden op de pagina weergegeven, ongeacht of ze al dan niet een veldbeschrijving hebben.

### <a name="export-the-descriptions-for-a-page"></a>De omschrijvingen voor een pagina exporteren

Volg deze stappen om de beschrijvingen voor een pagina te exporteren.

1. Selecteer een pagina in het veld **Selecteer een pagina**.
2. Klik op de knop **Openen in Microsoft Office** in de rechterbovenhoek en klik vervolgens op **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Zoeken naar een pagina

Er zijn verschillende manieren om een pagina te zoeken in het veld **Selecteer een pagina**. In veel gevallen moet u op de pijl in het veld **Selecteer een pagina** klikken om de vervolgkeuzelijst te openen en vervolgens uit een gefilterde lijst met pagina's een keuze maken.

- Typ een deel van de naam en open vervolgens een vervolgkeuzelijst om te selecteren uit een gefilterde lijst met pagina's.
- Open de vervolgkeuzelijst en klik vervolgens op de kop **Paginanaam** boven aan de lijst of op de kop **AOT-naam van pagina**. Er wordt een dialoogvenster weergegeven waarin u geavanceerde filteropties kunt gebruiken, zoals **Paginanaam begint met**.
- Typ de volledige naam van de pagina. Als u deze optie gebruikt, kunt u het beste de vervolgkeuzelijst openen en bekijken wat er nog meer in de lijst staat, zelfs of veldbeschrijvingen worden weergegeven.

    - Als er een enkele exacte overeenkomst met de naam is, worden de veldomschrijvingen voor die pagina weergegeven.
    - Als er meer dan één exacte overeenkomst is, worden geen beschrijvingen weergegeven. U moet de vervolgkeuzelijst openen en de gewenste pagina selecteren.
    - Als de naam die u hebt getypt deel uitmaakt van de naam van een andere pagina, ziet u de beschrijvingen voor uw pagina. Als u echter de vervolgkeuzelijst opent, ziet u extra pagina's die deze naam bevatten.

Zo worden er geen beschrijvingen weergegeven wanneer u **Telling** typt in het veld **Een pagina selecteren**. U opent de vervolgkeuzelijst en ziet dat er twee pagina's zijn met de naam **Counting**, plus verschillende pagina's die het woord "Telling" bevatten in de naam. Als u de pagina met de AOT-naam **InventJournalCountt** selecteert, worden de veldbeschrijvingen voor die pagina weergegeven. Als u echter de vervolgkeuzelijst opnieuw opent, ziet u dat de lijst nu alle pagina's bevat met "InventJournalCount" als deel van de AOT-naam.

## <a name="troubleshooting"></a>Problemen oplossen

Deze sectie bevat informatie om u te helpen problemen op te lossen die u kunt tegenkomen als u veldbeschrijvingen gebruikt.

### <a name="i-cant-find-a-field-description"></a>Ik kan geen veldomschrijving vinden

We zijn bezig met het toevoegen van omschrijvingen voor de complexere velden. Als u hulp nodig hebt voor een bepaald veld, laat dit ons dan weten door een opmerking voor dit onderwerp toe te voegen.

### <a name="the-field-description-isnt-helpful"></a>De veldomschrijving is niet nuttig

Laat ons dit weten door een opmerking voor dit onderwerp toe te voegen. Beschrijf, indien mogelijk, de aanvullende informatie die u nodig hebt.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Ik kan een veld op de pagina in Veldbeschrijvingen niet vinden.

Als u alle velden op een pagina wilt weergeven, stelt u de optie **Velden zonder beschrijving opnemen** in op **Ja.** Klik op het veld **Selecteer een pagina** om te controleren of u de juiste pagina hebt geselecteerd. Als de naam die u hebt getypt deel uitmaakt van een andere veldnaam, hebt u mogelijk de pagina met de langere naam geselecteerd.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Ik kan een pagina op de pagina Veldbeschrijvingen niet vinden.

Zie de sectie 'Zoeken naar pagina's' eerder in dit artikel voor meer informatie over de verschillende manieren om pagina's te zoeken. Als u de exacte naam van de pagina hebt ingevoerd, worden de veldbeschrijvingen mogelijk niet weergegeven als er meer dan één pagina met dezelfde naam is. Klik op de pijl in het veld **Selecteer een pagina** als u een gefilterde lijst met de beschikbare pagina's wilt openen.

## <a name="additional-resources"></a>Aanvullende resources

[Help voor velden aanpassen](../../dev-itpro/user-interface/customize-field-help.md)
