---
title: De samengestelde entiteit Bankjournaal bijwerken
description: Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "359354"
---
# <a name="update-the-bank-journal-composite-entity"></a>De samengestelde entiteit Bankjournaal bijwerken

[!include [banner](../includes/banner.md)]

Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.

Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.

1.  Compileer en synchroniseer de volgende samengestelde bankjournaalentiteiten, entiteiten en faseringstabellen:
    -   Samengestelde entiteit\\BankJournalEntity
    -   Entiteit\\BankJournalHeaderEntity
    -   Entiteit\\BankJournalLineEntity
    -   Tabel\\BankJournalHeaderStaging
    -   Tabel\\BankJournalLineStaging

2.  Gegevensbeheer\\gegevensprojecten.
    -   Maak het type **Banktransactie** voor de indeling **Brongegevens** beschikbaar.
        -   Indeling van brongegevens = XML-element
        -   Entiteitsnaam = Bankjournaal
        -   Gegevensbestand uploaden = nieuwe versie van SampleBankJournalCompositeEntity.xml
        -   Klik op **Ja** om het bestaande bestand te overschrijven.
        -   Klik op **Ja** om een nieuwe toewijzing te genereren.
        -   Controleer of het banktransactietype wordt toegewezen.
            -   Klik op **Kaart weergeven** voor de entiteit Regel.
            -   Controleer of Banktransactietype is toegewezen van Bron aan Fasering.

3.  Importeer het nieuwe afschrift.




