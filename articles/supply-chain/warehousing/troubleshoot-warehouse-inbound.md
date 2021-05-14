---
title: Problemen met inkomende magazijnbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomende magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920982"
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

Met een nieuwe functie voor verwerking van inkomende ladingen, *Meerontvangst voor ladinghoeveelheden*, wordt dit probleem opgelost. Als u deze functies wilt inschakelen, ga naar het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakel de volgende functies in (in de volgorde waarin ze staan vermeld):

1. Voorraadtransacties van inkooporder koppelen aan lading
1. Te grote ontvangst van laadhoeveelheden

Zie [Geregistreerde ladinghoeveelheden boeken op inkooporders](inbound-load-handling.md#post-registered-quantities) voor meer informatie.

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Wanneer ik inkomende orders registreer, krijg ik het volgende foutbericht: 'De hoeveelheid is niet geldig'.

### <a name="issue-description"></a>Probleembeschrijving

Als het veld **Groeperingsbeleid nummerplaten** is ingesteld op *Door gebruiker gedefinieerd* voor een menu-item voor mobiele apparaten dat wordt gebruikt om inkomende orders te registreren, ontvangt u een foutbericht ('De hoeveelheid is niet geldig') en kunt u de registratie niet voltooien.

### <a name="issue-cause"></a>Oorzaak van probleem

Wanneer *Door gebruiker gedefinieerd* wordt gebruikt als groeperingsbeleid voor kentekenplaten, splitst het systeem de inkomende voorraad op in afzonderlijke nummerplaten, zoals aangegeven door de eenheidsvolgordegroep. Als batch- of serienummers worden gebruikt om het artikel bij te houden dat wordt ontvangen, moeten de hoeveelheden van elke batch of serie worden opgegeven per nummerplaat die is geregistreerd. Als de hoeveelheid die is opgegeven voor een nummerplaat groter is dan de hoeveelheid die nog moet worden ontvangen voor de huidige dimensies, wordt het foutbericht weergegeven.

### <a name="issue-resolution"></a>Probleemoplossing

Wanneer u een artikel registreert met behulp van een menu-item voor mobiele apparaten waarbij het veld **Groeperingsbeleid nummerplaten** is ingesteld op *Door gebruiker gedefinieerd*, moet u mogelijk nummerplaatnummers, batchnummers of serienummers bevestigen of invoeren.

Op de bevestigingspagina van de nummerplaat toont het systeem de hoeveelheid die is toegewezen voor de huidige nummerplaat. Op de bevestigingspagina's voor batch- of serienummers toont het systeem de hoeveelheid die nog moet worden ontvangen voor de huidige nummerplaat. Het bevat ook een veld waarin u de hoeveelheid kunt invoeren die u wilt registreren voor die combinatie van nummerplaat en batch- of serienummer. Zorg er in dat geval voor dat de hoeveelheid die wordt geregistreerd voor de nummerplaat niet groter is dan de hoeveelheid die nog moet worden ontvangen.

Als er te veel nummerplaten worden gegenereerd bij inkomende orderregistratie, kan de waarde van het veld **Groeperingsbeleid nummerplaten** worden gewijzigd in *Nummerplaatgroepering*, kan een nieuwe eenheidsvolgordegroep aan het artikel worden toegewezen of kan de optie **Nummerplaatgroepering** worden gedeactiveerd voor de eenheidsvolgordegroep.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
