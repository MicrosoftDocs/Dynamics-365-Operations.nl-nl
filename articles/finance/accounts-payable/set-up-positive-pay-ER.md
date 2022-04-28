---
title: Positieve betalingsbestanden instellen en genereren met behulp van Elektronische rapportage
description: In dit onderwerp wordt uitgelegd hoe u positieve betalingsbestanden instelt met Elektronische rapportage.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544470"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Positieve betalingsbestanden instellen met behulp van Elektronische rapportage

U kunt positief betalen gebruiken om een electronische lijst met cheques te genereren die aan de bank wordt gegeven. Wanneer vervolgens een cheque aan de bank wordt gepresenteerd, vergelijkt de bank deze met de lijst met cheques. Als de cheque overeenkomt met wat de bank op de lijst heeft, keert de bank de cheque uit. Als de cheque niet overeenkomt met een cheque in de lijst, gaat de bank de cheque controleren.

## <a name="set-up-the-electronic-reporting-configuration"></a>De configuratie van Elektronische rapportage instellen

1. Ga naar **Werkgebieden \> Elektronische rapportage**.
2. Ga naar de tegel voor de configuratieprovider **Microsoft** en selecteer **Opslagplaatsen**.
3. Selecteer **Algemeen** en selecteer vervolgens **Openen**.
4. Als een verbinding met de opslagplaats tot stand moet worden gebracht, selecteert u de blauwe koppeling in het dialoogvenster.
5. Zoek en selecteer **Model positieve betaling \> Indeling positieve betaling** in de configuratielijst.
6. Selecteer op het sneltabblad **Versies** de nieuwste versie en selecteer vervolgens **Importeren**.

## <a name="set-up-a-positive-pay-format"></a>Indeling positieve betaling instellen

1. Ga naar **Contanten en bankbeheer \> Instellen \> Indelingen positieve betaling**.
2. Selecteer **Nieuw**.
3. Stel de velden **Betalingsindeling** en **Beschrijving** in.
4. Schakel het selectievakje **Algemene elektronische exportindeling** in.
5. Stel het veld **Indelingsconfiguratie exporteren** in op **Indeling positieve betaling**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Een positieve betalingsindeling toewijzen aan een bankrekening

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Open de bankrekening.
3. Stel op het sneltabblad **Algemeen** het veld **Indeling positieve betaling** in op de indeling die eerder is gemaakt.
4. Stel het veld **Begindatum positieve betaling** in op de huidige datum.

## <a name="generate-a-positive-pay-file"></a>Creëer een positief betalingsbestand

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Open een bankrekening waarvoor positieve betaling is ingesteld.
3. Selecteer **Betalingen beheren \> Positieve betaling \> Positief betalingsbestand**.
4. Stel het veld **Afsluitdatum** in. Cheques die voor deze datum zijn gegenereerd, worden opgenomen.

Het resulterende XML-bestand wordt gedownload.
