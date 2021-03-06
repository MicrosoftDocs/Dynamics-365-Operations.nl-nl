---
title: U kunt een zending niet bevestigen vanwege een probleem met de kalender
description: U kunt een zending niet bevestigen vanwege een probleem met de kalender
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938450"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>U kunt een zending niet bevestigen vanwege een probleem met de kalender

Foutcode: TRX2716

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> Voor het agendatype %1 moet de afspraak %2 worden in- en uitgecheckt.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

Er bestaan actieve afspraken voor de lading. Er is bijvoorbeeld een regel die vereist dat de chauffeur moet inchecken. Daarom bevindt de lading zich momenteel in een staat waarbij de verzendingsbevestiging mislukt.

## <a name="resolution"></a>Oplossing

U moet eventuele problemen onderzoeken en oplossen met de actieve afspraken die aan de lading zijn gekoppeld.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer in het actievenster op het tabblad **Transport** in de groep **Afspraken** de optie **Afspraak plannen**.
1. Volg één van deze stappen:

    - Controleer of voor de afspraak het in- of uitchecken van de chauffeur is voltooid.
    - Voltooi of annuleer de afspraak.
    - Schakel de optie **Inchecken van chauffeur vereist** voor de bijbehorende afspraakregel uit.
