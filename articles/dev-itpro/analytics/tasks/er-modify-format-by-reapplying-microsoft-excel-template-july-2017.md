--- 
title: Een indeling wijzigen door een Microsoft Excel-sjabloon voor elektronische aangifte opnieuw toe te passen (ER)
description: Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling voltooien.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a><span data-ttu-id="03a77-103">Een indeling wijzigen door een Microsoft Excel-sjabloon voor elektronische aangifte opnieuw toe te passen (ER)</span><span class="sxs-lookup"><span data-stu-id="03a77-103">Modify a format by reapplying a Microsoft Excel template for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03a77-104">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling voltooien.</span><span class="sxs-lookup"><span data-stu-id="03a77-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="03a77-105">In deze procedure wordt uitgelegd hoe u een elektronische rapportage (ER)-indelingsconfiguratie wijzigt door het opnieuw toepassen van een Microsoft Excel-sjabloon die is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="03a77-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="03a77-106">In deze procedure importeert u een gewijzigde Excel-sjabloon in Emergency Recovery-indelingsconfiguraties die zijn gemaakt voor het voorbeeldbedrijf, Litware, Inc., en genereert u vervolgens elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="03a77-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="03a77-107">Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="03a77-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="03a77-108">Deze stappen kunnen worden voltooid met de GBSI-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="03a77-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="03a77-109">Voordat u begint, downloadt u het bestand SampleVendPaymWsReport2.xlsx en slaat u het op, dat wordt vermeld in het Help-onderwerp Een indeling voor elektronische aangifte wijzigen door een Microsoft Excel-sjabloon opnieuw toe te passen (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="03a77-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="03a77-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="03a77-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="03a77-111">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief.</span><span class="sxs-lookup"><span data-stu-id="03a77-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="03a77-112">Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure Een configuratieprovider maken en deze als actief markeren.</span><span class="sxs-lookup"><span data-stu-id="03a77-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="03a77-113">Selecteer de ER-indeling</span><span class="sxs-lookup"><span data-stu-id="03a77-113">Select the ER format</span></span>
1. <span data-ttu-id="03a77-114">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="03a77-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="03a77-115">Vouw "Betalingsmodel" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="03a77-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="03a77-116">Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.</span><span class="sxs-lookup"><span data-stu-id="03a77-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="03a77-117">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="03a77-117">Click Attachments.</span></span>
    * <span data-ttu-id="03a77-118">Het Excel-bestand SampleVendPaymWsReport.xlsx Excel wordt momenteel gebruikt als een sjabloon voor betalingsjournaalverwerking.</span><span class="sxs-lookup"><span data-stu-id="03a77-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="03a77-119">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="03a77-119">Click Open.</span></span>
    * <span data-ttu-id="03a77-120">Klik op Openen om de indeling van de Excel-sjabloon te bekijken.</span><span class="sxs-lookup"><span data-stu-id="03a77-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="03a77-121">Bekijk de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="03a77-121">Review the template.</span></span> <span data-ttu-id="03a77-122">Deze bevat momenteel de volgende details van elke betalingsregel: rekeningnummer van leverancier, leveranciersnaam, bank, routenummer, rekeningnummer, debet, credit en valuta.</span><span class="sxs-lookup"><span data-stu-id="03a77-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="03a77-123">Voor dit voorbeeld willen we deze lijst uitbreiden door details toe te voegen over de betalingsdatum.</span><span class="sxs-lookup"><span data-stu-id="03a77-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="03a77-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="03a77-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="03a77-125">Een nieuwe Excel-sjabloon opnieuw toepassen op ER-indeling</span><span class="sxs-lookup"><span data-stu-id="03a77-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="03a77-126">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="03a77-126">Click Designer.</span></span>
    * <span data-ttu-id="03a77-127">Open de conceptversie van de geselecteerde ER-indeling voor bewerking.</span><span class="sxs-lookup"><span data-stu-id="03a77-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="03a77-128">Klik in het actievenster op Importeren.</span><span class="sxs-lookup"><span data-stu-id="03a77-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="03a77-129">Klik op Bijwerken vanuit Excel.</span><span class="sxs-lookup"><span data-stu-id="03a77-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="03a77-130">Klik op 'Sjabloon bijwerken' en selecteer vervolgens het bestand SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="03a77-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="03a77-131">Klik op Sjabloon bijwerken en blader om het eerder gedownloade bestand SampleVendPaymWsReport2.xlsx te krijgen.</span><span class="sxs-lookup"><span data-stu-id="03a77-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="03a77-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="03a77-132">Click OK.</span></span>
    * <span data-ttu-id="03a77-133">De sjabloon SampleVendPaymWsReport2.xlsx wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="03a77-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="03a77-134">De structuur van de ER-indeling wordt gesynchroniseerd met de inhoud van de sjabloon, waarvan elementen worden toegevoegd aan de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="03a77-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="03a77-135">Bestaande elementen in de ER-indeling die niet zijn opgenomen in de sjabloon, worden verwijderd uit de indelingsdefinitie.</span><span class="sxs-lookup"><span data-stu-id="03a77-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="03a77-136">Selecteer in de structuur 'Excel'.</span><span class="sxs-lookup"><span data-stu-id="03a77-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="03a77-137">Het veld Sjabloon bevat nu een verwijzing naar de nieuwe sjabloon.</span><span class="sxs-lookup"><span data-stu-id="03a77-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="03a77-138">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="03a77-138">Click Attachments.</span></span>
7. <span data-ttu-id="03a77-139">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="03a77-139">Click Open.</span></span>
    * <span data-ttu-id="03a77-140">Klik op Openen om de indeling van de gewijzigde Excel-sjabloon te bekijken.</span><span class="sxs-lookup"><span data-stu-id="03a77-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="03a77-141">Bekijk de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="03a77-141">Review the template.</span></span> <span data-ttu-id="03a77-142">Deze bevat nu een regel voor de betalingsdatum.</span><span class="sxs-lookup"><span data-stu-id="03a77-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="03a77-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="03a77-143">Close the page.</span></span>
9. <span data-ttu-id="03a77-144">Vouw in de structuur 'Excel' uit.</span><span class="sxs-lookup"><span data-stu-id="03a77-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="03a77-145">Vouw in de structuur 'Excel\PaymLines' uit.</span><span class="sxs-lookup"><span data-stu-id="03a77-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="03a77-146">Selecteer in de structuur 'Excel\Betalingsregels\Betaaldatum'.</span><span class="sxs-lookup"><span data-stu-id="03a77-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="03a77-147">De ER-indeling bevat nu één artikel meer.</span><span class="sxs-lookup"><span data-stu-id="03a77-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="03a77-148">Er is een cel, Betaaldatum, toegevoegd aan de Excel-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="03a77-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="03a77-149">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="03a77-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="03a77-150">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="03a77-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="03a77-151">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="03a77-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="03a77-152">Selecteer "model\Payments\Transaction date(TransactionDate)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="03a77-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="03a77-153">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="03a77-153">Click Bind.</span></span>
    * <span data-ttu-id="03a77-154">Geef op wat voor gegevens tijdens de uitvoering aan de nieuwe cel worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="03a77-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="03a77-155">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="03a77-155">Click Save.</span></span>
18. <span data-ttu-id="03a77-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="03a77-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="03a77-157">De gewijzigde conceptversie van de ER-indeling inschakelen voor gebruik in betalingsjournaalverwerking</span><span class="sxs-lookup"><span data-stu-id="03a77-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="03a77-158">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="03a77-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="03a77-159">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="03a77-159">Click User parameters.</span></span>
3. <span data-ttu-id="03a77-160">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="03a77-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="03a77-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="03a77-161">Click OK.</span></span>
5. <span data-ttu-id="03a77-162">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="03a77-162">Click Edit.</span></span>
6. <span data-ttu-id="03a77-163">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="03a77-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="03a77-164">De gewijzigde conceptversie van de ER-indeling gebruiken voor betalingsjournaalverwerking</span><span class="sxs-lookup"><span data-stu-id="03a77-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="03a77-165">Controleer het gemaakte werkblad, inclusief nieuwe details van betalingsregels: betalingsdatum.</span><span class="sxs-lookup"><span data-stu-id="03a77-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


