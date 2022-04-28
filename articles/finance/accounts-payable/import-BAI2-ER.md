---
title: Importeren van geavanceerde bankafstemming instellen via Elektronische rapportage
description: In dit onderwerp wordt uitgelegd hoe u Elektronische rapportage moet gebruiken om het proces voor het importeren van geavanceerde bankafstemming voor BAI2-afschriften in te stellen.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544478"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Importeren van geavanceerde bankafstemming instellen via Elektronische rapportage

[!include [banner](../includes/banner.md)]

Met de functie Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Microsoft Dynamics 365 Finance. In dit onderwerp wordt uitgelegd hoe u de importfunctionaliteit voor uw BAI2-bankafschriften kunt instellen.

## <a name="set-up-the-electronic-reporting-configuration"></a>De configuratie van Elektronische rapportage instellen

1. Ga naar **Werkgebieden \> Elektronische rapportage**.
2. Ga naar de tegel voor de configuratieprovider **Microsoft** en selecteer **Opslagplaatsen**.
3. Selecteer **Algemeen** en selecteer vervolgens **Openen**.
4. Als een verbinding met de opslagplaats tot stand moet worden gebracht, selecteert u de blauwe koppeling in het dialoogvenster.
5. Zoek **Bankafschriftmodel \> Bankafschriftmodel van BAI2** in de configuratielijst.
6. Selecteer de indeling **BAI2**.
7. Selecteer op het sneltabblad **Versies** de nieuwste versie en selecteer vervolgens **Importeren**.

## <a name="set-up-the-bank-statement-format"></a>De bankafschriftindeling instellen

1. Ga naar **Contanten en bankbeheer \> Instellingen \> Instelling van geavanceerde bankafstemming \> Indeling bankafschrift**.
2. Selecteer **Nieuw**.
3. Stel de velden **Afschriftindeling** en **Naam** in.
4. Schakel het selectievakje **Algemene elektronische importindeling** in.
5. Stel het veld **Indelingsconfiguratie importeren** in op **BAI2**.

## <a name="set-up-the-bank-account"></a>De bankrekening instellen

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Open de bankrekening.
3. Stel op het sneltabblad **Afstemming** de optie **Geavanceerde bankafstemming** in op **Ja**.
4. Stel het veld **Afschriftindeling** in op de indeling **BAI2**, die u eerder hebt gemaakt.

## <a name="import-the-bank-statement"></a>Het bankafschrift importeren

1. Ga naar **Contanten en bankbeheer \> Afstemming van bankafschrift \> Bankafschriften**.
2. Selecteer **Afschrift importeren** boven aan de pagina **Bankafschriften**.
3. Stel het veld **Bankrekening** in op de bankrekening in het afschrift.
4. Stel het veld **Afschriftindeling** in op de indeling **BAI2**, die u eerder hebt gemaakt.
5. Selecteer **Bladeren** en selecteer het bestand **BAI**.
6. Selecteer **Uploaden**.
7. Selecteer **OK** om het geselecteerde bestand te importeren.
