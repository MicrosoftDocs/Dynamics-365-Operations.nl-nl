---
title: Subadministratie overboeken naar het grootboek
description: In dit artikel worden mogelijkheden beschreven die verband houden met het overboekingsproces voor subadministratie in het grootboek.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7ef93b81ce37128f7ff400eb4034ffea01756038
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779848"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Subadministratie overboeken naar het grootboek

[!include [banner](../includes/banner.md)]

In dit artikel worden mogelijkheden beschreven die zijn gerelateerd aan de regels voor het overdragen van batches van journaalposten in de subadministratie.

In versie 8.1 werd de overdracht van regels toegestaan, waardoor de optie **Synchroon** werd afgeschaft. Zie [Verwijderde of afgeschafte functies voor apps voor financiën en bedrijfsactiviteiten](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20) voor meer informatie.

De volgende opties zijn beschikbaar voor het overboeken van batches uit de subadministratie:

- **Asynchroon**: het overboeken van posten in de subadministratie naar het grootboek wordt onmiddellijk gepland. Het boekstuk in het grootboek wordt geregistreerd zodra resources beschikbaar zijn om de aanvraag te verwerken op de server.
- **Geplande batch**: de boekhoudingsposten in de subadministratie die moeten worden overgeboekt, worden toegevoegd aan de verwerkingswachtrij in het grootboek. De vermeldingen in de wachtrij worden verwerkt in de volgorde waarin ze zijn ontvangen. Elk boekstuk in het grootboek werkt accounts bij op de geplande tijd als resources beschikbaar zijn om de batchtaak te verwerken op de server.

Er zijn verbeteringen uitgevoerd om de prestaties van de optie **Asynchroon** te verbeteren. Deze functie is ingeschakeld onder de functienaam **Prestatieoptimalisatie voor overboeken van subadministratie naar grootboek**.

De functionaliteit voor asynchrone overboeking van batches in de subadministratie helpt de gegevensoverdracht vanuit de subadministratie naar het grootboek te verbeteren. Door groepen kleinere transacties te groeperen en de transacties over te boeken in groepen, verwerkt de functionaliteit transacties efficiënter. Wanneer transacties worden gegroepeerd, worden de resources van de batchserver efficiënter gebruikt.

Voor een asynchrone overboeking van batches in de subadministratie moet de batchserver zijn ingesteld, online zijn en werken omdat batchtaken worden gemaakt om onmiddellijk op de batchserver te worden uitgevoerd. Wanneer de functie **Prestatieoptimalisatie voor overboeken van subadministratie naar grootboek** is ingeschakeld, moet u ook de systeembatchtaak **Procesautomatisering** met de naam **Procesautomatisering navragen systeemtaak** inschakelen. Zie [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md) voor meer informatie.

De efficiëntiewijziging op batchniveau gebruikt een enkele terugkerende batchtaak voor alle rechtspersonen in het systeem. Tijdens runtime wordt een nieuwe batchtaak gemaakt om de vereiste records te verwerken die nog niet zijn overgeboekt. U kunt meer instellingen beheren via de pagina **Procesautomatisering** in systeembeheer. Op die pagina kunt u het achtergrondproces wijzigen, de frequentie wijzigen en een slaapperiode definiëren.

Zie [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md) voor meer informatie over het instellen van procesautomatisering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

