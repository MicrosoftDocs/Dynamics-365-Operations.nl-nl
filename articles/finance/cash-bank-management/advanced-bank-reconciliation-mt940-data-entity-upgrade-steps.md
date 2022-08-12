---
title: 'Geavanceerde bankafstemming MT940-import: upgrade van de samengestelde gegevensentiteit'
description: Een volgnummer moet worden toegevoegd aan de entiteit voor bankafschriftimport, zodat de MT940-indeling wordt ondersteund.
author: angelad116
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e0cf603e04be4f8f784a32b9ef98d748d4d28e5b
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151465"
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
