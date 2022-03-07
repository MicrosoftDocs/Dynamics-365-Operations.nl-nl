---
title: 'Geavanceerde bankafstemming MT940-import: upgrade van de samengestelde gegevensentiteit'
description: Een volgnummer moet worden toegevoegd aan de entiteit voor bankafschriftimport, zodat de MT940-indeling wordt ondersteund.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c891a5139ff7de85e6762513f57236e24f1644529d7825c9ce5e1dfda50fbad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739378"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Geavanceerde bankafstemming MT940-import: upgrade van de samengestelde gegevensentiteit

[!include [banner](../includes/banner.md)]

Een volgnummer moet worden toegevoegd aan de entiteit voor bankafschriftimport, zodat de MT940-indeling wordt ondersteund. 

Met de volgende stappen kunt u de entiteit voor import van bankafschriften toevoegen, die de MT940-indeling ondersteunt.

1.  Compileer en synchroniseer de volgende bestanden:
    -   Samengestelde entiteit\\BankStatementImportEntity
    -   Entiteit\\BankStatementBalanceEntity
    -   Entiteit\\BankStatementDocumentEntity
    -   Entiteit\\BankStatementEntity
    -   Entiteit\\BankStatementLineEntity
    -   Tabellen\\BankStatementStaging

2.  Gegevensbeheer\\gegevensprojecten.
    1.  Laad de projecten voor MT940-import
        1.  Vervang de XSLT.
            -   Klik op **Kaart weergeven**.
            -   Klik op **Kaart weergeven** op het bankafschriftdocument.
            -   Klik op **Transformaties**.
            -   Verwijder het bestand BankReconiliation-to-Composite.xslt.
            -   Voeg de nieuwe versie van BankReconiliation-to-Composite.xsl toe.

        2.  Maak **Volgnummer** op de indeling **Brongegevens** zichtbaar.
            1.  Indeling van brongegevens = XML-element.
            2.  Naam entiteit = Bankafschriften.
            3.  Gegevensbestand uploaden = nieuwe versie van SampleBankCompositeEntity.xml.
            4.  Klik op **Ja** om het bestaande bestand te overschrijven.
            5.  Klik op **Ja** om een nieuwe toewijzing te genereren.
            6.  Controleer of **SequenceNumber** is toegewezen.
                -   Klik op **Kaart weergeven** op de entiteit Afschrift.
                -   Controleer dat **SequenceNumber** is toegewezen van Bron naar Fasering.

3.  Importeer het nieuwe afschrift.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]