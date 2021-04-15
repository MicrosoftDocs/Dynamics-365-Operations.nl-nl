---
title: Transactionele e-mails aanpassen per leveringsmethode
description: In dit onderwerp wordt beschreven hoe u aangepaste e-mailsjablonen instelt voor specifieke meldingstypen en leveringsmethoden in Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 411e694b33e0443a336f6a8cdad78714630e4bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799368"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="c7599-103">Transactionele e-mails aanpassen per leveringsmethode</span><span class="sxs-lookup"><span data-stu-id="c7599-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7599-104">In dit onderwerp wordt beschreven hoe u aangepaste e-mailsjablonen instelt voor specifieke meldingstypen en leveringsmethoden in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7599-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c7599-105">Transactionele e-mails kunnen nu worden aangepast voor een combinatie van een meldingstype (bijvoorbeeld **Bestelling gemaakt**, **Bestelling verpakt** of **Bestelling gefactureerd**) en een leveringsmethode (bijvoorbeeld nacht, afhalen in de winkel of afhalen bij een specifieke locatie).</span><span class="sxs-lookup"><span data-stu-id="c7599-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="c7599-106">Aangepaste transactionele e-mails zorgen ervoor dat detailhandelaren hun klantenbestellingen kunnen afhandelen op een manier die is afgestemd op de leveringsmethode van de bestelling.</span><span class="sxs-lookup"><span data-stu-id="c7599-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="c7599-107">De gebeurtenis 'Bestelling verpakt' kan bijvoorbeeld worden aangepast, zodat er instructies volgen voor klanten die afhalen op een specifieke locatie.</span><span class="sxs-lookup"><span data-stu-id="c7599-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="c7599-108">Ook kunnen er vervoerders- en leveringsgegevens worden geleverd voor klanten die ervoor kiezen hun bestelling te verzenden.</span><span class="sxs-lookup"><span data-stu-id="c7599-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="c7599-109">Als u de functionaliteit voor aangepaste transactionele e-mails wilt gebruiken, moet u eerst de optie **Transactionele e-mailsjablonen aanpassen per leveringsmethode** inschakelen door naar **Werkruimten \> Functiebeheer** in Commerce Headquarters te gaan.</span><span class="sxs-lookup"><span data-stu-id="c7599-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="c7599-110">E-mails kunnen worden aangepast op basis van de leveringsmethode voor de volgende meldingstypen:</span><span class="sxs-lookup"><span data-stu-id="c7599-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="c7599-111">**Bestelling geannuleerd** : dit type e-mailmelding is nieuw.</span><span class="sxs-lookup"><span data-stu-id="c7599-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="c7599-112">**Order gemaakt**</span><span class="sxs-lookup"><span data-stu-id="c7599-112">**Order created**</span></span>
- <span data-ttu-id="c7599-113">**Order is bevestigd**</span><span class="sxs-lookup"><span data-stu-id="c7599-113">**Order confirmed**</span></span>
- <span data-ttu-id="c7599-114">**Bestelling gefactureerd** : dit type e-mailmelding is nieuw.</span><span class="sxs-lookup"><span data-stu-id="c7599-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="c7599-115">Deze kan worden gebruikt in plaats van de melding **Bestelling verzonden** waarmee een melding wordt verzonden voor elke factuur die een leveringsmethode heeft (niet ophalen, uitvoeren of elektronische leveringsmethode).</span><span class="sxs-lookup"><span data-stu-id="c7599-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="c7599-116">**Bestelling opgezocht**</span><span class="sxs-lookup"><span data-stu-id="c7599-116">**Order picked**</span></span>
- <span data-ttu-id="c7599-117">**Bestelling verpakt**</span><span class="sxs-lookup"><span data-stu-id="c7599-117">**Order packed**</span></span>
- <span data-ttu-id="c7599-118">**Bestelling klaar voor ophalen** : dit type melding kan alleen worden aangepast aan de hand van de leveringsmethode als de functie **Ondersteuning voor meerdere ophaalmethodes** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c7599-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="c7599-119">In dat geval is dit meldingstype functioneel equivalent aan het meldingstype **Bestelling verpakt**.</span><span class="sxs-lookup"><span data-stu-id="c7599-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="c7599-120">**Betaling is mislukt**</span><span class="sxs-lookup"><span data-stu-id="c7599-120">**Payment failed**</span></span>
- <span data-ttu-id="c7599-121">**Vervangingsorder is gemaakt**</span><span class="sxs-lookup"><span data-stu-id="c7599-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="c7599-122">E-mailsjablonen configureren voor specifieke leveringsmethoden</span><span class="sxs-lookup"><span data-stu-id="c7599-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="c7599-123">Voor deze procedure is de veronderstelling dat u uw nieuwe, aangepaste e-mailsjablonen al hebt gemaakt en deze aan de pagina **E-mailsjablonen van organisatie** hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7599-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="c7599-124">Zie [E-mailsjablonen maken voor transactiegebeurtenissen](email-templates-transactions.md) voor informatie over het maken en uploaden van e-mailsjablonen.</span><span class="sxs-lookup"><span data-stu-id="c7599-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="c7599-125">Volg de volgende stappen om e-mailsjablonen te configureren voor specifieke leveringsmethoden in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c7599-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c7599-126">Ga naar **E-mailmeldingsprofiel voor Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c7599-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="c7599-127">Selecteer onder **Instellingen voor melding detailhandelgebeurtenissen** een bestaand meldingstype.</span><span class="sxs-lookup"><span data-stu-id="c7599-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="c7599-128">Terwijl het meldingstype nog steeds is geselecteerd, selecteert u **Leveringsmethoden configureren**.</span><span class="sxs-lookup"><span data-stu-id="c7599-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="c7599-129">In het dialoogvenster **Leveringsmethoden** selecteert u **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c7599-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="c7599-130">Selecteer in de nieuwe rij, in het veld **Leveringsmethode** de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="c7599-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="c7599-131">Selecteer in het veld **e-mail-id** het e-mailsjabloon waaraan u de leveringsmethode wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="c7599-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="c7599-132">Schakel het selectievakje **Actief** in.</span><span class="sxs-lookup"><span data-stu-id="c7599-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="c7599-133">Herhaal stappen 4 tot en met 7 om meer leveringsmethoden toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c7599-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="c7599-134">Wanneer u klaar bent, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7599-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="c7599-135">Als er meer dan één leveringsmethode aanwezig is in een verkooporder, wordt het standaardsjabloon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c7599-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="c7599-136">Het standaardsjabloon is het sjabloon dat is toegewezen aan het meldingstype op de pagina **E-mailmeldingsprofiel voor Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c7599-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="c7599-137">Als een verkooporder een leveringsmethode heeft die niet is geconfigureerd voor een aangepast e-mailsjabloon, wordt het standaard e-mailsjabloon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c7599-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7599-138">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c7599-138">Additional resources</span></span>

[<span data-ttu-id="c7599-139">Callcenterorders maken</span><span class="sxs-lookup"><span data-stu-id="c7599-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="c7599-140">Leveringsmethode wijzigen in POS</span><span class="sxs-lookup"><span data-stu-id="c7599-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]