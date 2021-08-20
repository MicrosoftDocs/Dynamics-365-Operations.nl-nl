---
title: Contante transacties en beheertransacties voor contant geld bewerken en controleren
description: In dit onderwerp wordt beschreven hoe contante transacties en beheertransacties voor contant geld in Microsoft Dynamics 365 Commerce kunnen worden bewerkt en gecontroleerd.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 85c4bd4c03b6ac09f2226d1767deabde1879f869e4b7c4d45e4d4c2a1d8effb3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765333"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Contante transacties en beheertransacties voor contant geld bewerken en controleren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe contante transacties en beheertransacties voor contant geld in Microsoft Dynamics 365 Commerce kunnen worden bewerkt en gecontroleerd.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce-klanten gebruiken een POS-toepassing (Point of Sale) van dezelfde leverancier en POS-toepassingen van andere leveranciers. Met de POS-toepassing van dezelfde leverancier worden winkeltransacties uit de kanalen binnengehaald in Commerce Headquarters via een batchproces. Bij toepassingen van derden worden transacties in Commerce Headquarters binnengehaald via integratie. In beide gevallen moet, nadat transacties in Commerce Headquarters zijn binnengehaald, een consistentiecontroleproces worden uitgevoerd. Dit proces voert meerdere validaties uit op de transacties en alleen transacties die met succes zijn gevalideerd, worden in het overzicht opgenomen, zodat ze kunnen worden geboekt in het hoofdkantoor van Commerce.

De validatie van transacties in Commerce kan om verschillende redenen mislukken. Een bug in de integratiecode of in de POS-toepassing kan inconsistente gegevens veroorzaken. Ook kan een gebruikersfout inconsistente gegevens veroorzaken. Een gebruiker verwijdert bijvoorbeeld een product nadat het is gesynchroniseerd met het kanaal of een gebruiker sluit een fiscale periode zonder transacties voor die periode te boeken. Deze transacties worden wel gemarkeerd en niet opgenomen in de overzichten, maar kunnen het dagelijkse proces verstoren van het boeken van de dagelijkse verkopen naar de financiële gegevens. In Commerce kunt u de transacties die niet worden gevalideerd, bewerken terwijl ook alle wijzigingen worden gecontroleerd.

## <a name="edit-transactions"></a>Transacties bewerken

In Commerce versie 10.0.5 gaat het bij transacties die kunnen worden bewerkt om contante transacties zoals verkopen en retouren. Bestellingen van klanten en online bestellingen kunnen niet worden bewerkt. In Commerce versie 10.0.6 en hoger kunnen ook contante beheertransacties worden bewerkt.

Voer de volgende stappen uit om transacties in Commerce Headquarters te bewerken.

