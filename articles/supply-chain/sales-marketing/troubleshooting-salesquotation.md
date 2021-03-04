---
title: Problemen met verkoopoffertes oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkoopoffertes.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425398"
---
# <a name="troubleshoot-sales-quotations"></a>Problemen met verkoopoffertes oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkoopoffertes.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Ik kan de verkoophoeveelheid van een verkoopofferte voor een serviceartikel niet wijzigen.

### <a name="issue-description"></a>Probleembeschrijving

Als u probeert een verkoophoeveelheid (veld **SalesQty**) voor een artikel van het type *Service* op een verkoopofferteregel in te stellen, wordt het volgende bericht weergegeven: 'Bijwerken niet toegestaan voor veld Hoeveelheid'.

### <a name="issue-resolution"></a>Probleemoplossing

U kunt geen verkoophoeveelheid instellen voor producten die serviceartikelen zijn. Als u bijvoorbeeld een service voor het installeren van een artikel aanbiedt, is het niet zinvol om een hoeveelheid vast te leggen, omdat er geen fysiek artikel is. Er is alleen een service.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]