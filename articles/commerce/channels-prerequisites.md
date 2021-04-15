---
title: Vereisten voor het instellen van kanalen
description: Dit onderwerp geeft een overzicht van de vereisten voor het instellen van kanalen in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800514"
---
# <a name="channel-setup-prerequisites"></a>Vereisten voor het instellen van kanalen

[!include [banner](includes/banner.md)]

Dit onderwerp geeft een overzicht van de vereisten voor het instellen van kanalen in Microsoft Dynamics 365 Commerce.

Voordat een Dynamics 365 Commerce-kanaal kan worden gemaakt, moeten verscheidene vereiste taken worden voltooid. De volgende lijsten met vereiste taken zijn gerangschikt op kanaaltype.

> [!NOTE]
> Nog niet alle documentatie is geschreven en koppelingen worden bijgewerkt wanneer nieuwe inhoud wordt gepubliceerd.

## <a name="initialization"></a>Initialisatie

- [Seedgegevens initialiseren](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globale vereisten die voor alle kanaaltypen zijn vereist

- [Uw rechtspersoonsstructuur definiëren en configureren](channels-legal-entities.md) 
- [Uw organisatiehiërarchie configureren](channels-org-hierarchies.md)
- [Een magazijn instellen](channels-setup-warehouse.md)
- [Btw configureren](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Een profiel voor e-mailmeldingen instellen](email-notification-profiles.md)
- [Nummerreeksen instellen](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Een standaardklant en -adresboek instellen](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Vereisten voor detailhandelafzetkanalen

- [Informatiecodes en informatiecodegroepen](info-codes-retail.md)
- [Een functionaliteitsprofiel detailhandel instellen](retail-functionality-profile.md)
- [Een werknemersadresboek instellen](new-address-book.md)
- [Een schermindeling instellen](pos-screen-layouts.md)
- [Een hardwarestation instellen](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Vereisten voor callcenterafzetkanalen

- Parameters van callcenter
- [Bestel- en restitutiebetalingsmethoden voor callcenters](work-with-payments.md)
- [Leveringsmethoden en toeslagen van callcenters](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Vereisten voor online kanalen

- [Een online functionaliteitsprofiel maken](online-functionality-profile.md)

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van kanalen](channels-overview.md)

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisatiehiërarchieën instellen](channels-org-hierarchies.md)

[Rechtspersonen maken](channels-legal-entities.md)

[Een detailhandelafzetkanaal instellen](channel-setup-retail.md)
    
[Een online afzetkanaal instellen](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
