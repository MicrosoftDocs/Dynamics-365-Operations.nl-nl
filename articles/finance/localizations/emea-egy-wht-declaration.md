---
title: Bronbelastingaangifte voor Egypte
description: In dit onderwerp wordt uitgelegd hoe u de bronbelastingaangiften voor Egypte configureert en genereert.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8c9aaa3868167806ce3189d724621991ec7e53eb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022806"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="25f7e-103">Bronbelastingaangifte voor Egypte (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="25f7e-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="25f7e-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="25f7e-104">Overview</span></span>
<span data-ttu-id="25f7e-105">In dit onderwerp wordt uitgelegd hoe u de bronbelastingaangifte en de bronbelastingaangifteformulieren 41 en 11 instelt en genereert voor rechtspersonen in Egypte</span><span class="sxs-lookup"><span data-stu-id="25f7e-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="25f7e-106">Alle Egyptische entiteiten moeten formulier 41 voorbereiden, waarin alle belastingen worden samengevat die zijn ingehouden van lokale leveranciers en serviceproviders.</span><span class="sxs-lookup"><span data-stu-id="25f7e-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="25f7e-107">Behalve formulier 41 moet ook formulier 11 worden gegenereerd voor alle ingehouden belastingen van buitenlandse leveranciers.</span><span class="sxs-lookup"><span data-stu-id="25f7e-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="25f7e-108">Het rapport **Bronbelastingaangifte** in Dynamics 365 Finance bevat de volgende rapporten:</span><span class="sxs-lookup"><span data-stu-id="25f7e-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="25f7e-109">Aangifteformuliernr.</span><span class="sxs-lookup"><span data-stu-id="25f7e-109">Declaration form No.</span></span> <span data-ttu-id="25f7e-110">41</span><span class="sxs-lookup"><span data-stu-id="25f7e-110">41</span></span>
- <span data-ttu-id="25f7e-111">Aangifteformuliernr.</span><span class="sxs-lookup"><span data-stu-id="25f7e-111">Declaration form No.</span></span> <span data-ttu-id="25f7e-112">11</span><span class="sxs-lookup"><span data-stu-id="25f7e-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="25f7e-113">Vereisten</span><span class="sxs-lookup"><span data-stu-id="25f7e-113">Prerequisites</span></span>
<span data-ttu-id="25f7e-114">Het primaire adres van de rechtspersoon moet in Egypte zijn.</span><span class="sxs-lookup"><span data-stu-id="25f7e-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="25f7e-115">In het werkgebied **Functiebeheer** moet de volgende functie zijn ingeschakeld:</span><span class="sxs-lookup"><span data-stu-id="25f7e-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="25f7e-116">**Algemene bronbelasting**</span><span class="sxs-lookup"><span data-stu-id="25f7e-116">**Global withholding tax**</span></span>

