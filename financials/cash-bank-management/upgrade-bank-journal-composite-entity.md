---
title: De samengestelde entiteit Bankjournaal bijwerken
description: Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 14d58604f5c0aaa4725345f58982387ad0a23205
ms.lasthandoff: 03/31/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>De samengestelde entiteit Bankjournaal bijwerken

[!include[banner](../includes/banner.md)]


Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.

Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.

1.  Compileer en synchroniseer de volgende samengestelde bankjournaalentiteiten, entiteiten en faseringstabellen:
    -   Samengestelde entiteit\\BankJournalEntity
    -   Entiteit\\BankJournalHeaderEntity
    -   Entiteit\\BankJournalLineEntity
    -   Tabel\\BankJournalHeaderStaging
    -   Tabel\\BankJournalLineStaging

2.  Gegevensbeheer\\gegevensprojecten.
    -   Maak het type **Banktransactie **voor de indeling **Brongegevens** beschikbaar.
        -   Indeling van brongegevens = XML-element
        -   Entiteitsnaam = Bankjournaal
        -   Gegevensbestand uploaden = nieuwe versie van SampleBankJournalCompositeEntity.xml
        -   Klik op **Ja** om het bestaande bestand te overschrijven.
        -   Klik op **Ja** om een nieuwe toewijzing te genereren.
        -   Controleer of het banktransactietype wordt toegewezen.
            -   Klik op **Kaart weergeven** voor de entiteit Regel.
            -   Controleer of Banktransactietype is toegewezen van Bron aan Fasering.

3.  Importeer het nieuwe afschrift.





