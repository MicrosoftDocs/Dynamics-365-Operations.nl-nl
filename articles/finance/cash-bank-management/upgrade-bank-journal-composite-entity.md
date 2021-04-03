---
title: De samengestelde entiteit Bankjournaal bijwerken
description: Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18137ca8cecc43b4269f14b36df2eb8063192e52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236342"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="ee782-103">De samengestelde entiteit Bankjournaal bijwerken</span><span class="sxs-lookup"><span data-stu-id="ee782-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee782-104">Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ee782-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="ee782-105">Gebruik de volgende stappen om het aanvullende veld BankTransactionType aan het samengestelde BankJournalEntity toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ee782-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="ee782-106">Compileer en synchroniseer de volgende samengestelde bankjournaalentiteiten, entiteiten en faseringstabellen:</span><span class="sxs-lookup"><span data-stu-id="ee782-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="ee782-107">Samengestelde entiteit\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="ee782-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="ee782-108">Entiteit\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="ee782-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="ee782-109">Entiteit\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="ee782-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="ee782-110">Tabel\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="ee782-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="ee782-111">Tabel\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="ee782-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="ee782-112">Gegevensbeheer\\gegevensprojecten.</span><span class="sxs-lookup"><span data-stu-id="ee782-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="ee782-113">Maak het type **Banktransactie** voor de indeling **Brongegevens** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="ee782-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="ee782-114">Indeling van brongegevens = XML-element</span><span class="sxs-lookup"><span data-stu-id="ee782-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="ee782-115">Entiteitsnaam = Bankjournaal</span><span class="sxs-lookup"><span data-stu-id="ee782-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="ee782-116">Gegevensbestand uploaden = nieuwe versie van SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="ee782-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="ee782-117">Klik op **Ja** om het bestaande bestand te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="ee782-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="ee782-118">Klik op **Ja** om een nieuwe toewijzing te genereren.</span><span class="sxs-lookup"><span data-stu-id="ee782-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="ee782-119">Controleer of het banktransactietype wordt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="ee782-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="ee782-120">Klik op **Kaart weergeven** voor de entiteit Regel.</span><span class="sxs-lookup"><span data-stu-id="ee782-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="ee782-121">Controleer of Banktransactietype is toegewezen van Bron aan Fasering.</span><span class="sxs-lookup"><span data-stu-id="ee782-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="ee782-122">Importeer het nieuwe afschrift.</span><span class="sxs-lookup"><span data-stu-id="ee782-122">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]