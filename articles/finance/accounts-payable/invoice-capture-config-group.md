---
title: Configuratiegroepen voor de oplossing Invoice Capture
description: Dit artikel biedt algemene informatie over configuratiegroepen in de oplossing Invoice Capture.
author: sunfzam
ms.date: 09/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691165"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Configuratiegroepen voor de oplossing Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Gebruikers kunnen met behulp van configuratiegroepen de lijst met factuurvelden en de handmatige controle-instelling voor rechtspersonen beheren. Gebruikers kunnen factuurconfiguraties voor verschillende rechtspersonen in groepen instellen. Alle rechtspersonen in dezelfde configuratiegroep gebruiken dezelfde factuurvelden en handmatige controle-instelling.

## <a name="manage-configuration-groups"></a>Configuratiegroepen beheren

Als u configuratiegroepen wilt beheren met de app, gaat u naar **Instellen** en selecteert u vervolgens **Systeeminstellingen \> Onderdeel voor configuratiegroepen definiëren**.

Op de pagina **Configuratiegroepen definiëren** wordt op het hoofdtabblad de lijst weergegeven met configuratiegroepen die zijn gedefinieerd. Daarnaast wordt een standaardconfiguratiegroep weergegeven. Voor elke configuratiegroep zijn de volgende acties beschikbaar:

- **Een configuratiegroep kopiëren**: u kunt een nieuwe configuratiegroep maken door een bestaande groep te dupliceren. De nieuwe groep heeft dezelfde waarden als de oorspronkelijke groep voor alle velden, behalve **Groepsnaam** en **Groepsomschrijving**. Als de configuratiegroep is gedupliceerd, selecteert u **OK**.
- **Configuratiegroepen verwijderen**: als u een configuratiegroep wilt verwijderen, selecteert u deze en selecteert u vervolgens **Verwijderen**.

    > [!NOTE]
    > De standaardconfiguratiegroep kan niet worden verwijderd.

- **De id van een configuratiegroep bewerken**: als u de id van een configuratiegroep wilt bewerken, selecteert u het veld **Groeps-id** en werkt u de waarde bij. De groeps-id mag geen spaties of speciale tekens bevatten en mag niet langer zijn dan 20 tekens.

    > [!NOTE]
    > De waarde van het veld **Groeps-id** kan maar één keer worden bijgewerkt.

- **De beschrijving van een configuratiegroep bewerken**: als u de beschrijving van een configuratiegroep wilt bewerken, selecteert u het veld **Beschrijving** en werkt u de waarde bij.
- **De instelling voor handmatige controle wijzigen**: gebruikers kunnen bepalen of een factuur handmatig moet worden gecontroleerd. Als u de instelling voor handmatige controle wilt wijzigen, selecteert u de optie **Moet handmatig worden gecontroleerd**. De volgende opties zijn beschikbaar:

    - **Altijd handmatige controle**: selecteer deze optie als facturen in de configuratiegroep altijd handmatig moeten worden beoordeeld.
    - **Voor fouten en waarschuwingen**: selecteer deze optie als facturen met fout- of waarschuwingsberichten handmatig moeten worden beoordeeld.
    - **Voor fouten**: selecteer deze optie als facturen met foutberichten handmatig moeten worden beoordeeld.

- **De instelling voor betrouwbaarheidsscore wijzigen**: de betrouwbaarheidsscore bestaat uit metagegevens die door de oplossing Invoice Capture worden verstrekt om over de nauwkeurigheid van herkende factuurgegevens te rapporteren. Hoe hoger de score, hoe nauwkeuriger de herkende gegevens kunnen zijn. Met de configuratie kunnen gebruikers bepalen wanneer handmatige controle vereist is, op basis van de betrouwbaarheidsscore. Gebruikers kunnen de drempelwaarde voor de betrouwbaarheidsscore voor facturen wijzigen. Als u de instelling voor de betrouwbaarheidsscore wilt bijwerken, selecteert u het veld **Betrouwbaarheidsscore** en werkt u de waarde bij.

    Er zijn twee typen waarschuwingen voor betrouwbaarheidsscores:

    - **Waarschuwing**: factuurvelden met betrouwbaarheidsscores boven de waarschuwingsdrempel worden als correct beschouwd. De waarschuwingsdrempel moet hoger zijn dan de foutdrempel en lager zijn dan 100.
    - **Fout**: factuurvelden met betrouwbaarheidsscores onder de foutdrempel worden als mislukt beschouwd. De gebruiker krijgt foutberichten te zien. De foutdrempel moet hoger zijn dan 0 (nul) en lager dan de waarschuwingsdrempel. Er worden waarschuwingsberichten weergegeven voor factuurvelden met betrouwbaarheidsscores tussen de waarschuwingsdrempel en de foutdrempel.

- **Factuurvelden beheren**: gebruikers kunnen de lijst met factuurvelden beheren die wordt weergegeven in de viewer voor het naast elkaar weergeven van documenten. Selecteer op het tabblad **Factuurveldbeheer** het tandwielsymbool, selecteer de factuurvelden die u wilt toevoegen en selecteer vervolgens **Opslaan**. De geselecteerde velden worden toegevoegd aan de lijst. Als u een factuurveld uit de lijst wilt verwijderen, selecteert u **Verwijderen** in het veld.

### <a name="manage-file-filters-optional"></a>Bestandsfilters beheren (optioneel)

Met Bestandsfilters beheren kunnen gebruikers extra filters definiëren voor binnenkomende factuurbestanden. Bestanden die niet aan de filtercriteria voldoen, worden ontvangen en weergegeven in de lijst **Ontvangen bestanden**, maar ze bevatten bestandsvalidatiefouten. Dit gedrag verschilt van het gedrag van filters die in het kanaal zijn gedefinieerd. Voor deze filters worden bestanden die niet aan de criteria voldoen, helemaal niet ontvangen. Gebruikers kunnen de inkomende bestanden controleren en bepalen of elk bestand een niet-geldige factuur is en ze kunnen het bestand verouderd maken of handmatig opnemen voor herkenning en opname in vastgelegde facturen.

Wanneer de oplossing Invoice Capture wordt geïnstalleerd, wordt een standaardbestandsfilter gedefinieerd. Dit bestandsfilter is globaal. Als u andere filterinstellingen wilt, kunt u het standaardfilter bijwerken. Als een veld verplicht is, selecteert u **Verplicht**. 

### <a name="accepted-file-size"></a>Geaccepteerde bestandsgrootte

U kunt de geaccepteerde bestandsgrootte kiezen.

> [!NOTE]
> Bestanden groter dan 20.480 KB worden niet ondersteund.

### <a name="supported-file-types"></a>Ondersteunde bestandstypen

Momenteel worden de volgende typen bestanden ondersteund:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF
