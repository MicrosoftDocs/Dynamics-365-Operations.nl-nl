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
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Problemen oplossen met bekendheid van oplossingen

[!include [banner](../../includes/banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service. Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot bekendheid van oplossingen.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="error-on-the-dual-write-page"></a>Fout op de pagina Twee keer wegschrijven

Op de pagina **Twee keer wegschrijven** kan een foutbericht van de volgende strekking worden weergegeven:

*De entiteit met de naam 'msdyn\_dualwriteentitymap' met namemapping='Logical' is niet gevonden in de MetadataCache.*

Om het probleem op te lossen, controleert u of de kernoplossing Twee keer wegschrijven in Common Data Service is geïnstalleerd. De kernoplossing Twee keer wegschrijven is een vereiste voor kennis over de oplossing.
