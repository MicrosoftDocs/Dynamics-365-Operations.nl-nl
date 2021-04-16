---
title: Problemen met uitgaande magazijnbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met uitgaande magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 919b6f433db47f24adc9a474942557a1467d1f71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828173"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Problemen met uitgaande magazijnbewerkingen oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met uitgaande magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Het volgende fout bericht wordt weergegeven: "Verkooporder kan niet worden vrijgegeven."

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem kan zich om verschillende redenen voordoen. De order bevindt zich bijvoorbeeld in kredietbeheerblokkering en er kunnen geen zendingen worden gemaakt totdat een geldig postadres is ingevoerd voor alle verkoopregels die aan een verkooporder zijn gekoppeld. Er is ook een orderblokkering die moet worden opgeheven voordat de order aan het magazijn kan worden vrijgegeven. Deze blokkering kan orderspecifiek zijn of kan zich op de klantrekening bevinden.

### <a name="issue-resolution"></a>Probleemoplossing

Voeg het adres toe of werk het bij op de verkooporder en de orderregels en geef vervolgens de order vrij aan het magazijn. Orders kunnen alleen aan het magazijn worden vrijgegeven als ze een geldig afleveradres hebben (volgens de instelling van de adresnotatie in de module **Organisatiebeheer**).

Onderzoek de orderblokkering en los de problemen op. Vervolgens verwijdert u de blokkering van de order of klant en geeft u de order vrij aan het magazijn.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Het volgende bericht wordt weergegeven: "De zending voor de lading 1% is bevestigd." Er worden echter geen regels geboekt.

### <a name="issue-description"></a>Probleembeschrijving

Een zending in een lading is bevestigd, maar er is geen verdere boeking uitgevoerd.

### <a name="issue-resolution"></a>Probleemoplossing

De zendingsbevestiging heeft geen invloed op de boeking. Hiermee wordt alleen de zendings- en ladingstatus bijgewerkt. De boeking moet plaatsvinden in een afzonderlijk proces.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Het volgende foutbericht wordt weergegeven: "Rechtstreekse levering verwerken kan niet voor magazijn 1% omdat magazijnbeheer is ingeschakeld. Geef een ander magazijn op waarvoor magazijnbeheer niet is ingeschakeld."

### <a name="issue-description"></a>Probleembeschrijving

Er wordt een artikel toegevoegd aan een verkoopregel voor rechtstreekse levering vanuit een magazijn dat is ingeschakeld voor magazijnbeheer (WMS). Dit foutbericht wordt weergegeven wanneer de verkoopregel wordt bijgewerkt. 

### <a name="issue-resolution"></a>Probleemoplossing

Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. In WMS wordt rechtstreekse levering momenteel niet ondersteund. Als u rechtstreekse levering wilt gebruiken, moet u dus een niet-WMS artikel en -magazijn selecteren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]