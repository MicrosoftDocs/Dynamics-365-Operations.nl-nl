---
title: Serviceorders annuleren
description: U kunt een serviceorder of serviceorderregel vanuit de serviceorder zelf annuleren of u kunt meerdere serviceorders annuleren door een periodieke taak uit te voeren.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
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
ms.openlocfilehash: b60feec05e923c25e0f0bacb28b510906d5f73cd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974680"
---
# <a name="cancel-service-orders"></a><span data-ttu-id="f5b94-103">Serviceorders annuleren</span><span class="sxs-lookup"><span data-stu-id="f5b94-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f5b94-104">U kunt een serviceorder of serviceorderregel vanuit de serviceorder zelf annuleren of u kunt meerdere serviceorders annuleren door een periodieke taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="f5b94-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f5b94-105">Serviceorders kunnen niet worden geannuleerd als in de fase waarin de serviceorder zich bevindt annuleren niet is toegestaan, als de serviceorder artikelbehoeften heeft of als de serviceorder al is geboekt.</span><span class="sxs-lookup"><span data-stu-id="f5b94-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="f5b94-106">Een serviceorder annuleren in het formulier Serviceorders</span><span class="sxs-lookup"><span data-stu-id="f5b94-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="f5b94-107">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="f5b94-108">Selecteer de serviceorder en klik in het actievenster op **Order annuleren**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="f5b94-109">Een serviceorderregel annuleren</span><span class="sxs-lookup"><span data-stu-id="f5b94-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="f5b94-110">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="f5b94-111">Dubbelklik op de serviceorder die de regel bevat die u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="f5b94-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="f5b94-112">Selecteer de serviceorderregel die u wilt annuleren en klik vervolgens op **Orderregel annuleren** om de status van de regel te wijzigen in **Geannuleerd**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="f5b94-113">Als u de annulering van een serviceorderregel ongedaan wilt maken en de status opnieuw wilt wijzigen in <STRONG>Gemaakt</STRONG>, klikt u op <STRONG>Annuleren intrekken</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f5b94-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="f5b94-114">Meerdere serviceorders annuleren</span><span class="sxs-lookup"><span data-stu-id="f5b94-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="f5b94-115">Klik op **Servicebeheer** \> **Periodiek** \> **Serviceorders** \> **Serviceorders annuleren**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="f5b94-116">Klik op de knop **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="f5b94-117">Selecteer in het formulier **Query** de kolom **Criteria** de serviceorders die u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="f5b94-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="f5b94-118">Klik op **OK** om het formulier **Query** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f5b94-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="f5b94-119">Schakel het selectievakje **Infologboek weergeven** in om een infologboek te genereren waarin de geannuleerde serviceorders worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f5b94-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="f5b94-120">Schakel het selectievakje **Annuleren intrekken** in als u de status **Geannuleerd** van een serviceorder wilt terugdraaien.</span><span class="sxs-lookup"><span data-stu-id="f5b94-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="f5b94-121">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-121">Click **OK**.</span></span>

<span data-ttu-id="f5b94-122">De geselecteerde serviceorders worden geannuleerd of de voortgangsstatus **Geannuleerd** wordt gewijzigd in **Onderhanden**.</span><span class="sxs-lookup"><span data-stu-id="f5b94-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f5b94-123">Als u het selectievakje <STRONG>Annuleren intrekken</STRONG> inschakelt, worden serviceorders met de voortgangsstatus <STRONG>Geannuleerd</STRONG> teruggedraaid en worden serviceorders met de voortgangsstatus <STRONG>Onderhanden</STRONG> niet geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="f5b94-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  


