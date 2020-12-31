---
title: Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen
description: Dit onderwerp biedt informatie over hoe u de indeling voor elektronische rapportage, die wordt gebruikt voor het genereren van bedrijfsdocumenten, kunt wijzigen door een gewijzigde Excel-sjabloon opnieuw toe te passen.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa15ae3111f7b91fd63afedb3ef21709d7d866d8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682212"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="4d714-103">Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen</span><span class="sxs-lookup"><span data-stu-id="4d714-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d714-104">Het hulpmiddel Elektronische rapportage (ER) wordt gebruikt voor het genereren van bedrijfsdocumenten in elektronische vorm.</span><span class="sxs-lookup"><span data-stu-id="4d714-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="4d714-105">Als u een bedrijfsdocument wilt genereren, moet u een indeling voor elektronische rapportage maken en vervolgens de ER-ontwerper gebruiken om de indeling van het bedrijfsdocument te bepalen en op te geven welke gegevens moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="4d714-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="4d714-106">Vervolgens kunt u de ER-indeling uitvoeren om het bedrijfsdocument te genereren.</span><span class="sxs-lookup"><span data-stu-id="4d714-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="4d714-107">Het ER-hulpmiddel kan worden gebruikt om bedrijfsdocumenten als Microsoft Excel-bestanden te genereren.</span><span class="sxs-lookup"><span data-stu-id="4d714-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="4d714-108">U kunt een Excel-document als sjabloon gebruiken voor deze documenten.</span><span class="sxs-lookup"><span data-stu-id="4d714-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="4d714-109">U geeft de documentindeling in de ER-ontwerper op door in de opgegeven ER-indeling de inhoud te importeren van het Excel-document dat u wilt gebruiken als sjabloon.</span><span class="sxs-lookup"><span data-stu-id="4d714-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="4d714-110">Speel de taakbegeleiding **ER Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling** (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) af voor meer informatie en en om te oefenen met dit scenario.</span><span class="sxs-lookup"><span data-stu-id="4d714-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="4d714-111">Als u het Excel-document bewerkt dat wordt gebruikt als een sjabloon voor een bedrijfsdocument, kunt u met nieuwe ER-functionaliteit de bijgewerkte sjabloon opnieuw toepassen op de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="4d714-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="4d714-112">De ER-indeling wordt vervolgens bijgewerkt zodat deze in overeenstemming is met de bijgewerkte sjabloon.</span><span class="sxs-lookup"><span data-stu-id="4d714-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="4d714-113">Speel de taakbegeleiding **Een indeling voor elektronische aangifte wijzigen door een Excel-sjabloon opnieuw toe te passen** (onderdeel van het bedrijfsproces 7.5.5.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10683)) af voor meer informatie over deze functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="4d714-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="4d714-114">Als onderdeel van de taakbegeleidingsstap voor het importeren van een bijgewerkte sjabloon gebruikt u de gewijzigde sjabloon van het Excel-bestand met het betalingsrapport (SampleVendPaymWsReport2) als sjabloon.</span><span class="sxs-lookup"><span data-stu-id="4d714-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>
