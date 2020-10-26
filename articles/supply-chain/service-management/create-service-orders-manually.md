---
title: Handmatig serviceorders maken
description: U kunt handmatig serviceorders maken door een serviceovereenkomst te gebruiken of door het formulier **Serviceorders** te gebruiken.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51cfdb94a368df9e7082af3c768c79df44000342
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978720"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="232c8-103">Handmatig serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="232c8-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="232c8-104">U kunt handmatig serviceorders maken door een serviceovereenkomst te gebruiken of door het formulier **Serviceorders** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="232c8-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="232c8-105">U kunt ook een serviceorder vanuit een project maken.</span><span class="sxs-lookup"><span data-stu-id="232c8-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="232c8-106">U kunt geautomatiseerde processen gebruiken om serviceorders te maken.</span><span class="sxs-lookup"><span data-stu-id="232c8-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="232c8-107">Handmatig een serviceorder maken vanuit een serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="232c8-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="232c8-108">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="232c8-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="232c8-109">Selecteer een serviceovereenkomst of maak een nieuwe serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="232c8-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="232c8-110">Klik op het tabblad **Leveren** en in de groep **Maken** op **Geplande serviceorders** om het formulier **Serviceorders maken** te openen.</span><span class="sxs-lookup"><span data-stu-id="232c8-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="232c8-111">Handmatig een serviceorder maken in het formulier Serviceorders</span><span class="sxs-lookup"><span data-stu-id="232c8-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="232c8-112">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="232c8-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="232c8-113">Druk op Ctrl+N om een nieuwe serviceorder te maken.</span><span class="sxs-lookup"><span data-stu-id="232c8-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="232c8-114">Maak serviceorderregels voor de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="232c8-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="232c8-115">Als het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is ingeschakeld, kunt u de transacties vanuit de serviceorderregels boeken zonder de serviceorder aan een serviceovereenkomst te koppelen.</span><span class="sxs-lookup"><span data-stu-id="232c8-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="232c8-116">Als het selectievakje is uitgeschakeld, moet u de handmatig gemaakte serviceorder aan een project koppelen voordat u de serviceorderregels boekt.</span><span class="sxs-lookup"><span data-stu-id="232c8-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="232c8-117">Een serviceorder vanuit een project maken</span><span class="sxs-lookup"><span data-stu-id="232c8-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="232c8-118">Klik op **Projectbeheer en boekhouding** \> **Algemeen** \> **Projecten** \> **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="232c8-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="232c8-119">Klik in het formulier **Projecten** in het **actievenster** op het tabblad **Beheren** \> op **Service** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="232c8-119">In the **Projects** form, on the **Action Pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="232c8-120">Volg de vorige procedure voor het handmatig maken van een serviceorder in het formulier **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="232c8-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="232c8-121">In het veld **Project-ID** wordt de projectverwijzing weergegeven.</span><span class="sxs-lookup"><span data-stu-id="232c8-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="232c8-122">Als het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is ingeschakeld, kunt u de transacties vanuit de serviceorderregels boeken zonder de serviceorder aan een serviceovereenkomst te koppelen.</span><span class="sxs-lookup"><span data-stu-id="232c8-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="232c8-123">Als het selectievakje is uitgeschakeld, moet u de handmatig gemaakte serviceorder aan een project koppelen voordat u de serviceorderregels boekt.</span><span class="sxs-lookup"><span data-stu-id="232c8-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="232c8-124">Een serviceorder maken op basis van het formulier Verkooporder</span><span class="sxs-lookup"><span data-stu-id="232c8-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="232c8-125">U kunt een serviceorder maken in het formulier **Verkooporders** met behulp van de wizard **Een nieuwe serviceorder maken op basis van de verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="232c8-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="232c8-126">Klik op **Verkoop en marketing** \> **Algemeen** \> **Verkooporders** \> **Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="232c8-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="232c8-127">Open de relevante verkooporder.</span><span class="sxs-lookup"><span data-stu-id="232c8-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="232c8-128">Klik op het tabblad **Verkooporder** op **Serviceorder** om de wizard **Een nieuwe serviceorder maken op basis van de verkooporder** te starten.</span><span class="sxs-lookup"><span data-stu-id="232c8-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="232c8-129">Klik op **Volgende \>** en voltooi de volgende stappen op de pagina **Overeenkomst selecteren voor serviceorder**:</span><span class="sxs-lookup"><span data-stu-id="232c8-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="232c8-130">Gebruik het veld **Serviceovereenkomst** om de serviceovereenkomst te selecteren waaraan de nieuwe serviceorder moet worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="232c8-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="232c8-131">Optioneel: gebruik het veld **Project-ID** om deze serviceorder te koppelen aan een bepaald project.</span><span class="sxs-lookup"><span data-stu-id="232c8-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="232c8-132">Klik op **Volgende \>** en voltooi de volgende stappen op de pagina **Serviceorder maken**:</span><span class="sxs-lookup"><span data-stu-id="232c8-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="232c8-133">Geef in het veld **Voorkeurstijd service** een datum en een tijd op waarop u wilt dat het serviceverzoek begint.</span><span class="sxs-lookup"><span data-stu-id="232c8-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="232c8-134">Optioneel: wijzig de tekst in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="232c8-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="232c8-135">Dit veld bevat standaard de omschrijving van de serviceovereenkomst die u hebt geselecteerd op de vorige pagina.</span><span class="sxs-lookup"><span data-stu-id="232c8-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="232c8-136">Selecteer in het veld **Verantwoordelijk** de ID van de werknemer die verantwoordelijk is voor de overeenkomst en voer, als u dit weet, de ID van de voorkeurstechnicus van de klant in voor het serviceverzoek.</span><span class="sxs-lookup"><span data-stu-id="232c8-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="232c8-137">Selecteer in het veld **Contact-ID** de persoon in het bedrijf van de klant met wie contact moet worden opgenomen over de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="232c8-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="232c8-138">Klik op **Volgende\>** en klik vervolgens op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="232c8-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="232c8-139">Zie ook</span><span class="sxs-lookup"><span data-stu-id="232c8-139">See also</span></span>

[<span data-ttu-id="232c8-140">Serviceorders</span><span class="sxs-lookup"><span data-stu-id="232c8-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="232c8-141">Automatisch serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="232c8-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="232c8-142">[Serviceorders maken (klasseformulier)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="232c8-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 

