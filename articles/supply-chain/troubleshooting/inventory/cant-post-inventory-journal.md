---
title: De voorraadjournaalwerkstroom wordt nooit voltooid en het journaal kan niet worden verwerkt
description: Nadat u een journaalgoedkeuringswerkstroom hebt ingediend, reageert de werkstroomverwerking niet meer en kunt u uw journalen niet bewerken of verwerken.
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
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475974"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>De voorraadjournaalwerkstroom wordt nooit voltooid en het journaal kan niet worden verwerkt

## <a name="symptoms"></a>Symptomen

Nadat u een journaalgoedkeuringswerkstroom hebt ingediend, reageert de werkstroomverwerking niet meer en kunt u uw journalen niet bewerken of verwerken.

## <a name="resolution"></a>Oplossing

Er zijn verschillende redenen waarom de verwerking van werkstromen niet kan worden voltooid. Controleer op de volgende problemen:

- Ga naar **Voorraadbeheer &gt; Instellingen &gt; Voorraadbeheerwerkstromen** en controleer de configuratie van de betrokken werkstroom. Zie [Goedkeuringswerkstromen van voorraadjournalen](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md) voor meer informatie.
- Mogelijk komt een uitzondering of fout in de werkstroom voor. Controleer de werkitemhistorie van de betrokken werkstroom om te zien of er een toepassingsfout is betrokken bij het beëindigen van de werkstroom.
- Het voorraadjournaal kan alleen worden bijgewerkt of bewerkt als het is goedgekeurd. Als terugroepen actief is, kunt u proberen het journaal terug te roepen. De uitvoering van de werkstroombatchtaak kan om meerdere redenen zijn uitgesteld. Een aantal van deze redenen kan worden veroorzaakt door het probleem met het werkstroomraamwerk.
