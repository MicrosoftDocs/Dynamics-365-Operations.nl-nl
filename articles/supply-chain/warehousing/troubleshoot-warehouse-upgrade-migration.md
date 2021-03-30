---
title: Problemen met de upgrade en migratie naar geavanceerd magazijnbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens upgraden en migreren naar geavanceerd magazijnbeheer.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f5bfee31ce27e919086f978fb3ff88ca61a65eba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208082"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="7e05d-103">Problemen met de upgrade en migratie naar geavanceerd magazijnbeheer oplossen</span><span class="sxs-lookup"><span data-stu-id="7e05d-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e05d-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens upgraden en migreren naar geavanceerd magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="7e05d-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="7e05d-105">Het volgende foutbericht wordt weergegeven: "java.security.cert.certPathValidatorException: vertrouwensanker voor certificaatpad is niet gevonden."</span><span class="sxs-lookup"><span data-stu-id="7e05d-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7e05d-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="7e05d-106">Issue description</span></span>

<span data-ttu-id="7e05d-107">U ontvangt dit foutbericht in de magazijn-app, omdat zelfondertekende certificaten niet worden vertrouwd op Android 8+ in on-premises-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="7e05d-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7e05d-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="7e05d-108">Issue resolution</span></span>

<span data-ttu-id="7e05d-109">Gebruik een externe (openbare) certificeringsinstantie (CA).</span><span class="sxs-lookup"><span data-stu-id="7e05d-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="7e05d-110">Er is een oplossing voor dit probleem beschikbaar in versie 1.9.0.0 van de magazijn-app.</span><span class="sxs-lookup"><span data-stu-id="7e05d-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="7e05d-111">Zie [Verbindingsproblemen in de magazijnapp oplossen](troubleshoot-warehouse-app-connection.md) voor informatie over dit probleem en hoe u het kunt oplossen.</span><span class="sxs-lookup"><span data-stu-id="7e05d-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="7e05d-112">Wat is het goedgekeurde proces voor het verplaatsen van basaal magazijnbeheer naar geavanceerd magazijnbeheer?</span><span class="sxs-lookup"><span data-stu-id="7e05d-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="7e05d-113">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="7e05d-113">Issue description</span></span>

<span data-ttu-id="7e05d-114">U werkt momenteel onder voorraad beheer en gebruikt de basisvoorraadfunctionaliteit en u wilt overstappen op geavanceerd magazijnbeheer om gebruik te kunnen maken van mobiele apparaten, waves en werk.</span><span class="sxs-lookup"><span data-stu-id="7e05d-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="7e05d-115">U ondervindt echter problemen wanneer u deze overstap wilt maken.</span><span class="sxs-lookup"><span data-stu-id="7e05d-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="7e05d-116">U kunt uw producten bijvoorbeeld niet wijzigen, zodat ze opslagdimensies (site, magazijn en locatie) gebruiken, omdat de producten hiervoor transacties hebben.</span><span class="sxs-lookup"><span data-stu-id="7e05d-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="7e05d-117">Daarom moet u weten wat het goedgekeurde proces is voor het verplaatsen van basaal magazijnbeheer naar geavanceerd magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="7e05d-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7e05d-118">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="7e05d-118">Issue resolution</span></span>

<span data-ttu-id="7e05d-119">Zie voor meer informatie over het proces voor het overstappen van basaal magazijnbeheer naar geavanceerd magazijnbeheer de volgende blogberichten en documentatie:</span><span class="sxs-lookup"><span data-stu-id="7e05d-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="7e05d-120">Magazijnbeheerproces inschakelen voor bestaande artikelen en magazijnen.</span><span class="sxs-lookup"><span data-stu-id="7e05d-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="7e05d-121">Migratie van Microsoft Dynamics AX WMS naar nieuwe R3-magazijn- en transportfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="7e05d-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="7e05d-122">Migratie van WMSI/WMS2-artikelen</span><span class="sxs-lookup"><span data-stu-id="7e05d-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="7e05d-123">Upgrade van magazijnbeheer van Microsoft Dynamics AX 2012 naar Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7e05d-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]