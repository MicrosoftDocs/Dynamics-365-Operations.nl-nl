---
title: Een consignatieaanvullingsorder maken
description: In dit artikel wordt uitgelegd hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a1d0a7d322b17d3d80dd9fade2b037dd148d9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859368"
---
# <a name="create-a-consignment-replenishment-order"></a>Een consignatieaanvullingsorder maken

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren. Het laat ook zien hoe u een ontvangst van producten registreert zodat de consignatievoorraad als voorhanden voorraad wordt geregistreerd die eigendom is van de leverancier. Deze procdure wordt gewoonlijk uitgevoerd door een inkoper. U kunt deze begeleiding gebruiken in het demobedrijf USMF. Deze procedure is voor een functie die in Dynamics 365 for Operations, versie 1611 is toegevoegd.

## <a name="create-a-consignment-replenishment-order"></a>Een consignatieaanvullingsorder maken
1. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Consignatie > Consignatieaanvullingsorders**.
2. Selecteer **Nieuw**.
3. In het veld **Leveranciersrekening** selecteert u leverancier **US-104** (u moet een leverancier selecteren die als eigenaar wordt vermeld op de pagina **Voorraadeigenaren**). 
4. Selecteer **OK**.
5. Selecteer **Regel toevoegen**.
6. Typ `M9211CI` in het veld **Artikelnummer** (u moet een artikel selecteren dat is ingesteld voor consignatievoorraad).
7. Voer een getal in het veld **Hoeveelheid** in.
8. Typ een datum in het veld **Gevraagde leveringsdatum**. De aangevraagde en bevestigde datums worden door de MRP-engine gebruikt voor de verwachte ontvangst van de goederen.  
9. Typ een datum in het veld **Bevestigde leveringsdatum**.
10. Vouw de sectie **Regeldetails** uit.
11. Selecteer het tabblad **Voorraaddimensies**.
12. Vernieuw de pagina om de eigenaar weer te geven in het veld **Eigenaar voorraaddimensies**. Leverancier US-104 is nu vermeld als de eigenaar.  

## <a name="check-the-inventory-transaction-status"></a>Controleer de status van de voorraadtransactie
1. Selecteer **Voorraadmodel**.
2. Selecteer **Transacties**.
3. In de gewenste rij is het veld **Ontvangst** op **Besteld** ingesteld.  
4. Sluit de pagina.

## <a name="receive-items"></a>Artikelen ontvangen
1. Selecteer **Productontvangstbon**.
2. Typ een waarde in het veld **Externe productontvangstbon**.
3. Typ in het veld **Hoeveelheid** een aantal dat lager is dan het aantal dat hier wordt weergegeven. 
4. Selecteer **OK**.

## <a name="check-the-on-hand-inventory"></a>Controleer de voorhanden voorraad
1. Selecteer **Voorraadmodel**.
2. Selecteer **Voorhanden**.
3. Selecteer **Overzicht**. De artikelen die zijn ontvangen als consignatievoorraad en die eigendom zijn van de leverancier, zijn voorhanden in de voorraad. De resterende hoeveelheid op de consignatieaanvullingsorder wordt weergegeven in het veld **Totaal van order**.  
4. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]