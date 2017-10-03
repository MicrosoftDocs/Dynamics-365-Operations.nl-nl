---
title: Het importproces voor geavanceerde bankafstemming instellen
description: Met de functie Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. In dit artikel wordt uitgelegd hoe u de importfunctionaliteit voor uw bankafschriften kunt instellen.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a4d1c81386c0ef03391f3127fa51a6b09a5142b3
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Het importproces voor geavanceerde bankafstemming instellen

[!include[banner](../includes/banner.md)]


Met de functie Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. In dit artikel wordt uitgelegd hoe u de importfunctionaliteit voor uw bankafschriften kunt instellen. 

De instelling voor de importeren van bankafschriften varieert, afhankelijk van de indeling van uw elektronische bankafschrift. Finance and Operations ondersteunt standaard drie indelingen voor bankafschriften: ISO20022, MT940 en BAI2.

## <a name="sample-files"></a>Voorbeeldbestanden
Voor alle drie indelingen moet u bestanden hebben die het elektronische bankafschrift vertalen van de oorspronkelijke indeling naar een indeling die in Finance and Operations kan worden gebruikt. U kunt de vereiste resourcebestanden vinden onder het knooppunt **Resources** in Application Explorer in Microsoft Visual Studio. Nadat u de bestanden hebt gevonden, kopieert u deze naar een enkele bekende locatie, zodat u ze gemakkelijker kunt uploaden tijdens het instellingsproces.

| Naam van bron                                           | Bestandsnaam                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Voorbeelden van bankafschriftindelingen en technische indelingen
Hieronder ziet u voorbeelden van de technische indelingsdefinities van geavanceerde bankafstemmingsimportbestanden en drie gerelateerde voorbeeldbestanden voor bankafschriften: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Technische indelingsdefinitie                             | Voorbeeldbestand van bankafschrift          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>De import van ISO20022-bankafschriften instellen
Eerst moet u de verwerkingsgroep voor de indeling voor bankafschriften definiëren voor ISO20022-bankafschriften met behulp van het gegevensentiteitsraamwerk.

1.  Ga naar **Werkgebieden** &gt; **Gegevensbeheer**.
2.  Klik op **Importeren**.
3.  Voer een naam voor de indeling in, zoals **ISO20022**.
4.  Stel het veld **Indeling van brongegevens** in op **XML-element**.
5.  Stel het veld **Entiteitnaam** in op **Bankafschriften**.
6.  U kunt de importbestanden uploaden door op **Uploaden** te klikken en te bladeren om het bestand **SampleBankCompositeEntity.xml** te selecteren dat u eerder hebt opgeslagen.
7.  Nadat de entiteit Bankafschriften is geüpload en de toewijzing is voltooid, klikt u op de actie **Kaart weergeven** voor de entiteit.
8.  De entiteit Bankafschriften is een samengestelde entiteit die uit vier afzonderlijke entiteiten bestaat. Selecteer in de lijst **BankStatementDocumentEntity** en klik vervolgens op de actie **Kaart weergeven**.
9.  Klik op het tabblad **Transformaties** op **Nieuw**.
10. Klik voor volgnummer 1 op **Bestand uploaden** en selecteer het bestand **ISO20022XML-to-Reconciliation.xslt** dat u eerder hebt opgeslagen. **Opmerking:** Finance and Operations-transformatiebestanden worden gebouwd voor de standaardindeling. Omdat banken vaak afwijken van deze indeling, moet u het transformatiebestand mogelijk bijwerken om het af te stemmen op uw indeling voor bankafschriften. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Klik op **Nieuw**.
12. Klik voor volgnummer 2 op **Bestand uploaden** en selecteer het bestand **BankReconciliation-to-Composite.xslt** dat u eerder hebt opgeslagen.
13. Klik op **Transformaties toepassen**.

Nadat de verwerkingsgroep van de indeling is ingesteld, is de volgende stap het definiëren van de regels voor de indeling voor bankafschriften voor ISO20022-bankafschriften.

1.  Ga naar **Kas- en bankbeheer** &gt; **Instellingen** &gt; **Instelling van geavanceerde bankafstemming** &gt; **Indeling bankafschrift**.
2.  Klik op **Nieuw**.
3.  Geef een indeling voor afschriften op, zoals **ISO20022**.
4.  Voer een naam in voor de indeling.
5.  Stel het veld **Verwerkingsgroep** in op de groep die u eerder hebt gedefinieerd, zoals **ISO20022**.
6.  Schakel het selectievakje **XML-bestand** in.

