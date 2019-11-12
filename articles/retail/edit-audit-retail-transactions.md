---
title: Transacties detailhandelwinkel bewerken en controleren
description: In dit onderwerp wordt de functionaliteit beschreven voor het bewerken en controleren van transacties voor detailhandelwinkels.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0201d31cd83b4360f96a7d8e2113caf9d913715
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622522"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Transacties detailhandelwinkel bewerken en controleren

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Dynamics 365 Retail-klanten gebruiken POS-toepassingen (Point of Sale) van dezelfde en andere leveranciers. Met de POS-toepassing van dezelfde leverancier worden winkeltransacties uit de kanalen in Retail Headquarters binnengehaald via een batchproces. Met toepassingen van derden worden transacties in Retail Headquarters binnengehaald via integratie. In beide gevallen moet er nadat transacties in Retail Headquarters zijn binnengehaald, een consistentiecontrole met meerdere validaties op de transacties worden uitgevoerd, zodat het overzicht dat in Retail Headquarters wordt geboekt alleen gevalideerde transacties bevat. 

De validatie van detailhandeltransacties kan om verschillende redenen mislukken. Een fout in de integratiecode of een fout in de POS-toepassing kan bijvoorbeeld leiden tot inconsistente gegevens. En een gebruikersfout, zoals het verwijderen van een product nadat het is gesynchroniseerd met het kanaal of het afsluiten van een boekperiode zonder dat er transacties voor deze periode worden geboekt, kan inconsistente gegevens veroorzaken.

Deze transacties worden gemarkeerd en niet opgenomen in de overzichten, maar kunnen het dagelijkse proces verstoren van het boeken van de detailhandelverkopen naar de financiële gegevens.

In Retail kunt u de specifieke detailhandeltransacties die niet worden gevalideerd, bewerken tijdens het controleren van alle wijzigingen. 

## <a name="edit-and-audit-transactions"></a>Transacties bewerken en controleren

In Retail versie 10.0.5 zijn contante transacties zoals verkopen en retouren, de enige transacties die kunnen worden bewerkt. Het bewerken van klantorders of online orders wordt niet ondersteund. In Retail versie 10.0.6 en hoger wordt het bewerken van beheertransacties voor contanten ook ondersteund.

1. Installeer de Dynamics Excel-invoegtoepassing.

2. Ga naar het werkgebied **Financiën van detailhandelwinkel**. De tegel **Mislukte transactievalidaties** biedt een vooraf gefilterde weergave van het formulier met de detailhandeltransactie die niet is geslaagd voor een of meer validatieregels.
 
3. Open het formulier. Klik op de record waarvoor de validatie is mislukt. Klik op **Office-invoegtoepassing** en klik vervolgens op **Geselecteerde transactie bewerken**. Een Excel-bestand met de details van de geselecteerde transactie wordt geopend met de volgende werkbladen:

    - Regels: dit werkblad bevat de koptekst- en productregels en gerelateerde gegevens voor de transactie.
    - Betalingen: dit werkblad bevat de details van de betalingsregels voor de transactie.
    - Kortingen: dit werkblad bevat de details over de kortingen voor de transactie.
    - Belastingen: dit werkblad bevat de details over de belastingen voor de transactie.
    - Toeslagen: dit werkblad bevat de gegevens over de toeslagen voor de transactie.

4. In het Excel-bestand wijzigt u de betreffende velden en uploadt u de gegevens weer naar Retail Headquarters met de publicatiefunctionaliteit van de Dynamics Excel-invoegtoepassing. Na de publicatie worden de wijzigingen weergegeven in het systeem. Tijdens het publiceren worden er geen validaties uitgevoerd voor wijzigingen door gebruikers.

