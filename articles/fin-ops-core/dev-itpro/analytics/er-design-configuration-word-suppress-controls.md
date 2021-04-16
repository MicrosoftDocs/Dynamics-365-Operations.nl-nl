---
title: Besturingselementen voor Word-inhoud onderdrukken in gegenereerde rapporten
description: In dit onderwerp wordt uitgelegd hoe u een ER-indeling (elektronische rapportage) configureert om rapporten te genereren als Microsoft Word-bestanden waarin inhoudsbesturingselementen worden onderdrukt.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753595"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="881ed-103">Besturingselementen voor Word-inhoud onderdrukken in gegenereerde rapporten</span><span class="sxs-lookup"><span data-stu-id="881ed-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="881ed-104">Als u rapporten wilt genereren als Microsoft Word-documenten, moet u een sjabloon voor de rapporten ontwerpen als een Word-document.</span><span class="sxs-lookup"><span data-stu-id="881ed-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="881ed-105">Deze sjabloon moet besturingselementen voor Word-inhoud bevatten als tijdelijke aanduidingen voor gegevens die tijdens runtime worden ingevuld.</span><span class="sxs-lookup"><span data-stu-id="881ed-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="881ed-106">Als u het Word-document wilt gebruiken is gemaakt als sjabloon voor uw rapporten, kunt u een nieuwe [ER (elektronische rapportage)](general-electronic-reporting.md)-[oplossing](er-quick-start1-new-solution.md) [configureren](er-design-configuration-word.md).</span><span class="sxs-lookup"><span data-stu-id="881ed-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="881ed-107">De oplossing moet een ER-[configuratie](general-electronic-reporting.md#Configuration) bevatten die een onderdeel voor [ER-indeling](general-electronic-reporting.md#FormatComponentOutbound) bevat.</span><span class="sxs-lookup"><span data-stu-id="881ed-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="881ed-108">Deze ER-indeling moet worden geconfigureerd om de ontworpen sjabloon te gebruiken voor het genereren van een rapport.</span><span class="sxs-lookup"><span data-stu-id="881ed-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="881ed-109">In versie 10.0.6 en hoger van Dynamics 365 Finance kunt u formules configureren in de ER-indeling om bepaalde besturingselementen voor Word-inhoud in gegenereerde documenten te onderdrukken.</span><span class="sxs-lookup"><span data-stu-id="881ed-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="881ed-110">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol Systeembeheerder of Functioneel consultant elektronische rapportage een ER-indeling kan configureren die rapporten genereert als Word-bestanden en enkele van de inhoudsbesturingselementen onderdrukt in de gegenereerde rapporten die zijn geconfigureerd met behulp van een Word-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="881ed-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="881ed-111">Deze stappen kunnen in het GBSI-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="881ed-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="881ed-112">Vereisten</span><span class="sxs-lookup"><span data-stu-id="881ed-112">Prerequisites</span></span>

