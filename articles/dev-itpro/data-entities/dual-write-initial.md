---
title: Uitvoeringsvolgorde voor de eerste synchronisatie van Finance and Operations en Common Data Service
description: In dit onderwerp wordt de synchronisatievolgorde aangegeven die u moet volgen om de eerste gegevens te maken.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873123"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Uitvoeringsvolgorde voor de eerste synchronisatie van Finance and Operations en Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Voordat u gegevensintegratie gebruikt, moet u de eerste gegevens maken die vereist zijn voor klanten, leveranciers en contactpersonen. U wilt bijvoorbeeld een nieuw **Leveranciersgroepartikel** maken en de **Betalingscondities** instellen op **Net30.** Voordat u het artikel in de **Leveranciersgroep** gaat maken, moet u er in dat geval voor zorgen dat **Net30** bestaat in zowel Microsoft Dynamics 365 for Finance and Operations en Common Data Service. (In de toekomst zal Microsoft in het platform Twee keer wegschrijven een functionaliteit met de naam Initiële synchronisatie uitbrengen. Deze functie voert een eenmalige gegevenssynchronisatie uit tussen Finance and Operations en Common Data Service als onderdeel van Twee keer wegschrijven.)

> [!TIP]
> Microsoft geeft een toewijzing voor Twee keer wegschrijven uit voor alle referentiegegevens, inclusief **Betalingscondities** (betalingscondities). Als u de initiële gegevens al in één systeem hebt, kan een kleine updatebewerking van een record Twee keer wegschrijven voor die record activeren.

U moet de volgende prioriteitsvolgorde volgen en ervoor zorgen dat de eerste gegevens beschikbaar zijn in zowel Finance and Operations als Common Data Service.

## <a name="vendor"></a>Leverancier

Dit is de volgorde van uitvoering voor de entiteit **Leverancier**:

1. Leveranciersgroep

    1. Betalingstermijn

        1. Betalingsdag en -regels
        2. Betalingsplanning

2. Leveranciersbetalingsmethode

## <a name="customer-organization"></a>Klant (organisatie)

Dit is de volgorde van uitvoering voor de entiteit **Klant**:

1. Klantgroep

    1. Betalingstermijn

        1. Betalingsdag en -regels
        2. Betaling 

2. Betalingsmethode van klant

## <a name="contact-person"></a>Contactpersoon (persoon)

Dit is de volgorde van uitvoering voor de entiteit **Contactpersoon**:

1. Klant
2. Leverancier
