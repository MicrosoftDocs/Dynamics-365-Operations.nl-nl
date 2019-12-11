---
title: Een favicon toevoegen
description: In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696986"
---
# <a name="add-a-favicon"></a><span data-ttu-id="dbe4c-103">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="dbe4c-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="dbe4c-104">In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="dbe4c-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="dbe4c-105">Overview</span></span>

<span data-ttu-id="dbe4c-106">Een favicon is een klein grafisch bestand dat onder andere wordt weergegeven op het tabblad van de webbrowser, in de adresbalk, de browsergeschiedenis en in bladwijzers of favorieten.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="dbe4c-107">Het is raadzaam om een favicon aan uw site toe te voegen, omdat deze uw merk vertegenwoordigt en benadrukt. Zo onderscheidt uw site zich van andere sites die uw klant bezoekt.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="dbe4c-108">Hoewel u meerdere favicons van verschillende grootten en bestandstypen kunt toevoegen aan uw site, wordt in dit onderwerp aangegeven hoe u één favicon toevoegt.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="dbe4c-109">Hetzelfde proces en dezelfde locatie worden echter gebruikt om meer favicons toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="dbe4c-110">Een favicon uploaden naar de verzameling met assets voor uw site</span><span class="sxs-lookup"><span data-stu-id="dbe4c-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="dbe4c-111">Volg deze stappen om een favicon te uploaden naar de verzameling met assets voor uw site.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="dbe4c-112">Ga naar **Activa \> Uploaden \> Activa uploaden**.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="dbe4c-113">Zoek en selecteer de favicon op het lokale bestandssysteem.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="dbe4c-114">Voer een titel in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="dbe4c-115">Kopieer in het eigenschappenvenster aan de rechterkant de openbare URL van de favicon.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="dbe4c-116">Als u niet de optie **Activa publiceren na upload** selecteert, moet u teruggaan naar de pagina **Activa** en de favicon later handmatig publiceren.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="dbe4c-117">De HTML voor de favicon maken</span><span class="sxs-lookup"><span data-stu-id="dbe4c-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="dbe4c-118">Gebruik het volgende HTML-fragment om de HTML voor de favicon te maken.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="dbe4c-119">Vervang voor het kenmerk **href** de **"Openbare\_URL\_voor\_uw\_favicon"** door de openbare URL die u eerder hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="dbe4c-120">De HTML voor de favicon toevoegen aan het element \<head\> van uw pagina's</span><span class="sxs-lookup"><span data-stu-id="dbe4c-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="dbe4c-121">Als u een favicon aan uw site wilt toevoegen, gebruikt u dezelfde procedure als wordt gebruikt om elk type HTML of script toe te voegen aan het element **\<head\>** van de sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="dbe4c-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbe4c-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="dbe4c-122">Additional resources</span></span>

[<span data-ttu-id="dbe4c-123">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="dbe4c-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="dbe4c-124">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="dbe4c-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="dbe4c-125">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="dbe4c-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="dbe4c-126">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="dbe4c-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="dbe4c-127">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="dbe4c-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="dbe4c-128">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="dbe4c-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

