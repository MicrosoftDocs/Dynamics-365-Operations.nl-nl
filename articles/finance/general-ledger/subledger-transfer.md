---
title: Subadministratie overboeken naar het grootboek
description: In dit onderwerp worden mogelijkheden beschreven in Microsoft Dynamics 365 Finance met betrekking tot het overboekingsproces voor subadministratie naar het grootboek.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000442"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Subadministratie overboeken naar het grootboek

[!include [banner](../includes/banner.md)]

In dit onderwerp worden mogelijkheden van Microsoft Dynamics 365 Finance beschreven die zijn gerelateerd aan de regels voor het overdragen van batches van journaalposten in de subadministratie.

In versie 8.1 werd de overdracht van regels toegestaan, waardoor de optie Synchroon werd afgeschaft. Zie voor meer informatie [Verwijderde of verouderde functies voor Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

De volgende opties zijn beschikbaar voor het overboeken van batches uit de subadministratie. 

 - Asynchroon: Met deze optie wordt onmiddellijk de overdracht van posten in de subadministratie naar het grootboek gepland. Het boekstuk in het grootboek wordt geregistreerd zodra resources vrij zijn om deze aanvraag te verwerken op de server. 

- Geplande batch: Met deze optie worden de posten uit de subadministratie toegevoegd die worden overgeboekt naar de verwerkingswachtrij in het grootboek, waar de posten worden verwerkt in de volgorde waarin ze worden ontvangen. Het boekstuk in het grootboek wordt geregistreerd op de geplande tijd, als resources vrij zijn om deze batchtaak te verwerken op de server. 
 
In versie 10.0.8 werden verbeteringen uitgevoerd om de prestaties van de optie Asynchroon te verbeteren. Deze functie is ingeschakeld onder de functienaam **Prestatieoptimalisatie voor overboeken van subadministratie naar grootboek**. 
 
Deze functionaliteit verbetert de overdracht van gegevens vanuit de subadministratie naar het grootboek. Dit maakt het proces efficiënter, en groepeert sets van kleinere transacties bijeen voor overboeking. Hierdoor kan de batchserver efficiënter worden gebruikt. Voor deze functionaliteit moet de batchserver zijn ingesteld en online en functioneel zijn, zodat de optie voor asynchrone overdrachts werkt. 
