---
title: Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom
description: U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 221e38cbe31e2ad24a56cb2e71206a1ebcdd619e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798999"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="37a65-103">Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom</span><span class="sxs-lookup"><span data-stu-id="37a65-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37a65-104">U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.</span><span class="sxs-lookup"><span data-stu-id="37a65-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="37a65-105">Er kan bijvoorbeeld een e-mailbericht naar een gebruiker worden verzonden wanneer deze een document voor goedkeuring toegewezen krijgt.</span><span class="sxs-lookup"><span data-stu-id="37a65-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="37a65-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="37a65-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="37a65-107">Ga naar **Navigatievenster > Modules > Systeembeheer > Gebruikers > Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="37a65-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="37a65-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="37a65-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37a65-109">Klik in het **actievenster** op **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="37a65-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="37a65-110">Klik op het tabblad **Workflow**. Controleer of de sectie **Meldingen** is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="37a65-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="37a65-111">Geef in de sectie **Meldingen** op hoe de gebruiker geïnformeerd moet worden over zaken die betrekking hebben op workflows.</span><span class="sxs-lookup"><span data-stu-id="37a65-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="37a65-112">Selecteer een optie in het veld **Meldingtype workflow voor regelartikelen**.</span><span class="sxs-lookup"><span data-stu-id="37a65-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="37a65-113">Gegroepeerd: Regelartikelmeldingen worden gegroepeerd tot één e-mailbericht.</span><span class="sxs-lookup"><span data-stu-id="37a65-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="37a65-114">Individueel: Een e-mailbericht wordt verzonden voor elk regelartikel.</span><span class="sxs-lookup"><span data-stu-id="37a65-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="37a65-115">Als u wilt dat de gebruiker meldingen ontvangt in de client, schakelt u het selectievakje **Meldingen verzenden in e-mail** in.</span><span class="sxs-lookup"><span data-stu-id="37a65-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="37a65-116">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="37a65-116">Click **Save**.</span></span>
7. <span data-ttu-id="37a65-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="37a65-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="37a65-118">De e-mailsjablonen voor workflows zijn e-mailsjablonen van het systeem of de organisatie, afhankelijk van of de workflow van systeemniveau (bedrijfsspecifiek) of organisatieniveau (bedrijfsspecifieke) is.</span><span class="sxs-lookup"><span data-stu-id="37a65-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>
