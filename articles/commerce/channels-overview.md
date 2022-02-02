---
title: Overzicht van kanalen
description: Dit onderwerp geeft een overzicht van afzetkanalen in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cc7f00d69a6fd57efcd9b6eece56ddc0702c6935
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985000"
---
# <a name="channels-overview"></a>Overzicht van kanalen


[!include [banner](includes/banner.md)]

Dit onderwerp geeft een overzicht van afzetkanalen in Microsoft Dynamics 365 Commerce. Het bevat informatie over de taken die u vóór en na het instellen van elk afzetkanaal moet uitvoeren.

## <a name="types-of-channels"></a>Typen afzetkanalen

Dynamics 365 Commerce ondersteunt drie verschillende afzetkanaaltypen: detailhandel, callcenter en online.

### <a name="retail-channels"></a>Detailhandelafzetkanalen

Detailhandelkanalen zijn de standaard fysieke winkels. Iedere winkel kan zijn eigen POS-kassa's, prijsgroepen, inkomsten- en uitgavenrekeningen en personeel hebben. 

### <a name="call-center-channels"></a>Callcenterafzetkanalen

Callcenterafzetkanalen vormen het bestel- en klantenbeheer via callcenters.

### <a name="online-channels"></a>Online afzetkanalen

Online afzetkanalen zijn de webwinkels. Wanneer een online kanaal is gemaakt, moet er een website worden gemaakt met behulp van het hulpprogramma Microsoft Dynamics 365 Commerce Site Builder of een andere e-Commerce oplossing van derden.

## <a name="channel-setup-basics"></a>Basisinformatie over het instellen van kanalen

Een kanaal wordt ingesteld met het Commerce-hulpprogramma. Elk kanaal kan zijn eigen betalingsmethoden, prijsgroepen, producthiërarchieën, assortimenten en reeks producten hebben. Nadat u een kanaal hebt gemaakt, wijst u de producten toe die u wilt voeren en verkopen. Elk kanaaltype heeft een unieke set functies die mogelijk moeten worden geconfigureerd. Zo moeten aan een detailhandelafzetkanaal werknemers, kassa's en klanten worden toegewezen. Nadat u een nieuw kanaal hebt gemaakt, moet dit worden toegewezen aan een organisatiehiërarchie.

## <a name="channel-setup-prerequisites"></a>Vereisten voor het instellen van kanalen

Voordat u een kanaal kunt instellen, moet u een aantal vereiste taken uitvoeren op basis van het type kanaaltype. Zie [Vereisten voor het instellen van kanalen](channels-prerequisites.md) voor meer informatie.

## <a name="set-up-a-channel"></a>Een kanaal instellen

Nadat u de vereiste taken hebt voltooid, gebruikt u de volgende koppelingen voor verdere installatie-instructies.

- [Een detailhandelafzetkanaal instellen](channel-setup-retail.md)
- [Een callcenterkanaal instellen](channel-setup-callcenter.md)
- [Een online afzetkanaal instellen](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Aanvullende resources

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Een detailhandelafzetkanaal instellen](channel-setup-retail.md)
    
[Een online afzetkanaal instellen](channel-setup-online.md)

[Een callcenterkanaal instellen](channel-setup-callcenter.md)

[Organisatiehiërarchieën instellen](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]