---
title: De samengestelde entiteit Bankjournaal bijwerken
description: Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 18b2b228f287a946eb18536b1ea93b0d6af6900c
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="14e89-103">De samengestelde entiteit Bankjournaal bijwerken</span><span class="sxs-lookup"><span data-stu-id="14e89-103">Update the bank journal composite entity</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="14e89-104">Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="14e89-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="14e89-105">Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="14e89-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="14e89-106">Compileer en synchroniseer de volgende samengestelde bankjournaalentiteiten, entiteiten en faseringstabellen:</span><span class="sxs-lookup"><span data-stu-id="14e89-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="14e89-107">Samengestelde entiteit\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="14e89-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="14e89-108">Entiteit\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="14e89-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="14e89-109">Entiteit\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="14e89-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="14e89-110">Tabel\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="14e89-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="14e89-111">Tabel\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="14e89-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="14e89-112">Gegevensbeheer\\gegevensprojecten.</span><span class="sxs-lookup"><span data-stu-id="14e89-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="14e89-113">Maak het type **Banktransactie**voor de indeling **Brongegevens** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="14e89-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="14e89-114">Indeling van brongegevens = XML-element</span><span class="sxs-lookup"><span data-stu-id="14e89-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="14e89-115">Entiteitsnaam = Bankjournaal</span><span class="sxs-lookup"><span data-stu-id="14e89-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="14e89-116">Gegevensbestand uploaden = nieuwe versie van SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="14e89-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="14e89-117">Klik op **Ja** om het bestaande bestand te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="14e89-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="14e89-118">Klik op **Ja** om een nieuwe toewijzing te genereren.</span><span class="sxs-lookup"><span data-stu-id="14e89-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="14e89-119">Controleer of het banktransactietype wordt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="14e89-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="14e89-120">Klik op **Kaart weergeven** voor de entiteit Regel.</span><span class="sxs-lookup"><span data-stu-id="14e89-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="14e89-121">Controleer of Banktransactietype is toegewezen van Bron aan Fasering.</span><span class="sxs-lookup"><span data-stu-id="14e89-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="14e89-122">Importeer het nieuwe afschrift.</span><span class="sxs-lookup"><span data-stu-id="14e89-122">Import the new statement.</span></span>





