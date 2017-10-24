---
title: Postcodes importeren of handmatig maken
description: In dit artikel wordt beschreven hoe u postcodes in de juiste indeling kunt importeren en handmatig maken. Dit onderwerp bevat informatie over de functie die is toegevoegd voor Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LogisticsAddressSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 29901
ms.search.region: Belgium, Netherlands, Sweden
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7b8cbd5f9c5540142869b748e2f9ee1453d5da
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="import-or-manually-create-postal-codes"></a><span data-ttu-id="34e0a-104">Postcodes importeren of handmatig maken</span><span class="sxs-lookup"><span data-stu-id="34e0a-104">Import or manually create postal codes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="34e0a-105">In dit artikel wordt beschreven hoe u postcodes in de juiste indeling kunt importeren en handmatig maken.</span><span class="sxs-lookup"><span data-stu-id="34e0a-105">This article explains how to import and manually create postal codes in the correct format.</span></span> <span data-ttu-id="34e0a-106">Dit onderwerp bevat informatie over de functie die is toegevoegd voor Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="34e0a-106">This topic includes information about feature that was added for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="34e0a-107">Met het importproces kunt u de postcodes voor een bepaald land of een bepaalde regio bijwerken.</span><span class="sxs-lookup"><span data-stu-id="34e0a-107">The import process lets you update the ZIP/postal codes for a specific country/region.</span></span> <span data-ttu-id="34e0a-108">U kunt postcodes ook handmatig maken.</span><span class="sxs-lookup"><span data-stu-id="34e0a-108">You can also create postal codes manually.</span></span>

## <a name="import-zippostal-codes"></a><span data-ttu-id="34e0a-109">Postcodes importeren</span><span class="sxs-lookup"><span data-stu-id="34e0a-109">Import ZIP/postal codes</span></span>
<span data-ttu-id="34e0a-110">U kunt de pagina **Postcodes importeren** gebruiken om nieuwe postcodes in Finance and Operations te importeren.</span><span class="sxs-lookup"><span data-stu-id="34e0a-110">You can use the **Import ZIP/postal codes** page to import new postal codes into Finance and Operations.</span></span> <span data-ttu-id="34e0a-111">Wanneer u de codes importeert, worden de bestaande postcodes door de nieuwe indeling vervangen en worden eventuele nieuwe codes toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="34e0a-111">When you import the codes, the existing ZIP or postal codes are replaced with the new format, and any new codes are added.</span></span>

<span data-ttu-id="34e0a-112">Voor sommige landen moet u het Gegevensbeheer-raamwerk gebruiken om codes te importeren, terwijl voor andere landen alleen een uploadbestand vereist is.</span><span class="sxs-lookup"><span data-stu-id="34e0a-112">For some countries, you must use the Data management framework to import codes, while for other countries only a upload file is required.</span></span> <span data-ttu-id="34e0a-113">Voor België, Nederland en Zweden moet een bestand worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="34e0a-113">Belgium, Netherlands, and Sweden require a file to upload.</span></span>

> [!NOTE]
> -   <span data-ttu-id="34e0a-114">Voor België bevat de officiële webpagina van de Belgische Post een officiële lijst van de postcodes en de bijbehorende plaatsnamen.</span><span class="sxs-lookup"><span data-stu-id="34e0a-114">For Belgium, the official webpage from the Belgian Post provides an official list of the postcodes and the corresponding city names.</span></span> <span data-ttu-id="34e0a-115">HTML-bestandsindeling wordt ondersteund voor het importeren.</span><span class="sxs-lookup"><span data-stu-id="34e0a-115">The import supports html file format.</span></span>
> -   <span data-ttu-id="34e0a-116">Voor Nederland levert een externe organisatie het bestand dat postcodes bevat.</span><span class="sxs-lookup"><span data-stu-id="34e0a-116">For Netherlands, a third-party organization provides the file that contains postal codes.</span></span> <span data-ttu-id="34e0a-117">Nadat de import is voltooid, worden alle postcodes in de indeling (NNNN AA) weergegeven.</span><span class="sxs-lookup"><span data-stu-id="34e0a-117">After the import is completed, all postal codes will appear in the format (NNNN AA).</span></span>
> -   <span data-ttu-id="34e0a-118">Voor Zweden biedt Postnummerservice.se twee typen bestanden: Zweedse postcodes en Zweedse adressen.</span><span class="sxs-lookup"><span data-stu-id="34e0a-118">For Sweden, Postnummerservice.se provides two types of files: Swedish postal codes and Swedish addresses.</span></span> <span data-ttu-id="34e0a-119">Tekstbestandsindeling wordt voor beide typen ondersteund voor het importeren.</span><span class="sxs-lookup"><span data-stu-id="34e0a-119">The import supports text file format for both types.</span></span>


## <a name="create-zippostal-codes-manually"></a><span data-ttu-id="34e0a-120">Handmatig postcodes maken</span><span class="sxs-lookup"><span data-stu-id="34e0a-120">Create ZIP/postal codes manually</span></span>
<span data-ttu-id="34e0a-121">In plaats van codes te importeren kunt u de pagina **Adresinstelling** gebruiken om handmatig nieuwe postcodes toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="34e0a-121">Instead of importing codes, you can use the **Address setup** page to manually add new ZIP/postal codes.</span></span>



