---
title: Bronbelastingaangifte voor Worden
description: In dit onderwerp wordt uitgelegd hoe u de bronbelastingaangifte voor Indonesië configureert en genereert.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6cf2f9240ea747054578c52343af34b15c250f38
ms.sourcegitcommit: f51e74ee9162fe2b63c6ce236e514840795acfe1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943656"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Bronbelastingaangifte voor Indonesië (ID-00005)

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt be uitgelegd hoe u het PPH-bronbelastingbestand kunt instellen en genereren dat rechtspersonen in Indonesië gebruiken om bronbelastingtransacties in de e-Bupot-toepassing te rapporteren.

De belastingdienst in Indonesië (DGT) bepaalt dat belastbare ondernemers (PKP) die bij KPP Pratama zijn geregistreerd als belastinginners/inhouders van inkomstenbelasting (PPh) artikel 23 en/of artikel 26 elektronisch aangifte inkomstenbelasting artikel 23 en 26 moeten doen via de e-Bupot-toepassing. 

- **Artikel 23**: het rapport bevat alle inhoudingstransacties van leveranciers waarbij de land-/regiocode van het primaire adres de code voor Indonesië is.
- **Artikel 26**: het rapport bevat alle inhoudingstransacties van leveranciers waarbij de land-/regiocode van het primaire adres niet de code voor Indonesië is.

## <a name="prerequisites"></a>Vereisten

- Het primaire adres van de rechtspersoon moet in Indonesië zijn.
- In de werkruimte **Functiebeheer** moet de functie **Algemene bronbelasting** zijn ingeschakeld. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het inschakelen van functies.

### <a name="download-electronic-reporting-configurations"></a>Configuraties van elektronische aangifte downloaden

Het genereren van een importbestand is gebaseerd op ER-configuraties (elektronische rapportage). Zie [Elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) voor meer informatie over de capaciteiten en concepten van configureerbare rapportage.

Volg de instructies in [Configuraties voor elektronische rapportage downloaden vanuit Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) voor meer informatie over productie- en gebruikersacceptatietestomgevingen (UAT).

Upload de volgende configuraties vanuit de opslagplaats om het importbestand te genereren:

- **Belastingaangiftemodel.versie.93.xml** of een latere versie
- **Belastingaangiftemodeltoewijzing.versie.93.153.xml** of een latere versie
- **WHT PPh-schema-import (ID).versie.93.14** of een latere versie

## <a name="set-up-general-ledger-parameters"></a>Grootboekparameters instellen

1. Ga naar **Belasting** \> **Instellingen** \> **Grootboekparameters**.
2. Selecteer op het tabblad **Bronbelasting** in het veld **Indelingstoewijzing voor bronbelastingaangifte** de optie **WHT PPh-schema import (ID)**. 
3. Ga naar **Belasting** \> **Instellingen** \> **Bronbelasting** \> **Opbrengsttypen bronbelasting** om **Kode Bukti Potong** in te stellen als opbrengsttype bronbelasting en vervolgens de codes toe te wijzen aan de gerelateerde artikelbronbelastinggroepen. De codes zijn vereist voor het genereren van het integratiebestand met behulp van de e-Bupot-toepassing. 

## <a name="generate-the-withholding-import-file"></a>Het bronimportbestand genereren

Het proces van het voorbereiden en genereren van het e-Bupot-bestand voor een specifieke periode is gebaseerd op de bronbelastingtransacties die tijdens de taak voor het vereffenen of boeken van belastingbetalingen zijn geboekt.

Volg deze stappen om het bestand te genereren.

1. Ga naar **Belasting** \> **Aangiften** \> **Bronbelasting** \> **PPH-importbestand e-bupot 23 en 26**.
2. Selecteer de begin- en einddatum voor het rapport en selecteer vervolgens de vereffeningsperiode.
3. Voer de transactiedatum in en selecteer vervolgens **OK**.
4. Selecteer de taal. Alle rapporten worden vertaald in het Engels (**en-us**) en Indonesisch (**id**).
5. Selecteer het type bedrijf en voer vervolgens de cheque- en documentnummers in. 
6. Controleer of het rapport is ondertekend door de manager. Deze gegevens worden gemeld in het bestand. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