<span data-ttu-id="25f7e-117">Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het inschakelen van functies.</span><span class="sxs-lookup"><span data-stu-id="25f7e-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="25f7e-118">Ga naar **Belasting** > **Instellen** > **Parameters** > **Grootboekparameters** en stel op het tabblad **Bronbelasting** de optie **Algemene bronbelasting** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="25f7e-119">Importeer in het werkgebied **Elektronische rapportage** de volgende indelingen voor elektronische rapportage in vanuit de opslagplaats:</span><span class="sxs-lookup"><span data-stu-id="25f7e-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="25f7e-120">Bronbelastingaangifte Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="25f7e-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="25f7e-121">De bovenstaande indeling is gebaseerd op het **belastingaangiftemodel** en maakt gebruik van de **Modeltoewijzing belastingaangifte**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="25f7e-122">Deze aanvullende configuratie wordt automatisch geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="25f7e-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="25f7e-123">Zie [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) voor meer informatie over het downloaden van ER-configuraties vanuit Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="25f7e-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="25f7e-124">Configuraties van elektronische aangifte downloaden</span><span class="sxs-lookup"><span data-stu-id="25f7e-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="25f7e-125">De implementatie van de bronbelastingaangifteformulieren voor Egypte is gebaseerd op ER-configuraties (elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="25f7e-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="25f7e-126">Zie [Elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) voor meer informatie over de capaciteiten en concepten van configureerbare rapportage.</span><span class="sxs-lookup"><span data-stu-id="25f7e-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="25f7e-127">Volg de instructies in het onderwerp [Configuraties voor elektronische rapportage downloaden vanuit Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) voor meer informatie over productie- en gebruikersacceptatietestomgevingen (UAT).</span><span class="sxs-lookup"><span data-stu-id="25f7e-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="25f7e-128">Als u de bronbelastingsaangiften wilt genereren in een Egyptische rechtspersoon, moet u de volgende configuraties uploaden:</span><span class="sxs-lookup"><span data-stu-id="25f7e-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="25f7e-129">Belastingaangiftemodel.versie.82.xml of hoger</span><span class="sxs-lookup"><span data-stu-id="25f7e-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="25f7e-130">Belastingaangiftemodeltoewijzing.versie.82.133.xml of hoger</span><span class="sxs-lookup"><span data-stu-id="25f7e-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="25f7e-131">Bronbelastingaangifte Excel (EG).versie.82.21 of een latere versie</span><span class="sxs-lookup"><span data-stu-id="25f7e-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="25f7e-132">Nadat u het downloaden van de ER-configuraties vanuit Lifecycle Services (LCS) of de algemene opslagplaats hebt voltooid, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="25f7e-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="25f7e-133">Ga naar het werkgebied **Elektronische rapportage** en selecteer de tegel **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="25f7e-134">Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen > Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="25f7e-135">Upload alle bestanden in de volgorde waarin ze onder de vorige opsommingstekens zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="25f7e-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="25f7e-136">Nadat alle configuraties zijn geüpload, moet de configuratiestructuur aanwezig zijn in Finance.</span><span class="sxs-lookup"><span data-stu-id="25f7e-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="25f7e-137">Toepassingsspecifieke parameters instellen</span><span class="sxs-lookup"><span data-stu-id="25f7e-137">Set up application-specific parameters</span></span>

<span data-ttu-id="25f7e-138">Met de optie voor toepassingspecifieke parameters kunnen gebruikers bepalen hoe de btw-transacties worden geclassificeerd en berekend in elke regel van een gegenereerd rapport, afhankelijk van de configuratie voor **artikelgroep voor bronbelasting** of andere criteria die zijn vastgelegd in de definitie van opzoekcriteria.</span><span class="sxs-lookup"><span data-stu-id="25f7e-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="25f7e-139">Bronbelastingaangifteformulier 41 bevat een specifieke kolom waarin de bronbelastingtransactie moet worden geclassificeerd in overeenstemming met de classificatie van de belastingdienst met de naam **Kortingscodetype**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="25f7e-140">In plaats van deze nieuwe classificaties als nieuwe invoergegevens op te nemen wanneer de transacties worden geboekt, worden de classificaties bepaald op basis van de verschillende opzoekacties in **Configuraties** > **Toepassingsspecifieke parameters instellen** > **Instellen** om te voldoen aan de vereisten van bronbelastingrapporten voor Egypte.</span><span class="sxs-lookup"><span data-stu-id="25f7e-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="25f7e-141">De volgende configuratie wordt gebruikt om de transacties te classificeren in het rapport Bronbelastingaangifteformulier 41:</span><span class="sxs-lookup"><span data-stu-id="25f7e-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="25f7e-142">**DiscountTaxTypeLookup** -> Kolomnr. 18</span><span class="sxs-lookup"><span data-stu-id="25f7e-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="25f7e-143">Voer de volgende stappen uit om de verschillende opzoekbewerkingen in te stellen die worden gebruikt om de bronbelastingaangiften en rapporten voor bijbehorende boeken te genereren.</span><span class="sxs-lookup"><span data-stu-id="25f7e-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="25f7e-144">Ga naar het werkgebied **Elektronische rapportage** en selecteer **Configuraties** > **Instellen** om de regels in te stellen om te identificeren hoe transacties worden geclassificeerd in het bronbelastingaangifterapport.</span><span class="sxs-lookup"><span data-stu-id="25f7e-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="25f7e-145">Selecteer de huidige versie en selecteer de zoeknaam op het sneltabblad **Zoekopdrachten**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="25f7e-146">Bijvoorbeeld **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="25f7e-147">Deze opzoekactie identificeert de lijst met kortingstypen die de belastingdienst vereist.</span><span class="sxs-lookup"><span data-stu-id="25f7e-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="25f7e-148">Selecteer op het sneltablijst **Voorwaarden** de optie **Toevoegen** en selecteer in de nieuwe regel in de kolom **Opzoekresultaat** de gerelateerde regel die de classificatie in **Kolom 18** vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="25f7e-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="25f7e-149">Selecteer in de kolom **Artikelgroep voor bronbelasting** de gerelateerde code die wordt gebruikt om de classificatie te identificeren.</span><span class="sxs-lookup"><span data-stu-id="25f7e-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="25f7e-150">Bijvoorbeeld **Toegestane korting**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="25f7e-151">Herhaal stappen 3 en 4 voor alle beschikbare opzoekbewerkingen.</span><span class="sxs-lookup"><span data-stu-id="25f7e-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="25f7e-152">Selecteer nogmaals **Toevoegen** om de laatste recordregel op te nemen en selecteer in de kolom **Opzoekresultaat** de optie **Niet van toepassing**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="25f7e-153">Selecteer **Niet leeg** in de resterende kolommen.</span><span class="sxs-lookup"><span data-stu-id="25f7e-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="25f7e-154">Grootboekparameters instellen</span><span class="sxs-lookup"><span data-stu-id="25f7e-154">Set up General ledger parameters</span></span>

<span data-ttu-id="25f7e-155">Als u de bronbelastingaangifteformulierrapporten wilt genereren in Microsoft Excel, definieert u een ER-indeling op de pagina **Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="25f7e-156">Ga naar **Belasting** > **Instellen** > **Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="25f7e-157">Selecteer op het tabblad **Bronbelasting** in het veld **Indelingstoewijzing voor bronbelastingaangifte** de optie **Bronbelastingaangifte Excel (EG)**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="25f7e-158">Als u het veld leeg laat, wordt de standaard btw-aangifte gegenereerd in de SSRS-indeling.</span><span class="sxs-lookup"><span data-stu-id="25f7e-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Aangifteformulier](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="25f7e-160">De formulieren voor bronbelastingaangifte genereren</span><span class="sxs-lookup"><span data-stu-id="25f7e-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="25f7e-161">Het proces van het voorbereiden en indienen van een bronbelastingaangifteformulier voor een specifieke periode is gebaseerd op de bronbelastingtransacties die tijdens de taak voor het vereffenen en boeken van belastingbetalingen zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="25f7e-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="25f7e-162">Zie [Algemene bronbelasting](../general-ledger/global-withholding-tax-overview.md) voor meer informatie over algemene bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="25f7e-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="25f7e-163">Voltooi de volgende stappen om het belastingaangifterapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="25f7e-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="25f7e-164">Ga naar **Belasting** > **Aangiften** > **Bronbelasting** > \**Betaling van bronbelasting*.</span><span class="sxs-lookup"><span data-stu-id="25f7e-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="25f7e-165">Selecteer de vereffeningsperiode en selecteer vervolgens de vanaf-datum voor het rapport.</span><span class="sxs-lookup"><span data-stu-id="25f7e-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="25f7e-166">Voer de transactiedatum in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="25f7e-167">Selecteer een of meer formuliertypen **Formulier 41**, **Formulier 11** of **Geen** in het dialoogvenster dat wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="25f7e-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="25f7e-168">Als u **Geen** selecteert, wordt het standaardrapport gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="25f7e-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="25f7e-169">Selecteer de taal.</span><span class="sxs-lookup"><span data-stu-id="25f7e-169">Select the language.</span></span> <span data-ttu-id="25f7e-170">Alle rapporten worden vertaald in **en-us** en **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="25f7e-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="25f7e-171">Voer het filiaal en de naam in van de bank waar de belastingbetaling plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="25f7e-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="25f7e-172">Selecteer het type bedrijf en voer vervolgens de cheque- en documentnummers in.</span><span class="sxs-lookup"><span data-stu-id="25f7e-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="25f7e-173">Voer het entiteitstype in.</span><span class="sxs-lookup"><span data-stu-id="25f7e-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="25f7e-174">Voer de naam in van de persoon die is geregistreerd om het formulier toe te wijzen en selecteer **OK** om het genereren van het rapport te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="25f7e-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
