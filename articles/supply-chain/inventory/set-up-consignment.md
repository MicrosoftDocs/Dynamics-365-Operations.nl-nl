---
title: Consignatie instellen
description: In dit onderwerp wordt uitgelegd hoe u bewerkingen voor inkomende consignatievoorraad configureert.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 51f7d6b0402ebbed417554978fc8d927f6b9c606
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207204"
---
# <a name="set-up-consignment"></a>Consignatie instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u bewerkingen voor inkomende consignatievoorraad configureert.

De consignatievoorraad is de voorraad die eigendom is van een leverancier, maar die op uw locatie is opgeslagen. Wanneer u klaar bent om de voorraad te verbruiken of te gebruiken, neemt u het eigendom van de voorraad over. In dit onderwerp worden de instellingen beschreven die nodig zijn voor consignatieprocessen. Meer informatie over consignatieprocessen vindt u in [Consignatie instellen](consignment.md).

## <a name="inventory-owners"></a>Voorraadeigenaren
Om fysieke binnenkomende consignatievoorraad te kunnen registreren, moet u een leverancier/eigenaar definiëren. Dit doet u op de pagina **Voorraadeigenaar**. Als u een **Leveranciersaccount** selecteert, worden standaardwaarden gegenereerd voor de velden **Naam** en **Eigenaar**. De waarde in het veld **Eigenaar** is zichtbaar voor de leverancier. Het kan nuttig zijn om deze waarde te wijzigen, als de namen van uw leveranciersaccounts niet eenvoudig herkenbaar zijn voor externe partijen. U kunt de waarde in het veld **Eigenaar** bewerken, maar alleen tot het moment dat u de **Voorraadeigenaar**-record opslaat. In het veld **Naam** wordt de naam ingevuld van de partij waaraan de leveranciersaccount is gekoppeld. Deze waarde kan niet worden gewijzigd.

[![Voorraadeigenaren](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Traceringsdimensiegroep
Artikelen die in consignatieprocessen worden gebruikt, moeten zijn gekoppeld aan een **Traceringsdimensiegroep** waarvoor de dimensie **Eigenaar** is ingesteld op **Actief**. Voor de dimensie Eigenaar zijn altijd de opties **Fysieke voorraad** en **Financiële voorraad** geselecteerd. De optie **In behoefteplan opnemen volgens dimensie** is nooit geselecteerd.

[![Traceringsdimensiegroep](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Journaal voor wijzigingen aan voorraadeigendom
In het journaal **Wijziging aan voorraadeigendom** wordt de overdracht van eigendom van de consignatievoorraad geregistreerd van de leverancier naar de rechtspersoon die de voorraad gebruikt. Net als bij andere voorraadjournaals moet het worden geïdentificeerd met de naam van een voorraadjournaal. Deze namen maakt u aan op de pagina **Voorraadjournaalnamen**. Het **Journaaltype** moet worden ingesteld op **Wijziging aan eigendom**.

[![journaal-wijziging-voorraadeigendom](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverancierssamenwerking in consignatieprocessen
Als uw leveranciers de interface van de leverancierssamenwerking gebruiken, kunnen ze daarmee het verbruik van voorraad op uw locatie volgen. Zie [Gebruikersbeveiliging in leveranciersportal](../procurement/configure-security-vendor-portal-users.md) voor meer informatie over het configureren van leveranciers voor leverancierssamenwerking.
