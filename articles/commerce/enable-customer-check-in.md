---
title: Incheckmeldingen van klanten in Point of Sale (POS) inschakelen
description: In dit onderwerp wordt beschreven hoe u incheckmeldingen voor klanten in het Microsoft Dynamics 365 Commerce POS kunt inschakelen.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937573"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="124b1-103">Incheckmeldingen van klanten in Point of Sale (POS) inschakelen</span><span class="sxs-lookup"><span data-stu-id="124b1-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="124b1-104">In dit onderwerp wordt beschreven hoe u incheckmeldingen voor klanten in het Microsoft Dynamics 365 Commerce POS kunt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="124b1-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="124b1-105">In hun e-mails voor 'Order gereed voor ophalen' kunnen organisaties een koppeling of knop bieden, waarmee klanten aan de winkel kunnen melden dat ze zich op het terrein bevinden en wachten tot hun pakket naar hen wordt gebracht.</span><span class="sxs-lookup"><span data-stu-id="124b1-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="124b1-106">Klanten ontvangen vervolgens een incheckbevestiging en de winkel ontvangt een melding als een taak in de POS-toepassing.</span><span class="sxs-lookup"><span data-stu-id="124b1-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="124b1-107">Deze taak dient als aansporing voor een verkoopmedewerker om de order af te geven bij het voertuig van de klant.</span><span class="sxs-lookup"><span data-stu-id="124b1-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="124b1-108">Zo hoeft de klant de winkel niet in te komen.</span><span class="sxs-lookup"><span data-stu-id="124b1-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="124b1-109">De workflow voor het inchecken van klanten kan ook worden geconfigureerd om extra informatie te verzamelen van klanten, zoals het nummer van de parkeerplaats, het merk, model en de kleur van de voertuig en instructies voor het afleveren.</span><span class="sxs-lookup"><span data-stu-id="124b1-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="124b1-110">Met deze informatie kan de winkelmedewerker de afhandeling van de order bespoedigen.</span><span class="sxs-lookup"><span data-stu-id="124b1-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="124b1-111">Klantincheck inschakelen</span><span class="sxs-lookup"><span data-stu-id="124b1-111">Enable customer check-in</span></span>

<span data-ttu-id="124b1-112">Wanneer de functie voor klantincheck is ingeschakeld, genereert Commerce een orderbevestigings-id (ook wel de afzetkanaalverwijzings-id genoemd).</span><span class="sxs-lookup"><span data-stu-id="124b1-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="124b1-113">Daarnaast worden orderbevestigings-id's gegenereerd voor orders die zijn gemaakt via kanalen POS of callcenter.</span><span class="sxs-lookup"><span data-stu-id="124b1-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="124b1-114">Als u de functie voor klantincheck wilt inschakelen in Commerce Headquarters, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="124b1-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="124b1-115">Ga naar **Werkgebieden \> Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="124b1-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="124b1-116">Zoek de functie **Consistente indeling van de kanaalverwijzings-id genereren voor alle kanalen**.</span><span class="sxs-lookup"><span data-stu-id="124b1-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="124b1-117">Selecteer de functie en selecteer vervolgens **Nu inschakelen** in het het deelvenster Eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="124b1-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="124b1-118">Een pagina voor incheckbevestiging maken</span><span class="sxs-lookup"><span data-stu-id="124b1-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="124b1-119">In uw webwinkel moet u een nieuwe pagina maken waarop u het inchecken kunt bevestigen.</span><span class="sxs-lookup"><span data-stu-id="124b1-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="124b1-120">Met extra configuratie kan de pagina ook een formulier bevatten dat extra informatie van klanten verzamelt, om de afhandeling van de order te bespoedigen.</span><span class="sxs-lookup"><span data-stu-id="124b1-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="124b1-121">Meer informatie over het instellen van de pagina en de module vindt u in [De module Klantincheck](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="124b1-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="124b1-122">De transactionele e-mailsjabloon configureren</span><span class="sxs-lookup"><span data-stu-id="124b1-122">Configure the transactional email template</span></span>

<span data-ttu-id="124b1-123">U moet een koppeling of knop **Ik ben er** toevoegen aan de sjabloon voor de transactie-e-mail die klanten ontvangen wanneer de order klaar is om te worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="124b1-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="124b1-124">Klanten gebruiken deze koppeling of knop om de winkel te laten weten dat ze er zijn om hun bestelling af te halen.</span><span class="sxs-lookup"><span data-stu-id="124b1-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="124b1-125">Voeg de koppeling of knop toe aan de sjabloon die is gekoppeld aan het meldingstype **Inpakken voltooid** en de leveringsmodus die u gebruikt voor het laten afhalen van bestellingen bij een afhaalpunt.</span><span class="sxs-lookup"><span data-stu-id="124b1-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="124b1-126">Maak in de sjabloon een HTML-koppeling of knop die verwijst naar de URL van de pagina voor het bevestigen van het inchecken die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="124b1-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="124b1-127">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="124b1-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="124b1-128">Meer informatie over het configureren van e-mailsjablonen vindt u in [Transactionele e-mails aanpassen per leveringsmethode](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="124b1-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="124b1-129">In POS wordt een incheckbevestigingstaak gemaakt</span><span class="sxs-lookup"><span data-stu-id="124b1-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="124b1-130">Nadat een klant de winkel heeft laten weten dat hij of zij er is om de bestelling af te halen, ontvangt hij of zij een bevestigingsmelding voor het inchecken en wordt een taak gemaakt in de takenlijst in POS voor de winkel waar de klant de order afhaalt.</span><span class="sxs-lookup"><span data-stu-id="124b1-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="124b1-131">De taak bevat alle klant- en ordergegevens die nodig zijn om de order af te handelen.</span><span class="sxs-lookup"><span data-stu-id="124b1-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="124b1-132">In de taak bevat het veld Instructies alle gegevens die via het formulier voor aanvullende informatie van de klant zijn verzameld.</span><span class="sxs-lookup"><span data-stu-id="124b1-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="124b1-133">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="124b1-133">Additional resources</span></span>

[<span data-ttu-id="124b1-134">De module Inchecken voor ophalen</span><span class="sxs-lookup"><span data-stu-id="124b1-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