De laatste stap is het inschakelen van geavanceerde bankafstemming en het instellen van de indeling voor bankafschriften voor de bankrekening.

1.  Ga naar **Kas- en bankbeheer** &gt; **Bankrekeningen**.
2.  Selecteer de bankrekening en open deze om de details weer te geven.
3.  Stel op het tabblad **Afstemming** de optie **Geavanceerde bankafstemming** in op **Ja**.
4.  Stel het veld **Afschriftindeling** in op de indeling die u eerder hebt gemaakt, zoals **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>De import van MT940-bankafschriften instellen
Eerst moet u de verwerkingsgroep voor de indeling voor bankafschriften definiëren voor MT940-bankafschriften met behulp van het gegevensentiteitsraamwerk.

1.  Ga naar **Werkgebieden** &gt; **Gegevensbeheer**.
2.  Klik op **Importeren**.
3.  Voer een naam voor de indeling in, zoals **MT940**.
4.  Stel het veld **Indeling van brongegevens** in op **XML-element**.
5.  Stel het veld **Entiteitnaam** in op **Bankafschriften**.
6.  U kunt importbestanden uploaden door op **Uploaden** te klikken en te bladeren om het bestand **SampleBankCompositeEntity.xml** te selecteren dat u eerder hebt opgeslagen.
7.  Nadat de entiteit Bankafschriften is geüpload en de toewijzing is voltooid, klikt u op de actie **Kaart weergeven** voor de entiteit.
8.  De entiteit Bankafschriften is een samengestelde entiteit die uit vier afzonderlijke entiteiten bestaat. Selecteer in de lijst **BankStatementDocumentEntity** en klik vervolgens op de actie **Kaart weergeven**.
9.  Klik op het tabblad **Transformaties** op **Nieuw**.
10. Klik voor volgnummer 1 op **Bestand uploaden** en selecteer het bestand **MT940TXT-to-MT940XML.xslt** dat u eerder hebt opgeslagen.
11. Klik op **Nieuw**.
12. Klik voor volgnummer 2 op **Bestand uploaden** en selecteer het bestand **MT940XML-to-Reconciliation.xslt** dat u eerder hebt opgeslagen. **Opmerking:** Finance and Operations-transformatiebestanden worden gebouwd voor de standaardindeling. Omdat banken vaak afwijken van deze indeling, moet u het transformatiebestand mogelijk bijwerken om het af te stemmen op uw indeling voor bankafschriften. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Klik op **Nieuw**.
14. Klik voor volgnummer 3 op **Bestand uploaden** en selecteer het bestand **BankReconciliation-to-Composite.xslt** dat u eerder hebt opgeslagen.
15. Klik op **Transformaties toepassen**.

Nadat de verwerkingsgroep van de indeling is ingesteld, is de volgende stap het definiëren van de regels voor de indeling voor bankafschriften voor MT940-bankafschriften.

1.  Ga naar **Kas- en bankbeheer** &gt; **Instellingen** &gt; **Instelling van geavanceerde bankafstemming** &gt; **Indeling bankafschrift**.
2.  Klik op **Nieuw**.
3.  Geef een indeling voor afschriften op, zoals **MT940**.
4.  Voer een naam in voor de indeling.
5.  Stel het veld **Verwerkingsgroep** in op de groep die u eerder hebt gedefinieerd, zoals **MT940**.
6.  Stel het veld **Bestandstype** in op **txt**.

De laatste stap is het inschakelen van geavanceerde bankafstemming en het instellen van de indeling voor bankafschriften voor de bankrekening.

1.  Ga naar **Kas- en bankbeheer** &gt; **Bankrekeningen**.
2.  Selecteer de bankrekening en open deze om de details weer te geven.
3.  Stel op het tabblad **Afstemming** de optie **Geavanceerde bankafstemming** in op **Ja**.
4.  Wanneer u gevraagd uw selectie te bevestigen en geavanceerde bankafstemming in te schakelen, klikt u op **OK**.
5.  Stel het veld **Afschriftindeling** in op de indeling die u eerder hebt gemaakt, zoals **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>De import van BAI2-bankafschriften instellen
Eerst moet u de verwerkingsgroep voor de indeling voor bankafschriften definiëren voor BAI2-bankafschriften met behulp van het gegevensentiteitsraamwerk.

