---
title: Detailhandel wordt niet weergegeven in de lijst met winkels waarbij kan worden opgehaald
description: Dit artikel bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer een detailhandelwinkel niet wordt weergegeven in de lijst met winkels waar artikelen kunnen worden opgehaald.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: b6cec3d9d598be221516506388e4797ad579a610
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286747"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Detailhandel wordt niet weergegeven in de lijst met winkels waarbij kan worden opgehaald

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer een detailhandelwinkel niet wordt weergegeven in de lijst met winkels waar artikelen kunnen worden opgehaald.

## <a name="description"></a>Beschrijving

Een detailhandelwinkel wordt niet weergegeven in de lijst met winkels waar artikelen kunnen worden opgehaald.

## <a name="resolution"></a>Oplossing

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>De lengtegraad en breedtegraad configureren voor het winkeladres in Commerce Headquarters

Voer deze stappen uit om de lengtegraad en breedtegraad te configureren voor het winkeladres in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanalen \> Winkels \> Alle winkels**.
1. Zoek de winkel die u wilt weergeven als ophaaloptie op de e-commercesite. Noteer de waarde bij **Nummer van operationele eenheid**.
1. Ga naar **Organisatiebeheer \> Organisaties \> Operationele eenheden**.
1. Zoek naar het nummer van de operationele eenheid dat u eerder hebt genoteerd en selecteer vervolgens de operationele eenheid in de zoekresultaten.
1. Selecteer op het sneltabblad **Adressen** de optie **Meer opties** en selecteer vervolgens **Geavanceerd**.
1. Ga naar het sneltabblad **Algemeen** en zorg ervoor dat de velden **Lengtegraad** en **Breedtegraad** correct zijn ingesteld. In deze stap controleert u of de waarden correct zijn opgegeven als positieve of negatieve getallen.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Afhandelingsgroepen configureren in Commerce Headquarters

Voer deze stappen uit om afhandelingsgroepen te configureren in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanalen \> Online winkels**.
1. Selecteer de online winkel die u wilt configureren.
1. Selecteer in het actievenster de optie **Instellingen** en selecteer vervolgens **Toewijzing afhandelingsgroep**.
1. Selecteer op de pagina **Toewijzing afhandelingsgroep** de afhandelingsgroep voor de online winkel.
1. Zorg er onder **Instellingen** voor dat de detailhandelwinkel correct is geconfigureerd voor de afhandelingsgroep.

## <a name="additional-resources"></a>Aanvullende bronnen 

[Een operationele eenheid maken](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Een online afzetkanaal instellen](../channel-setup-online.md)
