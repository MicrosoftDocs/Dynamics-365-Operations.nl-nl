---
title: Het eigendom van consignatievoorraad wijzigen op basis van de productievraag
description: Deze procedure laat zien hoe u de eigenaar van de consignatievoorraad wijzigt van de leverancier in uw rechtspersoon wanneer er vraag is naar de voorraad in productie.
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5925f5423d596adc4326dfff4734de2afd80b5a8
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Het eigendom van consignatievoorraad wijzigen op basis van de productievraag

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u de eigenaar van de consignatievoorraad wijzigt van de leverancier in uw rechtspersoon wanneer er vraag is naar de voorraad in productie. Deze wijziging van eigendom wordt uitgevoerd door een wijzigingslogboek van het voorraadeigendom te maken en te boeken. De regels van het eigendomwijzigingslogboek kunnen handmatig worden gemaakt of, zoals deze opname laat zien, worden gebaseerd op de bestaande productievraag. Gewoonlijk voert een werkvloersupervisor deze taak uit. U kunt deze procedure gebruiken in het demobedrijf USMF of voor uw eigen gegevens. Als u uw eigen gegevens gebruikt, moet u voldoen aan de volgende vereisten: een voorraadjournaalnaam die is ingesteld voor de wijziging van het voorraadeigendom, fysiek geregistreerde voorhanden artikelen in het bezit van de leverancier, en een of meer productieorderregels voor het materiaal. Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="create-an-inventory-ownership-journal"></a>Een voorraadeigendomsjournaal maken
1. Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Wijziging aan voorraadeigendom.
2. Klik op Nieuw.
    * Het wijzigingslogboek van het voorraadeigendom wordt gebruikt om de eigenaar van consignatievoorraad van de leverancier te wijzigen in de huidige rechtspersoon. Deze wijziging van eigendom wordt uitgevoerd door de voorhanden voorraad vrij te geven die eigendom is van de leverancier en die voorraad vervolgens te ontvangen voor de huidige rechtspersoon.  
3. Typ of selecteer een waarde in het veld Naam.
    * U kunt alleen voorraadjournaalnamen selecteren die het journaaltype Wijziging aan eigendom hebben.  
4. Klik op OK.
5. Klik op Functies.
6. Klik op Journaalregels maken op basis van productieorders.
    * U kunt de wijziging van het eigendomproces starten door alle productieregels te zoeken met vraag naar verbruik van grondstoffen.  
7. Selecteer een optie in het veld Op te nemen voorraaduitgiftestatussen.
    * Met deze optie kunt u filteren op de uitgiftestatus van de voorraadtransacties. U kunt bijvoorbeeld journaalregels maken voor voorraad met de status Verzameld en fysiek gereserveerd.  
8. Breid de sectie Op te nemen records uit.
    * In deze sectie kunt u aanvullende filterbewerkingen toepassen. U kunt bijvoorbeeld een specifieke grondstoffendatum selecteren.  
9. Klik op OK.

## <a name="post-the-inventory-ownership-change-journal"></a>De wijzigingen in het voorraadeigendomsjournaal boeken
1. Klik op Boeken.
    * Wanneer het journaal wordt geboekt, wordt de voorraad die in het bezit is van de leverancier vrijgegeven door een verwijzing voor Wijziging aan eigendom. Vervolgens wordt de voorraad ontvangen als voorhanden voorraad met een voorraadtransactie die met een inkooporderproductontvangstbon wordt bijgewerkt. Merk op dat alleen transacties worden gemaakt die samenhangen met het geboekte journaal. Er worden geen verwachte voorraadtransacties gegenereerd.  
2. Klik op OK.
3. Sluit de pagina.

