---
title: Fout aan werkorder toevoegen
description: In dit onderwerp wordt beschreven hoe u foutregistraties toevoegt aan werkorders in Activabeheer.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a79986e3b477865bc1816a1d28c1b7094ae3974
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809801"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="f4fe0-103">Fout aan werkorder toevoegen</span><span class="sxs-lookup"><span data-stu-id="f4fe0-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f4fe0-104">Aan een werkorder kunt u fouten toevoegen die in de foutontwerper zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="f4fe0-105">Er moeten een of meer foutrecords worden gekoppeld aan de activumtypen die worden gebruikt voor het activum dat is geselecteerd in de werkorder.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="f4fe0-106">Zie [Foutbeheer](../setup-for-work-orders/fault-management.md) voor meer informatie over de instelling.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="f4fe0-107">Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f4fe0-108">Selecteer de werkorder waarvoor u een foutregistratie wilt maken en selecteer vervolgens in het actievenster op het tabblad **Werkorder** in de groep **Activum** de optie **Fout in activum**.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="f4fe0-109">Selecteer op het sneltabblad **Symptomen** de optie **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="f4fe0-110">In het veld **Fout** wordt automatisch een volgnummer voor de fout ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="f4fe0-111">Selecteer het relevante symptoom in het veld **Foutsymptoom**.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="f4fe0-112">Selecteer in de velden **Foutgebied** en **Fouttype** de juiste waarden.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="f4fe0-113">Het veld **Foutdatum** wordt automatisch ingesteld op de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="f4fe0-114">U kunt desgewenst een andere datum selecteren.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="f4fe0-115">Voeg op het sneltabblad **Oorzaken voor geselecteerd symptoom** een regel toe waarin de oorzaak van het probleem wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="f4fe0-116">Voeg op het sneltabblad **Oplossingen voor geselecteerd symptoom** een regel toe waarin een mogelijke oplossing voor het probleem wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="f4fe0-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-117">Select **Save**.</span></span>

<span data-ttu-id="f4fe0-118">In de onderstaande afbeelding ziet u een voorbeeld van een foutregistratie.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-118">The illustration below shows an example of a fault registration.</span></span>

![Figuur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="f4fe0-120">Activafouten weergeven</span><span class="sxs-lookup"><span data-stu-id="f4fe0-120">View asset faults</span></span>

<span data-ttu-id="f4fe0-121">In de lijst **Activafouten** kunt u een overzicht weergeven van alle fouten die zijn geregistreerd voor activa.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="f4fe0-122">Op de lijstpagina **Activafouten** kunt u een overzicht weergeven van alle fouten die zijn geregistreerd voor activa.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="f4fe0-123">Open de pagina door **Activabeheer** > **Query's** > **Activafout** > **Activafouten** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="f4fe0-124">Rapport met activafouten afdrukken</span><span class="sxs-lookup"><span data-stu-id="f4fe0-124">Print asset fault report</span></span>

<span data-ttu-id="f4fe0-125">Via de lijstpagina **Alle activa** kunt u een rapport met activafouten afdrukken waarin alle foutregistraties en een grafisch overzicht van foutstatistieken worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="f4fe0-126">Selecteer **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="f4fe0-127">Selecteer het activum waarvoor u een foutrapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="f4fe0-128">Selecteer in het actievenster op het tabblad **Algemeen** in de groep **Rapporten** de optie **Activumfout**.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="f4fe0-129">Voer een specifieke periode in of selecteer een fouttype.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="f4fe0-130">Selecteer **OK** om het rapport af te drukken.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="f4fe0-131">U kunt een foutrapport voor verschillende activa of activatypen afdrukken door **Activabeheer** > **Rapporten** > **Activa** > **Fout in activum** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f4fe0-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]