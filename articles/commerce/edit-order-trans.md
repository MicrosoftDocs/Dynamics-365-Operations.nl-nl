---
title: Online orders en asynchrone ordertransacties van klanten bewerken en controleren
description: In dit onderwerp wordt beschreven hoe online orders en asynchrone ordertransacties van klanten in Microsoft Dynamics 365 Commerce kunnen worden bewerkt en gecontroleerd.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 8fa6f7a71bae759e2b8feb3c5778200bb7bdbfe9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010146"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Online orders en asynchrone ordertransacties van klanten bewerken en controleren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe online orders en asynchrone ordertransacties van klanten in Microsoft Dynamics 365 Commerce kunnen worden bewerkt en gecontroleerd.

## <a name="overview"></a>Overzicht

Tussen Commerce-versies 10.0.5 en 10.0.6 is ondersteuning toegevoegd voor het bewerken van contante transacties (zoals verkopen en retouren) en beheertransacties in contant geld (zoals wisselgeld invoeren en verwijderen). In Commerce versie 10.0.7 is ondersteuning toegevoegd voor het bewerken van online ordertransacties en asynchrone klantordertransacties.

## <a name="edit-and-audit-order-transactions"></a>Ordertransacties bewerken en controleren

Voer de volgende stappen uit om ordertransacties in Commerce Headquarters te bewerken en te controleren.

1. Installeer de [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Geef op de pagina **Detailhandelparameters** op het tabblad **Klantorders** op het sneltabblad **Order** een wachtcode op voor **Wachtcode voor ordersynchronisatiefouten**.
1. Open het werkgebied **Financiën van winkel**. De tegels **Synchronisatiefouten voor online orders** en **Synchronisatiefouten voor klantorders** bieden een vooraf gefilterde weergave van de pagina met detailhandelstransacties. Elke tegel toont de transactierecords die niet zijn gesynchroniseerd voor het bijbehorende ordertype.
1. Open de pagina **Synchronisatiefouten voor online orders** of de pagina **Synchronisatiefouten voor klantorders**. Selecteer een record om de details van de synchronisatiefout weer te geven. Het sneltabblad **Synchronisatiestatus** bevat de volgende foutdetails:

    - Orderstatus in behandeling
    - Details orderfout
    - Wijzigingsdatum en -tijd
    - Aantal nieuwe pogingen

1. Als de foutdetails aangeven dat de record moet worden hersteld, selecteert u **Office Add-in** en vervolgens **Geselecteerde transactie bewerken**. Er wordt een Excel-bestand geopend met de details van de geselecteerde transactie.

    - Als de transactie die wordt bewerkt een online ordertransactie is, bevat het Excel-bestand de volgende werkbladen:

        - **Transactie:** dit werkblad bevat de details over de koptekst voor de transactie.
        - **Verkooptransactie:** dit werkblad bevat de regeldetails voor de transactie.
        - **Betalingstransacties**: dit werkblad bevat de details van de betalingsregels voor de transactie.
        - **Kortingstransacties**: dit werkblad bevat de details over de kortingen voor de transactie.
        - **Belastingsstransacties**: dit werkblad bevat de details over de belasting voor de transactie.
        - **Toeslagtransacties**: dit werkblad bevat de gegevens over de toeslagen voor de transactie.

    - Als de transactie die wordt bewerkt een asynchrone klantordertransactie is, bevat het Excel-bestand de volgende werkbladen:

        - **Regels:** dit werkblad bevat de koptekst- en regeldetails voor de transactie.
        - **Betalingen**: dit werkblad bevat de details van de betalingsregels voor de transactie.
        - **Kortingen**: dit werkblad bevat de details over de kortingen voor de transactie.
        - **Belastingen**: dit werkblad bevat de details over de belastingen voor de transactie.
        - **Toeslagen**: dit werkblad bevat de gegevens over de toeslagen voor de transactie.

1. Voer in het Excel-bestand in het veld **Orderstatus in behandeling** **Bewerken** in en publiceer de wijziging. Op deze manier voorkomt u dat deze record tijdens de verwerking wordt overgeslagen door de taak **Order synchroniseren** die wordt uitgevoerd in batchmodus.
1. In het Excel-bestand wijzigt u de betreffende velden en uploadt u de gegevens weer naar Commerce Headquarters met de publicatiefunctionaliteit van de Dynamics Excel-invoegtoepassing. Na de publicatie van de gegevens worden de wijzigingen weergegeven in het systeem. Tijdens het publiceren worden er geen validaties uitgevoerd voor wijzigingen door gebruikers.
1. U kunt een volledig audittrail van de wijzigingen bekijken door **Audittrail weergeven** te selecteren in de koptekst **Detailhandelstransactie** voor wijzigingen op koptekstniveau en in de relevante sectie en record op de desbetreffende transactiepagina. Alle wijzigingen die betrekking hebben op verkoopregels worden bijvoorbeeld weergegeven op de pagina **Verkooptransacties** en alle wijzigingen die verband houden met betalingen worden weergegeven op de pagina **Betalingstransacties**. Voor de wijzigingen worden de volgende controlegegevens bijgehouden:

    - Wijzigingsdatum en -tijd
    - Veld
    - Oude waarde
    - Nieuwe waarde
    - Gewijzigd door

1. Nadat u de wijzigingen hebt aangebracht en gepubliceerd, selecteert u **Order synchroniseren** om het synchronisatieproces onmiddellijk te starten. U kunt ook wachten tot het synchronisatieproces dat in batchmodus wordt uitgevoerd, de transactie heeft verwerkt.

Nadat de orders met succes zijn gesynchroniseerd, worden ze standaard in een wachtstatus geplaatst op basis van de wachtcode die is gedefinieerd in de Commerce-parameters. De blokkering van de orders moet worden verwijderd voordat de orders verder kunnen worden verwerkt voor afhandeling of andere bewerkingen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Beheer van contante transacties bewerken en controleren](edit-cash-trans.md)

[Financiële dimensies voor detailhandelstransacties bewerken](edit-financial-dim.md)

[Een Excel-werkmap maken om detailhandelstransacties te bewerken](create-excel-edit.md)

[Velden toevoegen aan een Excel-werkmap om detailhandelstransacties te bewerken](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]