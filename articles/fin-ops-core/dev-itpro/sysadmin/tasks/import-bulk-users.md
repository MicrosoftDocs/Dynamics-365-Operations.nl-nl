---
title: Gebruikers importeren vanuit Azure Active Directory
description: Deze procedure kan worden gebruikt door systeembeheerders om handmatig geselecteerde gebruikers te importeren of een groot aantal gebruikers te importeren vanuit Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679809"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="3ee67-103">Gebruikers importeren vanuit Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3ee67-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="3ee67-104">Geselecteerde gebruikers importeren</span><span class="sxs-lookup"><span data-stu-id="3ee67-104">Import select users</span></span>

<span data-ttu-id="3ee67-105">Deze procedure kan worden gebruikt door systeembeheerders om een geselecteerde gebruikers te importeren vanuit Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3ee67-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="3ee67-106">Gebruiker wordt geïmporteerd met het huidige sessiebedrijf als standaardbedrijf.</span><span class="sxs-lookup"><span data-stu-id="3ee67-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3ee67-107">Wijzig het huidige bedrijf indien van toepassing voordat u gebruikers importeert.</span><span class="sxs-lookup"><span data-stu-id="3ee67-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3ee67-108">Ga naar **Systeembeheer > Gebruikers > Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="3ee67-109">Klik op **Gebruikers importeren**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-109">Click **Import users**.</span></span>
4. <span data-ttu-id="3ee67-110">Selecteer de gebruikers die moeten worden geïmporteerd en selecteer vervolgens **Gebruikers importeren**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="3ee67-111">Nadat het importeren is voltooid, moet u rollen toewijzen aan gebruikers.</span><span class="sxs-lookup"><span data-stu-id="3ee67-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="3ee67-112">Gebruikers bulksgewijs importeren</span><span class="sxs-lookup"><span data-stu-id="3ee67-112">Import users in bulk</span></span>

<span data-ttu-id="3ee67-113">Deze procedure kan worden gebruikt door systeembeheerders om een groot aantal gebruikers van Azure Active Directory te importeren.</span><span class="sxs-lookup"><span data-stu-id="3ee67-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="3ee67-114">Het is niet mogelijk om gebruikers te selecteren wanneer u de optie Batch importeren gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3ee67-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="3ee67-115">De import uitvoeren als een batchtaak</span><span class="sxs-lookup"><span data-stu-id="3ee67-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="3ee67-116">Gebruiker wordt geïmporteerd met het huidige sessiebedrijf als standaardbedrijf.</span><span class="sxs-lookup"><span data-stu-id="3ee67-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3ee67-117">Wijzig het huidige bedrijf indien van toepassing voordat u gebruikers importeert.</span><span class="sxs-lookup"><span data-stu-id="3ee67-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3ee67-118">Ga naar **Systeembeheer > Gebruikers > Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="3ee67-119">Klik op **Batch importeren**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="3ee67-120">Vouw de sectie **Op de achtergrond uitvoeren** uit.</span><span class="sxs-lookup"><span data-stu-id="3ee67-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="3ee67-121">Selecteer \*\*Ja in het veld **Batchverwerking**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="3ee67-122">Typ of selecteer een waarde in het veld **Batchgroep**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="3ee67-123">Deze stap is optioneel.</span><span class="sxs-lookup"><span data-stu-id="3ee67-123">This is an optional step.</span></span>  
7. <span data-ttu-id="3ee67-124">Selecteer **Ja** in het veld **Privé**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="3ee67-125">Deze stap is optioneel.</span><span class="sxs-lookup"><span data-stu-id="3ee67-125">This is an optional step.</span></span>  
8. <span data-ttu-id="3ee67-126">Selecteer **Ja** in het veld **Kritieke taak**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="3ee67-127">Deze stap is optioneel.</span><span class="sxs-lookup"><span data-stu-id="3ee67-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="3ee67-128">Selecteer een optie in het veld \*\*Categorie bewaken.</span><span class="sxs-lookup"><span data-stu-id="3ee67-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="3ee67-129">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-129">Click **OK**.</span></span>

<span data-ttu-id="3ee67-130">Nadat het importeren is voltooid, moet u rollen toewijzen aan gebruikers.</span><span class="sxs-lookup"><span data-stu-id="3ee67-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="3ee67-131">Uitvoeren in een sandbox-omgeving</span><span class="sxs-lookup"><span data-stu-id="3ee67-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="3ee67-132">Selecteer **Batch importeren**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="3ee67-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ee67-133">Select **OK**.</span></span>
