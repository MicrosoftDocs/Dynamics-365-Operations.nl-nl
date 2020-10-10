---
title: Export grootboektransacties
description: Dit onderwerp bevat informatie over het exporteren van grootboekrekeningsaldi naar een ASCII-bestand (tekst zonder opmaak) in CED-indeling voor België.
author: anasyash
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportExtraFieldsBE
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 273103
ms.search.region: Belgium
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.openlocfilehash: 4db6d56d72b9c3e4c9040c791e0cca279f794633
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819998"
---
# <a name="export-ledger-transactions"></a>Export grootboektransacties

[!include [banner](../includes/banner.md)]

De functie die in dit onderwerp wordt beschreven, wordt gebruikt om het totaalsaldo van elke grootboekrekening voor een bepaalde periode te exporteren naar een bestand zonder opmaak (ASCII) in CED-indeling. U kunt het gegenereerde bestand vervolgens importeren in software van derden om een boekhoudingsrapport te maken in overeenstemming met de vereisten die per land/regio gelden.

Deze functionaliteit is beschikbaar voor rechtspersonen die hun primaire adres in België hebben.

## <a name="prerequisites"></a>Vereisten

### <a name="create-posting-journals"></a>Boekingsjournalen maken

1. Ga naar **Grootboek** \> **Journaalinstellingen** \> **Boekingsjournalen**.
2. Selecteer op de pagina **Grootboekinstellingen** **Maken**. Er worden automatisch boekingsjournalen en bijbehorende nummerreeksen gemaakt.

## <a name="export-ledger-transactions-to-a-plain-text-file-in-ced-format"></a>Grootboektransacties in CED-indeling naar een bestand met tekst zonder opmaak exporteren

1. In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van ER-configuraties (elektronische rapportage) voor de volgende rapportindeling:

    - Exportindeling voor grootboektransacties (BE)

    Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](https://docs.microsoft.com/dynamics365/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

2. Ga in Dynamics 365 Finance naar **Grootboek** \> **Periodieke taken** \> **Grootboektransacties exporteren**.
3. Selecteer in het dialoogvenster **Grootboektransacties in CED-indeling naar een ASCII-bestand exporteren** in het veld **Indelingstoewijzing** de indeling **Exportindeling voor grootboektransacties (BE)** die u zojuist hebt gedownload, en selecteer vervolgens **OK**.
4. Stel in het dialoogvenster **Parameters elektronisch rapport** de volgende velden in.

| **Veld**          | **Beschrijving**                                                             |
|--------------------|-----------------------------------------------------------------------------|
| Begindatum          | Voer de eerste dag van de aangifteperiode in.                                |
| Einddatum            | Voer de laatste dag van de aangifteperiode in.                                 |
| Aangifte in euro's | Stel deze optie in op **Ja** als het bedrijf een andere valuta dan euro gebruikt. |

5. Selecteer **OK** om het txt-bestand te genereren en te downloaden.

    U boekt bijvoorbeeld de volgende grootboektransacties in het DEMF-bedrijf.

| **Datum**        | **Transactietype** | **Hoofdrekening**          | **Tegenrekening**        | **Nettobedrag** | **Btw-bedrag** | **Btw-code** |
|-----------------|----------------------|---------------------------|---------------------------|----------------|----------------|--------------------|
| 1 januari 2020 | Klantfactuur     | 110110 – Bankrekening in USD |                           | 1.000          | 190            | VAT19              |
| 1 januari 2020 | Leveranciersfactuur       |                           | 110120 – Bankrekening in CNY | 1,095          | 76.65          | EU7                |
| 1 januari 2020 | Klantfactuur     | 110115 – Bankrekening in CAD |                           | 800            | 0              | EUS                |

In dit geval bevat het gegenereerde bestand de volgende gegevens.

![Grootboektransactiegegevens](media/1_Export_ledger_transactions.png)

Hier volgt een uitleg van de kolommen in dit bestand:

- In de eerste kolom wordt de grootboekrekeningcode weergegeven.
- In de tweede kolom wordt het debetsaldo van de grootboekrekening weergegeven.
- In de derde kolom wordt het creditsaldo van de grootboekrekening weergegeven.
- In de vierde kolom wordt de naam van de grootboekrekening weergegeven.

> [!NOTE]
> Als u grootboektransacties voor klantfacturen wilt boeken, gaat u naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**. Voor leveranciersfacturen gaat u naar **Leveranciers** \> **Facturen** \> **Facturenjournaal**.
