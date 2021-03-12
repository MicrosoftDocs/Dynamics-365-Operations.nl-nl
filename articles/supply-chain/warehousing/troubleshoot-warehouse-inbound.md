---
title: Problemen met inkomende magazijnbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomende magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970238"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Problemen met inkomende magazijnbewerkingen oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomende magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Het volgende foutbericht wordt weergegeven: "Kwaliteitsorder %1 is gegenereerd. Kan het clusterprofiel niet vinden, controleer uw configuratie."

### <a name="issue-description"></a>Probleembeschrijving

Dit foutbericht is gerelateerd aan een ontvangstproces waarbij kwaliteitsbeheer (QMS) is ingeschakeld. Afhankelijk van de configuratie in uw omgeving, kunt u het probleem mogelijk oplossen met aanvullende informatie over de transactie die het foutbericht genereert.

### <a name="issue-resolution"></a>Probleemoplossing

Controleer eerst de instellingen voor [clusterverzameling](set-up-cluster-picking.md) en controleer of de clusterprofielen juist zijn ingesteld. U kunt een menuopdracht voor een mobiel apparaat voor clusterverzameling alleen gebruiken als clusterprofielen zijn ingesteld. Afhankelijk van uw omgeving, moet u mogelijk ook andere gerelateerde configuraties controleren.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Gecombineerde nummerplaat ontvangen werkt niet voor beschikkingscodes behalve Credit.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer het veld **Actie** voor een beschikkingscode is ingesteld op *Credit* of *Uitval*, kunt u de menuopdracht [Gecombineerde nummerplaat ontvangen](mixed-license-plate-receiving.md) alleen gebruiken om geretourneerde artikelen te verwerken.

### <a name="issue-resolution"></a>Probleemoplossing

Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. Op dit moment worden alleen [beschikkingscodes](../service-management/set-up-disposition-codes.md) waarvoor het veld **Actie** is ingesteld op *Credit* of *Uitval* ondersteund voor gecombineerde nummerplaat ontvangen.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Wanneer ik de periodieke taak Productontvangsten bijwerken uitvoer, worden onbevestigde inkooporders bevestigd.

### <a name="issue-description"></a>Probleembeschrijving

Nadat u de periodieke taak *Productontvangsten bijwerken* hebt uitgevoerd, bevestigt het systeem automatisch onbevestigde inkooporders met de voorraadtransactiestatus *Geregistreerd*.

### <a name="issue-resolution"></a>Probleemoplossing

Met een nieuwe functie voor verwerking van inkomende ladingen, *Meerontvangst voor ladinghoeveelheden*, wordt dit probleem opgelost. Als u deze functies wilt inschakeln, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de volgende functies in (in de volgorde waarin ze staan):

1. Voorraadtransacties van inkooporder koppelen aan lading
1. Te grote ontvangst van laadhoeveelheden

Zie [Geregistreerde ladinghoeveelheden boeken op inkooporders](inbound-load-handling.md#post-registered-quantities) voor meer informatie.