1.  Ga naar **Werkgebieden** &gt; **Gegevensbeheer**.
2.  Klik op **Importeren**.
3.  Voer een naam voor de indeling in, zoals **BAI2**.
4.  Stel het veld **Indeling van brongegevens** in op **XML-element**.
5.  Stel het veld **Entiteitnaam** in op **Bankafschriften**.
6.  U kunt importbestanden uploaden door op **Uploaden** te klikken en te bladeren om het bestand **SampleBankCompositeEntity.xml** te selecteren dat u eerder hebt opgeslagen.
7.  Nadat de entiteit Bankafschriften is geüpload en de toewijzing is voltooid, klikt u op de actie **Kaart weergeven** voor de entiteit.
8.  De entiteit Bankafschriften is een samengestelde entiteit die uit vier afzonderlijke entiteiten bestaat. Selecteer in de lijst **BankStatementDocumentEntity** en klik vervolgens op de actie **Kaart weergeven**.
9.  Klik op het tabblad **Transformaties** op **Nieuw**.
10. Klik voor volgnummer 1 op **Bestand uploaden** en selecteer het bestand **BAI2CSV-to-BAI2XML.xslt** dat u eerder hebt opgeslagen.
11. Klik op **Nieuw**.
12. Klik voor volgnummer 2 op **Bestand uploaden** en selecteer het bestand **BAI2XML-to-Reconciliation.xslt** dat u eerder hebt opgeslagen. **Opmerking:** Finance and Operations-transformatiebestanden worden gebouwd voor de standaardindeling. Omdat banken vaak afwijken van deze indeling, moet u het transformatiebestand mogelijk bijwerken om het af te stemmen op uw indeling voor bankafschriften. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Klik op **Nieuw**.
14. Klik voor volgnummer 3 op **Bestand uploaden** en selecteer het bestand **BankReconciliation-to-Composite.xslt** dat u eerder hebt opgeslagen.
15. Klik op **Transformaties toepassen**.

Nadat de verwerkingsgroep van de indeling is ingesteld, is de volgende stap het definiëren van de regels voor de indeling voor bankafschriften voor BAI2-bankafschriften.

1.  Ga naar **Kas- en bankbeheer** &gt; **Instellingen** &gt; **Instelling van geavanceerde bankafstemming** &gt; **Indeling bankafschrift**.
2.  Klik op **Nieuw**.
3.  Geef een indeling voor afschriften op, zoals **BAI2**.
4.  Voer een naam in voor de indeling.
5.  Stel het veld **Verwerkingsgroep** in op de groep die u eerder hebt gedefinieerd, zoals **BAI2**.
6.  Stel het veld **Bestandstype** in op **txt**.

De laatste stap is het inschakelen van geavanceerde bankafstemming en het instellen van de indeling voor bankafschriften voor de bankrekening.

1.  Ga naar **Kas- en bankbeheer** &gt; **Bankrekeningen**.
2.  Selecteer de bankrekening en open deze om de details weer te geven.
3.  Stel op het tabblad **Afstemming** de optie **Geavanceerde bankafstemming** in op **Ja**.
4.  Wanneer u gevraagd uw selectie te bevestigen en geavanceerde bankafstemming in te schakelen, klikt u op **OK**.
5.  Stel het veld **Afschriftindeling** in op de indeling die u eerder hebt gemaakt, zoals **BAI2**.

## <a name="test-the-bank-statement-import"></a>De import van bankafschriften testen
De laatste stap is testen of u uw bankafschrift kunt importeren.

1.  Ga naar **Kas- en bankbeheer** &gt; **Bankrekeningen**.
2.  Selecteer de bankrekening waarvoor de functie voor geavanceerde bankafstemming is ingeschakeld.
3.  Klik op het tabblad **Afstemmen** op **Bankafschriften**.
4.  Klik op de pagina **Bankafschrift** op **Afschrift importeren**.
5.  Stel het veld **Bankrekening** in op de geselecteerde bankrekening. Het veld **Afschriftindeling** wordt automatisch ingesteld, op basis van de instelling voor de bankrekening.
6.  Klik op **Bladeren** en selecteer uw elektronisch bankafschriftbestand.
7.  Klik op **Uploaden**.
8.  Klik tot slot op **OK**.

Als het importeren is voltooid, ontvangt u een bericht waarin wordt gemeld dat het afschrift is geïmporteerd. Als de import niet is gelukt, zoekt u de taak in de werkruimte **Gegevensbeheer** in de sectie **Taakgeschiedenis**. Klik op **Uitvoeringsdetails** voor de taak om de pagina **Uitvoeringsoverzicht** en klik vervolgens op **Uitvoeringslogboek weergeven** om de importfouten te bekijken.




