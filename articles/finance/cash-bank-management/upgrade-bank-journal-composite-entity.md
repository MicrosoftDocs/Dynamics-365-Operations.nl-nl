---
title: De samengestelde entiteit voor het bankjournaal bijwerken
description: In dit artikel worden de stappen beschreven om het aanvullende veld BankTransactionType aan de samengestelde BankJournalEntity toe te voegen.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1855f9680ba6bcf8eb46608882a128b4a21f0dac
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715198"
---
# <a name="update-the-bank-journal-composite-entity"></a>De samengestelde entiteit voor het bankjournaal bijwerken

[!include [banner](../includes/banner.md)]

In dit artikel worden de stappen beschreven om het aanvullende veld BankTransactionType aan de samengestelde BankJournalEntity toe te voegen.

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
