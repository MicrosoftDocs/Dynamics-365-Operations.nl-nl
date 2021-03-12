---
title: Een adres aan een serviceorder toevoegen
description: Dit onderwerp beschrijft hoe u een klantadres aan de serviceorder toe te voegen.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6c8f00eb1a1fe2ef3aea22da20ce218d7568f64
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966050"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="2dcfd-103">Een adres aan een serviceorder toevoegen</span><span class="sxs-lookup"><span data-stu-id="2dcfd-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2dcfd-104">Dit onderwerp beschrijft hoe u een klantadres aan de serviceorder toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="2dcfd-105">Wanneer u een serviceorder maakt, worden de adresgegevens overgedragen vanuit het project waaraan de serviceorder is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="2dcfd-106">U kunt echter een alternatieve locatie uit adressen selecteren die al in Microsoft Dynamics AX voor klanten, leveranciers, locaties, magazijnen, serviceorders en projecten worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="2dcfd-107">U kunt ook nieuw adres maken.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-107">You can also create a new address.</span></span> <span data-ttu-id="2dcfd-108">Standaard, wordt het nieuwe adres naar het project overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="2dcfd-109">Echter, u kunt opgeven dat het nieuwe adres alleen voor dit exemplaar van de service relevant is.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="2dcfd-110">Als u dit doet, wordt het nieuwe adres niet naar het project overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="2dcfd-111">Maak een klantadres voor een serviceorder</span><span class="sxs-lookup"><span data-stu-id="2dcfd-111">Create a customer address for a service order</span></span>

<span data-ttu-id="2dcfd-112">Om een adres aan een serviceorder toe te voegen, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="2dcfd-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="2dcfd-113">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="2dcfd-114">Open de serviceorder waarvoor u een adres wilt maken.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="2dcfd-115">Klik in het **Actievenster** op **Bewerken** en vervolgens op **Koptekstweergave**.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="2dcfd-116">Klik in het sneltabblad **Adres** op **Adres toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="2dcfd-117">Voer in het formulier **Nieuw adres** een unieke naam voor het adres in en vul de resterende velden verder in.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="2dcfd-118">Als u dezelfde naam als een bestaand adres invoert, zal de informatie die u in de resterende velden invoert informatie voor het bestaande adres overschrijven.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="2dcfd-119">Klik op **OK** om het nieuwe adres naar de serviceorder te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="2dcfd-120">Een alternatief adres opgeven op een serviceorder</span><span class="sxs-lookup"><span data-stu-id="2dcfd-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="2dcfd-121">Om een alternatief adres aan een serviceorder toe te voegen, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="2dcfd-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="2dcfd-122">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="2dcfd-123">Open de serviceorder waarvoor u een alternatief adres wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="2dcfd-124">Klik in het **Actievenster** op **Bewerken** en vervolgens op **Koptekstweergave**.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="2dcfd-125">Klik op het sneltabblad **Adres** op **Ander adres**.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="2dcfd-126">Selecteer in het formulier **Adresselectie** in het veld **Recordtype** **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="2dcfd-127">Selecteer een adres, en klik vervolgens op **OK** om het naar de serviceorder te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2dcfd-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


