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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 7f1a6e424996201ecae1b624c13cfc573745dc0a
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997273"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Problemen oplossen met bekendheid van oplossingen

[!include [banner](../../includes/banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service. Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot bekendheid van oplossingen.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="error-on-the-dual-write-page"></a>Fout op de pagina Twee keer wegschrijven

Op de pagina **Twee keer wegschrijven** kan een foutbericht van de volgende strekking worden weergegeven:

*De entiteit met de naam 'msdyn\_dualwriteentitymap' met namemapping='Logical' is niet gevonden in de MetadataCache.*

Om het probleem op te lossen, controleert u of de kernoplossing Twee keer wegschrijven in Common Data Service is geïnstalleerd. De kernoplossing Twee keer wegschrijven is een vereiste voor kennis over de oplossing.
