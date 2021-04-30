---
title: Subadministratie overboeken naar het grootboek
description: In dit onderwerp worden mogelijkheden beschreven in Microsoft Dynamics 365 Finance met betrekking tot het overboekingsproces voor subadministratie naar het grootboek.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897499"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Subadministratie overboeken naar het grootboek

[!include [banner](../includes/banner.md)]

In dit onderwerp worden mogelijkheden van Microsoft Dynamics 365 Finance beschreven die zijn gerelateerd aan de regels voor het overdragen van batches van journaalposten in de subadministratie.

In versie 8.1 werd de overdracht van regels toegestaan, waardoor de optie **Synchroon** werd afgeschaft. Zie voor meer informatie [Verwijderde of verouderde functies voor Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

De volgende opties zijn beschikbaar voor het overboeken van batches uit de subadministratie. 

 - Asynchroon: Met deze optie wordt onmiddellijk de overdracht van posten in de subadministratie naar het grootboek gepland. Het boekstuk in het grootboek wordt geregistreerd zodra resources vrij zijn om deze aanvraag te verwerken op de server. 

- Geplande batch: Met deze optie worden de posten uit de subadministratie toegevoegd die worden overgeboekt naar de verwerkingswachtrij in het grootboek, waar de posten worden verwerkt in de volgorde waarin ze worden ontvangen. Het boekstuk in het grootboek wordt geregistreerd op de geplande tijd, als resources vrij zijn om deze batchtaak te verwerken op de server. 
 
In versie 10.0.8 werden verbeteringen uitgevoerd om de prestaties van de optie Asynchroon te verbeteren. Deze functie is ingeschakeld onder de functienaam **Prestatieoptimalisatie voor overboeken van subadministratie naar grootboek**. 
 
Deze functionaliteit verbetert de overdracht van gegevens vanuit de subadministratie naar het grootboek. Dit maakt het proces efficiënter, en groepeert sets van kleinere transacties bijeen voor overboeking. Hierdoor kan de batchserver efficiënter worden gebruikt. Voor deze functionaliteit moet de batchserver zijn ingesteld en online en functioneel zijn, zodat de optie voor asynchrone overdracht werkt. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]