---
title: Problemen oplossen met importeren van bankafschriftbestanden
description: Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 Finance ondersteunt. Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren. Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten. Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand. In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc5b9cf3449b48767a27891a019f8fe8df2a900559898e3cb1849d25bec7c987
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757116"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Problemen oplossen met importeren van bankafschriftbestanden

[!include [banner](../includes/banner.md)]

Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 Finance ondersteunt. Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren. Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten. Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand. In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.

## <a name="what-is-the-error"></a>Wat is de fout?

Nadat u hebt geprobeerd een bankafschriftbestand te importeren, gaat u naar de geschiedenis van de taak in Gegevensbeheer en zoekt u de fout op in de uitvoeringsdetails. De foutmelding kan helpen door te verwijzen naar het afschrift, het saldo, of de afschriftregel. Hij bevat waarschijnlijk onvoldoende informatie om u te helpen het veld of het element te identificeren dat het probleem veroorzaakt.

> [!NOTE]
> Geïmporteerde bankafschriften kunnen slechts één moment in de tijd overlappen.  Als een afschrijft bijvoorbeeld op 1 januari 2021 om 00:00 uur eindigt, kan de begindatum voor de volgende afschrift 00:00 uur zijn op 1 januari 2021.

## <a name="what-are-the-differences"></a>Wat zijn de verschillen?
Vergelijk de indelingsdefinitie van het bankbestand met de importdefinitie van Finance en noteer eventuele verschillen tussen de velden en de elementen. Vergelijk het bankafschriftbestand met het gerelateerde Finance-voorbeeldbestand. Eventuele verschillen moeten gemakkelijk te zien zijn in de ISO20022-bestanden.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Verschillen in tijdzones op geïmporteerde bankafschriften
De datum-/tijdwaarden in het importbestand kunnen verschillen van de datum-/tijdwaarden die worden weergegeven in Finance and Operations. U kunt dit verschil voorkomen door een tijdzonevoorkeur in te voeren op de pagina **Gegevensbronnen configureren**. Zie [Het importproces voor geavanceerde bankafstemming instellen](set-up-advanced-bank-reconciliation-import-process.md) voor meer informatie over het invoeren van een tijdzonevoorkeur.

## <a name="transformations"></a>Transformaties
Doorgaans moeten wijzigingen worden doorgevoerd in één van drie transformaties. Elke transformatie is geschreven voor een specifieke standaard.

| Naam van bron                                         | Bestandsnaam                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Foutopsporing in transformaties
### <a name="adjust-the-bai2-and-mt940-files"></a>De BAI2- en MT940-bestanden aanpassen

De BAI2- en MT940-bestanden zijn op tekst gebaseerde bestanden en moeten worden aangepast om foutopsporing van Extensible Stylesheet Language-transformaties mogelijk te maken. Het programma voert deze aanpassing door wanneer een bestand wordt geïmporteerd.

1.  Maak een XML-bestand en kopieer hier de volgende tekst in.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Kopieer de inhoud van het bankafschriftbestand en vervang de tekst **PASTESTATEMENTFILEHERE** in het XML-bestand door de gekopieerde tekst.

### <a name="debug-the-xslt"></a>Foutopsporing van de XSLT

Zie <https://msdn.microsoft.com/library/ms255605.aspx> voor meer informatie.

1.  Start Microsoft Visual Studio.
2.  Maak een consoletoepassing aan.
3.  Open de betreffende XSLT.
4.  Klik op de XLST en de eigenschappenpagina ervan.
5.  Stel de invoer in op de locatie van het bankafschriftbestand.
6.  Definieer een locatie en een bestandsnaam voor de uitvoer.
7.  Stel de vereiste onderbrekingspunten in.
8.  Klik in het menu op **XML** &gt; **XSLT-foutopsporing starten**.

### <a name="format-the-xslt-output"></a>De XSLT-uitvoer opmaken

Tijdens het uitvoeren van de transformatie wordt een uitvoerbestand aangemaakt dat u in Visual Studio kunt weergeven. Door middel van Ctrl+A, Ctrl+K en Ctrl+D kunt u het outputbestand snel opmaken.

### <a name="adjust-the-transformation"></a>De transformatie aanpassen

Pas de transformatie aan om het gewenste veld of element in het bankafschriftbestand te krijgen. Wijs vervolgens dat veld of element toe aan het juiste Finance-element.

### <a name="debitcredit-indicator"></a>Debet- of creditindicator

Soms komt het voor dat debetbedragen worden geïmporteerd als creditbedragen en andersom. Om dit probleem op te lossen, moet u de betreffende XSLT aanpassen. Als u bankafschriften van meerdere banken ontvangt, controleer dan of ze allemaal dezelfde debet-/creditbenadering gebruiken, of maak afzonderlijke transformaties aan.

-   BAI2XML-to-Reconciliation.xlst sjabloon GetAmountCreditDebitIndicator
-   ISO20022XML-to-Reconcilation.xslt sjabloon GetCreditDebit
-   MT940XML-to-Reconcilation.xslt sjabloon GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Voorbeelden van bankafschriftindelingen en technische indelingen
In de onderstaande tabel ziet u voorbeelden van de technische indelingsdefinities voor geavanceerde bankafstemmingsimportbestanden en drie bijbehorende voorbeeldbestanden van bankafschriften: U kunt de voorbeeldbestanden en technische indelingen hier downloaden: [Voorbeelden van importbestanden](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Technische indelingsdefinitie                             | Voorbeeldbestand van bankafschrift          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
