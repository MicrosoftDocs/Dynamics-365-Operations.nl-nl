---
title: Problemen oplossen met importeren van bankafschriftbestanden
description: Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 for Finance and Operations ondersteunt. Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren. Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten. Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand. In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4006bf35673e3bb61bcf11619ecc68d295f29eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554823"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Problemen oplossen met importeren van bankafschriftbestanden

[!include [banner](../includes/banner.md)]

Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 for Finance and Operations ondersteunt. Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren. Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten. Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand. In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.

<a name="what-is-the-error"></a>Wat is de fout?
------------------

Nadat u hebt geprobeerd een bankafschriftbestand te importeren, gaat u naar de geschiedenis van de taak in Gegevensbeheer en zoekt u de fout op in de uitvoeringsdetails. De foutmelding kan helpen door te verwijzen naar het afschrift, het saldo, of de afschriftregel. Hij bevat waarschijnlijk onvoldoende informatie om u te helpen het veld of het element te identificeren dat het probleem veroorzaakt.

## <a name="what-are-the-differences"></a>Wat zijn de verschillen?
Vergelijk de indelingsdefinitie van het bankbestand met de importdefinitie van Finance and Operations en noteer eventuele verschillen tussen de velden en de elementen. Vergelijk het bankafschriftbestand met het gerelateerde Finance and Operations-voorbeeldbestand. Eventuele verschillen moeten gemakkelijk te zien zijn in de ISO20022-bestanden.

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

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopieer de inhoud van het bankafschriftbestand en vervang de tekst **PASTESTATEMENTFILEHERE** in het XML-bestand door de gekopieerde tekst.

### <a name="debug-the-xslt"></a>Foutopsporing van de XSLT

Zie <https://msdn.microsoft.com/en-us/library/ms255605.aspx> voor meer informatie.

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

Pas de transformatie aan om het gewenste veld of element in het bankafschriftbestand te krijgen. Wijs vervolgens dat veld of element toe aan het juiste Finance and Operations-element.

### <a name="debitcredit-indicator"></a>Debet- of creditindicator

Soms komt het voor dat debetbedragen worden geïmporteerd als creditbedragen en andersom. Om dit probleem op te lossen, moet u de betreffende XSLT aanpassen. Als u bankafschriften van meerdere banken ontvangt, controleer dan of ze allemaal dezelfde debet-/creditbenadering gebruiken, of maak afzonderlijke transformaties aan.

-   BAI2XML-to-Reconciliation.xlst sjabloon GetAmountCreditDebitIndicator
-   ISO20022XML-to-Reconcilation.xslt sjabloon GetCreditDebit
-   MT940XML-to-Reconcilation.xslt sjabloon GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Voorbeelden van bankafschriftindelingen en technische indelingen
In de onderstaande tabel ziet u voorbeelden van de technische indelingsdefinities voor geavanceerde bankafstemmingsimportbestanden en drie bijbehorende voorbeeldbestanden van bankafschriften: U kunt de voorbeeldbestanden en technische indelingen hier downloaden: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Technische indelingsdefinitie                             | Voorbeeldbestand van bankafschrift          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





