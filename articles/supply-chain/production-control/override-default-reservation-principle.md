---
title: Het standaardreserveringsprincipe voor materialen in de productie overschrijven
description: In dit onderwerp wordt beschreven hoe u een standaardreserveringsprincipe instelt voor elke artikelmodelgroep, zodat verschillende reserveringsprincipes automatisch kunnen worden toegepast voor elk artikel dat deel uitmaakt van een productiestuklijst of batchorderformule.
author: johanhoffmann
manager: tfehr
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2391ec11bd497c69ddb19e29533f5441d7374877
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501097"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Het standaardreserveringsprincipe voor materialen in de productie overschrijven

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Met de functie *Standaardproductiereservering overschrijven* kunt u een standaardreserveringsprincipe instellen voor elke artikelmodelgroep. Daarom kunnen er automatisch verschillende reserveringsprincipes worden toegepast voor elk artikel dat deel uitmaakt van een productiestuklijst of batchorderformule. U kunt selecteren of elke artikelmodelgroep voorbij moet gaan aan het standaardreserveringsprincipe dat voor een order is ingesteld, en u kunt in plaats daarvan instellen welk reserveringsprincipe moet worden gebruikt (*handmatig*, *raming*, *planning*, *vrijgave* of *begin*).

Wanneer u een nieuwe productieorder of batchorder maakt, wordt u gevraagd het reserveringsprincipe te selecteren dat op de order en alle stuklijst- of formuleregels moet worden toegepast. Wanneer de functie *Standaardproductiereservering overschrijven* wordt gebruikt, kunnen sommige of alle stuklijstregels of formuleregels voorbij gaan aan dat reserveringsprincipe en in plaats daarvan het reserveringsprincipe gebruiken dat is ingesteld voor de relevante artikelmodelgroep.

Als u bijvoorbeeld grondstoffen of ingrediënten hebt waarvoor orderverzameling is vereist, is voor de stuklijst- of formuleregels die voor deze producten worden gemaakt een fysieke reservering vereist, omdat fysieke reservering een vereiste is voor het genereren van magazijnwerk. Normaal gesproken kunt u, als u wilt dat de reservering automatisch wordt uitgevoerd, een van de volgende reserveringsprincipes selecteren: *raming*, *planning*, *vrijgave* of *begin*. Als u echter materialen of ingrediënten hebt waarvoor geen orderverzameling is vereist, omdat ze direct vanaf een locatie worden verbruikt, selecteert u doorgaans het *handmatige* reserveringsprincipe, waarmee geen fysieke reserveringen worden gemaakt of orderverzameling wordt gegenereerd.

## <a name="turn-on-the-feature"></a>De functie inschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Productiebeheer*
- **Functienaam**: *(Preview) Standaardproductiereservering overschrijven*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Een productiereserveringsbeleid toewijzen aan een artikelmodelgroep

1. Ga naar **Kostenbeheer \> Instelling voor boekhoudingbeleid voorraad \> Artikelmodelgroepen**.
1. Maak of selecteer een artikelmodelgroep.
1. Schakel op het sneltabblad **Voorraadbeleid** het selectievakje **Productiereservering artikel overschrijven** in.
1. Selecteer in het veld **Reservering** het reserveringsprincipe voor artikelen die bij de geselecteerde modelgroep horen. (De artikelen bevatten artikelen op een stuklijst- of formuleregel.)

    - **Handmatig**: artikelen in de modelgroep worden niet automatisch fysiek gereserveerd voor productie. Ze kunnen echter nog steeds handmatig worden gereserveerd.
    - **Raming**: artikelen in de modelgroep worden fysiek gereserveerd tijdens de raming van de productieorder.
    - **Planning**: artikelen in de modelgroep worden fysiek gereserveerd tijdens de planning van de productieorder.
    - **Vrijgave**: artikelen in de modelgroep worden fysiek gereserveerd wanneer de productieorder wordt vrijgegeven.
    - **Begin**: artikelen in de modelgroep worden fysiek gereserveerd aan het begin van de productieorder.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Voorbeeld: reserveringsprincipes gebruiken in een bulk-/verpakkingsscenario

Er wordt bulkmateriaal voor smeer geproduceerd in een mixer van 1000 liter. Nadat het bulkmateriaal klaar is, wordt het via verschillende vulstations in flessen van verschillende grootten gepompt. Nadat het vullen is voltooid, worden de flessen verpakt in dozen. Deze dozen worden vervolgens op pallets verpakt.

In dit scenario wordt er een batchorder gemaakt waarin 1000 liter bulkmateriaal wordt gemaakt. (Dit is de bulkorder.) Wanneer deze batchorder is voltooid, wordt deze gereed gemeld op de materiaalinvoerlocatie van de vulstations. Er wordt vervolgens een batchorder gemaakt om elke flesgrootte te vullen en te verpakken. (Deze orders zijn de verpakkingsorders.) De verpakkingsorders hebben een formule die bestaat uit het bulkmateriaal, een lege fles, een label en andere verpakkingsmaterialen. Omdat het bulkmateriaal direct vanaf de mengtank naar de vulstations stroomt, is er geen magazijnwerk vereist om dit ingrediënt te verzamelen en wordt het bulkmateriaal direct vanaf de invoerlocatie verbruikt. Daarom wordt het reserveringsprincipe ingesteld op *handmatig*. De andere materialen worden via orderverzameling klaargezet voor het vulstation. Daarom wordt het reserveringsprincipe voor deze regels ingesteld op *vrijgave*, zodat bijvoorbeeld de reservering automatisch plaatsvindt wanneer de verpakkingsorder wordt vrijgegeven.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]