---
title: Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom
description: U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "344588"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="91108-103">Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom</span><span class="sxs-lookup"><span data-stu-id="91108-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91108-104">U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.</span><span class="sxs-lookup"><span data-stu-id="91108-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="91108-105">Er kan bijvoorbeeld een e-mailbericht naar een gebruiker worden verzonden wanneer deze een document voor goedkeuring toegewezen krijgt.</span><span class="sxs-lookup"><span data-stu-id="91108-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="91108-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="91108-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="91108-107">Ga naar Systeembeheer > Gebruikers > Gebruikers.</span><span class="sxs-lookup"><span data-stu-id="91108-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="91108-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="91108-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="91108-109">Klik op Gebruikersopties.</span><span class="sxs-lookup"><span data-stu-id="91108-109">Click User options.</span></span>
4. <span data-ttu-id="91108-110">Klik op het tabblad Workflow.</span><span class="sxs-lookup"><span data-stu-id="91108-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="91108-111">Zorg ervoor dat de sectie Meldingen is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="91108-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="91108-112">Geef in de sectie Melding op, hoe u wilt dat de gebruiker geïnformeerd wordt over werkstroom-gerelateerde zaken.</span><span class="sxs-lookup"><span data-stu-id="91108-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="91108-113">Selecteer een optie in het veld Meldingtype workflow voor regelartikelen.</span><span class="sxs-lookup"><span data-stu-id="91108-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="91108-114">Gegroepeerd: Regelartikelmeldingen worden gegroepeerd tot één e-mailbericht.</span><span class="sxs-lookup"><span data-stu-id="91108-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="91108-115">Individueel: Een e-mailbericht wordt verzonden voor elk regelartikel.</span><span class="sxs-lookup"><span data-stu-id="91108-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="91108-116">Als u wilt dat de gebruiker meldingen ontvangt in de client, vinkt u het selectievakje Meldingen verzenden in e-mail aan.</span><span class="sxs-lookup"><span data-stu-id="91108-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="91108-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="91108-117">Click Save.</span></span>
7. <span data-ttu-id="91108-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="91108-118">Close the page.</span></span>

