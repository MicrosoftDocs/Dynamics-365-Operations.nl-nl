---
title: Problemen oplossen met bekendheid van oplossingen
description: Dit onderwerp bevat informatie over het oplossen van problemen met betrekking tot de bekendheid van oplossingen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172616"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="f16fa-103">Problemen oplossen met bekendheid van oplossingen</span><span class="sxs-lookup"><span data-stu-id="f16fa-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f16fa-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f16fa-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="f16fa-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot bekendheid van oplossingen.</span><span class="sxs-lookup"><span data-stu-id="f16fa-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f16fa-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f16fa-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="f16fa-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="f16fa-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="f16fa-108">Fout op de pagina Twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="f16fa-108">Error on the Dual-write page</span></span>

<span data-ttu-id="f16fa-109">Op de pagina **Twee keer wegschrijven** kan een foutbericht van de volgende strekking worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="f16fa-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="f16fa-110">*De entiteit met de naam 'msdyn\_dualwriteentitymap' met namemapping='Logical' is niet gevonden in de MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="f16fa-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="f16fa-111">Om het probleem op te lossen, controleert u of de kernoplossing Twee keer wegschrijven in Common Data Service is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="f16fa-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="f16fa-112">De kernoplossing Twee keer wegschrijven is een vereiste voor kennis over de oplossing.</span><span class="sxs-lookup"><span data-stu-id="f16fa-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
