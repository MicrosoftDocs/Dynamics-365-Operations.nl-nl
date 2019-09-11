---
title: Fout aan werkorder toevoegen
description: In dit onderwerp wordt beschreven hoe u foutregistraties toevoegt aan werkorders in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875593"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="58c58-103">Fout aan werkorder toevoegen</span><span class="sxs-lookup"><span data-stu-id="58c58-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="58c58-104">Aan een werkorder kunt u fouten toevoegen die in de foutontwerper zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="58c58-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="58c58-105">Het activum dat is geselecteerd in de werkorder moet activumtypen bevatten waaraan een of meer foutrecords zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="58c58-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="58c58-106">In de sectie [Foutbeheer](../setup-for-work-orders/fault-management.md) vindt u meer informatie over de instellingen.</span><span class="sxs-lookup"><span data-stu-id="58c58-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="58c58-107">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="58c58-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="58c58-108">Selecteer in de lijst de werkorder waarvoor u een foutregistratie wilt maken en klik op **Fout in activum**.</span><span class="sxs-lookup"><span data-stu-id="58c58-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="58c58-109">Klik op het sneltabblad **Symptomen** op **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="58c58-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="58c58-110">In het veld **Fout** wordt automatisch een volgnummer voor de fout ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="58c58-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="58c58-111">Selecteer het betreffende symptoom in het veld **Foutsymptoom**.</span><span class="sxs-lookup"><span data-stu-id="58c58-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="58c58-112">Selecteer **Foutgebied** en **Fouttype**.</span><span class="sxs-lookup"><span data-stu-id="58c58-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="58c58-113">Het veld **Foutdatum** wordt automatisch ingesteld op de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="58c58-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="58c58-114">Selecteer een andere datum, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="58c58-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="58c58-115">Voeg op het sneltabblad **Oorzaken voor geselecteerd symptoom** een regel toe waarin de oorzaak van het probleem wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="58c58-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="58c58-116">Voeg op het sneltabblad **Oplossingen voor geselecteerd symptoom** een regel toe waarin een mogelijke oplossing voor het probleem wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="58c58-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="58c58-117">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="58c58-117">Click **Save**.</span></span>

![Figuur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="58c58-119">Activafouten weergeven</span><span class="sxs-lookup"><span data-stu-id="58c58-119">View asset faults</span></span>

<span data-ttu-id="58c58-120">In de lijst **Activafouten** kunt u een overzicht weergeven van alle fouten die zijn geregistreerd voor activa.</span><span class="sxs-lookup"><span data-stu-id="58c58-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="58c58-121">Klik op **Activabeheer** > **Query's** > **Activafout** > **Activafouten** om de lijst te openen.</span><span class="sxs-lookup"><span data-stu-id="58c58-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="58c58-122">Rapport met activafouten afdrukken</span><span class="sxs-lookup"><span data-stu-id="58c58-122">Print asset fault report</span></span>

<span data-ttu-id="58c58-123">Via de lijstpagina **Alle activa** kunt u een rapport met activafouten afdrukken waarin alle foutregistraties en een grafisch overzicht van foutstatistieken worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="58c58-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="58c58-124">Klik op **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="58c58-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="58c58-125">Selecteer in de lijst **Activa** het activum waarvoor u een foutrapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="58c58-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="58c58-126">Klik op het tabblad **Algemeen** in de sectie **Rapporten** op **Fout in activum**.</span><span class="sxs-lookup"><span data-stu-id="58c58-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="58c58-127">Voeg een specifieke periode in of selecteer een fouttype.</span><span class="sxs-lookup"><span data-stu-id="58c58-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="58c58-128">Klik op **OK** om het rapport af te drukken.</span><span class="sxs-lookup"><span data-stu-id="58c58-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="58c58-129">U kunt ook een foutrapport voor verschillende activa of activatypen afdrukken door te klikken op **Activabeheer** > **Rapporten** > **Activa** > **Fout in activum**.</span><span class="sxs-lookup"><span data-stu-id="58c58-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

