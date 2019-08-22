---
title: Uitvoeringsvolgorde voor de eerste sychronisatie van Finance and Operations en Common Data Service
description: In dit onderwerp wordt de synchronisatievolgorde aangegeven van die u moet volgen om de eerste gegevens te maken.
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797293"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Uitvoeringsvolgorde voor de eerste sychronisatie van Finance and Operations en Common Data Service

Voordat u gegevensintegratie gebruikt, moet u de eerste gegevens maken die vereist zijn voor klanten, leveranciers en contactpersonen. Als u bijvoorbeeld een nieuw **Leveranciergroep**-item wilt maken en de **betalingsvoorwaarden** wilt instellen op **Net30**, moet u er eerst voor zorgen dat **Net30** bestaat in Finance and Operations en Common Data Service voordat u probeert het **Leveranciergroep**-item te maken. (In de toekomst zullen we een in het platform Twee keer wegschrijven een functionaliteit met de naam **Initiële synchronisatie**uitbrengen om als onderdeel van de installatie van Twee keer wegschrijven een eenmalige gegevenssynchronisatie uit te voeren tussen Finance and Operations en Common Data Service.)

Tips: we geven een toewijzing voor Twee keer wegschrijven uit voor alle referentiegegevens, inclusief **Betalingsvoorwaarden** (betalingsvoorwaarden). Als u de initiële gegevens al in één systeem hebt, kan een kleine updatebewerking van een record Twee keer wegschrijven voor die record activeren. 

U moet de volgende prioriteitsvolgorde volgen en ervoor zorgen dat de eerste gegevens beschikbaar zijn op zowel Finance and Operations als Common Data Service.   

## <a name="vendor"></a>Leverancier

De volgorde van uitvoering voor Leverancier is:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Klant (organisatie)

De volgorde van uitvoering voor Klant is:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Contactpersoon (persoon)

De volgorde van uitvoering voor Contactpersoon is:

```
Customer
Vendor               
```
