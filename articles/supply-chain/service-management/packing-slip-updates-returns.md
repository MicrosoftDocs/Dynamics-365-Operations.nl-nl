---
title: Pakbonnen bijwerken voor retouren
description: Voordat geretourneerde artikelen weer in de voorraad kunnen worden opgenomen, moet de pakbon voor de order waartoe deze artikelen behoren, worden bijgewerkt.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c82e43beddb8bae0a56b0894ce484ca7605b42e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006711"
---
# <a name="packing-slip-updates-for-returns"></a>Pakbonnen bijwerken voor retouren  

[!include [banner](../includes/banner.md)]


Voordat geretourneerde artikelen weer in de voorraad kunnen worden opgenomen, moet de pakbon voor de order waartoe deze artikelen behoren, worden bijgewerkt. Net zoals u met het factuurbijwerkproces de financiële transactie bijwerkt, werkt u met het pakbonbijwerkproces fysiek de voorraadrecord bij. Dit betekent dat u met het bijwerken van de pakbon, wijzigingen in de voorraad doorvoert. In het geval van geretourneerde artikelen worden de stappen die zijn toegewezen aan de beschikkingsactie, geïmplementeerd tijdens het bijwerken van de pakbon.

Het bijwerken van de pakbon kan worden verwerkt in het artikelontvangstjournaal of de retourorder.

Als onderdeel van het boekingsproces voor pakbonnen kan het referentienummer van de pakbon uit de verzenddocumenten van de klant worden gekoppeld aan de orderregels. Deze koppeling is optioneel en dient alleen ter informatie. Er worden geen transactiewijzigingen aangebracht.

Als niet alle verwachte geretourneerde artikelen zijn ontvangen, moet u alleen die hoeveelheid die is ontvangen, opnemen in de wijziging van de pakbon. Laat de resterende artikelen op de order staat tot de rest van de retourzending is gearriveerd.

Als een artikel van het quarantainemagazijn wordt teruggestuurd naar de afdeling Expeditie en ontvangst, bijvoorbeeld wanneer de quarantaine-inspecteur niet weet waar het artikel in de voorraad moet worden opgeslagen, moet de bijbehorende pakbon worden bijgewerkt om de beschikkingscode juist te registreren en op te volgen, die is opgegeven als gevolg van de quarantaine.

Wanneer u een pakbon bijwerkt voor een geretourneerd artikel dat van een verkoopovereenkomst afkomstig is, wordt de verkoopovereenkomsttoezegging voor dat artikel automatisch bijgewerkt met de wijziging in de hoeveelheid of het bedrag. 

## <a name="see-also"></a>Zie ook

[Facturen bijwerken voor retouren](perform-invoice-updates-for-returns.md)

  


