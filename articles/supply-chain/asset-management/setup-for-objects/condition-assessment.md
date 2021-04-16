---
title: Toestandsbeoordeling
description: In dit onderwerp wordt uitgelegd hoe u een sjabloon voor toestandsbeoordeling en registratie voor een activum in Activabeheer maakt.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 082a2bfd8818e511095e9ab2dcc22de59eb98d31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808419"
---
# <a name="condition-assessment"></a><span data-ttu-id="7e1cd-103">Toestandsbeoordeling</span><span class="sxs-lookup"><span data-stu-id="7e1cd-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7e1cd-104">In dit onderwerp wordt uitgelegd hoe u een sjabloon voor toestandsbeoordeling en registratie voor een activum in Activabeheer maakt.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="7e1cd-105">Een toestandsbeoordeling wordt met regelmatige tussenpozen uitgevoerd en het primaire doel is het maken en onderhouden van toestandsgegevens voor activa.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="7e1cd-106">Gezien vanuit preventief onderhoud, is het belangrijk om belangrijke informatie te bewaken, zoals de huidige toestand en de resterende levensduur.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="7e1cd-107">Bovendien kunt u, als u regelmatig een toestandsbeoordeling uitvoert, de omstandigheden op de machine in uw fabriek bewaken en vergelijken.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="7e1cd-108">Toestandsbeoordeling kan worden gebruikt om veel omstandigheden op uw apparatuur te meten en te bewaken.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="7e1cd-109">Voorbeeld: u zou trillingen op uw machines kunnen meten.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="7e1cd-110">Nadat u trillingsmetingen hebt vastgelegd in Activabeheer voor verschillende soorten apparatuur, kunt u zoeken naar de meest recengte geregistreerde beoordeling en trillingsmetingen bekijken.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="7e1cd-111">Toestandsbeoordeling wordt uitgevoerd voor activa.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="7e1cd-112">U stelt een sjabloon voor toestandsbeoordeling in op een type activum voordat u de procedure voor toestandsbeoordeling gaat uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="7e1cd-113">De reden voor het gebruik van sjablonen voor toestandsbeoordeling is om variatie van toestandsgegevens voor vergelijkbare activa te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="7e1cd-114">De volgorde voor het instellen en gebruiken van toestandsbeoordeling in Activabeheer is: eerst stelt u de vereiste sjablonen voor toestandsbeoordeling in.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="7e1cd-115">Vervolgens koppelt u sjablonen aan activatypen in het formulier **Activatypen**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="7e1cd-116">Tot slot kunt registraties voor toestandsbeoordeling maken voor een activum in het formulier **Activum**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="7e1cd-117">Een sjabloon voor toestandsbeoordeling maken</span><span class="sxs-lookup"><span data-stu-id="7e1cd-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="7e1cd-118">Selecteer **Activabeheer** > **Instellingen** > **Activatypen** > **Toestandsbeoordeling**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="7e1cd-119">Selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="7e1cd-120">Typ een id voor de sjabloon in het veld **Sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="7e1cd-121">Typ een naam voor de sjabloon in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="7e1cd-122">Voeg op het sneltabblad **Toestandsbeoordelingsregels** de regels toe die nodig zijn voor de toestandsbeoordeling, inclusief de selectie van het juiste toestandstype en de maateenheid.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="7e1cd-123">Voeg op het sneltabblad **Activatypen** de activatypen toe die gebruik moeten maken van de sjabloon voor toestandsbeoordeling.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="7e1cd-124">In de velden **Regels** en **Activatypen** in de groep **Details** boven aan het scherm ziet u het aantal beoordelingsregels en activatypen die zijn gerelateerd aan de geselecteerde sjabloon voor toestandsbeoordeling.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="7e1cd-125">Registratie van toestandsbeoordeling maken voor een activum</span><span class="sxs-lookup"><span data-stu-id="7e1cd-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="7e1cd-126">Selecteer **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="7e1cd-127">Selecteer in de lijst het activum waarvoor u een registratie van toestandsbeoordeling wilt maken.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="7e1cd-128">Klik op het tabblad **Algemeen** op **Toestandsbeoordeling**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="7e1cd-129">Klik op **Nieuw** om een nieuwe registratie te maken.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="7e1cd-130">Selecteer de datum voor de toestandsbeoordeling in het veld **Datum**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="7e1cd-131">Selecteer de naam van de medewerker die de registratie van de toestandsbeoordeling heeft uitgevoerd in het veld **Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="7e1cd-132">In het veld **Regels** ziet u het aantal beoordelingsregels dat is ingesteld voor de toestandsbeoordeling.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="7e1cd-133">Selecteer een sjabloon voor de toestandsbeoordeling in het veld **Sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="7e1cd-134">De naam van de sjabloon wordt automatisch ingevoegd in het veld **Naam** en de gerelateerde registratieregels worden ingevoegd op het sneltabblad **Toestandsbeoordelingsregels**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="7e1cd-135">U kunt notities invoegen die betrekking hebben op de geselecteerde toestandsbeoordeling op het sneltabblad **Notities**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="7e1cd-136">Voeg voor elke toestandsbeoordelingsregel meetgegevens in het veld **Waarde** in.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="7e1cd-137">U kunt een opmerking met betrekking tot de geselecteerde registratieregel invoegen op het sneltabblad **Toestandsbeoordelingsregels** > veld **Opmerkingen**.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="7e1cd-138">Als u een opmerking op een regel toevoegt, wordt het selectievakje **Opmerking** automatisch ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="7e1cd-139">Nadat u een toestandsbeoordelingsregistratie voor een activum hebt gemaakt, kunt u een rapport voor toestandsbeoordeling afdrukken.</span><span class="sxs-lookup"><span data-stu-id="7e1cd-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="7e1cd-140">U kunt ook de toestandsbeoordeling voor een werkorder registreren (**Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** > knop **Toestandsbeoordeling**).</span><span class="sxs-lookup"><span data-stu-id="7e1cd-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]