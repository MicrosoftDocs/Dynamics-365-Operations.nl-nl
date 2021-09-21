---
title: Kan de verkoophoeveelheid van een serviceartikel op een verkoopofferteregel niet instellen
description: Wanneer u met verkoopoffertes werkt, kunt u geen verkoophoeveelheid instellen voor producten die serviceartikelen zijn, omdat er geen fysieke artikelen moeten worden geteld.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476053"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Kan de verkoophoeveelheid van een serviceartikel op een verkoopofferteregel niet wijzigen

## <a name="symptoms"></a>Symptomen

Als u probeert een verkoophoeveelheid (veld **SalesQty**) voor een artikel van het type *Service* op een verkoopofferteregel in te stellen, wordt het volgende bericht weergegeven:

> 'Bijwerken niet toegestaan voor veld Hoeveelheid'.

## <a name="cause"></a>Oorzaak

Dit is zo ontworpen. U kunt geen verkoophoeveelheid instellen voor producten die serviceartikelen zijn. Als u bijvoorbeeld een service voor het installeren van een artikel aanbiedt, is het niet zinvol om een hoeveelheid vast te leggen, omdat er geen fysiek artikel is. Er is alleen een service.
