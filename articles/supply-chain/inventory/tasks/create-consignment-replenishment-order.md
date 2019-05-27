---
title: Een consignatieaanvullingsorder maken
description: Deze procedure laat zien hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3e33008d04ea8bb7d145c7b63cec23a4a45dd2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549869"
---
# <a name="create-a-consignment-replenishment-order"></a>Een consignatieaanvullingsorder maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren. Het laat ook zien hoe u een ontvangst van producten registreert zodat de consignatievoorraad als voorhanden voorraad wordt geregistreerd die eigendom is van de leverancier. Deze procdure wordt gewoonlijk uitgevoerd door een inkoper. U kunt deze begeleiding gebruiken in het demobedrijf USMF. Deze procedure is voor een functie die in Dynamics 365 for Operations, versie 1611 is toegevoegd.




## <a name="create-a-consignment-replenishment-order"></a>Een consignatieaanvullingsorder maken
1. Ga naar Inkoop en sourcing > Consignatie > Consignatieaanvullingsorders.
2. Klik op Nieuw.
3. Selecteer in het veld Leveranciersrekening de leverancier US-104.
    * U moet een leverancier selecteren die als eigenaar is geregistreerd op de pagina Voorraadeigenaren.  
4. Klik op OK.
5. Klik op Regel toevoegen.
6. Typ M9211CI in het veld Artikelnummer.
    * U moet een artikel selecteren dat is ingesteld voor consignatievoorraad.  
7. Voer in het veld Hoeveelheid een getal in.
8. Typ een datum in het veld Gevraagde leveringsdatum.
    * De aangevraagde en bevestigde datums worden door de MRP-engine gebruikt voor de verwachte ontvangst van de goederen.  
9. Typ een datum in het veld Bevestigde leveringsdatum.
10. Vouw de sectie Regeldetails uit.
11. Klik op het tabblad Voorraaddimensies.
12. Vernieuw de pagina om de eigenaar weer te geven in het veld Eigenaar voorraaddimensies.
    * Leverancier US-104 is nu vermeld als de eigenaar.  

## <a name="check-the-inventory-transaction-status"></a>Controleer de status van de voorraadtransactie
1. Klik op Voorraad.
2. Klik op Transacties.
3. Markeer in de lijst de geselecteerde rij.
    * Let op dat het veld Ontvangst op Besteld is ingesteld.  
4. Sluit de pagina.

## <a name="receive-items"></a>Artikelen ontvangen
1. Klik op Productontvangstbon.
2. Typ een waarde in het veld Externe productontvangstbon.
3. Typ in het veld Hoeveelheid een aantal dat lager is dan het aantal dat hier wordt weergegeven. 
4. Klik op OK.

## <a name="check-the-on-hand-inventory"></a>Controleer de voorhanden voorraad
1. Klik op Voorraad.
2. Klik op Voorhanden.
3. Klik op Overzicht.
    * De artikelen die zijn ontvangen als consignatievoorraad en die eigendom zijn van de leverancier, zijn voorhanden in de voorraad. De resterende hoeveelheid op de consignatieaanvullingsorder wordt weergegeven in het veld Totaal van order.  
4. Sluit de pagina.
5. Klik op Sluiten.

