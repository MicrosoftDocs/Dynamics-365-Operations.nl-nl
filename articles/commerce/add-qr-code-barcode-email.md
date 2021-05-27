---
title: Een QR-code of streepjescode toevoegen aan transactionele e-mails en ontvangstberichten
description: In dit onderwerp wordt uitgelegd hoe u QR-codes en streepjescodes die order-id's vertegenwoordigen kunt invoegen in transactionele e-mails en ontvangstberichten in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9eea69f9618d4387f5d6320620dfee5d74813fc0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019534"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="25f5e-103">Een QR-code of streepjescode toevoegen aan transactionele e-mails en ontvangstberichten</span><span class="sxs-lookup"><span data-stu-id="25f5e-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="25f5e-104">In dit onderwerp wordt uitgelegd hoe u QR-codes en streepjescodes die order-id's vertegenwoordigen kunt invoegen in transactionele e-mails en ontvangstberichten in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="25f5e-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="25f5e-105">U kunt eenvoudig QR-codes en streepjescodes in transactionele e-mails opnemen, zodat het opzoekproces voor orders in een detailhandelomgeving wordt versneld.</span><span class="sxs-lookup"><span data-stu-id="25f5e-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="25f5e-106">Als u QR-codes en streepjescodes wilt invoegen in e-mails, gebruikt u een HTML **\<img\>**-code waarin wordt gevraagd om een QR-code of streepjescodeafbeelding van een generatie- en renderingservice.</span><span class="sxs-lookup"><span data-stu-id="25f5e-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="25f5e-107">Microsoft levert deze service niet.</span><span class="sxs-lookup"><span data-stu-id="25f5e-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="25f5e-108">Er bestaat echter een groot aantal gratis of voordelige services waarmee u QR-codes of streepjescodes kunt gebruiken die dynamisch worden gegenereerd op basis van een waarde die wordt doorgegeven in een queryreeks.</span><span class="sxs-lookup"><span data-stu-id="25f5e-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="25f5e-109">Een QR-code of streepjescode toevoegen aan een transactionele e-mail</span><span class="sxs-lookup"><span data-stu-id="25f5e-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="25f5e-110">Volg deze stappen om een QR-code of streepjescode in te voegen in een transactioneel e-mailbericht dat als onderdeel van een e-commerce-aankoop wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="25f5e-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="25f5e-111">Open de bron-HTML voor de transactionele e-mailsjabloon en voeg een HTML **\<img\>**-code toe die naar uw QR-code- of streepjescodeservice wijst.</span><span class="sxs-lookup"><span data-stu-id="25f5e-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="25f5e-112">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="25f5e-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="25f5e-113">Hier volgt een uitleg van het voorafgaande voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="25f5e-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="25f5e-114">**UW\_QR\_CODE\_STREEPJES\_CODE\_SERVICE** stelt het domein van uw QR-code- of streepjescodeservice voor.</span><span class="sxs-lookup"><span data-stu-id="25f5e-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="25f5e-115">**gegevens** vertegenwoordigt de parameter die door de QR-code- of streepjescodeservice wordt gebruikt voor de ontvangst van de inhoud die moet worden weergegeven als QR-code of streepjescode.</span><span class="sxs-lookup"><span data-stu-id="25f5e-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="25f5e-116">De waarde **%salesid%** moet aan deze parameter worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="25f5e-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="25f5e-117">In dit voorbeeld wordt de waarde ook gebruikt als alt-tekst voor de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="25f5e-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="25f5e-118">**param1** en **param2** staan voor extra optionele parameters.</span><span class="sxs-lookup"><span data-stu-id="25f5e-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="25f5e-119">Ga naar **Retail en commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen van organisatie** en upload de bijgewerkte HTML naar de juiste transactionele e-mailsjabloon.</span><span class="sxs-lookup"><span data-stu-id="25f5e-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="25f5e-120">De parameters kunnen per provider verschillen voor de QR-code- en streepjescodeservice.</span><span class="sxs-lookup"><span data-stu-id="25f5e-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="25f5e-121">Neem daarom contact op met uw serviceprovider om de parameters te bevestigen waaraan u waarden moet toewijzen.</span><span class="sxs-lookup"><span data-stu-id="25f5e-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="25f5e-122">Een QR-code of streepjescode toevoegen aan een ontvangstbericht</span><span class="sxs-lookup"><span data-stu-id="25f5e-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="25f5e-123">Volg deze stappen om een QR-code of streepjescode in te voegen in een ontvangstbericht dat kan worden verzonden nadat een inkoop op het POS is gedaan.</span><span class="sxs-lookup"><span data-stu-id="25f5e-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="25f5e-124">Open de bron-HTML voor de e-mailsjabloon voor ontvangstbericht en voeg een HTML **\<img\>**-code toe die naar uw QR-code- of streepjescodeservice wijst.</span><span class="sxs-lookup"><span data-stu-id="25f5e-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="25f5e-125">Hieronder volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="25f5e-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="25f5e-126">Hier volgt een uitleg van het voorafgaande voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="25f5e-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="25f5e-127">**UW\_QR\_CODE\_STREEPJES\_CODE\_SERVICE** stelt het domein van uw QR-code- of streepjescodeservice voor.</span><span class="sxs-lookup"><span data-stu-id="25f5e-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="25f5e-128">**gegevens** vertegenwoordigt de parameter die door de QR-code- of streepjescodeservice wordt gebruikt voor de ontvangst van de inhoud die moet worden weergegeven als QR-code of streepjescode.</span><span class="sxs-lookup"><span data-stu-id="25f5e-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="25f5e-129">De waarde **%receiptid%** moet aan deze parameter worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="25f5e-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="25f5e-130">In dit voorbeeld wordt de waarde ook gebruikt als alt-tekst voor de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="25f5e-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="25f5e-131">**param1** en **param2** staan voor extra optionele parameters.</span><span class="sxs-lookup"><span data-stu-id="25f5e-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="25f5e-132">Ga naar **Retail en commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen van organisatie** en upload de bijgewerkte HTML naar de e-mailsjabloon met de e-mail-id **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="25f5e-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="25f5e-133">De parameters kunnen per provider verschillen voor de QR-code- en streepjescodeservice.</span><span class="sxs-lookup"><span data-stu-id="25f5e-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="25f5e-134">Neem daarom contact op met uw serviceprovider om de parameters te bevestigen waaraan u waarden moet toewijzen.</span><span class="sxs-lookup"><span data-stu-id="25f5e-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25f5e-135">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="25f5e-135">Additional resources</span></span>

[<span data-ttu-id="25f5e-136">E-mailontvangstbewijzen verzenden vanuit Modern POS</span><span class="sxs-lookup"><span data-stu-id="25f5e-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="25f5e-137">E-mailsjablonen maken voor transactiegebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="25f5e-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
