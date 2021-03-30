---
title: Het eigendom van consignatievoorraad wijzigen op basis van de productievraag
description: Deze procedure laat zien hoe u de eigenaar van de consignatievoorraad wijzigt van de leverancier in uw rechtspersoon wanneer er vraag is naar de voorraad in productie.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 508226a3b5693b123af639cf6f130be07811c3c2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209510"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Het eigendom van consignatievoorraad wijzigen op basis van de productievraag

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u de eigenaar van de consignatievoorraad wijzigt van de leverancier in uw rechtspersoon wanneer er vraag is naar de voorraad in productie. Deze wijziging van eigendom wordt uitgevoerd door een wijzigingslogboek van het voorraadeigendom te maken en te boeken. De regels van het eigendomwijzigingslogboek kunnen handmatig worden gemaakt of, zoals deze opname laat zien, worden gebaseerd op de bestaande productievraag. Gewoonlijk voert een werkvloersupervisor deze taak uit. U kunt deze procedure gebruiken in het demobedrijf USMF of voor uw eigen gegevens. Als u uw eigen gegevens gebruikt, moet u voldoen aan de volgende vereisten: een voorraadjournaalnaam die is ingesteld voor de wijziging van het voorraadeigendom, fysiek geregistreerde voorhanden artikelen in het bezit van de leverancier, en een of meer productieorderregels voor het materiaal. Deze procedure is voor een functie die in Dynamics 365 for Operations, versie 1611 is toegevoegd.

> [!NOTE]
> Uitgaande zendingsprocessen worden niet out-of-the-box ondersteund en de verwerking van de automatische eigendomsjournalen wordt niet ondersteund.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]