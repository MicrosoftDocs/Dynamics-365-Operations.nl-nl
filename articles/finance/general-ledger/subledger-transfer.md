---
title: Subadministratie overboeken naar het grootboek
description: In dit onderwerp worden mogelijkheden beschreven die verband houden met het overboekingsproces voor subadministratie in het grootboek.
author: rcarlson
ms.date: 12/08/2021
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
ms.openlocfilehash: 213bbc2541c614aa26b0c830431818fb99c7682d
ms.sourcegitcommit: f5885999e008a49fe072d95f15e239905c24918a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2021
ms.locfileid: "7900725"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Subadministratie overboeken naar het grootboek

[!include [banner](../includes/banner.md)]

In dit onderwerp worden mogelijkheden beschreven die zijn gerelateerd aan de regels voor het overdragen van batches van journaalposten in de subadministratie.

In versie 8.1 werd de overdracht van regels toegestaan, waardoor de optie **Synchroon** werd afgeschaft. Zie voor meer informatie [Verwijderde of verouderde functies voor Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

De volgende opties zijn beschikbaar voor het overboeken van batches uit de subadministratie:

- **Asynchroon**: het overboeken van posten in de subadministratie naar het grootboek wordt onmiddellijk gepland. Het boekstuk in het grootboek wordt geregistreerd zodra resources beschikbaar zijn om de aanvraag te verwerken op de server.
- **Geplande batch**: de boekhoudingsposten in de subadministratie die moeten worden overgeboekt, worden toegevoegd aan de verwerkingswachtrij in het grootboek. De vermeldingen in de wachtrij worden verwerkt in de volgorde waarin ze zijn ontvangen. Elk boekstuk in het grootboek werkt accounts bij op de geplande tijd als resources beschikbaar zijn om de batchtaak te verwerken op de server.

In versie 10.0.8 werden verbeteringen uitgevoerd om de prestaties van de optie **Asynchroon** te verbeteren. Deze functie is ingeschakeld onder de functienaam **Prestatieoptimalisatie voor overboeken van subadministratie naar grootboek**.

De functionaliteit voor asynchrone overboeking van batches in de subadministratie helpt de gegevensoverdracht vanuit de subadministratie naar het grootboek te verbeteren. Door groepen kleinere transacties te groeperen en de transacties over te boeken in groepen, verwerkt de functionaliteit transacties efficiënter. Wanneer transacties worden gegroepeerd, worden de resources van de batchserver efficiënter gebruikt.

Voor een asynchrone overboeking van batches in de subadministratie moet de batchserver zijn ingesteld, online zijn en werken omdat batchtaken worden gemaakt om onmiddellijk op de batchserver te worden uitgevoerd. Wanneer de functie **Prestatieoptimalisatie voor overboeken van subadministratie naar grootboek** is ingeschakeld, moet u ook de systeembatchtaak **Procesautomatisering** met de naam **Procesautomatisering navragen systeemtaak** inschakelen. Zie [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md) voor meer informatie.

De efficiëntiewijziging op batchniveau gebruikt een enkele terugkerende batchtaak voor alle rechtspersonen in het systeem. Tijdens runtime wordt een nieuwe batchtaak gemaakt om de vereiste records te verwerken die nog niet zijn overgeboekt. U kunt meer instellingen beheren via de pagina **Procesautomatisering** in systeembeheer. Op die pagina kunt u het achtergrondproces wijzigen, de frequentie wijzigen en een slaapperiode definiëren.

Zie [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md) voor meer informatie over het instellen van procesautomatisering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
