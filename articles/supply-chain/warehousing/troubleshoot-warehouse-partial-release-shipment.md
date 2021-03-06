---
title: Problemen met gedeeltelijke vrijgaven en gedeeltelijke zendingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken gedeeltelijke vrijgaven en gedeeltelijke zendingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828149"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Problemen met gedeeltelijke vrijgaven en gedeeltelijke zendingen oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken gedeeltelijke vrijgaven en gedeeltelijke zendingen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>De vrijgavestatus van een verkooporder blijft Gedeeltelijk vrijgegeven, zelfs nadat de verkooporder is gefactureerd.

### <a name="issue-description"></a>Probleembeschrijving

Een verkooporder is een leveringsorder, maar een of meer artikelen op de order hebben een andere leveringsmethode. Nadat de order is gefactureerd, heeft deze nog steeds de vrijgavestatus *Gedeeltelijk vrijgegeven*.

Een verkooporder heeft bijvoorbeeld twee artikelen: een voor levering en een voor ophalen. De levering en het ophalen zijn voltooid. Daarom zijn beide regels gefactureerd. De vrijgavestatus wordt echter nog steeds weergegeven als *Gedeeltelijk vrijgegeven*. Dit is misleidend.

### <a name="issue-resolution"></a>Probleemoplossing

De vrijgavestatus is alleen van toepassing op orderregels met artikelen waarvoor magazijnbeheer is ingeschakeld. Daarom blijft de vrijgavestatus *Gedeeltelijk vrijgegeven* in dit scenario. Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. Een uitbreiding kan worden toegevoegd als onderdeel van de pakbon en het factureringsproces om de vrijgavestatus bij te werken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]