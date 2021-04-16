---
title: Fouten opsporen in gegevensbronnen van een uitgevoerde ER-indeling om gegevensstromen en transformatie te analyseren
description: In dit onderwerp wordt uitgelegd hoe u fouten kunt opsporen in de gegevensbronnen van een uitgevoerde ER-indeling om de geconfigureerde gegevensstroom en transformatie beter te begrijpen.
author: NickSelin
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: fe3e6a4223fc8b26e523a982a2e1752a34b370de
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753667"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Fouten opsporen in gegevensbronnen van een uitgevoerde ER-indeling om gegevensstromen en transformatie te analyseren

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Wanneer u een oplossing voor Elektronische rapportage (ER) [configureert](tasks/er-format-configuration-2016-11.md) om uitgaande documenten te genereren, definieert u de methoden die worden gebruikt om gegevens uit de toepassing te halen en deze in te voeren in de gegenereerde uitvoer. Om de levenscyclusondersteuning van de ER-oplossing efficiënter te maken, moet uw oplossing bestaan uit een ER-[gegevensmodel](general-electronic-reporting.md#DataModelComponent) en de bijbehorende [toewijzings](general-electronic-reporting.md#ModelMappingComponent)componenten, en ook uit een ER-[indeling](general-electronic-reporting.md#FormatComponentOutbound) en toewijzingsonderdelen, zodat de modeltoewijzing toepassingsspecifiek is terwijl andere componenten toepassingsonafhankelijk blijven. Dit betekent dat verschillende ER-onderdelen [van invloed zijn op](general-electronic-reporting.md#FormatComponentOutbound) het invoerproces van gegevens in de gegenereerde uitvoer.

Soms zien de gegevens van de gegenereerde uitvoer er anders uit dan dezelfde gegevens in de toepassingsdatabase. In deze gevallen moet u bepalen welk ER-onderdeel verantwoordelijk is voor de gegevenstransformatie. De functie voor het oplossen van fouten in ER-gegevensbronnen vermindert de tijd en kosten die bij dit onderzoek zijn betrokken. U kunt de uitvoering van een ER-indeling onderbreken en de interface van het foutopsporingsprogramma voor gegevensbronnen openen. Daar kunt u bladeren in de beschikbare gegevensbronnen en een afzonderlijke gegevensbron selecteren voor uitvoering. Deze handmatige uitvoering simuleert de uitvoering van de gegevensbron tijdens de echte uitvoering van een ER-indeling. Het resultaat wordt weergegeven op een pagina waar u de ontvangen gegevens kunt analyseren.

Als u de functie voor foutopsporing in gegevensbronnen wilt inschakelen, stelt u de optie **Foutopsporing in gegevens bij indelingsuitvoering inschakelen** in op **Ja** in de ER-gebruikersparameters. U kunt vervolgens foutopsporing starten in de gegevensbron terwijl u een ER-indeling uitvoert om uitgaande documenten te genereren. U kunt ook de optie **Foutopsporing starten** gebruiken om foutopsporing in de gegevensbron te starten voor een ER-indeling die is geconfigureerd in de [ER Operations-ontwerper](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).

Dit onderwerp bevat richtlijnen voor het starten van foutopsporing in gegevensbronnen voor uitgevoerde ER-indelingen. Het geeft uitleg over de informatie die u kan helpen bij het begrijpen van de gegevensstroom en gegevenstransformaties. De voorbeelden in dit onderwerp gebruiken het bedrijfsproces voor het verwerken van leveranciersbetalingen.

## <a name="limitations"></a>Beperkingen

U kunt de foutopsporing voor gegevensbronnen gebruiken om toegang te krijgen tot gegevensbronnen die worden gebruikt in ER-indelingen voor het genereren van uitgaande documenten. U kunt geen fouten oplossen in gegevensbronnen met ER-indelingen die zijn ontworpen om inkomende documenten te parseren.

De volgende instellingen voor ER-indelingen zijn op dit moment niet toegankelijk voor foutopsporing in gegevensbronnen:

- Indelingen van transformaties
- Indeling en toewijzing van validatieregels
- Expressies inschakelen
- Details van gegevensverzameling in het geheugen

## <a name="prerequisites"></a>Vereisten

- Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot een van de volgende [rollen](../sysadmin/tasks/assign-users-security-roles.md):

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Het bedrijf moet worden ingesteld op **DEMF**.

- Volg de stappen in [bijlage 1](#appendix1) van dit onderwerp om de onderdelen van de Microsoft ER-oplossing te downloaden die vereist zijn om leveranciersbetalingen te verwerken.
- Volg de stappen in [bijlage 2](#appendix2) van dit onderwerp om Leveranciers voor te bereiden voor de verwerking van leveranciersbetalingen met de gedownloade ER-oplossing.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Een leveranciersbetaling verwerken om een betalingsbestand op te halen

1. Volg de stappen in [bijlage 3](#appendix3) van dit onderwerp om leveranciersbetalingen te verwerken.

    ![Verwerking van leveranciersbetalingen wordt uitgevoerd](./media/er-data-debugger-process-payment.png)

2. Download het zipbestand en sla het op op uw lokale computer.
3. Pak het betalingsbestand **ISO20022 Credit transfer.xml** in het zipbestand uit.
4. Open het uitgepakte betalingsbestand met de XML-bestandsviewer.

    De IBAN-code (International Bank Account Number) van de bankrekening van de leverancier bevat geen spaties. Dit wijkt af van de waarde die is [ingevoerd](#enteredIBANcode) op de pagina **Bankrekeningen**.

    ![IBAN-code zonder spaties](./media/er-data-debugger-payment-file.png)

    U kunt het foutopsporingsprogramma voor ER-gegevensbronnen gebruiken om te achterhalen door welk onderdeel van de ER-oplossing spaties in de IBAN-code worden verwijderd.

## <a name="turn-on-data-source-debugging"></a>Foutopsporing in gegevensbronnen inschakelen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de optie **Foutopsporing in gegevens bij indelingsuitvoering inschakelen** in op **Ja**.

    > [!NOTE]
    > Deze parameter specifiek is voor de gebruiker en het bedrijf.

    ![Dialoogvenster voor gebruikersparameters](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Een leveranciersbetaling verwerken voor foutopsporing

1. Volg de stappen in [bijlage 3](#appendix3) van dit onderwerp om leveranciersbetalingen te verwerken.
2. Selecteer **Ja** in het berichtvak om te bevestigen dat u de verwerking van leveranciersbetalingen wilt onderbreken en in plaats daarvan foutopsporing in de gegevensbron wilt starten op de pagina **Fouten opsporen in gegevensbronnen**.

    ![Venster met bevestigingsbericht](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Fouten opsporen in gegevensbronnen die worden gebruikt bij betalingsverwerking

### <a name="debug-the-model-mapping"></a>Foutopsporing uitvoeren in de modeltoewijzing

1. Selecteer op de pagina **Fouten opsporen in gegevensbronnen** in het actievenster **Modeltoewijzing** om de foutopsporing in dit ER-onderdeel te starten.
2. Selecteer in het deelvenster met de gegevensbron aan de linkerkant de gegevensbron **\$notSentTransactions** en selecteer **Alle records lezen**.

    U kunt de opties **1 record lezen**, **10 records lezen**, **100 records lezen** of **Alle records lezen** kiezen om te bepalen hoeveel records moeten worden gelezen van de geselecteerde gegevensbron. Op deze manier kunt u de toegang tot de gegevensbron simuleren vanuit de actieve ER-indeling.

3. Selecteer in het gegevensvenster aan de rechterkant de optie **Alles uitvouwen**.

    U ziet dat de geselecteerde gegevensbron van het type **Recordlijst** één record bevat.

4. Vouw de gegevensbron **\$notSentTransactions** uit en selecteer de geneste methode **vendBankAccountInTransactionCompany()**.
5. Vouw de methode **vendBankAccountInTransactionCompany()** uit en selecteer het geneste veld **IBAN**.
6. Selecteer **Waarde ophalen**.

    U kunt **Waarde ophalen** selecteren om de waarde van een geselecteerd veld van de geselecteerde gegevensbron te laten lezen. Op deze manier kunt u de toegang tot dit veld simuleren vanuit de actieve ER-indeling.

7. Selecteer **Alles uitvouwen**.

    ![Waarde van het IBAN-veld in de modeltoewijzing](./media/er-data-debugger-debugging-model-mapping.png)

    Zoals u ziet, is de modeltoewijzing niet verantwoordelijk voor de afgekapte spaties, omdat de geretourneerde IBAN-code voor de bankrekening van de leverancier spaties bevat. Daarom moet u de foutopsporing voor gegevensbronnen voortzetten.

### <a name="debug-the-format-mapping"></a>Fouten opsporen in de indelingstoewijzing

1. Selecteer op de pagina **Fouten opsporen in gegevensbronnen** in het actievenster **Indelingstoewijzing** om de foutopsporing in dit ER-onderdeel voort te zetten.
2. Selecteer de gegevensbron **\$PaymentByDebtor** en selecteer **Alle records lezen**.
3. Vouw **\$PaymentByDebtor** uit.
4. Vouw **\$PaymentByDebtor.Lines** uit en selecteer **Alle records lezen**.
5. Vouw **\$PaymentByDebtor.Lines.CreditorAccount** uit.
6. Vouw **\$PaymentByDebtor.Lines.CreditorAccount.Identification** uit en selecteer **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Selecteer **Waarde ophalen**.
8. Selecteer **Alles uitvouwen**.

    ![Waarde van het IBAN-veld in de indelingstoewijzing](./media/er-data-debugger-debugging-format-mapping.png)

    Zoals u ziet, zijn de gegevensbronnen van de indelingstoewijzing niet verantwoordelijk voor de afgekapte spaties, omdat de geretourneerde IBAN-code voor de bankrekening van de leverancier spaties bevat. Daarom moet u de foutopsporing voor gegevensbronnen voortzetten.

### <a name="debug-the-format"></a>Fouten opsporen in de indeling

1. Selecteer op de pagina **Fouten opsporen in gegevensbronnen** in het actievenster **Indeling** om de foutopsporing in dit ER-onderdeel voort te zetten.
2. Vouw de indelingselementen uit om **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** te selecteren en selecteer vervolgens **Alle records lezen**.
3. Vouw de indelingselementen uit om **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** te selecteren en selecteer vervolgens **Alle records lezen**.
4. Vouw de indelingselementen uit om **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** te selecteren en selecteer vervolgens **Waarde ophalen**.
5. Selecteer **Alles uitvouwen**.

    ![Waarde van het IBAN-veld in de indeling](./media/er-data-debugger-debugging-format.png)

   Zoals u ziet, is de indelingsbinding niet verantwoordelijk voor de afgekapte spaties, omdat de geretourneerde IBAN-code voor de bankrekening van de leverancier spaties bevat. Daarom is het element **BankIBAN** geconfigureerd voor het gebruik van een indelingstransformatie waarmee spaties worden afgekapt.

6. Sluit de foutopsporing voor de gegevensbron.

### <a name="review-the-format-transformations"></a>De indelingstransformaties controleren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** de optie **Betalingsmodel** \> **ISO20022-kredietoverboeking**.
3. Selecteer **Ontwerper** en vouw de elementen uit om **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** te selecteren.

    ![Het element BankIBAN op de pagina Indelingsontwerper](./media/er-data-debugger-referred-transformation.png)

    Zoals u ziet, is het element **BankIBAN** geconfigureerd voor het gebruik van de transformatie **niet-alfanumerieke tekens verwijderen**.

4. Selecteer het tabblad **Transformaties**.

    ![Het tabblad Transformaties voor het element BankIBAN](./media/er-data-debugger-transformation.png)

    Zoals u ziet, is de transformatie **Niet-alfanumerieke tekens verwijderen** geconfigureerd met een expressie waarmee spaties uit de opgegeven tekenreeks worden afgekapt.

## <a name="start-to-debug-in-the-operation-designer"></a>Beginnen met foutopsporing in Operations-ontwerper

Wanneer u een conceptversie van de ER-indeling configureert die rechtstreeks vanuit de Operations-ontwerper kan worden uitgevoerd, krijgt u toegang tot de foutopsporing voor de gegevensbron door **Foutopsporing starten** in het actievenster te selecteren.

![De knop Foutopsporing starten op de pagina Indelingsontwerper](./media/er-data-debugger-run-from-designer.png)

De indelingstoewijzing en indelingsonderdelen van de ER-indeling die wordt bewerkt, zijn beschikbaar voor foutopsporing.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Beginnen met foutopsporing in Ontwerper modeltoewijzing

Wanneer u een ER-modeltoewijzing configureert die rechtstreeks vanuit de pagina **Modeltoewijzing** kan worden uitgevoerd, krijgt u toegang tot de foutopsporing voor de gegevensbron door **Foutopsporing starten** in het actievenster te selecteren.

![De knop Foutopsporing starten op de pagina Modeltoewijzing](./media/er-data-debugger-run-from-designer-mapping.png)

Het onderdeel van de modeltoewijzing in de ER-toewijzing die wordt bewerkt, is beschikbaar voor foutopsporing.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>Bijlage 1: Een ER-oplossing ophalen

### <a name="download-an-er-solution"></a>Een ER-oplossing downloaden

Als u een ER-oplossing wilt gebruiken om een elektronisch betalingsbestand te genereren voor een leveranciersbetaling die wordt verwerkt, kunt u de ER-betalingsindeling **ISO20022-kredietoverboeking** [downloaden](download-electronic-reporting-configuration-lcs.md) die beschikbaar is in de bibliotheek met gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) of in de algemene opslagplaats.

![De ER-betalingsindeling importeren op de pagina Opslagplaats van configuratie](./media/er-data-debugger-import-from-repo.png)

Naast de geselecteerde ER-indeling moeten de volgende [configuraties](general-electronic-reporting.md#Configuration) automatisch worden geïmporteerd in uw Microsoft Dynamics 365 Finance-exemplaar als onderdeel van de ER-oplossing **ISO20022-kredietoverboeking**.

- **Betalingsmodel** [ER-gegevensmodel configureren](general-electronic-reporting.md#DataModelComponent)
- **ISO20022-kredietoverboeking** [ER-indeling configureren](general-electronic-reporting.md#FormatComponentOutbound)
- **Betalingsmodeltoewijzing 1611** [ER-modeltoewijzing configureren](general-electronic-reporting.md#ModelMappingComponent)
- **Betalingsmodeltoewijzing naar bestemming ISO20022** ER-modeltoewijzing configureren

U vindt deze configuraties op de pagina **Configuraties** van het ER-raamwerk (**Organisatiebeheer** \> **Elektronische rapporten** \> **Configuraties**).

![Geïmporteerde configuraties op de pagina Configuraties](./media/er-data-debugger-configurations.png)

Als een van de eerder genoemde configuraties ontbreekt in de configuratiestructuur, moet u deze handmatig downloaden vanuit de bibliotheek LCS gedeelde activa op dezelfde manier als u de indeling van de **ISO20022-kredietoverboeking** hebt gedownload.

### <a name="analyze-the-downloaded-er-solution"></a>De gedownloade ER-oplossing analyseren

#### <a name="review-the-model-mapping"></a>De modeltoewijzing controleren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Betalingsmodel** \> **Toewijzing voor betalingsmodel 1611**.
3. Selecteer **Ontwerper**.
4. Selecteer de toewijzingsrecord **Betalingsmodeltoewijzing ISO20022 CT**.
5. Selecteer **Ontwerper** en bekijk vervolgens de modeltoewijzing die is geopend.

    Het veld **Betalingen** van het gegevensmodel is gebonden aan de gegevensbron **\$notSentTransactions**, die de lijst met de te verwerken betalingsregels van de leverancier terugstuurt.

    ![Het veld Betalingen op de pagina Ontwerper modeltoewijzing](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>De indelingstoewijzing controleren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Betalingsmodel** \> **ISO20022-kredietoverboeking**.
3. Selecteer **Ontwerper**.
4. Controleer op het tabblad **Toewijzing** de indelingstoewijzing die is geopend.

    Het element **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element van de gegevens **ISO20022CTReports** \> **XMLHeader** is gebonden aan de gegevensbron **\$PaymentByDebtor** die is geconfigureerd om records van het veld **Betalingen** van het gegevens model te groeperen.

    ![Het element PmtInf op de pagina Indelingsontwerper](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>De indeling controleren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Betalingsmodel** \> **ISO20022-kredietoverboeking**.
3. Selecteer **Ontwerper** en bekijk vervolgens de indeling die is geopend.

    Het indelingselement onder **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is geconfigureerd om de IBAN-code van de leveranciersrekening in het betalingsbestand in te voeren.

    ![Het element BankIBAN op de pagina Indelingsontwerper](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>Bijlage 2: Leveranciers configureren

### <a name="modify-a-vendor-property"></a>Een leverancierseigenschap wijzigen

1. Ga naar **Leveranciers** \> **Leveranciers** \> **Alle leveranciers**.
2. Selecteer leverancier **DE-01002** en selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Instellen** de optie **Bankrekeningen**.
3. Voer op het sneltabblad **Identificatie** in het veld **IBAN** <a name="enteredIBANcode"></a> **GB33 BUKB 2020 1555 5555 55** in.
4. Selecteer **Opslaan**.

![Veld IBAN ingesteld op de pagina Bankrekeningen leverancier](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Een betalingsmethode instellen

1. Ga naar **Leveranciers** \> **Betalingsinstelling** \> **Betalingsmethoden**.
2. Selecteer de betalingsmethode **SEPA CT**.
3. Stel op het sneltabblad **Bestandsindelingen** in de sectie **Bestandsindelingen** de optie **Algemene elektronische exportindeling** in op **Ja**.
4. Selecteer in het veld **Indelingsconfiguratie exporteren** de ER-indeling **ISO20022-kredietoverboeking**.
5. Selecteer **Opslaan**.

![Instellingen voor Bestandsindelingen op de pagina Betalingsmethoden](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Een leveranciersbetaling toevoegen

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Voeg een nieuw betalingsjournaal toe.
3. Selecteer **Regels** en voeg een nieuwe betalingsregel toe.
4. Selecteer in het veld **Rekening** de leverancier **DE-01002**.
5. Voer een waarde in het veld **Debet** in.
6. Selecteer in het veld **Betalingsmethode** de optie **SEPA CT**.
7. Selecteer **Opslaan**.

![Leveranciersbetaling toegevoegd op de pagina Leveranciersbetalingen](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>Bijlage 3: Een leveranciersbetaling verwerken

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt gemaakt, en selecteer vervolgens **Regels**.
3. Selecteer de betalingsregel en selecteer vervolgens **Betalingsstatus** \> **Geen**.
4. Selecteer **Betalingen genereren**.
5. Selecteer in het veld **Betalingsmethode** de optie **SEPA CT**.
6. Selecteer in het veld **Bankrekening** de optie **DEMF OPER**.
7. Selecteer in het dialoogvenster **Betalingen genereren** de optie **OK**.
8. Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]