---
title: Clientwaarschuwingen per e-mail
description: Dit onderwerp biedt informatie over het instellen van regels die e-mailberichten verzenden wanneer vooraf gedefinieerde gebeurtenissen optreden.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9545731af20a96c322b4e92c17f3a46b7077295b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546957"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="eabec-103">Clientwaarschuwingen per e-mail</span><span class="sxs-lookup"><span data-stu-id="eabec-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="eabec-104">In Microsoft Dynamics 365 for Finance and Operations kunt u aangepaste waarschuwingsregels definiëren die gefilterde weergaven van gegevens controleren en automatisch e-mailberichten verzenden wanneer vooraf gedefinieerde gebeurtenissen plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="eabec-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="eabec-105">De optie voor het verzenden van e-mailmeldingen is beschikbaar voor alle ondersteunde typen waarschuwingen en kan ook worden ingeschakeld voor bestaande waarschuwingsregels.</span><span class="sxs-lookup"><span data-stu-id="eabec-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="eabec-106">U kunt ingebouwde besturingselementen gebruiken om waarschuwingsregels te maken die de gefilterde weergaven van systeembatchtaken controleren.</span><span class="sxs-lookup"><span data-stu-id="eabec-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="eabec-107">Door de waarde te controleren van het veld **Status** kunt u ook waarschuwingsregels configureren die e-mail verzenden wanneer een batchtaak mislukt.</span><span class="sxs-lookup"><span data-stu-id="eabec-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="eabec-108">Nadat deze waarschuwingsregels zijn gemaakt, hoeft u niet langer rapporten te controleren op wijzigingen in zakelijke gegevens.</span><span class="sxs-lookup"><span data-stu-id="eabec-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="eabec-109">In plaats daarvan kunt u de intelligente wijzigingsdetectieservice van Finance and Operations deze controle voor u laten uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="eabec-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="eabec-110">Clientwaarschuwingen,zijn afhankelijk van het e-mailsubsysteem dat wordt geleverd via integratie met Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="eabec-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="eabec-111">We raden aan dat u de SMTP-provider (Simple Mail Transfer Protocol) gebruikt, zodat e-distributie niet hoeft te vertrouwen op een lokale e-mailclient.</span><span class="sxs-lookup"><span data-stu-id="eabec-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="eabec-112">Om meldingen te verzenden per e-mail moeten klanten geïntegreerde e-mailservices configureren.</span><span class="sxs-lookup"><span data-stu-id="eabec-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="eabec-113">E-mailberichten worden verzonden naar ontvangers namens de eigenaren van waarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="eabec-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="eabec-114">Zie voor meer informatie over het configureren van e-mail in Finance and Operations [E-mail configureren en verzenden](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="eabec-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="eabec-115">In de volgende afbeelding ziet u het dialoogvenster **Waarschuwingsregel maken**, dat nu een optie **E-mail verzenden** bevat.</span><span class="sxs-lookup"><span data-stu-id="eabec-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="eabec-116">[![Dialoogvenster Waarschuwingsregel maken met de optie E-mail verzenden ingesteld op Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="eabec-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="eabec-117">Wanneer de optie **E-mail verzenden** is ingesteld op **Ja**, blijven waarschuwingen afgeleverd worden vanuit het actiecentrum.</span><span class="sxs-lookup"><span data-stu-id="eabec-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="eabec-118">Sjablonen voor e-mails met waarschuwingsberichten</span><span class="sxs-lookup"><span data-stu-id="eabec-118">Alert notification email templates</span></span>

<span data-ttu-id="eabec-119">De service verzendt e-mailberichten met behulp van vooraf gedefinieerde e-mailsjablonen die de basisgegevens van het waarschuwingsbericht leveren.</span><span class="sxs-lookup"><span data-stu-id="eabec-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="eabec-120">De volgende afbeelding toont de structuur van de waarschuwingsberichten die per e-mail worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="eabec-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="eabec-121">[![Waarschuwingsberichten op basis van een sjabloon voor maken van records, veldwijzigingen en sjabloonverwijdering](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="eabec-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