5. U kunt een volledig controlespoor van de wijzigingen bekijken door te klikken op **Audittrail weergeven** in de koptekst **Detailhandelstransactie** voor wijzigingen op koptekstniveau en in de relevante sectie en record op de desbetreffende transactiepagina. Alle wijzigingen met betrekking tot verkoopregels worden bijvoorbeeld weergegeven op de pagina **Verkooptransacties**, wijzigingen met betrekking tot betalingen worden weergegeven op de pagina **Betalingstransacties**, enzovoort. De volgende controledetails worden bijgehouden voor de wijzigingen.

   - Wijzigingsdatum en -tijd
   - Veld 
   - Oude waarde
   - Nieuwe waarde
   - Gewijzigd door

6. Nadat de wijzigingen zijn aangebracht en gepubliceerd, voert u de optie **Winkeltransacties valideren** opnieuw uit om te controleren of de aangebrachte wijzigingen consistent en geldig zijn.

> [!NOTE]
> U kunt alleen transacties bewerken waarvoor de validatie is mislukt. Als u transacties wilt bewerken die zijn gevalideerd, wijzigt u de validatiestatus van de transactie die u wilt wijzigen in **Fout** of **Geen**. Vervolgens kunt u deze bewerken. 


## <a name="bulk-edit-transactions"></a>Bulksgewijs bewerken van transacties

In Retail versie 10.0.6 en hoger wordt de optie voor het bulksgewijs bewerken van detailhandeltransacties op overzichtsniveau ondersteund. 

1. Gebruik de invoegtoepassing Excel om een overzicht te openen met transacties die u wilt wijzigen met behulp van stap 1-3 hierboven.

2. Kies een van de onderstaande opties.

    - **Contante transacties bewerken**. Met deze optie kunt u alle contante transacties bewerken die in het overzicht zijn opgenomen. De volgende Excel-werkbladen zijn beschikbaar.
    
       - **Transactie**: dit werkblad bevat alle informatie op koptekstniveau voor de verkooptransacties.
       - **Verkooptransactie**: dit werkblad bevat alle informatie op regelniveau voor de verkooptransacties.
       - **Betalingstransacties**: dit werkblad bevat alle informatie over betalingsregels voor de verkooptransacties.
       - **Kortingstransacties**: dit werkblad bevat alle informatie over kortingsregels voor de verkooptransacties.
       - **Belastingtransacties**: dit werkblad bevat alle informatie over belastingregels voor de verkooptransacties.
       - **Toeslagtransacties**: dit werkblad bevat alle informatie over toeslagregels voor de verkooptransacties.

    - **Transacties voor beheer van contant geld bewerken**. Met deze optie kunt u alle beheertransacties voor contant geld bewerken die in het overzicht zijn opgenomen. De volgende Excel-werkbladen zijn beschikbaar.
     
       - **Transactie**: dit werkblad bevat alle informatie op het koptekstniveau voor de beheertransacties van contant geld.
       - **Banktransacties betalingsmethode**: dit werkblad bevat alle transactiedetails voor bankstortingen.
       - **Kluistransacties betalingsmethode**: dit werkblad bevat alle transactiedetails voor kluisstortingen.
       - **Kascontrole**: dit werkblad bevat alle transactiedetails voor kascontroles.
       - **Inkomsten-/uitgaventransacties**: dit werkblad bevat alle details van de transactieregels voor inkomsten en uitgaven.
       - **Betalingstransacties**: dit werkblad bevat alle betalingsgerelateerde informatie voor de bewerking **Factuur betalen** en over inkomsten-/uitgaventransacties.

3.  Er worden geen validaties uitgevoerd wanneer u in bulk bewerkte transacties publiceert. U moet ervoor zorgen dat alle bewerkingen juist zijn en dat de betrouwbaarheid van de gegevens in de werkbladen behouden blijft. Als u bijvoorbeeld de transactiedatum wilt wijzigen voor scenario's waarin de fiscale of voorraadperiode voor de openstaande detailhandeltransacties wordt gesloten, moet u de datum wijzigen in alle Excel-werkbladen die de kolom **Werkdatum** bevatten. Als u transacties wilt valideren nadat deze zijn bewerkt, gebruikt u **Transacties opnieuw valideren** op de pagina **Detailhandeloverzichten**.
