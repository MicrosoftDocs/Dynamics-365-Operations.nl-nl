---
title: Importeren van geavanceerde bankafstemming instellen via Elektronische rapportage
description: In dit artikel wordt uitgelegd hoe u Elektronische rapportage moet gebruiken om het proces voor het importeren van geavanceerde bankafstemming in te stellen.
author: angelad116
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
ms.openlocfilehash: bfc1c2021387ed35e6ccb513167e896eddef2eaf
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759595"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Importeren van geavanceerde bankafstemming instellen via Elektronische rapportage

[!include [banner](../includes/banner.md)]

Met de functie Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Microsoft Dynamics 365 Finance. In dit artikel wordt uitgelegd hoe u de importfunctionaliteit voor uw bankafschriften kunt instellen. De instelling voor de importeren van bankafschriften varieert, afhankelijk van de indeling van uw elektronische bankafschrift. Microsoft Dynamics 365 Finance ondersteunt drie indelingen voor bankafschriften: ISO20022, MT940 en BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>De configuratie van Elektronische rapportage instellen

1. Ga naar **Werkgebieden \> Elektronische rapportage**.
2. Ga naar de tegel voor de configuratieprovider **Microsoft** en selecteer **Opslagplaatsen**.
3. Selecteer **Algemeen** en selecteer vervolgens **Openen**.
4. Als een verbinding met de opslagplaats tot stand moet worden gebracht, selecteert u de blauwe koppeling in het dialoogvenster.
5. Zoek **Geavanceerd model voor bankafstemmingsoverzicht \> ABR BAI2-indeling** in de configuratielijst.
6. Selecteer de indeling **BAI2**.
7. Selecteer op het sneltabblad **Versies** de nieuwste versie en selecteer vervolgens **Importeren**.

>[!NOTE]
>Het **Bankafschriftmodel van BAI2** wordt later afgeschaft. 

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


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Voorbeelden van bankafschriftindelingen en technische indelingen
Hieronder ziet u voorbeelden van de technische indelingsdefinities van geavanceerde bankafstemmingsimportbestanden en drie gerelateerde voorbeeldbestanden voor bankafschriften: [Voorbeelden van importbestanden](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Technische indelingsdefinitie                             | Voorbeeldbestand van bankafschrift          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