1. Installeer de [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Open in Commerce Headquarters het werkgebied **Financiën van winkel**. De tegel **Mislukte transactievalidaties** biedt een vooraf gefilterde weergave van de transactiepagina die niet is geslaagd voor een of meer validatieregels.
1. Open de transactiepagina, selecteer de record waarvan de validatie is mislukt, selecteer **Office Add-in** en vervolgens **Geselecteerde transactie bewerken**. Er wordt een Excel-bestand geopend met de details van de geselecteerde transactie. Dit bestand bevat de volgende werkbladen:

    - **Regels**: dit werkblad bevat de koptekst- en productregels voor de transactie en gerelateerde gegevens voor de transactie.
    - **Betalingen**: dit werkblad bevat de details van de betalingsregels voor de transactie.
    - **Kortingen**: dit werkblad bevat de details over de kortingen voor de transactie.
    - **Belastingen**: dit werkblad bevat de details over de belastingen voor de transactie.
    - **Toeslagen**: dit werkblad bevat de gegevens over de toeslagen voor de transactie.

1. In het Excel-bestand wijzigt u de betreffende velden en uploadt u de gegevens weer naar Commerce Headquarters met de publicatiefunctionaliteit van de Dynamics Excel-invoegtoepassing. Na de publicatie van de gegevens worden de wijzigingen weergegeven in het systeem. Tijdens het publiceren worden er geen validaties uitgevoerd voor wijzigingen door gebruikers.
1. U kunt een volledig audittrail van de wijzigingen bekijken door **Audittrail weergeven** te selecteren in de koptekst **Detailhandelstransactie** voor wijzigingen op koptekstniveau en in de relevante sectie en record op de desbetreffende transactiepagina. Alle wijzigingen die betrekking hebben op verkoopregels worden bijvoorbeeld weergegeven op de pagina **Verkooptransacties** en alle wijzigingen die verband houden met betalingen worden weergegeven op de pagina **Betalingstransacties**. Voor de wijzigingen worden de volgende controlegegevens bijgehouden:

    - Wijzigingsdatum en -tijd
    - Veld
    - Oude waarde
    - Nieuwe waarde
    - Gewijzigd door

1. Nadat de wijzigingen zijn aangebracht en gepubliceerd, voert u de optie **Winkeltransacties valideren** uit om te controleren of de wijzigingen consistent en geldig zijn.

> [!NOTE]
> U kunt alleen transacties bewerken waarvoor de validatie is mislukt. Als u een transactie wilt bewerken die is gevalideerd, wijzigt u de validatiestatus van de transactie die u wilt wijzigen in **Fout** of **Geen** en publiceert u de wijziging. Vervolgens kunt u de gegevens in de koptekst of in andere onderliggende records van de transactie bewerken en de koptekst of records publiceren.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Transacties die zijn gekoppeld aan een overzicht, in bulk bewerken

In Commerce versie 10.0.6 en hoger wordt de optie voor het bulksgewijs bewerken van transacties op overzichtsniveau ondersteund.

Voer deze stappen uit om transacties die zijn gekoppeld aan een overzicht in Commerce Headquarters in bulk te bewerken.

1. Open de pagina **Overzichten** en selecteer het overzicht dat de transacties bevat die moeten worden bewerkt.
1. Selecteer de knop **Openen in Microsoft Office**.
1. Afhankelijk van wat moet worden bewerkt, selecteert u een van de volgende opties:

    - **Contante transacties bewerken**: met deze optie kunt u alle contante transacties in het overzicht bewerken. De volgende Excel-werkbladen zijn beschikbaar:

        - **Transactie**: dit werkblad bevat alle informatie op koptekstniveau voor de verkooptransacties.
        - **Verkooptransactie**: dit werkblad bevat alle informatie op regelniveau voor de verkooptransacties.
        - **Betalingstransacties**: dit werkblad bevat alle informatie over betalingsregels voor de verkooptransacties.
        - **Kortingstransacties**: dit werkblad bevat alle informatie over kortingsregels voor de verkooptransacties.
        - **Belastingtransacties**: dit werkblad bevat alle informatie over belastingregels voor de verkooptransacties.
        - **Toeslagtransacties**: dit werkblad bevat alle informatie over toeslagregels voor de verkooptransacties.

    - **Beheertransacties van contant geld bewerken**: met deze optie kunt u alle beheertransacties van contant geld in het overzicht bewerken. De volgende Excel-werkbladen zijn beschikbaar:

        - **Transactie**: dit werkblad bevat alle informatie op het koptekstniveau voor de beheertransacties van contant geld.
        - **Banktransacties betalingsmethode**: dit werkblad bevat alle transactiedetails voor bankstortingen.
        - **Kluistransacties betalingsmethode**: dit werkblad bevat alle transactiedetails voor kluisstortingen.
        - **Kascontrole**: dit werkblad bevat alle transactiedetails voor kascontroles.
        - **Inkomsten-/uitgaventransacties**: dit werkblad bevat alle details van de transactieregels voor inkomsten en uitgaven.
        - **Betalingstransacties**: dit werkblad bevat alle betalingsgerelateerde informatie voor de bewerking **Factuur betalen** en over inkomsten-/uitgaventransacties.

1. Bewerk de vereiste transacties.

    > [!NOTE]
    > Er worden geen validaties uitgevoerd wanneer u in bulk bewerkte transacties publiceert. U moet ervoor zorgen dat alle bewerkingen juist zijn en dat de betrouwbaarheid van de gegevens in de werkbladen behouden blijft. Als u bijvoorbeeld de transactiedatum wilt wijzigen voor scenario's waarin de fiscale of voorraadperiode voor de openstaande transacties wordt gesloten, moet u de datum wijzigen in alle Excel-werkbladen die de kolom **Werkdatum** bevatten. Als u transacties wilt valideren nadat deze zijn bewerkt, selecteert u **Transacties opnieuw valideren** op de pagina **Overzichten**. Wacht tot de validatietaak is voltooid voordat u de instructie plaatst.

1. Als de aggregatie al is gegenereerd, opent u de pagina **Geaggregeerde transacties** en selecteert u **XML voor verkooporders regenereren**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Transacties die niet zijn gekoppeld aan een overzicht, in bulk bewerken

Commerce versie 10.0.10 en hoger ondersteunen de optie om transacties in bulk te bewerken waarvan de validatie is mislukt, maar die niet aan een overzicht zijn gekoppeld.

Voer deze stappen uit om transacties die niet zijn gekoppeld aan een overzicht in Commerce Headquarters in bulk te bewerken.

1. Open de pagina **Alle winkels** en selecteer de winkel waarvoor transacties moeten worden bewerkt.
1. Selecteer de knop **Openen in Microsoft Office** en selecteer vervolgens **Contante transacties bewerken**.
1. Bewerk de vereiste transacties en publiceer ze.

## <a name="additional-resources"></a>Aanvullende bronnen

[Online orders en asynchrone ordertransacties van klanten bewerken en controleren](edit-order-trans.md)

[Financiële dimensies voor detailhandelstransacties bewerken](edit-financial-dim.md)

[Een Excel-werkmap maken om detailhandelstransacties te bewerken](create-excel-edit.md)

[Velden toevoegen aan een Excel-werkmap om detailhandelstransacties te bewerken](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]