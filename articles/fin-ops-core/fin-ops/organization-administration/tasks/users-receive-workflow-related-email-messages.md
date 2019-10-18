---
title: Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom
description: U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189839"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="b8998-103">Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom</span><span class="sxs-lookup"><span data-stu-id="b8998-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8998-104">U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.</span><span class="sxs-lookup"><span data-stu-id="b8998-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="b8998-105">Er kan bijvoorbeeld een e-mailbericht naar een gebruiker worden verzonden wanneer deze een document voor goedkeuring toegewezen krijgt.</span><span class="sxs-lookup"><span data-stu-id="b8998-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="b8998-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="b8998-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b8998-107">Ga naar **Navigatievenster > Modules > Systeembeheer > Gebruikers > Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="b8998-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="b8998-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b8998-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b8998-109">Klik in het **actievenster** op **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="b8998-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="b8998-110">Klik op het tabblad **Workflow**. Controleer of de sectie **Meldingen** is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="b8998-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="b8998-111">Geef in de sectie **Meldingen** op hoe de gebruiker geïnformeerd moet worden over zaken die betrekking hebben op workflows.</span><span class="sxs-lookup"><span data-stu-id="b8998-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="b8998-112">Selecteer een optie in het veld **Meldingtype workflow voor regelartikelen**.</span><span class="sxs-lookup"><span data-stu-id="b8998-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="b8998-113">Gegroepeerd: Regelartikelmeldingen worden gegroepeerd tot één e-mailbericht.</span><span class="sxs-lookup"><span data-stu-id="b8998-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="b8998-114">Individueel: Een e-mailbericht wordt verzonden voor elk regelartikel.</span><span class="sxs-lookup"><span data-stu-id="b8998-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="b8998-115">Als u wilt dat de gebruiker meldingen ontvangt in de client, schakelt u het selectievakje **Meldingen verzenden in e-mail** in.</span><span class="sxs-lookup"><span data-stu-id="b8998-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="b8998-116">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b8998-116">Click **Save**.</span></span>
7. <span data-ttu-id="b8998-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8998-117">Close the page.</span></span>

