---
title: Leveringsmethode wijzigen in POS
description: In dit onderwerp wordt beschreven hoe u de bewerking Leveringsmethode wijzigen in POS configureert en gebruikt.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965422"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="c313e-103">Leveringsmethode wijzigen in POS</span><span class="sxs-lookup"><span data-stu-id="c313e-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c313e-104">In dit onderwerp wordt beschreven hoe u de functionaliteit Leveringsmethode wijzigen kunt instellen en gebruiken in uw POS-omgeving.</span><span class="sxs-lookup"><span data-stu-id="c313e-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="c313e-105">In Dynamics 365 Commerce 10.0.10 en hoger is de bewerking **Leveringsmethode wijzigen** (647) beschikbaar om aan uw POS-schermindelingen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c313e-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="c313e-106">De functie Leveringsmethode wijzigen biedt u de optie om de leveringsmethode te wijzigen voor een of meer voor verkoop geconfigureerde verkoopregels in de POS-transactie.</span><span class="sxs-lookup"><span data-stu-id="c313e-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="c313e-107">In eerdere versies van Commerce moest u de volledige configuratiestromen **Alles verzenden** of **Selectie verzenden** doorlopen als u de leveringsmethode wilde wijzigen voor een bestaande regel die voor verzending was geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="c313e-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="c313e-108">Dit proces was tijdrovend en kon leiden tot onbedoelde wijzigingen in de leveringsoorsprong of leveringsdatums voor de regel.</span><span class="sxs-lookup"><span data-stu-id="c313e-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="c313e-109">De nieuwe functionaliteit biedt een alternatieve methode voor het efficiënt bijwerken van de leveringsmethode op deze verkoopregels.</span><span class="sxs-lookup"><span data-stu-id="c313e-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="c313e-110">Zie [Schermindelingen voor het verkooppunt](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) voor meer informatie over het toevoegen van een bewerking aan een knop in uw POS-knoppenraster.</span><span class="sxs-lookup"><span data-stu-id="c313e-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="c313e-111">Wanneer deze functie is geconfigureerd in POS en u **Leveringsmethode wijzigen** selecteert, wordt er een lijstpagina weergegeven waarop u de regels kunt kiezen van de transactie waarvoor u de leveringsmethode wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c313e-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="c313e-112">U kunt enkele of alle regels kiezen of afsluiten zonder wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="c313e-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="c313e-113">De verkoopregels die eerder waren geconfigureerd voor verzending, zijn de enige regels in de lijst die u kunt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c313e-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="c313e-114">Als u een regel wilt wijzigen die is toegewezen voor ophalen of uitvoeren voor verzending, moet u de bewerking **Alles verzenden** of **Selectie verzenden** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c313e-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="c313e-115">Als u daarentegen een regel wilt wijzigen die is aangewezen voor ophalen of uitvoering, moet u de bewerking **Alles ophalen**, **Selectie ophalen**, **Alles uitvoeren** of **Selectie uitvoeren** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c313e-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="c313e-116">Nadat u de regels hebt geselecteerd die u wilt wijzigen, klikt u op **Leveringsmethode wijzigen** om te worden gevraagd de opties voor de leveringsmethode te selecteren.</span><span class="sxs-lookup"><span data-stu-id="c313e-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="c313e-117">Als u meerdere regels hebt geselecteerd om te wijzigen, worden in POS alleen leveringsmethoden weergegeven die zijn geconfigureerd als toegestaan voor alle geselecteerde producten.</span><span class="sxs-lookup"><span data-stu-id="c313e-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="c313e-118">Leveringsmethoden kunnen worden geconfigureerd voor de ondersteuning van specifieke producten en leveringsadressen.</span><span class="sxs-lookup"><span data-stu-id="c313e-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="c313e-119">Als er een leveringsmethode is die acceptabel is voor één combinatie van product en adres, maar die niet acceptabel is voor een andere geselecteerde combinatie van product en adres, is de leveringsmethode niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="c313e-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="c313e-120">U moet mogelijk regels één voor één selecteren en de leveringsmethode voor elke regel afzonderlijk wijzigen als u een leveringsmethode wilt selecteren voor een product dat niet door een ander product wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="c313e-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="c313e-121">Nadat u de nieuwe leveringsmethode hebt geselecteerd, wordt de transactiepagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c313e-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="c313e-122">Als u de nieuwe selecties voor de leveringsmethode wilt controleren, selecteert u het tabblad **Levering** in de transactielijst.</span><span class="sxs-lookup"><span data-stu-id="c313e-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c313e-123">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c313e-123">Additional resources</span></span>

[<span data-ttu-id="c313e-124">Callcenterorders maken</span><span class="sxs-lookup"><span data-stu-id="c313e-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="c313e-125">Transactionele e-mails aanpassen per leveringsmethode</span><span class="sxs-lookup"><span data-stu-id="c313e-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)
