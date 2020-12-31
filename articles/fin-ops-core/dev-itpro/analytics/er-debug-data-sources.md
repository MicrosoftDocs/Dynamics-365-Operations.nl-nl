---
title: Fouten opsporen in gegevensbronnen van een uitgevoerde ER-indeling om gegevensstromen en transformatie te analyseren
description: In dit onderwerp wordt uitgelegd hoe u fouten kunt opsporen in de gegevensbronnen van een uitgevoerde ER-indeling om de geconfigureerde gegevensstroom en transformatie beter te begrijpen.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680777"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="70293-103">Fouten opsporen in gegevensbronnen van een uitgevoerde ER-indeling om gegevensstromen en transformatie te analyseren</span><span class="sxs-lookup"><span data-stu-id="70293-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="70293-104">Wanneer u een oplossing voor Elektronische rapportage (ER) [configureert](tasks/er-format-configuration-2016-11.md) om uitgaande documenten te genereren, definieert u de methoden die worden gebruikt om gegevens uit de toepassing te halen en deze in te voeren in de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="70293-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="70293-105">Om de levenscyclusondersteuning van de ER-oplossing efficiënter te maken, moet uw oplossing bestaan uit een ER-[gegevensmodel](general-electronic-reporting.md#DataModelComponent) en de bijbehorende [toewijzings](general-electronic-reporting.md#ModelMappingComponent)componenten, en ook uit een ER-[indeling](general-electronic-reporting.md#FormatComponentOutbound) en toewijzingsonderdelen, zodat de modeltoewijzing toepassingsspecifiek is terwijl andere componenten toepassingsonafhankelijk blijven.</span><span class="sxs-lookup"><span data-stu-id="70293-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="70293-106">Dit betekent dat verschillende ER-onderdelen [van invloed zijn op](general-electronic-reporting.md#FormatComponentOutbound) het invoerproces van gegevens in de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="70293-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="70293-107">Soms zien de gegevens van de gegenereerde uitvoer er anders uit dan dezelfde gegevens in de toepassingsdatabase.</span><span class="sxs-lookup"><span data-stu-id="70293-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="70293-108">In deze gevallen moet u bepalen welk ER-onderdeel verantwoordelijk is voor de gegevenstransformatie.</span><span class="sxs-lookup"><span data-stu-id="70293-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="70293-109">De functie voor het oplossen van fouten in ER-gegevensbronnen vermindert de tijd en kosten die bij dit onderzoek zijn betrokken.</span><span class="sxs-lookup"><span data-stu-id="70293-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="70293-110">U kunt de uitvoering van een ER-indeling onderbreken en de interface van het foutopsporingsprogramma voor gegevensbronnen openen.</span><span class="sxs-lookup"><span data-stu-id="70293-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="70293-111">Daar kunt u bladeren in de beschikbare gegevensbronnen en een afzonderlijke gegevensbron selecteren voor uitvoering.</span><span class="sxs-lookup"><span data-stu-id="70293-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="70293-112">Deze handmatige uitvoering simuleert de uitvoering van de gegevensbron tijdens de echte uitvoering van een ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="70293-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="70293-113">Het resultaat wordt weergegeven op een pagina waar u de ontvangen gegevens kunt analyseren.</span><span class="sxs-lookup"><span data-stu-id="70293-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="70293-114">Als u de functie voor foutopsporing in gegevensbronnen wilt inschakelen, stelt u de optie **Foutopsporing in gegevens bij indelingsuitvoering inschakelen** in op **Ja** in de ER-gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="70293-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="70293-115">U kunt vervolgens foutopsporing starten in de gegevensbron terwijl u een ER-indeling uitvoert om uitgaande documenten te genereren.</span><span class="sxs-lookup"><span data-stu-id="70293-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="70293-116">U kunt ook de optie **Foutopsporing starten** gebruiken om foutopsporing in de gegevensbron te starten voor een ER-indeling die is geconfigureerd in de [ER Operations-ontwerper](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="70293-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="70293-117">Dit onderwerp bevat richtlijnen voor het starten van foutopsporing in gegevensbronnen voor uitgevoerde ER-indelingen.</span><span class="sxs-lookup"><span data-stu-id="70293-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="70293-118">Het geeft uitleg over de informatie die u kan helpen bij het begrijpen van de gegevensstroom en gegevenstransformaties.</span><span class="sxs-lookup"><span data-stu-id="70293-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="70293-119">De voorbeelden in dit onderwerp gebruiken het bedrijfsproces voor het verwerken van leveranciersbetalingen.</span><span class="sxs-lookup"><span data-stu-id="70293-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="70293-120">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="70293-120">Limitations</span></span>

<span data-ttu-id="70293-121">U kunt de foutopsporing voor gegevensbronnen gebruiken om toegang te krijgen tot gegevensbronnen die worden gebruikt in ER-indelingen voor het genereren van uitgaande documenten.</span><span class="sxs-lookup"><span data-stu-id="70293-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="70293-122">U kunt geen fouten oplossen in gegevensbronnen met ER-indelingen die zijn ontworpen om inkomende documenten te parseren.</span><span class="sxs-lookup"><span data-stu-id="70293-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="70293-123">De volgende instellingen voor ER-indelingen zijn op dit moment niet toegankelijk voor foutopsporing in gegevensbronnen:</span><span class="sxs-lookup"><span data-stu-id="70293-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="70293-124">Indelingen van transformaties</span><span class="sxs-lookup"><span data-stu-id="70293-124">Format transformations</span></span>
- <span data-ttu-id="70293-125">Indeling en toewijzing van validatieregels</span><span class="sxs-lookup"><span data-stu-id="70293-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="70293-126">Expressies inschakelen</span><span class="sxs-lookup"><span data-stu-id="70293-126">Enabling expressions</span></span>
- <span data-ttu-id="70293-127">Details van gegevensverzameling in het geheugen</span><span class="sxs-lookup"><span data-stu-id="70293-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="70293-128">Vereisten</span><span class="sxs-lookup"><span data-stu-id="70293-128">Prerequisites</span></span>

- <span data-ttu-id="70293-129">Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot een van de volgende [rollen](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="70293-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="70293-130">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="70293-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="70293-131">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="70293-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="70293-132">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="70293-132">System administrator</span></span>

- <span data-ttu-id="70293-133">Het bedrijf moet worden ingesteld op **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="70293-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="70293-134">Volg de stappen in [bijlage 1](#appendix1) van dit onderwerp om de onderdelen van de Microsoft ER-oplossing te downloaden die vereist zijn om leveranciersbetalingen te verwerken.</span><span class="sxs-lookup"><span data-stu-id="70293-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="70293-135">Volg de stappen in [bijlage 2](#appendix2) van dit onderwerp om Leveranciers voor te bereiden voor de verwerking van leveranciersbetalingen met de gedownloade ER-oplossing.</span><span class="sxs-lookup"><span data-stu-id="70293-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="70293-136">Een leveranciersbetaling verwerken om een betalingsbestand op te halen</span><span class="sxs-lookup"><span data-stu-id="70293-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="70293-137">Volg de stappen in [bijlage 3](#appendix3) van dit onderwerp om leveranciersbetalingen te verwerken.</span><span class="sxs-lookup"><span data-stu-id="70293-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Verwerking van leveranciersbetalingen wordt uitgevoerd](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="70293-139">Download het zipbestand en sla het op op uw lokale computer.</span><span class="sxs-lookup"><span data-stu-id="70293-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="70293-140">Pak het betalingsbestand **ISO20022 Credit transfer.xml** in het zipbestand uit.</span><span class="sxs-lookup"><span data-stu-id="70293-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="70293-141">Open het uitgepakte betalingsbestand met de XML-bestandsviewer.</span><span class="sxs-lookup"><span data-stu-id="70293-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="70293-142">De IBAN-code (International Bank Account Number) van de bankrekening van de leverancier bevat geen spaties.</span><span class="sxs-lookup"><span data-stu-id="70293-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="70293-143">Dit wijkt af van de waarde die is [ingevoerd](#enteredIBANcode) op de pagina **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="70293-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN-code zonder spaties](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="70293-145">U kunt het foutopsporingsprogramma voor ER-gegevensbronnen gebruiken om te achterhalen door welk onderdeel van de ER-oplossing spaties in de IBAN-code worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="70293-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="70293-146">Foutopsporing in gegevensbronnen inschakelen</span><span class="sxs-lookup"><span data-stu-id="70293-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="70293-147">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="70293-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="70293-148">Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="70293-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="70293-149">Stel de optie **Foutopsporing in gegevens bij indelingsuitvoering inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="70293-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="70293-150">Deze parameter specifiek is voor de gebruiker en het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="70293-150">This parameter is user-specific and company-specific.</span></span>

    ![Dialoogvenster voor gebruikersparameters](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="70293-152">Een leveranciersbetaling verwerken voor foutopsporing</span><span class="sxs-lookup"><span data-stu-id="70293-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="70293-153">Volg de stappen in [bijlage 3](#appendix3) van dit onderwerp om leveranciersbetalingen te verwerken.</span><span class="sxs-lookup"><span data-stu-id="70293-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="70293-154">Selecteer **Ja** in het berichtvak om te bevestigen dat u de verwerking van leveranciersbetalingen wilt onderbreken en in plaats daarvan foutopsporing in de gegevensbron wilt starten op de pagina **Fouten opsporen in gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="70293-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Venster met bevestigingsbericht](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="70293-156">Fouten opsporen in gegevensbronnen die worden gebruikt bij betalingsverwerking</span><span class="sxs-lookup"><span data-stu-id="70293-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="70293-157">Foutopsporing uitvoeren in de modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="70293-157">Debug the model mapping</span></span>

1. <span data-ttu-id="70293-158">Selecteer op de pagina **Fouten opsporen in gegevensbronnen** in het actievenster **Modeltoewijzing** om de foutopsporing in dit ER-onderdeel te starten.</span><span class="sxs-lookup"><span data-stu-id="70293-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="70293-159">Selecteer in het deelvenster met de gegevensbron aan de linkerkant de gegevensbron **\$notSentTransactions** en selecteer **Alle records lezen**.</span><span class="sxs-lookup"><span data-stu-id="70293-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="70293-160">U kunt de opties **1 record lezen**, **10 records lezen**, **100 records lezen** of **Alle records lezen** kiezen om te bepalen hoeveel records moeten worden gelezen van de geselecteerde gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="70293-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="70293-161">Op deze manier kunt u de toegang tot de gegevensbron simuleren vanuit de actieve ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="70293-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="70293-162">Selecteer in het gegevensvenster aan de rechterkant de optie **Alles uitvouwen**.</span><span class="sxs-lookup"><span data-stu-id="70293-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="70293-163">U ziet dat de geselecteerde gegevensbron van het type **Recordlijst** één record bevat.</span><span class="sxs-lookup"><span data-stu-id="70293-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="70293-164">Vouw de gegevensbron **\$notSentTransactions** uit en selecteer de geneste methode **vendBankAccountInTransactionCompany()**.</span><span class="sxs-lookup"><span data-stu-id="70293-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="70293-165">Vouw de methode **vendBankAccountInTransactionCompany()** uit en selecteer het geneste veld **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="70293-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="70293-166">Selecteer **Waarde ophalen**.</span><span class="sxs-lookup"><span data-stu-id="70293-166">Select **Get value**.</span></span>

    <span data-ttu-id="70293-167">U kunt **Waarde ophalen** selecteren om de waarde van een geselecteerd veld van de geselecteerde gegevensbron te laten lezen.</span><span class="sxs-lookup"><span data-stu-id="70293-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="70293-168">Op deze manier kunt u de toegang tot dit veld simuleren vanuit de actieve ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="70293-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="70293-169">Selecteer **Alles uitvouwen**.</span><span class="sxs-lookup"><span data-stu-id="70293-169">Select **Expand all**.</span></span>

    ![Waarde van het IBAN-veld in de modeltoewijzing](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="70293-171">Zoals u ziet, is de modeltoewijzing niet verantwoordelijk voor de afgekapte spaties, omdat de geretourneerde IBAN-code voor de bankrekening van de leverancier spaties bevat.</span><span class="sxs-lookup"><span data-stu-id="70293-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="70293-172">Daarom moet u de foutopsporing voor gegevensbronnen voortzetten.</span><span class="sxs-lookup"><span data-stu-id="70293-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="70293-173">Fouten opsporen in de indelingstoewijzing</span><span class="sxs-lookup"><span data-stu-id="70293-173">Debug the format mapping</span></span>

1. <span data-ttu-id="70293-174">Selecteer op de pagina **Fouten opsporen in gegevensbronnen** in het actievenster **Indelingstoewijzing** om de foutopsporing in dit ER-onderdeel voort te zetten.</span><span class="sxs-lookup"><span data-stu-id="70293-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="70293-175">Selecteer de gegevensbron **\$PaymentByDebtor** en selecteer **Alle records lezen**.</span><span class="sxs-lookup"><span data-stu-id="70293-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="70293-176">Vouw **\$PaymentByDebtor** uit.</span><span class="sxs-lookup"><span data-stu-id="70293-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="70293-177">Vouw **\$PaymentByDebtor.Lines** uit en selecteer **Alle records lezen**.</span><span class="sxs-lookup"><span data-stu-id="70293-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="70293-178">Vouw **\$PaymentByDebtor.Lines.CreditorAccount** uit.</span><span class="sxs-lookup"><span data-stu-id="70293-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="70293-179">Vouw **\$PaymentByDebtor.Lines.CreditorAccount.Identification** uit en selecteer **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="70293-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="70293-180">Selecteer **Waarde ophalen**.</span><span class="sxs-lookup"><span data-stu-id="70293-180">Select **Get value**.</span></span>
8. <span data-ttu-id="70293-181">Selecteer **Alles uitvouwen**.</span><span class="sxs-lookup"><span data-stu-id="70293-181">Select **Expand all**.</span></span>

    ![Waarde van het IBAN-veld in de indelingstoewijzing](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="70293-183">Zoals u ziet, zijn de gegevensbronnen van de indelingstoewijzing niet verantwoordelijk voor de afgekapte spaties, omdat de geretourneerde IBAN-code voor de bankrekening van de leverancier spaties bevat.</span><span class="sxs-lookup"><span data-stu-id="70293-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="70293-184">Daarom moet u de foutopsporing voor gegevensbronnen voortzetten.</span><span class="sxs-lookup"><span data-stu-id="70293-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="70293-185">Fouten opsporen in de indeling</span><span class="sxs-lookup"><span data-stu-id="70293-185">Debug the format</span></span>

1. <span data-ttu-id="70293-186">Selecteer op de pagina **Fouten opsporen in gegevensbronnen** in het actievenster **Indeling** om de foutopsporing in dit ER-onderdeel voort te zetten.</span><span class="sxs-lookup"><span data-stu-id="70293-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="70293-187">Vouw de indelingselementen uit om **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** te selecteren en selecteer vervolgens **Alle records lezen**.</span><span class="sxs-lookup"><span data-stu-id="70293-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="70293-188">Vouw de indelingselementen uit om **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** te selecteren en selecteer vervolgens **Alle records lezen**.</span><span class="sxs-lookup"><span data-stu-id="70293-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="70293-189">Vouw de indelingselementen uit om **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** te selecteren en selecteer vervolgens **Waarde ophalen**.</span><span class="sxs-lookup"><span data-stu-id="70293-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="70293-190">Selecteer **Alles uitvouwen**.</span><span class="sxs-lookup"><span data-stu-id="70293-190">Select **Expand all**.</span></span>

    ![Waarde van het IBAN-veld in de indeling](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="70293-192">Zoals u ziet, is de indelingsbinding niet verantwoordelijk voor de afgekapte spaties, omdat de geretourneerde IBAN-code voor de bankrekening van de leverancier spaties bevat.</span><span class="sxs-lookup"><span data-stu-id="70293-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="70293-193">Daarom is het element **BankIBAN** geconfigureerd voor het gebruik van een indelingstransformatie waarmee spaties worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="70293-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="70293-194">Sluit de foutopsporing voor de gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="70293-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="70293-195">De indelingstransformaties controleren</span><span class="sxs-lookup"><span data-stu-id="70293-195">Review the format transformations</span></span>

1. <span data-ttu-id="70293-196">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="70293-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="70293-197">Selecteer op de pagina **Configuraties** de optie **Betalingsmodel** \> **ISO20022-kredietoverboeking**.</span><span class="sxs-lookup"><span data-stu-id="70293-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="70293-198">Selecteer **Ontwerper** en vouw de elementen uit om **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="70293-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![Het element BankIBAN op de pagina Indelingsontwerper](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="70293-200">Zoals u ziet, is het element **BankIBAN** geconfigureerd voor het gebruik van de transformatie **niet-alfanumerieke tekens verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="70293-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="70293-201">Selecteer het tabblad **Transformaties**.</span><span class="sxs-lookup"><span data-stu-id="70293-201">Select the **Transformations** tab.</span></span>

    ![Het tabblad Transformaties voor het element BankIBAN](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="70293-203">Zoals u ziet, is de transformatie **Niet-alfanumerieke tekens verwijderen** geconfigureerd met een expressie waarmee spaties uit de opgegeven tekenreeks worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="70293-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="70293-204">Beginnen met foutopsporing in Operations-ontwerper</span><span class="sxs-lookup"><span data-stu-id="70293-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="70293-205">Wanneer u een conceptversie van de ER-indeling configureert die rechtstreeks vanuit de Operations-ontwerper kan worden uitgevoerd, krijgt u toegang tot de foutopsporing voor de gegevensbron door **Foutopsporing starten** in het actievenster te selecteren.</span><span class="sxs-lookup"><span data-stu-id="70293-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![De knop Foutopsporing starten op de pagina Indelingsontwerper](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="70293-207">De indelingstoewijzing en indelingsonderdelen van de ER-indeling die wordt bewerkt, zijn beschikbaar voor foutopsporing.</span><span class="sxs-lookup"><span data-stu-id="70293-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="70293-208">Beginnen met foutopsporing in Ontwerper modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="70293-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="70293-209">Wanneer u een ER-modeltoewijzing configureert die rechtstreeks vanuit de pagina **Modeltoewijzing** kan worden uitgevoerd, krijgt u toegang tot de foutopsporing voor de gegevensbron door **Foutopsporing starten** in het actievenster te selecteren.</span><span class="sxs-lookup"><span data-stu-id="70293-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![De knop Foutopsporing starten op de pagina Modeltoewijzing](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="70293-211">Het onderdeel van de modeltoewijzing in de ER-toewijzing die wordt bewerkt, is beschikbaar voor foutopsporing.</span><span class="sxs-lookup"><span data-stu-id="70293-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="70293-212">Bijlage 1: Een ER-oplossing ophalen</span><span class="sxs-lookup"><span data-stu-id="70293-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="70293-213">Een ER-oplossing downloaden</span><span class="sxs-lookup"><span data-stu-id="70293-213">Download an ER solution</span></span>

<span data-ttu-id="70293-214">Als u een ER-oplossing wilt gebruiken om een elektronisch betalingsbestand te genereren voor een leveranciersbetaling die wordt verwerkt, kunt u de ER-betalingsindeling **ISO20022-kredietoverboeking** [downloaden](download-electronic-reporting-configuration-lcs.md) die beschikbaar is in de bibliotheek met gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) of in de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="70293-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![De ER-betalingsindeling importeren op de pagina Opslagplaats van configuratie](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="70293-216">Naast de geselecteerde ER-indeling moeten de volgende [configuraties](general-electronic-reporting.md#Configuration) automatisch worden geïmporteerd in uw Microsoft Dynamics 365 Finance-exemplaar als onderdeel van de ER-oplossing **ISO20022-kredietoverboeking**.</span><span class="sxs-lookup"><span data-stu-id="70293-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="70293-217">**Betalingsmodel** [ER-gegevensmodel configureren](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="70293-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="70293-218">**ISO20022-kredietoverboeking** [ER-indeling configureren](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="70293-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="70293-219">**Betalingsmodeltoewijzing 1611** [ER-modeltoewijzing configureren](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="70293-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="70293-220">**Betalingsmodeltoewijzing naar bestemming ISO20022** ER-modeltoewijzing configureren</span><span class="sxs-lookup"><span data-stu-id="70293-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="70293-221">U vindt deze configuraties op de pagina **Configuraties** van het ER-raamwerk (**Organisatiebeheer** \> **Elektronische rapporten** \> **Configuraties**).</span><span class="sxs-lookup"><span data-stu-id="70293-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Geïmporteerde configuraties op de pagina Configuraties](./media/er-data-debugger-configurations.png)

<span data-ttu-id="70293-223">Als een van de eerder genoemde configuraties ontbreekt in de configuratiestructuur, moet u deze handmatig downloaden vanuit de bibliotheek LCS gedeelde activa op dezelfde manier als u de indeling van de **ISO20022-kredietoverboeking** hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="70293-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="70293-224">De gedownloade ER-oplossing analyseren</span><span class="sxs-lookup"><span data-stu-id="70293-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="70293-225">De modeltoewijzing controleren</span><span class="sxs-lookup"><span data-stu-id="70293-225">Review the model mapping</span></span>

1. <span data-ttu-id="70293-226">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="70293-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="70293-227">Selecteer **Betalingsmodel** \> **Toewijzing voor betalingsmodel 1611**.</span><span class="sxs-lookup"><span data-stu-id="70293-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="70293-228">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="70293-228">Select **Designer**.</span></span>
4. <span data-ttu-id="70293-229">Selecteer de toewijzingsrecord **Betalingsmodeltoewijzing ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="70293-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="70293-230">Selecteer **Ontwerper** en bekijk vervolgens de modeltoewijzing die is geopend.</span><span class="sxs-lookup"><span data-stu-id="70293-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="70293-231">Het veld **Betalingen** van het gegevensmodel is gebonden aan de gegevensbron **\$notSentTransactions**, die de lijst met de te verwerken betalingsregels van de leverancier terugstuurt.</span><span class="sxs-lookup"><span data-stu-id="70293-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Het veld Betalingen op de pagina Ontwerper modeltoewijzing](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="70293-233">De indelingstoewijzing controleren</span><span class="sxs-lookup"><span data-stu-id="70293-233">Review the format mapping</span></span>

1. <span data-ttu-id="70293-234">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="70293-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="70293-235">Selecteer **Betalingsmodel** \> **ISO20022-kredietoverboeking**.</span><span class="sxs-lookup"><span data-stu-id="70293-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="70293-236">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="70293-236">Select **Designer**.</span></span>
4. <span data-ttu-id="70293-237">Controleer op het tabblad **Toewijzing** de indelingstoewijzing die is geopend.</span><span class="sxs-lookup"><span data-stu-id="70293-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="70293-238">Het element **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element van de gegevens **ISO20022CTReports** \> **XMLHeader** is gebonden aan de gegevensbron **\$PaymentByDebtor** die is geconfigureerd om records van het veld **Betalingen** van het gegevens model te groeperen.</span><span class="sxs-lookup"><span data-stu-id="70293-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![Het element PmtInf op de pagina Indelingsontwerper](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="70293-240">De indeling controleren</span><span class="sxs-lookup"><span data-stu-id="70293-240">Review the format</span></span>

1. <span data-ttu-id="70293-241">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="70293-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="70293-242">Selecteer **Betalingsmodel** \> **ISO20022-kredietoverboeking**.</span><span class="sxs-lookup"><span data-stu-id="70293-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="70293-243">Selecteer **Ontwerper** en bekijk vervolgens de indeling die is geopend.</span><span class="sxs-lookup"><span data-stu-id="70293-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="70293-244">Het indelingselement onder **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is geconfigureerd om de IBAN-code van de leveranciersrekening in het betalingsbestand in te voeren.</span><span class="sxs-lookup"><span data-stu-id="70293-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![Het element BankIBAN op de pagina Indelingsontwerper](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="70293-246">Bijlage 2: Leveranciers configureren</span><span class="sxs-lookup"><span data-stu-id="70293-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="70293-247">Een leverancierseigenschap wijzigen</span><span class="sxs-lookup"><span data-stu-id="70293-247">Modify a vendor property</span></span>

1. <span data-ttu-id="70293-248">Ga naar **Leveranciers** \> **Leveranciers** \> **Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="70293-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="70293-249">Selecteer leverancier **DE-01002** en selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Instellen** de optie **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="70293-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="70293-250">Voer op het sneltabblad **Identificatie** in het veld **IBAN** <a name="enteredIBANcode"></a> **GB33 BUKB 2020 1555 5555 55** in.</span><span class="sxs-lookup"><span data-stu-id="70293-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="70293-251">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="70293-251">Select **Save**.</span></span>

![Veld IBAN ingesteld op de pagina Bankrekeningen leverancier](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="70293-253">Een betalingsmethode instellen</span><span class="sxs-lookup"><span data-stu-id="70293-253">Set up a method of payment</span></span>

1. <span data-ttu-id="70293-254">Ga naar **Leveranciers** \> **Betalingsinstelling** \> **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="70293-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="70293-255">Selecteer de betalingsmethode **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="70293-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="70293-256">Stel op het sneltabblad **Bestandsindelingen** in de sectie **Bestandsindelingen** de optie **Algemene elektronische exportindeling** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="70293-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="70293-257">Selecteer in het veld **Indelingsconfiguratie exporteren** de ER-indeling **ISO20022-kredietoverboeking**.</span><span class="sxs-lookup"><span data-stu-id="70293-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="70293-258">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="70293-258">Select **Save**.</span></span>

![Instellingen voor Bestandsindelingen op de pagina Betalingsmethoden](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="70293-260">Een leveranciersbetaling toevoegen</span><span class="sxs-lookup"><span data-stu-id="70293-260">Add a vendor payment</span></span>

1. <span data-ttu-id="70293-261">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="70293-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="70293-262">Voeg een nieuw betalingsjournaal toe.</span><span class="sxs-lookup"><span data-stu-id="70293-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="70293-263">Selecteer **Regels** en voeg een nieuwe betalingsregel toe.</span><span class="sxs-lookup"><span data-stu-id="70293-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="70293-264">Selecteer in het veld **Rekening** de leverancier **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="70293-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="70293-265">Voer een waarde in het veld **Debet** in.</span><span class="sxs-lookup"><span data-stu-id="70293-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="70293-266">Selecteer in het veld **Betalingsmethode** de optie **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="70293-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="70293-267">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="70293-267">Select **Save**.</span></span>

![Leveranciersbetaling toegevoegd op de pagina Leveranciersbetalingen](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="70293-269">Bijlage 3: Een leveranciersbetaling verwerken</span><span class="sxs-lookup"><span data-stu-id="70293-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="70293-270">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="70293-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="70293-271">Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt gemaakt, en selecteer vervolgens **Regels**.</span><span class="sxs-lookup"><span data-stu-id="70293-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="70293-272">Selecteer de betalingsregel en selecteer vervolgens **Betalingsstatus** \> **Geen**.</span><span class="sxs-lookup"><span data-stu-id="70293-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="70293-273">Selecteer **Betalingen genereren**.</span><span class="sxs-lookup"><span data-stu-id="70293-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="70293-274">Selecteer in het veld **Betalingsmethode** de optie **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="70293-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="70293-275">Selecteer in het veld **Bankrekening** de optie **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="70293-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="70293-276">Selecteer in het dialoogvenster **Betalingen genereren** de optie **OK**.</span><span class="sxs-lookup"><span data-stu-id="70293-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="70293-277">Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport**.</span><span class="sxs-lookup"><span data-stu-id="70293-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