<span data-ttu-id="881ed-113">Voordat u deze stappen uitvoert, moet u eerst de stappen in de volgende taakbegeleidingen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="881ed-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="881ed-114">Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling</span><span class="sxs-lookup"><span data-stu-id="881ed-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="881ed-115">ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling</span><span class="sxs-lookup"><span data-stu-id="881ed-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="881ed-116">Wanneer u de stappen van deze taakhandleidingen voltooit, worden de volgende items voorbereid:</span><span class="sxs-lookup"><span data-stu-id="881ed-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="881ed-117">Een ER-indeling voor een **voorbeeldwerkbladrapport** dat is geconfigureerd om een document te genereren in Word-indeling</span><span class="sxs-lookup"><span data-stu-id="881ed-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="881ed-118">Een [conceptversie](general-electronic-reporting.md#component-versioning) van de ER-indeling voor een **voorbeeldwerkbladrapport** dat is gemarkeerd als **Uitvoerbaar**</span><span class="sxs-lookup"><span data-stu-id="881ed-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="881ed-119">Een **elektronische** betalingsmethode die is geconfigureerd voor het gebruik van de ER-indeling voor een **voorbeeldwerkbladrapport** voor de verwerking van leverancierbetalingen</span><span class="sxs-lookup"><span data-stu-id="881ed-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="881ed-120">U moet ook de volgende sjabloon downloaden en opslaan voor het voorbeeldrapport:</span><span class="sxs-lookup"><span data-stu-id="881ed-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="881ed-121">Gebonden sjabloon 2 van betalingsrapport (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="881ed-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="881ed-122">De gedownloade Word-sjabloon controleren</span><span class="sxs-lookup"><span data-stu-id="881ed-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="881ed-123">Open in de Word-bureaubladtoepassing het sjabloonbestand **SampleVendPaymDocReportBounded2.docx** dat u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="881ed-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="881ed-124">Controleer of het sjabloonbestand een overzichtssectie bevat met de totale betalingsbedragen voor elke valutacode die in de verwerkte betalingen is gehanteerd.</span><span class="sxs-lookup"><span data-stu-id="881ed-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="881ed-125">De overzichtssectie bevindt zich in een afzonderlijke tabel van het Word-document.</span><span class="sxs-lookup"><span data-stu-id="881ed-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="881ed-126">De eerste rij in deze tabel bevat de kopteksten van de tabelkolommen als sectiekoptekst.</span><span class="sxs-lookup"><span data-stu-id="881ed-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="881ed-127">De tweede rij van deze tabel bevat de terugkerende inhoudsbesturingselementen als de sectiedetails.</span><span class="sxs-lookup"><span data-stu-id="881ed-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="881ed-128">Dit inhoudsbesturingselement wordt toegewezen aan het veld **SummaryLines** van het aangepaste XML-onderdeel **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="881ed-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="881ed-129">Op basis van deze toewijzing is het inhoudsbesturingselement gekoppeld aan het element **SummaryLines** van de bewerkbare ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="881ed-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="881ed-130">Het besturingselement voor terugkerende inhoud wordt gelabeld door de sleutel **SummaryLines** die overeenkomt met het veld van het aangepaste XML-onderdeel waaraan het is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="881ed-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Indeling van Word-sjabloon](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="881ed-132">De bestaande ER-rapportconfiguratie selecteren</span><span class="sxs-lookup"><span data-stu-id="881ed-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="881ed-133">Voor de volgende stappen gebruikt u de bestaande ER-configuratie die u hebt geconfigureerd bij het uitvoeren van de stappen in de eerder genoemde taakbegeleidingen.</span><span class="sxs-lookup"><span data-stu-id="881ed-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="881ed-134">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="881ed-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="881ed-135">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="881ed-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="881ed-136">Vouw op de pagina **Configuraties** in de configuratiestructuur **Betalingsmodel** uit en selecteer **Voorbeeldwerkbladrapport**.</span><span class="sxs-lookup"><span data-stu-id="881ed-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="881ed-137">Selecteer **Ontwerper** om de conceptversie van de geselecteerde ER-indeling te bewerken.</span><span class="sxs-lookup"><span data-stu-id="881ed-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="881ed-138">De huidige sjabloon vervangen door de nieuwe sjabloon</span><span class="sxs-lookup"><span data-stu-id="881ed-138">Replace the current template with the new template</span></span>

<span data-ttu-id="881ed-139">Momenteel wordt het bestand SampleVendPaymDocReportBounded.docx gebruikt als sjabloon voor het genereren van de uitvoer in Word-indeling.</span><span class="sxs-lookup"><span data-stu-id="881ed-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="881ed-140">In de volgende stappen vervangt deze Word=sjabloon door de nieuwe Word-sjabloon, SampleVendPaymDocReportBounded2.docx, die u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="881ed-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="881ed-141">Selecteer **Bijlagen** op de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="881ed-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="881ed-142">Selecteer op de pagina **Bijlagen** de optie **Verwijderen** om de bestaande sjabloon te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="881ed-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="881ed-143">Selecteer **Ja** om de verwijdering te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="881ed-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="881ed-144">Selecteer **Nieuw** \> **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="881ed-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="881ed-145">Selecteer **Bladeren**, blader vervolgens naar het bestand **SampleVendPaymDocReportBounded2.docx** dat u eerder hebt gedownload en selecteer dit.</span><span class="sxs-lookup"><span data-stu-id="881ed-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="881ed-146">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="881ed-146">Select **OK**.</span></span>
7. <span data-ttu-id="881ed-147">Sluit de pagina **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="881ed-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="881ed-148">Typ of selecteer op de pagina **Indelingsontwerper** in het veld **Sjabloon** het bestand **SampleVendPaymDocReportBounded2.docx**.</span><span class="sxs-lookup"><span data-stu-id="881ed-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="881ed-149">De indeling uitvoeren om Word-uitvoer te maken</span><span class="sxs-lookup"><span data-stu-id="881ed-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="881ed-150">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="881ed-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="881ed-151">Selecteer alle betalingen op de pagina **Leverancierbetalingen** op het tabblad **Lijst**.</span><span class="sxs-lookup"><span data-stu-id="881ed-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="881ed-152">Selecteer **Betalingsstatus** \> **Geen**.</span><span class="sxs-lookup"><span data-stu-id="881ed-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="881ed-153">Selecteer **Betalingen genereren**.</span><span class="sxs-lookup"><span data-stu-id="881ed-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="881ed-154">Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.</span><span class="sxs-lookup"><span data-stu-id="881ed-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="881ed-155">Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="881ed-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="881ed-156">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="881ed-156">Select **OK**.</span></span>
8. <span data-ttu-id="881ed-157">Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport** en analyseer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="881ed-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Betalingen voor verwerking op de pagina Leveranciersbetalingen](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="881ed-159">De uitvoer wordt weergegeven in Word-indeling en bevat de overzichtssectie.</span><span class="sxs-lookup"><span data-stu-id="881ed-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="881ed-160">De bewerkbare indeling configureren om de overzichtssectie te onderdrukken</span><span class="sxs-lookup"><span data-stu-id="881ed-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="881ed-161">Als u de overzichtssectie in een gegenereerd document wilt onderdrukken op basis van de aanvraag van een gebruiker die deze ER-indeling gebruikt, moet u de bewerkbare ER-indeling wijzigen.</span><span class="sxs-lookup"><span data-stu-id="881ed-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="881ed-162">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage** en open de conceptversie van de ER-indeling die u wilt bewerken.</span><span class="sxs-lookup"><span data-stu-id="881ed-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="881ed-163">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="881ed-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="881ed-164">Vouw op de pagina **Configuraties** in de configuratiestructuur **Betalingsmodel** \> **Voorbeeldwerkbladrapport** uit.</span><span class="sxs-lookup"><span data-stu-id="881ed-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="881ed-165">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="881ed-165">Select **Designer**.</span></span>
5. <span data-ttu-id="881ed-166">Vouw op de pagina **Indelingsontwerper** **Word** uit en selecteer **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="881ed-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="881ed-167">Voeg op het tabblad **Toewijzing** een nieuwe gegevensbron toe om de gebruiker tijdens runtime te vragen of de overzichtssectie moet worden onderdrukt:</span><span class="sxs-lookup"><span data-stu-id="881ed-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="881ed-168">Selecteer **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="881ed-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="881ed-169">Selecteer in het dialoogvenster **Gegevensbron toevoegen** de optie **Algemeen\gebruikersinvoerparameter** om het dialoogvenster **Gegevensbroneigenschappen 'gebruikersinvoerparameter'** te openen.</span><span class="sxs-lookup"><span data-stu-id="881ed-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="881ed-170">Voer in het veld **Naam** de tekst **uipSuppress** in.</span><span class="sxs-lookup"><span data-stu-id="881ed-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="881ed-171">Geef in het veld **Label** de optie **Overzichtssectie onderdrukken** op.</span><span class="sxs-lookup"><span data-stu-id="881ed-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="881ed-172">Selecteer of typ **NoYes** in het veld **Naam van gegevenstype voor bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="881ed-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="881ed-173">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="881ed-173">Select **OK**.</span></span>

7. <span data-ttu-id="881ed-174">Voeg een nieuwe gegevensbron toe van het opsommingstype **NoYes**:</span><span class="sxs-lookup"><span data-stu-id="881ed-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="881ed-175">Selecteer **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="881ed-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="881ed-176">Selecteer in het dialoogvenster **Gegevensbron toevoegen** de optie **Dynamics 365 for Operations\Opsomming** om het dialoogvenster **Gegevensbroneigenschappen 'Opsomming'** te openen.</span><span class="sxs-lookup"><span data-stu-id="881ed-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="881ed-177">Voer in het veld **Naam** de tekst **enumNoYes** in.</span><span class="sxs-lookup"><span data-stu-id="881ed-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="881ed-178">Geef in het veld **Label** de optie **Onderdrukkingsopties** op.</span><span class="sxs-lookup"><span data-stu-id="881ed-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="881ed-179">Selecteer of typ **NoYes** in het veld **Naam van gegevenstype voor bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="881ed-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="881ed-180">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="881ed-180">Select **OK**.</span></span>

8. <span data-ttu-id="881ed-181">Configureer voor het geselecteerde element voor de indeling **SummaryLines** de formule om op te geven wanneer het besturingselement voor Word-inhoud dat aan het geselecteerde indelingselement is gekoppeld moet worden onderdrukt:</span><span class="sxs-lookup"><span data-stu-id="881ed-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="881ed-182">Selecteer op het tabblad **Toewijzing** in de sectie **Verwijderd** de optie **Bewerken** om de pagina **[Formuleontwerper](general-electronic-reporting-formula-designer.md)** te openen.</span><span class="sxs-lookup"><span data-stu-id="881ed-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="881ed-183">Voer in het veld **Formule** de formule `uipSuppress = enumNoYes.Yes` in.</span><span class="sxs-lookup"><span data-stu-id="881ed-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="881ed-184">Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.</span><span class="sxs-lookup"><span data-stu-id="881ed-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="881ed-185">Deze formule wordt toegepast op een gegenereerd document **nadat alle andere indelingselementen zijn uitgevoerd**.</span><span class="sxs-lookup"><span data-stu-id="881ed-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="881ed-186">Als u deze formule wilt toepassen, wordt een besturingselement voor Word-inhoud dat is gelabeld als een indelingselement waarvoor de formule is geconfigureerd (**SummaryLines** in dit geval) gevonden in een gegenereerd document.</span><span class="sxs-lookup"><span data-stu-id="881ed-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="881ed-187">Dit inhoudsbesturingselement wordt vervolgens volledig verwijderd samen met de rij in de Word-tabel die het bevat.</span><span class="sxs-lookup"><span data-stu-id="881ed-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="881ed-188">De detailrij van de overzichtssectie wordt uit het gegenereerde document verwijderd.</span><span class="sxs-lookup"><span data-stu-id="881ed-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="881ed-189">Op het moment van ontwerpen kunt u de formule **Verwijderd** configureren voor een indelingselement, zelfs als geen inhoudsbesturingselement in de Word-sjabloon die u gebruikt een label heeft die overeenkomt met de naam van een indelingselement waarvoor de eigenschap **Verwijderd** is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="881ed-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="881ed-190">Wanneer u de indeling valideert tijdens het ontwerpen, ontvangt u een [waarschuwing](er-components-inspections.md#i14) over deze inconsistentie.</span><span class="sxs-lookup"><span data-stu-id="881ed-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="881ed-191">Tijdens de runtime wordt een uitzondering gemaakt als geen inhoudsbesturingselement in de Word-sjabloon die u gebruikt een label heeft die overeenkomt met de naam van een indelingselement waarvoor de eigenschap **Verwijderd** is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="881ed-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="881ed-192">Stel op het tabblad **Toewijzing** in de sectie **Verwijderd** de optie **Met bovenliggend element** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="881ed-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="881ed-193">U moet deze optie op **Ja** instellen als u de gehele Word-tabel wilt verwijderen als het bovenliggende object van de rij met de details van de overzichtssectie.</span><span class="sxs-lookup"><span data-stu-id="881ed-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="881ed-194">Als u deze optie op **Nee** instelt, blijft de koptekstrij in het gegenereerde document staan.</span><span class="sxs-lookup"><span data-stu-id="881ed-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="881ed-195">Selecteer **Opslaan** om de wijzigingen in de bewerkbare indeling op te slaan.</span><span class="sxs-lookup"><span data-stu-id="881ed-195">Select **Save** to save your changes to the editable format.</span></span>

    ![De gegenereerde uitvoer in Word-indeling](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="881ed-197">De gewijzigde indeling uitvoeren om Word-uitvoer te maken</span><span class="sxs-lookup"><span data-stu-id="881ed-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="881ed-198">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="881ed-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="881ed-199">Selecteer het betalingsjournaal dat u hebt gemaakt en selecteer vervolgens **Regels**.</span><span class="sxs-lookup"><span data-stu-id="881ed-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="881ed-200">Selecteer op de pagina **Leverancierbetalingen** alle rijen en selecteer vervolgens **Betalingsstatus** \> **Geen**.</span><span class="sxs-lookup"><span data-stu-id="881ed-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="881ed-201">Selecteer **Betalingen genereren**.</span><span class="sxs-lookup"><span data-stu-id="881ed-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="881ed-202">Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.</span><span class="sxs-lookup"><span data-stu-id="881ed-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="881ed-203">Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="881ed-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="881ed-204">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="881ed-204">Select **OK**.</span></span>
8. <span data-ttu-id="881ed-205">Ga naar het dialoogvenster **Parameters elektronisch rapport** en selecteer **Ja** in het veld **Overzichtssectie onderdrukken**.</span><span class="sxs-lookup"><span data-stu-id="881ed-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="881ed-206">Selecteer **OK** en analyseer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="881ed-206">Select **OK**, and analyze the generated output.</span></span>

    ![Gegenereerde uitvoer in Word-indeling](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="881ed-208">De uitvoer bevat niet de overzichtssectie omdat deze is onderdrukt.</span><span class="sxs-lookup"><span data-stu-id="881ed-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="881ed-209">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="881ed-209">Additional resources</span></span>

- [<span data-ttu-id="881ed-210">Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling</span><span class="sxs-lookup"><span data-stu-id="881ed-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="881ed-211">Een nieuwe ER-configuratie ontwerpen om rapporten in Word-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="881ed-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="881ed-212">ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling</span><span class="sxs-lookup"><span data-stu-id="881ed-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="881ed-213">Het geconfigureerde ER-onderdeel inspecteren om runtimeproblemen te voorkomen</span><span class="sxs-lookup"><span data-stu-id="881ed-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]