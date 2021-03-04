---
title: Export grootboektransacties
description: Dit onderwerp bevat informatie over het exporteren van grootboekrekeningsaldi naar een ASCII-bestand (tekst zonder opmaak) in CED-indeling voor België.
author: anasyash
manager: AnnBe
ms.date: 12/02/2020
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
ms.author: roschlom
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.openlocfilehash: 4820e343604f314291146a12aa5903a85d3fe533
ms.sourcegitcommit: 0e60df840688932795b9c8f8fd45d98f5ab6ba8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2020
ms.locfileid: "4668966"
---
# <a name="export-ledger-transactions"></a>Grootboektransacties exporteren

[!include [banner](../includes/banner.md)]

De functie die in dit onderwerp wordt beschreven, wordt gebruikt om het totaalsaldo van elke grootboekrekening voor een bepaalde periode te exporteren naar een bestand zonder opmaak (ASCII) in CED-indeling. U kunt het gegenereerde bestand vervolgens importeren in software van derden om een boekhoudingsrapport te maken in overeenstemming met de vereisten die per land/regio gelden.

Deze functionaliteit is beschikbaar voor rechtspersonen die hun primaire adres in België hebben.

## <a name="prerequisites"></a>Vereisten

### <a name="create-posting-journals"></a>Boekingsjournalen maken

1. Ga naar **Grootboek** \> **Journaalinstellingen** \> **Boekingsjournalen**.
2. Selecteer op de pagina **Grootboekinstellingen** **Maken**. Er worden automatisch boekingsjournalen en bijbehorende nummerreeksen gemaakt.

## <a name="export-ledger-transactions-to-a-plain-text-file-in-ced-format"></a>Grootboektransacties in CED-indeling naar een bestand met tekst zonder opmaak exporteren

### <a name="setup"></a>Instelling

1. Importeer uit de [algemene Microsoft-opslagplaats](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md) de meest recente versies van de ER-configuraties (Elektronische rapportage) voor de volgende rapportindeling.

    | **Dynamics 365 Finance-versie**          | **Configuratienaam**                                                                                           |
    |-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
    | Vóór 10.0.16                            | **Exportindeling van grootboektransacties (BE)** onder **Grootboekrekeningrapporten** > **Exporteren van grootboektransacties**-modle. |
    | Vanaf 10.0.16                     | **Exporteren van grootboekgegevens (BE)** onder model **Standaard auditfile (SAF-T)**.                                  |

    > ![ER-configuraties](media/be-audit-er-configs.png)

2. Na het importeren moeten de volgende of latere versies van de nieuwe configuraties zijn geïnstalleerd.

    | **Naam van ER-configuratie**         | **Type**           | **Versie** | **Beschrijving**                                                                                                             |
    |-----------------------------------|--------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------|
    | Standaardcontrolebestand (SAF-T)       | Model              | 82          | Het algemene ER-model voor standaard auditfiles.                                                                               |
    | Modeltoewijzing van grootboekgegevens | Modeltoewijzing      | 82.13       | De modeltoewijzing waarmee gegevensbronnen voor grootboekgegevens worden gedefinieerd.                                                        |
    | Grootboekgegevens exporteren (BE)   | Indeling (exporteren) | 82.8        | De tekstindeling voor de grootboekgegevens die kunnen worden geïmporteerd in software van derden. |

    > [!NOTE]
    > Nadat alle ER-configuraties uit de voorgaande tabel zijn geïmporteerd, stelt u de optie **Standaard voor modeltoewijzing** in op **Ja** voor de configuratie van **Modeltoewijzing van grootboekgegevens** op de pagina **Configuraties**.

    > ![Optie Standaard voor modeltoewijzing](media/be-audit-default-mm.png)

3. Vanaf versie 10.0.16: om de indeling **Exporteren van grootboekgegevens (BE)** te gebruiken, definieert u de naam van de ER-configuratie in een nieuwe grootboekparameter. Ga naar **Grootboek** > **Grootboek instellen** > **Grootboekparameters**. 
4. Vouw het sneltabblad **Elektronische rapportage** uit en selecteer het tabblad **Grootboek**. 
5. Selecteer in de groep **Grootboektransacties exporteren** in het veld **Grootboektransacties exporteren** de indeling **Exporteren van grootboekgegevens (BE)** en sla de nieuwe instelling op.

    ![Grootboekparameter](media/be-audit-gl-parameter.png)

### <a name="generate-the-export-ledger-transactions-report"></a>Het rapport Grootboektransacties exporteren genereren

1. Ga in Finance naar **Grootboek** \> **Periodieke taken** \> **Grootboektransacties exporteren**.
2. Als uw Finance-versie lager is dan 10.0.16, selecteert u in het dialoogvenster **Grootboektransacties in CED-indeling naar een ASCII-bestand exporteren** in het veld **Indelingstoewijzing** de indeling **Exportindeling voor grootboektransacties (BE)** die u zojuist hebt gedownload, en selecteer vervolgens **OK**. Geef vanaf versie 10.0.16 de ER-indeling op in de grootboekparameters. Wanneer de ER-indeling is gedefinieerd in de grootboekparameters, wordt deze door het systeem gebruikt om rapporten te genereren.
3. Geef de rapportageperiode op in de velden **Vanaf datum** en **Tot datum** in het dialoogvenster **Parameters voor elektronische rapporten**.
4. Als de valuta voor de boekhouding van uw rechtspersoon niet EURO is en u het rapport wilt genereren in EURO, selecteert u **Herberekenen naar EURO** in het dialoogvenster. Wanneer de boekhoudingsvaluta niet EURO maar de rapportagevaluta is en u **Herberekenen naar EURO** selecteert, wordt er een rapport gegenereerd met de bedragen die in het grootboek zijn opgeslagen in de rapportagevaluta. Wanneer de boekhoudingsvaluta of rapportagevaluta geen EURO is en u **Herberekenen naar EURO** selecteert, worden de bedragen in de boekhoudingsvaluta automatisch opnieuw berekend naar EURO door de wisselkoers te gebruiken die in het systeem is opgeslagen op de datum van elke transactie in het grootboek. Het genereren van het rapport kan langer duren dan een rapport dat zonder herberekening is gegenereerd.
5. Wanneer u het rapport **Grootboektransacties exporteren** voor een langere periode genereert, voert u dit in batches uit. Als u het rapport in batches wilt uitvoeren, vouwt u het sneltabblad **Op de achtergrond uitvoeren** uit, markeert u de parameter **Batchverwerking** en geeft u desgewenst andere parameters van de batch op. Volg het genereren van het rapport op de pagina **Elektronische rapportagetaken** op.
6. Selecteer **OK** om het txt-bestand te genereren en te downloaden.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]