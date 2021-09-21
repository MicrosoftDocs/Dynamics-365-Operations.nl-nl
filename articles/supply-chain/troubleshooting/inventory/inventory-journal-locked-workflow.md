---
title: Uw voorraadjournaal is vergrendeld en de werkstroombatchtaak werkt niet
description: Een van uw voorraadjournalen wordt vergrendeld door een bepaalde bewerking en wordt niet vrijgegeven
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475985"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Uw voorraadjournaal is vergrendeld en de werkstroombatchtaak werkt niet

## <a name="symptoms"></a>Symptomen

Een van uw voorraadjournalen wordt vergrendeld door een bepaalde bewerking en wordt niet vrijgegeven. Als er bijvoorbeeld een onbekende fout optreedt tijdens het boeken (wat een systeemvergrendelingsbewerking is), blijft het journaal mogelijk in de door het systeem vergrendelde status. In dit geval wordt met de handler van het werkstroomwerkitem een fout gegenereerd terwijl de validatie wordt vergrendeld.

## <a name="resolution"></a>Oplossing

Meld u aan bij het SQL Server-exemplaar voor Supply Chain Management en controleer of **InventJournalTable.SystemBlocked** is ingesteld op *1*. Als dat het geval is, zorg er dan voor dat de status van het journaal niet vergrendeld is en stel vervolgens **InventJournalTable.SystemBlocked** in op *0*.
