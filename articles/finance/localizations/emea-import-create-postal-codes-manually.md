---
title: Postcodes importeren of handmatig maken
description: In dit onderwerp wordt beschreven hoe u postcodes in de juiste indeling importeert en handmatig maakt.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LogisticsAddressSetup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 29901
ms.search.region: Belgium, Netherlands, Sweden
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9663c956ed51b862b86e44094a60d0907d3a1647
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183822"
---
# <a name="import-or-manually-create-postal-codes"></a><span data-ttu-id="858ed-103">Postcodes importeren of handmatig maken</span><span class="sxs-lookup"><span data-stu-id="858ed-103">Import or manually create postal codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="858ed-104">In dit onderwerp wordt beschreven hoe u postcodes in de juiste indeling importeert en handmatig maakt.</span><span class="sxs-lookup"><span data-stu-id="858ed-104">This topic explains how to import and manually create postal codes in the correct format.</span></span> 

<span data-ttu-id="858ed-105">Met het importproces kunt u de postcodes voor een bepaald land of een bepaalde regio bijwerken.</span><span class="sxs-lookup"><span data-stu-id="858ed-105">The import process lets you update the ZIP/postal codes for a specific country/region.</span></span> <span data-ttu-id="858ed-106">U kunt postcodes ook handmatig maken.</span><span class="sxs-lookup"><span data-stu-id="858ed-106">You can also create postal codes manually.</span></span>

## <a name="import-zippostal-codes"></a><span data-ttu-id="858ed-107">Postcodes importeren</span><span class="sxs-lookup"><span data-stu-id="858ed-107">Import ZIP/postal codes</span></span>
<span data-ttu-id="858ed-108">U kunt de pagina **Postcodes importeren** gebruiken om nieuwe postcodes in Dynamics 365 Finance te importeren.</span><span class="sxs-lookup"><span data-stu-id="858ed-108">You can use the **Import ZIP/postal codes** page to import new postal codes into Dynamics 365 Finance.</span></span> <span data-ttu-id="858ed-109">Wanneer u de codes importeert, worden de bestaande postcodes door de nieuwe indeling vervangen en worden eventuele nieuwe codes toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="858ed-109">When you import the codes, the existing ZIP or postal codes are replaced with the new format, and any new codes are added.</span></span>

<span data-ttu-id="858ed-110">Voor sommige landen moet u het Gegevensbeheer-raamwerk gebruiken om codes te importeren, terwijl voor andere landen alleen een uploadbestand vereist is.</span><span class="sxs-lookup"><span data-stu-id="858ed-110">For some countries, you must use the Data management framework to import codes, while for other countries only an upload file is required.</span></span> <span data-ttu-id="858ed-111">Voor België, Nederland en Zweden moet een bestand worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="858ed-111">Belgium, Netherlands, and Sweden require a file to upload.</span></span>

> [!NOTE]
> -   <span data-ttu-id="858ed-112">Voor België bevat de officiële webpagina van de Belgische Post een officiële lijst van de postcodes en de bijbehorende plaatsnamen.</span><span class="sxs-lookup"><span data-stu-id="858ed-112">For Belgium, the official webpage from the Belgian Post provides an official list of the postcodes and the corresponding city names.</span></span> <span data-ttu-id="858ed-113">HTML-bestandsindeling wordt ondersteund voor het importeren.</span><span class="sxs-lookup"><span data-stu-id="858ed-113">The import supports html file format.</span></span>
> -   <span data-ttu-id="858ed-114">Voor Nederland levert een externe organisatie het bestand dat postcodes bevat.</span><span class="sxs-lookup"><span data-stu-id="858ed-114">For Netherlands, a third-party organization provides the file that contains postal codes.</span></span> <span data-ttu-id="858ed-115">Nadat de import is voltooid, worden alle postcodes in de indeling (NNNN AA) weergegeven.</span><span class="sxs-lookup"><span data-stu-id="858ed-115">After the import is completed, all postal codes will appear in the format (NNNN AA).</span></span>
> -   <span data-ttu-id="858ed-116">Voor Zweden biedt Postnummerservice.se twee typen bestanden: Zweedse postcodes en Zweedse adressen.</span><span class="sxs-lookup"><span data-stu-id="858ed-116">For Sweden, Postnummerservice.se provides two types of files: Swedish postal codes and Swedish addresses.</span></span> <span data-ttu-id="858ed-117">Tekstbestandsindeling wordt voor beide typen ondersteund voor het importeren.</span><span class="sxs-lookup"><span data-stu-id="858ed-117">The import supports text file format for both types.</span></span>


## <a name="create-zippostal-codes-manually"></a><span data-ttu-id="858ed-118">Handmatig postcodes maken</span><span class="sxs-lookup"><span data-stu-id="858ed-118">Create ZIP/postal codes manually</span></span>
<span data-ttu-id="858ed-119">In plaats van codes te importeren kunt u de pagina **Adresinstelling** gebruiken om handmatig nieuwe postcodes toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="858ed-119">Instead of importing codes, you can use the **Address setup** page to manually add new ZIP/postal codes.</span></span>

