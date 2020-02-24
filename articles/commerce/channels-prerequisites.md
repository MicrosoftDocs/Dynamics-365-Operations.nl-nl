---
title: Vereisten voor het instellen van kanalen
description: Dit onderwerp geeft een overzicht van de vereisten voor het instellen van kanalen in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002284"
---
# <a name="channel-setup-prerequisites"></a>Vereisten voor het instellen van kanalen


[!include [banner](includes/banner.md)]

Dit onderwerp geeft een overzicht van de vereisten voor het instellen van kanalen in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Voordat een Dynamics 365 Commerce-kanaal kan worden gemaakt, moeten verscheidene vereiste taken worden voltooid. De volgende lijsten met vereiste taken zijn gerangschikt op kanaaltype.

> [!NOTE]
> Nog niet alle documentatie is geschreven en koppelingen worden bijgewerkt wanneer nieuwe inhoud wordt gepubliceerd.

## <a name="initialization"></a>Initialisatie

- [Seedgegevens initialiseren](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globale vereisten die voor alle kanaaltypen zijn vereist

- [Uw rechtspersoonsstructuur definiëren en configureren](channels-legal-entities.md) 
- [Uw organisatiehiërarchie configureren](channels-org-hierarchies.md)
- [Een magazijn instellen](channels-setup-warehouse.md)
- [Btw configureren](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [Een profiel voor e-mailmeldingen instellen](email-notification-profiles.md)
- [Nummerreeksen instellen](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Een standaardklant en -adresboek instellen](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Vereisten voor detailhandelafzetkanalen

- [Informatiecodes en informatiecodegroepen](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Een functionaliteitsprofiel detailhandel instellen](retail-functionality-profile.md)
- [Een werknemersadresboek instellen](new-address-book.md)
- [Een schermindeling instellen](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Een hardwarestation instellen](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Vereisten voor callcenterafzetkanalen

- Parameters van callcenter
- Restitutiemethoden van callcenter
- Huurtypen
- Betalingsservice
- Orderwachtstandcodes

## <a name="online-channel-prerequisites"></a>Vereisten voor online afzetkanalen

- [Een online functionaliteitsprofiel maken](online-functionality-profile.md)

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van kanalen](channels-overview.md)

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisatiehiërarchieën instellen](channels-org-hierarchies.md)

[Rechtspersonen maken](channels-legal-entities.md)

[Een detailhandelafzetkanaal instellen](channel-setup-retail.md)
    
[Een online afzetkanaal instellen](channel-setup-online.md)
