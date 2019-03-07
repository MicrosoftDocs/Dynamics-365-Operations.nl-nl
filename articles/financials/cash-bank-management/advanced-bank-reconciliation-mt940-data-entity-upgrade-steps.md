---
title: 'Geavanceerde bankafstemming MT940-import: upgrade van de samengestelde gegevensentiteit'
description: Een volgnummer moet worden toegevoegd aan de entiteit voor bankafschriftimport, zodat de MT940-indeling wordt ondersteund.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "343783"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="48184-103">Geavanceerde bankafstemming MT940-import: upgrade van de samengestelde gegevensentiteit</span><span class="sxs-lookup"><span data-stu-id="48184-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48184-104">Een volgnummer moet worden toegevoegd aan de entiteit voor bankafschriftimport, zodat de MT940-indeling wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="48184-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="48184-105">Met de volgende stappen kunt u de entiteit voor import van bankafschriften toevoegen, die de MT940-indeling ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="48184-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="48184-106">Compileer en synchroniseer de volgende bestanden:</span><span class="sxs-lookup"><span data-stu-id="48184-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="48184-107">Samengestelde entiteit\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="48184-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="48184-108">Entiteit\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="48184-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="48184-109">Entiteit\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="48184-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="48184-110">Entiteit\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="48184-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="48184-111">Entiteit\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="48184-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="48184-112">Tabellen\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="48184-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="48184-113">Gegevensbeheer\\gegevensprojecten.</span><span class="sxs-lookup"><span data-stu-id="48184-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="48184-114">Laad de projecten voor MT940-import</span><span class="sxs-lookup"><span data-stu-id="48184-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="48184-115">Vervang de XSLT.</span><span class="sxs-lookup"><span data-stu-id="48184-115">Change XSLT.</span></span>
            -   <span data-ttu-id="48184-116">Klik op **Kaart weergeven**.</span><span class="sxs-lookup"><span data-stu-id="48184-116">Click **View map**.</span></span>
            -   <span data-ttu-id="48184-117">Klik op **Kaart weergeven** op het bankafschriftdocument.</span><span class="sxs-lookup"><span data-stu-id="48184-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="48184-118">Klik op **Transformaties**.</span><span class="sxs-lookup"><span data-stu-id="48184-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="48184-119">Verwijder het bestand BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="48184-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="48184-120">Voeg de nieuwe versie van BankReconiliation-to-Composite.xsl toe.</span><span class="sxs-lookup"><span data-stu-id="48184-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="48184-121">Maak **Volgnummer** op de indeling **Brongegevens** zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="48184-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="48184-122">Indeling van brongegevens = XML-element.</span><span class="sxs-lookup"><span data-stu-id="48184-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="48184-123">Naam entiteit = Bankafschriften.</span><span class="sxs-lookup"><span data-stu-id="48184-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="48184-124">Gegevensbestand uploaden = nieuwe versie van SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="48184-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="48184-125">Klik op **Ja** om het bestaande bestand te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="48184-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="48184-126">Klik op **Ja** om een nieuwe toewijzing te genereren.</span><span class="sxs-lookup"><span data-stu-id="48184-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="48184-127">Controleer of **SequenceNumber** is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="48184-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="48184-128">Klik op **Kaart weergeven** op de entiteit Afschrift.</span><span class="sxs-lookup"><span data-stu-id="48184-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="48184-129">Controleer dat **SequenceNumber** is toegewezen van Bron naar Fasering.</span><span class="sxs-lookup"><span data-stu-id="48184-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="48184-130">Importeer het nieuwe afschrift.</span><span class="sxs-lookup"><span data-stu-id="48184-130">Import the new statement.</span></span>




