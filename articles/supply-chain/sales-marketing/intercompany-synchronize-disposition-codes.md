---
title: Beschikkingscodes synchroniseren
description: In dit artikel wordt de synchronisatie van beschikkingscodes voor intercompany-handel beschreven.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: d347181dd6ba12de0e114d74d43cd46230ba4fb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905655"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Intercompany-beschikkingscodes synchroniseren

[!include [banner](../../includes/banner.md)]

Ter ondersteuning van intercompany-retouren kunt u in Microsoft Dynamics 365 Supply Chain Management extern gedefinieerde beschikkingscodes toewijzen aan bijbehorende interne beschikkingscodes. Wanneer u een intercompany-keten instelt, moet u ervoor zorgen dat de beschikkingsacties in de twee bedrijven die aan elkaar zijn toegewezen, identiek zijn. Als deze verschillend zijn, kan het synchronisatieproces niet worden uitgevoerd.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Informatie over beschikkingscodes voor drieledige rechtstreekse retouren

Beschikkingscodes worden gesynchroniseerd vanuit de intercompany-verkooporderregel naar de oorspronkelijke verkooporderregel. Synchronisatie heeft echter alleen directe gevolgen voor de oorspronkelijke verkooporderregel. Dit effect houdt in dat diverse regeltoeslagen worden verwijderd op basis van de beschikkingscode en diverse toeslagen, die zijn ingesteld in bedrijf A. Bedrijf A is het bedrijf dat de retourorder maakt.

In een drieledige keten voor rechtstreekse levering worden alle beschikkingsacties ondersteund op de intercompany-verkooporderregel. Wanneer het product echter aan de klant wordt geretourneerd, moet u bevestigen dat het afleveradres in de retourorder overeenkomt met het afleveradres van de klant dat in de oorspronkelijke order is opgegeven.

> [!NOTE]
> Er zijn geen beschikkingscodes voor inkooporders beschikbaar. Als u beschikkingscodes wilt synchroniseren vanuit de intercompany-verkooporder naar de oorspronkelijke retourorder, moet u een synchronisatie tussen verkooporders uitvoeren.

## <a name="replacing-returned-items"></a>Geretourneerde artikelen vervangen

Als bij vervanging van een geretourneerd artikel al een vervangingsorder is gemaakt in bedrijf B, kunt u geen beschikkingscode selecteren en wordt in bedrijf A geen aanvullende vervangingsorder gemaakt.

## <a name="rules-for-intercompany-direct-deliveries"></a>Regels voor rechtstreekse intercompany-leveringen

De volgende algemene regels zijn van toepassing op oorspronkelijke retourorders in scenario's voor rechtstreekse intercompany-leveringen:

- Als de onderliggende beschikkingsactie van de oorspronkelijke verkooporderregel Crediteren en uitvallen, Crediteren of Retour naar klant is, wordt de beschikkingsactie Crediteren toegepast. Bij de actiecode Retour naar klant wordt het nettobedrag in de bestaande regel en in de zojuist gesynchroniseerde regel uit de intercompany-verkooporder echter op 0 (nul) gezet. Bovendien worden uitvalregels nooit gesynchroniseerd. Een regel die wordt toegevoegd aan een intercompany-verkooporder, wordt nooit gesynchroniseerd voor een verkooporder met een positieve hoeveelheid en een aan uitval gerelateerde beschikkingsactie (bijvoorbeeld Crediteren en uitvallen of Vervangen en uitvallen).
- Een onderliggende beschikkingsactie Crediteren en vervangen of Uitvallen en vervangen wordt niet overschreven. Deze wordt afgehandeld als een beschikkingsactie Crediteren en vervangen of Uitvallen en vervangen. Deze regel is zelfs van toepassing als er geen uitvalregel is gemaakt in bedrijf A en er geen vervangingsorder is gemaakt in bedrijf B (het bedrijf dat het geretourneerde artikel heeft ontvangen). Er wordt alleen een vervangingsorder in bedrijf A gemaakt wanneer de pakbon is bijgewerkt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
