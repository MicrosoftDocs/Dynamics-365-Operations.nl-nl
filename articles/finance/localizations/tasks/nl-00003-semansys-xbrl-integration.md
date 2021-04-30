---
title: Semansys XBRL-integratie
description: Deze procedure begeleidt u door het gebruik van Nederlandse functionaliteit om financiële gegevens naar de XML-indeling te exporteren.
author: mrolecki
ms.date: 05/28/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Netherlands
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62364a5b7fba2a9dec2e63657556d90828109c19
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892337"
---
# <a name="deliver-xbrl-to-the-dutch-regulatory-body-via-semansys-xbrlone"></a>XBRL aan de Nederlandse regelgevende instantie bezorgen via Semansys XBRLOne

[!include [banner](../../includes/banner.md)]

Dit onderwerp begeleidt u door de stappen voor het toewijzen, exporteren en leveren van XBRL (eXtensible Business Reporting Language) aan de Nederlandse regelgevende instantie.  

Het proces op hoog niveau is een proces van systeem naar mens naar systeem. Het eerste systeem waarvoor dit gevolgen heeft, is Microsoft Dynamics 365 Finance. Dit systeem is verantwoordelijk voor het maken van alle benodigde vermeldingen, rekeningschema's en toewijzingen. Nadat dit is voltooid, exporteert een gebruiker de gegevens in de Semansys DataBridge-indeling. Deze geëxporteerde gegevens kunnen vervolgens naar de XBRLOne-portal worden geüpload om naar XBRL te worden geconverteerd en vervolgens worden gevalideerd en bij de juiste Nederlandse regelgevende instantie worden afgeleverd. 

Voor dit proces zijn de volgende vereisten nodig:

- De rapportgegevens zijn beschikbaar voor toewijzing via Grootboek in Finance.
- Kennis van de juiste taxonomie waarvoor u rapporteert en de bevestiging dat u aan een Nederlandse regelgevende instantie levert.
- Importeer de elektronische rapporteringsconfiguraties **Nederlands XBRL-integratiemodel** en **Semansys XBRL (NL)**.

Zie voor meer informatie over het downloaden van ER-configuraties vanuit Microsoft Dynamics Lifecycle Services (LCS) [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](../../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

In het volgende voorbeeld ziet u welke stappen een gebruiker moet uitvoeren om de gegevens voor een jaarrapport voor 2019 te exporteren. 

1. Ga naar **Grootboek** > **Periodieke taken** > **Financiële gegevens naar XBRL exporteren**.
2. Voer een datum in het veld **Begindatum** in. Bijvoorbeeld *01/01/2019*.  
3. Voer een datum in het veld **Einddatum** in. Bijvoorbeeld *31/12/2019*.
4. Voer in het veld **Indelingstoewijzing** de juiste indelingen in.
5. Selecteer **OK**.

U kunt het Semansys DataBridge-indelingspakket nu naar de XBRLOne-portal overdragen voor de volgende stappen in het proces.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]