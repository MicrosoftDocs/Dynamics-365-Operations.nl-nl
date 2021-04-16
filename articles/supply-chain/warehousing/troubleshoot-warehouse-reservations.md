---
title: Problemen met reserveringen in magazijnbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnreserveringen in Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828101"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Problemen met reserveringen in magazijnbeheer oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnreserveringen in Microsoft Dynamics 365 Supply Chain Management.

Zie [Problemen met magazijnbatch- en seriereserveringshiërarchieën oplossen](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) voor onderwerpen die betrekking hebben op batch- en serienummerregistraties.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Ik krijg het volgende foutbericht: "Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen."

### <a name="issue-description"></a>Probleembeschrijving

U kunt de reservering van voorraad op een verkoopregel niet verwijderen, omdat er openstaand werk is voor de regel.

### <a name="issue-resolution"></a>Probleemoplossing

Controleer of er openstaand werk van een verpakkingsgroep bestaat om het artikel van een inpakstation naar een andere locatie te brengen (bijvoorbeeld *Laaddeur*). Bekijk de records in het **Historielogboek van werkaanmaak** en de pagina's **Werkgegevens** om te bepalen wat het is dat fysiek de voorraad reserveert en voer vervolgens de voltooiing of verwijdering van het werk uit om de reservering vrij te maken.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Het volgende foutbericht wordt weergegeven: "Voorraadhoeveelheid -%1 kan niet worden bijgewerkt vanwege onvoldoende voorraadtransacties voor artikel %2...."

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn. Hier volgt de hele tekst van het volledige foutbericht:

> Voorraad hoeveelheid -%1 kan niet worden bijgewerkt vanwege onvoldoende voorraadtransacties voor artikel %2 met dimensies Grootte =%3, Kleur=%4, Toevoegingen=%5, Site=%6, Magazijn=%7, Locatie=%8, Voorraadstatus=beschikbaar, Nummerplaat=%9, Batchnummer=%10 voor verwijzing-id %11 op partij-id %12.

### <a name="issue-resolution"></a>Probleemoplossing

Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren. Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Het volgende foutbericht wordt weergegeven: "Fysieke voorhanden...kan niet worden gereserveerd omdat slechts 0,00 in de voorraad beschikbaar zijn."

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn. Hier volgt de hele tekst van het volledige foutbericht:

> Fysiek voorhanden Site=%1, Magazijn=%2, Voorraadstatus=beschikbaar, Batchnummer=%3, Eigenaar=%4: %5 kan niet worden gereserveerd omdat slechts 0,00 in de voorraad beschikbaar zijn.

### <a name="issue-resolution"></a>Probleemoplossing

Dit probleem wordt waarschijnlijk veroorzaakt door openstaand werk. Voltooi het werk of ontvang een taak zonder werk te maken. Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren. Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
