---
title: Prestatieverbetering van rekeningstructuuractivering
description: In dit artikel wordt de nieuwe prestatieverbetering voor het activeringsproces van de rekeningstructuur beschreven.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713994"
---
# <a name="account-structure-activation-performance-enhancement"></a>Prestatieverbetering van rekeningstructuuractivering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Door deze prestatieverbetering kunt u rekeningstructuren sneller activeren door meerdere transactieupdates tegelijk uit te voeren. Bovendien wordt de structuur zelf gemarkeerd als actief nadat deze is gevalideerd en kan de transactieverwerking doorgaan terwijl bestaande niet-geboekte transacties naar de nieuwe structuur worden bijgewerkt. Aangezien het enige tijd kan duren om transacties bij te werken, kunt u de status van uw activering bijhouden door **Activeringsstatus weergeven** te selecteren boven het raster op de pagina **Rekeningstructuren**. U kunt de activeringsstatus ook bekijken door **Weergeven** te selecteren in het actievenster en vervolgens **Activeringstatus** te selecteren in het vervolgkeuzemenu.

[![Pagina Rekeningstructuren.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Nadat u **Activeringsstatus weergeven** hebt geselecteerd, verschijnt er een dialoogvenster met de afzonderlijke taken die worden uitgevoerd als onderdeel van het activeringsproces. Voor elke taak kunt u de status en de voltooiingsdatum en -tijd weergeven, nadat de taak is voltooid.

[![Tijdlijn van de activering van de rekeningstructuur.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Tips voor activering van rekeningstructuur

Het dialoogvenster voor het activeren van de rekeningstructuur dat verschijnt wanneer u **Activeren** selecteert voor een conceptrekeningstructuur, heeft een tabblad met de naam **Niet-geboekte transacties bijwerken**. Deze sectie bevat een optie met de naam **Gedwongen bijwerken**. U kunt deze optie selecteren om alle niet-geboekte transacties bij te werken naar de huidige structuur. Gebruik deze optie echter alleen wanneer er een fout is opgetreden of als Microsoft Ondersteuning heeft aangegeven dat u deze optie moet gebruiken.

Hier volgen enkele van de factoren die van invloed kunnen zijn op de prestaties van het activeringsproces:

- Een groot aantal niet-geboekte journaalrecords
- Een groot aantal records met openstaande brondocumenten, zoals vrije-tekstfacturen, leveranciersfacturen en gerelateerde documenten die het brondocumentraamwerk gebruiken en openstaande boekhoudingsverdelingen hebben
- De hoeveelheid gegevens in TaxUncommitted
- De hoeveelheid openstaande budgetgegevens
- Import van journaalgegevens terwijl activeringstaken nog worden uitgevoerd

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
